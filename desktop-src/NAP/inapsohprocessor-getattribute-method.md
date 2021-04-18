---
title: Método GetAttribute INapSoHProcessor (NapProtocol. h)
description: Recupera o tipo de atributo e o valor, dado o local do atributo.
ms.assetid: 0d7bc655-428b-4a31-b03f-445e80a6d194
keywords:
- Método GetAttribute NAP
- Método GetAttribute NAP, interface INapSoHProcessor
- Interface INapSoHProcessor NAP, método GetAttribute
topic_type:
- apiref
api_name:
- INapSoHProcessor.GetAttribute
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ed2d7d9cbafa5a44e0f6c24f4c42959c456722a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105810157"
---
# <a name="inapsohprocessorgetattribute-method"></a><span data-ttu-id="25d1d-106">Método INapSoHProcessor:: GetAttribute</span><span class="sxs-lookup"><span data-stu-id="25d1d-106">INapSoHProcessor::GetAttribute method</span></span>

> [!Note]  
> <span data-ttu-id="25d1d-107">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="25d1d-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="25d1d-108">O método **INapSoHProcessor:: GetAttribute** recupera o tipo e o valor do atributo, dado o local do atributo.</span><span class="sxs-lookup"><span data-stu-id="25d1d-108">The **INapSoHProcessor::GetAttribute** method retrieves the attribute type and value, given the attribute location.</span></span>

## <a name="syntax"></a><span data-ttu-id="25d1d-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="25d1d-109">Syntax</span></span>


```C++
HRESULT GetAttribute(
  [in]  UINT16            attributeLocation,
  [out] SoHAttributeType  *type,
  [out] SoHAttributeValue **value
);
```



## <a name="parameters"></a><span data-ttu-id="25d1d-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="25d1d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25d1d-111">*attributeLocation* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="25d1d-111">*attributeLocation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25d1d-112">O local (índice) do atributo cujo tipo e valor devem ser recuperados.</span><span class="sxs-lookup"><span data-stu-id="25d1d-112">The location (index) of the attribute whose type and value are to be retrieved.</span></span> <span data-ttu-id="25d1d-113">O valor de *attributeLocation* é retornado de uma chamada anterior para [**INapSoHProcessor:: FindNextAttribute**](inapsohprocessor-findnextattribute-method.md).</span><span class="sxs-lookup"><span data-stu-id="25d1d-113">The value of *attributeLocation* is returned from a prior call to [**INapSoHProcessor::FindNextAttribute**](inapsohprocessor-findnextattribute-method.md).</span></span>

</dd> <dt>

<span data-ttu-id="25d1d-114">*tipo* \[ de fora\]</span><span class="sxs-lookup"><span data-stu-id="25d1d-114">*type* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="25d1d-115">Um ponteiro para uma estrutura [**SoHAttributeType**](sohattributetype-enum.md) que especifica o tipo do atributo no *valor*.</span><span class="sxs-lookup"><span data-stu-id="25d1d-115">A pointer to an [**SoHAttributeType**](sohattributetype-enum.md) structure that specifies the attribute's type in *value*.</span></span>

</dd> <dt>

<span data-ttu-id="25d1d-116">*valor* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="25d1d-116">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="25d1d-117">Um ponteiro para um ponteiro para uma estrutura [**SoHAttributeValue**](sohattributevalue-union.md) que contém o valor do atributo, conforme definido pelo *tipo*.</span><span class="sxs-lookup"><span data-stu-id="25d1d-117">A pointer to a pointer to a [**SoHAttributeValue**](sohattributevalue-union.md) structure that contains the attribute's value as defined by *type*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25d1d-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="25d1d-118">Return value</span></span>

<span data-ttu-id="25d1d-119">Outros códigos de erro específicos de COM também podem ser retornados.</span><span class="sxs-lookup"><span data-stu-id="25d1d-119">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="25d1d-120">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="25d1d-120">Return code</span></span>                                                                                     | <span data-ttu-id="25d1d-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="25d1d-121">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="25d1d-122"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="25d1d-122"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="25d1d-123">Operação bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="25d1d-123">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="25d1d-124"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="25d1d-124"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="25d1d-125">Erro de permissões, acesso negado.</span><span class="sxs-lookup"><span data-stu-id="25d1d-125">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="25d1d-126"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="25d1d-126"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="25d1d-127">O limite de recursos do sistema não pôde executar a operação.</span><span class="sxs-lookup"><span data-stu-id="25d1d-127">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="25d1d-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="25d1d-128">Requirements</span></span>



| <span data-ttu-id="25d1d-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="25d1d-129">Requirement</span></span> | <span data-ttu-id="25d1d-130">Valor</span><span class="sxs-lookup"><span data-stu-id="25d1d-130">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="25d1d-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="25d1d-131">Minimum supported client</span></span><br/> | <span data-ttu-id="25d1d-132">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="25d1d-132">Windows Vista \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="25d1d-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="25d1d-133">Minimum supported server</span></span><br/> | <span data-ttu-id="25d1d-134">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="25d1d-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="25d1d-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="25d1d-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="25d1d-136"><dt>NapProtocol. h</dt></span><span class="sxs-lookup"><span data-stu-id="25d1d-136"><dt>NapProtocol.h</dt></span></span> </dl>   |
| <span data-ttu-id="25d1d-137">INSERI</span><span class="sxs-lookup"><span data-stu-id="25d1d-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="25d1d-138"><dt>NapProtocol. idl</dt></span><span class="sxs-lookup"><span data-stu-id="25d1d-138"><dt>NapProtocol.idl</dt></span></span> </dl> |
| <span data-ttu-id="25d1d-139">DLL</span><span class="sxs-lookup"><span data-stu-id="25d1d-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="25d1d-140"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="25d1d-140"><dt>Qutil.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="25d1d-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="25d1d-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25d1d-142">**INapSoHProcessor**</span><span class="sxs-lookup"><span data-stu-id="25d1d-142">**INapSoHProcessor**</span></span>](inapsohprocessor.md)
</dt> </dl>

 

 





