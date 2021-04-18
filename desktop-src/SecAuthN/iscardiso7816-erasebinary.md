---
description: Constrói um comando APDU (unidade de dados de protocolo de aplicativo) que define seqüencialmente parte do conteúdo de um arquivo elementar para seu estado de apagamento lógico, começando a partir de um determinado deslocamento.
ms.assetid: 89e2371e-e27d-475b-9427-bbf6d614c473
title: 'Método ISCardISO7816:: EraseBinary (Scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.EraseBinary
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: a9bad21bbb35b7ac16209ac0075267ef7300fe21
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105752014"
---
# <a name="iscardiso7816erasebinary-method"></a><span data-ttu-id="86b42-103">Método ISCardISO7816:: EraseBinary</span><span class="sxs-lookup"><span data-stu-id="86b42-103">ISCardISO7816::EraseBinary method</span></span>

<span data-ttu-id="86b42-104">\[O método **EraseBinary** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="86b42-104">\[The **EraseBinary** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="86b42-105">Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="86b42-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="86b42-106">Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="86b42-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="86b42-107">O método **EraseBinary** constrói um comando APDU ( [*unidade de dados de protocolo de aplicativo*](../secgloss/a-gly.md) ) que define seqüencialmente parte do conteúdo de um arquivo elementar para seu estado lógico apagado, começando a partir de um determinado deslocamento.</span><span class="sxs-lookup"><span data-stu-id="86b42-107">The **EraseBinary** method constructs an [*application protocol data unit*](../secgloss/a-gly.md) (APDU) command that sequentially sets part of the content of an elementary file to its logical erased state, starting from a given offset.</span></span>

## <a name="syntax"></a><span data-ttu-id="86b42-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="86b42-108">Syntax</span></span>


```C++
HRESULT EraseBinary(
  [in]      BYTE         byP1,
  [in]      BYTE         byP2,
  [in]      LPBYTEBUFFER pData,
  [in, out] LPSCARDCMD   *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="86b42-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="86b42-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86b42-110">*byP1* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="86b42-110">*byP1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86b42-111">Posição de RFU.</span><span class="sxs-lookup"><span data-stu-id="86b42-111">RFU position.</span></span>

<span data-ttu-id="86b42-112">Se B8 = 1 em P1, a B7 e a B6 de P1 são definidas como zero (RFU bits), B5 a B1 de P1 são um identificador curto de EF e P2 é o deslocamento do primeiro byte a ser apagado (em unidades de dados) desde o início do arquivo.</span><span class="sxs-lookup"><span data-stu-id="86b42-112">If b8=1 in P1, then b7 and b6 of P1 are set to zero (RFU bits), b5 to b1 of P1 are a short EF identifier and P2 is the offset of the first byte to be erased (in data units) from the beginning of the file.</span></span>

<span data-ttu-id="86b42-113">Se B8 = 0 em P1, P1 \| \| P2 será o deslocamento do primeiro byte a ser apagado (em unidades de dados) desde o início do arquivo.</span><span class="sxs-lookup"><span data-stu-id="86b42-113">If b8=0 in P1, then P1 \|\| P2 is the offset of the first byte to be erased (in data units) from the beginning of the file.</span></span>

<span data-ttu-id="86b42-114">Se o campo de dados estiver presente, ele codifica o deslocamento da primeira unidade de dados para não ser apagado.</span><span class="sxs-lookup"><span data-stu-id="86b42-114">If the data field is present, it codes the offset of the first data unit not to be erased.</span></span> <span data-ttu-id="86b42-115">Esse deslocamento deve ser maior do que aquele codificado no P1-P2.</span><span class="sxs-lookup"><span data-stu-id="86b42-115">This offset shall be higher than the one coded in P1-P2.</span></span> <span data-ttu-id="86b42-116">Quando o campo de dados estiver vazio, o comando será apagado até o final do arquivo.</span><span class="sxs-lookup"><span data-stu-id="86b42-116">When the data field is empty, the command erases up to the end of the file.</span></span>

</dd> <dt>

<span data-ttu-id="86b42-117">*byP2* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="86b42-117">*byP2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86b42-118">Posição de RFU.</span><span class="sxs-lookup"><span data-stu-id="86b42-118">RFU position.</span></span>

<span data-ttu-id="86b42-119">Se B8 = 1 em P1, a B7 e a B6 de P1 são definidas como zero (RFU bits), B5 a B1 de P1 são um identificador curto de EF e P2 é o deslocamento do primeiro byte a ser apagado (em unidades de dados) desde o início do arquivo.</span><span class="sxs-lookup"><span data-stu-id="86b42-119">If b8=1 in P1, then b7 and b6 of P1 are set to zero (RFU bits), b5 to b1 of P1 are a short EF identifier and P2 is the offset of the first byte to be erased (in data units) from the beginning of the file.</span></span>

<span data-ttu-id="86b42-120">Se B8 = 0 em P1, P1 \| \| P2 será o deslocamento do primeiro byte a ser apagado (em unidades de dados) desde o início do arquivo.</span><span class="sxs-lookup"><span data-stu-id="86b42-120">If b8=0 in P1, then P1 \|\| P2 is the offset of the first byte to be erased (in data units) from the beginning of the file.</span></span>

<span data-ttu-id="86b42-121">Se o campo de dados estiver presente, ele codifica o deslocamento da primeira unidade de dados para não ser apagado.</span><span class="sxs-lookup"><span data-stu-id="86b42-121">If the data field is present, it codes the offset of the first data unit not to be erased.</span></span> <span data-ttu-id="86b42-122">Esse deslocamento deve ser maior do que aquele codificado no P1-P2.</span><span class="sxs-lookup"><span data-stu-id="86b42-122">This offset shall be higher than the one coded in P1-P2.</span></span> <span data-ttu-id="86b42-123">Quando o campo de dados estiver vazio, o comando será apagado até o final do arquivo.</span><span class="sxs-lookup"><span data-stu-id="86b42-123">When the data field is empty, the command erases up to the end of the file.</span></span>

</dd> <dt>

<span data-ttu-id="86b42-124">*pData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="86b42-124">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86b42-125">Um ponteiro para os dados que especificam o intervalo de apagamento.</span><span class="sxs-lookup"><span data-stu-id="86b42-125">A pointer to the data that specifies the erase range.</span></span> <span data-ttu-id="86b42-126">Esse parâmetro pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="86b42-126">This parameter may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="86b42-127">*ppCmd* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="86b42-127">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="86b42-128">Na entrada, um ponteiro para um objeto de interface [**ISCardCmd**](iscardcmd.md) ou **nulo**.</span><span class="sxs-lookup"><span data-stu-id="86b42-128">On input, a pointer to an [**ISCardCmd**](iscardcmd.md) interface object or **NULL**.</span></span>

<span data-ttu-id="86b42-129">No retorno, ele é preenchido com o comando APDU construído por essa operação.</span><span class="sxs-lookup"><span data-stu-id="86b42-129">On return, it is filled with the APDU command constructed by this operation.</span></span> <span data-ttu-id="86b42-130">Se *ppCmd* foi definido como **NULL**, um objeto [**ISCardCmd**](iscardcmd.md) de [*cartão inteligente*](../secgloss/s-gly.md) será criado internamente e retornado usando o ponteiro *ppCmd* .</span><span class="sxs-lookup"><span data-stu-id="86b42-130">If *ppCmd* was set to **NULL**, a [*smart card*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) object is internally created and returned by using the *ppCmd* pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86b42-131">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="86b42-131">Return value</span></span>

<span data-ttu-id="86b42-132">O método retorna um dos seguintes valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="86b42-132">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="86b42-133">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="86b42-133">Return code</span></span>                                                                                   | <span data-ttu-id="86b42-134">Descrição</span><span class="sxs-lookup"><span data-stu-id="86b42-134">Description</span></span>                                          |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="86b42-135"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="86b42-135"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="86b42-136">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="86b42-136">The operation completed successfully.</span></span><br/>     |
| <dl> <span data-ttu-id="86b42-137"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="86b42-137"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="86b42-138">Um parâmetro inválido foi passado.</span><span class="sxs-lookup"><span data-stu-id="86b42-138">A parameter that is not valid was passed.</span></span><br/> |
| <dl> <span data-ttu-id="86b42-139"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="86b42-139"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="86b42-140">Um ponteiro inadequado foi passado.</span><span class="sxs-lookup"><span data-stu-id="86b42-140">A bad pointer was passed in.</span></span><br/>              |
| <dl> <span data-ttu-id="86b42-141"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="86b42-141"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="86b42-142">Sem memória.</span><span class="sxs-lookup"><span data-stu-id="86b42-142">Out of memory.</span></span><br/>                            |



 

## <a name="remarks"></a><span data-ttu-id="86b42-143">Comentários</span><span class="sxs-lookup"><span data-stu-id="86b42-143">Remarks</span></span>

<span data-ttu-id="86b42-144">O comando encapsulado só poderá ser executado se o status de segurança do [*cartão inteligente*](../secgloss/s-gly.md) satisfizer os atributos de segurança do arquivo elementar que está sendo processado.</span><span class="sxs-lookup"><span data-stu-id="86b42-144">The encapsulated command can only be performed if the security status of the [*smart card*](../secgloss/s-gly.md) satisfies the security attributes of the elementary file being processed.</span></span>

<span data-ttu-id="86b42-145">Quando o comando contém um identificador elementar curto válido, ele define o arquivo como o arquivo elementar atual.</span><span class="sxs-lookup"><span data-stu-id="86b42-145">When the command contains a valid short elementary identifier, it sets the file as current elementary file.</span></span>

<span data-ttu-id="86b42-146">Arquivos elementares sem uma estrutura transparente não podem ser apagados.</span><span class="sxs-lookup"><span data-stu-id="86b42-146">Elementary files without a transparent structure cannot be erased.</span></span> <span data-ttu-id="86b42-147">O comando encapsulado aborta se aplicado a um arquivo elementar sem uma estrutura transparente.</span><span class="sxs-lookup"><span data-stu-id="86b42-147">The encapsulated command aborts if applied to an elementary file without a transparent structure.</span></span>

<span data-ttu-id="86b42-148">Para obter uma lista de todos os métodos fornecidos por essa interface, consulte [**ISCardISO7816**](iscardiso7816.md).</span><span class="sxs-lookup"><span data-stu-id="86b42-148">For a list of all the methods provided by this interface, see [**ISCardISO7816**](iscardiso7816.md).</span></span>

<span data-ttu-id="86b42-149">Além dos códigos de erro COM listados acima, essa interface pode retornar um código de erro de cartão inteligente se uma função de cartão inteligente foi chamada para concluir a solicitação.</span><span class="sxs-lookup"><span data-stu-id="86b42-149">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="86b42-150">Para obter mais informações, consulte [valores de retorno de cartão inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="86b42-150">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="86b42-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="86b42-151">Requirements</span></span>



| <span data-ttu-id="86b42-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="86b42-152">Requirement</span></span> | <span data-ttu-id="86b42-153">Valor</span><span class="sxs-lookup"><span data-stu-id="86b42-153">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="86b42-154">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="86b42-154">Minimum supported client</span></span><br/> | <span data-ttu-id="86b42-155">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="86b42-155">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="86b42-156">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="86b42-156">Minimum supported server</span></span><br/> | <span data-ttu-id="86b42-157">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="86b42-157">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="86b42-158">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="86b42-158">End of client support</span></span><br/>    | <span data-ttu-id="86b42-159">Windows XP</span><span class="sxs-lookup"><span data-stu-id="86b42-159">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="86b42-160">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="86b42-160">End of server support</span></span><br/>    | <span data-ttu-id="86b42-161">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="86b42-161">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="86b42-162">parâmetro</span><span class="sxs-lookup"><span data-stu-id="86b42-162">Header</span></span><br/>                   | <dl> <span data-ttu-id="86b42-163"><dt>Scardssp. h</dt></span><span class="sxs-lookup"><span data-stu-id="86b42-163"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="86b42-164">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="86b42-164">Type library</span></span><br/>             | <dl> <span data-ttu-id="86b42-165"><dt>Scardsrv. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="86b42-165"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="86b42-166">DLL</span><span class="sxs-lookup"><span data-stu-id="86b42-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="86b42-167"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="86b42-167"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="86b42-168">IID</span><span class="sxs-lookup"><span data-stu-id="86b42-168">IID</span></span><br/>                      | <span data-ttu-id="86b42-169">IID \_ ISCardISO7816 é definido como 53B6AA68-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="86b42-169">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="86b42-170">Confira também</span><span class="sxs-lookup"><span data-stu-id="86b42-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86b42-171">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="86b42-171">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> <dt>

[<span data-ttu-id="86b42-172">**ReadBinary**</span><span class="sxs-lookup"><span data-stu-id="86b42-172">**ReadBinary**</span></span>](iscardiso7816-readbinary.md)
</dt> <dt>

[<span data-ttu-id="86b42-173">**UpdateBinary**</span><span class="sxs-lookup"><span data-stu-id="86b42-173">**UpdateBinary**</span></span>](iscardiso7816-updatebinary.md)
</dt> <dt>

[<span data-ttu-id="86b42-174">**WriteBinary**</span><span class="sxs-lookup"><span data-stu-id="86b42-174">**WriteBinary**</span></span>](iscardiso7816-writebinary.md)
</dt> </dl>

 

 
