---
description: <span id="vspixengine.callbackcommandtype"></span>Enumeração CallbackCommandType-uma enumeração usada para comunicação entre o mecanismo de captura e um host (como o Visual Studio Diagnóstico de Gráficos).
MS-HAID: vspixengine.CallbackCommandType
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Enumeração CallbackCommandType
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 78E0CD6C-5264-4F66-BAB9-20DC9C0C1EC1
api_name:
- CallbackCommandType
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 85e1b7d396d125add00824e9b7c94086e0da6be2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090124"
---
# <a name="span-idvspixenginecallbackcommandtypespancallbackcommandtype-enumeration"></a><span data-ttu-id="29eca-103"><span id="vspixengine.callbackcommandtype"></span>Enumeração CallbackCommandType</span><span class="sxs-lookup"><span data-stu-id="29eca-103"><span id="vspixengine.callbackcommandtype"></span>CallbackCommandType enumeration</span></span>

<span data-ttu-id="29eca-104">Uma enumeração usada para se comunicar entre o mecanismo de captura e um host (como o Visual Studio Diagnóstico de Gráficos).</span><span class="sxs-lookup"><span data-stu-id="29eca-104">An enum used to communicate between the capture engine and a host (such as Visual Studio Graphics Diagnostics).</span></span>

## <a name="syntax"></a><span data-ttu-id="29eca-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="29eca-105">Syntax</span></span>


```C++
};
```

## <a name="constants"></a><span data-ttu-id="29eca-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="29eca-106">Constants</span></span>

<span data-ttu-id="29eca-107"><span id="BeginCommunicationCallback"></span><span id="begincommunicationcallback"></span><span id="BEGINCOMMUNICATIONCALLBACK"></span>**BeginCommunicationCallback**</span><span class="sxs-lookup"><span data-stu-id="29eca-107"><span id="BeginCommunicationCallback"></span><span id="begincommunicationcallback"></span><span id="BEGINCOMMUNICATIONCALLBACK"></span>**BeginCommunicationCallback**</span></span>  
<span data-ttu-id="29eca-108">Resultados de BeginCommunication.</span><span class="sxs-lookup"><span data-stu-id="29eca-108">Results from BeginCommunication.</span></span>

<span data-ttu-id="29eca-109"><span id="ErrorListCallback"></span><span id="errorlistcallback"></span><span id="ERRORLISTCALLBACK"></span>**ErrorListCallback**</span><span class="sxs-lookup"><span data-stu-id="29eca-109"><span id="ErrorListCallback"></span><span id="errorlistcallback"></span><span id="ERRORLISTCALLBACK"></span>**ErrorListCallback**</span></span>  
<span data-ttu-id="29eca-110">Erros.</span><span class="sxs-lookup"><span data-stu-id="29eca-110">Errors.</span></span>

<span data-ttu-id="29eca-111"><span id="WarningListCallback"></span><span id="warninglistcallback"></span><span id="WARNINGLISTCALLBACK"></span>**WarningListCallback**</span><span class="sxs-lookup"><span data-stu-id="29eca-111"><span id="WarningListCallback"></span><span id="warninglistcallback"></span><span id="WARNINGLISTCALLBACK"></span>**WarningListCallback**</span></span>  
<span data-ttu-id="29eca-112">Avisos.</span><span class="sxs-lookup"><span data-stu-id="29eca-112">Warnings.</span></span>

<span data-ttu-id="29eca-113"><span id="MessagesCallback"></span><span id="messagescallback"></span><span id="MESSAGESCALLBACK"></span>**MessagesCallback**</span><span class="sxs-lookup"><span data-stu-id="29eca-113"><span id="MessagesCallback"></span><span id="messagescallback"></span><span id="MESSAGESCALLBACK"></span>**MessagesCallback**</span></span>  
<span data-ttu-id="29eca-114">Mensagens</span><span class="sxs-lookup"><span data-stu-id="29eca-114">Messages.</span></span>

