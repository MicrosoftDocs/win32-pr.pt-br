---
title: DuplicateSiblingIDs
description: DuplicateSiblingIDs
ms.assetid: 942385A4-BD14-4046-9ABC-110B32D96BB6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddd9bb311d4aafdf1f509d3404cfe057f96f6bf378b822f6f77cab4943cea097
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118115353"
---
# <a name="duplicatesiblingids"></a>DuplicateSiblingIDs

## <a name="text"></a>Texto

A ID de automação duplicada "" causará \\ {0} \\ ambiguidade entre os elementos.

## <a name="type"></a>Tipo

Erro

## <a name="description"></a>Descrição

Um elemento tem a mesma ID de automação que outro elemento.

Esse problema pode causar problemas de automação que impedem o código de teste de referenciar o elemento correto.

## <a name="possible-causes"></a>Possíveis causas

-   Elementos irmãos têm a mesma ID de automação.
-   Implementação incorreta da propriedade UIA AutomationId.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)
</dt> <dt>

[**IUIAutomationElement.CurrentAutomationId**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentautomationid)
</dt> </dl>

 

 




