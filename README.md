# Detecção de capacetes em motociclistas e ciclistas
Trabalho final da disciplina INE410121 - Visão Computacional (UFSC) 

Desenvolvimento de ferramenta para detecção de capacetes em diversos contextos utilizando técnicas clássicas e modernas de visão computacional.
A abordagem é feita utilizando HOG e a abordagem moderna é feita utilizando YOLO.

Este repositório foi desenvolvido pelo Grupo 04:
* Gustavo Batista
* Laura Fiorini
* Leonardo Leite
* Maurício Salvador

## Descrição do projeto

O desenvolvimento do um projeto de visão computacional em questão tem como objetivo identificar motoqueiros e ciclistas que estão andando com ou sem capacete de segurança. A intenção é identificar infrações de trânsito e prevenir possíveis acidentes. A utilização de capacetes é essencial para a segurança dos condutores, e a automação desse processo de identificação pode aumentar a eficiência da fiscalização.

Para alcançar esse objetivo, foram utilizadas duas abordagens diferentes de visão computacional: um modelo clássico e um modelo moderno.

### Modelo Clássico: HOG (Histograma de Gradientes Orientados)
Inicialmente, aplicou-se o método HOG, uma técnica tradicional de visão computacional que analisa os gradientes de orientação de imagem. O HOG é conhecido por sua capacidade de detectar objetos e formas em imagens, sendo amplamente utilizado para detecção de pedestres e reconhecimento de rostos.

Entretanto, nesse projeto, o HOG não apresentou resultados satisfatórios. Ele enfrentou dificuldades significativas para identificar consistentemente os rostos e capacetes dos motoqueiros e ciclistas. Provavelmente a variabilidade nas poses, iluminação e ângulos das imagens dificultou a eficiência do HOG, resultando em muitas falhas na detecção e classificações incorretas.

### Modelo Moderno: YOLO (You Only Look Once)
Devido às limitações do HOG, optou-se por utilizar uma abordagem mais moderna: a rede neural YOLO, especificamente as versões YOLOv5 e YOLOv10. A YOLO é uma das técnicas mais avançadas para detecção de objetos, reconhecida por sua alta precisão e velocidade.

A YOLO se mostrou extremamente eficaz para este projeto. Tanto o YOLOv5 quanto o YOLOv10 foram capazes de identificar com precisão motoqueiros e ciclistas, distinguindo aqueles que usavam capacetes dos que não usavam. No entanto, o YOLOv10 apresentou um desempenho ainda melhor que o YOLOv5, oferecendo resultados mais precisos e consistentes na identificação.

### Dados Utilizados
Os dados utilizados para treinar, testar e validar os modelos foram obtidos a partir da junção de dois datasets do Kaggle. A integração desses conjuntos de dados permitiu a criação de um dataset mais diversificado e robusto, contendo uma ampla variedade de imagens que abrangem diferentes cenários, poses e condições de iluminação.

* [Dataset 1: Rider, With Helmet, Without Helmet, Number Plate](https://www.kaggle.com/datasets/aneesarom/rider-with-helmet-without-helmet-number-plate)
* [Dataset 2: Helmet Detection](https://www.kaggle.com/datasets/andrewmvd/helmet-detection)

### Conclusão
Através da comparação entre o modelo clássico HOG e o moderno YOLO, ficou evidente a superioridade da rede YOLO para o propósito de identificar capacetes em motoqueiros e ciclistas. O uso de técnicas avançadas de redes neurais, juntamente com um dataset robusto, possibilitou a criação de um sistema eficaz e confiável para a detecção de infrações de trânsito relacionadas ao uso de capacetes. Entre as versões avaliadas, o YOLOv10 destacou-se pelo desempenho superior em comparação ao YOLOv5.

