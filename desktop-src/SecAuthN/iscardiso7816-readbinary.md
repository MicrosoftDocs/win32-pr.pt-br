---
description: O método ReadBinary constrói um comando APDU (unidade de dados de protocolo de aplicativo) que adquire uma mensagem de resposta que fornece a parte do conteúdo de um arquivo elementar de forma transparente.
ms.assetid: 15394c21-1e07-4ea1-8f11-817e07b31f9b
title: 'Método ISCardISO7816:: ReadBinary (Scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.ReadBinary
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: a29093d8725a3390df9837f4e2f395cfcf2eef29
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829753"
---
# <a name="iscardiso7816readbinary-method"></a><span data-ttu-id="60cb5-103">Método ISCardISO7816:: ReadBinary</span><span class="sxs-lookup"><span data-stu-id="60cb5-103">ISCardISO7816::ReadBinary method</span></span>

<span data-ttu-id="60cb5-104">\[O método **ReadBinary** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="60cb5-104">\[The **ReadBinary** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="60cb5-105">Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="60cb5-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="60cb5-106">Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="60cb5-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="60cb5-107">O método **ReadBinary** constrói um comando APDU ( [*unidade de dados de protocolo de aplicativo*](../secgloss/a-gly.md) ) que adquire uma mensagem de resposta que fornece a parte do conteúdo de um arquivo elementar de forma transparente.</span><span class="sxs-lookup"><span data-stu-id="60cb5-107">The **ReadBinary** method constructs an [*application protocol data unit*](../secgloss/a-gly.md) (APDU) command that acquires a response message that gives that part of the contents of a transparent-structured elementary file.</span></span>

## <a name="syntax"></a><span data-ttu-id="60cb5-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="60cb5-108">Syntax</span></span>


```C++
HRESULT ReadBinary(
  [in]      BYTE       byP1,
  [in]      BYTE       byP2,
  [in]      LONG       lBytesToRead,
  [in, out] LPSCARDCMD *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="60cb5-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="60cb5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60cb5-110">*byP1* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="60cb5-110">*byP1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60cb5-111">O campo P1-P2, deslocamento para o primeiro byte a ser lido desde o início do arquivo.</span><span class="sxs-lookup"><span data-stu-id="60cb5-111">The P1-P2 field, offset to the first byte to be read from the beginning of the file.</span></span> <span data-ttu-id="60cb5-112">Se B8 = 1 em P1, a B7 e a B6 de P1 são definidas como zero (RFU bits), B5 a B1 de P1 são um identificador curto de EF e P2 é o deslocamento do primeiro byte a ser lido em unidades de dados do início do arquivo.</span><span class="sxs-lookup"><span data-stu-id="60cb5-112">If b8=1 in P1, then b7 and b6 of P1 are set to zero (RFU bits), b5 to b1 of P1 are a short EF identifier and P2 is the offset of the first byte to be read in data units from the beginning of the file.</span></span> <span data-ttu-id="60cb5-113">Se B8 = 0 em P1, P1 \| \| P2 será o deslocamento do primeiro byte a ser lido em unidades de dados do início do arquivo.</span><span class="sxs-lookup"><span data-stu-id="60cb5-113">If b8=0 in P1, then P1\|\|P2 is the offset of the first byte to be read in data units from the beginning of the file.</span></span>

</dd> <dt>

<span data-ttu-id="60cb5-114">*byP2* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="60cb5-114">*byP2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60cb5-115">O campo P1-P2, deslocamento para o primeiro byte a ser lido desde o início do arquivo.</span><span class="sxs-lookup"><span data-stu-id="60cb5-115">The P1-P2 field, offset to the first byte to be read from the beginning of the file.</span></span> <span data-ttu-id="60cb5-116">Se B8 = 1 em P1, a B7 e a B6 de P1 são definidas como zero (RFU bits), B5 a B1 de P1 são um identificador curto de EF e P2 é o deslocamento do primeiro byte a ser lido em unidades de dados do início do arquivo.</span><span class="sxs-lookup"><span data-stu-id="60cb5-116">If b8=1 in P1, then b7 and b6 of P1 are set to zero (RFU bits), b5 to b1 of P1 are a short EF identifier and P2 is the offset of the first byte to be read in data units from the beginning of the file.</span></span> <span data-ttu-id="60cb5-117">Se B8 = 0 em P1, P1 \| \| P2 será o deslocamento do primeiro byte a ser lido em unidades de dados do início do arquivo.</span><span class="sxs-lookup"><span data-stu-id="60cb5-117">If b8=0 in P1, then P1\|\|P2 is the offset of the first byte to be read in data units from the beginning of the file.</span></span>

</dd> <dt>

<span data-ttu-id="60cb5-118">*lBytesToRead* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="60cb5-118">*lBytesToRead* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60cb5-119">Número de bytes a serem lidos do EF transparente.</span><span class="sxs-lookup"><span data-stu-id="60cb5-119">Number of bytes to read from the transparent EF.</span></span>

<span data-ttu-id="60cb5-120">Se o campo Le contiver apenas zeros, dentro do limite de 256 por comprimento curto ou 65536 para comprimento estendido, todos os bytes até o final do arquivo devem ser lidos.</span><span class="sxs-lookup"><span data-stu-id="60cb5-120">If the Le field contains only zeros, then within the limit of 256 for short length or 65536 for extended length, all the bytes until the end of the file should be read.</span></span>

</dd> <dt>

<span data-ttu-id="60cb5-121">*ppCmd* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="60cb5-121">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="60cb5-122">Na entrada, um ponteiro para um objeto de interface [**ISCardCmd**](iscardcmd.md) ou **nulo**.</span><span class="sxs-lookup"><span data-stu-id="60cb5-122">On input, a pointer to an [**ISCardCmd**](iscardcmd.md) interface object or **NULL**.</span></span>

<span data-ttu-id="60cb5-123">No retorno, ele é preenchido com o comando APDU construído por essa operação.</span><span class="sxs-lookup"><span data-stu-id="60cb5-123">On return, it is filled with the APDU command constructed by this operation.</span></span> <span data-ttu-id="60cb5-124">Se *ppCmd* foi definido como **NULL**, um objeto [**ISCardCmd**](iscardcmd.md) de [*cartão inteligente*](../secgloss/s-gly.md) será criado internamente e retornado usando o ponteiro *ppCmd* .</span><span class="sxs-lookup"><span data-stu-id="60cb5-124">If *ppCmd* was set to **NULL**, a [*smart card*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) object is internally created and returned using the *ppCmd* pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60cb5-125">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="60cb5-125">Return value</span></span>

<span data-ttu-id="60cb5-126">O método retorna um dos seguintes valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="60cb5-126">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="60cb5-127">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="60cb5-127">Return code</span></span>                                                                                   | <span data-ttu-id="60cb5-128">Descrição</span><span class="sxs-lookup"><span data-stu-id="60cb5-128">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="60cb5-129"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="60cb5-129"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="60cb5-130">Operação concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="60cb5-130">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="60cb5-131"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="60cb5-131"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="60cb5-132">Parâmetro inválido.</span><span class="sxs-lookup"><span data-stu-id="60cb5-132">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="60cb5-133"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="60cb5-133"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="60cb5-134">Um ponteiro inadequado foi passado.</span><span class="sxs-lookup"><span data-stu-id="60cb5-134">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="60cb5-135"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="60cb5-135"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="60cb5-136">Sem memória.</span><span class="sxs-lookup"><span data-stu-id="60cb5-136">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="60cb5-137">Comentários</span><span class="sxs-lookup"><span data-stu-id="60cb5-137">Remarks</span></span>

<span data-ttu-id="60cb5-138">O comando encapsulado só poderá ser executado se o status de segurança do [*cartão inteligente*](../secgloss/s-gly.md) satisfizer os atributos de segurança do arquivo elementar que está sendo processado.</span><span class="sxs-lookup"><span data-stu-id="60cb5-138">The encapsulated command can only be performed if the security status of the [*smart card*](../secgloss/s-gly.md) satisfies the security attributes of the elementary file being processed.</span></span>

<span data-ttu-id="60cb5-139">Quando o comando contém um identificador elementar curto válido, ele define o arquivo como o arquivo elementar atual.</span><span class="sxs-lookup"><span data-stu-id="60cb5-139">When the command contains a valid short elementary identifier, it sets the file as current elementary file.</span></span>

<span data-ttu-id="60cb5-140">Arquivos elementares sem uma estrutura transparente não podem ser apagados.</span><span class="sxs-lookup"><span data-stu-id="60cb5-140">Elementary files without a transparent structure cannot be erased.</span></span> <span data-ttu-id="60cb5-141">O comando encapsulado aborta se aplicado a um arquivo elementar sem uma estrutura transparente.</span><span class="sxs-lookup"><span data-stu-id="60cb5-141">The encapsulated command aborts if applied to an elementary file without a transparent structure.</span></span>

<span data-ttu-id="60cb5-142">Para obter uma lista de todos os métodos fornecidos por essa interface, consulte [**ISCardISO7816**](iscardiso7816.md).</span><span class="sxs-lookup"><span data-stu-id="60cb5-142">For a list of all the methods provided by this interface, see [**ISCardISO7816**](iscardiso7816.md).</span></span>

<span data-ttu-id="60cb5-143">Além dos códigos de erro COM listados acima, essa interface pode retornar um código de erro de cartão inteligente se uma função de cartão inteligente foi chamada para concluir a solicitação.</span><span class="sxs-lookup"><span data-stu-id="60cb5-143">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="60cb5-144">Para obter mais informações, consulte [valores de retorno de cartão inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="60cb5-144">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="60cb5-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="60cb5-145">Requirements</span></span>



| <span data-ttu-id="60cb5-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="60cb5-146">Requirement</span></span> | <span data-ttu-id="60cb5-147">Valor</span><span class="sxs-lookup"><span data-stu-id="60cb5-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="60cb5-148">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="60cb5-148">Minimum supported client</span></span><br/> | <span data-ttu-id="60cb5-149">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="60cb5-149">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="60cb5-150">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="60cb5-150">Minimum supported server</span></span><br/> | <span data-ttu-id="60cb5-151">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="60cb5-151">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="60cb5-152">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="60cb5-152">End of client support</span></span><br/>    | <span data-ttu-id="60cb5-153">Windows XP</span><span class="sxs-lookup"><span data-stu-id="60cb5-153">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="60cb5-154">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="60cb5-154">End of server support</span></span><br/>    | <span data-ttu-id="60cb5-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="60cb5-155">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="60cb5-156">parâmetro</span><span class="sxs-lookup"><span data-stu-id="60cb5-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="60cb5-157"><dt>Scardssp. h</dt></span><span class="sxs-lookup"><span data-stu-id="60cb5-157"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="60cb5-158">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="60cb5-158">Type library</span></span><br/>             | <dl> <span data-ttu-id="60cb5-159"><dt>Scardsrv. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="60cb5-159"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="60cb5-160">DLL</span><span class="sxs-lookup"><span data-stu-id="60cb5-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="60cb5-161"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="60cb5-161"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="60cb5-162">IID</span><span class="sxs-lookup"><span data-stu-id="60cb5-162">IID</span></span><br/>                      | <span data-ttu-id="60cb5-163">IID \_ ISCardISO7816 é definido como 53B6AA68-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="60cb5-163">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="60cb5-164">Confira também</span><span class="sxs-lookup"><span data-stu-id="60cb5-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60cb5-165">**EraseBinary**</span><span class="sxs-lookup"><span data-stu-id="60cb5-165">**EraseBinary**</span></span>](iscardiso7816-erasebinary.md)
</dt> <dt>

[<span data-ttu-id="60cb5-166">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="60cb5-166">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> <dt>

[<span data-ttu-id="60cb5-167">**UpdateBinary**</span><span class="sxs-lookup"><span data-stu-id="60cb5-167">**UpdateBinary**</span></span>](iscardiso7816-updatebinary.md)
</dt> <dt>

[<span data-ttu-id="60cb5-168">**WriteBinary**</span><span class="sxs-lookup"><span data-stu-id="60cb5-168">**WriteBinary**</span></span>](iscardiso7816-writebinary.md)
</dt> </dl>

 

 