<span data-ttu-id="29eca-115"><span id="RunExperimentCallback"></span><span id="runexperimentcallback"></span><span id="RUNEXPERIMENTCALLBACK"></span>**RunExperimentCallback**</span><span class="sxs-lookup"><span data-stu-id="29eca-115"><span id="RunExperimentCallback"></span><span id="runexperimentcallback"></span><span id="RUNEXPERIMENTCALLBACK"></span>**RunExperimentCallback**</span></span>  
<span data-ttu-id="29eca-116">Resultado de RunExperiment.</span><span class="sxs-lookup"><span data-stu-id="29eca-116">Result from RunExperiment.</span></span>

<span data-ttu-id="29eca-117"><span id="RunActionCallback"></span><span id="runactioncallback"></span><span id="RUNACTIONCALLBACK"></span>**RunActionCallback**</span><span class="sxs-lookup"><span data-stu-id="29eca-117"><span id="RunActionCallback"></span><span id="runactioncallback"></span><span id="RUNACTIONCALLBACK"></span>**RunActionCallback**</span></span>  
<span data-ttu-id="29eca-118">Resultado de RunAction.</span><span class="sxs-lookup"><span data-stu-id="29eca-118">Result from RunAction.</span></span>

<span data-ttu-id="29eca-119"><span id="NewFramesCallback"></span><span id="newframescallback"></span><span id="NEWFRAMESCALLBACK"></span>**NewFramesCallback**</span><span class="sxs-lookup"><span data-stu-id="29eca-119"><span id="NewFramesCallback"></span><span id="newframescallback"></span><span id="NEWFRAMESCALLBACK"></span>**NewFramesCallback**</span></span>  
<span data-ttu-id="29eca-120">Um valor que indica um retorno de chamada a ser chamado quando novos quadros tiverem sido capturados e estiverem prontos para serem exibidos.</span><span class="sxs-lookup"><span data-stu-id="29eca-120">A value that indicates a callback to be called when new frames have been captured and ready to display.</span></span>

<span data-ttu-id="29eca-121"><span id="BeginCommunicationCallbackLegacy"></span><span id="begincommunicationcallbacklegacy"></span><span id="BEGINCOMMUNICATIONCALLBACKLEGACY"></span>**BeginCommunicationCallbackLegacy**</span><span class="sxs-lookup"><span data-stu-id="29eca-121"><span id="BeginCommunicationCallbackLegacy"></span><span id="begincommunicationcallbacklegacy"></span><span id="BEGINCOMMUNICATIONCALLBACKLEGACY"></span>**BeginCommunicationCallbackLegacy**</span></span>  
<span data-ttu-id="29eca-122">Resultados de uma versão mais antiga do BeginCommunication usado no Windows 7 e no Windows 8.</span><span class="sxs-lookup"><span data-stu-id="29eca-122">Results from an older version of BeginCommunication used on Windows 7 and Windows 8.</span></span>

<span data-ttu-id="29eca-123"><span id="RunExperimentStatusCallback"></span><span id="runexperimentstatuscallback"></span><span id="RUNEXPERIMENTSTATUSCALLBACK"></span>**RunExperimentStatusCallback**</span><span class="sxs-lookup"><span data-stu-id="29eca-123"><span id="RunExperimentStatusCallback"></span><span id="runexperimentstatuscallback"></span><span id="RUNEXPERIMENTSTATUSCALLBACK"></span>**RunExperimentStatusCallback**</span></span>  
<span data-ttu-id="29eca-124">Resultado de RunExperiementProgress.</span><span class="sxs-lookup"><span data-stu-id="29eca-124">Result from RunExperiementProgress.</span></span>

## <a name="requirements"></a><span data-ttu-id="29eca-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="29eca-125">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="29eca-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="29eca-126">Header</span></span></p></td><td><span data-ttu-id="29eca-127">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="29eca-127">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



