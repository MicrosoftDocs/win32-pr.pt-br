---
description: As classes RealTimeStylus, GestureRecognizer e DynamicRenderer são implementadas como wrappers COM e estão disponíveis somente em código gerenciado.
ms.assetid: db8f0f25-3650-4843-92e4-af5460841e7e
title: Notas de implementação para as APIs StylusInput
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47150d6a9aff5495e89f30d29929fd7d604f9eed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920746"
---
# <a name="implementation-notes-for-the-stylusinput-apis"></a><span data-ttu-id="29542-103">Notas de implementação para as APIs StylusInput</span><span class="sxs-lookup"><span data-stu-id="29542-103">Implementation Notes for the StylusInput APIs</span></span>

<span data-ttu-id="29542-104">As classes [**RealTimeStylus**](realtimestylus-class.md), [GestureRecognizer](/previous-versions/ms575185(v=vs.100))e [DynamicRenderer](/previous-versions/ms575176(v=vs.100)) são implementadas como wrappers com e estão disponíveis somente em código gerenciado.</span><span class="sxs-lookup"><span data-stu-id="29542-104">The [**RealTimeStylus**](realtimestylus-class.md), [GestureRecognizer](/previous-versions/ms575185(v=vs.100)), and [DynamicRenderer](/previous-versions/ms575176(v=vs.100)) classes are implemented as COM wrappers and are available only in managed code.</span></span>

<span data-ttu-id="29542-105">Quando o objeto [**RealTimeStylus**](realtimestylus-class.md), [GestureRecognizer](/previous-versions/ms575185(v=vs.100))ou [DynamicRenderer](/previous-versions/ms575176(v=vs.100)) é adicionado como um plug-in a um objeto **RealTimeStylus** , os objetos COM subjacentes interagem no nível de com.</span><span class="sxs-lookup"><span data-stu-id="29542-105">When the [**RealTimeStylus**](realtimestylus-class.md), [GestureRecognizer](/previous-versions/ms575185(v=vs.100)), or [DynamicRenderer](/previous-versions/ms575176(v=vs.100)) object is added as a plug-in to a **RealTimeStylus** object, the underlying COM objects interact on the COM level.</span></span> <span data-ttu-id="29542-106">Portanto, chamar diretamente os métodos das interfaces [IStylusSyncPlugin](/previous-versions/ms575201(v=vs.100)) ou [IStylusAsyncPlugin](/previous-versions/ms575194(v=vs.100)) não tem suporte.</span><span class="sxs-lookup"><span data-stu-id="29542-106">Therefore, directly calling the methods of the [IStylusSyncPlugin](/previous-versions/ms575201(v=vs.100)) or [IStylusAsyncPlugin](/previous-versions/ms575194(v=vs.100)) interfaces are not supported.</span></span> <span data-ttu-id="29542-107">Adicionar o objeto **RealTimeStylus**, GestureRecognizer ou DynamicRenderer ao objeto **RealTimeStylus** é a única maneira de acessar esses recursos.</span><span class="sxs-lookup"><span data-stu-id="29542-107">Adding the **RealTimeStylus**, GestureRecognizer, or DynamicRenderer object to the **RealTimeStylus** object is the only way to access these features.</span></span>

 

 
