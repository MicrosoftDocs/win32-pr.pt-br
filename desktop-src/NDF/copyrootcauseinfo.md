---
title: Função CopyRootCauseInfo (Ndattributils. h)
description: Cria uma cópia de uma estrutura RootCauseInfo.
ms.assetid: 6bcd1341-657a-40c1-bebd-1c0f780ae337
keywords:
- NDF da função CopyRootCauseInfo
topic_type:
- apiref
api_name:
- CopyRootCauseInfo
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5093d7af6458668a763aa206cacd22a0526aa521
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918231"
---
# <a name="copyrootcauseinfo-function"></a><span data-ttu-id="59e8e-104">Função CopyRootCauseInfo</span><span class="sxs-lookup"><span data-stu-id="59e8e-104">CopyRootCauseInfo function</span></span>

<span data-ttu-id="59e8e-105">A função **CopyRootCauseInfo** cria uma cópia de uma estrutura [**RootCauseInfo**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo) .</span><span class="sxs-lookup"><span data-stu-id="59e8e-105">The **CopyRootCauseInfo** function creates a copy of a [**RootCauseInfo**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="59e8e-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="59e8e-106">Syntax</span></span>


```C++
HRESULT CopyRootCauseInfo(
  _Out_       RootCauseInfo *Dest,
  _In_  const RootCauseInfo *Source
);
```



## <a name="parameters"></a><span data-ttu-id="59e8e-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="59e8e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59e8e-108">*Dest* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="59e8e-108">*Dest* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="59e8e-109">Tipo: \**[**RootCauseInfo**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="59e8e-109">Type: \**[**RootCauseInfo**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo)\** _</span></span>

<span data-ttu-id="59e8e-110">A estrutura a ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="59e8e-110">The structure to be updated.</span></span>

</dd> <dt>

<span data-ttu-id="59e8e-111">_Source \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="59e8e-111">_Source\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59e8e-112">Tipo: \**const [**RootCauseInfo**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="59e8e-112">Type: \**const [**RootCauseInfo**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo)\** _</span></span>

<span data-ttu-id="59e8e-113">A estrutura existente a ser copiada.</span><span class="sxs-lookup"><span data-stu-id="59e8e-113">The existing structure to be copied.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59e8e-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="59e8e-114">Return value</span></span>

<span data-ttu-id="59e8e-115">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="59e8e-115">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="59e8e-116">Os valores de retorno possíveis incluem, mas não se limitam a, o seguinte.</span><span class="sxs-lookup"><span data-stu-id="59e8e-116">Possible return values include, but are not limited to, the following.</span></span>



| <span data-ttu-id="59e8e-117">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="59e8e-117">Return code</span></span>                                                                                   | <span data-ttu-id="59e8e-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="59e8e-118">Description</span></span>                                                                 |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="59e8e-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="59e8e-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="59e8e-120">A operação foi realizada com êxito.</span><span class="sxs-lookup"><span data-stu-id="59e8e-120">The operation succeeded.</span></span><br/>                                         |
| <dl> <span data-ttu-id="59e8e-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="59e8e-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="59e8e-122">Um ou mais parâmetros não foram fornecidos corretamente.</span><span class="sxs-lookup"><span data-stu-id="59e8e-122">One or more parameters has not been provided correctly.</span></span><br/>          |
| <dl> <span data-ttu-id="59e8e-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="59e8e-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="59e8e-124">Não há memória suficiente disponível para concluir esta operação.</span><span class="sxs-lookup"><span data-stu-id="59e8e-124">There is not enough memory available to complete this operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="59e8e-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="59e8e-125">Requirements</span></span>



| <span data-ttu-id="59e8e-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="59e8e-126">Requirement</span></span> | <span data-ttu-id="59e8e-127">Valor</span><span class="sxs-lookup"><span data-stu-id="59e8e-127">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="59e8e-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="59e8e-128">Minimum supported client</span></span><br/> | <span data-ttu-id="59e8e-129">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="59e8e-129">Windows 8 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="59e8e-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="59e8e-130">Minimum supported server</span></span><br/> | <span data-ttu-id="59e8e-131">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="59e8e-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="59e8e-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="59e8e-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="59e8e-133"><dt>Ndattributils. h</dt></span><span class="sxs-lookup"><span data-stu-id="59e8e-133"><dt>Ndattributils.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59e8e-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="59e8e-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59e8e-135">**RootCauseInfo**</span><span class="sxs-lookup"><span data-stu-id="59e8e-135">**RootCauseInfo**</span></span>](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo)
</dt> </dl>

 

 





