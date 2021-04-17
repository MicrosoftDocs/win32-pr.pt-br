---
description: Veja a seguir uma lista de códigos de erro que a TAPI pode retornar ao invocar operações em linhas, endereços ou chamadas.
ms.assetid: bdaf60d1-6ff2-4bd6-b246-8556d6cae644
title: Constantes de LINEERR_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ed7757377d26dbde832b7ef50f275b45e21760d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105780120"
---
# <a name="lineerr_-constants"></a><span data-ttu-id="e2108-103">\_Constantes LINEERR</span><span class="sxs-lookup"><span data-stu-id="e2108-103">LINEERR\_ Constants</span></span>

<span data-ttu-id="e2108-104">Veja a seguir uma lista de códigos de erro que a TAPI pode retornar ao invocar operações em linhas, endereços ou chamadas.</span><span class="sxs-lookup"><span data-stu-id="e2108-104">The following is a list of error codes that TAPI can return when invoking operations on lines, addresses, or calls.</span></span> <span data-ttu-id="e2108-105">Para obter mais informações sobre como determinar quais desses códigos de erro uma função específica pode retornar, consulte as descrições de função individuais.</span><span class="sxs-lookup"><span data-stu-id="e2108-105">For more information about how to determine which of these error codes a particular function can return, see the individual function descriptions.</span></span>

<dl> <dt>

