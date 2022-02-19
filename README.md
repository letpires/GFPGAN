<p align="center">
  <img src="https://github.com/letpires/GFPGAN/blob/main/photo.png" >
</p>

<h2 align="center">
  O que são GANs? E como usar GFP-GAN pra melhorar uma foto? 
</h2>

[Nesse vídeo](https://www.youtube.com/watch?v=DsrfCIXaRio&ab_channel=Let%C3%ADciaPires) eu vou mostrar para vocês o que são as Redes Adversárias Generativas (GANs) e como converter uma imagem borrada em imagem de qualidade com GFP-GAN, como na imagem acima.

## 🧠 O que são as GANs?

GAN é uma classe da Inteligência Artificial que trabalha com geração de conteúdo que, ao ser analisado, pode facilmente enganar, deixando incerto se é real (produzido por humanos) ou falso (produzido pela rede). Esta técnica foi inventada por Ian Goodfellow, junto de seus colegas, em 2014, e, em síntese, é constituída de 2 componentes principais: o discriminador e o gerador. Ambos, discriminador e gerador, são redes que possuem responsabilidades diferentes. O discriminador é uma rede responsável por avaliar se um determinado conteúdo é real. O gerador possui a responsabilidade de produzir o conteúdo em si. 
Imagine duas redes neurais competindo entre si. Uma delas produz imagens artificiais e a outra tem o papel de decidir se uma dada imagem é verdadeira ou falsa. 

## 👮 Explicando com analogia ao dinheiro, banco e ladrão:

<p align="center">
  <img src="https://github.com/letpires/GFPGAN/blob/main/analogia.png" >
</p>

O gerador vai produzir dinheiro FALSO e o banco produz o dinheiro REAL. As duas notas irão passar pelo discriminador, e ele vai dizer se é uma nota verdadeira ou falsa.

- O gerador (falsificador) é treinado para criar notas de dólares falsas indistinguíveis (o mais próximas possiveis) das notas reais (geradas pelo banco);
- O discriminador (policial) é treinado para determinar se o dinheiro é real ou falsificado;
- O falsificador tenta enganar a polícia, convencendo-o de que a nota que ele gerou é verdadeira;
- O discriminador detectará dinheiro falso e proverá feedback para o gerador, indicando porquê a nota foi considerada falsa - essa nota falsa colocar marca dagua, a cor tem que ser diferente...
- Com o tempo, o gerador ficará especialista em gerar dinheiro que são indistinguiveis das notas reais e o discriminador não conseguirá mais indicar que são notas falsas.
- Aprendem sobre as caracteristicas dos objetos para criar suas próprias imagens;
- O gerador gera imagens e o discriminador compara essas novas imagens (que são falsas) com as imagens reais (verdadeiras) que estão na base de dados de treinamento;
- As duas redes redes neurais aprendem sozinhas até que o gerador torne-se um especialista em gerar novas imagens que são indistinguíveis das imagens reais.

O pré-treinamento permite que o modelo opere de maneira supervisionada, usando uma grande quantidade de dados sobre temas específicos para sua aprendizagem. Ou seja, podemos dizer que a inteligência artificial pré-treinada conta com um sistema já existente, criado para resolver um problema semelhante.

## 📸 O que é a GFP-GAN e como utilizar?

Bom, eu vou mostrar uma ferramenta de GAN pré-treinada que conheci e achei bem interessante, que é o GFP-GAN, que ajuda a restaurar imagens faciais e aprimorá-las se estiver embaçada.

O modelo GFP-GAN para Restauração de Face Cega retém a Qualidade da Imagem e restaura as características faciais presentes na imagem melhor do que os modelos tradicionalmente usados presentes.

O GFP-GAN vem pré-treinado no conjunto de dados FFHQ, que consiste em cerca de 70.000 imagens de alta qualidade. Todas as imagens foram redimensionadas para 5122 durante o treinamento. O GFP-GAN é treinado em dados sintéticos que aproximam imagens reais de baixa qualidade e generalizam para imagens do mundo real durante a síntese de saída de inferência (dedução feita com base em informações).

Afim de teste, eu apliquei a ferramenta em uma foto minha de quando era criança que continha ruído e desfoque.

- A documentação do projeto e ferramenta vocês podem encontrar [nesse link](https://xinntao.github.io/projects/gfpgan)
- O repositório da ferramenta está [nesse link](https://github.com/TencentARC/GFPGAN)
- O banco de dados utilizado para inferência é o FFHQ, e pode ser acessado [nesse link](https://github.com/NVlabs/ffhq-dataset)
- Aqui etá o código que eu gerei no [Google Colab](https://github.com/letpires/GFPGAN/blob/main/GFPGAN.ipynb)
- E por fim, caso não queira utilizar código, pode usar essa [INTERFACE](https://refineryai.com/) que utiliza o GFP-GAN por trás, para corrigir suas fotos.

---

**Não esqueçam de deixar o like e se inscrever no meu [canal do Youtube](https://www.youtube.com/channel/UC7C3taM54q4rsEIDPFNVsLg) 💜**
