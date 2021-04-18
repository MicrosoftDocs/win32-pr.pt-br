---
description: Cancela a notificação de carregamento de DLL registrada anteriormente chamando a função LdrRegisterDllNotification.
ms.assetid: 18c3a027-e3cb-4083-afdc-00f416a70d8c
title: Função LdrUnregisterDllNotification
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LdrUnregisterDllNotification
api_type:
- DllExport
api_location:
- ntdll.dll
ms.openlocfilehash: 1fee03b4a06d274b495070eb40833b270a795158
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370352"
---
# <a name="ldrunregisterdllnotification-function"></a><span data-ttu-id="1dc3f-103">Função LdrUnregisterDllNotification</span><span class="sxs-lookup"><span data-stu-id="1dc3f-103">LdrUnregisterDllNotification function</span></span>

<span data-ttu-id="1dc3f-104">\[Essa função pode ser alterada ou removida do Windows sem aviso prévio.\]</span><span class="sxs-lookup"><span data-stu-id="1dc3f-104">\[This function may be changed or removed from Windows without further notice.\]</span></span>

<span data-ttu-id="1dc3f-105">Cancela a notificação de carregamento de DLL registrada anteriormente chamando a função [**LdrRegisterDllNotification**](ldrregisterdllnotification.md) .</span><span class="sxs-lookup"><span data-stu-id="1dc3f-105">Cancels DLL load notification previously registered by calling the [**LdrRegisterDllNotification**](ldrregisterdllnotification.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="1dc3f-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1dc3f-106">Syntax</span></span>


```C++
NTSTATUS NTAPI LdrUnregisterDllNotification(
  _In_ PVOID Cookie
);
```



## <a name="parameters"></a><span data-ttu-id="1dc3f-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1dc3f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1dc3f-108">*Cookie* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1dc3f-108">*Cookie* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1dc3f-109">Um ponteiro para o identificador de retorno de chamada recebido da chamadas [**LdrRegisterDllNotification**](ldrregisterdllnotification.md) registradas para notificação.</span><span class="sxs-lookup"><span data-stu-id="1dc3f-109">A pointer to the callback identifier received from the [**LdrRegisterDllNotification**](ldrregisterdllnotification.md) call that registered for notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1dc3f-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1dc3f-110">Return value</span></span>

<span data-ttu-id="1dc3f-111">Retorna um **NTSTATUS** ou um código de erro.</span><span class="sxs-lookup"><span data-stu-id="1dc3f-111">Returns an **NTSTATUS** or error code.</span></span>

<span data-ttu-id="1dc3f-112">Se a função for bem-sucedida, ela retornará o **status \_ êxito**.</span><span class="sxs-lookup"><span data-stu-id="1dc3f-112">If the function succeeds, it returns **STATUS\_SUCCESS**.</span></span>

<span data-ttu-id="1dc3f-113">Se a função de retorno de chamada não for encontrada, a função retornará a **dll de status \_ \_ não \_ encontrada**.</span><span class="sxs-lookup"><span data-stu-id="1dc3f-113">If the callback function is not found, the function returns **STATUS\_DLL\_NOT\_FOUND**.</span></span>

<span data-ttu-id="1dc3f-114">Os formulários e o significado dos códigos de erro **NTSTATUS** são listados no arquivo de cabeçalho Ntstatus. h disponível no WDK e são descritos na documentação do WDK.</span><span class="sxs-lookup"><span data-stu-id="1dc3f-114">The forms and significance of **NTSTATUS** error codes are listed in the Ntstatus.h header file available in the WDK, and are described in the WDK documentation.</span></span>

## <a name="remarks"></a><span data-ttu-id="1dc3f-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="1dc3f-115">Remarks</span></span>

<span data-ttu-id="1dc3f-116">Esta função não tem nenhum arquivo de cabeçalho associado.</span><span class="sxs-lookup"><span data-stu-id="1dc3f-116">This function has no associated header file.</span></span> <span data-ttu-id="1dc3f-117">A biblioteca de importação associada, ntdll. lib, está disponível no WDK.</span><span class="sxs-lookup"><span data-stu-id="1dc3f-117">The associated import library, Ntdll.lib, is available in the WDK.</span></span> <span data-ttu-id="1dc3f-118">Você também pode usar as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a Ntdll.dll.</span><span class="sxs-lookup"><span data-stu-id="1dc3f-118">You can also use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Ntdll.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="1dc3f-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1dc3f-119">Requirements</span></span>



| <span data-ttu-id="1dc3f-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="1dc3f-120">Requirement</span></span> | <span data-ttu-id="1dc3f-121">Valor</span><span class="sxs-lookup"><span data-stu-id="1dc3f-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="1dc3f-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1dc3f-122">Minimum supported client</span></span><br/> | <span data-ttu-id="1dc3f-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1dc3f-123">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="1dc3f-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1dc3f-124">Minimum supported server</span></span><br/> | <span data-ttu-id="1dc3f-125">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="1dc3f-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="1dc3f-126">DLL</span><span class="sxs-lookup"><span data-stu-id="1dc3f-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1dc3f-127"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1dc3f-127"><dt>Ntdll.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1dc3f-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="1dc3f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1dc3f-129">**LdrRegisterDllNotification**</span><span class="sxs-lookup"><span data-stu-id="1dc3f-129">**LdrRegisterDllNotification**</span></span>](ldrregisterdllnotification.md)
</dt> </dl>

 

 
