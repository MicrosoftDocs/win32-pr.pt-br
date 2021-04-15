---
description: 'O método IWiaDevMgr2:: RegisterEventCallbackCLSID registra um aplicativo para receber eventos, mesmo que o aplicativo não esteja em execução.'
ms.assetid: e0d421a7-ef49-4e27-9661-c358ac819712
title: 'Método IWiaDevMgr2:: RegisterEventCallbackCLSID (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaDevMgr2.RegisterEventCallbackCLSID
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 63e69d12d47f90ba40f5cc785d8b864c40158774
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501996"
---
# <a name="iwiadevmgr2registereventcallbackclsid-method"></a><span data-ttu-id="b7736-103">Método IWiaDevMgr2:: RegisterEventCallbackCLSID</span><span class="sxs-lookup"><span data-stu-id="b7736-103">IWiaDevMgr2::RegisterEventCallbackCLSID method</span></span>

<span data-ttu-id="b7736-104">O método **IWiaDevMgr2:: RegisterEventCallbackCLSID** registra um aplicativo para receber eventos, mesmo que o aplicativo não esteja em execução.</span><span class="sxs-lookup"><span data-stu-id="b7736-104">The **IWiaDevMgr2::RegisterEventCallbackCLSID** method registers an application to receive events even if the application is not running.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7736-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b7736-105">Syntax</span></span>


```C++
HRESULT RegisterEventCallbackCLSID(
  [in]               LONG lFlags,
  [in]               BSTR bstrDeviceID,
  [in]         const GUID *pEventGUID,
  [in, unique] const GUID *pClsID,
  [in]               BSTR bstrName,
  [in]               BSTR bstrDescription,
  [in]               BSTR bstrIcon
);
```



## <a name="parameters"></a><span data-ttu-id="b7736-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b7736-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7736-107">*lFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b7736-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7736-108">Tipo: **longo**</span><span class="sxs-lookup"><span data-stu-id="b7736-108">Type: **LONG**</span></span>

<span data-ttu-id="b7736-109">Especifica os sinalizadores de registro.</span><span class="sxs-lookup"><span data-stu-id="b7736-109">Specifies registration flags.</span></span> <span data-ttu-id="b7736-110">Pode ser definido com os seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="b7736-110">Can be set to the following values:</span></span>



| <span data-ttu-id="b7736-111">Sinalizador de registro</span><span class="sxs-lookup"><span data-stu-id="b7736-111">Registration Flag</span></span>                | <span data-ttu-id="b7736-112">Significado</span><span class="sxs-lookup"><span data-stu-id="b7736-112">Meaning</span></span>                                           |
|----------------------------------|---------------------------------------------------|
| <span data-ttu-id="b7736-113">\_retorno de \_ chamada de evento de registro WIA \_</span><span class="sxs-lookup"><span data-stu-id="b7736-113">WIA\_REGISTER\_EVENT\_CALLBACK</span></span>   | <span data-ttu-id="b7736-114">Registre-se no evento.</span><span class="sxs-lookup"><span data-stu-id="b7736-114">Register for the event.</span></span>                           |
| <span data-ttu-id="b7736-115">retorno de chamada do evento WIA \_ Cancelar registro \_ \_</span><span class="sxs-lookup"><span data-stu-id="b7736-115">WIA\_UNREGISTER\_EVENT\_CALLBACK</span></span> | <span data-ttu-id="b7736-116">Exclua o registro do evento.</span><span class="sxs-lookup"><span data-stu-id="b7736-116">Delete the registration for the event.</span></span>            |
| <span data-ttu-id="b7736-117">\_ \_ manipulador padrão de Set WIA \_</span><span class="sxs-lookup"><span data-stu-id="b7736-117">WIA\_SET\_DEFAULT\_HANDLER</span></span>       | <span data-ttu-id="b7736-118">Defina o aplicativo como o manipulador de eventos padrão.</span><span class="sxs-lookup"><span data-stu-id="b7736-118">Set the application as the default event handler.</span></span> |



 

