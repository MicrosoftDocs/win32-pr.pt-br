---
description: 'O método IWiaDevMgr2:: RegisterEventCallbackProgram registra um aplicativo para receber eventos de dispositivo. Ele é fornecido principalmente para compatibilidade com versões anteriores com aplicativos que não foram escritos para o WIA (Windows Image Acquisition) 2,0.'
ms.assetid: 6b427f19-719b-44ce-8e2c-3c44672345c8
title: 'Método IWiaDevMgr2:: RegisterEventCallbackProgram (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaDevMgr2.RegisterEventCallbackProgram
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 9b18b5833b7616493c24f0128caa7c910b685e37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105764285"
---
# <a name="iwiadevmgr2registereventcallbackprogram-method"></a><span data-ttu-id="f684c-104">Método IWiaDevMgr2:: RegisterEventCallbackProgram</span><span class="sxs-lookup"><span data-stu-id="f684c-104">IWiaDevMgr2::RegisterEventCallbackProgram method</span></span>

<span data-ttu-id="f684c-105">O método **IWiaDevMgr2:: RegisterEventCallbackProgram** registra um aplicativo para receber eventos de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f684c-105">The **IWiaDevMgr2::RegisterEventCallbackProgram** method registers an application to receive device events.</span></span> <span data-ttu-id="f684c-106">Ele é fornecido principalmente para compatibilidade com versões anteriores com aplicativos que não foram escritos para o WIA (Windows Image Acquisition) 2,0.</span><span class="sxs-lookup"><span data-stu-id="f684c-106">It is primarily provided for backward compatibility with applications that were not written for Windows Image Acquisition (WIA) 2.0.</span></span>

## <a name="syntax"></a><span data-ttu-id="f684c-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f684c-107">Syntax</span></span>


```C++
HRESULT RegisterEventCallbackProgram(
  [in]       LONG lFlags,
  [in]       BSTR bstrDeviceID,
  [in] const GUID *pEventGUID,
  [in]       BSTR bstrFullAppName,
  [in]       BSTR bstrCommandlineArg,
  [in]       BSTR bstrName,
  [in]       BSTR bstrDescription,
  [in]       BSTR bstrIcon
);
```



## <a name="parameters"></a><span data-ttu-id="f684c-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f684c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f684c-109">*lFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f684c-109">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f684c-110">Tipo: **longo**</span><span class="sxs-lookup"><span data-stu-id="f684c-110">Type: **LONG**</span></span>

<span data-ttu-id="f684c-111">Os sinalizadores de registro.</span><span class="sxs-lookup"><span data-stu-id="f684c-111">The registration flags.</span></span> <span data-ttu-id="f684c-112">Pode ser definido com os valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="f684c-112">Can be set to the following values.</span></span>



| <span data-ttu-id="f684c-113">Valor</span><span class="sxs-lookup"><span data-stu-id="f684c-113">Value</span></span>                                                                                                                                                                                                           | <span data-ttu-id="f684c-114">Significado</span><span class="sxs-lookup"><span data-stu-id="f684c-114">Meaning</span></span>                                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <span id="WIA_REGISTER_EVENT_CALLBACK"></span><span id="wia_register_event_callback"></span><dl> <span data-ttu-id="f684c-115"><dt>**\_retorno de \_ chamada de evento de registro WIA \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f684c-115"><dt>**WIA\_REGISTER\_EVENT\_CALLBACK**</dt></span></span> </dl>       | <span data-ttu-id="f684c-116">Registre-se no evento.</span><span class="sxs-lookup"><span data-stu-id="f684c-116">Register for the event.</span></span><br/>                           |
| <span id="WIA_UNREGISTER_EVENT_CALLBACK"></span><span id="wia_unregister_event_callback"></span><dl> <span data-ttu-id="f684c-117"><dt>**retorno de chamada do evento WIA \_ Cancelar registro \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f684c-117"><dt>**WIA\_UNREGISTER\_EVENT\_CALLBACK**</dt></span></span> </dl> | <span data-ttu-id="f684c-118">Exclua o registro do evento.</span><span class="sxs-lookup"><span data-stu-id="f684c-118">Delete the registration for the event.</span></span><br/>            |
| <span id="WIA_SET_DEFAULT_HANDLER"></span><span id="wia_set_default_handler"></span><dl> <span data-ttu-id="f684c-119"><dt>**\_ \_ manipulador padrão de Set WIA \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f684c-119"><dt>**WIA\_SET\_DEFAULT\_HANDLER**</dt></span></span> </dl>                   | <span data-ttu-id="f684c-120">Defina o aplicativo como o manipulador de eventos padrão.</span><span class="sxs-lookup"><span data-stu-id="f684c-120">Set the application as the default event handler.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="f684c-121">*bstrDeviceID* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f684c-121">*bstrDeviceID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f684c-122">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="f684c-122">Type: **BSTR**</span></span>