<span data-ttu-id="e2108-106"><span id="LINEERR_ADDRESSBLOCKED"></span><span id="lineerr_addressblocked"></span>**LINEERR \_ ADDRESSBLOCKED**</span><span class="sxs-lookup"><span data-stu-id="e2108-106"><span id="LINEERR_ADDRESSBLOCKED"></span><span id="lineerr_addressblocked"></span>**LINEERR\_ADDRESSBLOCKED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e2108-107">O endereço especificado está impedido de ser discado na chamada especificada.</span><span class="sxs-lookup"><span data-stu-id="e2108-107">The specified address is blocked from being dialed on the specified call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2108-108"><span id="LINEERR_ADDRESSBLOCKED"></span><span id="lineerr_addressblocked"></span>**LINEERR \_ ADDRESSBLOCKED**</span><span class="sxs-lookup"><span data-stu-id="e2108-108"><span id="LINEERR_ADDRESSBLOCKED"></span><span id="lineerr_addressblocked"></span>**LINEERR\_ADDRESSBLOCKED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e2108-109">O endereço de chamada de destino tem bloqueio de chamada habilitado.</span><span class="sxs-lookup"><span data-stu-id="e2108-109">The target call address has call blocking enabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2108-110"><span id="LINEERR_ALLOCATED"></span><span id="lineerr_allocated"></span>**LINEERR \_ alocada**</span><span class="sxs-lookup"><span data-stu-id="e2108-110"><span id="LINEERR_ALLOCATED"></span><span id="lineerr_allocated"></span>**LINEERR\_ALLOCATED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e2108-111">A linha não pode ser aberta devido a uma condição persistente, como a de uma porta serial que está sendo aberta exclusivamente por outro processo.</span><span class="sxs-lookup"><span data-stu-id="e2108-111">The line cannot be opened due to a persistent condition, such as that of a serial port being exclusively opened by another process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2108-112"><span id="LINEERR_BADDEVICEID"></span><span id="lineerr_baddeviceid"></span>**LINEERR \_ BADDEVICEID**</span><span class="sxs-lookup"><span data-stu-id="e2108-112"><span id="LINEERR_BADDEVICEID"></span><span id="lineerr_baddeviceid"></span>**LINEERR\_BADDEVICEID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e2108-113">O identificador de dispositivo ou o identificador de dispositivo de linha especificado, como em um parâmetro *dwDeviceID* , é inválido ou está fora do intervalo.</span><span class="sxs-lookup"><span data-stu-id="e2108-113">The specified device identifier or line device identifier, such as in a *dwDeviceID* parameter, is invalid or out of range.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2108-114"><span id="LINEERR_BEARERMODEUNAVAIL"></span><span id="lineerr_bearermodeunavail"></span>**LINEERR \_ BEARERMODEUNAVAIL**</span><span class="sxs-lookup"><span data-stu-id="e2108-114"><span id="LINEERR_BEARERMODEUNAVAIL"></span><span id="lineerr_bearermodeunavail"></span>**LINEERR\_BEARERMODEUNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e2108-115">O membro do modo de portador em [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) é inválido, o modo de portador especificado em **LINECALLPARAMS** não está disponível ou o modo de portador de chamada não pode ser alterado para o modo de portador especificado.</span><span class="sxs-lookup"><span data-stu-id="e2108-115">The bearer mode member in [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) is invalid, the bearer mode specified in **LINECALLPARAMS** is not available, or the call bearer mode cannot be changed to the specified bearer mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2108-116"><span id="LINEERR_BILLINGREJECTED"></span><span id="lineerr_billingrejected"></span>**LINEERR \_ BILLINGREJECTED**</span><span class="sxs-lookup"><span data-stu-id="e2108-116"><span id="LINEERR_BILLINGREJECTED"></span><span id="lineerr_billingrejected"></span>**LINEERR\_BILLINGREJECTED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e2108-117">O modo de cobrança da chamada foi rejeitado.</span><span class="sxs-lookup"><span data-stu-id="e2108-117">The billing mode of the call was rejected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2108-118"><span id="LINEERR_CALLUNAVAIL"></span><span id="lineerr_callunavail"></span>**LINEERR \_ CALLUNAVAIL**</span><span class="sxs-lookup"><span data-stu-id="e2108-118"><span id="LINEERR_CALLUNAVAIL"></span><span id="lineerr_callunavail"></span>**LINEERR\_CALLUNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e2108-119">Todas as aparências de chamada no endereço especificado estão em uso no momento.</span><span class="sxs-lookup"><span data-stu-id="e2108-119">All call appearances on the specified address are currently in use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2108-120"><span id="LINEERR_COMPLETIONOVERRUN"></span><span id="lineerr_completionoverrun"></span>**LINEERR \_ COMPLETIONOVERRUN**</span><span class="sxs-lookup"><span data-stu-id="e2108-120"><span id="LINEERR_COMPLETIONOVERRUN"></span><span id="lineerr_completionoverrun"></span>**LINEERR\_COMPLETIONOVERRUN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e2108-121">O número máximo de conclusões de chamadas pendentes foi excedido.</span><span class="sxs-lookup"><span data-stu-id="e2108-121">The maximum number of outstanding call completions has been exceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2108-122"><span id="LINEERR_CONFERENCEFULL"></span><span id="lineerr_conferencefull"></span>**LINEERR \_ CONFERENCEFULL**</span><span class="sxs-lookup"><span data-stu-id="e2108-122"><span id="LINEERR_CONFERENCEFULL"></span><span id="lineerr_conferencefull"></span>**LINEERR\_CONFERENCEFULL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e2108-123">O número máximo de partes de uma conferência foi atingido ou o número de partes solicitado não pode ser satisfeito.</span><span class="sxs-lookup"><span data-stu-id="e2108-123">The maximum number of parties for a conference has been reached, or the requested number of parties cannot be satisfied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2108-124"><span id="LINEERR_DIALBILLING"></span><span id="lineerr_dialbilling"></span>**LINEERR \_ DIALBILLING**</span><span class="sxs-lookup"><span data-stu-id="e2108-124"><span id="LINEERR_DIALBILLING"></span><span id="lineerr_dialbilling"></span>**LINEERR\_DIALBILLING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e2108-125">O parâmetro endereço discável contém caracteres de controle de discagem não processados pelo provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="e2108-125">The dialable address parameter contains dialing control characters not processed by the service provider.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2108-126"><span id="LINEERR_DIALDIALTONE"></span><span id="lineerr_dialdialtone"></span>**LINEERR \_ DIALDIALTONE**</span><span class="sxs-lookup"><span data-stu-id="e2108-126"><span id="LINEERR_DIALDIALTONE"></span><span id="lineerr_dialdialtone"></span>**LINEERR\_DIALDIALTONE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e2108-127">O parâmetro endereço discável contém caracteres de controle de discagem não processados pelo provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="e2108-127">The dialable address parameter contains dialing control characters not processed by the service provider.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2108-128"><span id="LINEERR_DIALPROMPT"></span><span id="lineerr_dialprompt"></span>**LINEERR \_ DIALPROMPT**</span><span class="sxs-lookup"><span data-stu-id="e2108-128"><span id="LINEERR_DIALPROMPT"></span><span id="lineerr_dialprompt"></span>**LINEERR\_DIALPROMPT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e2108-129">O parâmetro endereço discável contém caracteres de controle de discagem não processados pelo provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="e2108-129">The dialable address parameter contains dialing control characters not processed by the service provider.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2108-130"><span id="LINEERR_DIALQUIET"></span><span id="lineerr_dialquiet"></span>**LINEERR \_ DIALQUIET**</span><span class="sxs-lookup"><span data-stu-id="e2108-130"><span id="LINEERR_DIALQUIET"></span><span id="lineerr_dialquiet"></span>**LINEERR\_DIALQUIET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e2108-131">O parâmetro endereço discável contém caracteres de controle de discagem não processados pelo provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="e2108-131">The dialable address parameter contains dialing control characters not processed by the service provider.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2108-132"><span id="LINEERR_DIALVOICEDETECT"></span><span id="lineerr_dialvoicedetect"></span>**LINEERR \_ DIALVOICEDETECT**</span><span class="sxs-lookup"><span data-stu-id="e2108-132"><span id="LINEERR_DIALVOICEDETECT"></span><span id="lineerr_dialvoicedetect"></span>**LINEERR\_DIALVOICEDETECT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e2108-133">Uso do modificador de discagem (:) Não tem suporte.</span><span class="sxs-lookup"><span data-stu-id="e2108-133">Use of the dial modifier (:) is not supported.</span></span> <span data-ttu-id="e2108-134">Esse valor é exposto somente a aplicativos que negociam uma versão TAPI do 2,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="e2108-134">This value is exposed only to applications that negotiate a TAPI version of 2.0 or later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2108-135"><span id="LINEERR_DISCONNECTED"></span><span id="lineerr_disconnected"></span>**LINEERR \_ desconectado**</span><span class="sxs-lookup"><span data-stu-id="e2108-135"><span id="LINEERR_DISCONNECTED"></span><span id="lineerr_disconnected"></span>**LINEERR\_DISCONNECTED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e2108-136">A chamada foi desconectada.</span><span class="sxs-lookup"><span data-stu-id="e2108-136">The call has been disconnected.</span></span> <span data-ttu-id="e2108-137">Esse valor é exposto somente a aplicativos que negociam uma versão TAPI do 2,2 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="e2108-137">This value is exposed only to applications that negotiate a TAPI version of 2.2 or later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2108-138"><span id="LINEERR_INCOMPATIBLEAPIVERSION"></span><span id="lineerr_incompatibleapiversion"></span>**LINEERR \_ INCOMPATIBLEAPIVERSION**</span><span class="sxs-lookup"><span data-stu-id="e2108-138"><span id="LINEERR_INCOMPATIBLEAPIVERSION"></span><span id="lineerr_incompatibleapiversion"></span>**LINEERR\_INCOMPATIBLEAPIVERSION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e2108-139">O aplicativo solicitou uma versão TAPI ou um intervalo de versão que seja incompatível com o, ou que não tenha suporte do, a implementação da API de telefonia e o provedor de serviços correspondente.</span><span class="sxs-lookup"><span data-stu-id="e2108-139">The application requested a TAPI version or version range that is either incompatible with, or cannot be supported by, the Telephony API implementation and the corresponding service provider.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2108-140"><span id="LINEERR_INCOMPATIBLEEXTVERSION"></span><span id="lineerr_incompatibleextversion"></span>**LINEERR \_ INCOMPATIBLEEXTVERSION**</span><span class="sxs-lookup"><span data-stu-id="e2108-140"><span id="LINEERR_INCOMPATIBLEEXTVERSION"></span><span id="lineerr_incompatibleextversion"></span>**LINEERR\_INCOMPATIBLEEXTVERSION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e2108-141">O aplicativo solicitou um intervalo de versão de extensão inválido ou não tem suporte do provedor de serviços correspondente.</span><span class="sxs-lookup"><span data-stu-id="e2108-141">The application requested an extension version range that is either invalid or cannot be supported by the corresponding service provider.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2108-142"><span id="LINEERR_INIFILECORRUPT"></span><span id="lineerr_inifilecorrupt"></span>**LINEERR \_ INIFILECORRUPT**</span><span class="sxs-lookup"><span data-stu-id="e2108-142"><span id="LINEERR_INIFILECORRUPT"></span><span id="lineerr_inifilecorrupt"></span>**LINEERR\_INIFILECORRUPT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e2108-143">O arquivo de Telephon.ini não pode ser lido ou compreendido corretamente pela TAPI devido a inconsistências internas ou problemas de formatação.</span><span class="sxs-lookup"><span data-stu-id="e2108-143">The Telephon.ini file cannot be read or understood properly by TAPI because of internal inconsistencies or formatting problems.</span></span> <span data-ttu-id="e2108-144">Por exemplo, a \[ \] seção locais, \[ cartões \] ou \[ países \] do arquivo de Telephon.ini pode estar corrompida ou inconsistente.</span><span class="sxs-lookup"><span data-stu-id="e2108-144">For example, the \[Locations\], \[Cards\], or \[Countries\] section of the Telephon.ini file may be corrupted or inconsistent.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2108-145"><span id="LINEERR_INUSE"></span><span id="lineerr_inuse"></span>**LINEERR \_ INUSE**</span><span class="sxs-lookup"><span data-stu-id="e2108-145"><span id="LINEERR_INUSE"></span><span id="lineerr_inuse"></span>**LINEERR\_INUSE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e2108-146">O dispositivo de linha está em uso e não pode ser configurado no momento, permitir que uma parte seja adicionada, permitir que uma chamada seja respondida, permitir que uma chamada seja colocada ou permitir que uma chamada seja transferida.</span><span class="sxs-lookup"><span data-stu-id="e2108-146">The line device is in use and cannot currently be configured, allow a party to be added, allow a call to be answered, allow a call to be placed, or allow a call to be transferred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2108-147"><span id="LINEERR_INVALADDRESS"></span><span id="lineerr_invaladdress"></span>**LINEERR \_ INVALADDRESS**</span><span class="sxs-lookup"><span data-stu-id="e2108-147"><span id="LINEERR_INVALADDRESS"></span><span id="lineerr_invaladdress"></span>**LINEERR\_INVALADDRESS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e2108-148">Um endereço especificado é inválido ou não é permitido.</span><span class="sxs-lookup"><span data-stu-id="e2108-148">A specified address is either invalid or not allowed.</span></span> <span data-ttu-id="e2108-149">Se for inválido, o endereço contém caracteres ou dígitos inválidos ou o endereço de destino contém caracteres de controle de discagem (W, @, $ ou?) que não são suportados pelo provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="e2108-149">If invalid, the address contains invalid characters or digits, or the destination address contains dialing control characters (W, @, $, or ?) that are not supported by the service provider.</span></span> <span data-ttu-id="e2108-150">Se não for permitido, o endereço especificado não será atribuído à linha especificada ou não será válido para o redirecionamento de endereço.</span><span class="sxs-lookup"><span data-stu-id="e2108-150">If not allowed, the specified address is either not assigned to the specified line or is not valid for address redirection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2108-151"><span id="LINEERR_INVALADDRESSID"></span><span id="lineerr_invaladdressid"></span>**LINEERR \_ INVALADDRESSID**</span><span class="sxs-lookup"><span data-stu-id="e2108-151"><span id="LINEERR_INVALADDRESSID"></span><span id="lineerr_invaladdressid"></span>**LINEERR\_INVALADDRESSID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e2108-152">O identificador de endereço especificado é inválido ou está fora do intervalo.</span><span class="sxs-lookup"><span data-stu-id="e2108-152">The specified address identifier is either invalid or out of range.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2108-153"><span id="LINEERR_INVALADDRESSMODE"></span><span id="lineerr_invaladdressmode"></span>**LINEERR \_ INVALADDRESSMODE**</span><span class="sxs-lookup"><span data-stu-id="e2108-153"><span id="LINEERR_INVALADDRESSMODE"></span><span id="lineerr_invaladdressmode"></span>**LINEERR\_INVALADDRESSMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e2108-154">O modo de endereço especificado é inválido.</span><span class="sxs-lookup"><span data-stu-id="e2108-154">The specified address mode is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2108-155"><span id="LINEERR_INVALADDRESSSTATE"></span><span id="lineerr_invaladdressstate"></span>**LINEERR \_ INVALADDRESSSTATE**</span><span class="sxs-lookup"><span data-stu-id="e2108-155"><span id="LINEERR_INVALADDRESSSTATE"></span><span id="lineerr_invaladdressstate"></span>**LINEERR\_INVALADDRESSSTATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e2108-156">O estado de endereço especificado contém um ou mais bits que não [**são \_ constantes LINEADDRESSSTATE**](lineaddressstate--constants.md).</span><span class="sxs-lookup"><span data-stu-id="e2108-156">The specified address state contains one or more bits that are not [**LINEADDRESSSTATE\_ constants**](lineaddressstate--constants.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2108-157"><span id="LINEERR_INVALADDRESSTYPE"></span><span id="lineerr_invaladdresstype"></span>**LINEERR \_ INVALADDRESSTYPE**</span><span class="sxs-lookup"><span data-stu-id="e2108-157"><span id="LINEERR_INVALADDRESSTYPE"></span><span id="lineerr_invaladdresstype"></span>**LINEERR\_INVALADDRESSTYPE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e2108-158">O aplicativo referenciou um tipo de endereço que não é válido.</span><span class="sxs-lookup"><span data-stu-id="e2108-158">The application referenced an address type that is not valid.</span></span> <span data-ttu-id="e2108-159">Esse valor é exposto somente a aplicativos que negociam uma versão TAPI do 3,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="e2108-159">This value is exposed only to applications that negotiate a TAPI version of 3.0 or later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2108-160"><span id="LINEERR_INVALAGENTACTIVITY"></span><span id="lineerr_invalagentactivity"></span>**LINEERR \_ INVALAGENTACTIVITY**</span><span class="sxs-lookup"><span data-stu-id="e2108-160"><span id="LINEERR_INVALAGENTACTIVITY"></span><span id="lineerr_invalagentactivity"></span>**LINEERR\_INVALAGENTACTIVITY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e2108-161">A atividade do agente especificada não é válida.</span><span class="sxs-lookup"><span data-stu-id="e2108-161">The specified agent activity is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2108-162"><span id="LINEERR_INVALAGENTACTIVITY"></span><span id="lineerr_invalagentactivity"></span>**LINEERR \_ INVALAGENTACTIVITY**</span><span class="sxs-lookup"><span data-stu-id="e2108-162"><span id="LINEERR_INVALAGENTACTIVITY"></span><span id="lineerr_invalagentactivity"></span>**LINEERR\_INVALAGENTACTIVITY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e2108-163">O aplicativo que invoca essa operação é o destino da entrega indireta.</span><span class="sxs-lookup"><span data-stu-id="e2108-163">The application invoking this operation is the target of the indirect handoff.</span></span> <span data-ttu-id="e2108-164">Ou seja, a TAPI determinou que o aplicativo de chamada também é o aplicativo de prioridade mais alta para o tipo de mídia fornecido.</span><span class="sxs-lookup"><span data-stu-id="e2108-164">That is, TAPI has determined that the calling application is also the highest priority application for the given media type.</span></span> <span data-ttu-id="e2108-165">Esse valor é exposto somente a aplicativos que negociam uma versão TAPI do 2,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="e2108-165">This value is exposed only to applications that negotiate a TAPI version of 2.0 or later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2108-166"><span id="LINEERR_INVALAGENTGROUP"></span><span id="lineerr_invalagentgroup"></span>**LINEERR \_ INVALAGENTGROUP**</span><span class="sxs-lookup"><span data-stu-id="e2108-166"><span id="LINEERR_INVALAGENTGROUP"></span><span id="lineerr_invalagentgroup"></span>**LINEERR\_INVALAGENTGROUP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e2108-167">As informações do grupo de agentes especificadas não são válidas ou contêm erros.</span><span class="sxs-lookup"><span data-stu-id="e2108-167">The specified agent group information is not valid or contains errors.</span></span> <span data-ttu-id="e2108-168">A ação solicitada não foi executada.</span><span class="sxs-lookup"><span data-stu-id="e2108-168">The requested action has not been performed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2108-169"><span id="LINEERR_INVALAGENTGROUP"></span><span id="lineerr_invalagentgroup"></span>**LINEERR \_ INVALAGENTGROUP**</span><span class="sxs-lookup"><span data-stu-id="e2108-169"><span id="LINEERR_INVALAGENTGROUP"></span><span id="lineerr_invalagentgroup"></span>**LINEERR\_INVALAGENTGROUP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e2108-170">O aplicativo referenciou um grupo de agentes que não é válido.</span><span class="sxs-lookup"><span data-stu-id="e2108-170">The application referenced an agent group that is not valid.</span></span> <span data-ttu-id="e2108-171">Esse valor é exposto somente a aplicativos que negociam uma versão TAPI do 2,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="e2108-171">This value is exposed only to applications that negotiate a TAPI version of 2.0 or later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2108-172"><span id="LINEERR_INVALAGENTID"></span><span id="lineerr_invalagentid"></span>**LINEERR \_ INVALAGENTID**</span><span class="sxs-lookup"><span data-stu-id="e2108-172"><span id="LINEERR_INVALAGENTID"></span><span id="lineerr_invalagentid"></span>**LINEERR\_INVALAGENTID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e2108-173">O identificador de agente especificado é inválido.</span><span class="sxs-lookup"><span data-stu-id="e2108-173">The specified agent identifier is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2108-174"><span id="LINEERR_INVALAGENTID"></span><span id="lineerr_invalagentid"></span>**LINEERR \_ INVALAGENTID**</span><span class="sxs-lookup"><span data-stu-id="e2108-174"><span id="LINEERR_INVALAGENTID"></span><span id="lineerr_invalagentid"></span>**LINEERR\_INVALAGENTID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e2108-175">Foi usado um identificador de agente inválido.</span><span class="sxs-lookup"><span data-stu-id="e2108-175">An invalid agent identifier was used.</span></span> <span data-ttu-id="e2108-176">Esse valor é exposto somente a aplicativos que negociam uma versão TAPI do 2,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="e2108-176">This value is exposed only to applications that negotiate a TAPI version of 2.0 or later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2108-177"><span id="LINEERR_INVALAGENTSESSIONSTATE"></span><span id="lineerr_invalagentsessionstate"></span>**LINEERR \_ INVALAGENTSESSIONSTATE**</span><span class="sxs-lookup"><span data-stu-id="e2108-177"><span id="LINEERR_INVALAGENTSESSIONSTATE"></span><span id="lineerr_invalagentsessionstate"></span>**LINEERR\_INVALAGENTSESSIONSTATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e2108-178">O estado da sessão do agente é inválido.</span><span class="sxs-lookup"><span data-stu-id="e2108-178">The agent session state is invalid.</span></span> <span data-ttu-id="e2108-179">Esse valor é exposto somente a aplicativos que negociam uma versão TAPI do 2,2 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="e2108-179">This value is exposed only to applications that negotiate a TAPI version of 2.2 or later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2108-180"><span id="LINEERR_INVALAGENTSTATE"></span><span id="lineerr_invalagentstate"></span>**LINEERR \_ INVALAGENTSTATE**</span><span class="sxs-lookup"><span data-stu-id="e2108-180"><span id="LINEERR_INVALAGENTSTATE"></span><span id="lineerr_invalagentstate"></span>**LINEERR\_INVALAGENTSTATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e2108-181">O estado do agente especificado não é válido ou contém erros.</span><span class="sxs-lookup"><span data-stu-id="e2108-181">The specified agent state is not valid or contains errors.</span></span> <span data-ttu-id="e2108-182">Nenhuma alteração foi feita no estado do agente do endereço especificado.</span><span class="sxs-lookup"><span data-stu-id="e2108-182">No changes have been made to the agent state of the specified address.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2108-183"><span id="LINEERR_INVALAGENTSTATE"></span><span id="lineerr_invalagentstate"></span>**LINEERR \_ INVALAGENTSTATE**</span><span class="sxs-lookup"><span data-stu-id="e2108-183"><span id="LINEERR_INVALAGENTSTATE"></span><span id="lineerr_invalagentstate"></span>**LINEERR\_INVALAGENTSTATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e2108-184">O aplicativo referenciou um estado de agente que não é válido.</span><span class="sxs-lookup"><span data-stu-id="e2108-184">The application referenced an agent state that is not valid.</span></span> <span data-ttu-id="e2108-185">Esse valor é exposto somente a aplicativos que negociam uma versão TAPI do 2,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="e2108-185">This value is exposed only to applications that negotiate a TAPI version of 2.0 or later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2108-186"><span id="LINEERR_INVALAPPHANDLE"></span><span id="lineerr_invalapphandle"></span>**LINEERR \_ INVALAPPHANDLE**</span><span class="sxs-lookup"><span data-stu-id="e2108-186"><span id="LINEERR_INVALAPPHANDLE"></span><span id="lineerr_invalapphandle"></span>**LINEERR\_INVALAPPHANDLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e2108-187">O identificador do aplicativo (como especificado por um parâmetro *hLineApp* ) ou o identificador de registro do aplicativo é inválido.</span><span class="sxs-lookup"><span data-stu-id="e2108-187">The application handle (such as specified by a *hLineApp* parameter) or the application registration handle is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2108-188"><span id="LINEERR_INVALAPPNAME"></span><span id="lineerr_invalappname"></span>**LINEERR \_ INVALAPPNAME**</span><span class="sxs-lookup"><span data-stu-id="e2108-188"><span id="LINEERR_INVALAPPNAME"></span><span id="lineerr_invalappname"></span>**LINEERR\_INVALAPPNAME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e2108-189">O nome do aplicativo especificado é inválido.</span><span class="sxs-lookup"><span data-stu-id="e2108-189">The specified application name is invalid.</span></span> <span data-ttu-id="e2108-190">Se um nome de aplicativo for especificado pelo aplicativo, supõe-se que a cadeia de caracteres não contém nenhum caractere não-reproduzido e terminada com zero.</span><span class="sxs-lookup"><span data-stu-id="e2108-190">If an application name is specified by the application, it is assumed that the string does not contain any non-displayable characters, and is zero-terminated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2108-191"><span id="LINEERR_INVALBEARERMODE"></span><span id="lineerr_invalbearermode"></span>**LINEERR \_ INVALBEARERMODE**</span><span class="sxs-lookup"><span data-stu-id="e2108-191"><span id="LINEERR_INVALBEARERMODE"></span><span id="lineerr_invalbearermode"></span>**LINEERR\_INVALBEARERMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e2108-192">O modo de portador especificado é inválido.</span><span class="sxs-lookup"><span data-stu-id="e2108-192">The specified bearer mode is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2108-193"><span id="LINEERR_INVALCALLCOMPLMODE"></span><span id="lineerr_invalcallcomplmode"></span>**LINEERR \_ INVALCALLCOMPLMODE**</span><span class="sxs-lookup"><span data-stu-id="e2108-193"><span id="LINEERR_INVALCALLCOMPLMODE"></span><span id="lineerr_invalcallcomplmode"></span>**LINEERR\_INVALCALLCOMPLMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e2108-194">A conclusão especificada é inválida.</span><span class="sxs-lookup"><span data-stu-id="e2108-194">The specified completion is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2108-195"><span id="LINEERR_INVALCALLHANDLE"></span><span id="lineerr_invalcallhandle"></span>**LINEERR \_ INVALCALLHANDLE**</span><span class="sxs-lookup"><span data-stu-id="e2108-195"><span id="LINEERR_INVALCALLHANDLE"></span><span id="lineerr_invalcallhandle"></span>**LINEERR\_INVALCALLHANDLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e2108-196">O identificador de chamada especificado não é válido.</span><span class="sxs-lookup"><span data-stu-id="e2108-196">The specified call handle is not valid.</span></span> <span data-ttu-id="e2108-197">Por exemplo, o identificador não é **nulo** , mas não pertence à linha especificada.</span><span class="sxs-lookup"><span data-stu-id="e2108-197">For example, the handle is not **NULL** but does not belong to the given line.</span></span> <span data-ttu-id="e2108-198">Em alguns casos, o identificador do dispositivo de chamada especificado é inválido.</span><span class="sxs-lookup"><span data-stu-id="e2108-198">In some cases, the specified call device handle is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2108-199"><span id="LINEERR_INVALCALLPARAMS"></span><span id="lineerr_invalcallparams"></span>**LINEERR \_ INVALCALLPARAMS**</span><span class="sxs-lookup"><span data-stu-id="e2108-199"><span id="LINEERR_INVALCALLPARAMS"></span><span id="lineerr_invalcallparams"></span>**LINEERR\_INVALCALLPARAMS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e2108-200">Os parâmetros de chamada especificados são inválidos.</span><span class="sxs-lookup"><span data-stu-id="e2108-200">The specified call parameters are invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2108-201"><span id="LINEERR_INVALCALLPRIVILEGE"></span><span id="lineerr_invalcallprivilege"></span>**LINEERR \_ INVALCALLPRIVILEGE**</span><span class="sxs-lookup"><span data-stu-id="e2108-201"><span id="LINEERR_INVALCALLPRIVILEGE"></span><span id="lineerr_invalcallprivilege"></span>**LINEERR\_INVALCALLPRIVILEGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e2108-202">O parâmetro de privilégio de chamada especificado é inválido.</span><span class="sxs-lookup"><span data-stu-id="e2108-202">The specified call privilege parameter is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2108-203"><span id="LINEERR_INVALCALLSELECT"></span><span id="lineerr_invalcallselect"></span>**LINEERR \_ INVALCALLSELECT**</span><span class="sxs-lookup"><span data-stu-id="e2108-203"><span id="LINEERR_INVALCALLSELECT"></span><span id="lineerr_invalcallselect"></span>**LINEERR\_INVALCALLSELECT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e2108-204">O parâmetro Select especificado é inválido.</span><span class="sxs-lookup"><span data-stu-id="e2108-204">The specified select parameter is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2108-205"><span id="LINEERR_INVALCALLSTATE"></span><span id="lineerr_invalcallstate"></span>**LINEERR \_ INVALCALLSTATE**</span><span class="sxs-lookup"><span data-stu-id="e2108-205"><span id="LINEERR_INVALCALLSTATE"></span><span id="lineerr_invalcallstate"></span>**LINEERR\_INVALCALLSTATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e2108-206">O estado atual de uma chamada não está em um estado válido para a operação solicitada.</span><span class="sxs-lookup"><span data-stu-id="e2108-206">The current state of a call is not in a valid state for the requested operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2108-207"><span id="LINEERR_INVALCALLSTATELIST"></span><span id="lineerr_invalcallstatelist"></span>**LINEERR \_ INVALCALLSTATELIST**</span><span class="sxs-lookup"><span data-stu-id="e2108-207"><span id="LINEERR_INVALCALLSTATELIST"></span><span id="lineerr_invalcallstatelist"></span>**LINEERR\_INVALCALLSTATELIST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e2108-208">A lista de Estados da chamada especificada é inválida.</span><span class="sxs-lookup"><span data-stu-id="e2108-208">The specified call state list is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2108-209"><span id="LINEERR_INVALCARD"></span><span id="lineerr_invalcard"></span>**LINEERR \_ INVALCARD**</span><span class="sxs-lookup"><span data-stu-id="e2108-209"><span id="LINEERR_INVALCARD"></span><span id="lineerr_invalcard"></span>**LINEERR\_INVALCARD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e2108-210">O identificador de cartão permanente especificado em *dwCard* não pôde ser encontrado em nenhuma entrada na \[ seção de cartões \] no registro.</span><span class="sxs-lookup"><span data-stu-id="e2108-210">The permanent card identifier specified in *dwCard* could not be found in any entry in the \[Cards\] section in the registry.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2108-211"><span id="LINEERR_INVALCOMPLETIONID"></span><span id="lineerr_invalcompletionid"></span>**LINEERR \_ INVALCOMPLETIONID**</span><span class="sxs-lookup"><span data-stu-id="e2108-211"><span id="LINEERR_INVALCOMPLETIONID"></span><span id="lineerr_invalcompletionid"></span>**LINEERR\_INVALCOMPLETIONID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e2108-212">O identificador de conclusão é inválido.</span><span class="sxs-lookup"><span data-stu-id="e2108-212">The completion identifier is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2108-213"><span id="LINEERR_INVALCONFCALLHANDLE"></span><span id="lineerr_invalconfcallhandle"></span>**LINEERR \_ INVALCONFCALLHANDLE**</span><span class="sxs-lookup"><span data-stu-id="e2108-213"><span id="LINEERR_INVALCONFCALLHANDLE"></span><span id="lineerr_invalconfcallhandle"></span>**LINEERR\_INVALCONFCALLHANDLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e2108-214">O identificador de chamada especificado para a chamada de conferência é inválido ou não é um identificador para uma chamada de conferência.</span><span class="sxs-lookup"><span data-stu-id="e2108-214">The specified call handle for the conference call is invalid or is not a handle for a conference call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2108-215"><span id="LINEERR_INVALCONSULTCALLHANDLE"></span><span id="lineerr_invalconsultcallhandle"></span>**LINEERR \_ INVALCONSULTCALLHANDLE**</span><span class="sxs-lookup"><span data-stu-id="e2108-215"><span id="LINEERR_INVALCONSULTCALLHANDLE"></span><span id="lineerr_invalconsultcallhandle"></span>**LINEERR\_INVALCONSULTCALLHANDLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e2108-216">O identificador de chamada de consulta especificado é inválido.</span><span class="sxs-lookup"><span data-stu-id="e2108-216">The specified consultation call handle is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2108-217"><span id="LINEERR_INVALCOUNTRYCODE"></span><span id="lineerr_invalcountrycode"></span>**LINEERR \_ INVALCOUNTRYCODE**</span><span class="sxs-lookup"><span data-stu-id="e2108-217"><span id="LINEERR_INVALCOUNTRYCODE"></span><span id="lineerr_invalcountrycode"></span>**LINEERR\_INVALCOUNTRYCODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e2108-218">O código de país ou região especificado é inválido.</span><span class="sxs-lookup"><span data-stu-id="e2108-218">The specified country or region code is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2108-219"><span id="LINEERR_INVALDEVICECLASS"></span><span id="lineerr_invaldeviceclass"></span>**LINEERR \_ INVALDEVICECLASS**</span><span class="sxs-lookup"><span data-stu-id="e2108-219"><span id="LINEERR_INVALDEVICECLASS"></span><span id="lineerr_invaldeviceclass"></span>**LINEERR\_INVALDEVICECLASS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e2108-220">O dispositivo de linha não tem dispositivo associado para a classe de dispositivo fornecida ou a linha especificada não oferece suporte à classe de dispositivo indicada.</span><span class="sxs-lookup"><span data-stu-id="e2108-220">The line device has no associated device for the given device class, or the specified line does not support the indicated device class.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2108-221"><span id="LINEERR_INVALDEVICEHANDLE"></span><span id="lineerr_invaldevicehandle"></span>**LINEERR \_ INVALDEVICEHANDLE**</span><span class="sxs-lookup"><span data-stu-id="e2108-221"><span id="LINEERR_INVALDEVICEHANDLE"></span><span id="lineerr_invaldevicehandle"></span>**LINEERR\_INVALDEVICEHANDLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e2108-222">O identificador do dispositivo de linha é inválido.</span><span class="sxs-lookup"><span data-stu-id="e2108-222">The line device handle is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2108-223"><span id="LINEERR_INVALDIALPARAMS"></span><span id="lineerr_invaldialparams"></span>**LINEERR \_ INVALDIALPARAMS**</span><span class="sxs-lookup"><span data-stu-id="e2108-223"><span id="LINEERR_INVALDIALPARAMS"></span><span id="lineerr_invaldialparams"></span>**LINEERR\_INVALDIALPARAMS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e2108-224">Os parâmetros de discagem são inválidos.</span><span class="sxs-lookup"><span data-stu-id="e2108-224">The dialing parameters are invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2108-225"><span id="LINEERR_INVALDIGITLIST"></span><span id="lineerr_invaldigitlist"></span>**LINEERR \_ INVALDIGITLIST**</span><span class="sxs-lookup"><span data-stu-id="e2108-225"><span id="LINEERR_INVALDIGITLIST"></span><span id="lineerr_invaldigitlist"></span>**LINEERR\_INVALDIGITLIST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e2108-226">A lista de dígitos especificada é inválida.</span><span class="sxs-lookup"><span data-stu-id="e2108-226">The specified digit list is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2108-227"><span id="LINEERR_INVALDIGITMODE"></span><span id="lineerr_invaldigitmode"></span>**LINEERR \_ INVALDIGITMODE**</span><span class="sxs-lookup"><span data-stu-id="e2108-227"><span id="LINEERR_INVALDIGITMODE"></span><span id="lineerr_invaldigitmode"></span>**LINEERR\_INVALDIGITMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e2108-228">O modo de dígito especificado é inválido.</span><span class="sxs-lookup"><span data-stu-id="e2108-228">The specified digit mode is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2108-229"><span id="LINEERR_INVALDIGITS"></span><span id="lineerr_invaldigits"></span>**LINEERR \_ INVALDIGITS**</span><span class="sxs-lookup"><span data-stu-id="e2108-229"><span id="LINEERR_INVALDIGITS"></span><span id="lineerr_invaldigits"></span>**LINEERR\_INVALDIGITS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e2108-230">Os dígitos de terminação especificados não são válidos.</span><span class="sxs-lookup"><span data-stu-id="e2108-230">The specified termination digits are not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2108-231"><span id="LINEERR_INVALEXTVERSION"></span><span id="lineerr_invalextversion"></span>**LINEERR \_ INVALEXTVERSION**</span><span class="sxs-lookup"><span data-stu-id="e2108-231"><span id="LINEERR_INVALEXTVERSION"></span><span id="lineerr_invalextversion"></span>**LINEERR\_INVALEXTVERSION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e2108-232">O número de versão da extensão do provedor de serviços é inválido.</span><span class="sxs-lookup"><span data-stu-id="e2108-232">The service provider extension version number is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2108-233"><span id="LINEERR_INVALFEATURE"></span><span id="lineerr_invalfeature"></span>**LINEERR \_ INVALFEATURE**</span><span class="sxs-lookup"><span data-stu-id="e2108-233"><span id="LINEERR_INVALFEATURE"></span><span id="lineerr_invalfeature"></span>**LINEERR\_INVALFEATURE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e2108-234">O parâmetro *dwFeature* é inválido.</span><span class="sxs-lookup"><span data-stu-id="e2108-234">The *dwFeature* parameter is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2108-235"><span id="LINEERR_INVALFEATURE"></span><span id="lineerr_invalfeature"></span>**LINEERR \_ INVALFEATURE**</span><span class="sxs-lookup"><span data-stu-id="e2108-235"><span id="LINEERR_INVALFEATURE"></span><span id="lineerr_invalfeature"></span>**LINEERR\_INVALFEATURE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e2108-236">O aplicativo invocou um recurso que não está disponível nesta linha.</span><span class="sxs-lookup"><span data-stu-id="e2108-236">The application invoked a feature that is not available on this line.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2108-237"><span id="LINEERR_INVALGROUPID"></span><span id="lineerr_invalgroupid"></span>**LINEERR \_ INVALGROUPID**</span><span class="sxs-lookup"><span data-stu-id="e2108-237"><span id="LINEERR_INVALGROUPID"></span><span id="lineerr_invalgroupid"></span>**LINEERR\_INVALGROUPID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e2108-238">O identificador de grupo especificado é inválido.</span><span class="sxs-lookup"><span data-stu-id="e2108-238">The specified group identifier is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2108-239"><span id="LINEERR_INVALLINEHANDLE"></span><span id="lineerr_invallinehandle"></span>**LINEERR \_ INVALLINEHANDLE**</span><span class="sxs-lookup"><span data-stu-id="e2108-239"><span id="LINEERR_INVALLINEHANDLE"></span><span id="lineerr_invallinehandle"></span>**LINEERR\_INVALLINEHANDLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e2108-240">A chamada, o dispositivo, o dispositivo de linha ou o identificador de linha especificado é inválido.</span><span class="sxs-lookup"><span data-stu-id="e2108-240">The specified call, device, line device, or line handle is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2108-241"><span id="LINEERR_INVALLINESTATE"></span><span id="lineerr_invallinestate"></span>**LINEERR \_ INVALLINESTATE**</span><span class="sxs-lookup"><span data-stu-id="e2108-241"><span id="LINEERR_INVALLINESTATE"></span><span id="lineerr_invallinestate"></span>**LINEERR\_INVALLINESTATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e2108-242">A configuração do dispositivo não pode ser alterada no estado de linha atual.</span><span class="sxs-lookup"><span data-stu-id="e2108-242">The device configuration may not be changed in the current line state.</span></span> <span data-ttu-id="e2108-243">A linha pode estar em uso por outro aplicativo ou um parâmetro *dwLineStates* contém um ou mais bits que não são [ \_ constantes LINEDEVSTATE](linedevstate--constants.md).</span><span class="sxs-lookup"><span data-stu-id="e2108-243">The line may be in use by another application or a *dwLineStates* parameter contains one or more bits that are not [LINEDEVSTATE\_ constants](linedevstate--constants.md).</span></span> <span data-ttu-id="e2108-244">O **valor \_ INVALLINESTATE de LINEERR** também pode indicar que o dispositivo está desconectado ou fora do serviço.</span><span class="sxs-lookup"><span data-stu-id="e2108-244">The **LINEERR\_INVALLINESTATE** value can also indicate that the device is disconnected or out of service.</span></span> <span data-ttu-id="e2108-245">Esses Estados são indicados pela configuração dos bits correspondentes aos valores de *InLINEDEVSTATUSFLAGS \_ conectados* e *LINEDEVSTATUSFLAGS \_ InService* para 0 no membro **DwDevStatusFlags** da estrutura [**LINEDEVSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) retornada pela função [**lineGetLineDevStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetlinedevstatus) .</span><span class="sxs-lookup"><span data-stu-id="e2108-245">These states are indicated by setting the bits corresponding to the *LINEDEVSTATUSFLAGS\_CONNECTED* and *LINEDEVSTATUSFLAGS\_INSERVICE* values to 0 in the **dwDevStatusFlags** member of the [**LINEDEVSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) structure returned by the [**lineGetLineDevStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetlinedevstatus) function.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2108-246"><span id="LINEERR_INVALLOCATION"></span><span id="lineerr_invallocation"></span>**LINEERR \_ INVALLOCATION**</span><span class="sxs-lookup"><span data-stu-id="e2108-246"><span id="LINEERR_INVALLOCATION"></span><span id="lineerr_invallocation"></span>**LINEERR\_INVALLOCATION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e2108-247">O identificador de local permanente especificado em *dwLocation* não foi encontrado em nenhuma entrada na \[ seção locais \] no registro.</span><span class="sxs-lookup"><span data-stu-id="e2108-247">The permanent location identifier specified in *dwLocation* could not be found in any entry in the \[Locations\] section in the registry.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2108-248"><span id="LINEERR_INVALMEDIALIST"></span><span id="lineerr_invalmedialist"></span>**LINEERR \_ INVALMEDIALIST**</span><span class="sxs-lookup"><span data-stu-id="e2108-248"><span id="LINEERR_INVALMEDIALIST"></span><span id="lineerr_invalmedialist"></span>**LINEERR\_INVALMEDIALIST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e2108-249">A lista de mídias especificada é inválida.</span><span class="sxs-lookup"><span data-stu-id="e2108-249">The specified media list is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2108-250"><span id="LINEERR_INVALMEDIAMODE"></span><span id="lineerr_invalmediamode"></span>**LINEERR \_ INVALMEDIAMODE**</span><span class="sxs-lookup"><span data-stu-id="e2108-250"><span id="LINEERR_INVALMEDIAMODE"></span><span id="lineerr_invalmediamode"></span>**LINEERR\_INVALMEDIAMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e2108-251">A lista de tipos de mídia (modos) a serem monitorados contém informações inválidas, o parâmetro de tipo de mídia especificado é inválido ou o provedor de serviços não oferece suporte ao tipo de mídia especificado.</span><span class="sxs-lookup"><span data-stu-id="e2108-251">The list of media types (modes) to be monitored contains invalid information, the specified media type parameter is invalid, or the service provider does not support the specified media type.</span></span> <span data-ttu-id="e2108-252">Os tipos de mídia com suporte na linha são listados no membro **dwMediaModes** na estrutura [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) .</span><span class="sxs-lookup"><span data-stu-id="e2108-252">The media types supported on the line are listed in the **dwMediaModes** member in the [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) structure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2108-253"><span id="LINEERR_INVALMESSAGEID"></span><span id="lineerr_invalmessageid"></span>**LINEERR \_ INVALMESSAGEID**</span><span class="sxs-lookup"><span data-stu-id="e2108-253"><span id="LINEERR_INVALMESSAGEID"></span><span id="lineerr_invalmessageid"></span>**LINEERR\_INVALMESSAGEID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e2108-254">O número fornecido em *dwMessageID* está fora do intervalo especificado pelo membro **DwNumCompletionMessages** na estrutura [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) .</span><span class="sxs-lookup"><span data-stu-id="e2108-254">The number given in *dwMessageID* is outside the range specified by the **dwNumCompletionMessages** member in the [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) structure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2108-255"><span id="LINEERR_INVALPARAM"></span><span id="lineerr_invalparam"></span>**LINEERR \_ INVALPARAM**</span><span class="sxs-lookup"><span data-stu-id="e2108-255"><span id="LINEERR_INVALPARAM"></span><span id="lineerr_invalparam"></span>**LINEERR\_INVALPARAM**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e2108-256">Um parâmetro ou uma estrutura que um parâmetro aponta para conter informações inválidas, um país ou código de região inválido, um identificador de janela é inválido ou o parâmetro de lista de encaminhamento especificado contém informações inválidas.</span><span class="sxs-lookup"><span data-stu-id="e2108-256">A parameter or structure that a parameter points to contains invalid information, a country or region code is invalid, a window handle is invalid, or the specified forward list parameter contains invalid information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2108-257"><span id="LINEERR_INVALPARKID"></span><span id="lineerr_invalparkid"></span>**LINEERR \_ INVALPARKID**</span><span class="sxs-lookup"><span data-stu-id="e2108-257"><span id="LINEERR_INVALPARKID"></span><span id="lineerr_invalparkid"></span>**LINEERR\_INVALPARKID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e2108-258">O identificador de estacionamento é inválido.</span><span class="sxs-lookup"><span data-stu-id="e2108-258">The park identifier is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2108-259"><span id="LINEERR_INVALPARKMODE"></span><span id="lineerr_invalparkmode"></span>**LINEERR \_ INVALPARKMODE**</span><span class="sxs-lookup"><span data-stu-id="e2108-259"><span id="LINEERR_INVALPARKMODE"></span><span id="lineerr_invalparkmode"></span>**LINEERR\_INVALPARKMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e2108-260">O modo de estacionamento especificado é inválido.</span><span class="sxs-lookup"><span data-stu-id="e2108-260">The specified park mode is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2108-261"><span id="LINEERR_INVALPASSWORD"></span><span id="lineerr_invalpassword"></span>**LINEERR \_ INVALPASSWORD**</span><span class="sxs-lookup"><span data-stu-id="e2108-261"><span id="LINEERR_INVALPASSWORD"></span><span id="lineerr_invalpassword"></span>**LINEERR\_INVALPASSWORD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e2108-262">A senha especificada não está correta e a ação solicitada não foi executada.</span><span class="sxs-lookup"><span data-stu-id="e2108-262">The specified password is not correct and the requested action has not been carried out.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2108-263"><span id="LINEERR_INVALPASSWORD"></span><span id="lineerr_invalpassword"></span>**LINEERR \_ INVALPASSWORD**</span><span class="sxs-lookup"><span data-stu-id="e2108-263"><span id="LINEERR_INVALPASSWORD"></span><span id="lineerr_invalpassword"></span>**LINEERR\_INVALPASSWORD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e2108-264">O aplicativo usou uma senha inválida.</span><span class="sxs-lookup"><span data-stu-id="e2108-264">The application used an invalid password.</span></span> <span data-ttu-id="e2108-265">Esse valor é exposto somente a aplicativos que negociam uma versão TAPI do 2,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="e2108-265">This value is exposed only to applications that negotiate a TAPI version of 2.0 or later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2108-266"><span id="LINEERR_INVALPOINTER"></span><span id="lineerr_invalpointer"></span>**LINEERR \_ INVALPOINTER**</span><span class="sxs-lookup"><span data-stu-id="e2108-266"><span id="LINEERR_INVALPOINTER"></span><span id="lineerr_invalpointer"></span>**LINEERR\_INVALPOINTER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e2108-267">Um ou mais dos parâmetros de ponteiro especificados (como *lpCallList*, *lpdwAPIVersion*, *lpExtensionID*, *lpdwExtVersion*, *lphIcon*, *lpLineDevCaps* e *lpToneList*) são inválidos ou um ponteiro necessário para um parâmetro de saída é **nulo**.</span><span class="sxs-lookup"><span data-stu-id="e2108-267">One or more of the specified pointer parameters (such as *lpCallList*, *lpdwAPIVersion*, *lpExtensionID*, *lpdwExtVersion*, *lphIcon*, *lpLineDevCaps*, and *lpToneList*) are invalid, or a required pointer to an output parameter is **NULL**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2108-268"><span id="LINEERR_INVALPRIVSELECT"></span><span id="lineerr_invalprivselect"></span>**LINEERR \_ INVALPRIVSELECT**</span><span class="sxs-lookup"><span data-stu-id="e2108-268"><span id="LINEERR_INVALPRIVSELECT"></span><span id="lineerr_invalprivselect"></span>**LINEERR\_INVALPRIVSELECT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e2108-269">Um sinalizador inválido ou uma combinação de sinalizadores foi definida para o parâmetro *dwPrivileges* .</span><span class="sxs-lookup"><span data-stu-id="e2108-269">An invalid flag or combination of flags was set for the *dwPrivileges* parameter.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2108-270"><span id="LINEERR_INVALRATE"></span><span id="lineerr_invalrate"></span>**LINEERR \_ INVALRATE**</span><span class="sxs-lookup"><span data-stu-id="e2108-270"><span id="LINEERR_INVALRATE"></span><span id="lineerr_invalrate"></span>**LINEERR\_INVALRATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e2108-271">A taxa especificada é inválida.</span><span class="sxs-lookup"><span data-stu-id="e2108-271">The specified rate is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2108-272"><span id="LINEERR_INVALREQUESTMODE"></span><span id="lineerr_invalrequestmode"></span>**LINEERR \_ INVALREQUESTMODE**</span><span class="sxs-lookup"><span data-stu-id="e2108-272"><span id="LINEERR_INVALREQUESTMODE"></span><span id="lineerr_invalrequestmode"></span>**LINEERR\_INVALREQUESTMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e2108-273">O indicador [**LINEREQUESTMODE**](linerequestmode--constants.md) é inválido.</span><span class="sxs-lookup"><span data-stu-id="e2108-273">The [**LINEREQUESTMODE**](linerequestmode--constants.md) indicator is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2108-274"><span id="LINEERR_INVALTERMINALID"></span><span id="lineerr_invalterminalid"></span>**LINEERR \_ INVALTERMINALID**</span><span class="sxs-lookup"><span data-stu-id="e2108-274"><span id="LINEERR_INVALTERMINALID"></span><span id="lineerr_invalterminalid"></span>**LINEERR\_INVALTERMINALID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e2108-275">O identificador de terminal especificado é inválido.</span><span class="sxs-lookup"><span data-stu-id="e2108-275">The specified terminal identifier is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2108-276"><span id="LINEERR_INVALTERMINALMODE"></span><span id="lineerr_invalterminalmode"></span>**LINEERR \_ INVALTERMINALMODE**</span><span class="sxs-lookup"><span data-stu-id="e2108-276"><span id="LINEERR_INVALTERMINALMODE"></span><span id="lineerr_invalterminalmode"></span>**LINEERR\_INVALTERMINALMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e2108-277">O parâmetro de modos de terminal especificado é inválido.</span><span class="sxs-lookup"><span data-stu-id="e2108-277">The specified terminal modes parameter is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2108-278"><span id="LINEERR_INVALTIMEOUT"></span><span id="lineerr_invaltimeout"></span>**LINEERR \_ INVALTIMEOUT**</span><span class="sxs-lookup"><span data-stu-id="e2108-278"><span id="LINEERR_INVALTIMEOUT"></span><span id="lineerr_invaltimeout"></span>**LINEERR\_INVALTIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e2108-279">Não há suporte para tempos limite ou um valor fica fora do intervalo válido especificado em [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps).</span><span class="sxs-lookup"><span data-stu-id="e2108-279">Timeouts are not supported or a value falls outside the valid range specified in [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2108-280"><span id="LINEERR_INVALTONE"></span><span id="lineerr_invaltone"></span>**LINEERR \_ INVALTONE**</span><span class="sxs-lookup"><span data-stu-id="e2108-280"><span id="LINEERR_INVALTONE"></span><span id="lineerr_invaltone"></span>**LINEERR\_INVALTONE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e2108-281">O Tom personalizado especificado não representa um tom válido ou é composto de muitas frequências ou a estrutura de tons especificada não descreve um tom válido.</span><span class="sxs-lookup"><span data-stu-id="e2108-281">The specified custom tone does not represent a valid tone or is made up of too many frequencies or the specified tone structure does not describe a valid tone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2108-282"><span id="LINEERR_INVALTONELIST"></span><span id="lineerr_invaltonelist"></span>**LINEERR \_ INVALTONELIST**</span><span class="sxs-lookup"><span data-stu-id="e2108-282"><span id="LINEERR_INVALTONELIST"></span><span id="lineerr_invaltonelist"></span>**LINEERR\_INVALTONELIST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e2108-283">A lista de tons especificada é inválida.</span><span class="sxs-lookup"><span data-stu-id="e2108-283">The specified tone list is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2108-284"><span id="LINEERR_INVALTONEMODE"></span><span id="lineerr_invaltonemode"></span>**LINEERR \_ INVALTONEMODE**</span><span class="sxs-lookup"><span data-stu-id="e2108-284"><span id="LINEERR_INVALTONEMODE"></span><span id="lineerr_invaltonemode"></span>**LINEERR\_INVALTONEMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e2108-285">O parâmetro de modo de Tom especificado é inválido.</span><span class="sxs-lookup"><span data-stu-id="e2108-285">The specified tone mode parameter is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2108-286"><span id="LINEERR_INVALTRANSFERMODE"></span><span id="lineerr_invaltransfermode"></span>**LINEERR \_ INVALTRANSFERMODE**</span><span class="sxs-lookup"><span data-stu-id="e2108-286"><span id="LINEERR_INVALTRANSFERMODE"></span><span id="lineerr_invaltransfermode"></span>**LINEERR\_INVALTRANSFERMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e2108-287">O parâmetro do modo de transferência especificado é inválido.</span><span class="sxs-lookup"><span data-stu-id="e2108-287">The specified transfer mode parameter is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2108-288"><span id="LINEERR_LINEMAPPERFAILED"></span><span id="lineerr_linemapperfailed"></span>**LINEERR \_ LINEMAPPERFAILED**</span><span class="sxs-lookup"><span data-stu-id="e2108-288"><span id="LINEERR_LINEMAPPERFAILED"></span><span id="lineerr_linemapperfailed"></span>**LINEERR\_LINEMAPPERFAILED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e2108-289">LINEMAPPER foi o valor passado no parâmetro *dwDeviceID* , mas não foram encontradas linhas que correspondam aos requisitos especificados no parâmetro *lpCallParams* .</span><span class="sxs-lookup"><span data-stu-id="e2108-289">LINEMAPPER was the value passed in the *dwDeviceID* parameter, but no lines were found that match the requirements specified in the *lpCallParams* parameter.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2108-290"><span id="LINEERR_NOCONFERENCE"></span><span id="lineerr_noconference"></span>**LINEERR \_ NOconferência**</span><span class="sxs-lookup"><span data-stu-id="e2108-290"><span id="LINEERR_NOCONFERENCE"></span><span id="lineerr_noconference"></span>**LINEERR\_NOCONFERENCE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e2108-291">A chamada especificada não é um identificador de chamada de conferência ou uma chamada de participante.</span><span class="sxs-lookup"><span data-stu-id="e2108-291">The specified call is not a conference call handle or a participant call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2108-292"><span id="LINEERR_NODEVICE"></span><span id="lineerr_nodevice"></span>**LINEERR \_ NOdevice**</span><span class="sxs-lookup"><span data-stu-id="e2108-292"><span id="LINEERR_NODEVICE"></span><span id="lineerr_nodevice"></span>**LINEERR\_NODEVICE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e2108-293">O identificador de dispositivo especificado, que era válido anteriormente, não é mais aceito porque o dispositivo associado foi removido do sistema desde que a TAPI foi inicializada pela última vez.</span><span class="sxs-lookup"><span data-stu-id="e2108-293">The specified device identifier, which was previously valid, is no longer accepted because the associated device has been removed from the system since TAPI was last initialized.</span></span> <span data-ttu-id="e2108-294">Como alternativa, o dispositivo de linha não tem nenhum dispositivo associado para a classe de dispositivo fornecida.</span><span class="sxs-lookup"><span data-stu-id="e2108-294">Alternately, the line device has no associated device for the given device class.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2108-295"><span id="LINEERR_NODRIVER"></span><span id="lineerr_nodriver"></span>**LINEERR \_ NOunidade**</span><span class="sxs-lookup"><span data-stu-id="e2108-295"><span id="LINEERR_NODRIVER"></span><span id="lineerr_nodriver"></span>**LINEERR\_NODRIVER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e2108-296">Não foi possível localizar o Tapiaddr.dll ou o provedor de serviços de telefonia para o dispositivo especificado descobriu que um de seus componentes está ausente ou corrompido de uma forma que não foi detectada no momento da inicialização.</span><span class="sxs-lookup"><span data-stu-id="e2108-296">Either Tapiaddr.dll could not be located or the telephone service provider for the specified device found that one of its components is missing or corrupt in a way that was not detected at initialization time.</span></span> <span data-ttu-id="e2108-297">O usuário deve ser aconselhado a usar o painel de controle de telefonia para corrigir o problema.</span><span class="sxs-lookup"><span data-stu-id="e2108-297">The user should be advised to use the Telephony Control Panel to correct the problem.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2108-298"><span id="LINEERR_NOMEM"></span><span id="lineerr_nomem"></span>**nome do LINEERR \_**</span><span class="sxs-lookup"><span data-stu-id="e2108-298"><span id="LINEERR_NOMEM"></span><span id="lineerr_nomem"></span>**LINEERR\_NOMEM**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e2108-299">Memória insuficiente para executar a operação ou não é possível bloquear a memória.</span><span class="sxs-lookup"><span data-stu-id="e2108-299">Insufficient memory to perform the operation, or unable to lock memory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2108-300"><span id="LINEERR_NOMULTIPLEINSTANCE"></span><span id="lineerr_nomultipleinstance"></span>**LINEERR \_ NOMULTIPLEINSTANCE**</span><span class="sxs-lookup"><span data-stu-id="e2108-300"><span id="LINEERR_NOMULTIPLEINSTANCE"></span><span id="lineerr_nomultipleinstance"></span>**LINEERR\_NOMULTIPLEINSTANCE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e2108-301">Um provedor de serviços de telefonia que não dá suporte a várias instâncias é listado mais de uma vez \[ na \] seção de provedores no registro.</span><span class="sxs-lookup"><span data-stu-id="e2108-301">A telephony service provider that does not support multiple instances is listed more than once in the \[Providers\] section in the registry.</span></span> <span data-ttu-id="e2108-302">O aplicativo deve aconselhar o usuário a usar o painel de controle de telefonia para remover o driver duplicado.</span><span class="sxs-lookup"><span data-stu-id="e2108-302">The application should advise the user to use the Telephony Control Panel to remove the duplicated driver.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2108-303"><span id="LINEERR_NOMULTIPLEINSTANCE"></span><span id="lineerr_nomultipleinstance"></span>**LINEERR \_ NOMULTIPLEINSTANCE**</span><span class="sxs-lookup"><span data-stu-id="e2108-303"><span id="LINEERR_NOMULTIPLEINSTANCE"></span><span id="lineerr_nomultipleinstance"></span>**LINEERR\_NOMULTIPLEINSTANCE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e2108-304">Várias instâncias deste provedor de serviços não são permitidas.</span><span class="sxs-lookup"><span data-stu-id="e2108-304">Multiple instances of this service provider are not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2108-305"><span id="LINEERR_NOREQUEST"></span><span id="lineerr_norequest"></span>**LINEERR \_ NOrequest**</span><span class="sxs-lookup"><span data-stu-id="e2108-305"><span id="LINEERR_NOREQUEST"></span><span id="lineerr_norequest"></span>**LINEERR\_NOREQUEST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e2108-306">No momento, não há nenhuma solicitação pendente do modo indicado ou o aplicativo não é mais o aplicativo de prioridade mais alta para o modo de solicitação especificado.</span><span class="sxs-lookup"><span data-stu-id="e2108-306">There currently is no request pending of the indicated mode, or the application is no longer the highest-priority application for the specified request mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2108-307"><span id="LINEERR_NOTOWNER"></span><span id="lineerr_notowner"></span>**LINEERR \_ NOcidade**</span><span class="sxs-lookup"><span data-stu-id="e2108-307"><span id="LINEERR_NOTOWNER"></span><span id="lineerr_notowner"></span>**LINEERR\_NOTOWNER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e2108-308">O aplicativo não tem o privilégio de proprietário para a chamada especificada.</span><span class="sxs-lookup"><span data-stu-id="e2108-308">The application does not have owner privilege to the specified call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2108-309"><span id="LINEERR_NOTREGISTERED"></span><span id="lineerr_notregistered"></span>**LINEERR não \_ registrado**</span><span class="sxs-lookup"><span data-stu-id="e2108-309"><span id="LINEERR_NOTREGISTERED"></span><span id="lineerr_notregistered"></span>**LINEERR\_NOTREGISTERED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e2108-310">O aplicativo não está registrado como um destinatário de solicitação para o modo de solicitação indicado.</span><span class="sxs-lookup"><span data-stu-id="e2108-310">The application is not registered as a request recipient for the indicated request mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2108-311"><span id="LINEERR_OPERATIONFAILED"></span><span id="lineerr_operationfailed"></span>**LINEERR \_ OPERATIONFAILED**</span><span class="sxs-lookup"><span data-stu-id="e2108-311"><span id="LINEERR_OPERATIONFAILED"></span><span id="lineerr_operationfailed"></span>**LINEERR\_OPERATIONFAILED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e2108-312">A operação falhou por um motivo desconhecido ou não especificado.</span><span class="sxs-lookup"><span data-stu-id="e2108-312">The operation failed for an unspecified or unknown reason.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2108-313"><span id="LINEERR_OPERATIONUNAVAIL"></span><span id="lineerr_operationunavail"></span>**LINEERR \_ OPERATIONUNAVAIL**</span><span class="sxs-lookup"><span data-stu-id="e2108-313"><span id="LINEERR_OPERATIONUNAVAIL"></span><span id="lineerr_operationunavail"></span>**LINEERR\_OPERATIONUNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e2108-314">A operação não está disponível, por exemplo, para o dispositivo especificado ou para a linha especificada.</span><span class="sxs-lookup"><span data-stu-id="e2108-314">The operation is not available, such as for the given device or specified line.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2108-315"><span id="LINEERR_RATEUNAVAIL"></span><span id="lineerr_rateunavail"></span>**LINEERR \_ RATEUNAVAIL**</span><span class="sxs-lookup"><span data-stu-id="e2108-315"><span id="LINEERR_RATEUNAVAIL"></span><span id="lineerr_rateunavail"></span>**LINEERR\_RATEUNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e2108-316">O provedor de serviços atualmente não tem largura de banda suficiente disponível para a taxa especificada.</span><span class="sxs-lookup"><span data-stu-id="e2108-316">The service provider currently does not have enough bandwidth available for the specified rate.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2108-317"><span id="LINEERR_REINIT"></span><span id="lineerr_reinit"></span>**reinicialização do LINEERR \_**</span><span class="sxs-lookup"><span data-stu-id="e2108-317"><span id="LINEERR_REINIT"></span><span id="lineerr_reinit"></span>**LINEERR\_REINIT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e2108-318">Se a reinicialização da TAPI tiver sido solicitada, por exemplo, como resultado da adição ou remoção de um provedor de serviços de telefonia, as solicitações [**lineInitialize**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize), [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa)ou [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen) serão rejeitadas com esse erro até que o último aplicativo desligue seu uso da API (usando [**lineShutdown**](/windows/desktop/api/Tapi/nf-tapi-lineshutdown)), quando a nova configuração entrar em vigor e os aplicativos forem novamente permitidos para chamar **lineInitialize** ou **lineInitializeEx**.</span><span class="sxs-lookup"><span data-stu-id="e2108-318">If TAPI reinitialization has been requested, for example as a result of adding or removing a telephony service provider, then [**lineInitialize**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize), [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa), or [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen) requests are rejected with this error until the last application shuts down its usage of the API (using [**lineShutdown**](/windows/desktop/api/Tapi/nf-tapi-lineshutdown)), at which time the new configuration becomes effective and applications are once again permitted to call **lineInitialize** or **lineInitializeEx**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2108-319"><span id="LINEERR_REINIT"></span><span id="lineerr_reinit"></span>**reinicialização do LINEERR \_**</span><span class="sxs-lookup"><span data-stu-id="e2108-319"><span id="LINEERR_REINIT"></span><span id="lineerr_reinit"></span>**LINEERR\_REINIT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e2108-320">O aplicativo tentou inicializar a TAPI duas vezes.</span><span class="sxs-lookup"><span data-stu-id="e2108-320">The application attempted to initialize TAPI twice.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2108-321"><span id="LINEERR_REQUESTOVERRUN"></span><span id="lineerr_requestoverrun"></span>**LINEERR \_ REQUESTOVERRUN**</span><span class="sxs-lookup"><span data-stu-id="e2108-321"><span id="LINEERR_REQUESTOVERRUN"></span><span id="lineerr_requestoverrun"></span>**LINEERR\_REQUESTOVERRUN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e2108-322">Mais solicitações estão pendentes que o dispositivo pode manipular.</span><span class="sxs-lookup"><span data-stu-id="e2108-322">More requests are pending than the device can handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2108-323"><span id="LINEERR_RESOURCEUNAVAIL"></span><span id="lineerr_resourceunavail"></span>**LINEERR \_ RESOURCEUNAVAIL**</span><span class="sxs-lookup"><span data-stu-id="e2108-323"><span id="LINEERR_RESOURCEUNAVAIL"></span><span id="lineerr_resourceunavail"></span>**LINEERR\_RESOURCEUNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e2108-324">Recursos insuficientes para concluir a operação.</span><span class="sxs-lookup"><span data-stu-id="e2108-324">Insufficient resources to complete the operation.</span></span> <span data-ttu-id="e2108-325">Por exemplo, uma linha não pode ser aberta devido a um sobrecompromisso de recurso dinâmico.</span><span class="sxs-lookup"><span data-stu-id="e2108-325">For example, a line cannot be opened due to a dynamic resource overcommitment.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2108-326"><span id="LINEERR_STRUCTURETOOSMALL"></span><span id="lineerr_structuretoosmall"></span>**LINEERR \_ STRUCTURETOOSMALL**</span><span class="sxs-lookup"><span data-stu-id="e2108-326"><span id="LINEERR_STRUCTURETOOSMALL"></span><span id="lineerr_structuretoosmall"></span>**LINEERR\_STRUCTURETOOSMALL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e2108-327">O membro **dwTotalSize** de uma estrutura não especifica memória suficiente para conter a parte fixa da estrutura especificada.</span><span class="sxs-lookup"><span data-stu-id="e2108-327">The **dwTotalSize** member of a structure does not specify enough memory to contain the fixed portion of the specified structure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2108-328"><span id="LINEERR_TARGETNOTFOUND"></span><span id="lineerr_targetnotfound"></span>**LINEERR \_ TARGETNOTFOUND**</span><span class="sxs-lookup"><span data-stu-id="e2108-328"><span id="LINEERR_TARGETNOTFOUND"></span><span id="lineerr_targetnotfound"></span>**LINEERR\_TARGETNOTFOUND**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e2108-329">Não foi encontrado um destino para a entrega de chamada.</span><span class="sxs-lookup"><span data-stu-id="e2108-329">A target for the call handoff was not found.</span></span> <span data-ttu-id="e2108-330">Isso pode ocorrer se o aplicativo nomeado não abriu a mesma linha com o bit do \_ proprietário LINECALLPRIVILEGE no parâmetro *DwPrivileges* de [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen).</span><span class="sxs-lookup"><span data-stu-id="e2108-330">This can occur if the named application did not open the same line with the LINECALLPRIVILEGE\_OWNER bit in the *dwPrivileges* parameter of [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen).</span></span> <span data-ttu-id="e2108-331">Ou, no caso de entrega no modo de mídia, nenhum aplicativo abriu a mesma linha com o bit do \_ proprietário LINECALLPRIVILEGE no parâmetro *DwPrivileges* de [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen) e com o tipo de mídia especificado no parâmetro *DwMediaMode* que foi especificado no parâmetro *dwMediaModes* de [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen).</span><span class="sxs-lookup"><span data-stu-id="e2108-331">Or, in the case of media-mode handoff, no application has opened the same line with the LINECALLPRIVILEGE\_OWNER bit in the *dwPrivileges* parameter of [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen) and with the media type specified in the *dwMediaMode* parameter having been specified in the *dwMediaModes* parameter of [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2108-332"><span id="LINEERR_TARGETSELF"></span><span id="lineerr_targetself"></span>**LINEERR \_ TARGETSELF**</span><span class="sxs-lookup"><span data-stu-id="e2108-332"><span id="LINEERR_TARGETSELF"></span><span id="lineerr_targetself"></span>**LINEERR\_TARGETSELF**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e2108-333">O aplicativo que invoca essa operação é o destino da entrega indireta.</span><span class="sxs-lookup"><span data-stu-id="e2108-333">The application invoking this operation is the target of the indirect handoff.</span></span> <span data-ttu-id="e2108-334">Ou seja, a TAPI determinou que o aplicativo de chamada também é o aplicativo de prioridade mais alta para o tipo de mídia fornecido.</span><span class="sxs-lookup"><span data-stu-id="e2108-334">That is, TAPI has determined that the calling application is also the highest priority application for the given media type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2108-335"><span id="LINEERR_UNINITIALIZED"></span><span id="lineerr_uninitialized"></span>**LINEERR não \_ inicializado**</span><span class="sxs-lookup"><span data-stu-id="e2108-335"><span id="LINEERR_UNINITIALIZED"></span><span id="lineerr_uninitialized"></span>**LINEERR\_UNINITIALIZED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e2108-336">A operação foi invocada antes de qualquer aplicativo chamado [**lineInitialize**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize) ou [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa).</span><span class="sxs-lookup"><span data-stu-id="e2108-336">The operation was invoked before any application called [**lineInitialize**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize) or [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2108-337"><span id="LINEERR_USERCANCELLED"></span><span id="lineerr_usercancelled"></span>**LINEERR \_ USERcanceled**</span><span class="sxs-lookup"><span data-stu-id="e2108-337"><span id="LINEERR_USERCANCELLED"></span><span id="lineerr_usercancelled"></span>**LINEERR\_USERCANCELLED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e2108-338">O usuário cancelou a chamada.</span><span class="sxs-lookup"><span data-stu-id="e2108-338">The user cancelled the call.</span></span> <span data-ttu-id="e2108-339">Esse valor é exposto somente a aplicativos que negociam uma versão TAPI do 2,2 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="e2108-339">This value is exposed only to applications that negotiate a TAPI version of 2.2 or later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2108-340"><span id="LINEERR_USERUSERINFOTOOBIG"></span><span id="lineerr_useruserinfotoobig"></span>**LINEERR \_ USERUSERINFOTOOBIG**</span><span class="sxs-lookup"><span data-stu-id="e2108-340"><span id="LINEERR_USERUSERINFOTOOBIG"></span><span id="lineerr_useruserinfotoobig"></span>**LINEERR\_USERUSERINFOTOOBIG**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e2108-341">A cadeia de caracteres que contém informações de usuário do usuário excede o número máximo de bytes especificado no membro **dwUUIAcceptSize**, **dwUUIAnswerSize**, **dwUUIDropSize**, **dwUUIMakeCallSize** ou **dwUUISendUserUserInfoSize** de [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps), ou a cadeia de caracteres que contém as informações do usuário do usuário é muito longa.</span><span class="sxs-lookup"><span data-stu-id="e2108-341">The string containing user-user information exceeds the maximum number of bytes specified in the **dwUUIAcceptSize**, **dwUUIAnswerSize**, **dwUUIDropSize**, **dwUUIMakeCallSize**, or **dwUUISendUserUserInfoSize** member of [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps), or the string containing user-user information is too long.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e2108-342">Comentários</span><span class="sxs-lookup"><span data-stu-id="e2108-342">Remarks</span></span>

