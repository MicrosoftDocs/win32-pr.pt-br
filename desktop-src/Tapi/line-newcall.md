---
description: A mensagem de NewCall da linha TSPI \_ é enviada para a função de retorno de chamada LINEEVENT sempre que uma nova chamada que a TAPI não originou chega em uma linha aberta pela TAPI.
ms.assetid: 36122dfb-1ed6-459d-aa2b-69c86daaddd8
title: Mensagem de LINE_NEWCALL (TSPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed3e7380b2f328283e5f5cad9e84f5a1d0c450dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105796319"
---
# <a name="line_newcall-message"></a><span data-ttu-id="81f99-103">Mensagem de NewCall de linha \_</span><span class="sxs-lookup"><span data-stu-id="81f99-103">LINE\_NEWCALL message</span></span>

<span data-ttu-id="81f99-104">A mensagem **de \_ NewCall da linha** TSPI é enviada para a função de retorno de chamada [**LINEEVENT**](/windows/win32/api/tspi/nc-tspi-lineevent) sempre que uma nova chamada que a TAPI não originou chega em uma linha aberta pela TAPI.</span><span class="sxs-lookup"><span data-stu-id="81f99-104">The TSPI **LINE\_NEWCALL** message is sent to the [**LINEEVENT**](/windows/win32/api/tspi/nc-tspi-lineevent) callback function whenever a new call that TAPI has not originated arrives on a line that TAPI has open.</span></span> <span data-ttu-id="81f99-105">Essa deve ser a primeira mensagem enviada referente a essa chamada.</span><span class="sxs-lookup"><span data-stu-id="81f99-105">This must be the first message sent regarding that call.</span></span> <span data-ttu-id="81f99-106">A TAPI grava o identificador opaco *htCall* no local passado pelo provedor de serviços como *dwParam2*.</span><span class="sxs-lookup"><span data-stu-id="81f99-106">TAPI writes the *htCall* opaque handle to the location passed by the service provider as *dwParam2*.</span></span> <span data-ttu-id="81f99-107">Isso fornece ao provedor de serviços o valor de *htCall* a ser usado nas mensagens subsequentes.</span><span class="sxs-lookup"><span data-stu-id="81f99-107">This gives the service provider the *htCall* value to be used in subsequent messages.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="81f99-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="81f99-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81f99-109">*htLine*</span><span class="sxs-lookup"><span data-stu-id="81f99-109">*htLine*</span></span> 
</dt> <dd>

<span data-ttu-id="81f99-110">O identificador de objeto TAPI opaco para o dispositivo de linha.</span><span class="sxs-lookup"><span data-stu-id="81f99-110">The TAPI opaque object handle to the line device.</span></span>

</dd> <dt>

<span data-ttu-id="81f99-111">*htCall*</span><span class="sxs-lookup"><span data-stu-id="81f99-111">*htCall*</span></span> 
</dt> <dd>

<span data-ttu-id="81f99-112">Não utilizado.</span><span class="sxs-lookup"><span data-stu-id="81f99-112">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="81f99-113">*dwMsg*</span><span class="sxs-lookup"><span data-stu-id="81f99-113">*dwMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="81f99-114">A linha de valor \_ NewCall.</span><span class="sxs-lookup"><span data-stu-id="81f99-114">The value LINE\_NEWCALL.</span></span>

</dd> <dt>

<span data-ttu-id="81f99-115">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="81f99-115">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="81f99-116">O identificador opaco do provedor de serviço para a chamada, do tipo [**HDRVCALL**](hdrvline.md).</span><span class="sxs-lookup"><span data-stu-id="81f99-116">The service provider's opaque handle for the call, of type [**HDRVCALL**](hdrvline.md).</span></span> <span data-ttu-id="81f99-117">A TAPI passa esse valor como o parâmetro *hdCall* para identificar a chamada nos procedimentos subsequentes que ele invoca para operar na chamada.</span><span class="sxs-lookup"><span data-stu-id="81f99-117">TAPI passes this value as the *hdCall* parameter to identify the call in subsequent procedures it invokes to operate on the call.</span></span>

</dd> <dt>

<span data-ttu-id="81f99-118">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="81f99-118">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="81f99-119">Um ponteiro do tipo LPHTAPICALL apontando para um [**HTAPICALL**](htapicall.md).</span><span class="sxs-lookup"><span data-stu-id="81f99-119">A pointer of type LPHTAPICALL pointing to a [**HTAPICALL**](htapicall.md).</span></span> <span data-ttu-id="81f99-120">A TAPI grava o identificador opaco TAPI para a chamada para o local indicado.</span><span class="sxs-lookup"><span data-stu-id="81f99-120">TAPI writes the TAPI opaque handle for the call to the indicated location.</span></span> <span data-ttu-id="81f99-121">O provedor de serviços deve salvar esse valor e passá-lo como o parâmetro *htCall* para identificar a chamada em eventos subsequentes que ele relata para a chamada.</span><span class="sxs-lookup"><span data-stu-id="81f99-121">The service provider must save this value and pass it as the *htCall* parameter to identify the call in subsequent events it reports for the call.</span></span>

<span data-ttu-id="81f99-122">Esse parâmetro também pode adquirir um valor de **NULL** (consulte a seção de comentários a seguir).</span><span class="sxs-lookup"><span data-stu-id="81f99-122">This parameter can also acquire a value of **NULL** (see the following Remarks section).</span></span>

</dd> <dt>

<span data-ttu-id="81f99-123">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="81f99-123">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="81f99-124">Não utilizado.</span><span class="sxs-lookup"><span data-stu-id="81f99-124">Unused.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="81f99-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="81f99-125">Remarks</span></span>

<span data-ttu-id="81f99-126">O provedor de serviços deve enviar a mensagem [**\_ callstate de linha**](/previous-versions/windows/desktop/legacy/ms725219(v=vs.85)) como a próxima mensagem para essa chamada.</span><span class="sxs-lookup"><span data-stu-id="81f99-126">The service provider should send the [**LINE\_CALLSTATE**](/previous-versions/windows/desktop/legacy/ms725219(v=vs.85)) message as the next message for this call.</span></span> <span data-ttu-id="81f99-127">O evento **line \_ NewCall** é incomum, pois ele também passa um valor de volta para o provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="81f99-127">The **LINE\_NEWCALL** event is unusual in that it also passes a value back to the service provider.</span></span>

<span data-ttu-id="81f99-128">Essa função relata quaisquer novas chamadas originadas no provedor de serviços (entrada, saída, iniciadas no telefone e assim por diante) para as quais a TAPI e o provedor de serviços ainda não alteraram os identificadores opacos.</span><span class="sxs-lookup"><span data-stu-id="81f99-128">This function reports any new calls that originate in the service provider (inbound, outbound, initiated at the phone, and so on) for which TAPI and the service provider have not yet exchanged opaque handles.</span></span> <span data-ttu-id="81f99-129">Os identificadores são trocados para que a TAPI e o provedor de serviços possam, subsequentemente, fazer solicitações e relatar eventos que envolvam a chamada.</span><span class="sxs-lookup"><span data-stu-id="81f99-129">The handles are exchanged so that TAPI and the service provider can subsequently make requests and report events involving the call.</span></span> <span data-ttu-id="81f99-130">Como essas novas chamadas não são necessariamente de entrada, as chamadas podem inicialmente estar em qualquer Estado, não necessariamente no estado de *oferta* .</span><span class="sxs-lookup"><span data-stu-id="81f99-130">Because these new calls are not necessarily inbound, the calls can initially be in any state, not necessarily the *offering* state.</span></span> <span data-ttu-id="81f99-131">Se o provedor de serviços for iniciado e descobre que uma ou mais chamadas já estão ativas na linha, ela informará a TAPI delas com mensagens de **\_ NewCall de linha** seguidas por mensagens [**\_ callstate de linha**](/previous-versions/windows/desktop/legacy/ms725219(v=vs.85)) que indicam o estado atual.</span><span class="sxs-lookup"><span data-stu-id="81f99-131">If the service provider starts and discovers that one or more calls are already active on the line, it informs TAPI of them with **LINE\_NEWCALL** messages followed by [**LINE\_CALLSTATE**](/previous-versions/windows/desktop/legacy/ms725219(v=vs.85)) messages indicating the current state.</span></span> <span data-ttu-id="81f99-132">Uma nova chamada de saída, iniciada no telefone pelo usuário, seria relatada com uma **mensagem \_ NewCall de linha** e a mensagem **\_ callstate de linha** inicial indicaria que a chamada estava no estado de **sinal** de discagem (e continuando a partir daí).</span><span class="sxs-lookup"><span data-stu-id="81f99-132">A new outgoing call, initiated on the phone by the user, would be reported with a **LINE\_NEWCALL** message, and the initial **LINE\_CALLSTATE** message would indicate that the call was in **DIALTONE** state (and then continuing on from there).</span></span>

<span data-ttu-id="81f99-133">Se o provedor de serviços passar um grande número de chamadas para a TAPI em um período muito curto (durante o mesmo ciclo de interrupção), a TAPI poderá ficar registrada no processamento dessas chamadas.</span><span class="sxs-lookup"><span data-stu-id="81f99-133">If the service provider passes a large number of calls to TAPI in a very short amount of time (during the same interrupt cycle), TAPI can become backlogged in processing those calls.</span></span> <span data-ttu-id="81f99-134">Quando isso acontece, a TAPI sinaliza ao provedor de serviços para aguardar um pouco de tempo antes de enviar mais chamadas.</span><span class="sxs-lookup"><span data-stu-id="81f99-134">When this happens, TAPI signals to the service provider to wait a short time before sending any more calls.</span></span> <span data-ttu-id="81f99-135">Ele sinaliza isso escrevendo um valor de **NULL**, em vez de um [**HTAPICALL**](htapicall.md)válido, no local apontado pelo parâmetro *dwParam2* da **linha \_ NewCall**.</span><span class="sxs-lookup"><span data-stu-id="81f99-135">It signals this by writing a value of **NULL**, instead of a valid [**HTAPICALL**](htapicall.md), into the location pointed to by the *dwParam2* parameter of **LINE\_NEWCALL**.</span></span> <span data-ttu-id="81f99-136">Isso indica que a tentativa de processar o identificador de chamada recém oferecido não foi bem-sucedida, provavelmente devido a uma incapacidade temporária de alocar memória.</span><span class="sxs-lookup"><span data-stu-id="81f99-136">This indicates that the attempt to process the newly offered call handle was not successful, most likely due to a temporary inability to allocate memory.</span></span> <span data-ttu-id="81f99-137">O provedor de serviços pode responder descartando a chamada ou reenviando a mensagem **\_ NewCall de linha** após um atraso de agendamento (durante o qual o provedor de serviços deve produzir o processador para permitir que a TAPI processe outras ações pendentes).</span><span class="sxs-lookup"><span data-stu-id="81f99-137">The service provider can respond by dropping the call or by resending the **LINE\_NEWCALL** message after a scheduling delay (during which time the service provider should yield the processor to allow TAPI to process other pending actions).</span></span> <span data-ttu-id="81f99-138">Em qualquer caso, nenhuma mensagem adicional sobre a nova chamada pode ser passada para a TAPI até que a troca de identificador seja realizada com êxito.</span><span class="sxs-lookup"><span data-stu-id="81f99-138">In any case, no further messages regarding the new call can be passed to TAPI until the handle exchange succeeds.</span></span> <span data-ttu-id="81f99-139">Quando o local apontado por *dwParam2* adquire um valor não **nulo** , o provedor de serviços sabe que esse valor é um identificador [**HTAPICALL**](htapicall.md) válido para a chamada.</span><span class="sxs-lookup"><span data-stu-id="81f99-139">When the location pointed to by *dwParam2* acquires a non-**NULL** value, the service provider knows that this value is a valid [**HTAPICALL**](htapicall.md) handle to the call.</span></span>

<span data-ttu-id="81f99-140">Não há nenhuma mensagem diretamente correspondente no nível de TAPI.</span><span class="sxs-lookup"><span data-stu-id="81f99-140">There is no directly corresponding message at the TAPI level.</span></span> <span data-ttu-id="81f99-141">Essa mensagem é usada no nível de TSPI para introduzir de forma exclusiva e não ambígua uma nova chamada de entrada para a TAPI e recuperar o identificador opaco da TAPI para a chamada.</span><span class="sxs-lookup"><span data-stu-id="81f99-141">This message is used at the TSPI level to uniquely and unambiguously introduce a new incoming call to TAPI and retrieve the TAPI opaque identifier for the call.</span></span>

## <a name="requirements"></a><span data-ttu-id="81f99-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="81f99-142">Requirements</span></span>



| <span data-ttu-id="81f99-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="81f99-143">Requirement</span></span> | <span data-ttu-id="81f99-144">Valor</span><span class="sxs-lookup"><span data-stu-id="81f99-144">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="81f99-145">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="81f99-145">TAPI version</span></span><br/> | <span data-ttu-id="81f99-146">Requer TAPI 2,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="81f99-146">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="81f99-147">parâmetro</span><span class="sxs-lookup"><span data-stu-id="81f99-147">Header</span></span><br/>       | <dl> <span data-ttu-id="81f99-148"><dt>TSPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="81f99-148"><dt>Tspi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81f99-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="81f99-149">See also</span></span>

<dl> <dt>

<span data-ttu-id="81f99-150">[**chamada de LINHAstate \_**](/previous-versions/windows/desktop/legacy/ms725219(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="81f99-150">[**LINE\_CALLSTATE**](/previous-versions/windows/desktop/legacy/ms725219(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="81f99-151">**LINEEVENT**</span><span class="sxs-lookup"><span data-stu-id="81f99-151">**LINEEVENT**</span></span>](/windows/win32/api/tspi/nc-tspi-lineevent)
</dt> </dl>

 

