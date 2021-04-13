---
title: Método AppendAttribute INapSoHConstructor (NapProtocol. h)
description: Adiciona um TLV ao final do buffer SoH.
ms.assetid: 5706ceaa-757f-49d2-90e0-011415853875
keywords:
- Método AppendAttribute NAP
- Método AppendAttribute NAP, interface INapSoHConstructor
- INapSoHConstructor interface NAP, método AppendAttribute
topic_type:
- apiref
api_name:
- INapSoHConstructor.AppendAttribute
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc10fad9c775d324822700b77afed4e65a798db6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499351"
---
# <a name="inapsohconstructorappendattribute-method"></a><span data-ttu-id="7c3ba-106">Método INapSoHConstructor:: AppendAttribute</span><span class="sxs-lookup"><span data-stu-id="7c3ba-106">INapSoHConstructor::AppendAttribute method</span></span>

> [!Note]  
> <span data-ttu-id="7c3ba-107">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="7c3ba-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="7c3ba-108">O método **INapSoHConstructor:: AppendAttribute** adiciona um TLV ao final do buffer soh.</span><span class="sxs-lookup"><span data-stu-id="7c3ba-108">The **INapSoHConstructor::AppendAttribute** method adds a TLV to the end of the SoH buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c3ba-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7c3ba-109">Syntax</span></span>


```C++
HRESULT AppendAttribute(
  [in]       SoHAttributeType  type,
  [in] const SoHAttributeValue *value
);
```



## <a name="parameters"></a><span data-ttu-id="7c3ba-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7c3ba-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c3ba-111">*tipo* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="7c3ba-111">*type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c3ba-112">Uma enumeração [**SoHAttributeType**](sohattributetype-enum.md) que indica o tipo de atributo do novo TLV.</span><span class="sxs-lookup"><span data-stu-id="7c3ba-112">A [**SoHAttributeType**](sohattributetype-enum.md) enumeration that indicates the attribute type of the new TLV.</span></span>

</dd> <dt>

<span data-ttu-id="7c3ba-113">*valor* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="7c3ba-113">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c3ba-114">Um ponteiro para uma estrutura [**SoHAttributeValue**](sohattributevalue-union.md) que contém o valor para o novo TLV.</span><span class="sxs-lookup"><span data-stu-id="7c3ba-114">A pointer to an [**SoHAttributeValue**](sohattributevalue-union.md) structure that contains the value for the new TLV.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c3ba-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7c3ba-115">Return value</span></span>

<span data-ttu-id="7c3ba-116">Outros códigos de erro específicos de COM também podem ser retornados.</span><span class="sxs-lookup"><span data-stu-id="7c3ba-116">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="7c3ba-117">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="7c3ba-117">Return code</span></span>                                                                                     | <span data-ttu-id="7c3ba-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="7c3ba-118">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="7c3ba-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="7c3ba-119"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="7c3ba-120">Operação bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="7c3ba-120">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="7c3ba-121"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="7c3ba-121"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="7c3ba-122">Erro de permissões, acesso negado.</span><span class="sxs-lookup"><span data-stu-id="7c3ba-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="7c3ba-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="7c3ba-123"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="7c3ba-124">O limite de recursos do sistema não pôde executar a operação.</span><span class="sxs-lookup"><span data-stu-id="7c3ba-124">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7c3ba-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="7c3ba-125">Remarks</span></span>

<span data-ttu-id="7c3ba-126">O TLV [**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md) não deve ser adicionado usando essa função.</span><span class="sxs-lookup"><span data-stu-id="7c3ba-126">The [**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md) TLV must not be added using this function.</span></span> <span data-ttu-id="7c3ba-127">Ele é adicionado como o primeiro TLV de [**INapSoHConstructor:: Initialize**](inapsohconstructor-initialize-method.md) para pacotes soh recém-criados.</span><span class="sxs-lookup"><span data-stu-id="7c3ba-127">It is added as the first TLV by [**INapSoHConstructor::Initialize**](inapsohconstructor-initialize-method.md) to newly constructed SOH packets.</span></span>

<span data-ttu-id="7c3ba-128">Ao acrescentar um atributo que será consumido pelo sistema NAP, ele não deve ser criptografado ou modificado de nenhuma maneira.</span><span class="sxs-lookup"><span data-stu-id="7c3ba-128">When appending an attribute which will be consumed by the Nap System, it should not be encrypted or modified in any manner.</span></span> <span data-ttu-id="7c3ba-129">Se o HealthEntity requer MACs (verificação de integridade/criptografia) de informações privadas, ele deve ser incluído somente no atributo [**sohAttributeTypeVendorSpecific**](sohattributetype-enum.md) .</span><span class="sxs-lookup"><span data-stu-id="7c3ba-129">If the HealthEntity requires encryption/integrity checking (MACs) of private information, it should be included only in the [**sohAttributeTypeVendorSpecific**](sohattributetype-enum.md) attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c3ba-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7c3ba-130">Requirements</span></span>



| <span data-ttu-id="7c3ba-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c3ba-131">Requirement</span></span> | <span data-ttu-id="7c3ba-132">Valor</span><span class="sxs-lookup"><span data-stu-id="7c3ba-132">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c3ba-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7c3ba-133">Minimum supported client</span></span><br/> | <span data-ttu-id="7c3ba-134">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7c3ba-134">Windows Vista \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="7c3ba-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7c3ba-135">Minimum supported server</span></span><br/> | <span data-ttu-id="7c3ba-136">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7c3ba-136">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="7c3ba-137">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7c3ba-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="7c3ba-138"><dt>NapProtocol. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c3ba-138"><dt>NapProtocol.h</dt></span></span> </dl>   |
| <span data-ttu-id="7c3ba-139">INSERI</span><span class="sxs-lookup"><span data-stu-id="7c3ba-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7c3ba-140"><dt>NapProtocol. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7c3ba-140"><dt>NapProtocol.idl</dt></span></span> </dl> |
| <span data-ttu-id="7c3ba-141">DLL</span><span class="sxs-lookup"><span data-stu-id="7c3ba-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7c3ba-142"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7c3ba-142"><dt>Qutil.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="7c3ba-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="7c3ba-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c3ba-144">**INapSoHConstructor**</span><span class="sxs-lookup"><span data-stu-id="7c3ba-144">**INapSoHConstructor**</span></span>](inapsohconstructor.md)
</dt> </dl>

 

 





