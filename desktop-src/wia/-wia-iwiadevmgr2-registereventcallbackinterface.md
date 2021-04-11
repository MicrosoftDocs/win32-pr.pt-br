---
description: Registra um aplicativo em execução para notificação de eventos de aquisição de imagem do Windows (WIA) 2,0.
ms.assetid: 978dcd41-d63b-421d-b7e1-8e9368b36180
title: 'Método IWiaDevMgr2:: RegisterEventCallbackInterface (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaDevMgr2.RegisterEventCallbackInterface
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 7cd3a7e00cff56bc5d91bfc843ab79fe71aa1123
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169537"
---
# <a name="iwiadevmgr2registereventcallbackinterface-method"></a><span data-ttu-id="f5863-103">Método IWiaDevMgr2:: RegisterEventCallbackInterface</span><span class="sxs-lookup"><span data-stu-id="f5863-103">IWiaDevMgr2::RegisterEventCallbackInterface method</span></span>

<span data-ttu-id="f5863-104">Registra um aplicativo em execução para notificação de eventos de aquisição de imagem do Windows (WIA) 2,0.</span><span class="sxs-lookup"><span data-stu-id="f5863-104">Registers a running application for Windows Image Acquisition (WIA) 2.0 event notification.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5863-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f5863-105">Syntax</span></span>


```C++
HRESULT RegisterEventCallbackInterface(
  [in]        LONG              lFlags,
  [in]        BSTR              bstrDeviceID,
  [in]  const GUID              *pEventGUID,
  [in]        IWiaEventCallback *pIWiaEventCallback,
  [out]       IUnknown          **pEventObject
);
```



## <a name="parameters"></a><span data-ttu-id="f5863-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f5863-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5863-107">*lFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f5863-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5863-108">Tipo: **longo**</span><span class="sxs-lookup"><span data-stu-id="f5863-108">Type: **LONG**</span></span>

<span data-ttu-id="f5863-109">Atualmente não utilizado.</span><span class="sxs-lookup"><span data-stu-id="f5863-109">Currently unused.</span></span> <span data-ttu-id="f5863-110">Deve ser definido como zero.</span><span class="sxs-lookup"><span data-stu-id="f5863-110">Should be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="f5863-111">*bstrDeviceID* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f5863-111">*bstrDeviceID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5863-112">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="f5863-112">Type: **BSTR**</span></span>

<span data-ttu-id="f5863-113">Especifica o identificador exclusivo de um dispositivo WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="f5863-113">Specifies the unique identifier of a WIA 2.0 device.</span></span> <span data-ttu-id="f5863-114">Defina esse parâmetro como **NULL** para registrar o evento em todos os dispositivos WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="f5863-114">Set this parameter to **NULL** to register for the event on all WIA 2.0 devices.</span></span>

</dd> <dt>

<span data-ttu-id="f5863-115">*pEventGUID* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f5863-115">*pEventGUID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5863-116">Tipo: \**const GUID \** _</span><span class="sxs-lookup"><span data-stu-id="f5863-116">Type: \**const GUID\** _</span></span>

<span data-ttu-id="f5863-117">Especifica um ponteiro para o identificador de evento para o qual o aplicativo está se registrando.</span><span class="sxs-lookup"><span data-stu-id="f5863-117">Specifies a pointer to the event identifier that the application is registering for.</span></span> <span data-ttu-id="f5863-118">Consulte [identificadores de evento WIA](-wia-wia-event-identifiers.md) para identificadores de evento padrão.</span><span class="sxs-lookup"><span data-stu-id="f5863-118">See [WIA Event Identifiers](-wia-wia-event-identifiers.md) for standard event identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="f5863-119">_pIWiaEventCallback \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f5863-119">_pIWiaEventCallback\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5863-120">Tipo: \**[**IWiaEventCallback**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaeventcallback) \** _</span><span class="sxs-lookup"><span data-stu-id="f5863-120">Type: \**[**IWiaEventCallback**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaeventcallback)\** _</span></span>

<span data-ttu-id="f5863-121">Especifica um ponteiro para a interface [_ *IWiaEventCallback* \*](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaeventcallback) que o WIA 2,0 usa para enviar a notificação de eventos.</span><span class="sxs-lookup"><span data-stu-id="f5863-121">Specifies a pointer to the [_ *IWiaEventCallback*\*](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaeventcallback) interface that the WIA 2.0 uses to send event notification.</span></span>

</dd> <dt>

<span data-ttu-id="f5863-122">*pEventObject* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="f5863-122">*pEventObject* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f5863-123">Tipo: **[IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown)\*\***</span><span class="sxs-lookup"><span data-stu-id="f5863-123">Type: **[IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown)\*\***</span></span>

