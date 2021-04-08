---
description: O método AttachByReader abre o cartão inteligente no leitor nomeado.
ms.assetid: a92f3281-5018-4e90-bfa0-f03eb9373bb1
title: 'Método iscard:: AttachByReader (Scardmgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.AttachByReader
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 2607ea2e13be2dcccc3c1b6beebd40c86822d0a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922521"
---
# <a name="iscardattachbyreader-method"></a><span data-ttu-id="2a3a1-103">Método iscard:: AttachByReader</span><span class="sxs-lookup"><span data-stu-id="2a3a1-103">ISCard::AttachByReader method</span></span>

<span data-ttu-id="2a3a1-104">\[O método **AttachByReader** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="2a3a1-104">\[The **AttachByReader** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="2a3a1-105">Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="2a3a1-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="2a3a1-106">Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="2a3a1-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="2a3a1-107">O método **AttachByReader** abre o [*cartão inteligente*](../secgloss/s-gly.md) no [*leitor*](../secgloss/r-gly.md)nomeado.</span><span class="sxs-lookup"><span data-stu-id="2a3a1-107">The **AttachByReader** method opens the [*smart card*](../secgloss/s-gly.md) in the named [*reader*](../secgloss/r-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="2a3a1-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2a3a1-108">Syntax</span></span>


```C++
HRESULT AttachByReader(
  [in] BSTR              bstrReaderName,
  [in] SCARD_SHARE_MODES ShareMode,
  [in] SCARD_PROTOCOLS   PrefProtocol
);
```



## <a name="parameters"></a><span data-ttu-id="2a3a1-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2a3a1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a3a1-110">*bstrReaderName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2a3a1-110">*bstrReaderName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2a3a1-111">Um **BSTR** que contém o nome do leitor de cartão inteligente.</span><span class="sxs-lookup"><span data-stu-id="2a3a1-111">A **BSTR** that contains the name of the smart card reader.</span></span>

</dd> <dt>

<span data-ttu-id="2a3a1-112">*ShareMode* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2a3a1-112">*ShareMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2a3a1-113">Modo no qual solicitar acesso ao cartão inteligente.</span><span class="sxs-lookup"><span data-stu-id="2a3a1-113">Mode in which to claim access to the smart card.</span></span>



| <span data-ttu-id="2a3a1-114">Valor</span><span class="sxs-lookup"><span data-stu-id="2a3a1-114">Value</span></span>                                                                                                                                            | <span data-ttu-id="2a3a1-115">Significado</span><span class="sxs-lookup"><span data-stu-id="2a3a1-115">Meaning</span></span>                                                       |
|--------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="EXCLUSIVE"></span><span id="exclusive"></span><dl> <span data-ttu-id="2a3a1-116"><dt>**Exclude**</dt></span><span class="sxs-lookup"><span data-stu-id="2a3a1-116"><dt>**EXCLUSIVE**</dt></span></span> </dl> | <span data-ttu-id="2a3a1-117">Ninguém mais usa essa conexão com o cartão inteligente.</span><span class="sxs-lookup"><span data-stu-id="2a3a1-117">No one else use this connection to the smart card.</span></span><br/> |
| <span id="SHARED"></span><span id="shared"></span><dl> <span data-ttu-id="2a3a1-118"><dt>**COMPARTILHADO**</dt></span><span class="sxs-lookup"><span data-stu-id="2a3a1-118"><dt>**SHARED**</dt></span></span> </dl>          | <span data-ttu-id="2a3a1-119">Outros aplicativos podem usar essa conexão.</span><span class="sxs-lookup"><span data-stu-id="2a3a1-119">Other applications can use this connection.</span></span><br/>        |



 

</dd> <dt>

<span data-ttu-id="2a3a1-120">*PrefProtocol* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2a3a1-120">*PrefProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2a3a1-121">Valor de protocolo preferencial.</span><span class="sxs-lookup"><span data-stu-id="2a3a1-121">Preferred protocol value.</span></span>

<dl><span id="T0"></span><span id="t0"></span><dt>

<span data-ttu-id="2a3a1-122">**T0**</span><span class="sxs-lookup"><span data-stu-id="2a3a1-122">**T0**</span></span>
</dt><span id="T1"></span><span id="t1"></span><dt>

<span data-ttu-id="2a3a1-123">**T1**</span><span class="sxs-lookup"><span data-stu-id="2a3a1-123">**T1**</span></span>
</dt><span id="RAW"></span><span id="raw"></span><dt>

<span data-ttu-id="2a3a1-124">**RAW**</span><span class="sxs-lookup"><span data-stu-id="2a3a1-124">**RAW**</span></span>
</dt><span id="T0_T1"></span><span id="t0_t1"></span><dt>

<span data-ttu-id="2a3a1-125">**T0 \| T1**</span><span class="sxs-lookup"><span data-stu-id="2a3a1-125">**T0\|T1**</span></span>
</dt> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2a3a1-126">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2a3a1-126">Return value</span></span>

<span data-ttu-id="2a3a1-127">O método retorna um dos seguintes valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="2a3a1-127">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="2a3a1-128">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="2a3a1-128">Return code</span></span>                                                                                  | <span data-ttu-id="2a3a1-129">Descrição</span><span class="sxs-lookup"><span data-stu-id="2a3a1-129">Description</span></span>                                                                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2a3a1-130"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="2a3a1-130"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="2a3a1-131">A abertura no cartão inteligente no leitor nomeado foi concluída com êxito.</span><span class="sxs-lookup"><span data-stu-id="2a3a1-131">Open on the smart card in the named reader has been completed successfully.</span></span><br/>           |
| <dl> <span data-ttu-id="2a3a1-132"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="2a3a1-132"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="2a3a1-133">Há algo errado com um ou mais dos parâmetros passados para a função.</span><span class="sxs-lookup"><span data-stu-id="2a3a1-133">There is something wrong with one or more of the parameters passed into the function.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="2a3a1-134">Comentários</span><span class="sxs-lookup"><span data-stu-id="2a3a1-134">Remarks</span></span>

<span data-ttu-id="2a3a1-135">Além dos códigos de erro COM listados acima, essa interface pode retornar um código de erro de [*cartão inteligente*](../secgloss/s-gly.md) se uma função de cartão inteligente foi chamada para concluir a solicitação.</span><span class="sxs-lookup"><span data-stu-id="2a3a1-135">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="2a3a1-136">Para obter mais informações, consulte [valores de retorno de cartão inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="2a3a1-136">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

<span data-ttu-id="2a3a1-137">Quando terminar de usar o leitor, libere o anexo chamando o método [**iscard::D Etach**](iscard-detach.md) .</span><span class="sxs-lookup"><span data-stu-id="2a3a1-137">When you have finished using the reader, release the attachment by calling the [**ISCard::Detach**](iscard-detach.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="2a3a1-138">Exemplos</span><span class="sxs-lookup"><span data-stu-id="2a3a1-138">Examples</span></span>

<span data-ttu-id="2a3a1-139">O exemplo a seguir mostra a anexação a um cartão inteligente em um leitor de cartão inteligente especificado.</span><span class="sxs-lookup"><span data-stu-id="2a3a1-139">The following example shows attaching to a smart card in a specified smart card reader.</span></span>


```C++
#include <windows.h>
#include <stdio.h>
#include <Scardmgr.h>

// The reader name is vendor specific; change as needed.
#define READER_NAME L"Vendor Reader 0"

void main()
{
    BSTR     bstrReader = NULL;
    HRESULT  hr;

    bstrReader = SysAllocString(READER_NAME);
    if (NULL == bstrReader)
    {
        // Error encountered.
        exit(1);
    }

    // Connect to the reader.
    hr = pISCard->AttachByReader(bstrReader, SHARED, T0);
    if (FAILED(hr))
    {
        printf("Failed AttachByReader\n");
        // Take other error handling action.
        // ...
    }

    // Detach reader by calling ISCard::Detach (not shown).
    // ...

    // When done, free BSTR.
    if (NULL != bstrReader)
        SysFreeString(bstrReader);
}
```



## <a name="requirements"></a><span data-ttu-id="2a3a1-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2a3a1-140">Requirements</span></span>



| <span data-ttu-id="2a3a1-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="2a3a1-141">Requirement</span></span> | <span data-ttu-id="2a3a1-142">Valor</span><span class="sxs-lookup"><span data-stu-id="2a3a1-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2a3a1-143">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2a3a1-143">Minimum supported client</span></span><br/> | <span data-ttu-id="2a3a1-144">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="2a3a1-144">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="2a3a1-145">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2a3a1-145">Minimum supported server</span></span><br/> | <span data-ttu-id="2a3a1-146">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2a3a1-146">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2a3a1-147">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="2a3a1-147">End of client support</span></span><br/>    | <span data-ttu-id="2a3a1-148">Windows XP</span><span class="sxs-lookup"><span data-stu-id="2a3a1-148">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="2a3a1-149">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="2a3a1-149">End of server support</span></span><br/>    | <span data-ttu-id="2a3a1-150">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2a3a1-150">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="2a3a1-151">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2a3a1-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="2a3a1-152"><dt>Scardmgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="2a3a1-152"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="2a3a1-153">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="2a3a1-153">Type library</span></span><br/>             | <dl> <span data-ttu-id="2a3a1-154"><dt>Scardmgr. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="2a3a1-154"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="2a3a1-155">DLL</span><span class="sxs-lookup"><span data-stu-id="2a3a1-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2a3a1-156"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2a3a1-156"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="2a3a1-157">IID</span><span class="sxs-lookup"><span data-stu-id="2a3a1-157">IID</span></span><br/>                      | <span data-ttu-id="2a3a1-158">\_O IID iscard é definido como 1461AAC3-6810-11D0-918F-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="2a3a1-158">IID\_ISCard is defined as 1461AAC3-6810-11D0-918F-00AA00C18068</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="2a3a1-159">Confira também</span><span class="sxs-lookup"><span data-stu-id="2a3a1-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a3a1-160">**AttachByHandle**</span><span class="sxs-lookup"><span data-stu-id="2a3a1-160">**AttachByHandle**</span></span>](iscard-attachbyhandle.md)
</dt> <dt>

[<span data-ttu-id="2a3a1-161">**Detach**</span><span class="sxs-lookup"><span data-stu-id="2a3a1-161">**Detach**</span></span>](iscard-detach.md)
</dt> <dt>

[<span data-ttu-id="2a3a1-162">**Iscard**</span><span class="sxs-lookup"><span data-stu-id="2a3a1-162">**ISCard**</span></span>](iscard.md)
</dt> <dt>

[<span data-ttu-id="2a3a1-163">**Anexar novamente**</span><span class="sxs-lookup"><span data-stu-id="2a3a1-163">**ReAttach**</span></span>](iscard-reattach.md)
</dt> </dl>

 

 
