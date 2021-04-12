---
title: Marquee
description: Marquee
ms.assetid: 2715732a-25cc-4ba9-9aa6-181ebb9e1d1c
keywords:
- Aparências móveis do Windows Media Player, letreiros
- capas, letreiros
- referência para capas, letreiros
- marcas de aparência em capas, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7efa2db2c6079d47d207240b18a57ebbf7e41ae1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364232"
---
# <a name="marquee"></a>Marquee

Um letreiro é uma caixa de exibição de texto de rolagem que exibe informações de uma ou mais caixas de exibição de texto. Você não precisa adicionar um letreiro, mas ele pode ser muito útil quando você tem informações detalhadas que deseja exibir para o usuário em um espaço limitado.

O texto no letreiro será rolado somente se ambas as condições a seguir forem atendidas:

-   Você tem mais texto a ser exibido no letreiro do que a largura da caixa de exibição do letreiro digital.
-   O item de mídia foi interrompido ou pausado.

A seção de letreiro do arquivo de definição de capa deve começar com esta linha:


```C++
[ Marquee ]

```



> [!Note]  
> Para manter a compatibilidade com versões do Windows Media Player Mobile anteriores ao Windows Media Player 10 Mobile, o uso de "Marquis" em um arquivo de definição de capa ainda é considerado válido.

 

Em seguida, você deve adicionar uma ou mais linhas que contêm informações sobre cada uma das caixas de exibição do letreiro em sua capa.


```C++
    3,2,234,20   Tahoma,12,N  255,0,0    Playlist, Time, Filename

```



Você pode usar o modelo a seguir para a seção de letreiro de seu arquivo de definição de capa:


```C++
//  <Location>   <Font>       <Color>      <Text item combinations>
//  ----------   ------       -------      ------------------------

```



Você deve usar a seguinte ordem para obter informações em cada linha da seção de letreiro (cada parte da linha é necessária):

1.  [Local do letreiro](marquee-location.md)
2.  [Fonte do letreiro](marquee-font.md)
3.  [Cor do letreiro](marquee-color.md)
4.  [Combinações de texto](text-combinations.md)

Para obter um exemplo de código de letreiro, consulte a [seção letreiro de exemplo](sample-marquee-section.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Referência de capa**](skin-reference.md)
</dt> </dl>

 

 




