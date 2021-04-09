---
description: Instala um novo dispositivo. O usuário é solicitado a selecionar o dispositivo.
ms.assetid: 9bdee82c-1d0a-41ea-8b42-7ad96ac37663
title: Função InstallNewDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InstallNewDevice
api_type:
- DllExport
api_location:
- NewDev.dll
ms.openlocfilehash: 76a458ae071c61b9f1030aad535c4d4c6a31078c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089441"
---
# <a name="installnewdevice-function"></a><span data-ttu-id="60be0-104">Função InstallNewDevice</span><span class="sxs-lookup"><span data-stu-id="60be0-104">InstallNewDevice function</span></span>

<span data-ttu-id="60be0-105">Instala um novo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="60be0-105">Installs a new device.</span></span> <span data-ttu-id="60be0-106">O usuário é solicitado a selecionar o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="60be0-106">The user is prompted to select the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="60be0-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="60be0-107">Syntax</span></span>


```C++
BOOL WINAPI InstallNewDevice(
  _In_  HWND   hwndParent,
  _In_  LPGUID ClassGuid,
  _Out_ PDWORD pReboot
);
```



## <a name="parameters"></a><span data-ttu-id="60be0-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="60be0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60be0-109">*hwndParent* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="60be0-109">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60be0-110">Um identificador para a janela de nível superior a ser usado para qualquer interface do usuário necessária.</span><span class="sxs-lookup"><span data-stu-id="60be0-110">A handle to the top-level window to be used for any required user interface.</span></span>

</dd> <dt>

<span data-ttu-id="60be0-111">*ClassGuid* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="60be0-111">*ClassGuid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60be0-112">Um ponteiro para um **GUID** de classe.</span><span class="sxs-lookup"><span data-stu-id="60be0-112">A pointer to a class **GUID**.</span></span> <span data-ttu-id="60be0-113">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="60be0-113">This parameter is optional.</span></span> <span data-ttu-id="60be0-114">Se esse parâmetro for **nulo**, o usuário será iniciado na página opção de detecção.</span><span class="sxs-lookup"><span data-stu-id="60be0-114">If this parameter is **NULL**, the user starts at the detection choice page.</span></span> <span data-ttu-id="60be0-115">Se esse parâmetro for **GUID \_ NULL** ou **GUID \_ DEVCLASS \_ Unknown**, o usuário será iniciado na página de seleção de classe.</span><span class="sxs-lookup"><span data-stu-id="60be0-115">If this parameter is **GUID\_NULL** or **GUID\_DEVCLASS\_UNKNOWN**, the user starts at the class selection page.</span></span>

</dd> <dt>

<span data-ttu-id="60be0-116">*Preboot* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="60be0-116">*pReboot* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="60be0-117">Um ponteiro para uma variável que recebe o status de reinicialização.</span><span class="sxs-lookup"><span data-stu-id="60be0-117">A pointer to a variable that receives the reboot status.</span></span> <span data-ttu-id="60be0-118">Esse parâmetro pode ser **di \_ NEEDRESTART** ou **di \_ NEEDREBOOT**.</span><span class="sxs-lookup"><span data-stu-id="60be0-118">This parameter can be **DI\_NEEDRESTART** or **DI\_NEEDREBOOT**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60be0-119">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="60be0-119">Return value</span></span>

<span data-ttu-id="60be0-120">Se a função for bem-sucedida, o valor retornado será diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="60be0-120">If the function succeeds, the return value is nonzero.</span></span>

<span data-ttu-id="60be0-121">Se a função falhar, o valor retornado será zero.</span><span class="sxs-lookup"><span data-stu-id="60be0-121">If the function fails, the return value is zero.</span></span> <span data-ttu-id="60be0-122">Para obter informações de erro estendidas, chame [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="60be0-122">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="60be0-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="60be0-123">Remarks</span></span>

<span data-ttu-id="60be0-124">Esta função não tem biblioteca de importação associada.</span><span class="sxs-lookup"><span data-stu-id="60be0-124">This function has no associated import library.</span></span> <span data-ttu-id="60be0-125">Você deve usar as funções [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a NewDev.dll.</span><span class="sxs-lookup"><span data-stu-id="60be0-125">You must use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to NewDev.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="60be0-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="60be0-126">Requirements</span></span>



| <span data-ttu-id="60be0-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="60be0-127">Requirement</span></span> | <span data-ttu-id="60be0-128">Valor</span><span class="sxs-lookup"><span data-stu-id="60be0-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="60be0-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="60be0-129">Minimum supported client</span></span><br/> | <span data-ttu-id="60be0-130">Windows XP</span><span class="sxs-lookup"><span data-stu-id="60be0-130">Windows XP</span></span><br/>                                                                 |
| <span data-ttu-id="60be0-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="60be0-131">Minimum supported server</span></span><br/> | <span data-ttu-id="60be0-132">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="60be0-132">Windows Server 2003</span></span><br/>                                                        |
| <span data-ttu-id="60be0-133">DLL</span><span class="sxs-lookup"><span data-stu-id="60be0-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="60be0-134"><dt>NewDev.dll</dt></span><span class="sxs-lookup"><span data-stu-id="60be0-134"><dt>NewDev.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60be0-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="60be0-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60be0-136">Funções de gerenciamento de dispositivo</span><span class="sxs-lookup"><span data-stu-id="60be0-136">Device Management Functions</span></span>](device-management-functions.md)
</dt> </dl>

 

