---
description: Descrição de maneiras de melhorar o desempenho ao usar as APIs (interfaces de programação de aplicativo) do StylusInput.
ms.assetid: 2a541715-2d9e-4eb2-ab60-ec95368fca5a
title: Considerações sobre desempenho para a API StylusInput
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 721474f1e1097729246e5d497d20dcab868190a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103663257"
---
# <a name="performance-considerations-for-the-stylusinput-api"></a><span data-ttu-id="4fa55-103">Considerações sobre desempenho para a API StylusInput</span><span class="sxs-lookup"><span data-stu-id="4fa55-103">Performance Considerations for the StylusInput API</span></span>

<span data-ttu-id="4fa55-104">A lista a seguir descreve algumas maneiras de melhorar o desempenho de aplicativos que usam as APIs do StylusInput.</span><span class="sxs-lookup"><span data-stu-id="4fa55-104">The following list describes some ways in which to improve the performance of applications that use the StylusInput APIs.</span></span>

-   <span data-ttu-id="4fa55-105">Use a propriedade [Microsoft. StylusInput. IStylusSyncPlugin. DataInterest](/previous-versions/ms824752(v=msdn.10)) ou [Microsoft. StylusInput. IStylusAsyncPlugin. DataInterest](/previous-versions/ms824769(v=msdn.10)) para assinar apenas os dados relevantes para o seu plug-in.</span><span class="sxs-lookup"><span data-stu-id="4fa55-105">Use the [Microsoft.StylusInput.IStylusSyncPlugin.DataInterest](/previous-versions/ms824752(v=msdn.10)) or [Microsoft.StylusInput.IStylusAsyncPlugin.DataInterest](/previous-versions/ms824769(v=msdn.10)) property to subscribe only to the data that is relevant to your plug-in.</span></span> <span data-ttu-id="4fa55-106">Isso reduz o número total de chamadas de método que o objeto [**RealTimeStylus**](realtimestylus-class.md) faz e também reduz a complexidade do seu plug-in.</span><span class="sxs-lookup"><span data-stu-id="4fa55-106">This reduces the overall number of method calls the [**RealTimeStylus**](realtimestylus-class.md) object makes and also reduces the complexity of your plug-in.</span></span> <span data-ttu-id="4fa55-107">O objeto **RealTimeStylus** apenas verifica a propriedade DataInterest quando o plug-in é anexado.</span><span class="sxs-lookup"><span data-stu-id="4fa55-107">The **RealTimeStylus** object only checks the DataInterest property when the plug-in is attached.</span></span>
-   <span data-ttu-id="4fa55-108">Minimize a complexidade dos plug-ins síncronos. Plug-ins síncronos geralmente chamados pelo thread do objeto [**RealTimeStylus**](realtimestylus-class.md) e podem contribuir para atrasos na coleta de tinta.</span><span class="sxs-lookup"><span data-stu-id="4fa55-108">Minimize the complexity of synchronous plug-ins. Synchronous plug-ins generally called by the [**RealTimeStylus**](realtimestylus-class.md) object's thread and may contribute to delays in ink collection.</span></span>
-   <span data-ttu-id="4fa55-109">Considere tornar seu plug-in assíncrono.</span><span class="sxs-lookup"><span data-stu-id="4fa55-109">Consider making your plug-in asynchronous.</span></span> <span data-ttu-id="4fa55-110">Se o seu plug-in for complexo e precisar adicionar dados personalizados à fila do objeto [**RealTimeStylus**](realtimestylus-class.md) , considere usar um modelo **RealTimeStylus** em cascata e adicionar o plug-in à coleção de plug-ins síncrona do objeto **RealTimeStylus** secundário.</span><span class="sxs-lookup"><span data-stu-id="4fa55-110">If your plug-in is complex and needs to add custom data to the [**RealTimeStylus**](realtimestylus-class.md) object's queue, consider using a cascaded **RealTimeStylus** model and adding the plug-in to the secondary **RealTimeStylus** object's synchronous plug-in collection.</span></span> <span data-ttu-id="4fa55-111">Para obter mais informações sobre o modelo **RealTimeStylus** em cascata, consulte [o modelo RealTimeStylus em cascata](the-cascaded-realtimestylus-model.md).</span><span class="sxs-lookup"><span data-stu-id="4fa55-111">For more information about the cascaded **RealTimeStylus** model, see [The Cascaded RealTimeStylus Model](the-cascaded-realtimestylus-model.md).</span></span>

 

 
