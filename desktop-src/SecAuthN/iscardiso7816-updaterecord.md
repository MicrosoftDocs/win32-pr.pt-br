---
description: O método Atualizarregistro constrói um comando APDU (unidade de dados de protocolo de aplicativo) que atualiza um registro específico com os bits fornecidos no comando APDU.
ms.assetid: 66039afd-5d73-41b3-b87b-b5d598c6f3db
title: 'Método ISCardISO7816:: Atualizarregistro (Scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.UpdateRecord
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 6bf810594e623d58944f58d3b7671664b3be175f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104169700"
---
# <a name="iscardiso7816updaterecord-method"></a><span data-ttu-id="1fdc0-103">Método ISCardISO7816:: Atualizarregistro</span><span class="sxs-lookup"><span data-stu-id="1fdc0-103">ISCardISO7816::UpdateRecord method</span></span>

<span data-ttu-id="1fdc0-104">\[O método **atualizarregistro** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="1fdc0-104">\[The **UpdateRecord** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="1fdc0-105">Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="1fdc0-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="1fdc0-106">Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="1fdc0-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="1fdc0-107">O método **atualizarregistro** constrói um comando APDU ( [*unidade de dados de protocolo de aplicativo*](../secgloss/a-gly.md) ) que atualiza um registro específico com os bits fornecidos no comando APDU.</span><span class="sxs-lookup"><span data-stu-id="1fdc0-107">The **UpdateRecord** method constructs an [*application protocol data unit*](../secgloss/a-gly.md) (APDU) command that updates a specific record with the bits given in the APDU command.</span></span>

> [!Note]  
> <span data-ttu-id="1fdc0-108">Ao usar o endereçamento de registro atual, o comando define o ponteiro de registro no registro atualizado com êxito.</span><span class="sxs-lookup"><span data-stu-id="1fdc0-108">When using current record addressing, the command sets the record pointer on the successfully updated record.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="1fdc0-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1fdc0-109">Syntax</span></span>


```C++
HRESULT UpdateRecord(
  [in]      BYTE         byRecordId,
  [in]      BYTE         byRefCtrl,
  [in]      LPBYTEBUFFER pData,
  [in, out] LPSCARDCMD   *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="1fdc0-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1fdc0-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1fdc0-111">*byRecordId* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1fdc0-111">*byRecordId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1fdc0-112">Valor P1:</span><span class="sxs-lookup"><span data-stu-id="1fdc0-112">P1 value:</span></span>

<span data-ttu-id="1fdc0-113">P1 = 00 designa o registro atual</span><span class="sxs-lookup"><span data-stu-id="1fdc0-113">P1 = 00 designates the current record</span></span>

<span data-ttu-id="1fdc0-114">P1! = ' 00 ' é o número do registro especificado</span><span class="sxs-lookup"><span data-stu-id="1fdc0-114">P1 != '00' is the number of the specified record</span></span>

</dd> <dt>

<span data-ttu-id="1fdc0-115">*byRefCtrl* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1fdc0-115">*byRefCtrl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1fdc0-116">Codificação do controle de referência P2:</span><span class="sxs-lookup"><span data-stu-id="1fdc0-116">Coding of the reference control P2:</span></span>



| <span data-ttu-id="1fdc0-117">Valor</span><span class="sxs-lookup"><span data-stu-id="1fdc0-117">Value</span></span>                                                                                                                                                                                                | <span data-ttu-id="1fdc0-118">Significado</span><span class="sxs-lookup"><span data-stu-id="1fdc0-118">Meaning</span></span>                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <span id="Current_EF"></span><span id="current_ef"></span><span id="CURRENT_EF"></span><dl> <span data-ttu-id="1fdc0-119"><dt>**EF atual**</dt></span><span class="sxs-lookup"><span data-stu-id="1fdc0-119"><dt>**Current EF**</dt></span></span> </dl>                     | <span data-ttu-id="1fdc0-120">Posição do bit: 00000---</span><span class="sxs-lookup"><span data-stu-id="1fdc0-120">Bit position: 00000---</span></span><br/> <span data-ttu-id="1fdc0-121">EF selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="1fdc0-121">Currently selected EF.</span></span><br/> |
| <span id="Short_EF_ID"></span><span id="short_ef_id"></span><span id="SHORT_EF_ID"></span><dl> <span data-ttu-id="1fdc0-122"><dt>**ID curta do EF**</dt></span><span class="sxs-lookup"><span data-stu-id="1fdc0-122"><dt>**Short EF ID**</dt></span></span> </dl>                 | <span data-ttu-id="1fdc0-123">Posição do bit: xxxxx---</span><span class="sxs-lookup"><span data-stu-id="1fdc0-123">Bit position: xxxxx---</span></span><br/> <span data-ttu-id="1fdc0-124">Identificador curto do EF.</span><span class="sxs-lookup"><span data-stu-id="1fdc0-124">Short EF identifier.</span></span><br/>   |
| <span id="First_Record"></span><span id="first_record"></span><span id="FIRST_RECORD"></span><dl> <span data-ttu-id="1fdc0-125"><dt>**Primeiro registro**</dt></span><span class="sxs-lookup"><span data-stu-id="1fdc0-125"><dt>**First Record**</dt></span></span> </dl>             | <span data-ttu-id="1fdc0-126">Posição do bit:-----000</span><span class="sxs-lookup"><span data-stu-id="1fdc0-126">Bit position: -----000</span></span><br/>                                   |
| <span id="Last_Record"></span><span id="last_record"></span><span id="LAST_RECORD"></span><dl> <span data-ttu-id="1fdc0-127"><dt>**Último registro**</dt></span><span class="sxs-lookup"><span data-stu-id="1fdc0-127"><dt>**Last Record**</dt></span></span> </dl>                 | <span data-ttu-id="1fdc0-128">Posição do bit:-----001</span><span class="sxs-lookup"><span data-stu-id="1fdc0-128">Bit position: -----001</span></span><br/>                                   |
| <span id="Next_Record"></span><span id="next_record"></span><span id="NEXT_RECORD"></span><dl> <span data-ttu-id="1fdc0-129"><dt>**Próximo registro**</dt></span><span class="sxs-lookup"><span data-stu-id="1fdc0-129"><dt>**Next Record**</dt></span></span> </dl>                 | <span data-ttu-id="1fdc0-130">Posição do bit:-----010</span><span class="sxs-lookup"><span data-stu-id="1fdc0-130">Bit position: -----010</span></span><br/>                                   |
| <span id="Previous_Record"></span><span id="previous_record"></span><span id="PREVIOUS_RECORD"></span><dl> <span data-ttu-id="1fdc0-131"><dt>**Registro anterior**</dt></span><span class="sxs-lookup"><span data-stu-id="1fdc0-131"><dt>**Previous Record**</dt></span></span> </dl> | <span data-ttu-id="1fdc0-132">Posição do bit:-----011</span><span class="sxs-lookup"><span data-stu-id="1fdc0-132">Bit position: -----011</span></span><br/>                                   |
| <span id="Record___in_P1"></span><span id="record___in_p1"></span><span id="RECORD___IN_P1"></span><dl> <span data-ttu-id="1fdc0-133"><dt>**Registro \# em P1**</dt></span><span class="sxs-lookup"><span data-stu-id="1fdc0-133"><dt>**Record \# in P1**</dt></span></span> </dl>    | <span data-ttu-id="1fdc0-134">Posição do bit:-----100</span><span class="sxs-lookup"><span data-stu-id="1fdc0-134">Bit position: -----100</span></span><br/>                                   |



 

</dd> <dt>

<span data-ttu-id="1fdc0-135">*pData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1fdc0-135">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1fdc0-136">Ponteiro para o registro a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="1fdc0-136">Pointer to the record to be updated.</span></span>

</dd> <dt>

<span data-ttu-id="1fdc0-137">*ppCmd* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="1fdc0-137">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1fdc0-138">Na entrada, um ponteiro para um objeto de interface [**ISCardCmd**](iscardcmd.md) ou **nulo**.</span><span class="sxs-lookup"><span data-stu-id="1fdc0-138">On input, a pointer to an [**ISCardCmd**](iscardcmd.md) interface object or **NULL**.</span></span>

<span data-ttu-id="1fdc0-139">No retorno, ele é preenchido com o comando APDU construído por essa operação.</span><span class="sxs-lookup"><span data-stu-id="1fdc0-139">On return, it is filled with the APDU command constructed by this operation.</span></span> <span data-ttu-id="1fdc0-140">Se *ppCmd* foi definido como **NULL**, um objeto [**ISCardCmd**](iscardcmd.md) de [*cartão inteligente*](../secgloss/s-gly.md) será criado internamente e retornado por meio do ponteiro *ppCmd* .</span><span class="sxs-lookup"><span data-stu-id="1fdc0-140">If *ppCmd* was set to **NULL**, a [*smart card*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) object is internally created and returned via the *ppCmd* pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1fdc0-141">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1fdc0-141">Return value</span></span>

<span data-ttu-id="1fdc0-142">O método retorna um dos seguintes valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="1fdc0-142">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="1fdc0-143">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="1fdc0-143">Return code</span></span>                                                                                   | <span data-ttu-id="1fdc0-144">Descrição</span><span class="sxs-lookup"><span data-stu-id="1fdc0-144">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="1fdc0-145"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="1fdc0-145"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="1fdc0-146">Operação concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="1fdc0-146">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="1fdc0-147"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="1fdc0-147"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="1fdc0-148">Parâmetro inválido.</span><span class="sxs-lookup"><span data-stu-id="1fdc0-148">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="1fdc0-149"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="1fdc0-149"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="1fdc0-150">Um ponteiro inadequado foi passado.</span><span class="sxs-lookup"><span data-stu-id="1fdc0-150">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="1fdc0-151"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="1fdc0-151"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="1fdc0-152">Sem memória.</span><span class="sxs-lookup"><span data-stu-id="1fdc0-152">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="1fdc0-153">Comentários</span><span class="sxs-lookup"><span data-stu-id="1fdc0-153">Remarks</span></span>

<span data-ttu-id="1fdc0-154">O comando encapsulado só poderá ser executado se o status de segurança do [*cartão inteligente*](../secgloss/s-gly.md) satisfizer os atributos de segurança do arquivo elementar que está sendo processado.</span><span class="sxs-lookup"><span data-stu-id="1fdc0-154">The encapsulated command can only be performed if the security status of the [*smart card*](../secgloss/s-gly.md) satisfies the security attributes of the elementary file being processed.</span></span>

<span data-ttu-id="1fdc0-155">Quando o comando contém um identificador elementar curto válido, ele define o arquivo como o arquivo elementar atual.</span><span class="sxs-lookup"><span data-stu-id="1fdc0-155">When the command contains a valid short elementary identifier, it sets the file as current elementary file.</span></span> <span data-ttu-id="1fdc0-156">Se outro arquivo elementar estiver selecionado atualmente no momento da emissão desse comando, esse comando poderá ser processado sem a identificação do arquivo selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="1fdc0-156">If another elementary file is currently selected at the time of issuing this command, this command may be processed without identification of the currently selected file.</span></span>

<span data-ttu-id="1fdc0-157">Se o comando construído se aplicar a um arquivo elementar de forma linear ou fixa, ele será anulado se o tamanho do registro for diferente do tamanho do registro existente.</span><span class="sxs-lookup"><span data-stu-id="1fdc0-157">If the constructed command applies to a linear-fixed or cyclic-structured elementary file, it will abort if the record length is different from the length of the existing record.</span></span>

<span data-ttu-id="1fdc0-158">Se o comando se aplicar a um arquivo elementar de variável linear, ele poderá ser executado quando o tamanho do registro for diferente do tamanho do registro existente.</span><span class="sxs-lookup"><span data-stu-id="1fdc0-158">If the command applies to a linear-variable structured elementary file, it may be carried out when the record length is different from the length of the existing record.</span></span>

<span data-ttu-id="1fdc0-159">A opção "Previous" do comando (P2 = xxxxx011), aplicada a um arquivo cíclico, tem o mesmo comportamento que um comando construído por [**AppendRecord**](iscardiso7816-appendrecord.md).</span><span class="sxs-lookup"><span data-stu-id="1fdc0-159">The "previous" option of the command (P2=xxxxx011), applied to a cyclic file, has the same behavior as a command constructed by [**AppendRecord**](iscardiso7816-appendrecord.md).</span></span>

<span data-ttu-id="1fdc0-160">Os arquivos elementares sem uma estrutura de registro não podem ser lidos.</span><span class="sxs-lookup"><span data-stu-id="1fdc0-160">Elementary files without a record structure cannot be read.</span></span> <span data-ttu-id="1fdc0-161">O comando construído é anulado se aplicado a um arquivo elementar sem estrutura de registro.</span><span class="sxs-lookup"><span data-stu-id="1fdc0-161">The constructed command aborts if applied to an elementary file without record structure.</span></span>

<span data-ttu-id="1fdc0-162">Para obter uma lista de todos os métodos fornecidos por essa interface, consulte [**ISCardISO7816**](iscardiso7816.md).</span><span class="sxs-lookup"><span data-stu-id="1fdc0-162">For a list of all the methods provided by this interface, see [**ISCardISO7816**](iscardiso7816.md).</span></span>

<span data-ttu-id="1fdc0-163">Além dos códigos de erro COM listados acima, essa interface pode retornar um código de erro de cartão inteligente se uma função de cartão inteligente foi chamada para concluir a solicitação.</span><span class="sxs-lookup"><span data-stu-id="1fdc0-163">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="1fdc0-164">Para obter mais informações, consulte [valores de retorno de cartão inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="1fdc0-164">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1fdc0-165">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1fdc0-165">Requirements</span></span>



| <span data-ttu-id="1fdc0-166">Requisito</span><span class="sxs-lookup"><span data-stu-id="1fdc0-166">Requirement</span></span> | <span data-ttu-id="1fdc0-167">Valor</span><span class="sxs-lookup"><span data-stu-id="1fdc0-167">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1fdc0-168">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1fdc0-168">Minimum supported client</span></span><br/> | <span data-ttu-id="1fdc0-169">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="1fdc0-169">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="1fdc0-170">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1fdc0-170">Minimum supported server</span></span><br/> | <span data-ttu-id="1fdc0-171">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1fdc0-171">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1fdc0-172">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="1fdc0-172">End of client support</span></span><br/>    | <span data-ttu-id="1fdc0-173">Windows XP</span><span class="sxs-lookup"><span data-stu-id="1fdc0-173">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="1fdc0-174">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="1fdc0-174">End of server support</span></span><br/>    | <span data-ttu-id="1fdc0-175">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1fdc0-175">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="1fdc0-176">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1fdc0-176">Header</span></span><br/>                   | <dl> <span data-ttu-id="1fdc0-177"><dt>Scardssp. h</dt></span><span class="sxs-lookup"><span data-stu-id="1fdc0-177"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="1fdc0-178">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="1fdc0-178">Type library</span></span><br/>             | <dl> <span data-ttu-id="1fdc0-179"><dt>Scardsrv. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="1fdc0-179"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="1fdc0-180">DLL</span><span class="sxs-lookup"><span data-stu-id="1fdc0-180">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1fdc0-181"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1fdc0-181"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="1fdc0-182">IID</span><span class="sxs-lookup"><span data-stu-id="1fdc0-182">IID</span></span><br/>                      | <span data-ttu-id="1fdc0-183">IID \_ ISCardISO7816 é definido como 53B6AA68-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="1fdc0-183">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="1fdc0-184">Confira também</span><span class="sxs-lookup"><span data-stu-id="1fdc0-184">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1fdc0-185">**AppendRecord**</span><span class="sxs-lookup"><span data-stu-id="1fdc0-185">**AppendRecord**</span></span>](iscardiso7816-appendrecord.md)
</dt> <dt>

[<span data-ttu-id="1fdc0-186">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="1fdc0-186">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> <dt>

[<span data-ttu-id="1fdc0-187">**ReadRecord**</span><span class="sxs-lookup"><span data-stu-id="1fdc0-187">**ReadRecord**</span></span>](iscardiso7816-readrecord.md)
</dt> <dt>

[<span data-ttu-id="1fdc0-188">**WriteRecord**</span><span class="sxs-lookup"><span data-stu-id="1fdc0-188">**WriteRecord**</span></span>](iscardiso7816-writerecord.md)
</dt> </dl>

 

 