</dd> <dt>

<span data-ttu-id="b7736-119">*bstrDeviceID* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b7736-119">*bstrDeviceID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7736-120">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="b7736-120">Type: **BSTR**</span></span>

<span data-ttu-id="b7736-121">Especifica um identificador de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b7736-121">Specifies a device identifier.</span></span> <span data-ttu-id="b7736-122">Passe **NULL** para registrar o evento em todos os dispositivos WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="b7736-122">Pass **NULL** to register for the event on all WIA 2.0 devices.</span></span>

</dd> <dt>

<span data-ttu-id="b7736-123">*pEventGUID* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b7736-123">*pEventGUID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7736-124">Tipo: \**const GUID \** _</span><span class="sxs-lookup"><span data-stu-id="b7736-124">Type: \**const GUID\** _</span></span>

<span data-ttu-id="b7736-125">Especifica o evento para o qual o aplicativo está se registrando.</span><span class="sxs-lookup"><span data-stu-id="b7736-125">Specifies the event that the application is registering for.</span></span> <span data-ttu-id="b7736-126">Para obter uma lista de eventos padrão, consulte [identificadores de evento WIA](-wia-wia-event-identifiers.md).</span><span class="sxs-lookup"><span data-stu-id="b7736-126">For a list of standard events, see [WIA Event Identifiers](-wia-wia-event-identifiers.md).</span></span>

</dd> <dt>

<span data-ttu-id="b7736-127">_pClsID \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b7736-127">_pClsID\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7736-128">Tipo: \**const GUID \** _</span><span class="sxs-lookup"><span data-stu-id="b7736-128">Type: \**const GUID\** _</span></span>

<span data-ttu-id="b7736-129">Ponteiro para a ID de classe do aplicativo (_ \* CLSID \* \*).</span><span class="sxs-lookup"><span data-stu-id="b7736-129">Pointer to the application class ID (_\*CLSID\*\*).</span></span> <span data-ttu-id="b7736-130">O sistema de tempo de execução WIA 2,0 usa o **CLSID** do aplicativo para iniciar o aplicativo quando ocorre um evento no qual ele está registrado.</span><span class="sxs-lookup"><span data-stu-id="b7736-130">The WIA 2.0 run-time system uses the application **CLSID** to start the application when an event occurs that it is registered for.</span></span>

</dd> <dt>

<span data-ttu-id="b7736-131">*bstrname* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b7736-131">*bstrName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7736-132">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="b7736-132">Type: **BSTR**</span></span>

<span data-ttu-id="b7736-133">Especifica o nome do aplicativo que se registra para o evento.</span><span class="sxs-lookup"><span data-stu-id="b7736-133">Specifies the name of the application that registers for the event.</span></span>

</dd> <dt>

<span data-ttu-id="b7736-134">*bstrDescription* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b7736-134">*bstrDescription* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7736-135">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="b7736-135">Type: **BSTR**</span></span>

<span data-ttu-id="b7736-136">Especifica uma descrição de texto do aplicativo que se registra para o evento.</span><span class="sxs-lookup"><span data-stu-id="b7736-136">Specifies a text description of the application that registers for the event.</span></span>

</dd> <dt>

<span data-ttu-id="b7736-137">*bstrIcon* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b7736-137">*bstrIcon* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7736-138">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="b7736-138">Type: **BSTR**</span></span>

<span data-ttu-id="b7736-139">Especifica o nome de um arquivo de imagem a ser usado para o ícone do aplicativo que se registra para o evento.</span><span class="sxs-lookup"><span data-stu-id="b7736-139">Specifies the name of an image file to use for the icon for the application that registers for the event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7736-140">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b7736-140">Return value</span></span>

<span data-ttu-id="b7736-141">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="b7736-141">Type: **HRESULT**</span></span>

