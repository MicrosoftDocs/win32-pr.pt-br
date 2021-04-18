---
description: A partir do TAPI 2,1, as DLLs da interface do usuário do provedor de serviços de telefonia podem ser usadas para gerenciar e exibir caixas de diálogo. A TAPI carrega a DLL no processo de um aplicativo que invoca qualquer uma das funções de provedor de serviço que pode exibir uma caixa de diálogo.
ms.assetid: 0a0320d1-fb75-405e-8074-b37cef956c9f
title: O que há de novo na versão 2,1 do TSPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51642fb9ac960732f8e4a56805652333d0c32468
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105766209"
---
# <a name="whats-new-for-tspi-version-21"></a><span data-ttu-id="3abe5-104">O que há de novo na versão 2,1 do TSPI</span><span class="sxs-lookup"><span data-stu-id="3abe5-104">What's New for TSPI Version 2.1</span></span>

<span data-ttu-id="3abe5-105">A partir do TAPI 2,1, as DLLs da interface do usuário do provedor de serviços de telefonia podem ser usadas para gerenciar e exibir caixas de diálogo.</span><span class="sxs-lookup"><span data-stu-id="3abe5-105">Starting with TAPI 2.1, the telephony service provider user interface DLLs can be used to manage and display dialog boxes.</span></span> <span data-ttu-id="3abe5-106">A TAPI carrega a DLL no processo de um aplicativo que invoca qualquer uma das funções de provedor de serviço que pode exibir uma caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="3abe5-106">TAPI loads the DLL into the process of an application that invokes any of the service provider functions that can display a dialog.</span></span>

<span data-ttu-id="3abe5-107">A partir do TAPI 2,1, os manipuladores de solicitação de proxy podem ser implementados.</span><span class="sxs-lookup"><span data-stu-id="3abe5-107">Starting with TAPI 2.1, proxy request handlers can be implemented.</span></span> <span data-ttu-id="3abe5-108">Um manipulador é um aplicativo de telefonia completo que normalmente é executado em um servidor de telefonia e fornece serviços que são implementados mais adequadamente em um aplicativo do que um driver.</span><span class="sxs-lookup"><span data-stu-id="3abe5-108">A handler is a full telephony application that normally executes on a telephony server and provides services that are more appropriately implemented in an application than a driver.</span></span>

<span data-ttu-id="3abe5-109">As funções e mensagens que foram novas ou alteradas para TSPI versão 2,1 são as seguintes:</span><span class="sxs-lookup"><span data-stu-id="3abe5-109">Functions and messages that were new or changed for TSPI version 2.1 are as follows:</span></span>

