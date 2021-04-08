---
description: Recupera o byte do identificador de instrução da APDU (unidade de dados do protocolo de aplicativo).
ms.assetid: 294f51cd-0a13-4dfb-bf02-9edd11a7085e
title: 'Método ISCardCmd:: get_InstructionId (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_InstructionId
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 4b0125237ef94a5d6173f517483b9ae8781d5607
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922802"
---
# <a name="iscardcmdget_instructionid-method"></a><span data-ttu-id="093c4-103">Método de instrução ISCardCmd:: get \_</span><span class="sxs-lookup"><span data-stu-id="093c4-103">ISCardCmd::get\_InstructionId method</span></span>

<span data-ttu-id="093c4-104">\[O método **Get \_ educaid** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="093c4-104">\[The **get\_InstructionId** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="093c4-105">Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="093c4-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="093c4-106">Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="093c4-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="093c4-107">O método **Get \_ educaid** recupera o byte do identificador de instrução da APDU ( [*unidade de dados do protocolo de aplicativo*](../secgloss/a-gly.md) ).</span><span class="sxs-lookup"><span data-stu-id="093c4-107">The **get\_InstructionId** method retrieves the instruction identifier byte from the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span>

## <a name="syntax"></a><span data-ttu-id="093c4-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="093c4-108">Syntax</span></span>


```C++
HRESULT get_InstructionId(
  [out] BYTE *pbyIns
);
```



## <a name="parameters"></a><span data-ttu-id="093c4-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="093c4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="093c4-110">*pbyIns* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="093c4-110">*pbyIns* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="093c4-111">Ponteiro para o byte que é a ID de instrução do APDU no retorno.</span><span class="sxs-lookup"><span data-stu-id="093c4-111">Pointer to the byte that is the instruction ID from the APDU on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="093c4-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="093c4-112">Return value</span></span>

<span data-ttu-id="093c4-113">O método retorna um dos seguintes valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="093c4-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="093c4-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="093c4-114">Return code</span></span>                                                                                   | <span data-ttu-id="093c4-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="093c4-115">Description</span></span>                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="093c4-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="093c4-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="093c4-117">Operação concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="093c4-117">Operation completed successfully.</span></span><br/>     |
| <dl> <span data-ttu-id="093c4-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="093c4-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="093c4-119">O parâmetro *pbyIns* não é válido.</span><span class="sxs-lookup"><span data-stu-id="093c4-119">The *pbyIns* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="093c4-120"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="093c4-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="093c4-121">Um ponteiro inadequado foi passado em *pbyIns*.</span><span class="sxs-lookup"><span data-stu-id="093c4-121">A bad pointer was passed in *pbyIns*.</span></span><br/> |
| <dl> <span data-ttu-id="093c4-122"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="093c4-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="093c4-123">Sem memória.</span><span class="sxs-lookup"><span data-stu-id="093c4-123">Out of memory.</span></span><br/>                        |



 

## <a name="remarks"></a><span data-ttu-id="093c4-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="093c4-124">Remarks</span></span>

<span data-ttu-id="093c4-125">Para definir o identificador de instruções para um novo valor, chame [**putcollection \_**](iscardcmd-put-instructionid.md).</span><span class="sxs-lookup"><span data-stu-id="093c4-125">To set the instructional identifier to a new value, call [**put\_InstructionId**](iscardcmd-put-instructionid.md).</span></span>

<span data-ttu-id="093c4-126">Para obter uma lista de todos os métodos fornecidos por essa interface, consulte [**ISCardCmd**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="093c4-126">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="093c4-127">Além dos códigos de erro COM listados acima, essa interface pode retornar um código de erro de [*cartão inteligente*](../secgloss/s-gly.md) se uma função de cartão inteligente foi chamada para concluir a solicitação.</span><span class="sxs-lookup"><span data-stu-id="093c4-127">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="093c4-128">Para obter mais informações, consulte [valores de retorno de cartão inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="093c4-128">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="093c4-129">Exemplos</span><span class="sxs-lookup"><span data-stu-id="093c4-129">Examples</span></span>

<span data-ttu-id="093c4-130">O exemplo a seguir mostra como recuperar o byte do identificador de instrução da APDU ( [*unidade de dados do protocolo de aplicativo*](../secgloss/a-gly.md) ).</span><span class="sxs-lookup"><span data-stu-id="093c4-130">The following example shows how to retrieve the instruction identifier byte from the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span> <span data-ttu-id="093c4-131">O exemplo supõe que pISCardCmd é um ponteiro válido para uma instância da interface [**ISCardCmd**](iscardcmd.md) .</span><span class="sxs-lookup"><span data-stu-id="093c4-131">The example assumes that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
BYTE  byInstructID;
HRESULT hr;

// Retrieve the instruction ID.
hr = pISCardCmd->get_InstructionId(&byInstructID);
if (FAILED(hr))
{
  printf("Failed get_InstructionId\n");
  // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="093c4-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="093c4-132">Requirements</span></span>



| <span data-ttu-id="093c4-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="093c4-133">Requirement</span></span> | <span data-ttu-id="093c4-134">Valor</span><span class="sxs-lookup"><span data-stu-id="093c4-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="093c4-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="093c4-135">Minimum supported client</span></span><br/> | <span data-ttu-id="093c4-136">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="093c4-136">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="093c4-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="093c4-137">Minimum supported server</span></span><br/> | <span data-ttu-id="093c4-138">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="093c4-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="093c4-139">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="093c4-139">End of client support</span></span><br/>    | <span data-ttu-id="093c4-140">Windows XP</span><span class="sxs-lookup"><span data-stu-id="093c4-140">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="093c4-141">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="093c4-141">End of server support</span></span><br/>    | <span data-ttu-id="093c4-142">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="093c4-142">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="093c4-143">parâmetro</span><span class="sxs-lookup"><span data-stu-id="093c4-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="093c4-144"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="093c4-144"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="093c4-145">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="093c4-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="093c4-146"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="093c4-146"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="093c4-147">DLL</span><span class="sxs-lookup"><span data-stu-id="093c4-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="093c4-148"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="093c4-148"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="093c4-149">IID</span><span class="sxs-lookup"><span data-stu-id="093c4-149">IID</span></span><br/>                      | <span data-ttu-id="093c4-150">IID \_ ISCardCmd é definido como D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="093c4-150">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="093c4-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="093c4-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="093c4-152">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="093c4-152">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> <dt>

[<span data-ttu-id="093c4-153">**colocar \_ instruçãoid**</span><span class="sxs-lookup"><span data-stu-id="093c4-153">**put\_InstructionId**</span></span>](iscardcmd-put-instructionid.md)
</dt> </dl>

 

 
