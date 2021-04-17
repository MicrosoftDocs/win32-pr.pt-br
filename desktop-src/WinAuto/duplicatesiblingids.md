---
title: DuplicateSiblingIDs
description: DuplicateSiblingIDs
ms.assetid: 942385A4-BD14-4046-9ABC-110B32D96BB6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27ba2ccca45234bb49fc782c5522b4e446d77a2c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105765650"
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

 

 




