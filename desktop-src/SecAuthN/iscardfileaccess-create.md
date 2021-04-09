---
description: O método Create cria um arquivo em um determinado local dentro do sistema de arquivos do cartão inteligente.
ms.assetid: 6bfe0b22-6aad-4818-bb2a-d5b0af4ee3a6
title: 'Método ISCardFileAccess:: Create'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.Create
api_type:
- COM
api_location: ''
ms.openlocfilehash: 2cfc7e1492505191a7912f23e5471f5fa72fdcd8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090455"
---
# <a name="iscardfileaccesscreate-method"></a><span data-ttu-id="b933d-103">Método ISCardFileAccess:: Create</span><span class="sxs-lookup"><span data-stu-id="b933d-103">ISCardFileAccess::Create method</span></span>

<span data-ttu-id="b933d-104">\[O método **Create** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="b933d-104">\[The **Create** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="b933d-105">Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="b933d-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="b933d-106">Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="b933d-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="b933d-107">O método **Create** cria um arquivo em um determinado local dentro do sistema de arquivos do [*cartão inteligente*](../secgloss/s-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="b933d-107">The **Create** method creates a file at a given location within the [*smart card*](../secgloss/s-gly.md) file system.</span></span>

## <a name="syntax"></a><span data-ttu-id="b933d-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b933d-108">Syntax</span></span>


```C++
HRESULT Create(
  [in] REFTYPE      refType,
  [in] BSTR         bstrPathSpec,
  [in] TLV_TABLE    TLV,
  [in] SCARD_FLAGS  flags,
  [in] LPBYTEBUFFER pDataBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="b933d-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b933d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b933d-110">*refType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b933d-110">*refType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b933d-111">Tipo de referência usado em *bstrPathSpec*.</span><span class="sxs-lookup"><span data-stu-id="b933d-111">Type of reference used in *bstrPathSpec*.</span></span>

<dl><span id="SC_TYPE_BY_NAME"></span><span id="sc_type_by_name"></span><dt>

<span data-ttu-id="b933d-112">**SC \_ tipo \_ por \_ nome**</span><span class="sxs-lookup"><span data-stu-id="b933d-112">**SC\_TYPE\_BY\_NAME**</span></span>
</dt><span id="SC_TYPE_BY_ID"></span><span id="sc_type_by_id"></span><dt>

<span data-ttu-id="b933d-113">**SC \_ tipo \_ por \_ ID**</span><span class="sxs-lookup"><span data-stu-id="b933d-113">**SC\_TYPE\_BY\_ID**</span></span>
</dt><span id="SC_TYPE_BY_SHORT"></span><span id="sc_type_by_short"></span><dt>

<span data-ttu-id="b933d-114">**SC \_ tipo \_ por \_ curto**</span><span class="sxs-lookup"><span data-stu-id="b933d-114">**SC\_TYPE\_BY\_SHORT**</span></span>
</dt><span id="SC_TYPE_BY_ANY"></span><span id="sc_type_by_any"></span><dt>

<span data-ttu-id="b933d-115">**SC \_ tipo \_ por \_ qualquer**</span><span class="sxs-lookup"><span data-stu-id="b933d-115">**SC\_TYPE\_BY\_ANY**</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="b933d-116">*bstrPathSpec* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b933d-116">*bstrPathSpec* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b933d-117">ID do arquivo a ser criado no contexto atual.</span><span class="sxs-lookup"><span data-stu-id="b933d-117">File ID to be created within the current context.</span></span>

</dd> <dt>

<span data-ttu-id="b933d-118">*TLV* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b933d-118">*TLV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b933d-119">Lista de estruturas TLV (marca, comprimento, valor) que os valores precisam ser definidos.</span><span class="sxs-lookup"><span data-stu-id="b933d-119">List of TLV (tag,length,value) structures which values have to be set.</span></span>

</dd> <dt>

<span data-ttu-id="b933d-120">*sinalizadores* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="b933d-120">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b933d-121">Especifica se as mensagens seguras devem ser usadas e os dados alocados.</span><span class="sxs-lookup"><span data-stu-id="b933d-121">Specifies whether secure messaging has to be used and data preallocated.</span></span>

<dl><span id="SC_FL_SECURE_MESSAGING"></span><span id="sc_fl_secure_messaging"></span><dt>

<span data-ttu-id="b933d-122">**\_ \_ mensagens seguras do SC FL \_**</span><span class="sxs-lookup"><span data-stu-id="b933d-122">**SC\_FL\_SECURE\_MESSAGING**</span></span>
</dt><span id="SC_FL_PREALLOCATED"></span><span id="sc_fl_preallocated"></span><dt>

<span data-ttu-id="b933d-123">**SC \_ fl \_ prealocado**</span><span class="sxs-lookup"><span data-stu-id="b933d-123">**SC\_FL\_PREALLOCATED**</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="b933d-124">*pDataBuffer* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b933d-124">*pDataBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b933d-125">Ponteiro para dados alocados previamente.</span><span class="sxs-lookup"><span data-stu-id="b933d-125">Pointer to preallocated data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b933d-126">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b933d-126">Return value</span></span>

<span data-ttu-id="b933d-127">O método retorna um dos seguintes valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="b933d-127">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="b933d-128">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="b933d-128">Return code</span></span>                                                                                   | <span data-ttu-id="b933d-129">Descrição</span><span class="sxs-lookup"><span data-stu-id="b933d-129">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="b933d-130"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b933d-130"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="b933d-131">Operação concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="b933d-131">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="b933d-132"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="b933d-132"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="b933d-133">Parâmetro inválido.</span><span class="sxs-lookup"><span data-stu-id="b933d-133">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="b933d-134"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="b933d-134"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="b933d-135">Um ponteiro inadequado foi passado.</span><span class="sxs-lookup"><span data-stu-id="b933d-135">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="b933d-136"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="b933d-136"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="b933d-137">Sem memória.</span><span class="sxs-lookup"><span data-stu-id="b933d-137">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="b933d-138">Comentários</span><span class="sxs-lookup"><span data-stu-id="b933d-138">Remarks</span></span>

<span data-ttu-id="b933d-139">Para obter uma lista de todos os métodos definidos por essa interface, consulte [**ISCardFileAccess**](iscardfileaccess.md).</span><span class="sxs-lookup"><span data-stu-id="b933d-139">For a list of all the methods defined by this interface, see [**ISCardFileAccess**](iscardfileaccess.md).</span></span>

<span data-ttu-id="b933d-140">Além dos códigos de erro COM listados acima, essa interface pode retornar um código de erro de cartão inteligente se uma função de cartão inteligente foi chamada para concluir a solicitação.</span><span class="sxs-lookup"><span data-stu-id="b933d-140">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="b933d-141">Para obter mais informações, consulte [valores de retorno de cartão inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="b933d-141">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b933d-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b933d-142">Requirements</span></span>



| <span data-ttu-id="b933d-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="b933d-143">Requirement</span></span> | <span data-ttu-id="b933d-144">Valor</span><span class="sxs-lookup"><span data-stu-id="b933d-144">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b933d-145">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b933d-145">Minimum supported client</span></span><br/> | <span data-ttu-id="b933d-146">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="b933d-146">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="b933d-147">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b933d-147">Minimum supported server</span></span><br/> | <span data-ttu-id="b933d-148">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b933d-148">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="b933d-149">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="b933d-149">End of client support</span></span><br/>    | <span data-ttu-id="b933d-150">Windows XP</span><span class="sxs-lookup"><span data-stu-id="b933d-150">Windows XP</span></span><br/>                                |
| <span data-ttu-id="b933d-151">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="b933d-151">End of server support</span></span><br/>    | <span data-ttu-id="b933d-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b933d-152">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="b933d-153">Confira também</span><span class="sxs-lookup"><span data-stu-id="b933d-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b933d-154">**ISCardFileAccess**</span><span class="sxs-lookup"><span data-stu-id="b933d-154">**ISCardFileAccess**</span></span>](iscardfileaccess.md)
</dt> </dl>

 

 
