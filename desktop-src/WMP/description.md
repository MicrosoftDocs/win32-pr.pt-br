---
title: Descrição (Windows Media Player SDK)
description: Descrição
ms.assetid: 940ef0bf-d651-411a-b36d-99dcc01d8508
keywords:
- Windows Media Player Capas móveis, seção Descrição
- skins, seção Descrição
- referência para capas, seção Descrição
- Seção de descrição em capas
- arquivos de definição de capa, seção Descrição
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 486ca5235939352ffabb924aaf38a706b436d4c1358a92b9aef4996614c53623
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117749953"
---
# <a name="description-windows-media-player-sdk"></a>Descrição (Windows Media Player SDK)

Ao criar uma capa para o Windows Media Player Série 9 para Windows Mobile 2003 ou posterior, você deve incluir uma seção Descrição. A seção Descrição permite que você especifique a largura e a altura da exibição, a resolução de exibição e a orientação de exibição para a qual a capa foi projetada. A seção Descrição deve aparecer no arquivo de definição de capa antes de qualquer outra seção e logo após a declaração de versão inicial.

A seção Descrição do arquivo de definição de capa deve começar com a seguinte linha:


```C++
[ Description ]

```



Em seguida, você deve adicionar informações sobre as dimensões da capa e a resolução de exibição. O exemplo a seguir mostra como especificar dimensões:


```C++
//              <X,Y>       <DPI>

//              -------     -----

    Dimensions  240,320      96

```



Isso especifica que você criou a capa para ser exibida com 240 pixels de largura, 320 pixels de altura e usando resolução de exibição de 96 DPI. Observe que isso implica uma orientação de modo retrato.

Opcionalmente, você pode especificar o modo de orientação para o qual você criou a capa na seção de descrição. O exemplo a seguir mostra como especificar a orientação:


```C++
//     <Orientation>

//     -------------

    Orientation Portrait

```



A tabela a seguir lista os valores que você pode usar para Orientação.



| Orientação | Descrição                                                                                                  |
|-------------|--------------------------------------------------------------------------------------------------------------|
| Paisagem   | A largura da capa é maior que a altura da capa. A exibição é orientada de maneira horizontal.   |
| Retrato    | A altura da capa é maior que a largura da capa. A exibição é orientada de maneira vertical. |
| Square      | A altura da capa é igual à largura da capa. A exibição não tem orientação.                    |



 

> [!Note]  
> Windows Media Player Série 9 para Windows Mobile 2003 exibirá apenas uma capa específica quando a seção de descrição especificada no arquivo de definição de capa corresponde ao estado atual do dispositivo.

 

Você deve ter cuidado para sempre especificar as dimensões, a resolução e a orientação corretas para as quais sua capa foi autorada. Por exemplo, se as dimensões especificadas pela sua capa descreverem uma orientação paisagem, sua capa não estará disponível quando o dispositivo estiver no modo retrato, mesmo se você especificar Retrato na linha de orientação.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Referência de capa**](skin-reference.md)
</dt> </dl>

 

 




