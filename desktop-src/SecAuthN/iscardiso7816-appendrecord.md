---
description: O método AppendRecord constrói um comando de APDU (unidade de dados de protocolo de aplicativo) que acrescenta um registro ao final de um arquivo elementar estruturado linear (EF) ou grava o número de registro 1 em um arquivo elementares estruturado em cíclica.
ms.assetid: 4dd88661-41c4-4238-88c9-279b39afb206
title: 'Método ISCardISO7816:: AppendRecord (Scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.AppendRecord
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 28d1b6762e0a350bb87b673f21fa063ae2478e64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164985"
---
# <a name="iscardiso7816appendrecord-method"></a><span data-ttu-id="a401f-103">Método ISCardISO7816:: AppendRecord</span><span class="sxs-lookup"><span data-stu-id="a401f-103">ISCardISO7816::AppendRecord method</span></span>

<span data-ttu-id="a401f-104">\[O método **AppendRecord** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="a401f-104">\[The **AppendRecord** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="a401f-105">Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="a401f-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="a401f-106">Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="a401f-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="a401f-107">O método **AppendRecord** constrói um comando de APDU ( [*unidade de dados de protocolo de aplicativo*](../secgloss/a-gly.md) ) que acrescenta um registro ao final de um arquivo elementar estruturado linear (EF) ou grava o número de registro 1 em um arquivo elementares estruturado em cíclica.</span><span class="sxs-lookup"><span data-stu-id="a401f-107">The **AppendRecord** method constructs an [*application protocol data unit*](../secgloss/a-gly.md) (APDU) command that either appends a record to the end of a linear-structured elementary file (EF) or writes record number 1 in a cyclic-structured elementary file.</span></span>

## <a name="syntax"></a><span data-ttu-id="a401f-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a401f-108">Syntax</span></span>


```C++
HRESULT AppendRecord(
  [in]      BYTE         byRefCtrl,
  [in]      LPBYTEBUFFER pData,
  [in, out] LPSCARDCMD   *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="a401f-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a401f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a401f-110">*byRefCtrl* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a401f-110">*byRefCtrl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a401f-111">Identifica o arquivo elementar a ser anexado.</span><span class="sxs-lookup"><span data-stu-id="a401f-111">Identifies the elementary file to be appended.</span></span>



| <span data-ttu-id="a401f-112">Valor</span><span class="sxs-lookup"><span data-stu-id="a401f-112">Value</span></span>                                                                                                                                                                                | <span data-ttu-id="a401f-113">Significado</span><span class="sxs-lookup"><span data-stu-id="a401f-113">Meaning</span></span>                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <span id="Current_EF"></span><span id="current_ef"></span><span id="CURRENT_EF"></span><dl> <span data-ttu-id="a401f-114"><dt>**EF atual**</dt></span><span class="sxs-lookup"><span data-stu-id="a401f-114"><dt>**Current EF**</dt></span></span> </dl>     | <span data-ttu-id="a401f-115">Posição do bit: 00000000</span><span class="sxs-lookup"><span data-stu-id="a401f-115">Bit position: 00000000</span></span><br/> |
| <span id="Short_EF_ID"></span><span id="short_ef_id"></span><span id="SHORT_EF_ID"></span><dl> <span data-ttu-id="a401f-116"><dt>**ID curta do EF**</dt></span><span class="sxs-lookup"><span data-stu-id="a401f-116"><dt>**Short EF ID**</dt></span></span> </dl> | <span data-ttu-id="a401f-117">Posição do bit: xxxxx000</span><span class="sxs-lookup"><span data-stu-id="a401f-117">Bit position: xxxxx000</span></span><br/> |
| <span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span><dl> <span data-ttu-id="a401f-118"><dt>**Reservado**</dt></span><span class="sxs-lookup"><span data-stu-id="a401f-118"><dt>**Reserved**</dt></span></span> </dl>             | <span data-ttu-id="a401f-119">Posição do bit: xxxxxxxx</span><span class="sxs-lookup"><span data-stu-id="a401f-119">Bit position: xxxxxxxx</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="a401f-120">*pData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a401f-120">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a401f-121">Um ponteiro para os dados a serem acrescentados ao arquivo.</span><span class="sxs-lookup"><span data-stu-id="a401f-121">A pointer to the data to be appended to the file.</span></span>



| <span data-ttu-id="a401f-122">Valor</span><span class="sxs-lookup"><span data-stu-id="a401f-122">Value</span></span>                                                                                                                                                | <span data-ttu-id="a401f-123">Significado</span><span class="sxs-lookup"><span data-stu-id="a401f-123">Meaning</span></span>                 |
|------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| <span id="Tn"></span><span id="tn"></span><span id="TN"></span><dl> <span data-ttu-id="a401f-124"><dt>**TN**</dt></span><span class="sxs-lookup"><span data-stu-id="a401f-124"><dt>**Tn**</dt></span></span> </dl>     | <span data-ttu-id="a401f-125">1 byte</span><span class="sxs-lookup"><span data-stu-id="a401f-125">1 byte</span></span><br/>       |
| <span id="Ln_"></span><span id="ln_"></span><span id="LN_"></span><dl> <span data-ttu-id="a401f-126"><dt>**Ln**</dt></span><span class="sxs-lookup"><span data-stu-id="a401f-126"><dt>**Ln** </dt></span></span> </dl> | <span data-ttu-id="a401f-127">1 ou 3 bytes</span><span class="sxs-lookup"><span data-stu-id="a401f-127">1 or 3 bytes</span></span><br/> |
| <span id="data"></span><span id="DATA"></span><dl> <span data-ttu-id="a401f-128"><dt>**dado**</dt></span><span class="sxs-lookup"><span data-stu-id="a401f-128"><dt>**data**</dt></span></span> </dl>                    | <span data-ttu-id="a401f-129">Bytes de ln</span><span class="sxs-lookup"><span data-stu-id="a401f-129">Ln bytes</span></span><br/>     |



 

</dd> <dt>

<span data-ttu-id="a401f-130">*ppCmd* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="a401f-130">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a401f-131">Na entrada, um ponteiro para um objeto de interface [**ISCardCmd**](iscardcmd.md) ou **nulo**.</span><span class="sxs-lookup"><span data-stu-id="a401f-131">On input, a pointer to an [**ISCardCmd**](iscardcmd.md) interface object or **NULL**.</span></span>

<span data-ttu-id="a401f-132">No retorno, ele é preenchido com o comando APDU construído por essa operação.</span><span class="sxs-lookup"><span data-stu-id="a401f-132">On return, it is filled with the APDU command constructed by this operation.</span></span> <span data-ttu-id="a401f-133">Se *ppCmd* foi definido como **NULL**, um objeto [**ISCardCmd**](iscardcmd.md) de [*cartão inteligente*](../secgloss/s-gly.md) será criado internamente e retornado usando o ponteiro *ppCmd* .</span><span class="sxs-lookup"><span data-stu-id="a401f-133">If *ppCmd* was set to **NULL**, a [*smart card*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) object is internally created and returned by using the *ppCmd* pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a401f-134">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a401f-134">Return value</span></span>

<span data-ttu-id="a401f-135">O método retorna um dos seguintes valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="a401f-135">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="a401f-136">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="a401f-136">Return code</span></span>                                                                                   | <span data-ttu-id="a401f-137">Descrição</span><span class="sxs-lookup"><span data-stu-id="a401f-137">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="a401f-138"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a401f-138"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="a401f-139">Operação concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="a401f-139">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="a401f-140"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="a401f-140"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="a401f-141">Parâmetro inválido.</span><span class="sxs-lookup"><span data-stu-id="a401f-141">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="a401f-142"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="a401f-142"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="a401f-143">Um ponteiro inadequado foi passado.</span><span class="sxs-lookup"><span data-stu-id="a401f-143">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="a401f-144"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="a401f-144"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="a401f-145">Sem memória.</span><span class="sxs-lookup"><span data-stu-id="a401f-145">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="a401f-146">Comentários</span><span class="sxs-lookup"><span data-stu-id="a401f-146">Remarks</span></span>

<span data-ttu-id="a401f-147">O comando encapsulado só poderá ser executado se o status de segurança do [*cartão inteligente*](../secgloss/s-gly.md) satisfizer os atributos de segurança da leitura do arquivo elementar.</span><span class="sxs-lookup"><span data-stu-id="a401f-147">The encapsulated command can only be performed if the security status of the [*smart card*](../secgloss/s-gly.md) satisfies the security attributes of the elementary file read.</span></span>

<span data-ttu-id="a401f-148">Se outro arquivo elementar estiver selecionado no momento da emissão desse comando, ele poderá ser processado sem a identificação do arquivo selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="a401f-148">If another elementary file is selected at the time of issuing this command, it may be processed without identification of the currently selected file.</span></span>

<span data-ttu-id="a401f-149">Os arquivos elementares sem uma estrutura de registro não podem ser lidos.</span><span class="sxs-lookup"><span data-stu-id="a401f-149">Elementary files without a record structure cannot be read.</span></span> <span data-ttu-id="a401f-150">O comando encapsulado aborta se aplicado a um arquivo elementar sem uma estrutura de registro.</span><span class="sxs-lookup"><span data-stu-id="a401f-150">The encapsulated command aborts if applied to an elementary file without a record structure.</span></span>

<span data-ttu-id="a401f-151">Para obter uma lista de todos os métodos fornecidos por essa interface, consulte [**ISCardISO7816**](iscardiso7816.md).</span><span class="sxs-lookup"><span data-stu-id="a401f-151">For a list of all the methods provided by this interface, see [**ISCardISO7816**](iscardiso7816.md).</span></span>

<span data-ttu-id="a401f-152">Além dos códigos de erro COM listados acima, essa interface pode retornar um código de erro de cartão inteligente se uma função de cartão inteligente foi chamada para concluir a solicitação.</span><span class="sxs-lookup"><span data-stu-id="a401f-152">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="a401f-153">Para obter mais informações, consulte [valores de retorno de cartão inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="a401f-153">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a401f-154">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a401f-154">Requirements</span></span>



| <span data-ttu-id="a401f-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="a401f-155">Requirement</span></span> | <span data-ttu-id="a401f-156">Valor</span><span class="sxs-lookup"><span data-stu-id="a401f-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a401f-157">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a401f-157">Minimum supported client</span></span><br/> | <span data-ttu-id="a401f-158">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="a401f-158">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="a401f-159">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a401f-159">Minimum supported server</span></span><br/> | <span data-ttu-id="a401f-160">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a401f-160">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a401f-161">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="a401f-161">End of client support</span></span><br/>    | <span data-ttu-id="a401f-162">Windows XP</span><span class="sxs-lookup"><span data-stu-id="a401f-162">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="a401f-163">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="a401f-163">End of server support</span></span><br/>    | <span data-ttu-id="a401f-164">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a401f-164">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="a401f-165">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a401f-165">Header</span></span><br/>                   | <dl> <span data-ttu-id="a401f-166"><dt>Scardssp. h</dt></span><span class="sxs-lookup"><span data-stu-id="a401f-166"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="a401f-167">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="a401f-167">Type library</span></span><br/>             | <dl> <span data-ttu-id="a401f-168"><dt>Scardsrv. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="a401f-168"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="a401f-169">DLL</span><span class="sxs-lookup"><span data-stu-id="a401f-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a401f-170"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a401f-170"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="a401f-171">IID</span><span class="sxs-lookup"><span data-stu-id="a401f-171">IID</span></span><br/>                      | <span data-ttu-id="a401f-172">IID \_ ISCardISO7816 é definido como 53B6AA68-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="a401f-172">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="a401f-173">Confira também</span><span class="sxs-lookup"><span data-stu-id="a401f-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a401f-174">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="a401f-174">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> <dt>

[<span data-ttu-id="a401f-175">**ReadRecord**</span><span class="sxs-lookup"><span data-stu-id="a401f-175">**ReadRecord**</span></span>](iscardiso7816-readrecord.md)
</dt> <dt>

[<span data-ttu-id="a401f-176">**Atualizarregistro**</span><span class="sxs-lookup"><span data-stu-id="a401f-176">**UpdateRecord**</span></span>](iscardiso7816-updaterecord.md)
</dt> <dt>

[<span data-ttu-id="a401f-177">**WriteRecord**</span><span class="sxs-lookup"><span data-stu-id="a401f-177">**WriteRecord**</span></span>](iscardiso7816-writerecord.md)
</dt> </dl>

 

 
