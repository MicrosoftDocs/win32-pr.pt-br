---
description: Cria um arquivo (EF ou DF) que anteriormente não era válido usando o método Invalidate, acessível pelo aplicativo.
ms.assetid: 1906fcc5-ae76-4950-b2eb-e5ce1882637f
title: 'Método ISCardFileAccess:: rehabilitate'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.Rehabilitate
api_type:
- COM
api_location: ''
ms.openlocfilehash: 7ed02131de08104dab8aff23ee9054659fd4cd63
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105747302"
---
# <a name="iscardfileaccessrehabilitate-method"></a><span data-ttu-id="2710c-103">Método ISCardFileAccess:: rehabilitate</span><span class="sxs-lookup"><span data-stu-id="2710c-103">ISCardFileAccess::Rehabilitate method</span></span>

<span data-ttu-id="2710c-104">\[O método **rehabilitate** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="2710c-104">\[The **Rehabilitate** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="2710c-105">Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="2710c-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="2710c-106">Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="2710c-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="2710c-107">O método **rehabilitate** cria um arquivo (EF ou DF) que anteriormente não era válido usando o método [**Invalidate**](iscardfileaccess-invalidate.md) , acessível pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="2710c-107">The **Rehabilitate** method makes a file (EF or DF) that was previously made not valid by using the [**Invalidate**](iscardfileaccess-invalidate.md) method, accessible by the application.</span></span>

## <a name="syntax"></a><span data-ttu-id="2710c-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2710c-108">Syntax</span></span>


```C++
HRESULT Rehabilitate(
  [in] BSTR        bstrPathSpec,
  [in] SCARD_FLAGS flags
);
```



## <a name="parameters"></a><span data-ttu-id="2710c-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2710c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2710c-110">*bstrPathSpec* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2710c-110">*bstrPathSpec* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2710c-111">Arquivo para rehabilitate.</span><span class="sxs-lookup"><span data-stu-id="2710c-111">File to rehabilitate.</span></span>

</dd> <dt>

<span data-ttu-id="2710c-112">*sinalizadores* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="2710c-112">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2710c-113">Especifica se as mensagens seguras devem ser usadas.</span><span class="sxs-lookup"><span data-stu-id="2710c-113">Specifies whether secure messaging should be used.</span></span>

<dl><span id="SC_FL_SECURE_MESSAGING"></span><span id="sc_fl_secure_messaging"></span><dt>

<span data-ttu-id="2710c-114">**\_ \_ mensagens seguras do SC FL \_**</span><span class="sxs-lookup"><span data-stu-id="2710c-114">**SC\_FL\_SECURE\_MESSAGING**</span></span>
</dt> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2710c-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2710c-115">Return value</span></span>

<span data-ttu-id="2710c-116">O método retorna um dos seguintes valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="2710c-116">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="2710c-117">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="2710c-117">Return code</span></span>                                                                                   | <span data-ttu-id="2710c-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="2710c-118">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="2710c-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="2710c-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="2710c-120">Operação concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="2710c-120">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="2710c-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="2710c-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="2710c-122">Um parâmetro não é válido.</span><span class="sxs-lookup"><span data-stu-id="2710c-122">A parameter is not valid.</span></span><br/>         |
| <dl> <span data-ttu-id="2710c-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="2710c-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="2710c-124">Sem memória.</span><span class="sxs-lookup"><span data-stu-id="2710c-124">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="2710c-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="2710c-125">Remarks</span></span>

<span data-ttu-id="2710c-126">Para obter uma lista de todos os métodos definidos por essa interface, consulte [**ISCardFileAccess**](iscardfileaccess.md).</span><span class="sxs-lookup"><span data-stu-id="2710c-126">For a list of all the methods defined by this interface, see [**ISCardFileAccess**](iscardfileaccess.md).</span></span>

<span data-ttu-id="2710c-127">Além dos códigos de erro COM listados acima, essa interface pode retornar um código de erro de [*cartão inteligente*](../secgloss/s-gly.md) se uma função de cartão inteligente foi chamada para concluir a solicitação.</span><span class="sxs-lookup"><span data-stu-id="2710c-127">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="2710c-128">Para obter mais informações, consulte [valores de retorno de cartão inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="2710c-128">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2710c-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2710c-129">Requirements</span></span>



| <span data-ttu-id="2710c-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="2710c-130">Requirement</span></span> | <span data-ttu-id="2710c-131">Valor</span><span class="sxs-lookup"><span data-stu-id="2710c-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="2710c-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2710c-132">Minimum supported client</span></span><br/> | <span data-ttu-id="2710c-133">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="2710c-133">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="2710c-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2710c-134">Minimum supported server</span></span><br/> | <span data-ttu-id="2710c-135">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2710c-135">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="2710c-136">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="2710c-136">End of client support</span></span><br/>    | <span data-ttu-id="2710c-137">Windows XP</span><span class="sxs-lookup"><span data-stu-id="2710c-137">Windows XP</span></span><br/>                                |
| <span data-ttu-id="2710c-138">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="2710c-138">End of server support</span></span><br/>    | <span data-ttu-id="2710c-139">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2710c-139">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="2710c-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="2710c-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2710c-141">**Invalidar**</span><span class="sxs-lookup"><span data-stu-id="2710c-141">**Invalidate**</span></span>](iscardfileaccess-invalidate.md)
</dt> <dt>

[<span data-ttu-id="2710c-142">**ISCardFileAccess**</span><span class="sxs-lookup"><span data-stu-id="2710c-142">**ISCardFileAccess**</span></span>](iscardfileaccess.md)
</dt> </dl>

 

 
