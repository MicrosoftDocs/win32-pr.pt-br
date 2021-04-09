---
description: O método Close fecha o arquivo especificado. Não é permitido nenhum acesso adicional ao arquivo.
ms.assetid: fecce23e-8604-4a87-9efb-a26e2498c2f3
title: 'Método ISCardFileAccess:: Close'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.Close
api_type:
- COM
api_location: ''
ms.openlocfilehash: ac08d62e71045df49503eb4c05fcb5ea273b4cf6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090457"
---
# <a name="iscardfileaccessclose-method"></a><span data-ttu-id="1cebf-104">Método ISCardFileAccess:: Close</span><span class="sxs-lookup"><span data-stu-id="1cebf-104">ISCardFileAccess::Close method</span></span>

<span data-ttu-id="1cebf-105">\[O método **Close** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="1cebf-105">\[The **Close** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="1cebf-106">Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="1cebf-106">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="1cebf-107">Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="1cebf-107">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="1cebf-108">O método **Close** fecha o arquivo especificado.</span><span class="sxs-lookup"><span data-stu-id="1cebf-108">The **Close** method closes the specified file.</span></span> <span data-ttu-id="1cebf-109">Não é permitido nenhum acesso adicional ao arquivo.</span><span class="sxs-lookup"><span data-stu-id="1cebf-109">No further access to file is allowed.</span></span>

## <a name="syntax"></a><span data-ttu-id="1cebf-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1cebf-110">Syntax</span></span>


```C++
HRESULT Close(
  [in] HSCARD_FILE hFile
);
```



## <a name="parameters"></a><span data-ttu-id="1cebf-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1cebf-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1cebf-112">*hFile* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1cebf-112">*hFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1cebf-113">Um identificador para o arquivo a ser fechado.</span><span class="sxs-lookup"><span data-stu-id="1cebf-113">A handle to the file to be closed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1cebf-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1cebf-114">Return value</span></span>

<span data-ttu-id="1cebf-115">O método retorna um dos seguintes valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="1cebf-115">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="1cebf-116">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="1cebf-116">Return code</span></span>                                                                                   | <span data-ttu-id="1cebf-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="1cebf-117">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="1cebf-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="1cebf-118"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="1cebf-119">Operação concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="1cebf-119">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="1cebf-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="1cebf-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="1cebf-121">Parâmetro inválido.</span><span class="sxs-lookup"><span data-stu-id="1cebf-121">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="1cebf-122"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="1cebf-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="1cebf-123">Sem memória.</span><span class="sxs-lookup"><span data-stu-id="1cebf-123">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="1cebf-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="1cebf-124">Remarks</span></span>

<span data-ttu-id="1cebf-125">Para abrir um arquivo, chame [**Open**](iscardfileaccess-open.md).</span><span class="sxs-lookup"><span data-stu-id="1cebf-125">To open a file, call [**Open**](iscardfileaccess-open.md).</span></span>

<span data-ttu-id="1cebf-126">Para obter uma lista de todos os métodos definidos por essa interface, consulte [**ISCardFileAccess**](iscardfileaccess.md).</span><span class="sxs-lookup"><span data-stu-id="1cebf-126">For a list of all the methods defined by this interface, see [**ISCardFileAccess**](iscardfileaccess.md).</span></span>

<span data-ttu-id="1cebf-127">Além dos códigos de erro COM listados acima, essa interface pode retornar um código de erro de [*cartão inteligente*](../secgloss/s-gly.md) se uma função de cartão inteligente foi chamada para concluir a solicitação.</span><span class="sxs-lookup"><span data-stu-id="1cebf-127">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="1cebf-128">Para obter mais informações, consulte [valores de retorno de cartão inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="1cebf-128">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1cebf-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1cebf-129">Requirements</span></span>



| <span data-ttu-id="1cebf-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="1cebf-130">Requirement</span></span> | <span data-ttu-id="1cebf-131">Valor</span><span class="sxs-lookup"><span data-stu-id="1cebf-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="1cebf-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1cebf-132">Minimum supported client</span></span><br/> | <span data-ttu-id="1cebf-133">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="1cebf-133">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="1cebf-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1cebf-134">Minimum supported server</span></span><br/> | <span data-ttu-id="1cebf-135">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1cebf-135">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="1cebf-136">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="1cebf-136">End of client support</span></span><br/>    | <span data-ttu-id="1cebf-137">Windows XP</span><span class="sxs-lookup"><span data-stu-id="1cebf-137">Windows XP</span></span><br/>                                |
| <span data-ttu-id="1cebf-138">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="1cebf-138">End of server support</span></span><br/>    | <span data-ttu-id="1cebf-139">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1cebf-139">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="1cebf-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="1cebf-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1cebf-141">**ISCardFileAccess**</span><span class="sxs-lookup"><span data-stu-id="1cebf-141">**ISCardFileAccess**</span></span>](iscardfileaccess.md)
</dt> <dt>

[<span data-ttu-id="1cebf-142">**Aberto**</span><span class="sxs-lookup"><span data-stu-id="1cebf-142">**Open**</span></span>](iscardfileaccess-open.md)
</dt> </dl>

 

 
