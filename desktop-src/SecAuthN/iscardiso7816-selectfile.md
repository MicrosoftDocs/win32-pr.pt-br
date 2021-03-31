---
description: O método selectfile constrói um comando APDU (unidade de dados do protocolo de aplicativo) que define um arquivo elementar atual em um canal lógico. Os comandos subsequentes podem se referir implicitamente ao arquivo atual por meio do canal lógico.
ms.assetid: cb6231b3-fb1c-4350-8797-9efaa663c21b
title: 'Método ISCardISO7816:: selectfile (Scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.SelectFile
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 9bab499d32a65a2e6b4348458ec42328029760ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104169699"
---
# <a name="iscardiso7816selectfile-method"></a><span data-ttu-id="c85df-104">Método ISCardISO7816:: selectfile</span><span class="sxs-lookup"><span data-stu-id="c85df-104">ISCardISO7816::SelectFile method</span></span>

<span data-ttu-id="c85df-105">\[O método **selectfile** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="c85df-105">\[The **SelectFile** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="c85df-106">Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="c85df-106">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="c85df-107">Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="c85df-107">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="c85df-108">O método **selectfile** constrói um comando APDU ( [*unidade de dados do protocolo de aplicativo*](../secgloss/a-gly.md) ) que define um arquivo elementar atual em um canal lógico.</span><span class="sxs-lookup"><span data-stu-id="c85df-108">The **SelectFile** method constructs an [*application protocol data unit*](../secgloss/a-gly.md) (APDU) command that sets a current elementary file within a logical channel.</span></span> <span data-ttu-id="c85df-109">Os comandos subsequentes podem se referir implicitamente ao arquivo atual por meio do canal lógico.</span><span class="sxs-lookup"><span data-stu-id="c85df-109">Subsequent commands may implicitly refer to the current file through the logical channel.</span></span>

<span data-ttu-id="c85df-110">Selecionar um diretório (DF) dentro do repositório filestore — que pode ser a raiz (MF) do filestore — o torna o DF atual.</span><span class="sxs-lookup"><span data-stu-id="c85df-110">Selecting a directory (DF) within the card filestore — which may be the root (MF) of the filestore — makes it the current DF.</span></span> <span data-ttu-id="c85df-111">Após essa seleção, um arquivo elementar atual implícito pode ser referenciado por meio desse canal lógico.</span><span class="sxs-lookup"><span data-stu-id="c85df-111">After such a selection, an implicit current elementary file may be referred to through that logical channel.</span></span>

<span data-ttu-id="c85df-112">Selecionar um arquivo elementar define o arquivo selecionado e seu pai como arquivos atuais.</span><span class="sxs-lookup"><span data-stu-id="c85df-112">Selecting an elementary file sets the selected file and its parent as current files.</span></span>

<span data-ttu-id="c85df-113">Após a resposta a ser redefinida, o MF é selecionado implicitamente por meio do canal lógico básico, a menos que especificado de forma diferente nos bytes históricos ou na cadeia de caracteres de dados inicial.</span><span class="sxs-lookup"><span data-stu-id="c85df-113">After the answer to reset, the MF is implicitly selected through the basic logical channel, unless specified differently in the historical bytes or in the initial data string.</span></span>

## <a name="syntax"></a><span data-ttu-id="c85df-114">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c85df-114">Syntax</span></span>


```C++
HRESULT SelectFile(
  [in]      BYTE         byP1,
  [in]      BYTE         byP2,
  [in]      LPBYTEBUFFER pData,
  [in]      LONG         lBytesToRead,
  [in, out] LPSCARDCMD   *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="c85df-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c85df-115">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c85df-116">*byP1* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c85df-116">*byP1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c85df-117">Controle de seleção.</span><span class="sxs-lookup"><span data-stu-id="c85df-117">Selection control.</span></span>



| <span data-ttu-id="c85df-118">P1 (byte superior no Word): 8 7 6 5 4 3 2 1</span><span class="sxs-lookup"><span data-stu-id="c85df-118">P1 (upper byte in word): 8 7 6 5 4 3 2 1</span></span>                                                                                                                                                            | <span data-ttu-id="c85df-119">Significado</span><span class="sxs-lookup"><span data-stu-id="c85df-119">Meaning</span></span>                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------|
| <span id="000000xx"></span><span id="000000XX"></span><dl> <span data-ttu-id="c85df-120"><dt>**000000xx**</dt><dt></dt></span><span class="sxs-lookup"><span data-stu-id="c85df-120"><dt>**000000xx**</dt> <dt></dt></span></span> </dl> | <span data-ttu-id="c85df-121">Selecionar ID do arquivo</span><span class="sxs-lookup"><span data-stu-id="c85df-121">Select File ID</span></span><br/>          |
| <span id="00000000"></span><dl> <span data-ttu-id="c85df-122"><dt>**00000000**</dt><dt></dt></span><span class="sxs-lookup"><span data-stu-id="c85df-122"><dt>**00000000**</dt> <dt></dt></span></span> </dl>                            | <span data-ttu-id="c85df-123">EF, DF ou MF</span><span class="sxs-lookup"><span data-stu-id="c85df-123">EF, DF, or MF</span></span><br/>           |
| <span id="00000001"></span><dl> <span data-ttu-id="c85df-124"><dt>**00000001**</dt><dt></dt></span><span class="sxs-lookup"><span data-stu-id="c85df-124"><dt>**00000001**</dt> <dt></dt></span></span> </dl>                            | <span data-ttu-id="c85df-125">DF filho</span><span class="sxs-lookup"><span data-stu-id="c85df-125">Child DF</span></span><br/>                |
| <span id="00000010"></span><dl> <span data-ttu-id="c85df-126"><dt>**00000010**</dt><dt></dt></span><span class="sxs-lookup"><span data-stu-id="c85df-126"><dt>**00000010**</dt> <dt></dt></span></span> </dl>                            | <span data-ttu-id="c85df-127">EF em DF</span><span class="sxs-lookup"><span data-stu-id="c85df-127">EF under DF</span></span><br/>             |
| <span id="00000011"></span><dl> <span data-ttu-id="c85df-128"><dt>**00000011**</dt><dt></dt></span><span class="sxs-lookup"><span data-stu-id="c85df-128"><dt>**00000011**</dt> <dt></dt></span></span> </dl>                            | <span data-ttu-id="c85df-129">DF pai do DF atual</span><span class="sxs-lookup"><span data-stu-id="c85df-129">Parent DF of current DF</span></span><br/> |



 

<span data-ttu-id="c85df-130">Quando P1 = 00, o cartão saberá devido a uma codificação específica da ID do arquivo ou devido ao contexto de execução do comando se o arquivo a ser selecionado for o MF, um DF ou um EF.</span><span class="sxs-lookup"><span data-stu-id="c85df-130">When P1=00, the card knows either because of a specific coding of the file ID or because of the context of execution of the command if the file to select is the MF, a DF, or an EF.</span></span>

<span data-ttu-id="c85df-131">Quando P1-P2 = 0000, se uma ID de arquivo for fornecida, ela deverá ser exclusiva nos seguintes ambientes:</span><span class="sxs-lookup"><span data-stu-id="c85df-131">When P1-P2=0000, if a file ID is provided, then it shall be unique in the following environments:</span></span>

-   <span data-ttu-id="c85df-132">Filhos imediatos da DF atual</span><span class="sxs-lookup"><span data-stu-id="c85df-132">Immediate children of the current DF</span></span>
-   <span data-ttu-id="c85df-133">DF pai</span><span class="sxs-lookup"><span data-stu-id="c85df-133">Parent DF</span></span>
-   <span data-ttu-id="c85df-134">Filhos imediatos da DF pai</span><span class="sxs-lookup"><span data-stu-id="c85df-134">Immediate children of the parent DF</span></span>

<span data-ttu-id="c85df-135">Se P1-P2 = 0000 e se o campo de dados estiver vazio ou for igual a 3F00, selecione o MF.</span><span class="sxs-lookup"><span data-stu-id="c85df-135">If P1-P2=0000 and if the data field is empty or equal to 3F00, then select the MF.</span></span>

<span data-ttu-id="c85df-136">Quando P1 = 04, o campo de dados é um nome de DF, possivelmente truncado à direita.</span><span class="sxs-lookup"><span data-stu-id="c85df-136">When P1=04, the data field is a DF name, possibly right truncated.</span></span>

<span data-ttu-id="c85df-137">Quando há suporte, os comandos sucessivos com o mesmo campo de dados devem selecionar o DFs cujos nomes correspondem ao campo de dados (ou seja, começar com o campo de dados de comando).</span><span class="sxs-lookup"><span data-stu-id="c85df-137">When supported, successive such commands with the same data field shall select DFs whose names match with the data field (that is, start with the command data field).</span></span> <span data-ttu-id="c85df-138">Se o cartão aceitar o comando com um campo de dados vazio, todos ou um subconjunto do DFs poderá ser selecionado sucessivamente.</span><span class="sxs-lookup"><span data-stu-id="c85df-138">If the card accepts the command with an empty data field, then all or a subset of the DFs can be successively selected.</span></span>

</dd> <dt>

<span data-ttu-id="c85df-139">*byP2* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c85df-139">*byP2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c85df-140">Controle de seleção.</span><span class="sxs-lookup"><span data-stu-id="c85df-140">Selection control.</span></span>

</dd> <dt>

<span data-ttu-id="c85df-141">*pData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c85df-141">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c85df-142">Dados para a operação, se necessário; Senão, **NULL**.</span><span class="sxs-lookup"><span data-stu-id="c85df-142">Data for operation if needed; else, **NULL**.</span></span> <span data-ttu-id="c85df-143">Os tipos de dados que são passados nesse parâmetro incluem:</span><span class="sxs-lookup"><span data-stu-id="c85df-143">Types of data that are passed in this parameter include:</span></span>

-   <span data-ttu-id="c85df-144">ID do arquivo</span><span class="sxs-lookup"><span data-stu-id="c85df-144">file ID</span></span>
-   <span data-ttu-id="c85df-145">caminho do MF</span><span class="sxs-lookup"><span data-stu-id="c85df-145">path from the MF</span></span>
-   <span data-ttu-id="c85df-146">caminho do DF atual</span><span class="sxs-lookup"><span data-stu-id="c85df-146">path from the current DF</span></span>
-   <span data-ttu-id="c85df-147">Nome da DF</span><span class="sxs-lookup"><span data-stu-id="c85df-147">DF name</span></span>

</dd> <dt>

<span data-ttu-id="c85df-148">*lBytesToRead* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c85df-148">*lBytesToRead* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c85df-149">Empty (ou seja, 0) ou o comprimento máximo dos dados esperados em resposta.</span><span class="sxs-lookup"><span data-stu-id="c85df-149">Empty (that is, 0) or maximum length of data expected in response.</span></span>

</dd> <dt>

<span data-ttu-id="c85df-150">*ppCmd* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="c85df-150">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c85df-151">Na entrada, um ponteiro para um objeto de interface [**ISCardCmd**](iscardcmd.md) ou **nulo**.</span><span class="sxs-lookup"><span data-stu-id="c85df-151">On input, a pointer to an [**ISCardCmd**](iscardcmd.md) interface object or **NULL**.</span></span>

<span data-ttu-id="c85df-152">No retorno, ele é preenchido com o comando APDU construído por essa operação.</span><span class="sxs-lookup"><span data-stu-id="c85df-152">On return, it is filled with the APDU command constructed by this operation.</span></span> <span data-ttu-id="c85df-153">Se *ppCmd* foi definido como **NULL**, um objeto [**ISCardCmd**](iscardcmd.md) de [*cartão inteligente*](../secgloss/s-gly.md) será criado internamente e retornado por meio do ponteiro *ppCmd* .</span><span class="sxs-lookup"><span data-stu-id="c85df-153">If *ppCmd* was set to **NULL**, a [*smart card*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) object is internally created and returned via the *ppCmd* pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c85df-154">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c85df-154">Return value</span></span>

<span data-ttu-id="c85df-155">O método retorna um dos seguintes valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="c85df-155">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="c85df-156">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="c85df-156">Return code</span></span>                                                                                   | <span data-ttu-id="c85df-157">Descrição</span><span class="sxs-lookup"><span data-stu-id="c85df-157">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="c85df-158"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c85df-158"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="c85df-159">Operação concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="c85df-159">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="c85df-160"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="c85df-160"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="c85df-161">Parâmetro inválido.</span><span class="sxs-lookup"><span data-stu-id="c85df-161">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="c85df-162"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="c85df-162"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="c85df-163">Um ponteiro inadequado foi passado.</span><span class="sxs-lookup"><span data-stu-id="c85df-163">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="c85df-164"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="c85df-164"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="c85df-165">Sem memória.</span><span class="sxs-lookup"><span data-stu-id="c85df-165">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="c85df-166">Comentários</span><span class="sxs-lookup"><span data-stu-id="c85df-166">Remarks</span></span>

<span data-ttu-id="c85df-167">A menos que especificado de outra forma, a execução correta do comando encapsulado modifica o status de segurança de acordo com as seguintes regras:</span><span class="sxs-lookup"><span data-stu-id="c85df-167">Unless otherwise specified, the correct execution of the encapsulated command modifies the security status according to the following rules:</span></span>

-   <span data-ttu-id="c85df-168">Quando o arquivo elementar atual é alterado ou quando não há nenhum arquivo elementar atual, o status de segurança específico para um antigo arquivo elements atual é perdido.</span><span class="sxs-lookup"><span data-stu-id="c85df-168">When the current elementary file is changed, or when there is no current elementary file, the security status specific to a former current elementary file is lost.</span></span>
-   <span data-ttu-id="c85df-169">Quando o diretório de repositório de pasta atual (DF) é descendente ou é idêntico ao DF atual anterior, o status de segurança específico do DF atual antigo é perdido.</span><span class="sxs-lookup"><span data-stu-id="c85df-169">When the current filestore directory (DF) is descendant of, or identical to the former current DF, the security status specific to the former current DF is lost.</span></span> <span data-ttu-id="c85df-170">O status de segurança comum a todos os ancestrais comuns do DF atual e novo é mantido.</span><span class="sxs-lookup"><span data-stu-id="c85df-170">The security status common to all common ancestors of the previous and new current DF is maintained.</span></span>

<span data-ttu-id="c85df-171">Para obter uma lista de todos os métodos fornecidos por essa interface, consulte [**ISCardISO7816**](iscardiso7816.md).</span><span class="sxs-lookup"><span data-stu-id="c85df-171">For a list of all the methods provided by this interface, see [**ISCardISO7816**](iscardiso7816.md).</span></span>

<span data-ttu-id="c85df-172">Além dos códigos de erro COM listados acima, essa interface pode retornar um código de erro de cartão inteligente se uma função de cartão inteligente foi chamada para concluir a solicitação.</span><span class="sxs-lookup"><span data-stu-id="c85df-172">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="c85df-173">Para obter mais informações, consulte [valores de retorno de cartão inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="c85df-173">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c85df-174">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c85df-174">Requirements</span></span>



| <span data-ttu-id="c85df-175">Requisito</span><span class="sxs-lookup"><span data-stu-id="c85df-175">Requirement</span></span> | <span data-ttu-id="c85df-176">Valor</span><span class="sxs-lookup"><span data-stu-id="c85df-176">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c85df-177">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c85df-177">Minimum supported client</span></span><br/> | <span data-ttu-id="c85df-178">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="c85df-178">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="c85df-179">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c85df-179">Minimum supported server</span></span><br/> | <span data-ttu-id="c85df-180">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c85df-180">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c85df-181">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="c85df-181">End of client support</span></span><br/>    | <span data-ttu-id="c85df-182">Windows XP</span><span class="sxs-lookup"><span data-stu-id="c85df-182">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="c85df-183">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="c85df-183">End of server support</span></span><br/>    | <span data-ttu-id="c85df-184">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c85df-184">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="c85df-185">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c85df-185">Header</span></span><br/>                   | <dl> <span data-ttu-id="c85df-186"><dt>Scardssp. h</dt></span><span class="sxs-lookup"><span data-stu-id="c85df-186"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="c85df-187">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="c85df-187">Type library</span></span><br/>             | <dl> <span data-ttu-id="c85df-188"><dt>Scardsrv. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="c85df-188"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="c85df-189">DLL</span><span class="sxs-lookup"><span data-stu-id="c85df-189">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c85df-190"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c85df-190"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="c85df-191">IID</span><span class="sxs-lookup"><span data-stu-id="c85df-191">IID</span></span><br/>                      | <span data-ttu-id="c85df-192">IID \_ ISCardISO7816 é definido como 53B6AA68-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="c85df-192">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="c85df-193">Confira também</span><span class="sxs-lookup"><span data-stu-id="c85df-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c85df-194">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="c85df-194">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> </dl>

 

 
