---
description: Obtém informações de versão sobre o sistema operacional em execução no momento.
ms.assetid: F04F0981-A07D-4B38-9DE4-B8461EAFC19F
title: Função RtlGetVersion (Ntddk. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlGetVersion
api_type:
- DllExport
api_location:
- Ntdll.dll
- NtosKrnl.exe
ms.openlocfilehash: a6a026ee55a6ccd75162915729070ad76f621bc8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089073"
---
# <a name="rtlgetversion-function"></a><span data-ttu-id="d7c08-103">Função RtlGetVersion</span><span class="sxs-lookup"><span data-stu-id="d7c08-103">RtlGetVersion function</span></span>

<span data-ttu-id="d7c08-104">Obtém informações de versão sobre o sistema operacional em execução no momento.</span><span class="sxs-lookup"><span data-stu-id="d7c08-104">Gets version information about the currently running operating system.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7c08-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d7c08-105">Syntax</span></span>


```C++
NTSTATUS RtlGetVersion(
  _Out_ PRTL_OSVERSIONINFOW lpVersionInformation
);
```



## <a name="parameters"></a><span data-ttu-id="d7c08-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d7c08-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7c08-107">*lpVersionInformation* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="d7c08-107">*lpVersionInformation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d7c08-108">Ponteiro para uma estrutura [**\_ OSVERSIONINFOW DPE**](/windows-hardware/drivers/ddi/wdm/ns-wdm-_osversioninfow) ou uma estrutura [**\_ OSVERSIONINFOEXW DPE**](/windows-hardware/drivers/ddi/wdm/ns-wdm-_osversioninfoexw) que contém as informações de versão sobre o sistema operacional em execução no momento.</span><span class="sxs-lookup"><span data-stu-id="d7c08-108">Pointer to either a [**RTL\_OSVERSIONINFOW**](/windows-hardware/drivers/ddi/wdm/ns-wdm-_osversioninfow) structure or a [**RTL\_OSVERSIONINFOEXW**](/windows-hardware/drivers/ddi/wdm/ns-wdm-_osversioninfoexw) structure that contains the version information about the currently running operating system.</span></span> <span data-ttu-id="d7c08-109">Um chamador especifica qual estrutura de entrada é usada definindo o membro **dwOSVersionInfoSize** da estrutura como o tamanho em bytes da estrutura usada.</span><span class="sxs-lookup"><span data-stu-id="d7c08-109">A caller specifies which input structure is used by setting the **dwOSVersionInfoSize** member of the structure to the size in bytes of the structure that is used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7c08-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d7c08-110">Return value</span></span>

<span data-ttu-id="d7c08-111">Retorna o STATUS \_ Success.</span><span class="sxs-lookup"><span data-stu-id="d7c08-111">Returns STATUS\_SUCCESS.</span></span>

## <a name="remarks"></a><span data-ttu-id="d7c08-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="d7c08-112">Remarks</span></span>

<span data-ttu-id="d7c08-113">**RtlGetVersion** é o equivalente da função [**GetVersionEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa) no SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="d7c08-113">**RtlGetVersion** is the equivalent of the [**GetVersionEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa) function in the Windows SDK.</span></span> <span data-ttu-id="d7c08-114">Consulte o exemplo na SDK do Windows que mostra como obter a versão do sistema.</span><span class="sxs-lookup"><span data-stu-id="d7c08-114">See the example in the Windows SDK that shows how to get the system version.</span></span>

<span data-ttu-id="d7c08-115">Ao usar **RtlGetVersion** para determinar se uma versão específica do sistema operacional está em execução, um chamador deve verificar se há números de versão que sejam maiores ou iguais ao número de versão necessário.</span><span class="sxs-lookup"><span data-stu-id="d7c08-115">When using **RtlGetVersion** to determine whether a particular version of the operating system is running, a caller should check for version numbers that are greater than or equal to the required version number.</span></span> <span data-ttu-id="d7c08-116">Isso garante que um teste de versão tenha sucesso para versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="d7c08-116">This ensures that a version test succeeds for later versions of Windows.</span></span>

<span data-ttu-id="d7c08-117">Como os recursos do sistema operacional podem ser adicionados em uma DLL redistribuível, a verificação apenas dos números de versão principal e secundária não é a maneira mais confiável de verificar a presença de um recurso específico do sistema.</span><span class="sxs-lookup"><span data-stu-id="d7c08-117">Because operating system features can be added in a redistributable DLL, checking only the major and minor version numbers is not the most reliable way to verify the presence of a specific system feature.</span></span> <span data-ttu-id="d7c08-118">Um driver deve usar [**RtlVerifyVersionInfo**](/windows-hardware/drivers/ddi/wdm/nf-wdm-rtlverifyversioninfo) para testar a presença de um recurso específico do sistema.</span><span class="sxs-lookup"><span data-stu-id="d7c08-118">A driver should use [**RtlVerifyVersionInfo**](/windows-hardware/drivers/ddi/wdm/nf-wdm-rtlverifyversioninfo) to test for the presence of a specific system feature.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7c08-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d7c08-119">Requirements</span></span>



| <span data-ttu-id="d7c08-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7c08-120">Requirement</span></span> | <span data-ttu-id="d7c08-121">Valor</span><span class="sxs-lookup"><span data-stu-id="d7c08-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7c08-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d7c08-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d7c08-123">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d7c08-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="d7c08-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d7c08-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d7c08-125">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d7c08-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="d7c08-126">Plataforma de destino</span><span class="sxs-lookup"><span data-stu-id="d7c08-126">Target platform</span></span><br/>          | <dl> <span data-ttu-id="d7c08-127"><dt>[Universal](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt></span><span class="sxs-lookup"><span data-stu-id="d7c08-127"><dt>[Universal](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt></span></span> </dl>                  |
| <span data-ttu-id="d7c08-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d7c08-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="d7c08-129"><dt>Ntddk. h (incluir Ntddk. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d7c08-129"><dt>Ntddk.h (include Ntddk.h)</dt></span></span> </dl>                                                     |
| <span data-ttu-id="d7c08-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d7c08-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="d7c08-131"><dt>Ntdll. lib; </dt> <dt>NtosKrnl. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d7c08-131"><dt>Ntdll.lib; </dt> <dt>NtosKrnl.lib</dt></span></span> </dl> |
| <span data-ttu-id="d7c08-132">DLL</span><span class="sxs-lookup"><span data-stu-id="d7c08-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d7c08-133"><dt>Ntdll.dll; </dt> <dt>NtosKrnl.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d7c08-133"><dt>Ntdll.dll; </dt> <dt>NtosKrnl.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7c08-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="d7c08-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7c08-135">**PsGetVersion**</span><span class="sxs-lookup"><span data-stu-id="d7c08-135">**PsGetVersion**</span></span>](/windows-hardware/drivers/ddi/wdm/nf-wdm-psgetversion)
</dt> </dl>

 

 
