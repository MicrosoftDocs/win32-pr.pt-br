---
description: A mensagem de APPNEWCALL de linha TAPI \_ é enviada para informar um aplicativo quando um novo identificador de chamada foi criado espontaneamente em seu nome.
ms.assetid: 0c263025-e719-453e-91c4-a9f2d9321db3
title: Mensagem de LINE_APPNEWCALL (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33d24ca816fb69384e90e4215edbc90b9410b887
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810132"
---
# <a name="line_appnewcall-message"></a><span data-ttu-id="74b8b-103">Mensagem de APPNEWCALL de linha \_</span><span class="sxs-lookup"><span data-stu-id="74b8b-103">LINE\_APPNEWCALL message</span></span>

<span data-ttu-id="74b8b-104">A mensagem **de \_ APPNEWCALL de linha** TAPI é enviada para informar um aplicativo quando um novo identificador de chamada foi criado espontaneamente em seu nome (diferente de por meio de uma chamada à API do aplicativo; nesse caso, o identificador teria sido retornado por meio de um parâmetro de ponteiro passado para a função).</span><span class="sxs-lookup"><span data-stu-id="74b8b-104">The TAPI **LINE\_APPNEWCALL** message is sent to inform an application when a new call handle has been spontaneously created on its behalf (other than through an API call from the application, in which case the handle would have been returned through a pointer parameter passed into the function).</span></span>


```C++
        
```



## <a name="parameters"></a><span data-ttu-id="74b8b-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="74b8b-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74b8b-106">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="74b8b-106">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="74b8b-107">O identificador do aplicativo para o dispositivo de linha no qual a chamada foi criada.</span><span class="sxs-lookup"><span data-stu-id="74b8b-107">The application's handle to the line device on which the call has been created.</span></span>

</dd> <dt>

<span data-ttu-id="74b8b-108">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="74b8b-108">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="74b8b-109">A instância de retorno de chamada fornecida ao abrir a linha do telefonema.</span><span class="sxs-lookup"><span data-stu-id="74b8b-109">The callback instance supplied when opening the call's line.</span></span>

</dd> <dt>

<span data-ttu-id="74b8b-110">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="74b8b-110">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="74b8b-111">Identificador do endereço na linha na qual a chamada é exibida.</span><span class="sxs-lookup"><span data-stu-id="74b8b-111">Identifier of the address on the line on which the call appears.</span></span> <span data-ttu-id="74b8b-112">Um identificador de endereço é permanentemente associado a um endereço; o identificador permanece constante nas atualizações do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="74b8b-112">An address identifier is permanently associated with an address; the identifier remains constant across operating system upgrades.</span></span>

</dd> <dt>

<span data-ttu-id="74b8b-113">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="74b8b-113">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="74b8b-114">O identificador do aplicativo para a nova chamada.</span><span class="sxs-lookup"><span data-stu-id="74b8b-114">The application's handle to the new call.</span></span>

</dd> <dt>

<span data-ttu-id="74b8b-115">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="74b8b-115">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="74b8b-116">O privilégio de aplicativos para a nova chamada (LINECALLPRIVILEGE \_ Owner ou LINECALLPRIVILEGE \_ Monitor).</span><span class="sxs-lookup"><span data-stu-id="74b8b-116">The applications privilege to the new call (LINECALLPRIVILEGE\_OWNER or LINECALLPRIVILEGE\_MONITOR).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74b8b-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="74b8b-117">Return value</span></span>

<span data-ttu-id="74b8b-118">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="74b8b-118">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="74b8b-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="74b8b-119">Remarks</span></span>

<span data-ttu-id="74b8b-120">Os aplicativos que dão suporte à TAPI versão 2,0 ou posterior são enviados uma mensagem de **linha \_ APPNEWCALL** sempre que o aplicativo recebe espontaneamente um identificador para uma nova chamada.</span><span class="sxs-lookup"><span data-stu-id="74b8b-120">Applications supporting TAPI version 2.0 or later are sent a **LINE\_APPNEWCALL** message whenever the application is spontaneously given a handle to a new call.</span></span> <span data-ttu-id="74b8b-121">Como a mensagem inclui os parâmetros *hLine* e *dwAddressID* nos quais a chamada existe, o aplicativo pode rapidamente criar um novo objeto de chamada no contexto correto.</span><span class="sxs-lookup"><span data-stu-id="74b8b-121">Because the message includes the *hLine* and *dwAddressID* parameters on which the call exists, the application can readily create a new call object in the correct context.</span></span> <span data-ttu-id="74b8b-122">A **mensagem \_ APPNEWCALL de linha** é sempre imediatamente seguida por uma mensagem [**\_ callstate de linha**](line-callstate.md) que indica o estado inicial da chamada.</span><span class="sxs-lookup"><span data-stu-id="74b8b-122">The **LINE\_APPNEWCALL** message is always immediately followed by a [**LINE\_CALLSTATE**](line-callstate.md) message indicating the initial state of the call.</span></span>

<span data-ttu-id="74b8b-123">Os aplicativos mais antigos (que negociaram uma versão de API anterior a 2,0) são enviados apenas a uma mensagem [**\_ callstate de linha**](line-callstate.md) , conforme documentado em versões anteriores da API.</span><span class="sxs-lookup"><span data-stu-id="74b8b-123">Older applications (that negotiated an API version earlier than 2.0) are sent only a [**LINE\_CALLSTATE**](line-callstate.md) message, as documented in previous versions of the API.</span></span> <span data-ttu-id="74b8b-124">Tais aplicativos criaria um novo objeto de chamada ao receber uma mensagem [**\_ callstate de linha**](line-callstate.md) que tem *dwParam3* definido como um valor diferente de zero e contendo um identificador de chamada não atualmente conhecido pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="74b8b-124">Such applications would create a new call object upon receiving a [**LINE\_CALLSTATE**](line-callstate.md) message that has *dwParam3* set to a nonzero value and containing a call handle not presently known by the application.</span></span> <span data-ttu-id="74b8b-125">As desvantagens são que (a) o aplicativo deve chamar [**lineGetCallInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetcallinfo) para determinar os parâmetros *hLine* e *dwAddressID* associados à chamada; (b) o aplicativo deve verificar todos os identificadores de chamada conhecidos para determinar se a chamada é uma nova chamada; e (c) é possível, em determinadas condições, para o aplicativo acreditar que está recebendo um novo identificador de chamada quando, na realidade, ele apenas desalocou seu identificador para a chamada (por exemplo, o aplicativo acabou de desalocar um identificador de chamada, mas uma mensagem [**\_ callstate de linha**](line-callstate.md) que fornece a propriedade do aplicativo da chamada devido a um [**lineHandoff**](/windows/desktop/api/Tapi/nf-tapi-linehandoff) de outro aplicativo já estava na fila de mensagens TAPI do aplicativo).</span><span class="sxs-lookup"><span data-stu-id="74b8b-125">The disadvantages are that (a) the application must call [**lineGetCallInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetcallinfo) to determine the *hLine* and *dwAddressID* parameters associated with the call; (b) the application must scan all known call handles to determine that the call is a new call; and (c) it is possible, under certain conditions, for the application to think it is receiving a new call handle when in reality it has just deallocated its handle to the call (for example, the application has just deallocated a call handle, but a [**LINE\_CALLSTATE**](line-callstate.md) message giving the application ownership of the call due to a [**lineHandoff**](/windows/desktop/api/Tapi/nf-tapi-linehandoff) from another application was already in the application's TAPI message queue).</span></span>

## <a name="requirements"></a><span data-ttu-id="74b8b-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="74b8b-126">Requirements</span></span>



| <span data-ttu-id="74b8b-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="74b8b-127">Requirement</span></span> | <span data-ttu-id="74b8b-128">Valor</span><span class="sxs-lookup"><span data-stu-id="74b8b-128">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="74b8b-129">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="74b8b-129">TAPI version</span></span><br/> | <span data-ttu-id="74b8b-130">Requer TAPI 2,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="74b8b-130">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="74b8b-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="74b8b-131">Header</span></span><br/>       | <dl> <span data-ttu-id="74b8b-132"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="74b8b-132"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="74b8b-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="74b8b-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74b8b-134">**chamada de LINHAstate \_**</span><span class="sxs-lookup"><span data-stu-id="74b8b-134">**LINE\_CALLSTATE**</span></span>](line-callstate.md)
</dt> <dt>

[<span data-ttu-id="74b8b-135">**lineGetCallInfo**</span><span class="sxs-lookup"><span data-stu-id="74b8b-135">**lineGetCallInfo**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetcallinfo)
</dt> <dt>

[<span data-ttu-id="74b8b-136">**lineHandoff**</span><span class="sxs-lookup"><span data-stu-id="74b8b-136">**lineHandoff**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linehandoff)
</dt> </dl>

 

 




