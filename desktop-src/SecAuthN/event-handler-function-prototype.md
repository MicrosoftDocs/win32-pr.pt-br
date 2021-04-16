---
description: As funções de protótipo do manipulador de eventos são usadas para todas as funções que manipulam eventos de notificação do Winlogon.
ms.assetid: 99b91e80-5e4e-4119-89aa-c0a80fce69e3
title: Função de manipulador de eventos funções de retorno de chamada do protótipo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Event_Handler_Function_Name
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 935ddac5660c814b898be17218d879678f2135ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105750579"
---
# <a name="event-handler-function-prototype-callback-function"></a><span data-ttu-id="303a9-103">Função de manipulador de eventos funções de retorno de chamada do protótipo</span><span class="sxs-lookup"><span data-stu-id="303a9-103">Event Handler Function Prototype callback function</span></span>

<span data-ttu-id="303a9-104">\[As funções de protótipo do manipulador de eventos não estão mais disponíveis para uso a partir do Windows Server 2008 e do Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="303a9-104">\[Event Handler Prototype functions are no longer available for use as of Windows Server 2008 and Windows Vista.</span></span> <span data-ttu-id="303a9-105">\]</span><span class="sxs-lookup"><span data-stu-id="303a9-105">\]</span></span>

<span data-ttu-id="303a9-106">As funções de protótipo do manipulador de eventos são usadas para todas as funções que manipulam eventos de notificação do [*Winlogon*](/windows/desktop/SecGloss/w-gly) .</span><span class="sxs-lookup"><span data-stu-id="303a9-106">Event Handler Prototype functions are used for all functions that handle [*Winlogon*](/windows/desktop/SecGloss/w-gly) notification events.</span></span> <span data-ttu-id="303a9-107">O nome da função, representado abaixo do nome da função do *\_ manipulador de \_ \_ eventos* do espaço reservado, normalmente reflete o nome do evento manipulado pela função.</span><span class="sxs-lookup"><span data-stu-id="303a9-107">The name of the function, represented below by the place holder *Event\_Handler\_Function\_Name*, typically reflects the name of the event that the function handles.</span></span> <span data-ttu-id="303a9-108">Por exemplo, a função que manipula eventos de logon pode ser nomeada: **WLEventLogon**.</span><span class="sxs-lookup"><span data-stu-id="303a9-108">For example, the function that handles logon events might be named: **WLEventLogon**.</span></span>

## <a name="syntax"></a><span data-ttu-id="303a9-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="303a9-109">Syntax</span></span>


```C++
void Event_Handler_Function_Name(
  _In_ PWLX_NOTIFICATION_INFO pInfo
);
```



## <a name="parameters"></a><span data-ttu-id="303a9-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="303a9-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="303a9-111">*pInfo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="303a9-111">*pInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="303a9-112">Um ponteiro para uma estrutura de [**\_ \_ informações de notificação do WLX**](/windows/desktop/api/Winwlx/ns-winwlx-wlx_notification_info) que contém os detalhes do evento.</span><span class="sxs-lookup"><span data-stu-id="303a9-112">A pointer to a [**WLX\_NOTIFICATION\_INFO**](/windows/desktop/api/Winwlx/ns-winwlx-wlx_notification_info) structure that contains the details of the event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="303a9-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="303a9-113">Return value</span></span>

<span data-ttu-id="303a9-114">Essa função de retorno de chamada não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="303a9-114">This callback function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="303a9-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="303a9-115">Remarks</span></span>

<span data-ttu-id="303a9-116">Se o seu manipulador de eventos precisar criar processos filho, ele deverá chamar a função [**CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) .</span><span class="sxs-lookup"><span data-stu-id="303a9-116">If your event handler needs to create child processes, it should call the [**CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) function.</span></span> <span data-ttu-id="303a9-117">Caso contrário, o novo processo será criado na área de trabalho do Winlogon, não na área de trabalho do usuário.</span><span class="sxs-lookup"><span data-stu-id="303a9-117">Otherwise, the new process will be created on the Winlogon desktop, not the user's desktop.</span></span>

## <a name="examples"></a><span data-ttu-id="303a9-118">Exemplos</span><span class="sxs-lookup"><span data-stu-id="303a9-118">Examples</span></span>

<span data-ttu-id="303a9-119">O exemplo a seguir mostra como implementar manipuladores de eventos para eventos do Winlogon.</span><span class="sxs-lookup"><span data-stu-id="303a9-119">The following sample shows how to implement event handlers for Winlogon events.</span></span> <span data-ttu-id="303a9-120">Para simplificar, somente as implementações dos manipuladores de eventos de logon e logoff são mostradas.</span><span class="sxs-lookup"><span data-stu-id="303a9-120">For simplicity, only the implementations of the Logon and Logoff event handlers are shown.</span></span> <span data-ttu-id="303a9-121">Você pode implementar manipuladores para o restante dos eventos exatamente da mesma maneira.</span><span class="sxs-lookup"><span data-stu-id="303a9-121">You can implement handlers for the rest of the events in exactly the same manner.</span></span>


```C++
// Copyright (C) Microsoft. All rights reserved. 
#include <windows.h>

// Here is the entrance function for the DLL.
BOOL WINAPI LibMain(HINSTANCE hInstance, DWORD dwReason, LPVOID lpReserved)
{
    switch (dwReason)
    {
        case DLL_PROCESS_ATTACH:
            {

             // Disable DLL_THREAD_ATTACH & DLL_THREAD_DETACH
             // notification calls. This is a performance optimization
             // for multithreaded applications that do not need 
             // thread-level notifications of attachment or
             // detachment.

            DisableThreadLibraryCalls (hInstance);
            }
            break;
    }

    return TRUE;
}

// Here is the event handler for the Winlogon Logon event.
void WLEventLogon (PWLX_NOTIFICATION_INFO pInfo)
{

    // Print the name of the handler to debug output.
    // You can replace this with more useful functionality.
    OutputDebugString (TEXT("NOTIFY:  Entering WLEventLogon.\r\n"));
}

// Here is the event handler for the Winlogon Logoff event.
void WLEventLogoff (PWLX_NOTIFICATION_INFO pInfo)
{

    // Print the name of the handler to debug output.
    // You can replace this with more useful functionality.
    OutputDebugString (TEXT("NOTIFY:  Entering WLEventLogff.\r\n"));
}
```



## <a name="requirements"></a><span data-ttu-id="303a9-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="303a9-122">Requirements</span></span>



| <span data-ttu-id="303a9-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="303a9-123">Requirement</span></span> | <span data-ttu-id="303a9-124">Valor</span><span class="sxs-lookup"><span data-stu-id="303a9-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="303a9-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="303a9-125">Minimum supported client</span></span><br/> | <span data-ttu-id="303a9-126">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="303a9-126">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="303a9-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="303a9-127">Minimum supported server</span></span><br/> | <span data-ttu-id="303a9-128">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="303a9-128">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="303a9-129">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="303a9-129">End of client support</span></span><br/>    | <span data-ttu-id="303a9-130">Windows XP</span><span class="sxs-lookup"><span data-stu-id="303a9-130">Windows XP</span></span><br/>                                |
| <span data-ttu-id="303a9-131">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="303a9-131">End of server support</span></span><br/>    | <span data-ttu-id="303a9-132">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="303a9-132">Windows Server 2003</span></span><br/>                       |



 

