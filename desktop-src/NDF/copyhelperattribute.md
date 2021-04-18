---
title: Função CopyHelperAttribute (Ndattributils. h)
description: Cria uma cópia de uma \_ estrutura de atributo auxiliar.
ms.assetid: ff49be29-4cd8-4730-929f-c66a7325704f
keywords:
- NDF da função CopyHelperAttribute
topic_type:
- apiref
api_name:
- CopyHelperAttribute
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59fac3449ee48659980681c836d24406c4db7e2b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105787052"
---
# <a name="copyhelperattribute-function"></a><span data-ttu-id="1db92-104">Função CopyHelperAttribute</span><span class="sxs-lookup"><span data-stu-id="1db92-104">CopyHelperAttribute function</span></span>

<span data-ttu-id="1db92-105">A função **CopyHelperAttribute** cria uma cópia de uma estrutura de [**\_ atributo auxiliar**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute) .</span><span class="sxs-lookup"><span data-stu-id="1db92-105">The **CopyHelperAttribute** function creates a copy of a [**HELPER\_ATTRIBUTE**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="1db92-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1db92-106">Syntax</span></span>


```C++
HRESULT CopyHelperAttribute(
  _Out_       HELPER_ATTRIBUTE *Dest,
  _In_  const HELPER_ATTRIBUTE *Source
);
```



## <a name="parameters"></a><span data-ttu-id="1db92-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1db92-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1db92-108">*Dest* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="1db92-108">*Dest* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1db92-109">Tipo: \**\* [**\_ atributo auxiliar**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute)* _</span><span class="sxs-lookup"><span data-stu-id="1db92-109">Type: \**[**HELPER\_ATTRIBUTE**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute)\** _</span></span>

<span data-ttu-id="1db92-110">A estrutura a ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="1db92-110">The structure to be updated.</span></span>

</dd> <dt>

<span data-ttu-id="1db92-111">_Source \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1db92-111">_Source\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1db92-112">Tipo: \**const [**helper \_ atributo**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute) \** _</span><span class="sxs-lookup"><span data-stu-id="1db92-112">Type: \**const [**HELPER\_ATTRIBUTE**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute)\** _</span></span>

<span data-ttu-id="1db92-113">A estrutura existente a ser copiada.</span><span class="sxs-lookup"><span data-stu-id="1db92-113">The existing structure to be copied.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1db92-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1db92-114">Return value</span></span>

<span data-ttu-id="1db92-115">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="1db92-115">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="1db92-116">Os valores de retorno possíveis incluem, mas não se limitam a, o seguinte.</span><span class="sxs-lookup"><span data-stu-id="1db92-116">Possible return values include, but are not limited to, the following.</span></span>



| <span data-ttu-id="1db92-117">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="1db92-117">Return code</span></span>                                                                                   | <span data-ttu-id="1db92-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="1db92-118">Description</span></span>                                                                 |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1db92-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="1db92-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="1db92-120">A operação foi realizada com êxito.</span><span class="sxs-lookup"><span data-stu-id="1db92-120">The operation succeeded.</span></span><br/>                                         |
| <dl> <span data-ttu-id="1db92-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="1db92-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="1db92-122">Um ou mais parâmetros não foram fornecidos corretamente.</span><span class="sxs-lookup"><span data-stu-id="1db92-122">One or more parameters has not been provided correctly.</span></span><br/>          |
| <dl> <span data-ttu-id="1db92-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="1db92-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="1db92-124">Não há memória suficiente disponível para concluir esta operação.</span><span class="sxs-lookup"><span data-stu-id="1db92-124">There is not enough memory available to complete this operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="1db92-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1db92-125">Requirements</span></span>



| <span data-ttu-id="1db92-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="1db92-126">Requirement</span></span> | <span data-ttu-id="1db92-127">Valor</span><span class="sxs-lookup"><span data-stu-id="1db92-127">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="1db92-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1db92-128">Minimum supported client</span></span><br/> | <span data-ttu-id="1db92-129">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="1db92-129">Windows 8 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="1db92-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1db92-130">Minimum supported server</span></span><br/> | <span data-ttu-id="1db92-131">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="1db92-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="1db92-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1db92-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="1db92-133"><dt>Ndattributils. h</dt></span><span class="sxs-lookup"><span data-stu-id="1db92-133"><dt>Ndattributils.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1db92-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="1db92-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1db92-135">**\_atributo auxiliar**</span><span class="sxs-lookup"><span data-stu-id="1db92-135">**HELPER\_ATTRIBUTE**</span></span>](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute)
</dt> </dl>

 

 





