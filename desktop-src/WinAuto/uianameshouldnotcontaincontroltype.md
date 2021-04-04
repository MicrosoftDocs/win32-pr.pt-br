---
title: UiaNameShouldNotContainControlType
description: UiaNameShouldNotContainControlType
ms.assetid: 96F7A5FC-1879-4706-9E67-5B43D57F7281
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6178ca4cd4c4b2ed0deb0070116b597ba3bd1bc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822479"
---
# <a name="uianameshouldnotcontaincontroltype"></a>UiaNameShouldNotContainControlType

## <a name="text"></a>Texto

O nome do elemento ( {0} ) não deve conter o texto do ControlType ( {1} )

## <a name="type"></a>Tipo

Aviso

## <a name="description"></a>Descrição

O nome de um elemento incorpora seu tipo de controle UIA. Por exemplo, esse aviso pode ocorrer se a propriedade de nome UIA de um elemento com o tipo de controle de botão estiver definida como "meu botão".

Esse problema causa problemas para as pessoas que contam com um leitor de tela e um teclado para navegação porque o tipo de controle será lido duas vezes ou pode ser inpronunciado ou não intuitivo para os usuários.

## <a name="possible-causes"></a>Possíveis causas

-   O elemento ou seu pai tem um nome ou rótulo atribuído incorretamente.
-   O elemento ou seu pai tem um nome padrão que não foi revisado para um nome amigável. Por exemplo, Button1.
-   Um desenvolvedor não está ciente de que leitores de tela lêem nomes e tipos de controle.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)
</dt> <dt>

[**IUIAutomationElement:: CurrentName**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname)
</dt> </dl>

 

 




