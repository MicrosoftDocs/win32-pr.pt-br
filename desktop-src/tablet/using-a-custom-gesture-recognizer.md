---
description: Você pode usar um reconhecedor de gestor personalizado independentemente, ou além do GestureRecognizer. Crie seu reconhecedor de gestos personalizado como um IStylusSyncPlugin, faça com que ele crie CustomStylusData e inclua o plug-in no mesmo StylusSyncPluginCollection que o GestureRecognizer. No IStylusSyncPlugin, combine notificações de gesto dos reconhecedores em notificações a serem consumidas por um aplicativo.
ms.assetid: ed4e8f56-9137-47fd-a8f9-17eebfd06e97
title: Usando um reconhecedor de gestor personalizado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa4c58dd93bdb19f1f930be38e40f0068fa02239f09603035b572559d1f8a916
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119091287"
---
# <a name="using-a-custom-gesture-recognizer"></a>Usando um reconhecedor de gestor personalizado

Você pode usar um reconhecedor de gestor personalizado independentemente, ou além do [**GestureRecognizer**](gesturerecognizer-class.md).

Crie o reconhecedor de gestos personalizado como um [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin), faça com que ele crie [CustomStylusData](/previous-versions/ms575208(v=vs.100))e inclua o plug-in no mesmo [StylusSyncPluginCollection](/previous-versions/ms824788(v=msdn.10)) que o [**GestureRecognizer**](gesturerecognizer-class.md). No **IStylusSyncPlugin**, combine notificações de gesto dos reconhecedores em notificações a serem consumidas por um aplicativo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Acessando e manipulando a entrada da caneta](accessing-and-manipulating-stylus-input.md)
</dt> </dl>

 

 
