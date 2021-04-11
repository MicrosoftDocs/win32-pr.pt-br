---
description: Recupera o modo de segurança atual do Windows. O Windows pode estar no modo bloqueado, no modo normal desbloqueado ou no modo de avaliação.
ms.assetid: FD280818-C6DE-4CEA-A772-E239A8DB891F
title: Função WldpQueryWindowsLockdownMode (Wldp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WldpQueryWindowsLockdownMode
api_type:
- DllExport
api_location:
- wldp.dll
ms.openlocfilehash: fc746270a0634525154417cfba7e1529bee7edfb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164119"
---
# <a name="wldpquerywindowslockdownmode-function"></a><span data-ttu-id="0b9b0-104">Função WldpQueryWindowsLockdownMode</span><span class="sxs-lookup"><span data-stu-id="0b9b0-104">WldpQueryWindowsLockdownMode function</span></span>

<span data-ttu-id="0b9b0-105">Recupera o modo de segurança atual do Windows.</span><span class="sxs-lookup"><span data-stu-id="0b9b0-105">Retrieves the current Windows secure mode.</span></span> <span data-ttu-id="0b9b0-106">O Windows pode estar no modo bloqueado, no modo normal desbloqueado ou no modo de avaliação.</span><span class="sxs-lookup"><span data-stu-id="0b9b0-106">Windows can be in locked mode, unlocked normal mode, or trial mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b9b0-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0b9b0-107">Syntax</span></span>


```C++
 WINAPI WldpQueryWindowsLockdownMode(
  _Out_ PWLDP_WINDOWS_LOCKDOWN_MODE lockdownMode
);
```



## <a name="parameters"></a><span data-ttu-id="0b9b0-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0b9b0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b9b0-109">*lockdownmode* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="0b9b0-109">*lockdownMode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0b9b0-110">Em caso de sucesso, retorna um [**\_ modo de \_ bloqueio \_ do Windows PWLDP**](wldp-windows-lockdown-mode.md) que indica o modo de segurança para o dispositivo atual do Windows 10.</span><span class="sxs-lookup"><span data-stu-id="0b9b0-110">On success, returns a [**PWLDP\_WINDOWS\_LOCKDOWN\_MODE**](wldp-windows-lockdown-mode.md) that indicates the secure mode for the current Windows 10 device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b9b0-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0b9b0-111">Return value</span></span>

<span data-ttu-id="0b9b0-112">Esse método retornará **S \_ OK** , se for bem-sucedido ou um código de falha.</span><span class="sxs-lookup"><span data-stu-id="0b9b0-112">This method returns **S\_OK** if successful or a failure code otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b9b0-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0b9b0-113">Requirements</span></span>



| <span data-ttu-id="0b9b0-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b9b0-114">Requirement</span></span> | <span data-ttu-id="0b9b0-115">Valor</span><span class="sxs-lookup"><span data-stu-id="0b9b0-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="0b9b0-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0b9b0-116">Minimum supported client</span></span><br/> | <span data-ttu-id="0b9b0-117">\[Somente aplicativos da área de trabalho do Windows 10, versão 1803\]</span><span class="sxs-lookup"><span data-stu-id="0b9b0-117">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="0b9b0-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0b9b0-118">Minimum supported server</span></span><br/> | <span data-ttu-id="0b9b0-119">\[Somente aplicativos da área de trabalho do Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="0b9b0-119">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="0b9b0-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0b9b0-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="0b9b0-121"><dt>Wldp. h</dt></span><span class="sxs-lookup"><span data-stu-id="0b9b0-121"><dt>Wldp.h</dt></span></span> </dl>   |
| <span data-ttu-id="0b9b0-122">DLL</span><span class="sxs-lookup"><span data-stu-id="0b9b0-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0b9b0-123"><dt>Wldp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0b9b0-123"><dt>Wldp.dll</dt></span></span> </dl> |



 

 