<span data-ttu-id="e2108-343">Os valores de 0xC0000000 a 0xFFFFFFFF estão disponíveis para extensões específicas do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e2108-343">The values 0xC0000000 through 0xFFFFFFFF are available for device-specific extensions.</span></span> <span data-ttu-id="e2108-344">Os valores 0x80000000 a 0xBFFFFFFF são reservados, enquanto 0x00000000 a 0x7FFFFFFF são usados como identificadores de solicitação.</span><span class="sxs-lookup"><span data-stu-id="e2108-344">The values 0x80000000 through 0xBFFFFFFF are reserved, while 0x00000000 through 0x7FFFFFFF are used as request identifiers.</span></span>

<span data-ttu-id="e2108-345">Se um aplicativo receber um erro retornando que ele não trata especificamente (como um erro definido por uma extensão específica do dispositivo), ele deve tratar o erro como um LINEERR \_ OPERATIONFAILED (por um motivo não especificado).</span><span class="sxs-lookup"><span data-stu-id="e2108-345">If an application gets an error return that it does not specifically handle (such as an error defined by a device-specific extension), it should treat the error as a LINEERR\_OPERATIONFAILED (for an unspecified reason).</span></span>

<span data-ttu-id="e2108-346">Ao invocar as \_ constantes LINEERR que são novas com a TAPI 3,0, o arquivo Tapierr.MC deve ser atualizado com novas mensagens.</span><span class="sxs-lookup"><span data-stu-id="e2108-346">When invoking the LINEERR\_constants which are new with TAPI 3.0, the Tapierr.mc file must be updated with new messages.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2108-347">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e2108-347">Requirements</span></span>



