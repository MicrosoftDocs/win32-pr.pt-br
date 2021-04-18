---
title: Implementando o comportamento do dispositivo
description: O comportamento de um dispositivo é definido pelos serviços que ele expõe.
ms.assetid: 5b352870-6de1-42f2-a178-ed7036b7afc9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb702adf3ccb0f21bc71f08e98427cca15495f3b
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "105751607"
---
# <a name="implementing-device-behavior"></a><span data-ttu-id="7a6ba-103">Implementando o comportamento do dispositivo</span><span class="sxs-lookup"><span data-stu-id="7a6ba-103">Implementing Device Behavior</span></span>

<span data-ttu-id="7a6ba-104">O comportamento de um dispositivo é definido pelos serviços que ele expõe.</span><span class="sxs-lookup"><span data-stu-id="7a6ba-104">The behavior of a device is defined by the services it exposes.</span></span> <span data-ttu-id="7a6ba-105">Cada serviço tem uma descrição de serviço que lista suas ações e variáveis de estado.</span><span class="sxs-lookup"><span data-stu-id="7a6ba-105">Each service has a service description that lists its actions and state variables.</span></span> <span data-ttu-id="7a6ba-106">Juntas, essas descrições de serviço compõem a interface do serviço, que define a maneira como um ponto de controle pode interagir com um serviço.</span><span class="sxs-lookup"><span data-stu-id="7a6ba-106">Taken together, these service descriptions make up the service interface, which defines the way in which a control point can interact with a service.</span></span> <span data-ttu-id="7a6ba-107">Cada serviço deve ter pelo menos uma ação.</span><span class="sxs-lookup"><span data-stu-id="7a6ba-107">Each service must have at least one action.</span></span>

<span data-ttu-id="7a6ba-108">Para implementar um serviço, um dispositivo hospedado deve fornecer um objeto de Component Object Model (COM) que expõe a interface para o serviço.</span><span class="sxs-lookup"><span data-stu-id="7a6ba-108">To implement a service, a hosted device must provide a Component Object Model (COM) object that exposes the interface for the service.</span></span> <span data-ttu-id="7a6ba-109">Na descrição do serviço, as interfaces de serviço são especificadas na linguagem de modelo UPnP (UTL); no entanto, as interfaces de objeto COM normalmente são especificadas na IDL (Interface Definition Language).</span><span class="sxs-lookup"><span data-stu-id="7a6ba-109">In the service description, the service interfaces are specified in UPnP Template Language (UTL); however, COM object interfaces typically are specified in Interface Definition Language (IDL).</span></span> <span data-ttu-id="7a6ba-110">Você também pode especificar a interface COM em um arquivo de cabeçalho ou biblioteca de tipos.</span><span class="sxs-lookup"><span data-stu-id="7a6ba-110">You can also specify the COM interface in a type library or header file.</span></span> <span data-ttu-id="7a6ba-111">O SDK (Software Development Kit) da plataforma inclui a ferramenta Utl2idl, que traduz uma descrição de serviço em UTL para uma interface COM em IDL.</span><span class="sxs-lookup"><span data-stu-id="7a6ba-111">The Platform Software Development Kit (SDK) includes the Utl2idl tool, which translates a service description in UTL to a COM interface in IDL.</span></span>

<span data-ttu-id="7a6ba-112">Os exemplos a seguir ilustram esse processo de conversão.</span><span class="sxs-lookup"><span data-stu-id="7a6ba-112">The following samples illustrate this conversion process.</span></span> <span data-ttu-id="7a6ba-113">A descrição do serviço é fornecida pelo desenvolvedor do dispositivo e é escrita em UTL.</span><span class="sxs-lookup"><span data-stu-id="7a6ba-113">The service description is provided by the device developer and is written in UTL.</span></span>

