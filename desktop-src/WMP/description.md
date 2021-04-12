---
title: Descrição (SDK do Windows Media Player)
description: Descrição
ms.assetid: 940ef0bf-d651-411a-b36d-99dcc01d8508
keywords:
- Capas móveis do Windows Media Player, seção Descrição
- capas, seção de descrição
- referência para capas, seção de descrição
- Seção de descrição em capas
- arquivos de definição de capa, seção de descrição
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4a1b714fb917f9d13ee710509cfc5bf696e3eef
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104369126"
---
# <a name="description-windows-media-player-sdk"></a>Descrição (SDK do Windows Media Player)

Ao criar uma capa para o Windows Media Player 9 Series para Windows Mobile 2003 ou posterior, você deve incluir uma seção de descrição. A seção Descrição permite que você especifique a largura e a altura da exibição, a resolução de vídeo e a orientação de exibição para a qual a capa foi projetada. A seção descrição deve aparecer no arquivo de definição de capa antes de qualquer outra seção e logo após a declaração de versão inicial.

A seção de descrição do arquivo de definição de capa deve começar com a seguinte linha:


```C++
[ Description ]

```



Em seguida, você deve adicionar informações sobre as dimensões da capa e a resolução da tela. O exemplo a seguir mostra como especificar dimensões:


```C++
//              <X,Y>       <DPI>

//              -------     -----

    Dimensions  240,320      96

```



Isso especifica que você criou a capa a ser exibida em 240 pixels de largura, 320 pixels de altura e usando a resolução de vídeo de 96 DPI. Observe que isso implica em uma orientação de modo retrato.

Opcionalmente, você pode especificar o modo de orientação para o qual você criou a capa na seção Descrição. O exemplo a seguir mostra como especificar a orientação:


```C++
//     <Orientation>

//     -------------

    Orientation Portrait

```



A tabela a seguir lista os valores que você pode usar para orientação.



| Orientação | Descrição                                                                                                  |
|-------------|--------------------------------------------------------------------------------------------------------------|
| Paisagem   | A largura da capa é maior que a altura da capa. A exibição é orientada de maneira horizontal.   |
| Retrato    | A altura da capa é maior que a largura da capa. A exibição é orientada em uma maneira vertical. |
| Square      | A altura da capa é igual à largura da capa. A exibição não tem orientação.                    |



 

> [!Note]  
> O Windows Media Player 9 Series para Windows Mobile 2003 exibirá apenas uma determinada capa quando a seção de descrição especificada no arquivo de definição de capa corresponder ao estado atual do dispositivo.

 

Você deve ter cuidado para sempre especificar as dimensões, a resolução e a orientação corretas para as quais sua capa foi criada. Por exemplo, se as dimensões especificadas pela sua capa descreverem uma orientação paisagem, sua capa não estará disponível quando o dispositivo estiver no modo retrato, mesmo se você especificar retrato na linha de orientação.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Referência de capa**](skin-reference.md)
</dt> </dl>

 

 




