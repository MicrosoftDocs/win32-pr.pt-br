---
title: DuplicateSiblingNames
description: DuplicateSiblingNames
ms.assetid: 4E9FFD16-EAC0-4778-8DEB-D179E2197411
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aed5a7caeadc34519988fe8a4a1f12ec4e05ce13
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103637239"
---
# <a name="duplicatesiblingnames"></a>DuplicateSiblingNames

## <a name="text"></a>Texto

O nome irmão duplicado + role "" causará \\ {0} \\ ambiguidade entre os elementos.

## <a name="type"></a>Type

Erro

## <a name="description"></a>Descrição

Um elemento tem o mesmo nome e função/ControlType que outro elemento.

Esse problema pode causar confusão porque os leitores de tela lerám o mesmo texto para todos os elementos com o mesmo nome e função/ControlType.

## <a name="possible-causes"></a>Possíveis causas

-   O nome do elemento contém texto role/ControlType.
-   O nome do elemento ou o nome de seu pai não está definido ou está definido incorretamente.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IAccessible:: obter \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)
</dt> <dt>

[Propriedade Name](name-property.md)
</dt> <dt>

[**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)
</dt> <dt>

[**IUIAutomationElement. CurrentName**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname)
</dt> </dl>

 

 




