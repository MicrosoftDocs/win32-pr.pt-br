---
title: Exemplo de arte simples
description: Exemplo de arte simples
ms.assetid: e17c29c3-3bc6-43f5-83e1-94005218417f
keywords:
- Windows Media Player capas, arquivos de arte
- capas, arquivos de arte
- arquivos para capas, arte
- arquivos de arte para capas, exemplos
- aparências de Windows Media Player, exemplos
- capas, exemplos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bbd50cb4ad0dbd76babd99439a885f9e77557d04e18f2698bb970effa23d6b7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119615909"
---
# <a name="simple-art-example"></a>Exemplo de arte simples

Três arquivos Art são necessários para criar uma aparência simples com dois botões. Uma imagem primária e uma imagem de mapeamento são necessárias e uma imagem alternativa fornece uma indicação visual para o usuário de que um botão é clicável.

Esses arquivos de arte foram criados em um programa de arte que usa camadas. O uso de camadas facilita a tarefa de garantir que suas imagens primárias, de mapeamento e alternativas tenham o mesmo tamanho e fiquem alinhadas umas com as outras.

As instruções detalhadas sobre como criar a arte estão no [Guia de criação de capas](skin-creation-guide.md).

## <a name="primary-image"></a>Imagem primária

a imagem primária é uma elipse amarela simples com dois botões, um rosa para iniciar Windows Media Player e o botão roxo para interrompê-lo. O plano de fundo é um pouco mais escuro amarelo do que o oval. Essa imagem é mostrada na ilustração a seguir.

![imagem primária](images/absam01b.png)

A imagem primária era das imagens a seguir, cada uma em uma camada separada. Primeiro, uma oval foi criada com um efeito de bisel de camada e de entalhe. Essa imagem é mostrada na ilustração a seguir.

![imagem oval](images/absam01s.png)

Em seguida, os dois botões foram criados, também com efeitos de chanfro de camada e de entalhe. Isso é mostrado na ilustração a seguir.

![dois botões](images/absam01p.png)

Em seguida, o plano de fundo da imagem foi criado. Um amarelo ligeiramente mais escuro foi escolhido para que qualquer suavização entre a oval e o plano de fundo não seja notado. O valor de cor é \# CCCC00. Essa imagem é mostrada na ilustração a seguir.

![imagem de plano de fundo](images/absam01y.png)

As camadas que continham essas imagens foram tornadas visíveis e salvas como uma cópia no formato de bitmap, criando a imagem primária. A imagem composta primária será usada pelo atributo **backgroundImage** do elemento **View** .

## <a name="mapping-image"></a>Imagem de mapeamento

Uma imagem de mapeamento é necessária para especificar quando e onde uma capa é clicada. Uma imagem de mapeamento foi criada com uma área vermelha e uma área verde. Essa imagem é mostrada na ilustração a seguir.

![imagem de mapeamento](images/absam01m.png)

a área verde será usada para identificar a área na capa que será iniciada Windows Media Player e a área vermelha será usada para interrompê-la. A imagem de mapeamento tem o mesmo tamanho da imagem primária.

A imagem de mapeamento foi criada copiando a camada de botão para uma nova camada e desativando o efeito de bisel e entalhe. as imagens simples são necessárias para mapeamento porque Windows Media Player procurará por valores de cor únicos em cada área. Ele só pode pesquisar por uma cor que você definir, como vermelho ( \# FF0000). Se a imagem tiver um chanfro ou outro efeito, nem todos eles serão o vermelho exato de que você precisa.

Para tornar os botões de mapeamento uma cor fácil de se lembrar, as imagens foram preenchidas com vermelho puro e verde puro, mas qualquer cor pode ser usada. Você precisará se lembrar dos números de cor em seu mapa para que eles possam ser inseridos no arquivo de definição de aparência XML. Nesse caso, Red é \# FF0000 e Green é \# 00FF00.

Em seguida, com apenas a nova camada visível, a imagem foi salva como uma cópia em um arquivo BMP. Ele será chamado pelo atributo **mappingImage** do elemento **Button** .

## <a name="alternate-image"></a>Imagem alternativa

Imagens alternativas não são necessárias, mas são muito úteis para dar indicações visuais ao usuário. Nesse caso, uma imagem em foco é recomendada para que o usuário saiba em quais áreas podem ser clicadas.

Uma imagem alternativa foi criada com dois botões amarelos. Isso é mostrado na ilustração a seguir.

![imagem em foco](images/absam01h.png)

A imagem alternativa foi criada copiando a camada do botão original para uma nova camada e, em seguida, alterando a cor de preenchimento para amarelo. O efeito de bisel e entalhe foi mantido. Em seguida, uma nova camada foi criada e as imagens foram adicionadas: a seta indica "Play" e o quadrado indica "Stop". Em seguida, com apenas o novo botão amarelo e as camadas de tipo visíveis, a imagem foi salva como uma cópia em um arquivo de bitmap.

O resultado é que quando o mouse passa sobre uma área definida pela imagem de mapeamento, a imagem em foco será exibida, alertando o leitor de que, se clicarem nesse ponto, poderão reproduzir ou parar Windows Media Player.

## <a name="final-image"></a>Imagem final

Aqui está a imagem final da capa.

![imagem final](images/absam01f.png)

Essa é a imagem que você verá se passar o mouse sobre o botão rosa à direita.

![passar o mouse sobre o botão direito](images/absam01r.png)

## <a name="xml-code-for-the-art-example"></a>Código XML para o exemplo de arte

Os detalhes de como escrever código XML são fornecidos no guia de [criação de capa](skin-creation-guide.md), mas para mostrar o quanto o código é necessário para criar uma aparência de trabalho, aqui está o código para o trabalho artístico neste exemplo.

Botões predefinidos são usados para as funções Play e Stop. você deve carregar um arquivo ou uma lista de reprodução da âncora de mídia Windows. quando Windows Media Player muda para o modo de capa, uma pequena caixa é exibida no canto inferior direito da tela. Essa caixa é chamada de "âncora". Clicar na âncora oferece a funcionalidade mínima necessária, caso uma capa não forneça uma maneira de retornar ao modo completo de Windows Media Player. O usuário pode alternar entre os modos usando o menu **Exibir** se estiver em modo completo ou clicando na âncora se estiver no modo de capa.


```C++
<THEME>
    <VIEW
        clippingColor = "#CCCC00"
        backgroundImage = "background.bmp"
        titleBar = "false">
         
        <BUTTONGROUP
            mappingImage = "map.bmp"
            hoverImage = "hover.bmp">
                
        <PLAYELEMENT
            mappingColor = "#00FF00"/>

        <STOPELEMENT
            mappingColor = "#FF0000"/>
                
        </BUTTONGROUP>
    </VIEW>
</THEME>

```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Arquivos de arte**](art-files.md)
</dt> </dl>

 

 




