---
title: Os elementos DragPattern/DragDropPattern exigem DropEffect válidos
description: Os elementos DragPattern/DragDropPattern exigem DropEffect válidos
ms.assetid: 508DD4F3-4878-4A9E-859D-06BBDA505708
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9cd95e1da2d3d05c7499f72c86d454da2832947cafd0150e8f62b2f3e8d56af2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118115674"
---
# <a name="dragpatterndragdroppattern-elements-requires-valid-dropeffect"></a>Os elementos DragPattern/DragDropPattern exigem DropEffect válidos

## <a name="text"></a>Texto

Elementos que oferecem suporte a arrastar/soltar devem ter um conjunto ' DropEffect ' válido

## <a name="type"></a>Tipo

Erro

## <a name="description"></a>Descrição

O elemento dá suporte a [**IUIAutomationDragPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdragpattern) ou a [**IUIAutomationDropTargetPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdroptargetpattern), mas não tem um conjunto de propriedades [**DropEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) válido.

Esse problema causa problemas para as pessoas que dependem de um leitor de tela. O usuário não poderá informar o efeito que esse objeto tem ao arrastar.

## <a name="possible-causes"></a>Possíveis causas

-   O elemento, ou seu pai, não criou [**DropEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) ou [**DropEffects**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffects) um nome ou rótulo atribuído incorretamente.
-   Um desenvolvedor não está ciente de que os leitores de tela lêem DropEffect (s).

 

 