<span data-ttu-id="f684c-123">Um identificador de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f684c-123">A device identifier.</span></span> <span data-ttu-id="f684c-124">Passe **NULL** para registrar o evento em todos os dispositivos WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="f684c-124">Pass **NULL** to register for the event on all WIA 2.0 devices.</span></span>

</dd> <dt>

<span data-ttu-id="f684c-125">*pEventGUID* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f684c-125">*pEventGUID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f684c-126">Tipo: \**const GUID \** _</span><span class="sxs-lookup"><span data-stu-id="f684c-126">Type: \**const GUID\** _</span></span>

<span data-ttu-id="f684c-127">O evento para o qual o aplicativo está se registrando.</span><span class="sxs-lookup"><span data-stu-id="f684c-127">The event that the application is registering for.</span></span> <span data-ttu-id="f684c-128">Para obter uma lista de GUIDs de eventos válidos, consulte [identificadores de evento WIA](-wia-wia-event-identifiers.md).</span><span class="sxs-lookup"><span data-stu-id="f684c-128">For a list of valid event GUIDs, see [WIA Event Identifiers](-wia-wia-event-identifiers.md).</span></span>

</dd> <dt>

<span data-ttu-id="f684c-129">_bstrFullAppName \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f684c-129">_bstrFullAppName\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f684c-130">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="f684c-130">Type: **BSTR**</span></span>

<span data-ttu-id="f684c-131">O nome do caminho completo do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f684c-131">The full path name of the application.</span></span>

</dd> <dt>

<span data-ttu-id="f684c-132">*bstrCommandlineArg* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f684c-132">*bstrCommandlineArg* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f684c-133">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="f684c-133">Type: **BSTR**</span></span>

<span data-ttu-id="f684c-134">Os argumentos de linha de comando apropriados para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f684c-134">The appropriate command-line arguments for the application.</span></span>

</dd> <dt>

<span data-ttu-id="f684c-135">*bstrname* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f684c-135">*bstrName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f684c-136">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="f684c-136">Type: **BSTR**</span></span>

<span data-ttu-id="f684c-137">O nome do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f684c-137">The name of the application.</span></span> <span data-ttu-id="f684c-138">O nome é exibido para o usuário quando vários aplicativos são registrados para o mesmo evento.</span><span class="sxs-lookup"><span data-stu-id="f684c-138">The name is displayed to the user when multiple applications register for the same event.</span></span>

</dd> <dt>

<span data-ttu-id="f684c-139">*bstrDescription* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f684c-139">*bstrDescription* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f684c-140">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="f684c-140">Type: **BSTR**</span></span>

<span data-ttu-id="f684c-141">A descrição do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f684c-141">The description of the application.</span></span> <span data-ttu-id="f684c-142">A descrição é exibida para o usuário quando vários aplicativos são registrados para o mesmo evento.</span><span class="sxs-lookup"><span data-stu-id="f684c-142">The description is displayed to the user when multiple applications register for the same event.</span></span>

</dd> <dt>

<span data-ttu-id="f684c-143">*bstrIcon* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f684c-143">*bstrIcon* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f684c-144">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="f684c-144">Type: **BSTR**</span></span>

<span data-ttu-id="f684c-145">O ícone que representa o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f684c-145">The icon that represents the application.</span></span> <span data-ttu-id="f684c-146">O ícone é exibido para o usuário quando vários aplicativos são registrados para o mesmo evento.</span><span class="sxs-lookup"><span data-stu-id="f684c-146">The icon is displayed to the user when multiple applications register for the same event.</span></span> <span data-ttu-id="f684c-147">A cadeia de caracteres contém o nome do aplicativo e o índice de base zero do ícone separado por uma vírgula, por exemplo, "MyApp, 0".</span><span class="sxs-lookup"><span data-stu-id="f684c-147">The string contains the name of the application and the zero-based index of the icon separated by a comma, for example, "MyApp, 0".</span></span> <span data-ttu-id="f684c-148">Pode haver mais de um ícone que representa um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f684c-148">There might be more than one icon that represents an application.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f684c-149">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f684c-149">Return value</span></span>

