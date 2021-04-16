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
# <a name="using-a-custom-gesture-recognizer"></a><span data-ttu-id="6962a-104">Usando um reconhecedor de gestor personalizado</span><span class="sxs-lookup"><span data-stu-id="6962a-104">Using a Custom Gesture Recognizer</span></span>

<span data-ttu-id="6962a-105">Você pode usar um reconhecedor de gestor personalizado independentemente, ou além do [**GestureRecognizer**](gesturerecognizer-class.md).</span><span class="sxs-lookup"><span data-stu-id="6962a-105">You can use a custom gesture recognizer independently, or in addition to the [**GestureRecognizer**](gesturerecognizer-class.md).</span></span>

<span data-ttu-id="6962a-106">Crie o reconhecedor de gestos personalizado como um [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin), faça com que ele crie [CustomStylusData](/previous-versions/ms575208(v=vs.100))e inclua o plug-in no mesmo [StylusSyncPluginCollection](/previous-versions/ms824788(v=msdn.10)) que o [**GestureRecognizer**](gesturerecognizer-class.md).</span><span class="sxs-lookup"><span data-stu-id="6962a-106">Create your custom gesture recognizer as an [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin), have it create [CustomStylusData](/previous-versions/ms575208(v=vs.100)), and include the plug-in in the same [StylusSyncPluginCollection](/previous-versions/ms824788(v=msdn.10)) as the [**GestureRecognizer**](gesturerecognizer-class.md).</span></span> <span data-ttu-id="6962a-107">No **IStylusSyncPlugin**, combine notificações de gesto dos reconhecedores em notificações a serem consumidas por um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6962a-107">In the **IStylusSyncPlugin**, combine gesture notifications from both recognizers into notifications to be consumed by an application.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6962a-108">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6962a-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6962a-109">Acessando e manipulando a entrada da caneta</span><span class="sxs-lookup"><span data-stu-id="6962a-109">Accessing and Manipulating Stylus Input</span></span>](accessing-and-manipulating-stylus-input.md)
</dt> </dl>

 

 
