---
description: O método WriteBinary constrói um comando APDU (unidade de dados de protocolo de aplicativo) que grava valores binários em um arquivo elementar.
ms.assetid: e38273d5-4eb0-4c0b-829a-c78e511a38bc
title: 'Método ISCardISO7816:: WriteBinary (Scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.WriteBinary
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 330e817bc501c451026589087991fb43c0b5ac57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920682"
---
# <a name="iscardiso7816writebinary-method"></a><span data-ttu-id="3ae62-103">Método ISCardISO7816:: WriteBinary</span><span class="sxs-lookup"><span data-stu-id="3ae62-103">ISCardISO7816::WriteBinary method</span></span>

<span data-ttu-id="3ae62-104">\[O método **WriteBinary** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="3ae62-104">\[The **WriteBinary** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="3ae62-105">Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="3ae62-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="3ae62-106">Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="3ae62-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="3ae62-107">O método **WriteBinary** constrói um comando APDU ( [*unidade de dados de protocolo de aplicativo*](../secgloss/a-gly.md) ) que grava valores binários em um arquivo elementar.</span><span class="sxs-lookup"><span data-stu-id="3ae62-107">The **WriteBinary** method constructs an [*application protocol data unit*](../secgloss/a-gly.md) (APDU) command that writes binary values into an elementary file.</span></span>

<span data-ttu-id="3ae62-108">Dependendo dos atributos do arquivo, o comando executa uma das seguintes operações:</span><span class="sxs-lookup"><span data-stu-id="3ae62-108">Depending upon the file attributes, the command performs one of the following operations:</span></span>

-   <span data-ttu-id="3ae62-109">A lógica ou os bits já presentes no cartão com os bits fornecidos no comando APDU (o estado de apagamento lógico dos bits do arquivo é 0).</span><span class="sxs-lookup"><span data-stu-id="3ae62-109">The logical OR of the bits already present in the card with the bits given in the command APDU (logical erased state of the bits of the file is 0).</span></span>
-   <span data-ttu-id="3ae62-110">A lógica e o dos bits já estão presentes no cartão com os bits fornecidos no comando APDU (o estado de apagamento lógico dos bits do arquivo é 1).</span><span class="sxs-lookup"><span data-stu-id="3ae62-110">The logical AND of the bits already present in the card with the bits given in the command APDU (logical erased state of the bits of the file is 1).</span></span>
-   <span data-ttu-id="3ae62-111">A gravação única no cartão dos bits fornecidos no comando APDU.</span><span class="sxs-lookup"><span data-stu-id="3ae62-111">The one-time write in the card of the bits given in the command APDU.</span></span>

<span data-ttu-id="3ae62-112">Quando nenhuma indicação é fornecida no byte de codificação de dados, a lógica ou o comportamento se aplica.</span><span class="sxs-lookup"><span data-stu-id="3ae62-112">When no indication is given in the data coding byte, the logical OR behavior applies.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ae62-113">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3ae62-113">Syntax</span></span>


```C++
HRESULT WriteBinary(
  [in]      BYTE         byP1,
  [in]      BYTE         byP2,
  [in]      LPBYTEBUFFER pData,
  [in, out] LPSCARDCMD   *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="3ae62-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3ae62-114">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ae62-115">*byP1* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3ae62-115">*byP1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ae62-116">Offset para o local de gravação desde o início do arquivo binário (EF).</span><span class="sxs-lookup"><span data-stu-id="3ae62-116">Offset to the write location from the beginning of the binary file (EF).</span></span> <span data-ttu-id="3ae62-117">Se B8 = 1 em P1, a B7 e a B6 de P1 são definidas como zero (RFU bits), B5 a B1 de P1 são um identificador curto de EF e P2 é o deslocamento do primeiro byte a ser gravado em unidades de dados do início do arquivo.</span><span class="sxs-lookup"><span data-stu-id="3ae62-117">If b8=1 in P1, then b7 and b6 of P1 are set to zero (RFU bits), b5 to b1 of P1 are a short EF identifier and P2 is the offset of the first byte to be written in data units from the beginning of the file.</span></span> <span data-ttu-id="3ae62-118">Se B8 = 0 em P1, P1 \| \| P2 será o deslocamento do primeiro byte a ser gravado em unidades de dados desde o início do arquivo.</span><span class="sxs-lookup"><span data-stu-id="3ae62-118">If b8=0 in P1, then P1\|\|P2 is the offset of the first byte to be written in data units from the beginning of the file.</span></span>

</dd> <dt>

<span data-ttu-id="3ae62-119">*byP2* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3ae62-119">*byP2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ae62-120">Offset para o local de gravação desde o início do arquivo binário (EF).</span><span class="sxs-lookup"><span data-stu-id="3ae62-120">Offset to the write location from the beginning of the binary file (EF).</span></span> <span data-ttu-id="3ae62-121">Se B8 = 1 em P1, a B7 e a B6 de P1 são definidas como zero (RFU bits), B5 a B1 de P1 são um identificador curto de EF e P2 é o deslocamento do primeiro byte a ser gravado em unidades de dados do início do arquivo.</span><span class="sxs-lookup"><span data-stu-id="3ae62-121">If b8=1 in P1, then b7 and b6 of P1 are set to zero (RFU bits), b5 to b1 of P1 are a short EF identifier and P2 is the offset of the first byte to be written in data units from the beginning of the file.</span></span> <span data-ttu-id="3ae62-122">Se B8 = 0 em P1, P1 \| \| P2 será o deslocamento do primeiro byte a ser gravado em unidades de dados desde o início do arquivo.</span><span class="sxs-lookup"><span data-stu-id="3ae62-122">If b8=0 in P1, then P1\|\|P2 is the offset of the first byte to be written in data units from the beginning of the file.</span></span>

</dd> <dt>

<span data-ttu-id="3ae62-123">*pData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3ae62-123">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ae62-124">Ponteiro para a cadeia de caracteres das unidades de dados a serem gravadas.</span><span class="sxs-lookup"><span data-stu-id="3ae62-124">Pointer to the string of data units to be written.</span></span>

</dd> <dt>

<span data-ttu-id="3ae62-125">*ppCmd* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="3ae62-125">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="3ae62-126">Na entrada, um ponteiro para um objeto de interface [**ISCardCmd**](iscardcmd.md) ou **nulo**.</span><span class="sxs-lookup"><span data-stu-id="3ae62-126">On input, a pointer to an [**ISCardCmd**](iscardcmd.md) interface object or **NULL**.</span></span>

<span data-ttu-id="3ae62-127">No retorno, ele é preenchido com o comando APDU construído por essa operação.</span><span class="sxs-lookup"><span data-stu-id="3ae62-127">On return, it is filled with the APDU command constructed by this operation.</span></span> <span data-ttu-id="3ae62-128">Se *ppCmd* foi definido como **NULL**, um objeto [**ISCardCmd**](iscardcmd.md) de [*cartão inteligente*](../secgloss/s-gly.md) será criado internamente e retornado por meio do ponteiro *ppCmd* .</span><span class="sxs-lookup"><span data-stu-id="3ae62-128">If *ppCmd* was set to **NULL**, a [*smart card*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) object is internally created and returned via the *ppCmd* pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3ae62-129">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3ae62-129">Return value</span></span>

<span data-ttu-id="3ae62-130">O método retorna um dos seguintes valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="3ae62-130">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="3ae62-131">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="3ae62-131">Return code</span></span>                                                                                   | <span data-ttu-id="3ae62-132">Descrição</span><span class="sxs-lookup"><span data-stu-id="3ae62-132">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="3ae62-133"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="3ae62-133"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="3ae62-134">Operação concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="3ae62-134">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="3ae62-135"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="3ae62-135"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="3ae62-136">Parâmetro inválido.</span><span class="sxs-lookup"><span data-stu-id="3ae62-136">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="3ae62-137"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="3ae62-137"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="3ae62-138">Um ponteiro inadequado foi passado.</span><span class="sxs-lookup"><span data-stu-id="3ae62-138">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="3ae62-139"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="3ae62-139"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="3ae62-140">Sem memória.</span><span class="sxs-lookup"><span data-stu-id="3ae62-140">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="3ae62-141">Comentários</span><span class="sxs-lookup"><span data-stu-id="3ae62-141">Remarks</span></span>

<span data-ttu-id="3ae62-142">O comando encapsulado só poderá ser executado se o status de segurança do [*cartão inteligente*](../secgloss/s-gly.md) satisfizer os atributos de segurança do arquivo elementar que está sendo processado.</span><span class="sxs-lookup"><span data-stu-id="3ae62-142">The encapsulated command can only be performed if the security status of the [*smart card*](../secgloss/s-gly.md) satisfies the security attributes of the elementary file being processed.</span></span>

<span data-ttu-id="3ae62-143">Quando o comando contém um identificador elementar curto válido, ele define o arquivo como o arquivo elementar atual.</span><span class="sxs-lookup"><span data-stu-id="3ae62-143">When the command contains a valid short elementary identifier, it sets the file as current elementary file.</span></span>

<span data-ttu-id="3ae62-144">Quando uma operação de gravação binária tiver sido aplicada a uma unidade de dados de um EF de gravação única, qualquer outra operação de gravação referente a essa unidade de dados será anulada se o conteúdo da unidade de dados ou o indicador de estado de apagamento lógico (se houver) anexado a essa unidade de dados for diferente do estado de apagamento lógico.</span><span class="sxs-lookup"><span data-stu-id="3ae62-144">When a write binary operation has been applied to a data unit of a one-time write EF, any further write operation referring to this data unit will be aborted if the content of the data unit or the logical erased state indicator (if any) attached to this data unit is different from the logical erased state.</span></span>

<span data-ttu-id="3ae62-145">Os arquivos elementares sem uma estrutura transparente não podem ser gravados.</span><span class="sxs-lookup"><span data-stu-id="3ae62-145">Elementary files without a transparent structure cannot be written to.</span></span> <span data-ttu-id="3ae62-146">O comando encapsulado aborta se aplicado a um arquivo elementar sem uma estrutura transparente.</span><span class="sxs-lookup"><span data-stu-id="3ae62-146">The encapsulated command aborts if applied to an elementary file without a transparent structure.</span></span>

<span data-ttu-id="3ae62-147">Para obter uma lista de todos os métodos fornecidos por essa interface, consulte [**ISCardISO7816**](iscardiso7816.md).</span><span class="sxs-lookup"><span data-stu-id="3ae62-147">For a list of all the methods provided by this interface, see [**ISCardISO7816**](iscardiso7816.md).</span></span>

<span data-ttu-id="3ae62-148">Além dos códigos de erro COM listados acima, essa interface pode retornar um código de erro de cartão inteligente se uma função de cartão inteligente foi chamada para concluir a solicitação.</span><span class="sxs-lookup"><span data-stu-id="3ae62-148">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="3ae62-149">Para obter mais informações, consulte [valores de retorno de cartão inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="3ae62-149">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3ae62-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3ae62-150">Requirements</span></span>



| <span data-ttu-id="3ae62-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="3ae62-151">Requirement</span></span> | <span data-ttu-id="3ae62-152">Valor</span><span class="sxs-lookup"><span data-stu-id="3ae62-152">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3ae62-153">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3ae62-153">Minimum supported client</span></span><br/> | <span data-ttu-id="3ae62-154">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="3ae62-154">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="3ae62-155">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3ae62-155">Minimum supported server</span></span><br/> | <span data-ttu-id="3ae62-156">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3ae62-156">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3ae62-157">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="3ae62-157">End of client support</span></span><br/>    | <span data-ttu-id="3ae62-158">Windows XP</span><span class="sxs-lookup"><span data-stu-id="3ae62-158">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="3ae62-159">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="3ae62-159">End of server support</span></span><br/>    | <span data-ttu-id="3ae62-160">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="3ae62-160">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="3ae62-161">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3ae62-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="3ae62-162"><dt>Scardssp. h</dt></span><span class="sxs-lookup"><span data-stu-id="3ae62-162"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="3ae62-163">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="3ae62-163">Type library</span></span><br/>             | <dl> <span data-ttu-id="3ae62-164"><dt>Scardsrv. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="3ae62-164"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="3ae62-165">DLL</span><span class="sxs-lookup"><span data-stu-id="3ae62-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3ae62-166"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3ae62-166"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="3ae62-167">IID</span><span class="sxs-lookup"><span data-stu-id="3ae62-167">IID</span></span><br/>                      | <span data-ttu-id="3ae62-168">IID \_ ISCardISO7816 é definido como 53B6AA68-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="3ae62-168">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="3ae62-169">Confira também</span><span class="sxs-lookup"><span data-stu-id="3ae62-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ae62-170">**EraseBinary**</span><span class="sxs-lookup"><span data-stu-id="3ae62-170">**EraseBinary**</span></span>](iscardiso7816-erasebinary.md)
</dt> <dt>

[<span data-ttu-id="3ae62-171">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="3ae62-171">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> <dt>

[<span data-ttu-id="3ae62-172">**ReadBinary**</span><span class="sxs-lookup"><span data-stu-id="3ae62-172">**ReadBinary**</span></span>](iscardiso7816-readbinary.md)
</dt> <dt>

[<span data-ttu-id="3ae62-173">**UpdateBinary**</span><span class="sxs-lookup"><span data-stu-id="3ae62-173">**UpdateBinary**</span></span>](iscardiso7816-updatebinary.md)
</dt> </dl>

 

 
