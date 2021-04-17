---
title: Os elementos DragPattern/DragDropPattern exigem o nome
description: Os elementos DragPattern/DragDropPattern exigem o nome
ms.assetid: DEF58FB2-5830-4162-87D0-40DEC1237529
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ecc60eeca59f4754f9c160696cdfa2556c36a5e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105772992"
---
# <a name="dragpatterndragdroppattern-elements-requires-name"></a>Os elementos DragPattern/DragDropPattern exigem o nome

## <a name="text"></a>Texto

Elementos que oferecem suporte a arrastar/soltar devem ter um ' name ' válido definido

## <a name="type"></a>Tipo

Erro

## <a name="description"></a>Descrição

O elemento dá suporte a [**IUIAutomationDragPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdragpattern) ou a [**IUIAutomationDropTargetPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdroptargetpattern), mas não tem um nome válido definido.

Esse problema causa problemas para as pessoas que dependem de um leitor de tela. O usuário não conseguirá dizer qual é esse objeto, pois a tela de leitura não lerá um nome válido para distinguir o que é esse elemento ao arrastar.

## <a name="possible-causes"></a>Possíveis causas

-   O elemento, ou seu pai, tem um nome ou rótulo atribuído incorretamente.
-   Um desenvolvedor não está ciente de que leitores de tela lêem nomes e tipos de controle.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IAccessible:: obter \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)
</dt> <dt>

[Propriedade Name](name-property.md)
</dt> <dt>

[**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)
</dt> <dt>

[**IUIAutomationElement:: CurrentName**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname)
</dt> </dl>

 

 




