---
description: Define o segundo parâmetro (P2) de byte na APDU (unidade de dados do protocolo de aplicativo).
ms.assetid: 8d11b967-33cd-4bfa-b294-cc0c422cf6cf
title: 'ISCardCmd: método de ut_P2 de:p (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.put_P2
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 362da530dece37a0a0ca600b1edb414d29e1bd48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164284"
---
# <a name="iscardcmdput_p2-method"></a><span data-ttu-id="4581e-103">ISCardCmd::p \_ método UT P2</span><span class="sxs-lookup"><span data-stu-id="4581e-103">ISCardCmd::put\_P2 method</span></span>

<span data-ttu-id="4581e-104">\[O método **Put \_ P2** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="4581e-104">\[The **put\_P2** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="4581e-105">Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="4581e-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="4581e-106">Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="4581e-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="4581e-107">O método **Put \_ P2** define o segundo byte do parâmetro (P2) na [*unidade de dados do protocolo de aplicativo*](../secgloss/a-gly.md) (APDU).</span><span class="sxs-lookup"><span data-stu-id="4581e-107">The **put\_P2** method sets the second parameter (P2) byte in the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span>

## <a name="syntax"></a><span data-ttu-id="4581e-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4581e-108">Syntax</span></span>


```C++
HRESULT put_P2(
  [in] BYTE byP2
);
```



## <a name="parameters"></a><span data-ttu-id="4581e-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4581e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4581e-110">*byP2* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4581e-110">*byP2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4581e-111">O byte que é o campo P2.</span><span class="sxs-lookup"><span data-stu-id="4581e-111">The byte that is the P2 field.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4581e-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4581e-112">Return value</span></span>

<span data-ttu-id="4581e-113">O método retorna um dos seguintes valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="4581e-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="4581e-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="4581e-114">Return code</span></span>                                                                                   | <span data-ttu-id="4581e-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="4581e-115">Description</span></span>                                   |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="4581e-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="4581e-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="4581e-117">Operação concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="4581e-117">Operation completed successfully.</span></span><br/>  |
| <dl> <span data-ttu-id="4581e-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="4581e-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="4581e-119">O parâmetro *byP2* não é válido.</span><span class="sxs-lookup"><span data-stu-id="4581e-119">The *byP2* parameter is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="4581e-120"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="4581e-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="4581e-121">Sem memória.</span><span class="sxs-lookup"><span data-stu-id="4581e-121">Out of memory.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="4581e-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="4581e-122">Remarks</span></span>

<span data-ttu-id="4581e-123">Para definir o valor P1 do APDU, chame [**Put \_ P1**](iscardcmd-put-p1.md).</span><span class="sxs-lookup"><span data-stu-id="4581e-123">To set the P1 value of the APDU, call [**put\_P1**](iscardcmd-put-p1.md).</span></span>

<span data-ttu-id="4581e-124">Para recuperar os valores P1, P2 e P3 existentes, chame [**Get \_ P1**](iscardcmd-get-p1.md), [**Get \_ P2**](iscardcmd-get-p2.md) ou [**Get \_ P3**](iscardcmd-get-p3.md) respectivamente.</span><span class="sxs-lookup"><span data-stu-id="4581e-124">To retrieve the existing P1, P2, and P3 values, call [**get\_P1**](iscardcmd-get-p1.md), [**get\_P2**](iscardcmd-get-p2.md) or [**get\_P3**](iscardcmd-get-p3.md) respectively.</span></span>

<span data-ttu-id="4581e-125">Para obter uma lista de todos os métodos fornecidos por essa interface, consulte [**ISCardCmd**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="4581e-125">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="4581e-126">Além dos códigos de erro COM listados acima, essa interface pode retornar um código de erro de [*cartão inteligente*](../secgloss/s-gly.md) se uma função de cartão inteligente foi chamada para concluir a solicitação.</span><span class="sxs-lookup"><span data-stu-id="4581e-126">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="4581e-127">Para obter mais informações, consulte [valores de retorno de cartão inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="4581e-127">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="4581e-128">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4581e-128">Examples</span></span>

<span data-ttu-id="4581e-129">O exemplo a seguir mostra como definir o segundo byte do parâmetro (P2) da [*unidade de dados do protocolo de aplicativo*](../secgloss/a-gly.md) (APDU).</span><span class="sxs-lookup"><span data-stu-id="4581e-129">The following example shows how to set the second parameter (P2) byte of the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span> <span data-ttu-id="4581e-130">O exemplo supõe que pISCardCmd é um ponteiro válido para uma instância da interface [**ISCardCmd**](iscardcmd.md) .</span><span class="sxs-lookup"><span data-stu-id="4581e-130">The example assumes that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
HRESULT  hr;

// Set the P2 byte.
hr = pISCardCmd->put_P2(0x06);
if (FAILED(hr))
{
  printf("Failed put_P2\n");
  // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="4581e-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4581e-131">Requirements</span></span>



| <span data-ttu-id="4581e-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="4581e-132">Requirement</span></span> | <span data-ttu-id="4581e-133">Valor</span><span class="sxs-lookup"><span data-stu-id="4581e-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4581e-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4581e-134">Minimum supported client</span></span><br/> | <span data-ttu-id="4581e-135">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="4581e-135">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="4581e-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4581e-136">Minimum supported server</span></span><br/> | <span data-ttu-id="4581e-137">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4581e-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4581e-138">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="4581e-138">End of client support</span></span><br/>    | <span data-ttu-id="4581e-139">Windows XP</span><span class="sxs-lookup"><span data-stu-id="4581e-139">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="4581e-140">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="4581e-140">End of server support</span></span><br/>    | <span data-ttu-id="4581e-141">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4581e-141">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="4581e-142">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4581e-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="4581e-143"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="4581e-143"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="4581e-144">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="4581e-144">Type library</span></span><br/>             | <dl> <span data-ttu-id="4581e-145"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="4581e-145"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="4581e-146">DLL</span><span class="sxs-lookup"><span data-stu-id="4581e-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4581e-147"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4581e-147"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="4581e-148">IID</span><span class="sxs-lookup"><span data-stu-id="4581e-148">IID</span></span><br/>                      | <span data-ttu-id="4581e-149">IID \_ ISCardCmd é definido como D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="4581e-149">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="4581e-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="4581e-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4581e-151">**obter \_ P1**</span><span class="sxs-lookup"><span data-stu-id="4581e-151">**get\_P1**</span></span>](iscardcmd-get-p1.md)
</dt> <dt>

[<span data-ttu-id="4581e-152">**obter \_ P2**</span><span class="sxs-lookup"><span data-stu-id="4581e-152">**get\_P2**</span></span>](iscardcmd-get-p2.md)
</dt> <dt>

[<span data-ttu-id="4581e-153">**obter \_ P3**</span><span class="sxs-lookup"><span data-stu-id="4581e-153">**get\_P3**</span></span>](iscardcmd-get-p3.md)
</dt> <dt>

[<span data-ttu-id="4581e-154">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="4581e-154">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> <dt>

[<span data-ttu-id="4581e-155">**colocar \_ P1**</span><span class="sxs-lookup"><span data-stu-id="4581e-155">**put\_P1**</span></span>](iscardcmd-put-p1.md)
</dt> </dl>

 

 
