---
title: Função InitializeNapAgentNotifier (NapUtil. h)
description: Assina o processo de chamada para notificações de alteração de estado NapAgent e notificações de alteração de estado de quarentena.
ms.assetid: 24180194-50d7-4f54-845d-25402af9cf9a
keywords:
- Função InitializeNapAgentNotifier NAP
topic_type:
- apiref
api_name:
- InitializeNapAgentNotifier
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f59c4c342f693038040f374bbdbcdb8ab226f74d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918232"
---
# <a name="initializenapagentnotifier-function"></a><span data-ttu-id="a4a43-104">Função InitializeNapAgentNotifier</span><span class="sxs-lookup"><span data-stu-id="a4a43-104">InitializeNapAgentNotifier function</span></span>

> [!Note]  
> <span data-ttu-id="a4a43-105">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="a4a43-105">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="a4a43-106">A função **InitializeNapAgentNotifier** assina o processo de chamada para as notificações de alteração de estado NapAgent e as notificações de alteração de estado de quarentena.</span><span class="sxs-lookup"><span data-stu-id="a4a43-106">The **InitializeNapAgentNotifier** function subscribes the calling process to NapAgent state change notifications and quarantine state change notifications.</span></span> <span data-ttu-id="a4a43-107">Essas notificações são fornecidas pelo serviço NapAgent.</span><span class="sxs-lookup"><span data-stu-id="a4a43-107">These notifications are provided by the NapAgent service.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4a43-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a4a43-108">Syntax</span></span>


```C++
NAPAPI HRESULT WINAPI InitializeNapAgentNotifier(
  _In_ NapNotifyType type,
  _In_ HANDLE        hNotifyEvent
);
```



## <a name="parameters"></a><span data-ttu-id="a4a43-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a4a43-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4a43-110">*tipo* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="a4a43-110">*type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4a43-111">Um valor de [**NapNotifyType**](/windows/win32/api/naptypes/ne-naptypes-napnotifytype) que especifica o tipo de notificações de serviço a receber.</span><span class="sxs-lookup"><span data-stu-id="a4a43-111">A [**NapNotifyType**](/windows/win32/api/naptypes/ne-naptypes-napnotifytype) value that specifies the type of service notifications to receive.</span></span>

</dd> <dt>

<span data-ttu-id="a4a43-112">*hNotifyEvent* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a4a43-112">*hNotifyEvent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4a43-113">Um identificador de evento usado para notificação.</span><span class="sxs-lookup"><span data-stu-id="a4a43-113">An event handle used for notification.</span></span> <span data-ttu-id="a4a43-114">O chamador deve passar um identificador aberto para o parâmetro *hNotifyEvent* .</span><span class="sxs-lookup"><span data-stu-id="a4a43-114">The caller must pass an open handle to the *hNotifyEvent* parameter.</span></span> <span data-ttu-id="a4a43-115">O chamador também deve fechar o identificador de eventos quando ele não for mais necessário.</span><span class="sxs-lookup"><span data-stu-id="a4a43-115">The caller must also close the event handle when it is no longer needed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a4a43-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a4a43-116">Return value</span></span>



| <span data-ttu-id="a4a43-117">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="a4a43-117">Return code</span></span>                                                                                                | <span data-ttu-id="a4a43-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="a4a43-118">Description</span></span>                                                                                               |
|------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a4a43-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a4a43-119"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="a4a43-120">Inicialização concluída com êxito.</span><span class="sxs-lookup"><span data-stu-id="a4a43-120">Initialization completed successfully.</span></span><br/>                                                         |
| <dl> <span data-ttu-id="a4a43-121"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="a4a43-121"><dt>**E\_FAIL**</dt></span></span> </dl>                     | <span data-ttu-id="a4a43-122">Falha de inicialização.</span><span class="sxs-lookup"><span data-stu-id="a4a43-122">Initialization failed.</span></span><br/>                                                                         |
| <dl> <span data-ttu-id="a4a43-123"><dt>**ERRO \_ já \_ inicializado**</dt></span><span class="sxs-lookup"><span data-stu-id="a4a43-123"><dt>**ERROR\_ALREADY\_INITIALIZED**</dt></span></span> </dl> | <span data-ttu-id="a4a43-124">O processo já assinou as notificações do serviço NapAgent do *tipo* especificado.</span><span class="sxs-lookup"><span data-stu-id="a4a43-124">The process has already subscribed to NapAgent service notifications of the *type* specified.</span></span> <br/> |
| <dl> <span data-ttu-id="a4a43-125"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="a4a43-125"><dt>**E\_INVALIDARG**</dt></span></span> </dl>               | <span data-ttu-id="a4a43-126">Um argumento inválido foi passado.</span><span class="sxs-lookup"><span data-stu-id="a4a43-126">An invalid argument was passed.</span></span> <br/>                                                               |



 

## <a name="remarks"></a><span data-ttu-id="a4a43-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="a4a43-127">Remarks</span></span>

<span data-ttu-id="a4a43-128">Essa função não é thread-safe.</span><span class="sxs-lookup"><span data-stu-id="a4a43-128">This function is not thread safe.</span></span>

<span data-ttu-id="a4a43-129">Cada processo que requer uma assinatura para notificações de serviço NapAgent do *tipo* especificado deve chamar **InitializeNapAgentNotifier** para assinar notificações.</span><span class="sxs-lookup"><span data-stu-id="a4a43-129">Each process that requires a subscription to NapAgent service notifications of the specified *type* must call **InitializeNapAgentNotifier** to subscribe to notifications.</span></span> <span data-ttu-id="a4a43-130">Se um processo precisar assinar mais de um tipo de notificação, ele deverá chamar **InitializeNapAgentNotifier** uma vez para cada tipo de notificação.</span><span class="sxs-lookup"><span data-stu-id="a4a43-130">If a process must subscribe to more than one type of notification, it must call **InitializeNapAgentNotifier** once for each type of notification.</span></span>

<span data-ttu-id="a4a43-131">Quando um processo não requer notificações adicionais, o processo deve chamar [**UninitializeNapAgentNotifier**](uninitializenapagentnotifier.md) para o *tipo* especificado.</span><span class="sxs-lookup"><span data-stu-id="a4a43-131">Once a process does not require further notifications, the process must call [**UninitializeNapAgentNotifier**](uninitializenapagentnotifier.md) for the specified *type*.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4a43-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a4a43-132">Requirements</span></span>



| <span data-ttu-id="a4a43-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="a4a43-133">Requirement</span></span> | <span data-ttu-id="a4a43-134">Valor</span><span class="sxs-lookup"><span data-stu-id="a4a43-134">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="a4a43-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a4a43-135">Minimum supported client</span></span><br/> | <span data-ttu-id="a4a43-136">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a4a43-136">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="a4a43-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a4a43-137">Minimum supported server</span></span><br/> | <span data-ttu-id="a4a43-138">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a4a43-138">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="a4a43-139">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a4a43-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="a4a43-140"><dt>NapUtil. h</dt></span><span class="sxs-lookup"><span data-stu-id="a4a43-140"><dt>NapUtil.h</dt></span></span> </dl> |
| <span data-ttu-id="a4a43-141">DLL</span><span class="sxs-lookup"><span data-stu-id="a4a43-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a4a43-142"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a4a43-142"><dt>Qutil.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a4a43-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="a4a43-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4a43-144">**UninitializeNapAgentNotifier**</span><span class="sxs-lookup"><span data-stu-id="a4a43-144">**UninitializeNapAgentNotifier**</span></span>](uninitializenapagentnotifier.md)
</dt> </dl>

 

 