<span data-ttu-id="b7736-142">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="b7736-142">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b7736-143">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b7736-143">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b7736-144">Comentários</span><span class="sxs-lookup"><span data-stu-id="b7736-144">Remarks</span></span>

<span data-ttu-id="b7736-145">Os aplicativos WIA 2,0 usam esse método para se registrar para receber eventos de dispositivo de hardware.</span><span class="sxs-lookup"><span data-stu-id="b7736-145">WIA 2.0 applications use this method to register to receive hardware device events.</span></span> <span data-ttu-id="b7736-146">Depois que **IWiaDevMgr2:: RegisterEventCallbackCLSID** for chamado, o aplicativo será registrado para receber eventos de dispositivo WIA 2,0, mesmo se ele não estiver em execução.</span><span class="sxs-lookup"><span data-stu-id="b7736-146">After **IWiaDevMgr2::RegisterEventCallbackCLSID** is called, the application is registered to receive WIA 2.0 device events even if it is not running.</span></span>

<span data-ttu-id="b7736-147">Quando o evento ocorre, o sistema WIA 2,0 determina qual aplicativo está registrado para receber o evento.</span><span class="sxs-lookup"><span data-stu-id="b7736-147">When the event occurs, the WIA 2.0 system determines which application is registered to receive the event.</span></span> <span data-ttu-id="b7736-148">Ele usa a função [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) e o CLSID especificado no parâmetro *pCLSID* para criar uma instância do aplicativo e, em seguida, chama o método [**ImageEventCallback**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaeventcallback-imageeventcallback) para transmitir as informações do evento para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b7736-148">It uses the [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) function and the CLSID specified in the *pClsID* parameter to create an instance of the application, and then calls the [**ImageEventCallback**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaeventcallback-imageeventcallback) method to transmit the event information to the application.</span></span>

<span data-ttu-id="b7736-149">Um aplicativo pode invocar o método [**EnumRegisterEventInfo**](-wia-iwiaitem2-enumregistereventinfo.md) para enumerar informações de registro de evento.</span><span class="sxs-lookup"><span data-stu-id="b7736-149">An application can invoke the [**EnumRegisterEventInfo**](-wia-iwiaitem2-enumregistereventinfo.md) method to enumerate event registration information.</span></span>

<span data-ttu-id="b7736-150">Se o aplicativo não for um componente COM (Component Object Model registrado) e não for compatível com a arquitetura WIA 2,0, use o método [**IWiaDevMgr2:: RegisterEventCallbackProgram**](-wia-iwiadevmgr2-registereventcallbackprogram.md) para registrar um aplicativo para eventos de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b7736-150">If the application is not a registered Component Object Model (COM) component and is not compatible with the WIA 2.0 architecture, use the [**IWiaDevMgr2::RegisterEventCallbackProgram**](-wia-iwiadevmgr2-registereventcallbackprogram.md) method to register an application for device events.</span></span>

> [!Note]  
> <span data-ttu-id="b7736-151">Em um aplicativo multi-threaded, não há nenhuma garantia de que o retorno de chamada de notificação de evento seja retornado no mesmo thread que registrou o retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="b7736-151">In a multi-threaded application, there is no guarantee that the event notification callback is returned on the same thread that registered the callback.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b7736-152">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b7736-152">Requirements</span></span>



| <span data-ttu-id="b7736-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="b7736-153">Requirement</span></span> | <span data-ttu-id="b7736-154">Valor</span><span class="sxs-lookup"><span data-stu-id="b7736-154">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="b7736-155">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b7736-155">Minimum supported client</span></span><br/> | <span data-ttu-id="b7736-156">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b7736-156">Windows Vista \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="b7736-157">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b7736-157">Minimum supported server</span></span><br/> | <span data-ttu-id="b7736-158">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b7736-158">Windows Server 2008 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="b7736-159">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b7736-159">Header</span></span><br/>                   | <dl> <span data-ttu-id="b7736-160"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="b7736-160"><dt>Wia.h</dt></span></span> </dl> |



 

 