``` syntax
<?xml version="1.0" ?> 
  <scpd xmlns="urn:schemas-upnp-org:service-1-0">

    <specVersion>
      <major>1</major> 
      <minor>0</minor> 
    </specVersion>

    <serviceStateTable>
      <stateVariable>
        <name>Power</name> 
        <dataType>Boolean</dataType> 
        <defaultValue>0</defaultValue> 
      </stateVariable>

      <stateVariable>
        <name>Level</name> 
        <dataType>i4</dataType> 
        <allowedValueRange>
          <minimum>0</minimum> 
            <maximum>10</maximum> 
            <step>1</step> 
        </allowedValueRange>
        <defaultValue>0</defaultValue> 
      </stateVariable>

      <stateVariable>
        <name>State</name> 
        <dataType>string</dataType> 
        <allowedValueList>
          <allowedValue>ON</allowedValue> 
          <allowedValue>OFF</allowedValue> 
          <allowedValue>DIMMED</allowedValue> 
        </allowedValueList>
        <defaultValue>OFF</defaultValue> 
      </stateVariable>
    </serviceStateTable>

    <actionList>
      <action>
        <name>PowerOn</name> 
      </action>

      <action>
        <name>PowerOff</name> 
      </action>

      <action>
        <name>SetLevel</name> 
        <argumentList>
          <argument>
            <name>NewLevel</name> 
            <relatedStateVariable>Level</relatedStateVariable> 
            <direction>in</direction> 
          </argument>
          <argument>
            <name>NewState</name> 
            <relatedStateVariable>State</relatedStateVariable> 
            <direction>out</direction> 
          </argument>
        </argumentList>
      </action>

      <action>
        <name>IncreaseLevel</name> 
      </action>

      <action>
        <name>DecreaseLevel</name> 
      </action>
    </actionList>
</scpd>
```

<span data-ttu-id="7a6ba-114">A próxima etapa é executar a ferramenta Utl2idl.</span><span class="sxs-lookup"><span data-stu-id="7a6ba-114">The next step is to run the Utl2idl tool.</span></span> <span data-ttu-id="7a6ba-115">Ele produz o arquivo IDL que contém a interface COM.</span><span class="sxs-lookup"><span data-stu-id="7a6ba-115">It produces the IDL file that contains the COM interface.</span></span> <span data-ttu-id="7a6ba-116">Para obter mais informações sobre arquivos IDL e a palavra-chave da **interface** , consulte [arquivo de definição de interface (IDL)](/windows/desktop/Midl/interface-definition-idl-file) e [**interface**](/windows/desktop/Midl/interface) na referência de MIDL.</span><span class="sxs-lookup"><span data-stu-id="7a6ba-116">For more information about IDL files and the **interface** keyword, see [Interface Definition (IDL) File](/windows/desktop/Midl/interface-definition-idl-file) and [**interface**](/windows/desktop/Midl/interface) in the MIDL reference.</span></span>

``` syntax
#include <windows.h>
typedef [v1_enum] enum SCPD_DISPIDS
{
     DISPID_POWER = 1,
     DISPID_LEVEL,
     DISPID_STATE,
     DISPID_POWERON,
     DISPID_POWEROFF,
     DISPID_SETLEVEL,
     DISPID_INCREASELEVEL,
     DISPID_DECREASELEVEL
} SCPD_DISPIDS;

[
     uuid(68369839-960d-4c8c-8d0d-c319c69e73be),
     oleautomation,
     pointer_default(unique)
]
interface IUPnPService_scpd : IUnknown 
{
     [propget, id(DISPID_POWER), helpstring("Property Power")]
     HRESULT Power(
          [out, retval] VARIANT_BOOL *pPower);

     [propget, id(DISPID_LEVEL), helpstring("Property Level")]
     HRESULT Level(
          [out, retval] long *pLevel);

     [propget, id(DISPID_STATE), helpstring("Property State")]
     HRESULT State(
          [out, retval] BSTR *pState);

     [ id(DISPID_POWERON), helpstring("Method PowerOn")]
     HRESULT PowerOn();

     [ id(DISPID_POWEROFF), helpstring("Method PowerOff")]
     HRESULT PowerOff();

     [ id(DISPID_SETLEVEL), helpstring("Method SetLevel")]
     HRESULT SetLevel(
          [in] long NewLevel,
          [in, out] BSTR *pNewState;
                                
     [ id(DISPID_INCREASELEVEL), helpstring("Method IncreaseLevel")]
     HRESULT IncreaseLevel();

     [ id(DISPID_DECREASELEVEL), helpstring("Method DecreaseLevel")]
     HRESULT DecreaseLevel();
};
```

