---
description: Faz com que o arquivo especificado (EF ou DF) não seja válido. Um arquivo que não é válido não pode ser acessado por outros métodos antes de usar o rehabilitate.
ms.assetid: 5600fcf0-091c-437e-a45c-4de5b0a47d68
title: 'Método ISCardFileAccess:: Invalidate'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.Invalidate
api_type:
- COM
api_location: ''
ms.openlocfilehash: 3e1d74885f97eca64f403155f1dba52e398b9426
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105752227"
---
# <a name="iscardfileaccessinvalidate-method"></a><span data-ttu-id="45dd8-104">Método ISCardFileAccess:: Invalidate</span><span class="sxs-lookup"><span data-stu-id="45dd8-104">ISCardFileAccess::Invalidate method</span></span>

<span data-ttu-id="45dd8-105">\[O método **Invalidate** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="45dd8-105">\[The **Invalidate** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="45dd8-106">Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="45dd8-106">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="45dd8-107">Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="45dd8-107">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="45dd8-108">O método **Invalidate** faz com que o arquivo especificado (EF ou DF) não seja válido.</span><span class="sxs-lookup"><span data-stu-id="45dd8-108">The **Invalidate** method makes the specified file (EF or DF) not valid.</span></span> <span data-ttu-id="45dd8-109">Um arquivo que não é válido não pode ser acessado por outros métodos antes de usar o [**rehabilitate**](iscardfileaccess-rehabilitate.md).</span><span class="sxs-lookup"><span data-stu-id="45dd8-109">A file that is not valid cannot be accessed by other methods prior to using [**Rehabilitate**](iscardfileaccess-rehabilitate.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="45dd8-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="45dd8-110">Syntax</span></span>


```C++
HRESULT Invalidate(
  [in] BSTR        bstrPathSpec,
  [in] SCARD_FLAGS flags
);
```



## <a name="parameters"></a><span data-ttu-id="45dd8-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="45dd8-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45dd8-112">*bstrPathSpec* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="45dd8-112">*bstrPathSpec* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45dd8-113">Grupo.</span><span class="sxs-lookup"><span data-stu-id="45dd8-113">File.</span></span>

</dd> <dt>

<span data-ttu-id="45dd8-114">*sinalizadores* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="45dd8-114">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45dd8-115">Especifica se as mensagens seguras devem ser usadas.</span><span class="sxs-lookup"><span data-stu-id="45dd8-115">Specifies whether secure messaging should be used.</span></span>

<dl><span id="SC_FL_SECURE_MESSAGING"></span><span id="sc_fl_secure_messaging"></span><dt>

<span data-ttu-id="45dd8-116">**\_ \_ mensagens seguras do SC FL \_**</span><span class="sxs-lookup"><span data-stu-id="45dd8-116">**SC\_FL\_SECURE\_MESSAGING**</span></span>
</dt> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="45dd8-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="45dd8-117">Return value</span></span>

<span data-ttu-id="45dd8-118">O método retorna um dos seguintes valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="45dd8-118">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="45dd8-119">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="45dd8-119">Return code</span></span>                                                                                   | <span data-ttu-id="45dd8-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="45dd8-120">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="45dd8-121"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="45dd8-121"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="45dd8-122">Operação concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="45dd8-122">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="45dd8-123"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="45dd8-123"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="45dd8-124">Um parâmetro não é válido.</span><span class="sxs-lookup"><span data-stu-id="45dd8-124">A parameter is not valid.</span></span><br/>         |
| <dl> <span data-ttu-id="45dd8-125"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="45dd8-125"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="45dd8-126">Um ponteiro inadequado foi passado.</span><span class="sxs-lookup"><span data-stu-id="45dd8-126">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="45dd8-127"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="45dd8-127"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="45dd8-128">Sem memória.</span><span class="sxs-lookup"><span data-stu-id="45dd8-128">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="45dd8-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="45dd8-129">Remarks</span></span>

<span data-ttu-id="45dd8-130">Para obter uma lista de todos os métodos definidos por essa interface, consulte [**ISCardFileAccess**](iscardfileaccess.md).</span><span class="sxs-lookup"><span data-stu-id="45dd8-130">For a list of all the methods defined by this interface, see [**ISCardFileAccess**](iscardfileaccess.md).</span></span>

<span data-ttu-id="45dd8-131">Além dos códigos de erro COM listados acima, essa interface pode retornar um código de erro de [*cartão inteligente*](../secgloss/s-gly.md) se uma função de cartão inteligente foi chamada para concluir a solicitação.</span><span class="sxs-lookup"><span data-stu-id="45dd8-131">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="45dd8-132">Para obter mais informações, consulte [valores de retorno de cartão inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="45dd8-132">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="45dd8-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="45dd8-133">Requirements</span></span>



| <span data-ttu-id="45dd8-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="45dd8-134">Requirement</span></span> | <span data-ttu-id="45dd8-135">Valor</span><span class="sxs-lookup"><span data-stu-id="45dd8-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="45dd8-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="45dd8-136">Minimum supported client</span></span><br/> | <span data-ttu-id="45dd8-137">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="45dd8-137">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="45dd8-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="45dd8-138">Minimum supported server</span></span><br/> | <span data-ttu-id="45dd8-139">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="45dd8-139">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="45dd8-140">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="45dd8-140">End of client support</span></span><br/>    | <span data-ttu-id="45dd8-141">Windows XP</span><span class="sxs-lookup"><span data-stu-id="45dd8-141">Windows XP</span></span><br/>                                |
| <span data-ttu-id="45dd8-142">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="45dd8-142">End of server support</span></span><br/>    | <span data-ttu-id="45dd8-143">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="45dd8-143">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="45dd8-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="45dd8-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45dd8-145">**ISCardFileAccess**</span><span class="sxs-lookup"><span data-stu-id="45dd8-145">**ISCardFileAccess**</span></span>](iscardfileaccess.md)
</dt> <dt>

[<span data-ttu-id="45dd8-146">**Rehabilitate**</span><span class="sxs-lookup"><span data-stu-id="45dd8-146">**Rehabilitate**</span></span>](iscardfileaccess-rehabilitate.md)
</dt> </dl>

 

 
