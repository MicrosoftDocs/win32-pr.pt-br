---
description: O método PutData constrói um comando APDU (unidade de dados de protocolo de aplicativo) que armazena um único objeto de dados primitivos ou o conjunto de objetos de dados contidos em um objeto de dados construído, dependendo do arquivo selecionado.
ms.assetid: 6bad45fb-b202-4eb0-b2f4-fe0a6af64330
title: 'ISCardISO7816: método utData de:P (Scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.PutData
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 3c15239943a92067011011b6cedca191fa78c3a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829328"
---
# <a name="iscardiso7816putdata-method"></a><span data-ttu-id="a6868-103">ISCardISO7816: método utData de:P</span><span class="sxs-lookup"><span data-stu-id="a6868-103">ISCardISO7816::PutData method</span></span>

<span data-ttu-id="a6868-104">\[O método **PutData** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="a6868-104">\[The **PutData** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="a6868-105">Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="a6868-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="a6868-106">Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="a6868-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="a6868-107">O método **PutData** constrói um comando APDU ( [*unidade de dados de protocolo de aplicativo*](../secgloss/a-gly.md) ) que armazena um único objeto de dados primitivos ou o conjunto de objetos de dados contidos em um objeto de dados construído, dependendo do arquivo selecionado.</span><span class="sxs-lookup"><span data-stu-id="a6868-107">The **PutData** method constructs an [*application protocol data unit*](../secgloss/a-gly.md) (APDU) command that stores a single primitive data object or the set of data objects contained in a constructed data object, depending on the file selected.</span></span>

<span data-ttu-id="a6868-108">A forma como os objetos são armazenados (gravar uma vez e/ou atualizar e/ou acrescentar) depende da definição ou da natureza dos objetos de dados.</span><span class="sxs-lookup"><span data-stu-id="a6868-108">How the objects are stored (writing once and/or updating and/or appending) depends on the definition or the nature of the data objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6868-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a6868-109">Syntax</span></span>


```C++
HRESULT PutData(
  [in]      BYTE         byP1,
  [in]      BYTE         byP2,
  [in]      LPBYTEBUFFER pData,
  [in, out] LPSCARDCMD   *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="a6868-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a6868-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6868-111">*byP1* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a6868-111">*byP1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a6868-112">Codificação de P1-P2.</span><span class="sxs-lookup"><span data-stu-id="a6868-112">Coding of P1-P2.</span></span>



| <span data-ttu-id="a6868-113">Valor</span><span class="sxs-lookup"><span data-stu-id="a6868-113">Value</span></span>                                                                                  | <span data-ttu-id="a6868-114">Significado</span><span class="sxs-lookup"><span data-stu-id="a6868-114">Meaning</span></span>                                          |
|----------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="a6868-115"><dt>0000-003F</dt></span><span class="sxs-lookup"><span data-stu-id="a6868-115"><dt>0000 - 003F</dt></span></span> </dl> | <span data-ttu-id="a6868-116">RFU</span><span class="sxs-lookup"><span data-stu-id="a6868-116">RFU</span></span><br/>                                   |
| <dl> <span data-ttu-id="a6868-117"><dt>0040-00FF</dt></span><span class="sxs-lookup"><span data-stu-id="a6868-117"><dt>0040 - 00FF</dt></span></span> </dl> | <span data-ttu-id="a6868-118">BER – marca TLV (1 byte) em P2</span><span class="sxs-lookup"><span data-stu-id="a6868-118">BER-TLV tag (1 byte) in P2</span></span><br/>            |
| <dl> <span data-ttu-id="a6868-119"><dt>0100-01FF</dt></span><span class="sxs-lookup"><span data-stu-id="a6868-119"><dt>0100 - 01FF</dt></span></span> </dl> | <span data-ttu-id="a6868-120">Dados de aplicativo (codificação proprietária)</span><span class="sxs-lookup"><span data-stu-id="a6868-120">Application data (proprietary coding)</span></span><br/> |
| <dl> <span data-ttu-id="a6868-121"><dt>0200-02FF</dt></span><span class="sxs-lookup"><span data-stu-id="a6868-121"><dt>0200 - 02FF</dt></span></span> </dl> | <span data-ttu-id="a6868-122">Marca de TLV simples em P2</span><span class="sxs-lookup"><span data-stu-id="a6868-122">SIMPLE-TLV tag in P2</span></span><br/>                  |
| <dl> <span data-ttu-id="a6868-123"><dt>0300-03FF</dt></span><span class="sxs-lookup"><span data-stu-id="a6868-123"><dt>0300 - 03FF</dt></span></span> </dl> | <span data-ttu-id="a6868-124">RFU</span><span class="sxs-lookup"><span data-stu-id="a6868-124">RFU</span></span><br/>                                   |
| <dl> <span data-ttu-id="a6868-125"><dt>0400 - 04FF</dt></span><span class="sxs-lookup"><span data-stu-id="a6868-125"><dt>0400 - 04FF</dt></span></span> </dl> | <span data-ttu-id="a6868-126">BER-TLV marca (2 bytes) em P1-P2</span><span class="sxs-lookup"><span data-stu-id="a6868-126">BER-TLV tag (2 bytes) in P1-P2</span></span><br/>        |



 

</dd> <dt>

<span data-ttu-id="a6868-127">*byP2* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a6868-127">*byP2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a6868-128">Codificação de P1-P2.</span><span class="sxs-lookup"><span data-stu-id="a6868-128">Coding of P1-P2.</span></span>



| <span data-ttu-id="a6868-129">Valor</span><span class="sxs-lookup"><span data-stu-id="a6868-129">Value</span></span>                                                                                  | <span data-ttu-id="a6868-130">Significado</span><span class="sxs-lookup"><span data-stu-id="a6868-130">Meaning</span></span>                                          |
|----------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="a6868-131"><dt>0000-003F</dt></span><span class="sxs-lookup"><span data-stu-id="a6868-131"><dt>0000 - 003F</dt></span></span> </dl> | <span data-ttu-id="a6868-132">RFU</span><span class="sxs-lookup"><span data-stu-id="a6868-132">RFU</span></span><br/>                                   |
| <dl> <span data-ttu-id="a6868-133"><dt>0040-00FF</dt></span><span class="sxs-lookup"><span data-stu-id="a6868-133"><dt>0040 - 00FF</dt></span></span> </dl> | <span data-ttu-id="a6868-134">BER – marca TLV (1 byte) em P2</span><span class="sxs-lookup"><span data-stu-id="a6868-134">BER-TLV tag (1 byte) in P2</span></span><br/>            |
| <dl> <span data-ttu-id="a6868-135"><dt>0100-01FF</dt></span><span class="sxs-lookup"><span data-stu-id="a6868-135"><dt>0100 - 01FF</dt></span></span> </dl> | <span data-ttu-id="a6868-136">Dados de aplicativo (codificação proprietária)</span><span class="sxs-lookup"><span data-stu-id="a6868-136">Application data (proprietary coding)</span></span><br/> |
| <dl> <span data-ttu-id="a6868-137"><dt>0200-02FF</dt></span><span class="sxs-lookup"><span data-stu-id="a6868-137"><dt>0200 - 02FF</dt></span></span> </dl> | <span data-ttu-id="a6868-138">Marca de TLV simples em P2</span><span class="sxs-lookup"><span data-stu-id="a6868-138">SIMPLE-TLV tag in P2</span></span><br/>                  |
| <dl> <span data-ttu-id="a6868-139"><dt>0300-03FF</dt></span><span class="sxs-lookup"><span data-stu-id="a6868-139"><dt>0300 - 03FF</dt></span></span> </dl> | <span data-ttu-id="a6868-140">RFU</span><span class="sxs-lookup"><span data-stu-id="a6868-140">RFU</span></span><br/>                                   |
| <dl> <span data-ttu-id="a6868-141"><dt>0400 - 04FF</dt></span><span class="sxs-lookup"><span data-stu-id="a6868-141"><dt>0400 - 04FF</dt></span></span> </dl> | <span data-ttu-id="a6868-142">BER-TLV marca (2 bytes) em P1-P2</span><span class="sxs-lookup"><span data-stu-id="a6868-142">BER-TLV tag (2 bytes) in P1-P2</span></span><br/>        |



 

</dd> <dt>

<span data-ttu-id="a6868-143">*pData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a6868-143">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a6868-144">Ponteiro para um buffer de bytes que contém os parâmetros e os dados a serem gravados.</span><span class="sxs-lookup"><span data-stu-id="a6868-144">Pointer to a byte buffer that contains the parameters and data to be written.</span></span>

</dd> <dt>

<span data-ttu-id="a6868-145">*ppCmd* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="a6868-145">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a6868-146">Na entrada, um ponteiro para um objeto de interface [**ISCardCmd**](iscardcmd.md) ou **nulo**.</span><span class="sxs-lookup"><span data-stu-id="a6868-146">On input, a pointer to an [**ISCardCmd**](iscardcmd.md) interface object or **NULL**.</span></span>

<span data-ttu-id="a6868-147">No retorno, ele é preenchido com o comando APDU construído por essa operação.</span><span class="sxs-lookup"><span data-stu-id="a6868-147">On return, it is filled with the APDU command constructed by this operation.</span></span> <span data-ttu-id="a6868-148">Se *ppCmd* foi definido como **NULL**, um objeto [**ISCardCmd**](iscardcmd.md) de [*cartão inteligente*](../secgloss/s-gly.md) será criado internamente e retornado usando o ponteiro *ppCmd* .</span><span class="sxs-lookup"><span data-stu-id="a6868-148">If *ppCmd* was set to **NULL**, a [*smart card*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) object is internally created and returned using the *ppCmd* pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a6868-149">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a6868-149">Return value</span></span>

<span data-ttu-id="a6868-150">O método retorna um dos seguintes valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="a6868-150">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="a6868-151">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="a6868-151">Return code</span></span>                                                                                   | <span data-ttu-id="a6868-152">Description</span><span class="sxs-lookup"><span data-stu-id="a6868-152">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="a6868-153"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a6868-153"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="a6868-154">Operação concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="a6868-154">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="a6868-155"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="a6868-155"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="a6868-156">Parâmetro inválido.</span><span class="sxs-lookup"><span data-stu-id="a6868-156">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="a6868-157"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="a6868-157"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="a6868-158">Um ponteiro inadequado foi passado.</span><span class="sxs-lookup"><span data-stu-id="a6868-158">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="a6868-159"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="a6868-159"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="a6868-160">Sem memória.</span><span class="sxs-lookup"><span data-stu-id="a6868-160">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="a6868-161">Comentários</span><span class="sxs-lookup"><span data-stu-id="a6868-161">Remarks</span></span>

<span data-ttu-id="a6868-162">O comando só poderá ser executado se o status de segurança satisfizer as condições de segurança definidas pelo aplicativo no [*contexto*](../secgloss/c-gly.md) para a função.</span><span class="sxs-lookup"><span data-stu-id="a6868-162">The command can be performed only if the security status satisfies the security conditions defined by the application within the [*context*](../secgloss/c-gly.md) for the function.</span></span>

<dl> <dt>

<span data-ttu-id="a6868-163"><span id="Store_Application_Data"></span><span id="store_application_data"></span><span id="STORE_APPLICATION_DATA"></span>Armazenar dados de aplicativos</span><span class="sxs-lookup"><span data-stu-id="a6868-163"><span id="Store_Application_Data"></span><span id="store_application_data"></span><span id="STORE_APPLICATION_DATA"></span>Store Application Data</span></span>
</dt> <dd>

<span data-ttu-id="a6868-164">Quando o valor P1-P2 está no intervalo de 0100 a 01FF, o valor de P1-P2 deve ser um identificador reservado para testes internos de cartão e para serviços proprietários significativos em um determinado contexto de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a6868-164">When the value of P1-P2 lies in the range from 0100 to 01FF, the value of P1-P2 shall be an identifier reserved for card internal tests and for proprietary services meaningful within a given application context.</span></span>

</dd> <dt>

<span data-ttu-id="a6868-165"><span id="Store_Data_Objects"></span><span id="store_data_objects"></span><span id="STORE_DATA_OBJECTS"></span>Armazenar objetos de dados</span><span class="sxs-lookup"><span data-stu-id="a6868-165"><span id="Store_Data_Objects"></span><span id="store_data_objects"></span><span id="STORE_DATA_OBJECTS"></span>Store Data Objects</span></span>
</dt> <dd>

<span data-ttu-id="a6868-166">Quando o valor P1-P2 está no intervalo de 0040 a 00FF, o valor de P2 deve ser uma marca BER-TLV em um único byte.</span><span class="sxs-lookup"><span data-stu-id="a6868-166">When the value P1-P2 lies in the range from 0040 to 00FF, the value of P2 shall be a BER-TLV tag on a single byte.</span></span> <span data-ttu-id="a6868-167">O valor de 00FF é reservado para indicar que o campo de dados transporta objetos de dados BER-TLV.</span><span class="sxs-lookup"><span data-stu-id="a6868-167">The value of 00FF is reserved for indicating that the data field carries BER-TLV data objects.</span></span>

<span data-ttu-id="a6868-168">Quando o valor de P1-P2 está no intervalo de 0200 a 02FF, o valor de P2 deve ser uma marca de TLV simples.</span><span class="sxs-lookup"><span data-stu-id="a6868-168">When the value of P1-P2 lies in the range 0200 to 02FF, the value of P2 shall be a SIMPLE-TLV tag.</span></span> <span data-ttu-id="a6868-169">O valor 0200 é RFU.</span><span class="sxs-lookup"><span data-stu-id="a6868-169">The value 0200 is RFU.</span></span> <span data-ttu-id="a6868-170">O valor 02FF é reservado para indicar que o campo de dados contém objetos de dados de TLV simples.</span><span class="sxs-lookup"><span data-stu-id="a6868-170">The value 02FF is reserved for indicating that the data field carries SIMPLE-TLV data objects.</span></span>

<span data-ttu-id="a6868-171">Quando o valor de P1-P2 estiver no intervalo de 4000 a FFFF, o valor de P1-P2 deverá ser uma marca BER-TLV em dois bytes.</span><span class="sxs-lookup"><span data-stu-id="a6868-171">When the value of P1-P2 lies in the range from 4000 to FFFF, the value of P1-P2 shall be a BER-TLV tag on two bytes.</span></span> <span data-ttu-id="a6868-172">Os valores de 4000 a FFFF são RFU.</span><span class="sxs-lookup"><span data-stu-id="a6868-172">The values 4000 to FFFF are RFU.</span></span>

<span data-ttu-id="a6868-173">Quando um objeto de dados primitivo é fornecido, o campo de dados da mensagem de comando deve conter o valor do objeto de dados primitivo correspondente.</span><span class="sxs-lookup"><span data-stu-id="a6868-173">When a primitive data object is provided, the data field of the command message shall contain the value of the corresponding primitive data object.</span></span>

<span data-ttu-id="a6868-174">Quando um objeto de dados construído é fornecido, o campo de dados da mensagem de comando deve conter o valor do objeto de dados construído (ou seja, objetos de dados incluindo sua marca, comprimento e valor).</span><span class="sxs-lookup"><span data-stu-id="a6868-174">When a constructed data object is provided, the data field of the command message shall contain the value of the constructed data object (that is, data objects including their tag, length, and value).</span></span>

</dd> </dl>

<span data-ttu-id="a6868-175">Para obter uma lista de todos os métodos fornecidos por essa interface, consulte [**ISCardISO7816**](iscardiso7816.md).</span><span class="sxs-lookup"><span data-stu-id="a6868-175">For a list of all the methods provided by this interface, see [**ISCardISO7816**](iscardiso7816.md).</span></span>

<span data-ttu-id="a6868-176">Além dos códigos de erro COM listados acima, essa interface pode retornar um código de erro de cartão inteligente se uma função de cartão inteligente foi chamada para concluir a solicitação.</span><span class="sxs-lookup"><span data-stu-id="a6868-176">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="a6868-177">Para obter mais informações, consulte [valores de retorno de cartão inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="a6868-177">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a6868-178">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a6868-178">Requirements</span></span>



| <span data-ttu-id="a6868-179">Requisito</span><span class="sxs-lookup"><span data-stu-id="a6868-179">Requirement</span></span> | <span data-ttu-id="a6868-180">Valor</span><span class="sxs-lookup"><span data-stu-id="a6868-180">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a6868-181">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a6868-181">Minimum supported client</span></span><br/> | <span data-ttu-id="a6868-182">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="a6868-182">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="a6868-183">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a6868-183">Minimum supported server</span></span><br/> | <span data-ttu-id="a6868-184">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a6868-184">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a6868-185">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="a6868-185">End of client support</span></span><br/>    | <span data-ttu-id="a6868-186">Windows XP</span><span class="sxs-lookup"><span data-stu-id="a6868-186">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="a6868-187">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="a6868-187">End of server support</span></span><br/>    | <span data-ttu-id="a6868-188">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a6868-188">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="a6868-189">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a6868-189">Header</span></span><br/>                   | <dl> <span data-ttu-id="a6868-190"><dt>Scardssp. h</dt></span><span class="sxs-lookup"><span data-stu-id="a6868-190"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="a6868-191">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="a6868-191">Type library</span></span><br/>             | <dl> <span data-ttu-id="a6868-192"><dt>Scardsrv. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="a6868-192"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="a6868-193">DLL</span><span class="sxs-lookup"><span data-stu-id="a6868-193">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a6868-194"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a6868-194"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="a6868-195">IID</span><span class="sxs-lookup"><span data-stu-id="a6868-195">IID</span></span><br/>                      | <span data-ttu-id="a6868-196">IID \_ ISCardISO7816 é definido como 53B6AA68-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="a6868-196">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="a6868-197">Confira também</span><span class="sxs-lookup"><span data-stu-id="a6868-197">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6868-198">**GetData**</span><span class="sxs-lookup"><span data-stu-id="a6868-198">**GetData**</span></span>](iscardiso7816-getdata.md)
</dt> <dt>

[<span data-ttu-id="a6868-199">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="a6868-199">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> </dl>

 

 