> [!Note]
> <span data-ttu-id="7a6ba-117">O valor de retorno é o \[ primeiro \] parâmetro de saída na lista de argumentos na descrição do serviço; no entanto, ele é listado como o último parâmetro após a tradução.</span><span class="sxs-lookup"><span data-stu-id="7a6ba-117">The return value is the first \[out\] parameter in the list of arguments in the service description; however, it is listed as the last parameter after translation.</span></span>
> 
> <span data-ttu-id="7a6ba-118">Todos os outros parâmetros permanecem na mesma ordem.</span><span class="sxs-lookup"><span data-stu-id="7a6ba-118">All other parameters remain in the same order.</span></span>

 

<span data-ttu-id="7a6ba-119">Para fornecer a funcionalidade do serviço, implemente essa interface COM.</span><span class="sxs-lookup"><span data-stu-id="7a6ba-119">To provide the functionality of the service, implement this COM interface.</span></span>

## <a name="obtaining-information-about-an-endpoint"></a><span data-ttu-id="7a6ba-120">Obtendo informações sobre um ponto de extremidade</span><span class="sxs-lookup"><span data-stu-id="7a6ba-120">Obtaining Information About an Endpoint</span></span>

<span data-ttu-id="7a6ba-121">Na estrutura UPnP, as informações do ponto de extremidade incluem informações sobre uma solicitação e sua origem.</span><span class="sxs-lookup"><span data-stu-id="7a6ba-121">In the UPnP framework, endpoint information includes information about a request and its source.</span></span> <span data-ttu-id="7a6ba-122">Um dispositivo pode examinar essas informações para tomar uma decisão sobre a solicitação.</span><span class="sxs-lookup"><span data-stu-id="7a6ba-122">A device can examine this information in order to make a decision about the request.</span></span>

