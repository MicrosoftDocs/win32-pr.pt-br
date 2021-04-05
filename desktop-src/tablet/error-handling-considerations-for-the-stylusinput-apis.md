---
description: Visão geral do tratamento de erros ao usar as APIs (interfaces de programação de aplicativo) do StylusInput.
ms.assetid: 7d7ff5b2-3eda-4570-96fe-b3b8f41ff69b
title: Considerações de tratamento de erro para a API StylusInput
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35fa582a8dbf531588f6d3d0c142c4ec7b40a058
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920961"
---
# <a name="error-handling-considerations-for-the-stylusinput-api"></a><span data-ttu-id="e6734-103">Considerações de tratamento de erro para a API StylusInput</span><span class="sxs-lookup"><span data-stu-id="e6734-103">Error Handling Considerations for the StylusInput API</span></span>

<span data-ttu-id="e6734-104">As exceções não tratadas geradas por um plug-in são capturadas pelo objeto [**RealTimeStylus**](realtimestylus-class.md) .</span><span class="sxs-lookup"><span data-stu-id="e6734-104">Unhandled exceptions thrown by a plug-in are caught by the [**RealTimeStylus**](realtimestylus-class.md) object.</span></span> <span data-ttu-id="e6734-105">Quando um plug-in gera uma exceção, o fluxo normal de dados é interrompido.</span><span class="sxs-lookup"><span data-stu-id="e6734-105">When a plug-in throws an exception, the normal flow of data is interrupted.</span></span> <span data-ttu-id="e6734-106">O objeto **RealTimeStylus** :</span><span class="sxs-lookup"><span data-stu-id="e6734-106">The **RealTimeStylus** object:</span></span>

1.  <span data-ttu-id="e6734-107">Cria um objeto [ErrorData](/previous-versions/ms575221(v=vs.100)) (em código gerenciado).</span><span class="sxs-lookup"><span data-stu-id="e6734-107">Creates an [ErrorData](/previous-versions/ms575221(v=vs.100)) object (in managed code).</span></span>
2.  <span data-ttu-id="e6734-108">Chama o método de [**erro**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-error) (em código gerenciado, o método [Microsoft. StylusInput. IStylusSyncPlugin. Error](/previous-versions/ms824754(v=msdn.10)) ou [Microsoft. StylusInput. IStylusAsyncPlugin. Error](/previous-versions/ms824771(v=msdn.10)) ) do plug-in que gerou a exceção.</span><span class="sxs-lookup"><span data-stu-id="e6734-108">Calls the [**Error**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-error) method (in managed code, either the [Microsoft.StylusInput.IStylusSyncPlugin.Error](/previous-versions/ms824754(v=msdn.10)) or [Microsoft.StylusInput.IStylusAsyncPlugin.Error](/previous-versions/ms824771(v=msdn.10)) method) of the plug-in that threw the exception.</span></span>
3.  <span data-ttu-id="e6734-109">Chama o método de [**erro**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-error) dos plug-ins restantes nessa coleção.</span><span class="sxs-lookup"><span data-stu-id="e6734-109">Calls the [**Error**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-error) method of the remaining plug-ins in that collection.</span></span>
4.  <span data-ttu-id="e6734-110">Se o plug-in que gerou a exceção for um plug-in síncrono, o objeto [ErrorData](/previous-versions/ms575221(v=vs.100)) (em código gerenciado) será adicionado à fila de saída.</span><span class="sxs-lookup"><span data-stu-id="e6734-110">If the plug-in that threw the exception is a synchronous plug-in, the [ErrorData](/previous-versions/ms575221(v=vs.100)) object (in managed code) is added to the output queue.</span></span>
5.  <span data-ttu-id="e6734-111">O objeto [**RealTimeStylus**](realtimestylus-class.md) retoma o processamento normal dos dados originais.</span><span class="sxs-lookup"><span data-stu-id="e6734-111">The [**RealTimeStylus**](realtimestylus-class.md) object resumes normal processing of the original data.</span></span>

<span data-ttu-id="e6734-112">Se um plug-in lançar uma exceção do seu método de [**erro**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-error) , o objeto [**RealTimeStylus**](realtimestylus-class.md) capturará a exceção, mas não gerará um novo objeto [ErrorData](/previous-versions/ms575221(v=vs.100)) .</span><span class="sxs-lookup"><span data-stu-id="e6734-112">If a plug-in throws an exception from its [**Error**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-error) method, the [**RealTimeStylus**](realtimestylus-class.md) object catches the exception but does not generate a new [ErrorData](/previous-versions/ms575221(v=vs.100)) object.</span></span> <span data-ttu-id="e6734-113">Para obter mais informações sobre como o ErrorData é adicionado à fila, consulte [dados de plug-in e a classe RealTimeStylus](plug-in-data-and-the-realtimestylus-class.md).</span><span class="sxs-lookup"><span data-stu-id="e6734-113">For more information about how ErrorData is added to the queue, see [Plug-in Data and the RealTimeStylus Class](plug-in-data-and-the-realtimestylus-class.md).</span></span>

<span data-ttu-id="e6734-114">O objeto [**RealTimeStylus**](realtimestylus-class.md) não interrompe o processamento de dados do fluxo de dados da caneta eletrônica quando um de seus plug-ins gera uma exceção.</span><span class="sxs-lookup"><span data-stu-id="e6734-114">The [**RealTimeStylus**](realtimestylus-class.md) object does not stop processing data from the tablet pen's data stream when one of its plug-ins throws an exception.</span></span> <span data-ttu-id="e6734-115">Dependendo do seu design, alguns dos seus plug-ins talvez precisem assinar a notificação [ErrorData](/previous-versions/ms575221(v=vs.100)) e modificar seu comportamento quando ocorrer uma exceção.</span><span class="sxs-lookup"><span data-stu-id="e6734-115">Depending on your design, some of your plug-ins may need to subscribe to the [ErrorData](/previous-versions/ms575221(v=vs.100)) notification and modify their behavior when an exception occurs.</span></span>

 

 
