---
description: O método SetProperties define o primitivo referenciado por TLVs (marca, comprimento, valor) para o objeto especificado.
ms.assetid: f8f75c8e-14f4-4bc4-b49d-b232ede374b0
title: 'Método ISCardFileAccess:: SetProperties'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.SetProperties
api_type:
- COM
api_location: ''
ms.openlocfilehash: b54c2193ec17bca9f9b3ba00b2c2bc133707dbb2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105748742"
---
# <a name="iscardfileaccesssetproperties-method"></a><span data-ttu-id="fd8e5-103">Método ISCardFileAccess:: SetProperties</span><span class="sxs-lookup"><span data-stu-id="fd8e5-103">ISCardFileAccess::SetProperties method</span></span>

<span data-ttu-id="fd8e5-104">\[O método **SetProperties** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="fd8e5-104">\[The **SetProperties** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="fd8e5-105">Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="fd8e5-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="fd8e5-106">Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="fd8e5-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="fd8e5-107">O método **SetProperties** define o primitivo referenciado por TLVs (marca, comprimento, valor) para o objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="fd8e5-107">The **SetProperties** method sets the primitive referred by TLVs (tag, length, value) for the specified object.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd8e5-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fd8e5-108">Syntax</span></span>


```C++
HRESULT SetProperties(
  [in] REFTYPE     refType,
  [in] BSTR        bstrPathSpec,
  [in] SCARD_FLAGS flags,
  [in] LPTLV_TABLE pTable
);
```



## <a name="parameters"></a><span data-ttu-id="fd8e5-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fd8e5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd8e5-110">*refType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fd8e5-110">*refType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd8e5-111">Tipo de referência usado em *bstrPathSpec*.</span><span class="sxs-lookup"><span data-stu-id="fd8e5-111">Type of reference used in *bstrPathSpec*.</span></span>

<dl><span id="SC_TYPE_BY_NAME"></span><span id="sc_type_by_name"></span><dt>

<span data-ttu-id="fd8e5-112">**SC \_ tipo \_ por \_ nome**</span><span class="sxs-lookup"><span data-stu-id="fd8e5-112">**SC\_TYPE\_BY\_NAME**</span></span>
</dt><span id="SC_TYPE_BY_ID"></span><span id="sc_type_by_id"></span><dt>

<span data-ttu-id="fd8e5-113">**SC \_ tipo \_ por \_ ID**</span><span class="sxs-lookup"><span data-stu-id="fd8e5-113">**SC\_TYPE\_BY\_ID**</span></span>
</dt><span id="SC_TYPE_BY_SHORT"></span><span id="sc_type_by_short"></span><dt>

<span data-ttu-id="fd8e5-114">**SC \_ tipo \_ por \_ curto**</span><span class="sxs-lookup"><span data-stu-id="fd8e5-114">**SC\_TYPE\_BY\_SHORT**</span></span>
</dt><span id="SC_TYPE_BY_ANY"></span><span id="sc_type_by_any"></span><dt>

<span data-ttu-id="fd8e5-115">**SC \_ tipo \_ por \_ qualquer**</span><span class="sxs-lookup"><span data-stu-id="fd8e5-115">**SC\_TYPE\_BY\_ANY**</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="fd8e5-116">*bstrPathSpec* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fd8e5-116">*bstrPathSpec* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd8e5-117">Grupo.</span><span class="sxs-lookup"><span data-stu-id="fd8e5-117">File.</span></span>

</dd> <dt>

<span data-ttu-id="fd8e5-118">*sinalizadores* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="fd8e5-118">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd8e5-119">Especifica se as mensagens seguras devem ser usadas.</span><span class="sxs-lookup"><span data-stu-id="fd8e5-119">Specifies whether secure messaging should be used.</span></span>

<dl><span id="SC_FL_SECURE_MESSAGING"></span><span id="sc_fl_secure_messaging"></span><dt>

<span data-ttu-id="fd8e5-120">**\_ \_ mensagens seguras do SC FL \_**</span><span class="sxs-lookup"><span data-stu-id="fd8e5-120">**SC\_FL\_SECURE\_MESSAGING**</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="fd8e5-121">*pTable* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fd8e5-121">*pTable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd8e5-122">Ponteiro para estruturas TLV cujo valor deve ser definido.</span><span class="sxs-lookup"><span data-stu-id="fd8e5-122">Pointer to TLV structures whose value should be set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd8e5-123">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fd8e5-123">Return value</span></span>

<span data-ttu-id="fd8e5-124">O método retorna um dos seguintes valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="fd8e5-124">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="fd8e5-125">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="fd8e5-125">Return code</span></span>                                                                                   | <span data-ttu-id="fd8e5-126">Descrição</span><span class="sxs-lookup"><span data-stu-id="fd8e5-126">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="fd8e5-127"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="fd8e5-127"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="fd8e5-128">Operação concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="fd8e5-128">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="fd8e5-129"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="fd8e5-129"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="fd8e5-130">Parâmetro inválido.</span><span class="sxs-lookup"><span data-stu-id="fd8e5-130">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="fd8e5-131"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="fd8e5-131"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="fd8e5-132">Um ponteiro inadequado foi passado.</span><span class="sxs-lookup"><span data-stu-id="fd8e5-132">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="fd8e5-133"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="fd8e5-133"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="fd8e5-134">Sem memória.</span><span class="sxs-lookup"><span data-stu-id="fd8e5-134">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="fd8e5-135">Comentários</span><span class="sxs-lookup"><span data-stu-id="fd8e5-135">Remarks</span></span>

<span data-ttu-id="fd8e5-136">Para obter uma lista de todos os métodos definidos por essa interface, consulte [**ISCardFileAccess**](iscardfileaccess.md).</span><span class="sxs-lookup"><span data-stu-id="fd8e5-136">For a list of all the methods defined by this interface, see [**ISCardFileAccess**](iscardfileaccess.md).</span></span>

<span data-ttu-id="fd8e5-137">Além dos códigos de erro COM listados acima, essa interface pode retornar um código de erro de [*cartão inteligente*](../secgloss/s-gly.md) se uma função de cartão inteligente foi chamada para concluir a solicitação.</span><span class="sxs-lookup"><span data-stu-id="fd8e5-137">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="fd8e5-138">Para obter mais informações, consulte [valores de retorno de cartão inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="fd8e5-138">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fd8e5-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fd8e5-139">Requirements</span></span>



| <span data-ttu-id="fd8e5-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="fd8e5-140">Requirement</span></span> | <span data-ttu-id="fd8e5-141">Valor</span><span class="sxs-lookup"><span data-stu-id="fd8e5-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="fd8e5-142">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fd8e5-142">Minimum supported client</span></span><br/> | <span data-ttu-id="fd8e5-143">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="fd8e5-143">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="fd8e5-144">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fd8e5-144">Minimum supported server</span></span><br/> | <span data-ttu-id="fd8e5-145">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="fd8e5-145">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="fd8e5-146">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="fd8e5-146">End of client support</span></span><br/>    | <span data-ttu-id="fd8e5-147">Windows XP</span><span class="sxs-lookup"><span data-stu-id="fd8e5-147">Windows XP</span></span><br/>                                |
| <span data-ttu-id="fd8e5-148">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="fd8e5-148">End of server support</span></span><br/>    | <span data-ttu-id="fd8e5-149">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="fd8e5-149">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="fd8e5-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="fd8e5-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd8e5-151">**ISCardFileAccess**</span><span class="sxs-lookup"><span data-stu-id="fd8e5-151">**ISCardFileAccess**</span></span>](iscardfileaccess.md)
</dt> </dl>

 

 