<span data-ttu-id="f5863-124">Recebe o endereço de um ponteiro para a interface [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="f5863-124">Receives the address of a pointer to the [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5863-125">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f5863-125">Return value</span></span>

<span data-ttu-id="f5863-126">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="f5863-126">Type: **HRESULT**</span></span>

<span data-ttu-id="f5863-127">Retorna os códigos de erro COM padrão ou o seguinte.</span><span class="sxs-lookup"><span data-stu-id="f5863-127">Returns the standard COM error codes or the following.</span></span>



| <span data-ttu-id="f5863-128">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="f5863-128">Return code</span></span>                                                                               | <span data-ttu-id="f5863-129">Descrição</span><span class="sxs-lookup"><span data-stu-id="f5863-129">Description</span></span>                                                            |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f5863-130"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="f5863-130"><dt>**E\_NOTIMPL**</dt></span></span> </dl> | <span data-ttu-id="f5863-131">A interface [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) não pode ser retornada.</span><span class="sxs-lookup"><span data-stu-id="f5863-131">The [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface cannot be returned.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="f5863-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="f5863-132">Remarks</span></span>

> [!WARNING]
> <span data-ttu-id="f5863-133">O uso dos métodos [**IWiaDevMgr:: RegisterEventCallbackInterface**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackinterface), **IWiaDevMgr2:: RegisterEventCallbackInterface** e [**DeviceManager. RegisterEvent**](/previous-versions/windows/desktop/wiaaut/-wiaaut-idevicemanager-registerevent) do mesmo processo após a reinicialização do serviço de imagem ainda pode causar uma violação de acesso, se as funções tiverem sido usadas antes de o serviço ser interrompido.</span><span class="sxs-lookup"><span data-stu-id="f5863-133">Using the [**IWiaDevMgr::RegisterEventCallbackInterface**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackinterface), **IWiaDevMgr2::RegisterEventCallbackInterface**, and [**DeviceManager.RegisterEvent**](/previous-versions/windows/desktop/wiaaut/-wiaaut-idevicemanager-registerevent) methods from the same process after the Still Image Service is restarted may cause an access violation, if the functions were used before the service was stopped.</span></span>

 

<span data-ttu-id="f5863-134">Quando os aplicativos WIA 2,0 começam a ser executados, eles usam esse método para se registrar para receber eventos de dispositivo de hardware.</span><span class="sxs-lookup"><span data-stu-id="f5863-134">When WIA 2.0 applications begin executing, they use this method to register to receive hardware device events.</span></span> <span data-ttu-id="f5863-135">Isso impede que o aplicativo seja reiniciado quando outro evento para o qual ele está registrado ocorre.</span><span class="sxs-lookup"><span data-stu-id="f5863-135">This prevents the application from being restarted when another event for which it is registered occurs.</span></span> <span data-ttu-id="f5863-136">Quando um aplicativo chama **IWiaDevMgr2:: RegisterEventCallbackInterface** para se registrar para receber eventos WIA 2,0 de um dispositivo, os eventos registrados são roteados para o programa pela WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="f5863-136">Once an application calls **IWiaDevMgr2::RegisterEventCallbackInterface** to register itself to receive WIA 2.0 events from a device, the registered events are routed to the program by WIA 2.0.</span></span>

<span data-ttu-id="f5863-137">Os aplicativos devem chamar o método [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) nos ponteiros de interface recebidos por meio do parâmetro *pEventObject* .</span><span class="sxs-lookup"><span data-stu-id="f5863-137">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on the interface pointers they receive through the *pEventObject* parameter.</span></span>

> [!Note]  
> <span data-ttu-id="f5863-138">Em um aplicativo multithread, o retorno de chamada de notificação de evento pode vir em um thread diferente daquele que registrou o retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="f5863-138">In a multithreaded application, the event notification callback may come in on a different thread from the one that registered the callback.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f5863-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f5863-139">Requirements</span></span>



| <span data-ttu-id="f5863-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5863-140">Requirement</span></span> | <span data-ttu-id="f5863-141">Valor</span><span class="sxs-lookup"><span data-stu-id="f5863-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f5863-142">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f5863-142">Minimum supported client</span></span><br/> | <span data-ttu-id="f5863-143">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f5863-143">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="f5863-144">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f5863-144">Minimum supported server</span></span><br/> | <span data-ttu-id="f5863-145">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f5863-145">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="f5863-146">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f5863-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="f5863-147"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="f5863-147"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="f5863-148">INSERI</span><span class="sxs-lookup"><span data-stu-id="f5863-148">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f5863-149"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f5863-149"><dt>Wia.idl</dt></span></span> </dl> |



 

 
