---
description: O método Clear limpa a APDU (unidade de dados do protocolo de aplicativo) e os buffers de mensagens do APDU de resposta.
ms.assetid: 5fd3ebb9-b492-4668-9dd8-3ffbcfceb12c
title: 'Método ISCardCmd:: Clear (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.Clear
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 0701906c38764ed1b4817f40430dde9b48bfb12e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090473"
---
# <a name="iscardcmdclear-method"></a><span data-ttu-id="cbb3b-103">Método ISCardCmd:: Clear</span><span class="sxs-lookup"><span data-stu-id="cbb3b-103">ISCardCmd::Clear method</span></span>

<span data-ttu-id="cbb3b-104">\[O método **Clear** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="cbb3b-104">\[The **Clear** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="cbb3b-105">Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="cbb3b-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="cbb3b-106">Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="cbb3b-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="cbb3b-107">O método **Clear** limpa a APDU ( [*unidade de dados do protocolo de aplicativo*](../secgloss/a-gly.md) ) e os buffers de mensagens do APDU de [*resposta*](../secgloss/r-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="cbb3b-107">The **Clear** method clears the [*application protocol data unit*](../secgloss/a-gly.md) (APDU) and [*reply APDU*](../secgloss/r-gly.md) message buffers.</span></span>

## <a name="syntax"></a><span data-ttu-id="cbb3b-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cbb3b-108">Syntax</span></span>


```C++
HRESULT Clear();
```



## <a name="parameters"></a><span data-ttu-id="cbb3b-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cbb3b-109">Parameters</span></span>

<span data-ttu-id="cbb3b-110">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="cbb3b-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="cbb3b-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cbb3b-111">Return value</span></span>

<span data-ttu-id="cbb3b-112">O método retorna um dos seguintes valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="cbb3b-112">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="cbb3b-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="cbb3b-113">Return code</span></span>                                                                             | <span data-ttu-id="cbb3b-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="cbb3b-114">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="cbb3b-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="cbb3b-115"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="cbb3b-116">Operação concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="cbb3b-116">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="cbb3b-117"><dt>**\_falso**</dt></span><span class="sxs-lookup"><span data-stu-id="cbb3b-117"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="cbb3b-118">Erro desconhecido.</span><span class="sxs-lookup"><span data-stu-id="cbb3b-118">Unknown error.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="cbb3b-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="cbb3b-119">Remarks</span></span>

<span data-ttu-id="cbb3b-120">Para criar um comando APDU, chame [**BuildCmd**](iscardcmd-buildcmd.md).</span><span class="sxs-lookup"><span data-stu-id="cbb3b-120">To build a command APDU, call [**BuildCmd**](iscardcmd-buildcmd.md).</span></span>

<span data-ttu-id="cbb3b-121">Para obter uma lista de todos os métodos fornecidos por essa interface, consulte [**ISCardCmd**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="cbb3b-121">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="cbb3b-122">Além dos códigos de erro COM listados acima, essa interface pode retornar um código de erro de cartão inteligente se uma função de cartão inteligente foi chamada para concluir a solicitação.</span><span class="sxs-lookup"><span data-stu-id="cbb3b-122">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="cbb3b-123">Para obter mais informações, consulte [valores de retorno de cartão inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="cbb3b-123">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="cbb3b-124">Exemplos</span><span class="sxs-lookup"><span data-stu-id="cbb3b-124">Examples</span></span>

<span data-ttu-id="cbb3b-125">O exemplo a seguir mostra como limpar os buffers de mensagens APDU e Reply APDU.</span><span class="sxs-lookup"><span data-stu-id="cbb3b-125">The following example shows how to clear the APDU and reply APDU message buffers.</span></span>


```C++
HRESULT  hr;

hr = pISCardCmd->Clear();
if (FAILED(hr))
{
    printf("Failed ISCardCmd::Clear\n");
    // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="cbb3b-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cbb3b-126">Requirements</span></span>



| <span data-ttu-id="cbb3b-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="cbb3b-127">Requirement</span></span> | <span data-ttu-id="cbb3b-128">Valor</span><span class="sxs-lookup"><span data-stu-id="cbb3b-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cbb3b-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cbb3b-129">Minimum supported client</span></span><br/> | <span data-ttu-id="cbb3b-130">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="cbb3b-130">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="cbb3b-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cbb3b-131">Minimum supported server</span></span><br/> | <span data-ttu-id="cbb3b-132">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="cbb3b-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="cbb3b-133">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="cbb3b-133">End of client support</span></span><br/>    | <span data-ttu-id="cbb3b-134">Windows XP</span><span class="sxs-lookup"><span data-stu-id="cbb3b-134">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="cbb3b-135">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="cbb3b-135">End of server support</span></span><br/>    | <span data-ttu-id="cbb3b-136">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="cbb3b-136">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="cbb3b-137">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cbb3b-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="cbb3b-138"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="cbb3b-138"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="cbb3b-139">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="cbb3b-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="cbb3b-140"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="cbb3b-140"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="cbb3b-141">DLL</span><span class="sxs-lookup"><span data-stu-id="cbb3b-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cbb3b-142"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cbb3b-142"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="cbb3b-143">IID</span><span class="sxs-lookup"><span data-stu-id="cbb3b-143">IID</span></span><br/>                      | <span data-ttu-id="cbb3b-144">IID \_ ISCardCmd é definido como D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="cbb3b-144">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="cbb3b-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="cbb3b-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cbb3b-146">**ISCardCmd::BuildCmd**</span><span class="sxs-lookup"><span data-stu-id="cbb3b-146">**ISCardCmd::BuildCmd**</span></span>](iscardcmd-buildcmd.md)
</dt> <dt>

[<span data-ttu-id="cbb3b-147">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="cbb3b-147">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> </dl>

 

 
