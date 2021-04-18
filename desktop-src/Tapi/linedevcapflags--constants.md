---
description: As \_ constantes de sinalizador de bit LINEDEVCAPFLAGS são uma coleção de boolianos que descreve vários recursos de dispositivo de linha.
ms.assetid: 0c537488-9fb9-4961-bd0a-1937aefc0b08
title: Constantes de LINEDEVCAPFLAGS_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffefca75c00fdf09b1886affbff7f0ea90bab6c1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105766973"
---
# <a name="linedevcapflags_-constants"></a><span data-ttu-id="3a6d4-103">\_Constantes LINEDEVCAPFLAGS</span><span class="sxs-lookup"><span data-stu-id="3a6d4-103">LINEDEVCAPFLAGS\_ Constants</span></span>

<span data-ttu-id="3a6d4-104">As constantes de sinalizador de bit **LINEDEVCAPFLAGS \_** são uma coleção de boolianos que descreve vários recursos de dispositivo de linha.</span><span class="sxs-lookup"><span data-stu-id="3a6d4-104">The **LINEDEVCAPFLAGS\_** bit-flag constants are a collection of Booleans describing various line device capabilities.</span></span>

<dl> <dt>

<span data-ttu-id="3a6d4-105"><span id="LINEDEVCAPFLAGS_CALLHUB"></span><span id="linedevcapflags_callhub"></span>**LINEDEVCAPFLAGS \_ CALLHUB**</span><span class="sxs-lookup"><span data-stu-id="3a6d4-105"><span id="LINEDEVCAPFLAGS_CALLHUB"></span><span id="linedevcapflags_callhub"></span>**LINEDEVCAPFLAGS\_CALLHUB**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="3a6d4-106">Indica se os hubs de chamada têm suporte nesta linha.</span><span class="sxs-lookup"><span data-stu-id="3a6d4-106">Indicates whether call hubs are supported on this line.</span></span> <span data-ttu-id="3a6d4-107">Esse sinalizador é exposto somente a aplicativos que negociam uma versão de TAPI 3,0 ou superior.</span><span class="sxs-lookup"><span data-stu-id="3a6d4-107">This flag is exposed only to applications that negotiate a TAPI version of 3.0 or higher.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3a6d4-108"><span id="LINEDEVCAPFLAGS_CALLHUBTRACKING"></span><span id="linedevcapflags_callhubtracking"></span>**LINEDEVCAPFLAGS \_ CALLHUBTRACKING**</span><span class="sxs-lookup"><span data-stu-id="3a6d4-108"><span id="LINEDEVCAPFLAGS_CALLHUBTRACKING"></span><span id="linedevcapflags_callhubtracking"></span>**LINEDEVCAPFLAGS\_CALLHUBTRACKING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="3a6d4-109">Indica se o acompanhamento do hub de chamadas tem suporte nesta linha.</span><span class="sxs-lookup"><span data-stu-id="3a6d4-109">Indicates whether call hub tracking is supported on this line.</span></span> <span data-ttu-id="3a6d4-110">Esse sinalizador é exposto somente a aplicativos que negociam uma versão de TAPI 3,0 ou superior.</span><span class="sxs-lookup"><span data-stu-id="3a6d4-110">This flag is exposed only to applications that negotiate a TAPI version of 3.0 or higher.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3a6d4-111"><span id="LINEDEVCAPFLAGS_CLOSEDROP"></span><span id="linedevcapflags_closedrop"></span>**LINEDEVCAPFLAGS \_ CLOSEDROP**</span><span class="sxs-lookup"><span data-stu-id="3a6d4-111"><span id="LINEDEVCAPFLAGS_CLOSEDROP"></span><span id="linedevcapflags_closedrop"></span>**LINEDEVCAPFLAGS\_CLOSEDROP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="3a6d4-112">Especifica o que acontece quando uma linha aberta é fechada enquanto o aplicativo chama ativo na linha.</span><span class="sxs-lookup"><span data-stu-id="3a6d4-112">Specifies what happens when an open line is closed while the application has calls active on the line.</span></span> <span data-ttu-id="3a6d4-113">Se **for true**, o provedor de Serviços descartará (limpará) todas as chamadas ativas na linha quando o último aplicativo que abriu a linha a fechar com [**lineClose**](/windows/desktop/api/Tapi/nf-tapi-lineclose).</span><span class="sxs-lookup"><span data-stu-id="3a6d4-113">If **TRUE**, the service provider drops (clears) all active calls on the line when the last application that has opened the line closes it with [**lineClose**](/windows/desktop/api/Tapi/nf-tapi-lineclose).</span></span> <span data-ttu-id="3a6d4-114">Se **for false**, o provedor de serviços não descartará chamadas ativas nesses casos.</span><span class="sxs-lookup"><span data-stu-id="3a6d4-114">If **FALSE**, the service provider does not drop active calls in such cases.</span></span> <span data-ttu-id="3a6d4-115">Em vez disso, as chamadas permanecem ativas e sob o controle de dispositivos externos.</span><span class="sxs-lookup"><span data-stu-id="3a6d4-115">Instead, the calls remain active and under control of external devices.</span></span> <span data-ttu-id="3a6d4-116">Um provedor de serviços normalmente define esse bit como **false** se houver algum outro dispositivo que possa manter a chamada ativa, por exemplo, se uma linha analógica tiver o computador e o conjunto de telefone se conectar diretamente a eles em uma configuração de linha de terceiros, o telefone offhook manterá automaticamente a chamada ativa mesmo depois que o computador for desligado.</span><span class="sxs-lookup"><span data-stu-id="3a6d4-116">A service provider typically sets this bit to **FALSE** if there is some other device that can keep the call alive, for example, if an analog line has the computer and phone set both connect directly to them in a party-line configuration, the offhook phone will automatically keep the call active even after the computer powers down.</span></span>

