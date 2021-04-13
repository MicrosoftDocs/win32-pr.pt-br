---
title: Função UninitializeNapAgentNotifier (NapUtil. h)
description: Cancela a assinatura do processo de chamada de notificações de alteração de estado NapAgent e notificações de alteração de estado de quarentena.
ms.assetid: b676ee33-caf6-48f0-acf8-5be1b23c62fe
keywords:
- Função UninitializeNapAgentNotifier NAP
topic_type:
- apiref
api_name:
- UninitializeNapAgentNotifier
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5d68b43fba64be82908d73803113f871b08c93c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369478"
---
# <a name="uninitializenapagentnotifier-function"></a><span data-ttu-id="f7df3-104">Função UninitializeNapAgentNotifier</span><span class="sxs-lookup"><span data-stu-id="f7df3-104">UninitializeNapAgentNotifier function</span></span>

> [!Note]  
> <span data-ttu-id="f7df3-105">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="f7df3-105">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="f7df3-106">A função **UninitializeNapAgentNotifier** cancela a assinatura do processo de chamada das notificações de alteração de estado NapAgent e das notificações de alteração de estado de quarentena.</span><span class="sxs-lookup"><span data-stu-id="f7df3-106">The **UninitializeNapAgentNotifier** function unsubscribes the calling process from NapAgent state change notifications and quarantine state change notifications.</span></span> <span data-ttu-id="f7df3-107">Essas notificações são fornecidas pelo serviço NapAgent.</span><span class="sxs-lookup"><span data-stu-id="f7df3-107">These notifications are provided by the NapAgent service.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7df3-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f7df3-108">Syntax</span></span>


```C++
NAPAPI VOID WINAPI UninitializeNapAgentNotifier(
  _In_ NapNotifyType type
);
```



## <a name="parameters"></a><span data-ttu-id="f7df3-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f7df3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7df3-110">*tipo* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="f7df3-110">*type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7df3-111">Um valor de [**NapNotifyType**](/windows/win32/api/naptypes/ne-naptypes-napnotifytype) que especifica o tipo de notificações de serviço da qual cancelar a assinatura.</span><span class="sxs-lookup"><span data-stu-id="f7df3-111">A [**NapNotifyType**](/windows/win32/api/naptypes/ne-naptypes-napnotifytype) value that specifies the type of service notifications to unsubscribe from.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f7df3-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f7df3-112">Return value</span></span>

<span data-ttu-id="f7df3-113">Esta função não tem valores de retorno.</span><span class="sxs-lookup"><span data-stu-id="f7df3-113">This function has no return values.</span></span>

## <a name="remarks"></a><span data-ttu-id="f7df3-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="f7df3-114">Remarks</span></span>

<span data-ttu-id="f7df3-115">Essa função não é thread-safe.</span><span class="sxs-lookup"><span data-stu-id="f7df3-115">This function is not thread safe.</span></span>

<span data-ttu-id="f7df3-116">Cada processo assinado para notificações de serviço NapAgent do *tipo* especificado deve chamar **UninitializeNapAgentNotifier** para cancelar a assinatura de notificações.</span><span class="sxs-lookup"><span data-stu-id="f7df3-116">Each process subscribed to NapAgent service notifications of the specified *type* must call **UninitializeNapAgentNotifier** to unsubscribe from notifications.</span></span> <span data-ttu-id="f7df3-117">Se um processo for assinado para mais de um tipo de notificação, ele deverá chamar **UninitializeNapAgentNotifier** uma vez para cada tipo de notificação.</span><span class="sxs-lookup"><span data-stu-id="f7df3-117">If a process is subscribed to more than one type of notification, it must call **UninitializeNapAgentNotifier** once for each type of notification.</span></span>

<span data-ttu-id="f7df3-118">Essa função falhará silenciosamente se o processo não tiver chamado anteriormente [**InitializeNapAgentNotifier**](initializenapagentnotifier.md) para o tipo de notificação.</span><span class="sxs-lookup"><span data-stu-id="f7df3-118">This function will fail silently if the process had not previously called [**InitializeNapAgentNotifier**](initializenapagentnotifier.md) for the notification type.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7df3-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f7df3-119">Requirements</span></span>



| <span data-ttu-id="f7df3-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="f7df3-120">Requirement</span></span> | <span data-ttu-id="f7df3-121">Valor</span><span class="sxs-lookup"><span data-stu-id="f7df3-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f7df3-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f7df3-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f7df3-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f7df3-123">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="f7df3-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f7df3-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f7df3-125">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f7df3-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="f7df3-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f7df3-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="f7df3-127"><dt>NapUtil. h</dt></span><span class="sxs-lookup"><span data-stu-id="f7df3-127"><dt>NapUtil.h</dt></span></span> </dl> |
| <span data-ttu-id="f7df3-128">DLL</span><span class="sxs-lookup"><span data-stu-id="f7df3-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f7df3-129"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f7df3-129"><dt>Qutil.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f7df3-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="f7df3-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7df3-131">**InitializeNapAgentNotifier**</span><span class="sxs-lookup"><span data-stu-id="f7df3-131">**InitializeNapAgentNotifier**</span></span>](initializenapagentnotifier.md)
</dt> </dl>

 

 





