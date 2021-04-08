---
description: O método ManageChannel constrói um comando APDU (unidade de dados de protocolo de aplicativo) que abre e fecha canais lógicos.
ms.assetid: a55b5b3f-0404-45bd-afeb-e96173319a50
title: 'Método ISCardISO7816:: ManageChannel (Scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.ManageChannel
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: f0b9af92e280781405c2cb570c93e8873a279765
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010826"
---
# <a name="iscardiso7816managechannel-method"></a><span data-ttu-id="e5884-103">Método ISCardISO7816:: ManageChannel</span><span class="sxs-lookup"><span data-stu-id="e5884-103">ISCardISO7816::ManageChannel method</span></span>

<span data-ttu-id="e5884-104">\[O método **ManageChannel** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="e5884-104">\[The **ManageChannel** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="e5884-105">Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="e5884-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="e5884-106">Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="e5884-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="e5884-107">O método **ManageChannel** constrói um comando APDU ( [*unidade de dados de protocolo de aplicativo*](../secgloss/a-gly.md) ) que abre e fecha canais lógicos.</span><span class="sxs-lookup"><span data-stu-id="e5884-107">The **ManageChannel** method constructs an [*application protocol data unit*](../secgloss/a-gly.md) (APDU) command that opens and closes logical channels.</span></span>

<span data-ttu-id="e5884-108">A função abrir abre um novo canal lógico diferente do básico.</span><span class="sxs-lookup"><span data-stu-id="e5884-108">The open function opens a new logical channel other than the basic one.</span></span> <span data-ttu-id="e5884-109">As opções são fornecidas para o cartão atribuir um número de canal lógico ou para o número de canal lógico a ser fornecido ao cartão.</span><span class="sxs-lookup"><span data-stu-id="e5884-109">Options are provided for the card to assign a logical channel number, or for the logical channel number to be supplied to the card.</span></span>

<span data-ttu-id="e5884-110">A função close fecha explicitamente um canal lógico diferente do básico.</span><span class="sxs-lookup"><span data-stu-id="e5884-110">The close function explicitly closes a logical channel other than the basic one.</span></span> <span data-ttu-id="e5884-111">Após o fechamento bem-sucedido, o canal lógico deverá estar disponível para reutilização.</span><span class="sxs-lookup"><span data-stu-id="e5884-111">After the successful closing, the logical channel shall be available for re-use.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5884-112">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e5884-112">Syntax</span></span>


```C++
HRESULT ManageChannel(
  [in]      BYTE       byChannelState,
  [in]      BYTE       byChannel,
  [in, out] LPSCARDCMD *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="e5884-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e5884-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5884-114">*byChannelState* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e5884-114">*byChannelState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5884-115">O bit B8 de P1 é usado para indicar a função Open ou a função close; se B8 for 0, o canal de gerenciamento deverá abrir um canal lógico e, se B8 for 1, o canal de gerenciamento deverá fechar um canal lógico:</span><span class="sxs-lookup"><span data-stu-id="e5884-115">Bit b8 of P1 is used to indicate the open function or the close function; if b8 is 0, then MANAGE CHANNEL shall open a logical channel and if b8 is 1, then MANAGE CHANNEL shall close a logical channel:</span></span>

<span data-ttu-id="e5884-116">P1 = ' 00 ' para abrir</span><span class="sxs-lookup"><span data-stu-id="e5884-116">P1 = '00' to open</span></span>

<span data-ttu-id="e5884-117">P1 = ' 80 ' para fechar</span><span class="sxs-lookup"><span data-stu-id="e5884-117">P1 = '80' to close</span></span>

<span data-ttu-id="e5884-118">Outros valores são RFU</span><span class="sxs-lookup"><span data-stu-id="e5884-118">Other values are RFU</span></span>

</dd> <dt>

<span data-ttu-id="e5884-119">*byChannel* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e5884-119">*byChannel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5884-120">Para a função Open (P1 = ' 00 '), os bits B1 e B2 de P2 são usados para codificar o número de canal lógico da mesma maneira que no byte de classe, os outros bits de P2 são RFU.</span><span class="sxs-lookup"><span data-stu-id="e5884-120">For the open function (P1 = '00'), the bits b1 and b2 of P2 are used to code the logical channel number in the same manner as in the class byte, the other bits of P2 are RFU.</span></span>

<span data-ttu-id="e5884-121">Quando B1 e B2 de P2 forem **nulas**, o cartão atribuirá um número de canal lógico que será retornado em bits B1 e B2 do campo de dados.</span><span class="sxs-lookup"><span data-stu-id="e5884-121">When b1 and b2 of P2 are **NULL**, then the card will assign a logical channel number that will be returned in bits b1 and b2 of the data field.</span></span>

<span data-ttu-id="e5884-122">Quando B1 e/ou B2 de P2 não são **nulas**, eles codificam um número de canal lógico diferente do básico; em seguida, o cartão abrirá o número de canal lógico atribuído externamente.</span><span class="sxs-lookup"><span data-stu-id="e5884-122">When b1 and/or b2 of P2 are not **NULL**, they code a logical channel number other than the basic one; then the card will open the externally assigned logical channel number.</span></span>

</dd> <dt>

<span data-ttu-id="e5884-123">*ppCmd* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="e5884-123">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e5884-124">Na entrada, um ponteiro para um objeto de interface [**ISCardCmd**](iscardcmd.md) ou **nulo**.</span><span class="sxs-lookup"><span data-stu-id="e5884-124">On input, a pointer to an [**ISCardCmd**](iscardcmd.md) interface object or **NULL**.</span></span>

<span data-ttu-id="e5884-125">No retorno, ele é preenchido com o comando APDU construído por essa operação.</span><span class="sxs-lookup"><span data-stu-id="e5884-125">On return, it is filled with the APDU command constructed by this operation.</span></span> <span data-ttu-id="e5884-126">Se *ppCmd* foi definido como **NULL**, um objeto [**ISCardCmd**](iscardcmd.md) de [*cartão inteligente*](../secgloss/s-gly.md) será criado internamente e retornado usando o ponteiro *ppCmd* .</span><span class="sxs-lookup"><span data-stu-id="e5884-126">If *ppCmd* was set to **NULL**, a [*smart card*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) object is internally created and returned using the *ppCmd* pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5884-127">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e5884-127">Return value</span></span>

<span data-ttu-id="e5884-128">O método retorna um dos seguintes valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="e5884-128">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="e5884-129">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="e5884-129">Return code</span></span>                                                                                   | <span data-ttu-id="e5884-130">Descrição</span><span class="sxs-lookup"><span data-stu-id="e5884-130">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="e5884-131"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e5884-131"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="e5884-132">Operação concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="e5884-132">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="e5884-133"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="e5884-133"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="e5884-134">Parâmetro inválido.</span><span class="sxs-lookup"><span data-stu-id="e5884-134">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="e5884-135"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="e5884-135"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="e5884-136">Um ponteiro inadequado foi passado.</span><span class="sxs-lookup"><span data-stu-id="e5884-136">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="e5884-137"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="e5884-137"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="e5884-138">Sem memória.</span><span class="sxs-lookup"><span data-stu-id="e5884-138">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="e5884-139">Comentários</span><span class="sxs-lookup"><span data-stu-id="e5884-139">Remarks</span></span>

<span data-ttu-id="e5884-140">Quando a função Open for executada com êxito a partir do canal lógico básico, o MF deverá ser selecionado implicitamente como o DF atual e o status de segurança do novo canal lógico deverá ser o mesmo que o canal lógico básico após a ATR.</span><span class="sxs-lookup"><span data-stu-id="e5884-140">When the open function is successfully performed from the basic logical channel, the MF shall be implicitly selected as the current DF and the security status of the new logical channel should be the same as the basic logical channel after ATR.</span></span> <span data-ttu-id="e5884-141">O status de segurança do novo canal lógico deve ser separado do de qualquer outro canal lógico.</span><span class="sxs-lookup"><span data-stu-id="e5884-141">The security status of the new logical channel should be separate from that of any other logical channel.</span></span>

<span data-ttu-id="e5884-142">Quando a função Open é executada com êxito de um canal lógico, que não é o básico, o DF atual do canal lógico que emitiu o comando será selecionado como o DF atual.</span><span class="sxs-lookup"><span data-stu-id="e5884-142">When the open function is successfully performed from a logical channel, which is not the basic one, the current DF of the logical channel that issued the command will be selected as the current DF.</span></span> <span data-ttu-id="e5884-143">Além disso, o status de segurança para o novo canal lógico deve ser o mesmo que o status de segurança do canal lógico do qual a função abrir foi executada.</span><span class="sxs-lookup"><span data-stu-id="e5884-143">In addition, the security status for the new logical channel should be the same as the security status of the logical channel from which the open function was performed.</span></span>

<span data-ttu-id="e5884-144">Após uma função de fechamento bem-sucedida, o status de segurança relacionado a esse canal lógico é perdido.</span><span class="sxs-lookup"><span data-stu-id="e5884-144">After a successful close function, the security status related to this logical channel is lost.</span></span>

<span data-ttu-id="e5884-145">Para obter uma lista de todos os métodos fornecidos por essa interface, consulte [**ISCardISO7816**](iscardiso7816.md).</span><span class="sxs-lookup"><span data-stu-id="e5884-145">For a list of all the methods provided by this interface, see [**ISCardISO7816**](iscardiso7816.md).</span></span>

<span data-ttu-id="e5884-146">Além dos códigos de erro COM listados acima, essa interface pode retornar um código de erro de cartão inteligente se uma função de cartão inteligente foi chamada para concluir a solicitação.</span><span class="sxs-lookup"><span data-stu-id="e5884-146">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="e5884-147">Para obter mais informações, consulte [valores de retorno de cartão inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="e5884-147">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e5884-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e5884-148">Requirements</span></span>



| <span data-ttu-id="e5884-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="e5884-149">Requirement</span></span> | <span data-ttu-id="e5884-150">Valor</span><span class="sxs-lookup"><span data-stu-id="e5884-150">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e5884-151">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e5884-151">Minimum supported client</span></span><br/> | <span data-ttu-id="e5884-152">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="e5884-152">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="e5884-153">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e5884-153">Minimum supported server</span></span><br/> | <span data-ttu-id="e5884-154">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e5884-154">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e5884-155">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="e5884-155">End of client support</span></span><br/>    | <span data-ttu-id="e5884-156">Windows XP</span><span class="sxs-lookup"><span data-stu-id="e5884-156">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="e5884-157">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="e5884-157">End of server support</span></span><br/>    | <span data-ttu-id="e5884-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e5884-158">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="e5884-159">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e5884-159">Header</span></span><br/>                   | <dl> <span data-ttu-id="e5884-160"><dt>Scardssp. h</dt></span><span class="sxs-lookup"><span data-stu-id="e5884-160"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="e5884-161">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="e5884-161">Type library</span></span><br/>             | <dl> <span data-ttu-id="e5884-162"><dt>Scardsrv. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="e5884-162"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="e5884-163">DLL</span><span class="sxs-lookup"><span data-stu-id="e5884-163">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e5884-164"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e5884-164"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="e5884-165">IID</span><span class="sxs-lookup"><span data-stu-id="e5884-165">IID</span></span><br/>                      | <span data-ttu-id="e5884-166">IID \_ ISCardISO7816 é definido como 53B6AA68-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="e5884-166">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="e5884-167">Confira também</span><span class="sxs-lookup"><span data-stu-id="e5884-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5884-168">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="e5884-168">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> </dl>

 

 
