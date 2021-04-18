---
description: Assina notificações de alteração de status de serviço usando uma função de retorno de chamada.
ms.assetid: d67113eb-2141-444c-9f09-eaa772bcad8a
title: Função SubscribeServiceChangeNotifications (Winsvcp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SubscribeServiceChangeNotifications
api_type:
- DllExport
api_location:
- SecHost.dll
- API-MS-Win-Service-Private-L1-1-0.dll
- API-MS-Win-Service-Private-L1-1-1.dll
- Advapi32.dll
- API-MS-Win-Service-Private-L1-1-2.dll
ms.openlocfilehash: e327a44d613b514123862b1ddcb1bf302fea63ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105755551"
---
# <a name="subscribeservicechangenotifications-function"></a><span data-ttu-id="726f7-103">Função SubscribeServiceChangeNotifications</span><span class="sxs-lookup"><span data-stu-id="726f7-103">SubscribeServiceChangeNotifications function</span></span>

<span data-ttu-id="726f7-104">Assina notificações de alteração de status de serviço usando uma função de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="726f7-104">Subscribes for service status change notifications using a callback function.</span></span>

## <a name="syntax"></a><span data-ttu-id="726f7-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="726f7-105">Syntax</span></span>


```C++
DWORD WINAPI SubscribeServiceChangeNotifications(
  _In_     SC_HANDLE                     hService,
  _In_     SC_EVENT_TYPE                 eEventType,
  _In_     PSC_NOTIFICATION_CALLBACK     pCallback,
  _In_opt_ PVOID                         pCallbackContext,
  _Out_    PSC_NOTIFICATION_REGISTRATION *pSubscription
);
```



## <a name="parameters"></a><span data-ttu-id="726f7-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="726f7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="726f7-107">*hService* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="726f7-107">*hService* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="726f7-108">Um identificador para o serviço ou um identificador para o Gerenciador de controle de serviço (SCM) para monitorar as alterações.</span><span class="sxs-lookup"><span data-stu-id="726f7-108">A handle to the service or a handle to the service control manager (SCM) to monitor for changes.</span></span>

<span data-ttu-id="726f7-109">Identificadores para serviços são retornados pela função [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) e [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) e devem ter o direito de acesso de **\_ \_ status de consulta de serviço** .</span><span class="sxs-lookup"><span data-stu-id="726f7-109">Handles to services are returned by the [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) and [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) function and must have the **SERVICE\_QUERY\_STATUS** access right.</span></span> <span data-ttu-id="726f7-110">Os identificadores para o Gerenciador de controle de serviço são retornados pela função [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) e devem ter o direito de acesso do **serviço de \_ \_ enumeração \_ SC Manager** .</span><span class="sxs-lookup"><span data-stu-id="726f7-110">Handles to the service control manager are returned by the [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) function and must have the **SC\_MANAGER\_ENUMERATE\_SERVICE** access right.</span></span>

</dd> <dt>

<span data-ttu-id="726f7-111">*eEventType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="726f7-111">*eEventType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="726f7-112">Especifica o tipo de alterações de status que devem ser relatadas.</span><span class="sxs-lookup"><span data-stu-id="726f7-112">Specifies the type of status changes that should be reported.</span></span> <span data-ttu-id="726f7-113">Esse parâmetro é definido como um dos valores especificados no [**tipo de \_ evento \_ SC**](sc-event-type.md).</span><span class="sxs-lookup"><span data-stu-id="726f7-113">This parameter is set to one of the values specified in [**SC\_EVENT\_TYPE**](sc-event-type.md).</span></span> <span data-ttu-id="726f7-114">O comportamento dessa função é diferente dependendo do tipo de evento da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="726f7-114">The behavior for this function is different depending on the event type as follows.</span></span>



| <span data-ttu-id="726f7-115">Valor</span><span class="sxs-lookup"><span data-stu-id="726f7-115">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="726f7-116">Significado</span><span class="sxs-lookup"><span data-stu-id="726f7-116">Meaning</span></span>                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span id="SC_EVENT_DATABASE_CHANGE"></span><span id="sc_event_database_change"></span><dl> <span data-ttu-id="726f7-117"><dt>**Sc \_ \_ \_ Alteração de banco de dados de eventos**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="726f7-117"><dt>**SC\_EVENT\_DATABASE\_CHANGE**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="726f7-118">Um serviço foi adicionado ou excluído.</span><span class="sxs-lookup"><span data-stu-id="726f7-118">A service has been added or deleted.</span></span> <span data-ttu-id="726f7-119">O parâmetro *hService* deve ser um identificador para o SCM.</span><span class="sxs-lookup"><span data-stu-id="726f7-119">The *hService* parameter must be a handle to the SCM.</span></span><br/>                  |
| <span id="SC_EVENT_PROPERTY_CHANGE"></span><span id="sc_event_property_change"></span><dl> <span data-ttu-id="726f7-120"><dt>**Sc \_ \_ \_ Alteração de propriedade de evento**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="726f7-120"><dt>**SC\_EVENT\_PROPERTY\_CHANGE**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="726f7-121">Uma ou mais propriedades de serviço foram atualizadas.</span><span class="sxs-lookup"><span data-stu-id="726f7-121">One or more service properties have been updated.</span></span> <span data-ttu-id="726f7-122">O parâmetro *hService* deve ser um identificador para o serviço.</span><span class="sxs-lookup"><span data-stu-id="726f7-122">The *hService* parameter must be a handle to the service.</span></span><br/> |
| <span id="SC_EVENT_STATUS_CHANGE"></span><span id="sc_event_status_change"></span><dl> <span data-ttu-id="726f7-123"><dt>**Sc \_ \_ \_ Alteração do status do evento**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="726f7-123"><dt>**SC\_EVENT\_STATUS\_CHANGE**</dt> <dt>2</dt></span></span> </dl>       | <span data-ttu-id="726f7-124">O status de um serviço foi alterado.</span><span class="sxs-lookup"><span data-stu-id="726f7-124">The status of a service has changed.</span></span> <span data-ttu-id="726f7-125">O parâmetro *hService* deve ser um identificador para o serviço.</span><span class="sxs-lookup"><span data-stu-id="726f7-125">The *hService* parameter must be a handle to the service.</span></span><br/>              |



 

</dd> <dt>

<span data-ttu-id="726f7-126">*pCallback* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="726f7-126">*pCallback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="726f7-127">Especifica a função de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="726f7-127">Specifies the callback function.</span></span> <span data-ttu-id="726f7-128">O retorno de chamada deve ser definido como tendo um tipo de **\_ retorno de \_ chamada de notificação SC**.</span><span class="sxs-lookup"><span data-stu-id="726f7-128">The callback must be defined as having a type of **SC\_NOTIFICATION\_CALLBACK**.</span></span> <span data-ttu-id="726f7-129">Para obter mais informações, consulte Comentários.</span><span class="sxs-lookup"><span data-stu-id="726f7-129">For more information, see Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="726f7-130">*pCallbackContext* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="726f7-130">*pCallbackContext* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="726f7-131">Um ponteiro que representa o contexto para este retorno de chamada de notificação.</span><span class="sxs-lookup"><span data-stu-id="726f7-131">A pointer representing the context for this notification callback.</span></span>

</dd> <dt>

<span data-ttu-id="726f7-132">*pSubscription* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="726f7-132">*pSubscription* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="726f7-133">Retorna um ponteiro para a assinatura resultante do registro de retorno de chamada de notificação.</span><span class="sxs-lookup"><span data-stu-id="726f7-133">Returns a pointer to the subscription resulting from the notification callback registration.</span></span> <span data-ttu-id="726f7-134">O chamador é responsável por chamar [**UnsubscribeServiceChangeNotifications**](unsubscribeservicechangenotifications.md) para parar de receber notificações.</span><span class="sxs-lookup"><span data-stu-id="726f7-134">The caller is responsible for calling [**UnsubscribeServiceChangeNotifications**](unsubscribeservicechangenotifications.md) to stop receiving notifications.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="726f7-135">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="726f7-135">Return value</span></span>

<span data-ttu-id="726f7-136">Se a função for bem-sucedida, o valor de retorno **será \_ êxito no erro**.</span><span class="sxs-lookup"><span data-stu-id="726f7-136">If the function succeeds, the return value is **ERROR\_SUCCESS**.</span></span>

<span data-ttu-id="726f7-137">Se a função falhar, o valor de retorno será um dos [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="726f7-137">If the function fails, the return value is one of the [system error codes](/windows/desktop/Debug/system-error-codes).</span></span>

## <a name="remarks"></a><span data-ttu-id="726f7-138">Comentários</span><span class="sxs-lookup"><span data-stu-id="726f7-138">Remarks</span></span>

<span data-ttu-id="726f7-139">A função de retorno de chamada é declarada da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="726f7-139">The callback function is declared as follows:</span></span>


```C++
typedef VOID CALLBACK SC_NOTIFICATION_CALLBACK(
    _In_    DWORD                   dwNotify,
    _In_    PVOID                   pCallbackContext
);
typedef SC_NOTIFICATION_CALLBACK* PSC_NOTIFICATION_CALLBACK;
```



<span data-ttu-id="726f7-140">A função de retorno de chamada recebe um ponteiro para o contexto fornecido pelo chamador.</span><span class="sxs-lookup"><span data-stu-id="726f7-140">The callback function receives a pointer to the context provided by the caller.</span></span> <span data-ttu-id="726f7-141">O retorno de chamada é invocado como resultado do evento de alteração de status do serviço.</span><span class="sxs-lookup"><span data-stu-id="726f7-141">The callback is invoked as a result of the service status change event.</span></span> <span data-ttu-id="726f7-142">Quando o retorno de chamada é invocado, ele é fornecido com uma bitmask de valores **\_ \_ \* xxx**\* de notificação de serviço que indicam o tipo de alteração de status do serviço.</span><span class="sxs-lookup"><span data-stu-id="726f7-142">When the callback is invoked, it is provided with a bitmask of **SERVICE\_NOTIFY\_\*XXX**\* values that indicating the type of service status change.</span></span> <span data-ttu-id="726f7-143">Quando o retorno de chamada é fornecido com zero em vez de um valor válido de \*\*notificação de serviço \_ \_ \* xxx\*\*\*, o aplicativo deve verificar o que foi alterado.</span><span class="sxs-lookup"><span data-stu-id="726f7-143">When the callback is provided with zero instead of a valid **SERVICE\_NOTIFY\_\*XXX**\* value, the application must verify what was changed.</span></span>

<span data-ttu-id="726f7-144">A função de retorno de chamada não deve bloquear a execução.</span><span class="sxs-lookup"><span data-stu-id="726f7-144">The callback function must not block execution.</span></span> <span data-ttu-id="726f7-145">Se você espera que a execução da função de retorno de chamada seja demorada, descarregue o trabalho que você executa na função de retorno de chamada para um thread separado, enfileirando um item de trabalho para um thread em um pool de threads.</span><span class="sxs-lookup"><span data-stu-id="726f7-145">If you expect the execution of the callback function to take time, offload the work that you perform in the callback function to a separate thread by queuing a work item to a thread in a thread pool.</span></span> <span data-ttu-id="726f7-146">Alguns tipos de trabalho que podem fazer a função de retorno de chamada levará tempo incluem a execução de e/s de arquivo, a espera de um evento e a realização de chamadas de procedimento remoto externo.</span><span class="sxs-lookup"><span data-stu-id="726f7-146">Some types of work that can make the callback function take time include performing file I/O, waiting on an event, and making external remote procedure calls.</span></span>

## <a name="requirements"></a><span data-ttu-id="726f7-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="726f7-147">Requirements</span></span>



| <span data-ttu-id="726f7-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="726f7-148">Requirement</span></span> | <span data-ttu-id="726f7-149">Valor</span><span class="sxs-lookup"><span data-stu-id="726f7-149">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="726f7-150">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="726f7-150">Minimum supported client</span></span><br/> | <span data-ttu-id="726f7-151">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="726f7-151">Windows 8 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="726f7-152">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="726f7-152">Minimum supported server</span></span><br/> | <span data-ttu-id="726f7-153">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="726f7-153">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="726f7-154">parâmetro</span><span class="sxs-lookup"><span data-stu-id="726f7-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="726f7-155"><dt>Winsvcp. h</dt></span><span class="sxs-lookup"><span data-stu-id="726f7-155"><dt>Winsvcp.h</dt></span></span> </dl>   |
| <span data-ttu-id="726f7-156">DLL</span><span class="sxs-lookup"><span data-stu-id="726f7-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="726f7-157"><dt>SecHost.dll</dt></span><span class="sxs-lookup"><span data-stu-id="726f7-157"><dt>SecHost.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="726f7-158">Confira também</span><span class="sxs-lookup"><span data-stu-id="726f7-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="726f7-159">**CreateService**</span><span class="sxs-lookup"><span data-stu-id="726f7-159">**CreateService**</span></span>](/windows/desktop/api/Winsvc/nf-winsvc-createservicea)
</dt> <dt>

[<span data-ttu-id="726f7-160">**OpenService**</span><span class="sxs-lookup"><span data-stu-id="726f7-160">**OpenService**</span></span>](/windows/desktop/api/Winsvc/nf-winsvc-openservicea)
</dt> <dt>

[<span data-ttu-id="726f7-161">**OpenSCManager**</span><span class="sxs-lookup"><span data-stu-id="726f7-161">**OpenSCManager**</span></span>](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera)
</dt> <dt>

[<span data-ttu-id="726f7-162">**UnsubscribeServiceChangeNotifications**</span><span class="sxs-lookup"><span data-stu-id="726f7-162">**UnsubscribeServiceChangeNotifications**</span></span>](unsubscribeservicechangenotifications.md)
</dt> <dt>

[<span data-ttu-id="726f7-163">**QueryServiceDynamicInformation**</span><span class="sxs-lookup"><span data-stu-id="726f7-163">**QueryServiceDynamicInformation**</span></span>](/windows/desktop/api/Winsvc/nf-winsvc-queryservicedynamicinformation)
</dt> </dl>

 

