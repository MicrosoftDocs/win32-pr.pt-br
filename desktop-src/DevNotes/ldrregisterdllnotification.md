---
description: Registra para notificação quando uma DLL é carregada pela primeira vez. Essa notificação ocorre antes que a vinculação dinâmica ocorra.
ms.assetid: c2757aa0-76fa-427a-a4f6-cb26e7f7d0d1
title: Função LdrRegisterDllNotification
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LdrRegisterDllNotification
api_type:
- DllExport
api_location:
- ntdll.dll
ms.openlocfilehash: 82ec05a24f4cccc89cece666b18cb63412a78259
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010105"
---
# <a name="ldrregisterdllnotification-function"></a><span data-ttu-id="683fe-104">Função LdrRegisterDllNotification</span><span class="sxs-lookup"><span data-stu-id="683fe-104">LdrRegisterDllNotification function</span></span>

<span data-ttu-id="683fe-105">\[Essa função pode ser alterada ou removida do Windows sem aviso prévio.\]</span><span class="sxs-lookup"><span data-stu-id="683fe-105">\[This function may be changed or removed from Windows without further notice.\]</span></span>

<span data-ttu-id="683fe-106">Registra para notificação quando uma DLL é carregada pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="683fe-106">Registers for notification when a DLL is first loaded.</span></span> <span data-ttu-id="683fe-107">Essa notificação ocorre antes que a vinculação dinâmica ocorra.</span><span class="sxs-lookup"><span data-stu-id="683fe-107">This notification occurs before dynamic linking takes place.</span></span>

## <a name="syntax"></a><span data-ttu-id="683fe-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="683fe-108">Syntax</span></span>


```C++
NTSTATUS NTAPI LdrRegisterDllNotification(
  _In_     ULONG                          Flags,
  _In_     PLDR_DLL_NOTIFICATION_FUNCTION NotificationFunction,
  _In_opt_ PVOID                          Context,
  _Out_    PVOID                          *Cookie
);
```



## <a name="parameters"></a><span data-ttu-id="683fe-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="683fe-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="683fe-110">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="683fe-110">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="683fe-111">Esse parâmetro deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="683fe-111">This parameter must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="683fe-112">*NotificationFunction* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="683fe-112">*NotificationFunction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="683fe-113">Um ponteiro para uma função de retorno de chamada de notificação [*LdrDllNotification*](ldrdllnotification.md) para chamar quando a dll é carregada.</span><span class="sxs-lookup"><span data-stu-id="683fe-113">A pointer to an [*LdrDllNotification*](ldrdllnotification.md) notification callback function to call when the DLL is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="683fe-114">*Contexto* \[ do em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="683fe-114">*Context* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="683fe-115">Um ponteiro para dados de contexto para a função de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="683fe-115">A pointer to context data for the callback function.</span></span>

</dd> <dt>

<span data-ttu-id="683fe-116">*Cookie* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="683fe-116">*Cookie* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="683fe-117">Um ponteiro para uma variável para receber um identificador para a função de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="683fe-117">A pointer to a variable to receive an identifier for the callback function.</span></span> <span data-ttu-id="683fe-118">Esse identificador é usado para cancelar o registro da função de retorno de chamada de notificação.</span><span class="sxs-lookup"><span data-stu-id="683fe-118">This identifier is used to unregister the notification callback function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="683fe-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="683fe-119">Return value</span></span>

<span data-ttu-id="683fe-120">Se a função for bem-sucedida, ela retornará o **status \_ êxito**.</span><span class="sxs-lookup"><span data-stu-id="683fe-120">If the function succeeds, it returns **STATUS\_SUCCESS**.</span></span>

<span data-ttu-id="683fe-121">Os formulários e o significado dos códigos de erro **NTSTATUS** são listados no arquivo de cabeçalho Ntstatus. h disponível no WDK e são descritos na documentação do WDK.</span><span class="sxs-lookup"><span data-stu-id="683fe-121">The forms and significance of **NTSTATUS** error codes are listed in the Ntstatus.h header file available in the WDK, and are described in the WDK documentation.</span></span>

## <a name="remarks"></a><span data-ttu-id="683fe-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="683fe-122">Remarks</span></span>

<span data-ttu-id="683fe-123">Esta função não tem nenhum arquivo de cabeçalho associado.</span><span class="sxs-lookup"><span data-stu-id="683fe-123">This function has no associated header file.</span></span> <span data-ttu-id="683fe-124">A biblioteca de importação associada, ntdll. lib, está disponível no WDK.</span><span class="sxs-lookup"><span data-stu-id="683fe-124">The associated import library, Ntdll.lib, is available in the WDK.</span></span> <span data-ttu-id="683fe-125">Você também pode usar as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a Ntdll.dll.</span><span class="sxs-lookup"><span data-stu-id="683fe-125">You can also use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Ntdll.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="683fe-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="683fe-126">Requirements</span></span>



| <span data-ttu-id="683fe-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="683fe-127">Requirement</span></span> | <span data-ttu-id="683fe-128">Valor</span><span class="sxs-lookup"><span data-stu-id="683fe-128">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="683fe-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="683fe-129">Minimum supported client</span></span><br/> | <span data-ttu-id="683fe-130">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="683fe-130">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="683fe-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="683fe-131">Minimum supported server</span></span><br/> | <span data-ttu-id="683fe-132">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="683fe-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="683fe-133">DLL</span><span class="sxs-lookup"><span data-stu-id="683fe-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="683fe-134"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="683fe-134"><dt>Ntdll.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="683fe-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="683fe-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="683fe-136">*LdrDllNotification*</span><span class="sxs-lookup"><span data-stu-id="683fe-136">*LdrDllNotification*</span></span>](ldrdllnotification.md)
</dt> <dt>

[<span data-ttu-id="683fe-137">**LdrUnregisterDllNotification**</span><span class="sxs-lookup"><span data-stu-id="683fe-137">**LdrUnregisterDllNotification**</span></span>](ldrunregisterdllnotification.md)
</dt> </dl>

 

 
