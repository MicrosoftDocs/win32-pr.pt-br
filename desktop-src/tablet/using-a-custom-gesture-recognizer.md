---
description: Você pode usar um reconhecedor de gestor personalizado independentemente, ou além do GestureRecognizer. Crie seu reconhecedor de gestos personalizado como um IStylusSyncPlugin, faça com que ele crie CustomStylusData e inclua o plug-in no mesmo StylusSyncPluginCollection que o GestureRecognizer. No IStylusSyncPlugin, combine notificações de gesto dos reconhecedores em notificações a serem consumidas por um aplicativo.
ms.assetid: ed4e8f56-9137-47fd-a8f9-17eebfd06e97
title: Usando um reconhecedor de gestor personalizado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 376f567680cfe7e862f280d1b8e8dc35a2017316
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105782462"
---
# <a name="using-a-custom-gesture-recognizer"></a>Usando um reconhecedor de gestor personalizado

Você pode usar um reconhecedor de gestor personalizado independentemente, ou além do [**GestureRecognizer**](gesturerecognizer-class.md).

Crie o reconhecedor de gestos personalizado como um [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin), faça com que ele crie [CustomStylusData](/previous-versions/ms575208(v=vs.100))e inclua o plug-in no mesmo [StylusSyncPluginCollection](/previous-versions/ms824788(v=msdn.10)) que o [**GestureRecognizer**](gesturerecognizer-class.md). No **IStylusSyncPlugin**, combine notificações de gesto dos reconhecedores em notificações a serem consumidas por um aplicativo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Acessando e manipulando a entrada da caneta](accessing-and-manipulating-stylus-input.md)
</dt> </dl>

 

 