| <span data-ttu-id="e2108-348">Requisito</span><span class="sxs-lookup"><span data-stu-id="e2108-348">Requirement</span></span> | <span data-ttu-id="e2108-349">Valor</span><span class="sxs-lookup"><span data-stu-id="e2108-349">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="e2108-350">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="e2108-350">TAPI version</span></span><br/> | <span data-ttu-id="e2108-351">Requer TAPI 2,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="e2108-351">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="e2108-352">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e2108-352">Header</span></span><br/>       | <dl> <span data-ttu-id="e2108-353"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="e2108-353"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2108-354">Confira também</span><span class="sxs-lookup"><span data-stu-id="e2108-354">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2108-355">**LINEADDRESSCAPS**</span><span class="sxs-lookup"><span data-stu-id="e2108-355">**LINEADDRESSCAPS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)
</dt> <dt>

[<span data-ttu-id="e2108-356">**LINEDEVCAPS**</span><span class="sxs-lookup"><span data-stu-id="e2108-356">**LINEDEVCAPS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linedevcaps)
</dt> <dt>

[<span data-ttu-id="e2108-357">**LINEDEVSTATUS**</span><span class="sxs-lookup"><span data-stu-id="e2108-357">**LINEDEVSTATUS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linedevstatus)
</dt> <dt>

[<span data-ttu-id="e2108-358">**lineGetLineDevStatus**</span><span class="sxs-lookup"><span data-stu-id="e2108-358">**lineGetLineDevStatus**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetlinedevstatus)
</dt> <dt>

[<span data-ttu-id="e2108-359">**lineInitialize**</span><span class="sxs-lookup"><span data-stu-id="e2108-359">**lineInitialize**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineinitialize)
</dt> <dt>

[<span data-ttu-id="e2108-360">**lineInitializeEx**</span><span class="sxs-lookup"><span data-stu-id="e2108-360">**lineInitializeEx**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa)
</dt> <dt>

[<span data-ttu-id="e2108-361">**lineOpen**</span><span class="sxs-lookup"><span data-stu-id="e2108-361">**lineOpen**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineopen)
</dt> <dt>

[<span data-ttu-id="e2108-362">**lineShutdown**</span><span class="sxs-lookup"><span data-stu-id="e2108-362">**lineShutdown**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineshutdown)
</dt> </dl>

 

 




