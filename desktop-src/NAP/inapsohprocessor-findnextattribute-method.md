---
title: Método INapSoHProcessor FindNextAttribute (NapProtocol. h)
description: Localiza o local (índice) do próximo atributo do tipo indicado por SoHAttributeType.
ms.assetid: 0ff94a32-ece8-4a89-9ee9-93c5e14dfb6c
keywords:
- Método FindNextAttribute NAP
- Método FindNextAttribute NAP, interface INapSoHProcessor
- INapSoHProcessor interface NAP, método FindNextAttribute
topic_type:
- apiref
api_name:
- INapSoHProcessor.FindNextAttribute
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1a270e36f8254ed5dbfcd9776cf013f9d10d4a1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644330"
---
# <a name="inapsohprocessorfindnextattribute-method"></a><span data-ttu-id="28369-106">Método INapSoHProcessor:: FindNextAttribute</span><span class="sxs-lookup"><span data-stu-id="28369-106">INapSoHProcessor::FindNextAttribute method</span></span>

> [!Note]  
> <span data-ttu-id="28369-107">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="28369-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="28369-108">O método **INapSoHProcessor:: FindNextAttribute** localiza o local (índice) do próximo atributo do tipo indicado por *SoHAttributeType*.</span><span class="sxs-lookup"><span data-stu-id="28369-108">The **INapSoHProcessor::FindNextAttribute** method finds the location (index) of the next attribute of the type indicated by *SoHAttributeType*.</span></span>

## <a name="syntax"></a><span data-ttu-id="28369-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="28369-109">Syntax</span></span>


```C++
HRESULT FindNextAttribute(
  [in]  UINT16           fromLocation,
  [in]  SoHAttributeType type,
  [out] UINT16           *attributeLocation
);
```



## <a name="parameters"></a><span data-ttu-id="28369-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="28369-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28369-111">*fromLocation* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="28369-111">*fromLocation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28369-112">O local inicial (índice) no pacote da declaração de integridade (SoH) para iniciar a pesquisa de atributo.</span><span class="sxs-lookup"><span data-stu-id="28369-112">The starting location (index) in the Statement of Health (SoH) packet to begin the attribute search.</span></span> <span data-ttu-id="28369-113">Esse valor deve estar no intervalo de 0 a (**numAttrib** -1) em que **numAttrib** é recuperado usando [**INapSoHProcessor:: GetNumberOfAttributes**](inapsohprocessor-getnumberofattributes-method.md).</span><span class="sxs-lookup"><span data-stu-id="28369-113">This value must be in the range of 0 to (**numAttrib** - 1) where **numAttrib** is retrieved using [**INapSoHProcessor::GetNumberOfAttributes**](inapsohprocessor-getnumberofattributes-method.md).</span></span>

> [!Note]  
> <span data-ttu-id="28369-114">O pacote SoH usa índices de atributos baseados em 0.</span><span class="sxs-lookup"><span data-stu-id="28369-114">The SoH packet uses 0-based attribute indices.</span></span>

 

</dd> <dt>

<span data-ttu-id="28369-115">*tipo* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="28369-115">*type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28369-116">Uma estrutura [**SoHAttributeType**](sohattributetype-enum.md) que contém o tipo de atributo a ser localizado.</span><span class="sxs-lookup"><span data-stu-id="28369-116">An [**SoHAttributeType**](sohattributetype-enum.md) structure that contains the attribute type to locate.</span></span>

</dd> <dt>

<span data-ttu-id="28369-117">*attributeLocation* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="28369-117">*attributeLocation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="28369-118">Um ponteiro que contém o local (índice) no pacote SoH do primeiro atributo do tipo *SoHAttributeType* do índice *fromLocation*.</span><span class="sxs-lookup"><span data-stu-id="28369-118">A pointer that contains the location (index) in the SoH packet of the first attribute of type *SoHAttributeType* from the index *fromLocation*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28369-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="28369-119">Return value</span></span>

<span data-ttu-id="28369-120">Outros códigos de erro específicos de COM também podem ser retornados.</span><span class="sxs-lookup"><span data-stu-id="28369-120">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="28369-121">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="28369-121">Return code</span></span>                                                                                            | <span data-ttu-id="28369-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="28369-122">Description</span></span>                                                        |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="28369-123"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="28369-123"><dt>**S\_OK** </dt></span></span> </dl>                  | <span data-ttu-id="28369-124">Operação bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="28369-124">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="28369-125"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="28369-125"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl>        | <span data-ttu-id="28369-126">Erro de permissões, acesso negado.</span><span class="sxs-lookup"><span data-stu-id="28369-126">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="28369-127"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="28369-127"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>         | <span data-ttu-id="28369-128">O limite de recursos do sistema não pôde executar a operação.</span><span class="sxs-lookup"><span data-stu-id="28369-128">System resource limit, could not perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="28369-129"><dt>**arquivo de erro \_ \_ não \_ encontrado**</dt></span><span class="sxs-lookup"><span data-stu-id="28369-129"><dt>**ERROR\_FILE\_NOT\_FOUND**</dt></span></span> </dl> | <span data-ttu-id="28369-130">Atributo não encontrado.</span><span class="sxs-lookup"><span data-stu-id="28369-130">Attribute not found.</span></span><br/>                                    |



 

## <a name="remarks"></a><span data-ttu-id="28369-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="28369-131">Remarks</span></span>

<span data-ttu-id="28369-132">O método **FindNextAttribute** procura atributos do tipo *SoHAttributeType* a partir do índice especificado por *fromLocation* e superior até que uma correspondência seja encontrada.</span><span class="sxs-lookup"><span data-stu-id="28369-132">The **FindNextAttribute** method searches for attributes of type *SoHAttributeType* from the index specified by *fromLocation* and higher until a match is found.</span></span> <span data-ttu-id="28369-133">Se nenhuma correspondência for encontrada, **o \_ arquivo de erro \_ não \_ encontrado** será retornado.</span><span class="sxs-lookup"><span data-stu-id="28369-133">If no match is found, **ERROR\_FILE\_NOT\_FOUND** is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="28369-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="28369-134">Requirements</span></span>



| <span data-ttu-id="28369-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="28369-135">Requirement</span></span> | <span data-ttu-id="28369-136">Valor</span><span class="sxs-lookup"><span data-stu-id="28369-136">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="28369-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="28369-137">Minimum supported client</span></span><br/> | <span data-ttu-id="28369-138">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="28369-138">Windows Vista \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="28369-139">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="28369-139">Minimum supported server</span></span><br/> | <span data-ttu-id="28369-140">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="28369-140">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="28369-141">parâmetro</span><span class="sxs-lookup"><span data-stu-id="28369-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="28369-142"><dt>NapProtocol. h</dt></span><span class="sxs-lookup"><span data-stu-id="28369-142"><dt>NapProtocol.h</dt></span></span> </dl>   |
| <span data-ttu-id="28369-143">INSERI</span><span class="sxs-lookup"><span data-stu-id="28369-143">IDL</span></span><br/>                      | <dl> <span data-ttu-id="28369-144"><dt>NapProtocol. idl</dt></span><span class="sxs-lookup"><span data-stu-id="28369-144"><dt>NapProtocol.idl</dt></span></span> </dl> |
| <span data-ttu-id="28369-145">DLL</span><span class="sxs-lookup"><span data-stu-id="28369-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="28369-146"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="28369-146"><dt>Qutil.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="28369-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="28369-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28369-148">**INapSoHProcessor**</span><span class="sxs-lookup"><span data-stu-id="28369-148">**INapSoHProcessor**</span></span>](inapsohprocessor.md)
</dt> </dl>

 

 





