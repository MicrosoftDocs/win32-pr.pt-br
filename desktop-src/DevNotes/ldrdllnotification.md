---
description: Uma função de retorno de chamada de notificação especificada com a função LdrRegisterDllNotification.
ms.assetid: 12202797-c80c-4fa3-9cc4-dcb1a9f01551
title: Função de retorno de chamada LdrDllNotification
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LdrDllNotification
- PLDR_DLL_NOTIFICATION_FUNCTION
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: e29cd7b17c634250f56cbafcf86379449ac88199
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826117"
---
# <a name="ldrdllnotification-callback-function"></a><span data-ttu-id="65051-103">Função de retorno de chamada LdrDllNotification</span><span class="sxs-lookup"><span data-stu-id="65051-103">LdrDllNotification callback function</span></span>

<span data-ttu-id="65051-104">\[Essa função pode ser alterada ou removida do Windows sem aviso prévio.\]</span><span class="sxs-lookup"><span data-stu-id="65051-104">\[This function may be changed or removed from Windows without further notice.\]</span></span>

<span data-ttu-id="65051-105">Uma função de retorno de chamada de notificação especificada com a função [**LdrRegisterDllNotification**](ldrregisterdllnotification.md) .</span><span class="sxs-lookup"><span data-stu-id="65051-105">A notification callback function specified with the [**LdrRegisterDllNotification**](ldrregisterdllnotification.md) function.</span></span> <span data-ttu-id="65051-106">O carregador chama essa função quando uma DLL é carregada pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="65051-106">The loader calls this function when a DLL is first loaded.</span></span>

<span data-ttu-id="65051-107">**AVISO:** Não é seguro que a função de retorno de chamada de notificação chame funções em qualquer DLL.</span><span class="sxs-lookup"><span data-stu-id="65051-107">**Warning:** It is unsafe for the notification callback function to call functions in any DLL.</span></span>

## <a name="syntax"></a><span data-ttu-id="65051-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="65051-108">Syntax</span></span>


```C++
VOID CALLBACK LdrDllNotification(
  _In_     ULONG                       NotificationReason,
  _In_     PCLDR_DLL_NOTIFICATION_DATA NotificationData,
  _In_opt_ PVOID                       Context
);
```



## <a name="parameters"></a><span data-ttu-id="65051-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="65051-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65051-110">*NotificationReason* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="65051-110">*NotificationReason* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65051-111">O motivo pelo qual a função de retorno de chamada de notificação foi chamada.</span><span class="sxs-lookup"><span data-stu-id="65051-111">The reason that the notification callback function was called.</span></span> <span data-ttu-id="65051-112">Esse parâmetro pode usar um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="65051-112">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="65051-113">Valor</span><span class="sxs-lookup"><span data-stu-id="65051-113">Value</span></span>                                                                                                                                                                                                                                                                                        | <span data-ttu-id="65051-114">Significado</span><span class="sxs-lookup"><span data-stu-id="65051-114">Meaning</span></span>                                                                                                                               |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LDR_DLL_NOTIFICATION_REASON_LOADED"></span><span id="ldr_dll_notification_reason_loaded"></span><dl> <span data-ttu-id="65051-115"><dt>**LDR \_ Motivo da notificação de DLL \_ \_ \_ carregado**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="65051-115"><dt>**LDR\_DLL\_NOTIFICATION\_REASON\_LOADED**</dt> <dt>1</dt></span></span> </dl>       | <span data-ttu-id="65051-116">A DLL foi carregada.</span><span class="sxs-lookup"><span data-stu-id="65051-116">The DLL was loaded.</span></span> <span data-ttu-id="65051-117">O parâmetro *NotificationData* aponta para a estrutura de dados de notificação de uma **\_ dll LDR \_ carregada \_ \_** .</span><span class="sxs-lookup"><span data-stu-id="65051-117">The *NotificationData* parameter points to an **LDR\_DLL\_LOADED\_NOTIFICATION\_DATA** structure.</span></span> <br/>     |
| <span id="LDR_DLL_NOTIFICATION_REASON_UNLOADED"></span><span id="ldr_dll_notification_reason_unloaded"></span><dl> <span data-ttu-id="65051-118"><dt>**LDR \_ Motivo da notificação de DLL \_ \_ \_ descarregado**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="65051-118"><dt>**LDR\_DLL\_NOTIFICATION\_REASON\_UNLOADED**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="65051-119">A DLL foi descarregada.</span><span class="sxs-lookup"><span data-stu-id="65051-119">The DLL was unloaded.</span></span> <span data-ttu-id="65051-120">O parâmetro *NotificationData* aponta para uma estrutura de **\_ \_ \_ \_ dados de notificação descarregada da DLL de LDR** .</span><span class="sxs-lookup"><span data-stu-id="65051-120">The *NotificationData* parameter points to an **LDR\_DLL\_UNLOADED\_NOTIFICATION\_DATA** structure.</span></span> <br/> |



 

