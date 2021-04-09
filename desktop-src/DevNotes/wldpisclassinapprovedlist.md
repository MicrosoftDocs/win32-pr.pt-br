---
description: Chama a biblioteca para validar se um CLSID específico é seguro para ser chamado.
ms.assetid: 94C8731B-88FD-4240-BF5D-2CD67C41B063
title: Função WldpIsClassInApprovedList (Wldp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WldpIsClassInApprovedList
api_type:
- DllExport
api_location:
- wldp.dll
ms.openlocfilehash: 01762c60a3f1aef1574cc218ace9988669175efe
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104088890"
---
# <a name="wldpisclassinapprovedlist-function"></a><span data-ttu-id="23219-103">Função WldpIsClassInApprovedList</span><span class="sxs-lookup"><span data-stu-id="23219-103">WldpIsClassInApprovedList function</span></span>

<span data-ttu-id="23219-104">Chama a biblioteca para validar se um **CLSID** específico é seguro para ser chamado.</span><span class="sxs-lookup"><span data-stu-id="23219-104">Calls the library to validate if a particular **CLSID** is safe to be called.</span></span> <span data-ttu-id="23219-105">A função não tem biblioteca de importação associada.</span><span class="sxs-lookup"><span data-stu-id="23219-105">The function has no associated import library.</span></span> <span data-ttu-id="23219-106">Você deve usar as funções LoadLibrary e GetProcAddress para vincular dinamicamente a wldp.dll.</span><span class="sxs-lookup"><span data-stu-id="23219-106">You must use the LoadLibrary and GetProcAddress functions to dynamically link to wldp.dll.</span></span>

## <a name="syntax"></a><span data-ttu-id="23219-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="23219-107">Syntax</span></span>


```C++
HRESULT WINAPI WldpIsClassInApprovedList(
        REFCLSID               classID,
  _In_  PWLDP_HOST_INFORMATION hostInformation,
  _Out_ PBOOL                  isApproved,
        DWORD                  optionalFlags
);
```



## <a name="parameters"></a><span data-ttu-id="23219-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="23219-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23219-109">*classID*</span><span class="sxs-lookup"><span data-stu-id="23219-109">*classID*</span></span> 
</dt> <dd>

<span data-ttu-id="23219-110">A ID da classe COM para verificar a aprovação.</span><span class="sxs-lookup"><span data-stu-id="23219-110">The COM class ID to check for approval.</span></span>

</dd> <dt>

<span data-ttu-id="23219-111">*hostInformation* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="23219-111">*hostInformation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23219-112">Uma estrutura de [**\_ \_ informações de host WLDP**](wldp-host-information.md) que identifica o host a ser avaliado.</span><span class="sxs-lookup"><span data-stu-id="23219-112">A [**WLDP\_HOST\_INFORMATION**](wldp-host-information.md) structure identifying the host to be evaluated.</span></span>

</dd> <dt>

<span data-ttu-id="23219-113">*IsApproved* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="23219-113">*isApproved* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="23219-114">Após a conclusão bem-sucedida, conterá **true** se a ID da classe for aprovada; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="23219-114">On successful completion, contains **TRUE** if the class ID is approved; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="23219-115">*optionalFlags*</span><span class="sxs-lookup"><span data-stu-id="23219-115">*optionalFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="23219-116">Esse parâmetro é reservado e deve ser definido como zero.</span><span class="sxs-lookup"><span data-stu-id="23219-116">This parameter is reserved and must be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23219-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="23219-117">Return value</span></span>

<span data-ttu-id="23219-118">Esse método retornará **S \_ OK** , se for bem-sucedido ou um código de falha.</span><span class="sxs-lookup"><span data-stu-id="23219-118">This method returns **S\_OK** if successful or a failure code otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="23219-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="23219-119">Requirements</span></span>



| <span data-ttu-id="23219-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="23219-120">Requirement</span></span> | <span data-ttu-id="23219-121">Valor</span><span class="sxs-lookup"><span data-stu-id="23219-121">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="23219-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="23219-122">Minimum supported client</span></span><br/> | <span data-ttu-id="23219-123">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="23219-123">Windows 10 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="23219-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="23219-124">Minimum supported server</span></span><br/> | <span data-ttu-id="23219-125">\[Somente aplicativos da área de trabalho do Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="23219-125">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="23219-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="23219-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="23219-127"><dt>Wldp. h</dt></span><span class="sxs-lookup"><span data-stu-id="23219-127"><dt>Wldp.h</dt></span></span> </dl>   |
| <span data-ttu-id="23219-128">DLL</span><span class="sxs-lookup"><span data-stu-id="23219-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="23219-129"><dt>Wldp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="23219-129"><dt>Wldp.dll</dt></span></span> </dl> |



 

 




