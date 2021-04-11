---
description: O método Delete exclui um arquivo em um determinado local dentro do sistema de arquivos do cartão inteligente.
ms.assetid: f51b0329-c5dc-4f70-a92e-19dc0dbc55f8
title: 'ISCardFileAccess: método de:D xcluir'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.Delete
api_type:
- COM
api_location: ''
ms.openlocfilehash: 6331225cd3baf105682e2d275ad6be53f16f5b64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296369"
---
# <a name="iscardfileaccessdelete-method"></a><span data-ttu-id="48ca5-103">ISCardFileAccess: método de:D xcluir</span><span class="sxs-lookup"><span data-stu-id="48ca5-103">ISCardFileAccess::Delete method</span></span>

<span data-ttu-id="48ca5-104">\[O método **delete** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="48ca5-104">\[The **Delete** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="48ca5-105">Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="48ca5-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="48ca5-106">Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="48ca5-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="48ca5-107">O método **delete** exclui um arquivo em um determinado local dentro do sistema de arquivos do [*cartão inteligente*](../secgloss/s-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="48ca5-107">The **Delete** method deletes a file at a given location within the [*smart card*](../secgloss/s-gly.md) file system.</span></span>

## <a name="syntax"></a><span data-ttu-id="48ca5-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="48ca5-108">Syntax</span></span>


```C++
HRESULT Delete(
  [in] REFTYPE     refType,
  [in] BSTR        bstrPathSpec,
  [in] SCARD_FLAGS flags
);
```



## <a name="parameters"></a><span data-ttu-id="48ca5-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="48ca5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48ca5-110">*refType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="48ca5-110">*refType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48ca5-111">Tipo de referência usado em *bstrPathSpec*.</span><span class="sxs-lookup"><span data-stu-id="48ca5-111">Type of reference used in *bstrPathSpec*.</span></span>

<dl><span id="SC_TYPE_BY_NAME"></span><span id="sc_type_by_name"></span><dt>

<span data-ttu-id="48ca5-112">**SC \_ tipo \_ por \_ nome**</span><span class="sxs-lookup"><span data-stu-id="48ca5-112">**SC\_TYPE\_BY\_NAME**</span></span>
</dt><span id="SC_TYPE_BY_ID"></span><span id="sc_type_by_id"></span><dt>

<span data-ttu-id="48ca5-113">**SC \_ tipo \_ por \_ ID**</span><span class="sxs-lookup"><span data-stu-id="48ca5-113">**SC\_TYPE\_BY\_ID**</span></span>
</dt><span id="SC_TYPE_BY_SHORT"></span><span id="sc_type_by_short"></span><dt>

<span data-ttu-id="48ca5-114">**SC \_ tipo \_ por \_ curto**</span><span class="sxs-lookup"><span data-stu-id="48ca5-114">**SC\_TYPE\_BY\_SHORT**</span></span>
</dt><span id="SC_TYPE_BY_ANY"></span><span id="sc_type_by_any"></span><dt>

<span data-ttu-id="48ca5-115">**SC \_ tipo \_ por \_ qualquer**</span><span class="sxs-lookup"><span data-stu-id="48ca5-115">**SC\_TYPE\_BY\_ANY**</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="48ca5-116">*bstrPathSpec* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="48ca5-116">*bstrPathSpec* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48ca5-117">Identificador do arquivo a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="48ca5-117">Identifier of the file to be deleted.</span></span>

</dd> <dt>

<span data-ttu-id="48ca5-118">*sinalizadores* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="48ca5-118">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48ca5-119">Especifica se as mensagens seguras devem ser usadas e os dados alocados.</span><span class="sxs-lookup"><span data-stu-id="48ca5-119">Specifies whether secure messaging has to be used and data preallocated.</span></span>

<dl><span id="SC_FL_SECURE_MESSAGING"></span><span id="sc_fl_secure_messaging"></span><dt>

<span data-ttu-id="48ca5-120">**\_ \_ mensagens seguras do SC FL \_**</span><span class="sxs-lookup"><span data-stu-id="48ca5-120">**SC\_FL\_SECURE\_MESSAGING**</span></span>
</dt><span id="SC_FL_PREALLOCATED"></span><span id="sc_fl_preallocated"></span><dt>

<span data-ttu-id="48ca5-121">**SC \_ fl \_ prealocado**</span><span class="sxs-lookup"><span data-stu-id="48ca5-121">**SC\_FL\_PREALLOCATED**</span></span>
</dt> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="48ca5-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="48ca5-122">Return value</span></span>

<span data-ttu-id="48ca5-123">O método retorna um dos seguintes valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="48ca5-123">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="48ca5-124">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="48ca5-124">Return code</span></span>                                                                                  | <span data-ttu-id="48ca5-125">Descrição</span><span class="sxs-lookup"><span data-stu-id="48ca5-125">Description</span></span>                                               |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <span data-ttu-id="48ca5-126"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="48ca5-126"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="48ca5-127">A operação foi concluída com êxito.</span><span class="sxs-lookup"><span data-stu-id="48ca5-127">Operation was completed successfully.</span></span><br/>          |
| <dl> <span data-ttu-id="48ca5-128"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="48ca5-128"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="48ca5-129">Parâmetro inválido.</span><span class="sxs-lookup"><span data-stu-id="48ca5-129">Invalid parameter.</span></span><br/>                             |
| <dl> <span data-ttu-id="48ca5-130"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="48ca5-130"><dt>**E\_NOTIMPL**</dt></span></span> </dl>    | <span data-ttu-id="48ca5-131">A interface não implementou este método.</span><span class="sxs-lookup"><span data-stu-id="48ca5-131">The interface has not implemented this method.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="48ca5-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="48ca5-132">Remarks</span></span>

<span data-ttu-id="48ca5-133">Para obter uma lista de todos os métodos definidos por essa interface, consulte [**ISCardFileAccess**](iscardfileaccess.md).</span><span class="sxs-lookup"><span data-stu-id="48ca5-133">For a list of all the methods defined by this interface, see [**ISCardFileAccess**](iscardfileaccess.md).</span></span>

<span data-ttu-id="48ca5-134">Além dos códigos de erro COM listados acima, essa interface pode retornar um código de erro de cartão inteligente se uma função de cartão inteligente foi chamada para concluir a solicitação.</span><span class="sxs-lookup"><span data-stu-id="48ca5-134">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="48ca5-135">Para obter mais informações, consulte [valores de retorno de cartão inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="48ca5-135">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="48ca5-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="48ca5-136">Requirements</span></span>



| <span data-ttu-id="48ca5-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="48ca5-137">Requirement</span></span> | <span data-ttu-id="48ca5-138">Valor</span><span class="sxs-lookup"><span data-stu-id="48ca5-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="48ca5-139">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="48ca5-139">Minimum supported client</span></span><br/> | <span data-ttu-id="48ca5-140">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="48ca5-140">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="48ca5-141">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="48ca5-141">Minimum supported server</span></span><br/> | <span data-ttu-id="48ca5-142">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="48ca5-142">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="48ca5-143">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="48ca5-143">End of client support</span></span><br/>    | <span data-ttu-id="48ca5-144">Windows XP</span><span class="sxs-lookup"><span data-stu-id="48ca5-144">Windows XP</span></span><br/>                                |
| <span data-ttu-id="48ca5-145">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="48ca5-145">End of server support</span></span><br/>    | <span data-ttu-id="48ca5-146">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="48ca5-146">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="48ca5-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="48ca5-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48ca5-148">**Criar**</span><span class="sxs-lookup"><span data-stu-id="48ca5-148">**Create**</span></span>](iscardfileaccess-create.md)
</dt> <dt>

[<span data-ttu-id="48ca5-149">**ISCardFileAccess**</span><span class="sxs-lookup"><span data-stu-id="48ca5-149">**ISCardFileAccess**</span></span>](iscardfileaccess.md)
</dt> </dl>

 

 