<span data-ttu-id="3a6d4-117">Os aplicativos devem verificar esse sinalizador para determinar se deve avisar o usuário (com uma caixa de diálogo OK/cancelar) de que as chamadas ativas serão perdidas.</span><span class="sxs-lookup"><span data-stu-id="3a6d4-117">Applications should check this flag to determine whether to warn the user (with an OK/Cancel dialog box) that active calls will be lost.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3a6d4-118"><span id="LINEDEVCAPFLAGS_CROSSADDRCONF"></span><span id="linedevcapflags_crossaddrconf"></span>**LINEDEVCAPFLAGS \_ CROSSADDRCONF**</span><span class="sxs-lookup"><span data-stu-id="3a6d4-118"><span id="LINEDEVCAPFLAGS_CROSSADDRCONF"></span><span id="linedevcapflags_crossaddrconf"></span>**LINEDEVCAPFLAGS\_CROSSADDRCONF**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="3a6d4-119">Especifica se as chamadas em endereços diferentes nessa linha podem ser conferências.</span><span class="sxs-lookup"><span data-stu-id="3a6d4-119">Specifies whether calls on different addresses on this line can be conferenced.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3a6d4-120"><span id="LINEDEVCAPFLAGS_DIALBILLING"></span><span id="linedevcapflags_dialbilling"></span>**LINEDEVCAPFLAGS \_ DIALBILLING**</span><span class="sxs-lookup"><span data-stu-id="3a6d4-120"><span id="LINEDEVCAPFLAGS_DIALBILLING"></span><span id="linedevcapflags_dialbilling"></span>**LINEDEVCAPFLAGS\_DIALBILLING**</span></span>
</dt> <dd> <dl> <dt>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3a6d4-121"><span id="LINEDEVCAPFLAGS_DIALDIALTONE"></span><span id="linedevcapflags_dialdialtone"></span>**LINEDEVCAPFLAGS \_ DIALDIALTONE**</span><span class="sxs-lookup"><span data-stu-id="3a6d4-121"><span id="LINEDEVCAPFLAGS_DIALDIALTONE"></span><span id="linedevcapflags_dialdialtone"></span>**LINEDEVCAPFLAGS\_DIALDIALTONE**</span></span>
</dt> <dd> <dl> <dt>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3a6d4-122"><span id="LINEDEVCAPFLAGS_DIALQUIET"></span><span id="linedevcapflags_dialquiet"></span>**LINEDEVCAPFLAGS \_ DIALQUIET**</span><span class="sxs-lookup"><span data-stu-id="3a6d4-122"><span id="LINEDEVCAPFLAGS_DIALQUIET"></span><span id="linedevcapflags_dialquiet"></span>**LINEDEVCAPFLAGS\_DIALQUIET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="3a6d4-123">Esses sinalizadores indicam se o modificador de cadeia de caracteres de discagem "$", "@" ou "W" tem suporte para um determinado dispositivo de linha.</span><span class="sxs-lookup"><span data-stu-id="3a6d4-123">These flags indicate whether the "$", "@", or "W" dialable string modifier is supported for a given line device.</span></span> <span data-ttu-id="3a6d4-124">Será **verdadeiro** se o modificador for suportado; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="3a6d4-124">It is **TRUE** if the modifier is supported; otherwise, **FALSE**.</span></span> <span data-ttu-id="3a6d4-125">O "?" (avisar o usuário para continuar a discagem) nunca é suportado por um dispositivo de linha.</span><span class="sxs-lookup"><span data-stu-id="3a6d4-125">The "?" (prompt user to continue dialing) is never supported by a line device.</span></span> <span data-ttu-id="3a6d4-126">Esses sinalizadores permitem que um aplicativo determine antecipadamente quais modificadores resultariam na geração de um LINEERR.</span><span class="sxs-lookup"><span data-stu-id="3a6d4-126">These flags allow an application to determine up front which modifiers would result in the generation of a LINEERR.</span></span> <span data-ttu-id="3a6d4-127">O aplicativo tem a opção de cadeias de caracteres de discagem antes da verificação para não há suporte ou para a transmissão da cadeia de caracteres "RAW" de [**lineTranslateAddress**](/windows/desktop/api/Tapi/nf-tapi-linetranslateaddress) diretamente para o provedor como parte de funções como [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) ou [**lineDial**](/windows/desktop/api/Tapi/nf-tapi-linedial) e permite que a função gere um erro para informar qual modificador sem suporte ocorre primeiro na cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="3a6d4-127">The application has the choice of pre-scanning dialable strings for unsupported characters or of passing the "raw" string from [**lineTranslateAddress**](/windows/desktop/api/Tapi/nf-tapi-linetranslateaddress) directly to the provider as part of functions such as [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) or [**lineDial**](/windows/desktop/api/Tapi/nf-tapi-linedial) and let the function generate an error to tell it which unsupported modifier occurs first in the string.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3a6d4-128"><span id="LINEDEVCAPFLAGS_HIGHLEVCOMP"></span><span id="linedevcapflags_highlevcomp"></span>**LINEDEVCAPFLAGS \_ HIGHLEVCOMP**</span><span class="sxs-lookup"><span data-stu-id="3a6d4-128"><span id="LINEDEVCAPFLAGS_HIGHLEVCOMP"></span><span id="linedevcapflags_highlevcomp"></span>**LINEDEVCAPFLAGS\_HIGHLEVCOMP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="3a6d4-129">Especifica se os elementos de informações de compatibilidade de alto nível têm suporte nesta linha.</span><span class="sxs-lookup"><span data-stu-id="3a6d4-129">Specifies whether high-level compatibility information elements are supported on this line.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3a6d4-130"><span id="LINEDEVCAPFLAGS_LOWLEVCOMP"></span><span id="linedevcapflags_lowlevcomp"></span>**LINEDEVCAPFLAGS \_ LOWLEVCOMP**</span><span class="sxs-lookup"><span data-stu-id="3a6d4-130"><span id="LINEDEVCAPFLAGS_LOWLEVCOMP"></span><span id="linedevcapflags_lowlevcomp"></span>**LINEDEVCAPFLAGS\_LOWLEVCOMP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="3a6d4-131">Especifica se os elementos de informações de compatibilidade de nível baixo têm suporte nesta linha.</span><span class="sxs-lookup"><span data-stu-id="3a6d4-131">Specifies whether low-level compatibility information elements are supported on this line.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3a6d4-132"><span id="LINEDEVCAPFLAGS_MEDIACONTROL"></span><span id="linedevcapflags_mediacontrol"></span>**LINEDEVCAPFLAGS \_ MEDIACONTROL**</span><span class="sxs-lookup"><span data-stu-id="3a6d4-132"><span id="LINEDEVCAPFLAGS_MEDIACONTROL"></span><span id="linedevcapflags_mediacontrol"></span>**LINEDEVCAPFLAGS\_MEDIACONTROL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="3a6d4-133">Especifica se as operações de controle de mídia estão disponíveis para chamadas nesta linha.</span><span class="sxs-lookup"><span data-stu-id="3a6d4-133">Specifies whether media-control operations are available for calls at this line.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3a6d4-134"><span id="LINEDEVCAPFLAGS_MSP"></span><span id="linedevcapflags_msp"></span>**LINEDEVCAPFLAGS \_ MSP**</span><span class="sxs-lookup"><span data-stu-id="3a6d4-134"><span id="LINEDEVCAPFLAGS_MSP"></span><span id="linedevcapflags_msp"></span>**LINEDEVCAPFLAGS\_MSP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="3a6d4-135">Indica se um MSP (provedor de serviços de mídia) está associado à linha.</span><span class="sxs-lookup"><span data-stu-id="3a6d4-135">Indicates whether a Media Service Provider (MSP) is associated with the line.</span></span> <span data-ttu-id="3a6d4-136">Esse sinalizador é exposto somente a aplicativos que negociam uma versão de TAPI 3,0 ou superior.</span><span class="sxs-lookup"><span data-stu-id="3a6d4-136">This flag is exposed only to applications that negotiate a TAPI version of 3.0 or higher.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3a6d4-137"><span id="LINEDEVCAPFLAGS_MULTIPLEADDR"></span><span id="linedevcapflags_multipleaddr"></span>**LINEDEVCAPFLAGS \_ MULTIPLEADDR**</span><span class="sxs-lookup"><span data-stu-id="3a6d4-137"><span id="LINEDEVCAPFLAGS_MULTIPLEADDR"></span><span id="linedevcapflags_multipleaddr"></span>**LINEDEVCAPFLAGS\_MULTIPLEADDR**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="3a6d4-138">Especifica se [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall), [**lineDial**](/windows/desktop/api/Tapi/nf-tapi-linedial), [**TSPI \_ lineMakeCall**](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall)ou [**TSPI \_ lineDial**](/windows/win32/api/tspi/nf-tspi-tspi_linedial) é capaz de lidar com vários endereços de uma vez (como para multiplexação inversa).</span><span class="sxs-lookup"><span data-stu-id="3a6d4-138">Specifies whether [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall), [**lineDial**](/windows/desktop/api/Tapi/nf-tapi-linedial), [**TSPI\_lineMakeCall**](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall), or [**TSPI\_lineDial**](/windows/win32/api/tspi/nf-tspi-tspi_linedial) is able to deal with multiple addresses at once (as for inverse multiplexing).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3a6d4-139"><span id="LINEDEVCAPFLAGS_PRIVATEOBJECTS"></span><span id="linedevcapflags_privateobjects"></span>**LINEDEVCAPFLAGS \_ PRIVATEOBJECTS**</span><span class="sxs-lookup"><span data-stu-id="3a6d4-139"><span id="LINEDEVCAPFLAGS_PRIVATEOBJECTS"></span><span id="linedevcapflags_privateobjects"></span>**LINEDEVCAPFLAGS\_PRIVATEOBJECTS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="3a6d4-140">Indica se as [interfaces específicas do provedor](./provider-specific-interfaces.md) foram implementadas.</span><span class="sxs-lookup"><span data-stu-id="3a6d4-140">Indicates whether [provider-specific Interfaces](./provider-specific-interfaces.md) have been implemented.</span></span> <span data-ttu-id="3a6d4-141">Esse sinalizador é exposto somente a aplicativos que negociam uma versão de TAPI 3,0 ou superior.</span><span class="sxs-lookup"><span data-stu-id="3a6d4-141">This flag is exposed only to applications that negotiate a TAPI version of 3.0 or higher.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3a6d4-142">Comentários</span><span class="sxs-lookup"><span data-stu-id="3a6d4-142">Remarks</span></span>

