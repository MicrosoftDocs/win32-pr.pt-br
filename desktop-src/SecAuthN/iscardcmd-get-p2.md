---
description: Recupera o segundo byte do parâmetro (P2) da unidade de dados do protocolo de aplicativo (APDU).
ms.assetid: c719786f-0f50-472e-a92e-a64c333fc255
title: 'Método ISCardCmd:: get_P2 (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_P2
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 7811ad3e42264477210830f340338d0786ed5547
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090465"
---
# <a name="iscardcmdget_p2-method"></a><span data-ttu-id="b984a-103">Método ISCardCmd:: get \_ P2</span><span class="sxs-lookup"><span data-stu-id="b984a-103">ISCardCmd::get\_P2 method</span></span>

<span data-ttu-id="b984a-104">\[O método **Get \_ P2** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="b984a-104">\[The **get\_P2** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="b984a-105">Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="b984a-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="b984a-106">Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="b984a-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="b984a-107">O método **Get \_ P2** recupera o segundo byte do parâmetro (P2) da [*unidade de dados do protocolo de aplicativo*](../secgloss/a-gly.md) (APDU).</span><span class="sxs-lookup"><span data-stu-id="b984a-107">The **get\_P2** method retrieves the second parameter (P2) byte from the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span>

## <a name="syntax"></a><span data-ttu-id="b984a-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b984a-108">Syntax</span></span>


```C++
HRESULT get_P2(
  [out] BYTE *pbyP2
);
```



## <a name="parameters"></a><span data-ttu-id="b984a-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b984a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b984a-110">*pbyP2* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="b984a-110">*pbyP2* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b984a-111">Ponteiro para o byte que é o P2 do APDU no retorno.</span><span class="sxs-lookup"><span data-stu-id="b984a-111">Pointer to the byte that is the P2 from the APDU on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b984a-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b984a-112">Return value</span></span>

<span data-ttu-id="b984a-113">O método retorna um dos seguintes valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="b984a-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="b984a-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="b984a-114">Return code</span></span>                                                                                   | <span data-ttu-id="b984a-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="b984a-115">Description</span></span>                                     |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="b984a-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b984a-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="b984a-117">Operação concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="b984a-117">Operation completed successfully.</span></span><br/>    |
| <dl> <span data-ttu-id="b984a-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="b984a-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="b984a-119">O parâmetro *pbyP2* não é válido.</span><span class="sxs-lookup"><span data-stu-id="b984a-119">The *pbyP2* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="b984a-120"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="b984a-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="b984a-121">Um ponteiro inadequado foi passado em *pbyP2*.</span><span class="sxs-lookup"><span data-stu-id="b984a-121">A bad pointer was passed in *pbyP2*.</span></span><br/> |
| <dl> <span data-ttu-id="b984a-122"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="b984a-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="b984a-123">Sem memória.</span><span class="sxs-lookup"><span data-stu-id="b984a-123">Out of memory.</span></span><br/>                       |



 

## <a name="remarks"></a><span data-ttu-id="b984a-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="b984a-124">Remarks</span></span>

<span data-ttu-id="b984a-125">Para definir o parâmetro P2 como um novo valor, chame [**Put \_ P2**](iscardcmd-put-p2.md).</span><span class="sxs-lookup"><span data-stu-id="b984a-125">To set the P2 parameter to a new value, call [**put\_P2**](iscardcmd-put-p2.md).</span></span>

<span data-ttu-id="b984a-126">Para obter os parâmetros P1 ou P3, chame [**Get \_ P1**](iscardcmd-get-p1.md) e [**Get \_ P3**](iscardcmd-get-p3.md) respectivamente.</span><span class="sxs-lookup"><span data-stu-id="b984a-126">To get the P1 or P3 parameters, call [**get\_P1**](iscardcmd-get-p1.md) and [**get\_P3**](iscardcmd-get-p3.md) respectively.</span></span>

<span data-ttu-id="b984a-127">Para obter uma lista de todos os métodos fornecidos por essa interface, consulte [**ISCardCmd**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="b984a-127">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="b984a-128">Além dos códigos de erro COM listados acima, essa interface pode retornar um código de erro de [*cartão inteligente*](../secgloss/s-gly.md) se uma função de cartão inteligente foi chamada para concluir a solicitação.</span><span class="sxs-lookup"><span data-stu-id="b984a-128">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="b984a-129">Para obter mais informações, consulte [valores de retorno de cartão inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="b984a-129">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="b984a-130">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b984a-130">Examples</span></span>

<span data-ttu-id="b984a-131">O exemplo a seguir mostra como recuperar o segundo byte do parâmetro (P2) da [*unidade de dados do protocolo de aplicativo*](../secgloss/a-gly.md) (APDU).</span><span class="sxs-lookup"><span data-stu-id="b984a-131">The following example shows how to retrieve the second parameter (P2) byte from the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span> <span data-ttu-id="b984a-132">O exemplo supõe que pISCardCmd é um ponteiro válido para uma instância da interface [**ISCardCmd**](iscardcmd.md) .</span><span class="sxs-lookup"><span data-stu-id="b984a-132">The example assumes that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
BYTE  byP2;
HRESULT  hr;

// Retrieve the P2 byte.
hr = pISCardCmd->get_P2(&byP2);
if (FAILED(hr))
{
  printf("Failed get_P2\n");
  // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="b984a-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b984a-133">Requirements</span></span>



| <span data-ttu-id="b984a-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="b984a-134">Requirement</span></span> | <span data-ttu-id="b984a-135">Valor</span><span class="sxs-lookup"><span data-stu-id="b984a-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b984a-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b984a-136">Minimum supported client</span></span><br/> | <span data-ttu-id="b984a-137">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="b984a-137">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="b984a-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b984a-138">Minimum supported server</span></span><br/> | <span data-ttu-id="b984a-139">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b984a-139">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b984a-140">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="b984a-140">End of client support</span></span><br/>    | <span data-ttu-id="b984a-141">Windows XP</span><span class="sxs-lookup"><span data-stu-id="b984a-141">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="b984a-142">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="b984a-142">End of server support</span></span><br/>    | <span data-ttu-id="b984a-143">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b984a-143">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="b984a-144">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b984a-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="b984a-145"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="b984a-145"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="b984a-146">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="b984a-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="b984a-147"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="b984a-147"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="b984a-148">DLL</span><span class="sxs-lookup"><span data-stu-id="b984a-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b984a-149"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b984a-149"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="b984a-150">IID</span><span class="sxs-lookup"><span data-stu-id="b984a-150">IID</span></span><br/>                      | <span data-ttu-id="b984a-151">IID \_ ISCardCmd é definido como D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="b984a-151">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="b984a-152">Confira também</span><span class="sxs-lookup"><span data-stu-id="b984a-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b984a-153">**obter \_ P1**</span><span class="sxs-lookup"><span data-stu-id="b984a-153">**get\_P1**</span></span>](iscardcmd-get-p1.md)
</dt> <dt>

[<span data-ttu-id="b984a-154">**obter \_ P3**</span><span class="sxs-lookup"><span data-stu-id="b984a-154">**get\_P3**</span></span>](iscardcmd-get-p3.md)
</dt> <dt>

[<span data-ttu-id="b984a-155">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="b984a-155">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> <dt>

[<span data-ttu-id="b984a-156">**colocar \_ P2**</span><span class="sxs-lookup"><span data-stu-id="b984a-156">**put\_P2**</span></span>](iscardcmd-put-p2.md)
</dt> </dl>

 

 