-   [<span data-ttu-id="3abe5-110">**TSPI_lineConditionalMediaDetection**</span><span class="sxs-lookup"><span data-stu-id="3abe5-110">**TSPI_lineConditionalMediaDetection**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineconditionalmediadetection)
-   <span data-ttu-id="3abe5-111">**TSPI_lineDropNoOwner**—**obsoleto**</span><span class="sxs-lookup"><span data-stu-id="3abe5-111">**TSPI_lineDropNoOwner**—**obsolete**</span></span>
-   <span data-ttu-id="3abe5-112">**TSPI_lineDropOnClose**—**obsoleto**</span><span class="sxs-lookup"><span data-stu-id="3abe5-112">**TSPI_lineDropOnClose**—**obsolete**</span></span>
-   [<span data-ttu-id="3abe5-113">**TSPI_lineGetID**</span><span class="sxs-lookup"><span data-stu-id="3abe5-113">**TSPI_lineGetID**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetid)
-   [<span data-ttu-id="3abe5-114">**TSPI_lineSetCallData**</span><span class="sxs-lookup"><span data-stu-id="3abe5-114">**TSPI_lineSetCallData**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetcalldata)
-   [<span data-ttu-id="3abe5-115">**TSPI_lineSetCallQualityOfService**</span><span class="sxs-lookup"><span data-stu-id="3abe5-115">**TSPI_lineSetCallQualityOfService**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetcallqualityofservice)
-   [<span data-ttu-id="3abe5-116">**TSPI_lineSetCallTreatment**</span><span class="sxs-lookup"><span data-stu-id="3abe5-116">**TSPI_lineSetCallTreatment**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetcalltreatment)
-   [<span data-ttu-id="3abe5-117">**TSPI_lineSetLineDevStatus**</span><span class="sxs-lookup"><span data-stu-id="3abe5-117">**TSPI_lineSetLineDevStatus**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetlinedevstatus)
-   [<span data-ttu-id="3abe5-118">**TSPI_phoneGetID**</span><span class="sxs-lookup"><span data-stu-id="3abe5-118">**TSPI_phoneGetID**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_phonegetid)
-   [<span data-ttu-id="3abe5-119">**TSPI_providerInit**</span><span class="sxs-lookup"><span data-stu-id="3abe5-119">**TSPI_providerInit**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_providerinit)
-   [<span data-ttu-id="3abe5-120">**TSPI_providerShutdown**</span><span class="sxs-lookup"><span data-stu-id="3abe5-120">**TSPI_providerShutdown**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_providershutdown)
-   <span data-ttu-id="3abe5-121">[**LINE_GATHERDIGITS**](/previous-versions/windows/desktop/legacy/ms725229(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3abe5-121">[**LINE_GATHERDIGITS**](/previous-versions/windows/desktop/legacy/ms725229(v=vs.85))</span></span>
-   <span data-ttu-id="3abe5-122">[**LINE_GENERATE**](/previous-versions/windows/desktop/legacy/ms725230(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3abe5-122">[**LINE_GENERATE**](/previous-versions/windows/desktop/legacy/ms725230(v=vs.85))</span></span>
-   <span data-ttu-id="3abe5-123">[**LINE_MONITORDIGITS**](/previous-versions/windows/desktop/legacy/ms725232(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3abe5-123">[**LINE_MONITORDIGITS**](/previous-versions/windows/desktop/legacy/ms725232(v=vs.85))</span></span>
-   <span data-ttu-id="3abe5-124">[**LINE_MONITORMEDIA**](/previous-versions/windows/desktop/legacy/ms725233(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3abe5-124">[**LINE_MONITORMEDIA**](/previous-versions/windows/desktop/legacy/ms725233(v=vs.85))</span></span>
-   <span data-ttu-id="3abe5-125">[**LINE_MONITORTONE**](/previous-versions/windows/desktop/legacy/ms725234(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3abe5-125">[**LINE_MONITORTONE**](/previous-versions/windows/desktop/legacy/ms725234(v=vs.85))</span></span>
-   <span data-ttu-id="3abe5-126">[**LINE_REMOVE**](/previous-versions/windows/desktop/legacy/ms725237(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3abe5-126">[**LINE_REMOVE**](/previous-versions/windows/desktop/legacy/ms725237(v=vs.85))</span></span>
-   <span data-ttu-id="3abe5-127">[**PHONE_REMOVE**](/previous-versions/windows/desktop/legacy/ms725260(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3abe5-127">[**PHONE_REMOVE**](/previous-versions/windows/desktop/legacy/ms725260(v=vs.85))</span></span>

<span data-ttu-id="3abe5-128">A DLL da interface do usuário do provedor de serviços de telefonia fornece um meio de permitir a interação do usuário dentro do contexto do aplicativo em vez do próprio provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="3abe5-128">The Telephony service provider user interface DLL provides a means of allowing user interaction within the context of the application rather than the service provider itself.</span></span> <span data-ttu-id="3abe5-129">A versão 2,1 do TSPI forneceu as seguintes novas funções, mensagens e estruturas para implementação:</span><span class="sxs-lookup"><span data-stu-id="3abe5-129">TSPI version 2.1 delivered the following new functions, messages, and structures for implementation:</span></span>

-   [<span data-ttu-id="3abe5-130">**TSPI_providerFreeDialogInstance**</span><span class="sxs-lookup"><span data-stu-id="3abe5-130">**TSPI_providerFreeDialogInstance**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_providerfreedialoginstance)
-   [<span data-ttu-id="3abe5-131">**TSPI_providerGenericDialogData**</span><span class="sxs-lookup"><span data-stu-id="3abe5-131">**TSPI_providerGenericDialogData**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_providergenericdialogdata)
-   [<span data-ttu-id="3abe5-132">**TSPI_providerUIIdentify**</span><span class="sxs-lookup"><span data-stu-id="3abe5-132">**TSPI_providerUIIdentify**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_provideruiidentify)
-   [<span data-ttu-id="3abe5-133">**TUISPI_lineConfigDialog**</span><span class="sxs-lookup"><span data-stu-id="3abe5-133">**TUISPI_lineConfigDialog**</span></span>](/windows/win32/api/tspi/nf-tspi-tuispi_lineconfigdialog)
-   [<span data-ttu-id="3abe5-134">**TUISPI_lineConfigDialogEdit**</span><span class="sxs-lookup"><span data-stu-id="3abe5-134">**TUISPI_lineConfigDialogEdit**</span></span>](/windows/win32/api/tspi/nf-tspi-tuispi_lineconfigdialogedit)
-   [<span data-ttu-id="3abe5-135">**TUISPI_phoneConfigDialog**</span><span class="sxs-lookup"><span data-stu-id="3abe5-135">**TUISPI_phoneConfigDialog**</span></span>](/windows/win32/api/tspi/nf-tspi-tuispi_phoneconfigdialog)
-   [<span data-ttu-id="3abe5-136">**TUISPI_providerConfig**</span><span class="sxs-lookup"><span data-stu-id="3abe5-136">**TUISPI_providerConfig**</span></span>](/windows/win32/api/tspi/nf-tspi-tuispi_providerconfig)
-   [<span data-ttu-id="3abe5-137">**TUISPI_providerGenericDialog**</span><span class="sxs-lookup"><span data-stu-id="3abe5-137">**TUISPI_providerGenericDialog**</span></span>](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialog)
-   [<span data-ttu-id="3abe5-138">**TUISPI_providerGenericDialogData**</span><span class="sxs-lookup"><span data-stu-id="3abe5-138">**TUISPI_providerGenericDialogData**</span></span>](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialogdata)
-   [<span data-ttu-id="3abe5-139">**TUISPI_providerInstall**</span><span class="sxs-lookup"><span data-stu-id="3abe5-139">**TUISPI_providerInstall**</span></span>](/windows/win32/api/tspi/nf-tspi-tuispi_providerinstall)
-   [<span data-ttu-id="3abe5-140">**TUISPI_providerRemove**</span><span class="sxs-lookup"><span data-stu-id="3abe5-140">**TUISPI_providerRemove**</span></span>](/windows/win32/api/tspi/nf-tspi-tuispi_providerremove)
-   [<span data-ttu-id="3abe5-141">**TUISPICREATEDIALOGINSTANCEPARAMS**</span><span class="sxs-lookup"><span data-stu-id="3abe5-141">**TUISPICREATEDIALOGINSTANCEPARAMS**</span></span>](/windows/win32/api/tspi/ns-tspi-tuispicreatedialoginstanceparams)
-   [<span data-ttu-id="3abe5-142">**TUISPIDLLCALLBACK**</span><span class="sxs-lookup"><span data-stu-id="3abe5-142">**TUISPIDLLCALLBACK**</span></span>](/windows/win32/api/tspi/nc-tspi-tuispidllcallback)
-   [<span data-ttu-id="3abe5-143">**LINE_CREATEDIALOGINSTANCE**</span><span class="sxs-lookup"><span data-stu-id="3abe5-143">**LINE_CREATEDIALOGINSTANCE**</span></span>](line-createdialoginstance.md)
-   [<span data-ttu-id="3abe5-144">**LINE_SENDDIALOGINSTANCEDATA**</span><span class="sxs-lookup"><span data-stu-id="3abe5-144">**LINE_SENDDIALOGINSTANCEDATA**</span></span>](line-senddialoginstancedata.md)

 

 
