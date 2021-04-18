---
description: O método UpdateBinary constrói um comando APDU (unidade de dados de protocolo de aplicativo) que atualiza os bits presentes em um arquivo elementar com os bits fornecidos no comando APDU.
ms.assetid: 14ac6ad9-efcf-48ea-8712-19caeee47521
title: 'Método ISCardISO7816:: UpdateBinary (Scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.UpdateBinary
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: d9651189cab228eaa5dacc9c2f5963201bbc65c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105749969"
---
# <a name="iscardiso7816updatebinary-method"></a><span data-ttu-id="f5c5b-103">Método ISCardISO7816:: UpdateBinary</span><span class="sxs-lookup"><span data-stu-id="f5c5b-103">ISCardISO7816::UpdateBinary method</span></span>

<span data-ttu-id="f5c5b-104">\[O método **UpdateBinary** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="f5c5b-104">\[The **UpdateBinary** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="f5c5b-105">Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="f5c5b-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="f5c5b-106">Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="f5c5b-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="f5c5b-107">O método **UpdateBinary** constrói um comando APDU ( [*unidade de dados de protocolo de aplicativo*](../secgloss/a-gly.md) ) que atualiza os bits presentes em um arquivo elementar com os bits fornecidos no comando APDU.</span><span class="sxs-lookup"><span data-stu-id="f5c5b-107">The **UpdateBinary** method constructs an [*application protocol data unit*](../secgloss/a-gly.md) (APDU) command that updates the bits present in an elementary file with the bits given in the APDU command.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5c5b-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f5c5b-108">Syntax</span></span>


```C++
HRESULT UpdateBinary(
  [in]      BYTE         byP1,
  [in]      BYTE         byP2,
  [in]      LPBYTEBUFFER pData,
  [in, out] LPSCARDCMD   *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="f5c5b-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f5c5b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5c5b-110">*byP1* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f5c5b-110">*byP1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5c5b-111">Deslocamento para o local de gravação (atualização) no binário desde o início do binário.</span><span class="sxs-lookup"><span data-stu-id="f5c5b-111">Offset to the write (update) location into the binary from the start of the binary.</span></span> <span data-ttu-id="f5c5b-112">Se B8 = 1 em P1, a B7 e a B6 de P1 são definidas como zero (RFU bits), B5 a B1 de P1 são um identificador curto de EF e P2 é o deslocamento do primeiro byte a ser atualizado em unidades de dados a partir do início do arquivo.</span><span class="sxs-lookup"><span data-stu-id="f5c5b-112">If b8=1 in P1, then b7 and b6 of P1 are set to zero (RFU bits), b5 to b1 of P1 are a short EF identifier and P2 is the offset of the first byte to be updated in data units from the beginning of the file.</span></span> <span data-ttu-id="f5c5b-113">Se B8 = 0 em P1, P1 \| \| P2 será o deslocamento do primeiro byte a ser atualizado nas unidades de dados a partir do início do arquivo.</span><span class="sxs-lookup"><span data-stu-id="f5c5b-113">If b8=0 in P1, then P1 \|\| P2 is the offset of the first byte to be updated in data units from the beginning of the file.</span></span>

</dd> <dt>

<span data-ttu-id="f5c5b-114">*byP2* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f5c5b-114">*byP2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5c5b-115">Deslocamento para o local de gravação (atualização) no binário desde o início do binário.</span><span class="sxs-lookup"><span data-stu-id="f5c5b-115">Offset to the write (update) location into the binary from the start of the binary.</span></span> <span data-ttu-id="f5c5b-116">Se B8 = 1 em P1, a B7 e a B6 de P1 são definidas como zero (RFU bits), B5 a B1 de P1 são um identificador curto de EF e P2 é o deslocamento do primeiro byte a ser atualizado em unidades de dados a partir do início do arquivo.</span><span class="sxs-lookup"><span data-stu-id="f5c5b-116">If b8=1 in P1, then b7 and b6 of P1 are set to zero (RFU bits), b5 to b1 of P1 are a short EF identifier and P2 is the offset of the first byte to be updated in data units from the beginning of the file.</span></span> <span data-ttu-id="f5c5b-117">Se B8 = 0 em P1, P1 \| \| P2 será o deslocamento do primeiro byte a ser atualizado nas unidades de dados a partir do início do arquivo.</span><span class="sxs-lookup"><span data-stu-id="f5c5b-117">If b8=0 in P1, then P1 \|\| P2 is the offset of the first byte to be updated in data units from the beginning of the file.</span></span>

</dd> <dt>

<span data-ttu-id="f5c5b-118">*pData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f5c5b-118">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5c5b-119">Ponteiro para a cadeia de caracteres das unidades de dados a serem atualizadas.</span><span class="sxs-lookup"><span data-stu-id="f5c5b-119">Pointer to the string of data units to be updated.</span></span>

</dd> <dt>

<span data-ttu-id="f5c5b-120">*ppCmd* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="f5c5b-120">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f5c5b-121">Na entrada, um ponteiro para um objeto de interface [**ISCardCmd**](iscardcmd.md) ou **nulo**.</span><span class="sxs-lookup"><span data-stu-id="f5c5b-121">On input, a pointer to an [**ISCardCmd**](iscardcmd.md) interface object or **NULL**.</span></span>

<span data-ttu-id="f5c5b-122">No retorno, ele é preenchido com o comando APDU construído por essa operação.</span><span class="sxs-lookup"><span data-stu-id="f5c5b-122">On return, it is filled with the APDU command constructed by this operation.</span></span> <span data-ttu-id="f5c5b-123">Se *ppCmd* foi definido como **NULL**, um objeto [**ISCardCmd**](iscardcmd.md) de [*cartão inteligente*](../secgloss/s-gly.md) será criado internamente e retornado usando o ponteiro *ppCmd* .</span><span class="sxs-lookup"><span data-stu-id="f5c5b-123">If *ppCmd* was set to **NULL**, a [*smart card*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) object is internally created and returned using the *ppCmd* pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5c5b-124">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f5c5b-124">Return value</span></span>

<span data-ttu-id="f5c5b-125">O método retorna um dos seguintes valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="f5c5b-125">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="f5c5b-126">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="f5c5b-126">Return code</span></span>                                                                                   | <span data-ttu-id="f5c5b-127">Descrição</span><span class="sxs-lookup"><span data-stu-id="f5c5b-127">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="f5c5b-128"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f5c5b-128"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="f5c5b-129">Operação concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="f5c5b-129">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="f5c5b-130"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="f5c5b-130"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="f5c5b-131">Parâmetro inválido.</span><span class="sxs-lookup"><span data-stu-id="f5c5b-131">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="f5c5b-132"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="f5c5b-132"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="f5c5b-133">Um ponteiro inadequado foi passado.</span><span class="sxs-lookup"><span data-stu-id="f5c5b-133">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="f5c5b-134"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="f5c5b-134"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="f5c5b-135">Sem memória.</span><span class="sxs-lookup"><span data-stu-id="f5c5b-135">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="f5c5b-136">Comentários</span><span class="sxs-lookup"><span data-stu-id="f5c5b-136">Remarks</span></span>

<span data-ttu-id="f5c5b-137">O comando encapsulado só poderá ser executado se o status de segurança do cartão inteligente satisfizer os atributos de segurança do arquivo elementar que está sendo processado.</span><span class="sxs-lookup"><span data-stu-id="f5c5b-137">The encapsulated command can only be performed if the security status of the smart card satisfies the security attributes of the elementary file being processed.</span></span>

<span data-ttu-id="f5c5b-138">Quando o comando contém um identificador elementar curto válido, ele define o arquivo como o arquivo elementar atual.</span><span class="sxs-lookup"><span data-stu-id="f5c5b-138">When the command contains a valid short elementary identifier, it sets the file as current elementary file.</span></span>

<span data-ttu-id="f5c5b-139">Arquivos elementares sem uma estrutura transparente não podem ser apagados.</span><span class="sxs-lookup"><span data-stu-id="f5c5b-139">Elementary files without a transparent structure cannot be erased.</span></span> <span data-ttu-id="f5c5b-140">O comando encapsulado aborta se aplicado a um arquivo elementar sem uma estrutura transparente.</span><span class="sxs-lookup"><span data-stu-id="f5c5b-140">The encapsulated command aborts if applied to an elementary file without a transparent structure.</span></span>

<span data-ttu-id="f5c5b-141">Para obter uma lista de todos os métodos fornecidos por essa interface, consulte [**ISCardISO7816**](iscardiso7816.md).</span><span class="sxs-lookup"><span data-stu-id="f5c5b-141">For a list of all the methods provided by this interface, see [**ISCardISO7816**](iscardiso7816.md).</span></span>

<span data-ttu-id="f5c5b-142">Além dos códigos de erro COM listados acima, essa interface pode retornar um código de erro de cartão inteligente se uma função de cartão inteligente foi chamada para concluir a solicitação.</span><span class="sxs-lookup"><span data-stu-id="f5c5b-142">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="f5c5b-143">Para obter mais informações, consulte [valores de retorno de cartão inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="f5c5b-143">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f5c5b-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f5c5b-144">Requirements</span></span>



| <span data-ttu-id="f5c5b-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5c5b-145">Requirement</span></span> | <span data-ttu-id="f5c5b-146">Valor</span><span class="sxs-lookup"><span data-stu-id="f5c5b-146">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f5c5b-147">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f5c5b-147">Minimum supported client</span></span><br/> | <span data-ttu-id="f5c5b-148">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="f5c5b-148">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="f5c5b-149">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f5c5b-149">Minimum supported server</span></span><br/> | <span data-ttu-id="f5c5b-150">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f5c5b-150">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f5c5b-151">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="f5c5b-151">End of client support</span></span><br/>    | <span data-ttu-id="f5c5b-152">Windows XP</span><span class="sxs-lookup"><span data-stu-id="f5c5b-152">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="f5c5b-153">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="f5c5b-153">End of server support</span></span><br/>    | <span data-ttu-id="f5c5b-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f5c5b-154">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="f5c5b-155">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f5c5b-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="f5c5b-156"><dt>Scardssp. h</dt></span><span class="sxs-lookup"><span data-stu-id="f5c5b-156"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="f5c5b-157">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="f5c5b-157">Type library</span></span><br/>             | <dl> <span data-ttu-id="f5c5b-158"><dt>Scardsrv. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="f5c5b-158"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="f5c5b-159">DLL</span><span class="sxs-lookup"><span data-stu-id="f5c5b-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f5c5b-160"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f5c5b-160"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="f5c5b-161">IID</span><span class="sxs-lookup"><span data-stu-id="f5c5b-161">IID</span></span><br/>                      | <span data-ttu-id="f5c5b-162">IID \_ ISCardISO7816 é definido como 53B6AA68-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="f5c5b-162">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="f5c5b-163">Confira também</span><span class="sxs-lookup"><span data-stu-id="f5c5b-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5c5b-164">**EraseBinary**</span><span class="sxs-lookup"><span data-stu-id="f5c5b-164">**EraseBinary**</span></span>](iscardiso7816-erasebinary.md)
</dt> <dt>

[<span data-ttu-id="f5c5b-165">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="f5c5b-165">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> <dt>

[<span data-ttu-id="f5c5b-166">**ReadBinary**</span><span class="sxs-lookup"><span data-stu-id="f5c5b-166">**ReadBinary**</span></span>](iscardiso7816-readbinary.md)
</dt> <dt>

[<span data-ttu-id="f5c5b-167">**WriteBinary**</span><span class="sxs-lookup"><span data-stu-id="f5c5b-167">**WriteBinary**</span></span>](iscardiso7816-writebinary.md)
</dt> </dl>

 

 
