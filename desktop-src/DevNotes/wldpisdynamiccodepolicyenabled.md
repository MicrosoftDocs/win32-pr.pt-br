---
description: Recupera um valor que descreve o status de imposição de política do Device Guard para código dinâmico do .NET.
ms.assetid: 11E6C631-0FF8-4DB2-931A-1012B3CA4357
title: Função WldpIsDynamicCodePolicyEnabled (Wldp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WldpIsDynamicCodePolicyEnabled
api_type:
- DllExport
api_location:
- wldp.dll
ms.openlocfilehash: 4df0555f89e9c575a7d97b69a5252c17936eb3d2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104088889"
---
# <a name="wldpisdynamiccodepolicyenabled-function"></a><span data-ttu-id="7253a-103">Função WldpIsDynamicCodePolicyEnabled</span><span class="sxs-lookup"><span data-stu-id="7253a-103">WldpIsDynamicCodePolicyEnabled function</span></span>

<span data-ttu-id="7253a-104">Recupera um valor que descreve o status de imposição de política do Device Guard para código dinâmico do .NET.</span><span class="sxs-lookup"><span data-stu-id="7253a-104">Retrieves a value that describes the Device Guard policy enforcement status for .NET dynamic code.</span></span>

## <a name="syntax"></a><span data-ttu-id="7253a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7253a-105">Syntax</span></span>


```C++
HRESULT WINAPI WldpIsDynamicCodePolicyEnabled(
  _Out_ PBOOL  isEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="7253a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7253a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7253a-107">*IsEnabled* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="7253a-107">*isEnabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7253a-108">Em caso de sucesso, retornará **true** se a política de proteção do dispositivo impor a política de código dinâmico do .net; caso contrário, retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="7253a-108">On success, returns **true** if the Device Guard policy enforces .NET Dynamic Code policy; otherwise, returns **false**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7253a-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7253a-109">Return value</span></span>

<span data-ttu-id="7253a-110">Esse método retornará **S \_ OK** , se for bem-sucedido ou um código de falha.</span><span class="sxs-lookup"><span data-stu-id="7253a-110">This method returns **S\_OK** if successful or a failure code otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="7253a-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="7253a-111">Remarks</span></span>

<span data-ttu-id="7253a-112">O código dinâmico refere-se à CRL do .NET código gerado dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="7253a-112">Dynamic code refers to .NET CRL dynamically-generated code.</span></span>

## <a name="requirements"></a><span data-ttu-id="7253a-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7253a-113">Requirements</span></span>



| <span data-ttu-id="7253a-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="7253a-114">Requirement</span></span> | <span data-ttu-id="7253a-115">Valor</span><span class="sxs-lookup"><span data-stu-id="7253a-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="7253a-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7253a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="7253a-117">\[Somente aplicativos da área de trabalho do Windows 10, versão 1803\]</span><span class="sxs-lookup"><span data-stu-id="7253a-117">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="7253a-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7253a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="7253a-119">\[Somente aplicativos da área de trabalho do Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="7253a-119">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="7253a-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7253a-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="7253a-121"><dt>Wldp. h</dt></span><span class="sxs-lookup"><span data-stu-id="7253a-121"><dt>Wldp.h</dt></span></span> </dl>   |
| <span data-ttu-id="7253a-122">DLL</span><span class="sxs-lookup"><span data-stu-id="7253a-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7253a-123"><dt>Wldp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7253a-123"><dt>Wldp.dll</dt></span></span> </dl> |



 

 




