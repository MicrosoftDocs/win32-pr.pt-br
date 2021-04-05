---
description: Define o identificador de instrução fornecido na APDU (unidade de dados do protocolo de aplicativo).
ms.assetid: ea527ffd-b053-467d-883d-b93d5bbfb071
title: 'ISCardCmd: método de ut_InstructionId de:p (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.put_InstructionId
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 6194accfb834152cf07a58fbb8036b13d3fdcd5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921152"
---
# <a name="iscardcmdput_instructionid-method"></a><span data-ttu-id="b6688-103">ISCardCmd::p \_ método de instruções UT</span><span class="sxs-lookup"><span data-stu-id="b6688-103">ISCardCmd::put\_InstructionId method</span></span>

<span data-ttu-id="b6688-104">\[O método de **\_ instrução Put** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="b6688-104">\[The **put\_InstructionId** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="b6688-105">Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="b6688-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="b6688-106">Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="b6688-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="b6688-107">O método de **\_ instrução Put** define o identificador de instrução fornecido na APDU ( [*unidade de dados do protocolo de aplicativo*](../secgloss/a-gly.md) ).</span><span class="sxs-lookup"><span data-stu-id="b6688-107">The **put\_InstructionId** method sets the given instruction identifier in the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span>

## <a name="syntax"></a><span data-ttu-id="b6688-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b6688-108">Syntax</span></span>


```C++
HRESULT put_InstructionId(
  [in] BYTE byIns
);
```



## <a name="parameters"></a><span data-ttu-id="b6688-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b6688-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6688-110">*byIns* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b6688-110">*byIns* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6688-111">O byte que é o identificador de instrução.</span><span class="sxs-lookup"><span data-stu-id="b6688-111">The byte that is the instruction identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6688-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b6688-112">Return value</span></span>

<span data-ttu-id="b6688-113">O método retorna um dos seguintes valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="b6688-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="b6688-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="b6688-114">Return code</span></span>                                                                                   | <span data-ttu-id="b6688-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="b6688-115">Description</span></span>                                    |
|-----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="b6688-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b6688-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="b6688-117">Operação concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="b6688-117">Operation completed successfully.</span></span><br/>   |
| <dl> <span data-ttu-id="b6688-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="b6688-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="b6688-119">O parâmetro *byIns* não é válido.</span><span class="sxs-lookup"><span data-stu-id="b6688-119">The *byIns* parameter is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="b6688-120"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="b6688-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="b6688-121">Sem memória.</span><span class="sxs-lookup"><span data-stu-id="b6688-121">Out of memory.</span></span><br/>                      |



 

## <a name="remarks"></a><span data-ttu-id="b6688-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="b6688-122">Remarks</span></span>

<span data-ttu-id="b6688-123">Para obter o identificador de instrução existente, chame [**Get \_ educaid**](iscardcmd-get-instructionid.md).</span><span class="sxs-lookup"><span data-stu-id="b6688-123">To get the existing instructional identifier, call [**get\_InstructionId**](iscardcmd-get-instructionid.md).</span></span>

<span data-ttu-id="b6688-124">Para obter uma lista de todos os métodos fornecidos por essa interface, consulte [**ISCardCmd**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="b6688-124">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="b6688-125">Além dos códigos de erro COM listados acima, essa interface pode retornar um código de erro de [*cartão inteligente*](../secgloss/s-gly.md) se uma função de cartão inteligente foi chamada para concluir a solicitação.</span><span class="sxs-lookup"><span data-stu-id="b6688-125">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="b6688-126">Para obter mais informações, consulte [valores de retorno de cartão inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="b6688-126">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="b6688-127">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b6688-127">Examples</span></span>

<span data-ttu-id="b6688-128">O exemplo a seguir mostra como definir um identificador de instrução na APDU ( [*unidade de dados do protocolo de aplicativo*](../secgloss/a-gly.md) ).</span><span class="sxs-lookup"><span data-stu-id="b6688-128">The following example shows how to set an instruction identifier in the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span> <span data-ttu-id="b6688-129">O exemplo supõe que pISCardCmd é um ponteiro válido para uma instância da interface [**ISCardCmd**](iscardcmd.md) .</span><span class="sxs-lookup"><span data-stu-id="b6688-129">The example assumes that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
HRESULT hr;

// Set the instruction ID.
hr = pISCardCmd->put_InstructionId(0xb2);
if (FAILED(hr))
{
  printf("Failed put_InstructionId\n");
  // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="b6688-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b6688-130">Requirements</span></span>



| <span data-ttu-id="b6688-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="b6688-131">Requirement</span></span> | <span data-ttu-id="b6688-132">Valor</span><span class="sxs-lookup"><span data-stu-id="b6688-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b6688-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b6688-133">Minimum supported client</span></span><br/> | <span data-ttu-id="b6688-134">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="b6688-134">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="b6688-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b6688-135">Minimum supported server</span></span><br/> | <span data-ttu-id="b6688-136">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b6688-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b6688-137">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="b6688-137">End of client support</span></span><br/>    | <span data-ttu-id="b6688-138">Windows XP</span><span class="sxs-lookup"><span data-stu-id="b6688-138">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="b6688-139">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="b6688-139">End of server support</span></span><br/>    | <span data-ttu-id="b6688-140">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b6688-140">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="b6688-141">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b6688-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="b6688-142"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="b6688-142"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="b6688-143">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="b6688-143">Type library</span></span><br/>             | <dl> <span data-ttu-id="b6688-144"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="b6688-144"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="b6688-145">DLL</span><span class="sxs-lookup"><span data-stu-id="b6688-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b6688-146"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b6688-146"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="b6688-147">IID</span><span class="sxs-lookup"><span data-stu-id="b6688-147">IID</span></span><br/>                      | <span data-ttu-id="b6688-148">IID \_ ISCardCmd é definido como D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="b6688-148">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="b6688-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="b6688-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6688-150">**obter \_ instrução**</span><span class="sxs-lookup"><span data-stu-id="b6688-150">**get\_InstructionId**</span></span>](iscardcmd-get-instructionid.md)
</dt> <dt>

[<span data-ttu-id="b6688-151">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="b6688-151">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> </dl>

 

 
