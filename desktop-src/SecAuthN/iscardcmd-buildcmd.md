---
description: Constrói uma APDU (unidade de dados de protocolo de aplicativo de comando) válida para transmissão para um cartão inteligente.
ms.assetid: d1003cc3-c235-4635-ad5a-8cea7363bf30
title: 'Método ISCardCmd:: BuildCmd (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.BuildCmd
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: f44597ea087f7ccec191abc9dd03787780e88b2d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170656"
---
# <a name="iscardcmdbuildcmd-method"></a><span data-ttu-id="e50e3-103">Método ISCardCmd:: BuildCmd</span><span class="sxs-lookup"><span data-stu-id="e50e3-103">ISCardCmd::BuildCmd method</span></span>

<span data-ttu-id="e50e3-104">\[O método **BuildCmd** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="e50e3-104">\[The **BuildCmd** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="e50e3-105">Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="e50e3-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="e50e3-106">Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="e50e3-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="e50e3-107">O método **BuildCmd** constrói uma APDU ( [*unidade de dados de protocolo de aplicativo*](../secgloss/a-gly.md) de comando) válida para transmissão para um [*cartão inteligente*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="e50e3-107">The **BuildCmd** method constructs a valid command [*application protocol data unit*](../secgloss/a-gly.md) (APDU) for transmission to a [*smart card*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="e50e3-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e50e3-108">Syntax</span></span>


```C++
HRESULT BuildCmd(
  [in] BYTE         byClassId,
  [in] BYTE         byInsId,
  [in] BYTE         byP1,
  [in] BYTE         byP2,
  [in] LPBYTEBUFFER pbyData,
  [in] LONG         *p1Le
);
```



## <a name="parameters"></a><span data-ttu-id="e50e3-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e50e3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e50e3-110">*byClassId* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e50e3-110">*byClassId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e50e3-111">Identificador de classe de comando.</span><span class="sxs-lookup"><span data-stu-id="e50e3-111">Command class identifier.</span></span>

</dd> <dt>

<span data-ttu-id="e50e3-112">*byInsId* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e50e3-112">*byInsId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e50e3-113">Identificador de instrução de comando.</span><span class="sxs-lookup"><span data-stu-id="e50e3-113">Command instruction identifier.</span></span>

</dd> <dt>

<span data-ttu-id="e50e3-114">*byP1* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e50e3-114">*byP1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e50e3-115">Primeiro parâmetro do comando.</span><span class="sxs-lookup"><span data-stu-id="e50e3-115">Command's first parameter.</span></span>

</dd> <dt>

<span data-ttu-id="e50e3-116">*byP2* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e50e3-116">*byP2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e50e3-117">O segundo parâmetro do comando.</span><span class="sxs-lookup"><span data-stu-id="e50e3-117">Command's second parameter.</span></span>

</dd> <dt>

<span data-ttu-id="e50e3-118">*pbyData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e50e3-118">*pbyData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e50e3-119">Ponteiro para a parte de dados do comando.</span><span class="sxs-lookup"><span data-stu-id="e50e3-119">Pointer to the data portion of the command.</span></span>

</dd> <dt>

<span data-ttu-id="e50e3-120">*p1Le* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e50e3-120">*p1Le* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e50e3-121">Ponteiro para um inteiro longo que contém o comprimento esperado dos dados retornados.</span><span class="sxs-lookup"><span data-stu-id="e50e3-121">Pointer to a LONG integer containing the expected length of the returned data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e50e3-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e50e3-122">Return value</span></span>

<span data-ttu-id="e50e3-123">O método retorna um dos seguintes valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="e50e3-123">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="e50e3-124">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="e50e3-124">Return code</span></span>                                                                                   | <span data-ttu-id="e50e3-125">Descrição</span><span class="sxs-lookup"><span data-stu-id="e50e3-125">Description</span></span>                                    |
|-----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="e50e3-126"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e50e3-126"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="e50e3-127">Operação concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="e50e3-127">Operation completed successfully.</span></span><br/>   |
| <dl> <span data-ttu-id="e50e3-128"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="e50e3-128"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="e50e3-129">Um dos parâmetros não é válido.</span><span class="sxs-lookup"><span data-stu-id="e50e3-129">One of the parameters is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="e50e3-130"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="e50e3-130"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="e50e3-131">Um ponteiro inadequado foi passado.</span><span class="sxs-lookup"><span data-stu-id="e50e3-131">A bad pointer was passed in.</span></span><br/>        |
| <dl> <span data-ttu-id="e50e3-132"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="e50e3-132"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="e50e3-133">Sem memória.</span><span class="sxs-lookup"><span data-stu-id="e50e3-133">Out of memory.</span></span><br/>                      |



 

## <a name="remarks"></a><span data-ttu-id="e50e3-134">Comentários</span><span class="sxs-lookup"><span data-stu-id="e50e3-134">Remarks</span></span>

<span data-ttu-id="e50e3-135">Para encapsular o comando em outro comando, chame [**encapsulate**](iscardcmd-encapsulate.md).</span><span class="sxs-lookup"><span data-stu-id="e50e3-135">To encapsulate the command into another command, call [**Encapsulate**](iscardcmd-encapsulate.md).</span></span>

<span data-ttu-id="e50e3-136">Para obter uma lista de todos os métodos fornecidos por essa interface, consulte [**ISCardCmd**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="e50e3-136">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="e50e3-137">Além dos códigos de erro COM listados acima, essa interface pode retornar um código de erro de cartão inteligente se uma função de cartão inteligente foi chamada para concluir a solicitação.</span><span class="sxs-lookup"><span data-stu-id="e50e3-137">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="e50e3-138">Para obter mais informações, consulte [valores de retorno de cartão inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="e50e3-138">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="e50e3-139">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e50e3-139">Examples</span></span>

<span data-ttu-id="e50e3-140">O exemplo a seguir mostra como construir um comando APDU.</span><span class="sxs-lookup"><span data-stu-id="e50e3-140">The following example shows how to construct a command APDU.</span></span> <span data-ttu-id="e50e3-141">O exemplo supõe que pISCardCmd é um ponteiro válido para uma instância da interface [**ISCardCmd**](iscardcmd.md) e que pIByteRequest é um ponteiro válido para uma instância da interface [**IByteBuffer**](ibytebuffer.md) inicializada com uma chamada anterior para o método [**IByteBuffer:: Initialize**](ibytebuffer-initialize.md) .</span><span class="sxs-lookup"><span data-stu-id="e50e3-141">The example assumes that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface and that pIByteRequest is a valid pointer to an instance of the [**IByteBuffer**](ibytebuffer.md) interface initialized with a previous call to the [**IByteBuffer::Initialize**](ibytebuffer-initialize.md) method.</span></span>


```C++
LONG       lLe = 0;
HRESULT    hr;

hr = pISCardCmd->BuildCmd(0x00,   // Some cards prefer 0xC0
                          0xa4,   // 'Select File'
                          0x00,
                          0x00,
                          pIByteRequest,
                          &lLe);
if (FAILED(hr))
{
    printf("Failed ISCardCmd::BuildCmd\n");
    // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="e50e3-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e50e3-142">Requirements</span></span>



| <span data-ttu-id="e50e3-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="e50e3-143">Requirement</span></span> | <span data-ttu-id="e50e3-144">Valor</span><span class="sxs-lookup"><span data-stu-id="e50e3-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e50e3-145">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e50e3-145">Minimum supported client</span></span><br/> | <span data-ttu-id="e50e3-146">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="e50e3-146">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="e50e3-147">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e50e3-147">Minimum supported server</span></span><br/> | <span data-ttu-id="e50e3-148">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e50e3-148">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e50e3-149">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="e50e3-149">End of client support</span></span><br/>    | <span data-ttu-id="e50e3-150">Windows XP</span><span class="sxs-lookup"><span data-stu-id="e50e3-150">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="e50e3-151">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="e50e3-151">End of server support</span></span><br/>    | <span data-ttu-id="e50e3-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e50e3-152">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="e50e3-153">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e50e3-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="e50e3-154"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="e50e3-154"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="e50e3-155">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="e50e3-155">Type library</span></span><br/>             | <dl> <span data-ttu-id="e50e3-156"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="e50e3-156"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="e50e3-157">DLL</span><span class="sxs-lookup"><span data-stu-id="e50e3-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e50e3-158"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e50e3-158"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="e50e3-159">IID</span><span class="sxs-lookup"><span data-stu-id="e50e3-159">IID</span></span><br/>                      | <span data-ttu-id="e50e3-160">IID \_ ISCardCmd é definido como D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="e50e3-160">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="e50e3-161">Confira também</span><span class="sxs-lookup"><span data-stu-id="e50e3-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e50e3-162">**Encapsular**</span><span class="sxs-lookup"><span data-stu-id="e50e3-162">**Encapsulate**</span></span>](iscardcmd-encapsulate.md)
</dt> <dt>

[<span data-ttu-id="e50e3-163">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="e50e3-163">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> </dl>

 

 
