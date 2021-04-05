---
description: O método GetData constrói um comando APDU (unidade de dados de protocolo de aplicativo) que recupera um único objeto de dados primitivos ou um conjunto de objetos de dados (contidos em um objeto de dados construído), dependendo do tipo de arquivo selecionado.
ms.assetid: d764a765-f451-4bf7-9d06-f5901062dcac
title: 'Método ISCardISO7816:: GetData (Scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.GetData
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 93dca04daa50e068a68dc62cf11a580eb8e3b1c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662687"
---
# <a name="iscardiso7816getdata-method"></a><span data-ttu-id="80413-103">Método ISCardISO7816:: GetData</span><span class="sxs-lookup"><span data-stu-id="80413-103">ISCardISO7816::GetData method</span></span>

<span data-ttu-id="80413-104">\[O método **GetData** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="80413-104">\[The **GetData** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="80413-105">Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="80413-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="80413-106">Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="80413-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="80413-107">O método **GetData** constrói um comando APDU ( [*unidade de dados de protocolo de aplicativo*](../secgloss/a-gly.md) ) que recupera um único objeto de dados primitivos ou um conjunto de objetos de dados (contidos em um objeto de dados construído), dependendo do tipo de arquivo selecionado.</span><span class="sxs-lookup"><span data-stu-id="80413-107">The **GetData** method constructs an [*application protocol data unit*](../secgloss/a-gly.md) (APDU) command that retrieves either a single primitive data object or a set of data objects (contained in a constructed data object), depending on the type of file selected.</span></span>

## <a name="syntax"></a><span data-ttu-id="80413-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="80413-108">Syntax</span></span>


```C++
HRESULT GetData(
  [in]      BYTE       byP1,
  [in]      BYTE       byP2,
  [in]      LONG       lBytesToGet,
  [in, out] LPSCARDCMD *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="80413-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="80413-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80413-110">*byP1* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="80413-110">*byP1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80413-111">Parâmetros.</span><span class="sxs-lookup"><span data-stu-id="80413-111">Parameters.</span></span>



| <span data-ttu-id="80413-112">Valor</span><span class="sxs-lookup"><span data-stu-id="80413-112">Value</span></span>                                                                                  | <span data-ttu-id="80413-113">Significado</span><span class="sxs-lookup"><span data-stu-id="80413-113">Meaning</span></span>                                          |
|----------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="80413-114"><dt>0000-003F</dt></span><span class="sxs-lookup"><span data-stu-id="80413-114"><dt>0000 - 003F</dt></span></span> </dl> | <span data-ttu-id="80413-115">RFU</span><span class="sxs-lookup"><span data-stu-id="80413-115">RFU</span></span><br/>                                   |
| <dl> <span data-ttu-id="80413-116"><dt>0040-00FF</dt></span><span class="sxs-lookup"><span data-stu-id="80413-116"><dt>0040 - 00FF</dt></span></span> </dl> | <span data-ttu-id="80413-117">BER – marca TLV (1 byte) em P2</span><span class="sxs-lookup"><span data-stu-id="80413-117">BER-TLV tag (1 byte) in P2</span></span><br/>            |
| <dl> <span data-ttu-id="80413-118"><dt>0100-01FF</dt></span><span class="sxs-lookup"><span data-stu-id="80413-118"><dt>0100 - 01FF</dt></span></span> </dl> | <span data-ttu-id="80413-119">Dados de aplicativo (codificação proprietária)</span><span class="sxs-lookup"><span data-stu-id="80413-119">Application data (proprietary coding)</span></span><br/> |
| <dl> <span data-ttu-id="80413-120"><dt>0200-02FF</dt></span><span class="sxs-lookup"><span data-stu-id="80413-120"><dt>0200 - 02FF</dt></span></span> </dl> | <span data-ttu-id="80413-121">Marca de TLV simples em P2</span><span class="sxs-lookup"><span data-stu-id="80413-121">SIMPLE-TLV tag in P2</span></span><br/>                  |
| <dl> <span data-ttu-id="80413-122"><dt>0300-03FF</dt></span><span class="sxs-lookup"><span data-stu-id="80413-122"><dt>0300 - 03FF</dt></span></span> </dl> | <span data-ttu-id="80413-123">RFU</span><span class="sxs-lookup"><span data-stu-id="80413-123">RFU</span></span><br/>                                   |
| <dl> <span data-ttu-id="80413-124"><dt>0400 - 04FF</dt></span><span class="sxs-lookup"><span data-stu-id="80413-124"><dt>0400 - 04FF</dt></span></span> </dl> | <span data-ttu-id="80413-125">BER-TLV marca (2 bytes) em P1-P2</span><span class="sxs-lookup"><span data-stu-id="80413-125">BER-TLV tag (2 bytes) in P1-P2</span></span><br/>        |



 

</dd> <dt>

<span data-ttu-id="80413-126">*byP2* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="80413-126">*byP2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80413-127">Parâmetros.</span><span class="sxs-lookup"><span data-stu-id="80413-127">Parameters.</span></span>



| <span data-ttu-id="80413-128">Valor</span><span class="sxs-lookup"><span data-stu-id="80413-128">Value</span></span>                                                                                  | <span data-ttu-id="80413-129">Significado</span><span class="sxs-lookup"><span data-stu-id="80413-129">Meaning</span></span>                                          |
|----------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="80413-130"><dt>0000-003F</dt></span><span class="sxs-lookup"><span data-stu-id="80413-130"><dt>0000 - 003F</dt></span></span> </dl> | <span data-ttu-id="80413-131">RFU</span><span class="sxs-lookup"><span data-stu-id="80413-131">RFU</span></span><br/>                                   |
| <dl> <span data-ttu-id="80413-132"><dt>0040-00FF</dt></span><span class="sxs-lookup"><span data-stu-id="80413-132"><dt>0040 - 00FF</dt></span></span> </dl> | <span data-ttu-id="80413-133">BER – marca TLV (1 byte) em P2</span><span class="sxs-lookup"><span data-stu-id="80413-133">BER-TLV tag (1 byte) in P2</span></span><br/>            |
| <dl> <span data-ttu-id="80413-134"><dt>0100-01FF</dt></span><span class="sxs-lookup"><span data-stu-id="80413-134"><dt>0100 - 01FF</dt></span></span> </dl> | <span data-ttu-id="80413-135">Dados de aplicativo (codificação proprietária)</span><span class="sxs-lookup"><span data-stu-id="80413-135">Application data (proprietary coding)</span></span><br/> |
| <dl> <span data-ttu-id="80413-136"><dt>0200-02FF</dt></span><span class="sxs-lookup"><span data-stu-id="80413-136"><dt>0200 - 02FF</dt></span></span> </dl> | <span data-ttu-id="80413-137">Marca de TLV simples em P2</span><span class="sxs-lookup"><span data-stu-id="80413-137">SIMPLE-TLV tag in P2</span></span><br/>                  |
| <dl> <span data-ttu-id="80413-138"><dt>0300-03FF</dt></span><span class="sxs-lookup"><span data-stu-id="80413-138"><dt>0300 - 03FF</dt></span></span> </dl> | <span data-ttu-id="80413-139">RFU</span><span class="sxs-lookup"><span data-stu-id="80413-139">RFU</span></span><br/>                                   |
| <dl> <span data-ttu-id="80413-140"><dt>0400 - 04FF</dt></span><span class="sxs-lookup"><span data-stu-id="80413-140"><dt>0400 - 04FF</dt></span></span> </dl> | <span data-ttu-id="80413-141">BER-TLV marca (2 bytes) em P1-P2</span><span class="sxs-lookup"><span data-stu-id="80413-141">BER-TLV tag (2 bytes) in P1-P2</span></span><br/>        |



 

</dd> <dt>

<span data-ttu-id="80413-142">*lBytesToGet* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="80413-142">*lBytesToGet* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80413-143">Número de bytes esperados na resposta.</span><span class="sxs-lookup"><span data-stu-id="80413-143">Number of bytes expected in the response.</span></span>

</dd> <dt>

<span data-ttu-id="80413-144">*ppCmd* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="80413-144">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="80413-145">Na entrada, um ponteiro para um objeto de interface [**ISCardCmd**](iscardcmd.md) ou **nulo**.</span><span class="sxs-lookup"><span data-stu-id="80413-145">On input, a pointer to an [**ISCardCmd**](iscardcmd.md) interface object or **NULL**.</span></span>

<span data-ttu-id="80413-146">No retorno, ele é preenchido com o comando APDU construído por essa operação.</span><span class="sxs-lookup"><span data-stu-id="80413-146">On return, it is filled with the APDU command constructed by this operation.</span></span> <span data-ttu-id="80413-147">Se *ppCmd* foi definido como **NULL**, um objeto [**ISCardCmd**](iscardcmd.md) de [*cartão inteligente*](../secgloss/s-gly.md) será criado internamente e retornado usando o ponteiro *ppCmd* .</span><span class="sxs-lookup"><span data-stu-id="80413-147">If *ppCmd* was set to **NULL**, a [*smart card*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) object is internally created and returned using the *ppCmd* pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="80413-148">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="80413-148">Return value</span></span>

<span data-ttu-id="80413-149">O método retorna um dos seguintes valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="80413-149">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="80413-150">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="80413-150">Return code</span></span>                                                                                   | <span data-ttu-id="80413-151">Descrição</span><span class="sxs-lookup"><span data-stu-id="80413-151">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="80413-152"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="80413-152"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="80413-153">Operação concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="80413-153">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="80413-154"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="80413-154"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="80413-155">Parâmetro inválido.</span><span class="sxs-lookup"><span data-stu-id="80413-155">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="80413-156"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="80413-156"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="80413-157">Um ponteiro inadequado foi passado.</span><span class="sxs-lookup"><span data-stu-id="80413-157">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="80413-158"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="80413-158"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="80413-159">Sem memória.</span><span class="sxs-lookup"><span data-stu-id="80413-159">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="80413-160">Comentários</span><span class="sxs-lookup"><span data-stu-id="80413-160">Remarks</span></span>

<span data-ttu-id="80413-161">O comando encapsulado só poderá ser executado se o status de segurança do [*cartão inteligente*](../secgloss/s-gly.md) satisfizer os atributos de segurança do arquivo elementar que está sendo lido.</span><span class="sxs-lookup"><span data-stu-id="80413-161">The encapsulated command can only be performed if the security status of the [*smart card*](../secgloss/s-gly.md) satisfies the security attributes of the elementary file being read.</span></span> <span data-ttu-id="80413-162">As condições de segurança são dependentes da política do cartão e podem ser manipuladas por meio de [**ExternalAuthenticate**](iscardiso7816-externalauthenticate.md), [**InternalAuthenticate**](iscardiso7816-internalauthenticate.md), [**ISCardAuth**](iscardauth.md)e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="80413-162">Security conditions are dependent on the policy of the card, and may be manipulated through [**ExternalAuthenticate**](iscardiso7816-externalauthenticate.md), [**InternalAuthenticate**](iscardiso7816-internalauthenticate.md), [**ISCardAuth**](iscardauth.md), and so on.</span></span>

<span data-ttu-id="80413-163">Para selecionar um arquivo, chame [**selectfile**](iscardiso7816-selectfile.md).</span><span class="sxs-lookup"><span data-stu-id="80413-163">To select a file, call [**SelectFile**](iscardiso7816-selectfile.md).</span></span>

<span data-ttu-id="80413-164">Para obter uma lista de todos os métodos fornecidos por essa interface, consulte [**ISCardISO7816**](iscardiso7816.md).</span><span class="sxs-lookup"><span data-stu-id="80413-164">For a list of all the methods provided by this interface, see [**ISCardISO7816**](iscardiso7816.md).</span></span>

<span data-ttu-id="80413-165">Além dos códigos de erro COM listados acima, essa interface pode retornar um código de erro de cartão inteligente se uma função de cartão inteligente foi chamada para concluir a solicitação.</span><span class="sxs-lookup"><span data-stu-id="80413-165">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="80413-166">Para obter mais informações, consulte [valores de retorno de cartão inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="80413-166">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="80413-167">Requisitos</span><span class="sxs-lookup"><span data-stu-id="80413-167">Requirements</span></span>



| <span data-ttu-id="80413-168">Requisito</span><span class="sxs-lookup"><span data-stu-id="80413-168">Requirement</span></span> | <span data-ttu-id="80413-169">Valor</span><span class="sxs-lookup"><span data-stu-id="80413-169">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="80413-170">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="80413-170">Minimum supported client</span></span><br/> | <span data-ttu-id="80413-171">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="80413-171">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="80413-172">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="80413-172">Minimum supported server</span></span><br/> | <span data-ttu-id="80413-173">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="80413-173">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="80413-174">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="80413-174">End of client support</span></span><br/>    | <span data-ttu-id="80413-175">Windows XP</span><span class="sxs-lookup"><span data-stu-id="80413-175">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="80413-176">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="80413-176">End of server support</span></span><br/>    | <span data-ttu-id="80413-177">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="80413-177">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="80413-178">parâmetro</span><span class="sxs-lookup"><span data-stu-id="80413-178">Header</span></span><br/>                   | <dl> <span data-ttu-id="80413-179"><dt>Scardssp. h</dt></span><span class="sxs-lookup"><span data-stu-id="80413-179"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="80413-180">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="80413-180">Type library</span></span><br/>             | <dl> <span data-ttu-id="80413-181"><dt>Scardsrv. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="80413-181"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="80413-182">DLL</span><span class="sxs-lookup"><span data-stu-id="80413-182">DLL</span></span><br/>                      | <dl> <span data-ttu-id="80413-183"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="80413-183"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="80413-184">IID</span><span class="sxs-lookup"><span data-stu-id="80413-184">IID</span></span><br/>                      | <span data-ttu-id="80413-185">IID \_ ISCardISO7816 é definido como 53B6AA68-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="80413-185">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="80413-186">Confira também</span><span class="sxs-lookup"><span data-stu-id="80413-186">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80413-187">**ExternalAuthenticate**</span><span class="sxs-lookup"><span data-stu-id="80413-187">**ExternalAuthenticate**</span></span>](iscardiso7816-externalauthenticate.md)
</dt> <dt>

[<span data-ttu-id="80413-188">**InternalAuthenticate**</span><span class="sxs-lookup"><span data-stu-id="80413-188">**InternalAuthenticate**</span></span>](iscardiso7816-internalauthenticate.md)
</dt> <dt>

[<span data-ttu-id="80413-189">**ISCardAuth**</span><span class="sxs-lookup"><span data-stu-id="80413-189">**ISCardAuth**</span></span>](iscardauth.md)
</dt> <dt>

[<span data-ttu-id="80413-190">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="80413-190">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> <dt>

[<span data-ttu-id="80413-191">**PutData**</span><span class="sxs-lookup"><span data-stu-id="80413-191">**PutData**</span></span>](iscardiso7816-putdata.md)
</dt> <dt>

[<span data-ttu-id="80413-192">**Selecionarfile**</span><span class="sxs-lookup"><span data-stu-id="80413-192">**SelectFile**</span></span>](iscardiso7816-selectfile.md)
</dt> </dl>

 

 
