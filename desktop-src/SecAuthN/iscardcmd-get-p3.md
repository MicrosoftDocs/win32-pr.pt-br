---
description: Recupera o terceiro byte do parâmetro (P3) da unidade de dados do protocolo de aplicativo (APDU).
ms.assetid: 5fe90686-f542-42be-91ed-6600eaee3e7b
title: 'Método ISCardCmd:: get_P3 (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_P3
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: b1072fc9c4ca3b2a238cc8893104df1a831c99c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090466"
---
# <a name="iscardcmdget_p3-method"></a><span data-ttu-id="3aff1-103">Método ISCardCmd:: get \_ P3</span><span class="sxs-lookup"><span data-stu-id="3aff1-103">ISCardCmd::get\_P3 method</span></span>

<span data-ttu-id="3aff1-104">\[O método **Get \_ P3** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="3aff1-104">\[The **get\_P3** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="3aff1-105">Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="3aff1-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="3aff1-106">Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="3aff1-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="3aff1-107">O método **Get \_ P3** recupera o terceiro byte do parâmetro (P3) da [*unidade de dados do protocolo de aplicativo*](../secgloss/a-gly.md) (APDU).</span><span class="sxs-lookup"><span data-stu-id="3aff1-107">The **get\_P3** method retrieves the third parameter (P3) byte from the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span> <span data-ttu-id="3aff1-108">Esse valor de byte somente leitura representa o tamanho da parte de dados do APDU.</span><span class="sxs-lookup"><span data-stu-id="3aff1-108">This read-only byte value represents the size of the data portion of the APDU.</span></span>

## <a name="syntax"></a><span data-ttu-id="3aff1-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3aff1-109">Syntax</span></span>


```C++
HRESULT get_P3(
  [out] BYTE *pbyP3
);
```



## <a name="parameters"></a><span data-ttu-id="3aff1-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3aff1-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3aff1-111">*pbyP3* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="3aff1-111">*pbyP3* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3aff1-112">Ponteiro para o byte que é P3 do APDU no retorno.</span><span class="sxs-lookup"><span data-stu-id="3aff1-112">Pointer to the byte that is the P3 from the APDU on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3aff1-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3aff1-113">Return value</span></span>

<span data-ttu-id="3aff1-114">O método retorna um dos seguintes valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="3aff1-114">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="3aff1-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="3aff1-115">Return code</span></span>                                                                                   | <span data-ttu-id="3aff1-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="3aff1-116">Description</span></span>                                     |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="3aff1-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="3aff1-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="3aff1-118">Operação concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="3aff1-118">Operation completed successfully.</span></span><br/>    |
| <dl> <span data-ttu-id="3aff1-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="3aff1-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="3aff1-120">O *pbyP3* não é válido.</span><span class="sxs-lookup"><span data-stu-id="3aff1-120">The *pbyP3* is not valid.</span></span><br/>            |
| <dl> <span data-ttu-id="3aff1-121"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="3aff1-121"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="3aff1-122">Um ponteiro inadequado foi passado em *pbyP3*.</span><span class="sxs-lookup"><span data-stu-id="3aff1-122">A bad pointer was passed in *pbyP3*.</span></span><br/> |
| <dl> <span data-ttu-id="3aff1-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="3aff1-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="3aff1-124">Sem memória.</span><span class="sxs-lookup"><span data-stu-id="3aff1-124">Out of memory.</span></span><br/>                       |



 

## <a name="remarks"></a><span data-ttu-id="3aff1-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="3aff1-125">Remarks</span></span>

<span data-ttu-id="3aff1-126">O parâmetro P3 é somente leitura e, portanto, não pode ser definido.</span><span class="sxs-lookup"><span data-stu-id="3aff1-126">The P3 parameter is read-only, and therefore cannot be set.</span></span>

<span data-ttu-id="3aff1-127">Para obter os parâmetros P1 ou P2, chame [**Get \_ P1**](iscardcmd-get-p1.md) e [**Get \_ P2**](iscardcmd-get-p2.md) , respectivamente.</span><span class="sxs-lookup"><span data-stu-id="3aff1-127">To get the P1 or P2 parameters, call [**get\_P1**](iscardcmd-get-p1.md) and [**get\_P2**](iscardcmd-get-p2.md) respectively.</span></span>

<span data-ttu-id="3aff1-128">Para obter uma lista de todos os métodos fornecidos por essa interface, consulte [**ISCardCmd**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="3aff1-128">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="3aff1-129">Além dos códigos de erro COM listados acima, essa interface pode retornar um código de erro de [*cartão inteligente*](../secgloss/s-gly.md) se uma função de cartão inteligente foi chamada para concluir a solicitação.</span><span class="sxs-lookup"><span data-stu-id="3aff1-129">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="3aff1-130">Para obter mais informações, consulte [valores de retorno de cartão inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="3aff1-130">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="3aff1-131">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3aff1-131">Examples</span></span>

<span data-ttu-id="3aff1-132">O exemplo a seguir mostra como recuperar o terceiro byte do parâmetro (P3) da [*unidade de dados do protocolo de aplicativo*](../secgloss/a-gly.md) (APDU).</span><span class="sxs-lookup"><span data-stu-id="3aff1-132">The following example shows how to retrieve the third parameter (P3) byte from the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span> <span data-ttu-id="3aff1-133">O exemplo supõe que pISCardCmd é um ponteiro válido para uma instância da interface [**ISCardCmd**](iscardcmd.md) .</span><span class="sxs-lookup"><span data-stu-id="3aff1-133">The example assumes that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
BYTE  byP3;
HRESULT  hr;

// Retrieve the P3 byte.
hr = pISCardCmd->get_P3(&byP3);
if (FAILED(hr))
{
  printf("Failed get_P3\n");
  // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="3aff1-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3aff1-134">Requirements</span></span>



| <span data-ttu-id="3aff1-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="3aff1-135">Requirement</span></span> | <span data-ttu-id="3aff1-136">Valor</span><span class="sxs-lookup"><span data-stu-id="3aff1-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3aff1-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3aff1-137">Minimum supported client</span></span><br/> | <span data-ttu-id="3aff1-138">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="3aff1-138">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="3aff1-139">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3aff1-139">Minimum supported server</span></span><br/> | <span data-ttu-id="3aff1-140">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3aff1-140">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3aff1-141">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="3aff1-141">End of client support</span></span><br/>    | <span data-ttu-id="3aff1-142">Windows XP</span><span class="sxs-lookup"><span data-stu-id="3aff1-142">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="3aff1-143">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="3aff1-143">End of server support</span></span><br/>    | <span data-ttu-id="3aff1-144">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="3aff1-144">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="3aff1-145">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3aff1-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="3aff1-146"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="3aff1-146"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="3aff1-147">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="3aff1-147">Type library</span></span><br/>             | <dl> <span data-ttu-id="3aff1-148"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="3aff1-148"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="3aff1-149">DLL</span><span class="sxs-lookup"><span data-stu-id="3aff1-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3aff1-150"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3aff1-150"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="3aff1-151">IID</span><span class="sxs-lookup"><span data-stu-id="3aff1-151">IID</span></span><br/>                      | <span data-ttu-id="3aff1-152">IID \_ ISCardCmd é definido como D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="3aff1-152">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="3aff1-153">Confira também</span><span class="sxs-lookup"><span data-stu-id="3aff1-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3aff1-154">**obter \_ P1**</span><span class="sxs-lookup"><span data-stu-id="3aff1-154">**get\_P1**</span></span>](iscardcmd-get-p1.md)
</dt> <dt>

[<span data-ttu-id="3aff1-155">**obter \_ P2**</span><span class="sxs-lookup"><span data-stu-id="3aff1-155">**get\_P2**</span></span>](iscardcmd-get-p2.md)
</dt> <dt>

[<span data-ttu-id="3aff1-156">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="3aff1-156">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> </dl>

 

 
