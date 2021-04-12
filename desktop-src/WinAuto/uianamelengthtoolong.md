---
title: UiaNameLengthTooLong
description: UiaNameLengthTooLong
ms.assetid: 01AF3F1E-9A3F-48B4-8219-6E80BAFC82EE
keywords:
- UIA_NamePropertyId do identificador AutomationElement. NameProperty
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ab786b7167dab4a25384ce3abe2509babcf1f82
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364343"
---
# <a name="uianamelengthtoolong"></a>UiaNameLengthTooLong

## <a name="text"></a>Texto

O nome do elemento não deve retornar uma cadeia de caracteres com mais de um {0} caractere

## <a name="type"></a>Tipo

Erro

## <a name="description"></a>Descrição

O nome de um elemento contém muitos caracteres. Por exemplo, o método [**IUIAutomationElement:: CurrentName**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname) usado para recuperar o nome UIA de um elemento retorna uma cadeia de caracteres maior que o limite.

Esse problema causa problemas para as pessoas que contam com um leitor de tela e um teclado para navegação porque um elemento pode ter um nome não-pronunciado e não intuitivo.

## <a name="possible-causes"></a>Possíveis causas

O elemento ou seu pai tem um nome ou rótulo atribuído incorretamente.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)
</dt> <dt>

[**IUIAutomationElement:: CurrentName**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname)
</dt> </dl>

 

 