<span data-ttu-id="3a6d4-143">Sem extensibilidade.</span><span class="sxs-lookup"><span data-stu-id="3a6d4-143">No extensibility.</span></span> <span data-ttu-id="3a6d4-144">Todos os 32 bits são reservados.</span><span class="sxs-lookup"><span data-stu-id="3a6d4-144">All 32 bits are reserved.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a6d4-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3a6d4-145">Requirements</span></span>



| <span data-ttu-id="3a6d4-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a6d4-146">Requirement</span></span> | <span data-ttu-id="3a6d4-147">Valor</span><span class="sxs-lookup"><span data-stu-id="3a6d4-147">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="3a6d4-148">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="3a6d4-148">TAPI version</span></span><br/> | <span data-ttu-id="3a6d4-149">Requer TAPI 2,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="3a6d4-149">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="3a6d4-150">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3a6d4-150">Header</span></span><br/>       | <dl> <span data-ttu-id="3a6d4-151"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="3a6d4-151"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a6d4-152">Confira também</span><span class="sxs-lookup"><span data-stu-id="3a6d4-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a6d4-153">**lineClose**</span><span class="sxs-lookup"><span data-stu-id="3a6d4-153">**lineClose**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineclose)
</dt> <dt>

[<span data-ttu-id="3a6d4-154">**lineDial**</span><span class="sxs-lookup"><span data-stu-id="3a6d4-154">**lineDial**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linedial)
</dt> <dt>

[<span data-ttu-id="3a6d4-155">**lineMakeCall**</span><span class="sxs-lookup"><span data-stu-id="3a6d4-155">**lineMakeCall**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linemakecall)
</dt> <dt>

[<span data-ttu-id="3a6d4-156">**lineTranslateAddress**</span><span class="sxs-lookup"><span data-stu-id="3a6d4-156">**lineTranslateAddress**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linetranslateaddress)
</dt> </dl>

 

