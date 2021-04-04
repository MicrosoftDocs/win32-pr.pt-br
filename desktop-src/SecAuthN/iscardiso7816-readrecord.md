---
description: O método ReadRecord constrói um comando APDU (unidade de dados de protocolo de aplicativo) que lê o conteúdo dos registros especificados ou a parte inicial de um registro de um arquivo elementar.
ms.assetid: b00a3242-93bc-4779-8c62-89157fbcb5d1
title: 'Método ISCardISO7816:: ReadRecord (Scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.ReadRecord
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 0cb9697315a6f9dd2436cd7a64d54fa6b44e00f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010984"
---
# <a name="iscardiso7816readrecord-method"></a><span data-ttu-id="1457c-103">Método ISCardISO7816:: ReadRecord</span><span class="sxs-lookup"><span data-stu-id="1457c-103">ISCardISO7816::ReadRecord method</span></span>

<span data-ttu-id="1457c-104">\[O método **ReadRecord** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="1457c-104">\[The **ReadRecord** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="1457c-105">Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="1457c-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="1457c-106">Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="1457c-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="1457c-107">O método **ReadRecord** constrói um comando APDU ( [*unidade de dados de protocolo de aplicativo*](../secgloss/a-gly.md) ) que lê o conteúdo dos registros especificados ou a parte inicial de um registro de um arquivo elementar.</span><span class="sxs-lookup"><span data-stu-id="1457c-107">The **ReadRecord** method constructs an [*application protocol data unit*](../secgloss/a-gly.md) (APDU) command that reads either the contents of the specified records or the beginning part of one record of an elementary file.</span></span>

## <a name="syntax"></a><span data-ttu-id="1457c-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1457c-108">Syntax</span></span>


```C++
HRESULT ReadRecord(
  [in]      BYTE       byRecordId,
  [in]      BYTE       byRefCtrl,
  [in]      LONG       lBytesToRead,
  [in, out] LPSCARDCMD *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="1457c-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1457c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1457c-110">*byRecordId* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1457c-110">*byRecordId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1457c-111">Registro o número ou a ID do primeiro registro a ser lido (00 indica o registro atual).</span><span class="sxs-lookup"><span data-stu-id="1457c-111">Record number or ID of the first record to be read (00 indicates the current record).</span></span>

</dd> <dt>

<span data-ttu-id="1457c-112">*byRefCtrl* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1457c-112">*byRefCtrl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1457c-113">Codificação do controle de referência.</span><span class="sxs-lookup"><span data-stu-id="1457c-113">Coding of the reference control.</span></span>



| <span data-ttu-id="1457c-114">Valor</span><span class="sxs-lookup"><span data-stu-id="1457c-114">Value</span></span>                                                                                                                                                                                | <span data-ttu-id="1457c-115">Significado</span><span class="sxs-lookup"><span data-stu-id="1457c-115">Meaning</span></span>                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Current_EF"></span><span id="current_ef"></span><span id="CURRENT_EF"></span><dl> <span data-ttu-id="1457c-116"><dt>**EF atual**</dt></span><span class="sxs-lookup"><span data-stu-id="1457c-116"><dt>**Current EF**</dt></span></span> </dl>     | <span data-ttu-id="1457c-117">Posição do bit: 00000---</span><span class="sxs-lookup"><span data-stu-id="1457c-117">Bit position: 00000---</span></span><br/> <span data-ttu-id="1457c-118">EF selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="1457c-118">Currently selected EF.</span></span><br/>                    |
| <span id="Short_EF_ID"></span><span id="short_ef_id"></span><span id="SHORT_EF_ID"></span><dl> <span data-ttu-id="1457c-119"><dt>**ID curta do EF**</dt></span><span class="sxs-lookup"><span data-stu-id="1457c-119"><dt>**Short EF ID**</dt></span></span> </dl> | <span data-ttu-id="1457c-120">Posição do bit: xxxxx---</span><span class="sxs-lookup"><span data-stu-id="1457c-120">Bit position: xxxxx---</span></span><br/> <span data-ttu-id="1457c-121">Identificador curto do EF.</span><span class="sxs-lookup"><span data-stu-id="1457c-121">Short EF identifier.</span></span><br/>                      |
| <span id="RFU"></span><span id="rfu"></span><dl> <span data-ttu-id="1457c-122"><dt>**RFU**</dt></span><span class="sxs-lookup"><span data-stu-id="1457c-122"><dt>**RFU**</dt></span></span> </dl>                                                       | <span data-ttu-id="1457c-123">Posição do bit: 11111---</span><span class="sxs-lookup"><span data-stu-id="1457c-123">Bit position: 11111---</span></span><br/>                                                      |
| <span id="Record__"></span><span id="record__"></span><span id="RECORD__"></span><dl> <span data-ttu-id="1457c-124"><dt>**Gravável \#**</dt></span><span class="sxs-lookup"><span data-stu-id="1457c-124"><dt>**Record \#**</dt></span></span> </dl>            | <span data-ttu-id="1457c-125">Posição do bit:-----1xx</span><span class="sxs-lookup"><span data-stu-id="1457c-125">Bit position: -----1xx</span></span><br/> <span data-ttu-id="1457c-126">Uso do número de registro em P1.</span><span class="sxs-lookup"><span data-stu-id="1457c-126">Usage of record number in P1.</span></span><br/>             |
| <span id="Read_Record"></span><span id="read_record"></span><span id="READ_RECORD"></span><dl> <span data-ttu-id="1457c-127"><dt>**Ler registro**</dt></span><span class="sxs-lookup"><span data-stu-id="1457c-127"><dt>**Read Record**</dt></span></span> </dl> | <span data-ttu-id="1457c-128">Posição do bit:-----100</span><span class="sxs-lookup"><span data-stu-id="1457c-128">Bit position: -----100</span></span><br/> <span data-ttu-id="1457c-129">Leia o registro P1.</span><span class="sxs-lookup"><span data-stu-id="1457c-129">Read record P1.</span></span><br/>                           |
| <span id="Up_to_Last"></span><span id="up_to_last"></span><span id="UP_TO_LAST"></span><dl> <span data-ttu-id="1457c-130"><dt>**Até o último**</dt></span><span class="sxs-lookup"><span data-stu-id="1457c-130"><dt>**Up to Last**</dt></span></span> </dl>     | <span data-ttu-id="1457c-131">Posição do bit:-----101</span><span class="sxs-lookup"><span data-stu-id="1457c-131">Bit position: -----101</span></span><br/> <span data-ttu-id="1457c-132">Leia todos os registros de P1 até o último.</span><span class="sxs-lookup"><span data-stu-id="1457c-132">Read all records from P1 up to the last.</span></span> <br/> |
| <span id="Up_to_P1"></span><span id="up_to_p1"></span><span id="UP_TO_P1"></span><dl> <span data-ttu-id="1457c-133"><dt>**Até P1**</dt></span><span class="sxs-lookup"><span data-stu-id="1457c-133"><dt>**Up to P1**</dt></span></span> </dl>             | <span data-ttu-id="1457c-134">Posição do bit:-----110</span><span class="sxs-lookup"><span data-stu-id="1457c-134">Bit position: -----110</span></span><br/> <span data-ttu-id="1457c-135">Leia todos os registros do último até P1.</span><span class="sxs-lookup"><span data-stu-id="1457c-135">Read all records from the last up to P1.</span></span> <br/> |
| <span id="RFU"></span><span id="rfu"></span><dl> <span data-ttu-id="1457c-136"><dt>**RFU**</dt></span><span class="sxs-lookup"><span data-stu-id="1457c-136"><dt>**RFU**</dt></span></span> </dl>                                                       | <span data-ttu-id="1457c-137">Posição do bit:-----111</span><span class="sxs-lookup"><span data-stu-id="1457c-137">Bit position: -----111</span></span><br/>                                                      |
| <span id="Record_ID"></span><span id="record_id"></span><span id="RECORD_ID"></span><dl> <span data-ttu-id="1457c-138"><dt>**ID do Registro**</dt></span><span class="sxs-lookup"><span data-stu-id="1457c-138"><dt>**Record ID**</dt></span></span> </dl>         | <span data-ttu-id="1457c-139">Posição do bit:-----0XX</span><span class="sxs-lookup"><span data-stu-id="1457c-139">Bit position: -----0xx</span></span><br/> <span data-ttu-id="1457c-140">Uso do número de registro em P1.</span><span class="sxs-lookup"><span data-stu-id="1457c-140">Usage of record number in P1.</span></span><br/>             |
| <span id="First_Occur"></span><span id="first_occur"></span><span id="FIRST_OCCUR"></span><dl> <span data-ttu-id="1457c-141"><dt>**Primeira ocorrência**</dt></span><span class="sxs-lookup"><span data-stu-id="1457c-141"><dt>**First Occur**</dt></span></span> </dl> | <span data-ttu-id="1457c-142">Posição do bit:-----000</span><span class="sxs-lookup"><span data-stu-id="1457c-142">Bit position: -----000</span></span><br/> <span data-ttu-id="1457c-143">Leia a primeira ocorrência.</span><span class="sxs-lookup"><span data-stu-id="1457c-143">Read first occurrence.</span></span> <br/>                   |
| <span id="Last_Occur"></span><span id="last_occur"></span><span id="LAST_OCCUR"></span><dl> <span data-ttu-id="1457c-144"><dt>**Última ocorrência**</dt></span><span class="sxs-lookup"><span data-stu-id="1457c-144"><dt>**Last Occur**</dt></span></span> </dl>     | <span data-ttu-id="1457c-145">Posição do bit:-----001</span><span class="sxs-lookup"><span data-stu-id="1457c-145">Bit position: -----001</span></span><br/> <span data-ttu-id="1457c-146">Leia a última ocorrência.</span><span class="sxs-lookup"><span data-stu-id="1457c-146">Read last occurrence.</span></span> <br/>                    |
| <span id="Next_Occur"></span><span id="next_occur"></span><span id="NEXT_OCCUR"></span><dl> <span data-ttu-id="1457c-147"><dt>**Na próxima ocorrência**</dt></span><span class="sxs-lookup"><span data-stu-id="1457c-147"><dt>**Next Occur**</dt></span></span> </dl>     | <span data-ttu-id="1457c-148">Posição do bit:-----010</span><span class="sxs-lookup"><span data-stu-id="1457c-148">Bit position: -----010</span></span><br/> <span data-ttu-id="1457c-149">Leia a próxima ocorrência.</span><span class="sxs-lookup"><span data-stu-id="1457c-149">Read next occurrence.</span></span> <br/>                    |
| <span id="Previous"></span><span id="previous"></span><span id="PREVIOUS"></span><dl> <span data-ttu-id="1457c-150"><dt>**Anterior**</dt></span><span class="sxs-lookup"><span data-stu-id="1457c-150"><dt>**Previous**</dt></span></span> </dl>             | <span data-ttu-id="1457c-151">Posição do bit:-----011</span><span class="sxs-lookup"><span data-stu-id="1457c-151">Bit position: -----011</span></span><br/> <span data-ttu-id="1457c-152">Ler ocorrência anterior.</span><span class="sxs-lookup"><span data-stu-id="1457c-152">Read previous occurrence.</span></span> <br/>                |
| <span id="Secret"></span><span id="secret"></span><span id="SECRET"></span><dl> <span data-ttu-id="1457c-153"><dt>**RADIUS**</dt></span><span class="sxs-lookup"><span data-stu-id="1457c-153"><dt>**Secret**</dt></span></span> </dl>                     | <span data-ttu-id="1457c-154">Posição do bit:---xxxxx</span><span class="sxs-lookup"><span data-stu-id="1457c-154">Bit position: ---xxxxx</span></span><br/>                                                      |



 

</dd> <dt>

<span data-ttu-id="1457c-155">*lBytesToRead* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1457c-155">*lBytesToRead* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1457c-156">Número de bytes a serem lidos do EF transparente.</span><span class="sxs-lookup"><span data-stu-id="1457c-156">Number of bytes to read from the transparent EF.</span></span>

<span data-ttu-id="1457c-157">Se o campo Le contiver apenas zeros, dependendo de b3b2b1 de P2 e dentro do limite de 256 para comprimento curto ou 65536 para comprimento estendido, o comando deverá ler completamente o único registro solicitado ou a sequência de registros solicitada.</span><span class="sxs-lookup"><span data-stu-id="1457c-157">If the Le field contains only zeros, then depending on b3b2b1 of P2 and within the limit of 256 for short length or 65536 for extended length, the command should read completely either the single requested record or the requested sequence of records.</span></span>

</dd> <dt>

<span data-ttu-id="1457c-158">*ppCmd* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="1457c-158">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1457c-159">Na entrada, um ponteiro para um objeto de interface [**ISCardCmd**](iscardcmd.md) ou **nulo**.</span><span class="sxs-lookup"><span data-stu-id="1457c-159">On input, a pointer to an [**ISCardCmd**](iscardcmd.md) interface object or **NULL**.</span></span>

<span data-ttu-id="1457c-160">No retorno, ele é preenchido com o comando APDU construído por essa operação.</span><span class="sxs-lookup"><span data-stu-id="1457c-160">On return, it is filled with the APDU command constructed by this operation.</span></span> <span data-ttu-id="1457c-161">Se *ppCmd* foi definido como **NULL**, um objeto [**ISCardCmd**](iscardcmd.md) de [*cartão inteligente*](../secgloss/s-gly.md) será criado internamente e retornado por meio do ponteiro *ppCmd* .</span><span class="sxs-lookup"><span data-stu-id="1457c-161">If *ppCmd* was set to **NULL**, a [*smart card*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) object is internally created and returned via the *ppCmd* pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1457c-162">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1457c-162">Return value</span></span>

<span data-ttu-id="1457c-163">O método retorna um dos seguintes valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="1457c-163">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="1457c-164">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="1457c-164">Return code</span></span>                                                                                   | <span data-ttu-id="1457c-165">Description</span><span class="sxs-lookup"><span data-stu-id="1457c-165">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="1457c-166"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="1457c-166"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="1457c-167">Operação concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="1457c-167">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="1457c-168"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="1457c-168"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="1457c-169">Parâmetro inválido.</span><span class="sxs-lookup"><span data-stu-id="1457c-169">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="1457c-170"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="1457c-170"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="1457c-171">Um ponteiro inadequado foi passado.</span><span class="sxs-lookup"><span data-stu-id="1457c-171">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="1457c-172"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="1457c-172"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="1457c-173">Sem memória.</span><span class="sxs-lookup"><span data-stu-id="1457c-173">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="1457c-174">Comentários</span><span class="sxs-lookup"><span data-stu-id="1457c-174">Remarks</span></span>

<span data-ttu-id="1457c-175">O comando encapsulado só poderá ser executado se o status de segurança do [*cartão inteligente*](../secgloss/s-gly.md) satisfizer os atributos de segurança do arquivo elementar que está sendo lido.</span><span class="sxs-lookup"><span data-stu-id="1457c-175">The encapsulated command can only be performed if the security status of the [*smart card*](../secgloss/s-gly.md) satisfies the security attributes of the elementary file being read.</span></span>

<span data-ttu-id="1457c-176">Se outro arquivo elementar estiver selecionado atualmente no momento da emissão desse comando, ele poderá ser processado sem a identificação do arquivo selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="1457c-176">If another elementary file is currently selected at the time of issuing this command, it may be processed without identification of the currently selected file.</span></span>

<span data-ttu-id="1457c-177">Quando o comando contém um identificador elementar curto válido, ele define o arquivo como o arquivo elementar atual.</span><span class="sxs-lookup"><span data-stu-id="1457c-177">When the command contains a valid short elementary identifier, it sets the file as current elementary file.</span></span>

<span data-ttu-id="1457c-178">Os arquivos elementares sem uma estrutura de registro não podem ser lidos.</span><span class="sxs-lookup"><span data-stu-id="1457c-178">Elementary files without a record structure cannot be read.</span></span> <span data-ttu-id="1457c-179">O comando encapsulado aborta se aplicado a um arquivo elementar sem uma estrutura de registro.</span><span class="sxs-lookup"><span data-stu-id="1457c-179">The encapsulated command aborts if applied to an elementary file without a record structure.</span></span>

<span data-ttu-id="1457c-180">Para obter uma lista de todos os métodos fornecidos por essa interface, consulte [**ISCardISO7816**](iscardiso7816.md).</span><span class="sxs-lookup"><span data-stu-id="1457c-180">For a list of all the methods provided by this interface, see [**ISCardISO7816**](iscardiso7816.md).</span></span>

<span data-ttu-id="1457c-181">Além dos códigos de erro COM listados acima, essa interface pode retornar um código de erro de cartão inteligente se uma função de cartão inteligente foi chamada para concluir a solicitação.</span><span class="sxs-lookup"><span data-stu-id="1457c-181">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="1457c-182">Para obter mais informações, consulte [valores de retorno de cartão inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="1457c-182">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1457c-183">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1457c-183">Requirements</span></span>



| <span data-ttu-id="1457c-184">Requisito</span><span class="sxs-lookup"><span data-stu-id="1457c-184">Requirement</span></span> | <span data-ttu-id="1457c-185">Valor</span><span class="sxs-lookup"><span data-stu-id="1457c-185">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1457c-186">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1457c-186">Minimum supported client</span></span><br/> | <span data-ttu-id="1457c-187">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="1457c-187">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="1457c-188">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1457c-188">Minimum supported server</span></span><br/> | <span data-ttu-id="1457c-189">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1457c-189">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1457c-190">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="1457c-190">End of client support</span></span><br/>    | <span data-ttu-id="1457c-191">Windows XP</span><span class="sxs-lookup"><span data-stu-id="1457c-191">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="1457c-192">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="1457c-192">End of server support</span></span><br/>    | <span data-ttu-id="1457c-193">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1457c-193">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="1457c-194">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1457c-194">Header</span></span><br/>                   | <dl> <span data-ttu-id="1457c-195"><dt>Scardssp. h</dt></span><span class="sxs-lookup"><span data-stu-id="1457c-195"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="1457c-196">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="1457c-196">Type library</span></span><br/>             | <dl> <span data-ttu-id="1457c-197"><dt>Scardsrv. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="1457c-197"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="1457c-198">DLL</span><span class="sxs-lookup"><span data-stu-id="1457c-198">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1457c-199"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1457c-199"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="1457c-200">IID</span><span class="sxs-lookup"><span data-stu-id="1457c-200">IID</span></span><br/>                      | <span data-ttu-id="1457c-201">IID \_ ISCardISO7816 é definido como 53B6AA68-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="1457c-201">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="1457c-202">Confira também</span><span class="sxs-lookup"><span data-stu-id="1457c-202">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1457c-203">**AppendRecord**</span><span class="sxs-lookup"><span data-stu-id="1457c-203">**AppendRecord**</span></span>](iscardiso7816-appendrecord.md)
</dt> <dt>

[<span data-ttu-id="1457c-204">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="1457c-204">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> <dt>

[<span data-ttu-id="1457c-205">**Atualizarregistro**</span><span class="sxs-lookup"><span data-stu-id="1457c-205">**UpdateRecord**</span></span>](iscardiso7816-updaterecord.md)
</dt> <dt>

[<span data-ttu-id="1457c-206">**WriteRecord**</span><span class="sxs-lookup"><span data-stu-id="1457c-206">**WriteRecord**</span></span>](iscardiso7816-writerecord.md)
</dt> </dl>

 

 