</dd> <dt>

<span data-ttu-id="65051-121">*NotificationData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="65051-121">*NotificationData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65051-122">Um ponteiro para uma constante **de \_ \_ notificação de dll DDL de LDR** que contém dados de notificação.</span><span class="sxs-lookup"><span data-stu-id="65051-122">A pointer to a constant **LDR\_DLL\_NOTIFICATION** union that contains notification data.</span></span> <span data-ttu-id="65051-123">Essa União tem a seguinte definição:</span><span class="sxs-lookup"><span data-stu-id="65051-123">This union has the following definition:</span></span>

``` syntax
typedef union _LDR_DLL_NOTIFICATION_DATA {
    LDR_DLL_LOADED_NOTIFICATION_DATA Loaded;
    LDR_DLL_UNLOADED_NOTIFICATION_DATA Unloaded;
} LDR_DLL_NOTIFICATION_DATA, *PLDR_DLL_NOTIFICATION_DATA;
```

<span data-ttu-id="65051-124">A estrutura de **\_ dados de notificação da dll LDR \_ carregada \_ \_** tem a seguinte definição:</span><span class="sxs-lookup"><span data-stu-id="65051-124">The **LDR\_DLL\_LOADED\_NOTIFICATION\_DATA** structure has the following definition:</span></span>

``` syntax
typedef struct _LDR_DLL_LOADED_NOTIFICATION_DATA {
    ULONG Flags;                    //Reserved.
    PCUNICODE_STRING FullDllName;   //The full path name of the DLL module.
    PCUNICODE_STRING BaseDllName;   //The base file name of the DLL module.
    PVOID DllBase;                  //A pointer to the base address for the DLL in memory.
    ULONG SizeOfImage;              //The size of the DLL image, in bytes.
} LDR_DLL_LOADED_NOTIFICATION_DATA, *PLDR_DLL_LOADED_NOTIFICATION_DATA;
```

<span data-ttu-id="65051-125">A estrutura de dados de notificação de a **dll de LDR \_ \_ descarregada \_ \_** tem a seguinte definição:</span><span class="sxs-lookup"><span data-stu-id="65051-125">The **LDR\_DLL\_UNLOADED\_NOTIFICATION\_DATA** structure has the following definition:</span></span>

``` syntax
typedef struct _LDR_DLL_UNLOADED_NOTIFICATION_DATA {
    ULONG Flags;                    //Reserved.
    PCUNICODE_STRING FullDllName;   //The full path name of the DLL module.
    PCUNICODE_STRING BaseDllName;   //The base file name of the DLL module.
    PVOID DllBase;                  //A pointer to the base address for the DLL in memory.
    ULONG SizeOfImage;              //The size of the DLL image, in bytes.
} LDR_DLL_UNLOADED_NOTIFICATION_DATA, *PLDR_DLL_UNLOADED_NOTIFICATION_DATA;
```

</dd> <dt>

<span data-ttu-id="65051-126">*Contexto* \[ do em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="65051-126">*Context* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="65051-127">Um ponteiro para dados de contexto para a função de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="65051-127">A pointer to context data for the callback function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65051-128">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="65051-128">Return value</span></span>

<span data-ttu-id="65051-129">Essa função de retorno de chamada não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="65051-129">This callback function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="65051-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="65051-130">Remarks</span></span>

<span data-ttu-id="65051-131">A função de retorno de chamada de notificação é chamada antes que a vinculação dinâmica ocorra.</span><span class="sxs-lookup"><span data-stu-id="65051-131">The notification callback function is called before dynamic linking takes place.</span></span>

## <a name="requirements"></a><span data-ttu-id="65051-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="65051-132">Requirements</span></span>



| <span data-ttu-id="65051-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="65051-133">Requirement</span></span> | <span data-ttu-id="65051-134">Valor</span><span class="sxs-lookup"><span data-stu-id="65051-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="65051-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="65051-135">Minimum supported client</span></span><br/> | <span data-ttu-id="65051-136">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="65051-136">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="65051-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="65051-137">Minimum supported server</span></span><br/> | <span data-ttu-id="65051-138">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="65051-138">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="65051-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="65051-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65051-140">**LdrRegisterDllNotification**</span><span class="sxs-lookup"><span data-stu-id="65051-140">**LdrRegisterDllNotification**</span></span>](ldrregisterdllnotification.md)
</dt> <dt>

[<span data-ttu-id="65051-141">**LdrUnregisterDllNotification**</span><span class="sxs-lookup"><span data-stu-id="65051-141">**LdrUnregisterDllNotification**</span></span>](ldrunregisterdllnotification.md)
</dt> </dl>

 

 