<span data-ttu-id="f684c-150">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="f684c-150">Type: **HRESULT**</span></span>

<span data-ttu-id="f684c-151">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="f684c-151">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f684c-152">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f684c-152">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f684c-153">Comentários</span><span class="sxs-lookup"><span data-stu-id="f684c-153">Remarks</span></span>

<span data-ttu-id="f684c-154">Use **IWiaDevMgr2:: RegisterEventCallbackProgram** para se registrar em eventos de dispositivo de hardware.</span><span class="sxs-lookup"><span data-stu-id="f684c-154">Use **IWiaDevMgr2::RegisterEventCallbackProgram** to register for hardware device events.</span></span> <span data-ttu-id="f684c-155">Quando um evento ocorre quando um aplicativo é registrado para o, o aplicativo é iniciado e as informações do evento são transmitidas para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f684c-155">When an event occurs that an application is registered for, the application is launched, and the event information is transmitted to the application.</span></span>

<span data-ttu-id="f684c-156">Use o método [**EnumRegisterEventInfo**](-wia-iwiaitem2-enumregistereventinfo.md) para recuperar um ponteiro para um objeto enumerador para propriedades de registro de evento.</span><span class="sxs-lookup"><span data-stu-id="f684c-156">Use the [**EnumRegisterEventInfo**](-wia-iwiaitem2-enumregistereventinfo.md) method to retrieve a pointer to an enumerator object for event registration properties.</span></span>

<span data-ttu-id="f684c-157">Use apenas o método **IWiaDevMgr2:: RegisterEventCallbackProgram** para compatibilidade com versões anteriores com aplicativos não escritos para a arquitetura WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="f684c-157">Only use the **IWiaDevMgr2::RegisterEventCallbackProgram** method for backward compatibility with applications not written for the WIA 2.0 architecture.</span></span> <span data-ttu-id="f684c-158">Use as interfaces de Component Object Model (COM) fornecidas pela arquitetura WIA 2,0 para novos aplicativos.</span><span class="sxs-lookup"><span data-stu-id="f684c-158">Use the Component Object Model (COM) interfaces provided by the WIA 2.0 architecture for new applications.</span></span> <span data-ttu-id="f684c-159">Especificamente, chame [**IWiaDevMgr2:: RegisterEventCallbackInterface**](-wia-iwiadevmgr2-registereventcallbackinterface.md) ou [**IWiaDevMgr2:: RegisterEventCallbackCLSID**](-wia-iwiadevmgr2-registereventcallbackclsid.md) para registrar um novo aplicativo para eventos de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f684c-159">Specifically, call [**IWiaDevMgr2::RegisterEventCallbackInterface**](-wia-iwiadevmgr2-registereventcallbackinterface.md) or [**IWiaDevMgr2::RegisterEventCallbackCLSID**](-wia-iwiadevmgr2-registereventcallbackclsid.md) to register a new application for device events.</span></span>

<span data-ttu-id="f684c-160">Normalmente, esse método é chamado por um programa de instalação ou um script.</span><span class="sxs-lookup"><span data-stu-id="f684c-160">Typically, this method is called by an install program or a script.</span></span> <span data-ttu-id="f684c-161">O programa ou script de instalação registra o aplicativo para receber eventos de dispositivo WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="f684c-161">The install program or script registers the application to receive WIA 2.0 device events.</span></span> <span data-ttu-id="f684c-162">Quando o evento ocorre, o aplicativo é iniciado pelo sistema de tempo de execução WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="f684c-162">When the event occurs, the application is started by the WIA 2.0 run-time system.</span></span>

## <a name="requirements"></a><span data-ttu-id="f684c-163">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f684c-163">Requirements</span></span>



| <span data-ttu-id="f684c-164">Requisito</span><span class="sxs-lookup"><span data-stu-id="f684c-164">Requirement</span></span> | <span data-ttu-id="f684c-165">Valor</span><span class="sxs-lookup"><span data-stu-id="f684c-165">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="f684c-166">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f684c-166">Minimum supported client</span></span><br/> | <span data-ttu-id="f684c-167">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f684c-167">Windows Vista \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="f684c-168">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f684c-168">Minimum supported server</span></span><br/> | <span data-ttu-id="f684c-169">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f684c-169">Windows Server 2008 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="f684c-170">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f684c-170">Header</span></span><br/>                   | <dl> <span data-ttu-id="f684c-171"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="f684c-171"><dt>Wia.h</dt></span></span> </dl> |



 

 