<span data-ttu-id="7a6ba-123">Informações de ponto de extremidade estão disponíveis opcionalmente para o serviço implementado.</span><span class="sxs-lookup"><span data-stu-id="7a6ba-123">Endpoint information is optionally available to the implemented service.</span></span> <span data-ttu-id="7a6ba-124">O host do dispositivo tem acesso às informações do ponto de extremidade; no entanto, o host do dispositivo não comunica as informações ao serviço implementado por padrão.</span><span class="sxs-lookup"><span data-stu-id="7a6ba-124">The device host has access to endpoint information; however, the device host does not communicate the information to the implemented service by default.</span></span> <span data-ttu-id="7a6ba-125">Você pode habilitar o host do dispositivo para compartilhar as informações do ponto de extremidade com o serviço implementado, modificando a interface COM no arquivo IDL (produzido pela ferramenta Utl2idl).</span><span class="sxs-lookup"><span data-stu-id="7a6ba-125">You can enable the device host to share the endpoint information with the implemented service by modifying the COM interface in the IDL file (produced by the Utl2idl tool).</span></span> <span data-ttu-id="7a6ba-126">Você pode adicionar um \[ \] parâmetro in para cada método que requer informações de ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="7a6ba-126">You can add an \[in\] parameter to each method that requires endpoint information.</span></span> <span data-ttu-id="7a6ba-127">O \[ parâmetro adicional in \] deve ser o primeiro na lista de argumentos, um ponteiro para uma interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) e explicitamente nomeado **punkRemoteEndpointInfo**.</span><span class="sxs-lookup"><span data-stu-id="7a6ba-127">The additional \[in\] parameter must be the first one in the list of arguments, a pointer to an [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface, and explicitly named **punkRemoteEndpointInfo**.</span></span> <span data-ttu-id="7a6ba-128">As modificações no XML do serviço não são necessárias ou recomendadas.</span><span class="sxs-lookup"><span data-stu-id="7a6ba-128">Modifications to the Service XML are not required, or recommended.</span></span> <span data-ttu-id="7a6ba-129">O exemplo a seguir mostra a nova definição do método de **ativação** quando ele é alterado para que ele receba informações de ponto de extremidade:</span><span class="sxs-lookup"><span data-stu-id="7a6ba-129">The following example shows the new definition of the **PowerOn** method when it is amended so that it receives endpoint information:</span></span>

<span data-ttu-id="7a6ba-130">"HRESULT powery ( \[ em \] IUnknown \* punkRemoteEndpointInfo);"</span><span class="sxs-lookup"><span data-stu-id="7a6ba-130">"HRESULT PowerOn(\[in\] IUnknown \*punkRemoteEndpointInfo);"</span></span>

<span data-ttu-id="7a6ba-131">Um ponteiro para um objeto de informações do ponto de extremidade, uma interface [**IUPnPRemoteEndpointInfo**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpremoteendpointinfo) , é passado por esse novo parâmetro pelo host do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7a6ba-131">A pointer to an endpoint information object, an [**IUPnPRemoteEndpointInfo**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpremoteendpointinfo) interface, is passed through this new parameter by the device host.</span></span> <span data-ttu-id="7a6ba-132">A interface **IUPnPRemoteEndpointInfo** fornece três métodos para acessar as informações do ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="7a6ba-132">The **IUPnPRemoteEndpointInfo** interface provides three methods for accessing the endpoint information.</span></span> <span data-ttu-id="7a6ba-133">Você deve chamar o método apropriado para obter as informações de ponto de extremidade exigidas pela implementação do serviço.</span><span class="sxs-lookup"><span data-stu-id="7a6ba-133">You must call the appropriate method to get the endpoint information that is required by the service implementation.</span></span>

<span data-ttu-id="7a6ba-134">Como alternativa à modificação manual da interface COM, você pode usar a ferramenta Utl2idl com a opção **-CI** .</span><span class="sxs-lookup"><span data-stu-id="7a6ba-134">As an alternative to manual modification of the COM interface, you can use the Utl2idl tool with the **-ci** switch.</span></span> <span data-ttu-id="7a6ba-135">Essa opção faz com que a ferramenta adicione o parâmetro de informações do ponto de extremidade a cada um dos métodos na interface COM.</span><span class="sxs-lookup"><span data-stu-id="7a6ba-135">This switch causes the tool to add the endpoint information parameter to each of the methods in the COM interface.</span></span> <span data-ttu-id="7a6ba-136">Usar a opção **-CI** não facilita a modificação de métodos individuais.</span><span class="sxs-lookup"><span data-stu-id="7a6ba-136">Using the **-ci** switch does not facilitate modification of individual methods.</span></span> <span data-ttu-id="7a6ba-137">Se as informações do ponto de extremidade não forem necessárias para todos os métodos de uma interface, você deverá adicionar o parâmetro manualmente para produzir as implementações mais eficientes.</span><span class="sxs-lookup"><span data-stu-id="7a6ba-137">If endpoint information is not needed by all methods of an interface, you should add the parameter manually in order to produce the most efficient implementations.</span></span>

## <a name="implementing-a-service-object"></a><span data-ttu-id="7a6ba-138">Implementando um objeto de serviço</span><span class="sxs-lookup"><span data-stu-id="7a6ba-138">Implementing a Service Object</span></span>

<span data-ttu-id="7a6ba-139">Você deve usar a ferramenta Utl2idl para converter cada descrição de serviço de um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7a6ba-139">You must use the Utl2idl tool to translate each service description of a device.</span></span>

<span data-ttu-id="7a6ba-140">Um objeto que fornece a funcionalidade para um serviço é chamado de objeto de [*serviço*](s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="7a6ba-140">An object that provides the functionality for a service is referred to as a [*service object*](s-gly.md).</span></span> <span data-ttu-id="7a6ba-141">Além de fornecer a funcionalidade de serviço, os objetos de serviço manipulam erros usando a interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="7a6ba-141">In addition to providing service functionality, service objects handle errors by using the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="7a6ba-142">Para obter mais informações, consulte [usando a API de host do dispositivo com tecnologia UPnP](using-the-device-host-api-with-upnp-technology.md).</span><span class="sxs-lookup"><span data-stu-id="7a6ba-142">For more information, see [Using the Device Host API with UPnP Technology](using-the-device-host-api-with-upnp-technology.md).</span></span>

<span data-ttu-id="7a6ba-143">Para garantir a compatibilidade com Visual Basic, que não oferece \[ suporte \] a parâmetros de saída, a **direção** dos parâmetros **/Direction** na descrição do serviço são convertidas para \[ in, parâmetros de saída \] em IDL.</span><span class="sxs-lookup"><span data-stu-id="7a6ba-143">To ensure compatibility with Visual Basic, which does not support \[out\] parameters, the **direction** out **/direction** parameters in the service description are converted to \[in, out\] parameters in IDL.</span></span> <span data-ttu-id="7a6ba-144">O servidor deve liberar esses \[ parâmetros de saída \] .</span><span class="sxs-lookup"><span data-stu-id="7a6ba-144">The server must free these \[in, out\] parameters.</span></span>

## <a name="implementing-a-device-control-object"></a><span data-ttu-id="7a6ba-145">Implementando um objeto de controle de dispositivo</span><span class="sxs-lookup"><span data-stu-id="7a6ba-145">Implementing a Device Control Object</span></span>

<span data-ttu-id="7a6ba-146">Além de implementar objetos de serviço, você deve implementar um [*objeto de controle de dispositivo*](d-gly.md).</span><span class="sxs-lookup"><span data-stu-id="7a6ba-146">In addition to implementing service objects, you must implement a [*device control object*](d-gly.md).</span></span> <span data-ttu-id="7a6ba-147">Um objeto de controle de dispositivo é o ponto central de gerenciamento e controle para os objetos de serviço do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7a6ba-147">A device control object is the central point of management and control for the device's service objects.</span></span> <span data-ttu-id="7a6ba-148">No momento do registro, o objeto de controle de dispositivo é passado para o host do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7a6ba-148">At registration time, the device control object is passed to the device host.</span></span> <span data-ttu-id="7a6ba-149">Quando chega uma assinatura de evento ou uma solicitação de controle para um dos serviços do dispositivo, o host do dispositivo chama esse objeto de controle de dispositivo para obter o objeto de serviço relevante.</span><span class="sxs-lookup"><span data-stu-id="7a6ba-149">When an event subscription or control request arrives for one of the device's services, the device host calls into this device control object to obtain the relevant service object.</span></span> <span data-ttu-id="7a6ba-150">Nesse momento, o objeto de controle de dispositivo cria uma instância do objeto de serviço ou retorna a interface de uma instância existente do objeto de serviço.</span><span class="sxs-lookup"><span data-stu-id="7a6ba-150">At that time, the device control object either creates an instance of the service object or returns the interface of an existing instance of the service object.</span></span>

<span data-ttu-id="7a6ba-151">Você pode registrar uma descrição de dispositivo em vários computadores ou várias vezes no mesmo computador.</span><span class="sxs-lookup"><span data-stu-id="7a6ba-151">You can register a device description on multiple computers or multiple times on the same computer.</span></span> <span data-ttu-id="7a6ba-152">Como o nome do dispositivo exclusivo (UDN) deve ser diferente para cada instância do dispositivo, o host do dispositivo gera um UDN exclusivo para cada dispositivo e dispositivo inserido toda vez que o dispositivo é registrado.</span><span class="sxs-lookup"><span data-stu-id="7a6ba-152">Because the Unique Device Name (UDN) must be different for each instance of the device, the device host generates a unique UDN for each device and embedded device each time the device is registered.</span></span> <span data-ttu-id="7a6ba-153">Use o UDN especificado no modelo de descrição do dispositivo para obter o UDN real gerado pelo host do dispositivo e associado ao dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7a6ba-153">Use the UDN specified in the device description template to obtain the actual UDN generated by the device host and associated with the device.</span></span> <span data-ttu-id="7a6ba-154">Para cancelar o registro de um dispositivo, você deve usar a ID fornecida pela estrutura UPnP quando o dispositivo foi registrado.</span><span class="sxs-lookup"><span data-stu-id="7a6ba-154">To unregister a device, you must use the ID provided by the UPnP framework when the device was registered.</span></span>

<span data-ttu-id="7a6ba-155">Os objetos de controle de dispositivo devem implementar a interface [**IUPnPDeviceControl**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpdevicecontrol) .</span><span class="sxs-lookup"><span data-stu-id="7a6ba-155">Device control objects must implement the [**IUPnPDeviceControl**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpdevicecontrol) interface.</span></span> <span data-ttu-id="7a6ba-156">O host do dispositivo invoca o método [**IUPnPDeviceControl:: Initialize**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpdevicecontrol-initialize) do objeto de controle de dispositivo, passando a descrição do dispositivo baseado em UPnP que o host do dispositivo publicou anteriormente para o dispositivo e uma cadeia de inicialização que foi especificada no momento do registro (consulte [registrando um dispositivo hospedado no host do dispositivo](registering-a-hosted-device-with-the-device-host.md)).</span><span class="sxs-lookup"><span data-stu-id="7a6ba-156">The device host invokes the [**IUPnPDeviceControl::Initialize**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpdevicecontrol-initialize) method of the device control object, passing in the UPnP-based device description that the device host previously published for the device and an initialization string that was specified at registration time (see [Registering a Hosted Device with the Device Host](registering-a-hosted-device-with-the-device-host.md)).</span></span> <span data-ttu-id="7a6ba-157">A partir dessa descrição do dispositivo, o objeto de controle de dispositivo lê o UDNs atribuído a cada um dos dispositivos na árvore do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7a6ba-157">From this device description, the device control object reads the UDNs assigned to each of the devices in the device tree.</span></span> <span data-ttu-id="7a6ba-158">Você também pode usar o método [**IUPnPRegistrar:: GetUniqueDeviceName**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-getuniquedevicename) para obter essas informações.</span><span class="sxs-lookup"><span data-stu-id="7a6ba-158">You can also use the [**IUPnPRegistrar::GetUniqueDeviceName**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-getuniquedevicename) method to obtain this information.</span></span>

<span data-ttu-id="7a6ba-159">Quando o host do dispositivo requer um ponteiro para um objeto de serviço que implementa um serviço específico, ele invoca o método [**IUPnPDeviceControl:: GetServiceObject**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpdevicecontrol-getserviceobject) no objeto de controle de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7a6ba-159">When the device host requires a pointer to a service object that implements a particular service, it invokes the [**IUPnPDeviceControl::GetServiceObject**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpdevicecontrol-getserviceobject) method on the device control object.</span></span> <span data-ttu-id="7a6ba-160">O host do dispositivo passa o UDN e a ID do serviço para o qual ele está solicitando um objeto de serviço e o endereço de um ponteiro [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) no qual o método deve retornar um ponteiro para o objeto de serviço.</span><span class="sxs-lookup"><span data-stu-id="7a6ba-160">The device host passes the UDN and the service ID of the service for which it is requesting a service object and the address of an [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) pointer at which the method is expected to return a pointer to the service object.</span></span> <span data-ttu-id="7a6ba-161">O parâmetro UDN é necessário porque o objeto de controle de dispositivo gerencia os serviços para toda a árvore de dispositivos, incluindo dispositivos aninhados.</span><span class="sxs-lookup"><span data-stu-id="7a6ba-161">The UDN parameter is necessary because the device control object manages services for the entire device tree, including nested devices.</span></span> <span data-ttu-id="7a6ba-162">Se o host do dispositivo solicitar um dispositivo aninhado, **GetServiceObject** usará o UDN para identificá-lo.</span><span class="sxs-lookup"><span data-stu-id="7a6ba-162">If the device host requests a nested device, **GetServiceObject** uses the UDN to identify it.</span></span>

 

 