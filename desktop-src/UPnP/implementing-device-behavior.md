---
title: Implementando o comportamento do dispositivo
description: O comportamento de um dispositivo é definido pelos serviços que ele expõe.
ms.assetid: 5b352870-6de1-42f2-a178-ed7036b7afc9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fce2857c11a02ef5eeebe7b2cd5e75ee76138929e5bd95a2e3bdfa7ffd2c71dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119137259"
---
# <a name="implementing-device-behavior"></a>Implementando o comportamento do dispositivo

O comportamento de um dispositivo é definido pelos serviços que ele expõe. Cada serviço tem uma descrição de serviço que lista suas ações e variáveis de estado. Juntas, essas descrições de serviço compõem a interface do serviço, que define a maneira como um ponto de controle pode interagir com um serviço. Cada serviço deve ter pelo menos uma ação.

Para implementar um serviço, um dispositivo hospedado deve fornecer um objeto de Component Object Model (COM) que expõe a interface para o serviço. Na descrição do serviço, as interfaces de serviço são especificadas na linguagem de modelo UPnP (UTL); no entanto, as interfaces de objeto COM normalmente são especificadas na IDL (Interface Definition Language). Você também pode especificar a interface COM em um arquivo de cabeçalho ou biblioteca de tipos. O SDK (Software Development Kit) da plataforma inclui a ferramenta Utl2idl, que traduz uma descrição de serviço em UTL para uma interface COM em IDL.

Os exemplos a seguir ilustram esse processo de conversão. A descrição do serviço é fornecida pelo desenvolvedor do dispositivo e é escrita em UTL.

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

A próxima etapa é executar a ferramenta Utl2idl. Ele produz o arquivo IDL que contém a interface COM. Para obter mais informações sobre arquivos IDL e a palavra-chave da **interface** , consulte [arquivo de definição de interface (IDL)](/windows/desktop/Midl/interface-definition-idl-file) e [**interface**](/windows/desktop/Midl/interface) na referência de MIDL.

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
> O valor de retorno é o \[ primeiro \] parâmetro de saída na lista de argumentos na descrição do serviço; no entanto, ele é listado como o último parâmetro após a tradução.
> 
> Todos os outros parâmetros permanecem na mesma ordem.

 

Para fornecer a funcionalidade do serviço, implemente essa interface COM.

## <a name="obtaining-information-about-an-endpoint"></a>Obtendo informações sobre um ponto de extremidade

Na estrutura UPnP, as informações do ponto de extremidade incluem informações sobre uma solicitação e sua origem. Um dispositivo pode examinar essas informações para tomar uma decisão sobre a solicitação.

Informações de ponto de extremidade estão disponíveis opcionalmente para o serviço implementado. O host do dispositivo tem acesso às informações do ponto de extremidade; no entanto, o host do dispositivo não comunica as informações ao serviço implementado por padrão. Você pode habilitar o host do dispositivo para compartilhar as informações do ponto de extremidade com o serviço implementado, modificando a interface COM no arquivo IDL (produzido pela ferramenta Utl2idl). Você pode adicionar um \[ \] parâmetro in para cada método que requer informações de ponto de extremidade. O \[ parâmetro adicional in \] deve ser o primeiro na lista de argumentos, um ponteiro para uma interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) e explicitamente nomeado **punkRemoteEndpointInfo**. As modificações no XML do serviço não são necessárias ou recomendadas. O exemplo a seguir mostra a nova definição do método de **ativação** quando ele é alterado para que ele receba informações de ponto de extremidade:

"HRESULT powery ( \[ em \] IUnknown \* punkRemoteEndpointInfo);"

Um ponteiro para um objeto de informações do ponto de extremidade, uma interface [**IUPnPRemoteEndpointInfo**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpremoteendpointinfo) , é passado por esse novo parâmetro pelo host do dispositivo. A interface **IUPnPRemoteEndpointInfo** fornece três métodos para acessar as informações do ponto de extremidade. Você deve chamar o método apropriado para obter as informações de ponto de extremidade exigidas pela implementação do serviço.

Como alternativa à modificação manual da interface COM, você pode usar a ferramenta Utl2idl com a opção **-CI** . Essa opção faz com que a ferramenta adicione o parâmetro de informações do ponto de extremidade a cada um dos métodos na interface COM. Usar a opção **-CI** não facilita a modificação de métodos individuais. Se as informações do ponto de extremidade não forem necessárias para todos os métodos de uma interface, você deverá adicionar o parâmetro manualmente para produzir as implementações mais eficientes.

## <a name="implementing-a-service-object"></a>Implementando um objeto de serviço

Você deve usar a ferramenta Utl2idl para converter cada descrição de serviço de um dispositivo.

Um objeto que fornece a funcionalidade para um serviço é chamado de objeto de [*serviço*](s-gly.md). Além de fornecer a funcionalidade de serviço, os objetos de serviço manipulam erros usando a interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . Para obter mais informações, consulte [usando a API de host do dispositivo com tecnologia UPnP](using-the-device-host-api-with-upnp-technology.md).

para garantir a compatibilidade com Visual Basic, que não oferece \[ suporte \] a parâmetros de saída, a **direção** dos parâmetros **/direction** na descrição do serviço são convertidas para \[ in, parâmetros de saída \] em IDL. O servidor deve liberar esses \[ parâmetros de saída \] .

## <a name="implementing-a-device-control-object"></a>Implementando um objeto de controle de dispositivo

Além de implementar objetos de serviço, você deve implementar um [*objeto de controle de dispositivo*](d-gly.md). Um objeto de controle de dispositivo é o ponto central de gerenciamento e controle para os objetos de serviço do dispositivo. No momento do registro, o objeto de controle de dispositivo é passado para o host do dispositivo. Quando chega uma assinatura de evento ou uma solicitação de controle para um dos serviços do dispositivo, o host do dispositivo chama esse objeto de controle de dispositivo para obter o objeto de serviço relevante. Nesse momento, o objeto de controle de dispositivo cria uma instância do objeto de serviço ou retorna a interface de uma instância existente do objeto de serviço.

Você pode registrar uma descrição de dispositivo em vários computadores ou várias vezes no mesmo computador. Como o nome do dispositivo exclusivo (UDN) deve ser diferente para cada instância do dispositivo, o host do dispositivo gera um UDN exclusivo para cada dispositivo e dispositivo inserido toda vez que o dispositivo é registrado. Use o UDN especificado no modelo de descrição do dispositivo para obter o UDN real gerado pelo host do dispositivo e associado ao dispositivo. Para cancelar o registro de um dispositivo, você deve usar a ID fornecida pela estrutura UPnP quando o dispositivo foi registrado.

Os objetos de controle de dispositivo devem implementar a interface [**IUPnPDeviceControl**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpdevicecontrol) . O host do dispositivo invoca o método [**IUPnPDeviceControl:: Initialize**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpdevicecontrol-initialize) do objeto de controle de dispositivo, passando a descrição do dispositivo baseado em UPnP que o host do dispositivo publicou anteriormente para o dispositivo e uma cadeia de inicialização que foi especificada no momento do registro (consulte [registrando um dispositivo hospedado no host do dispositivo](registering-a-hosted-device-with-the-device-host.md)). A partir dessa descrição do dispositivo, o objeto de controle de dispositivo lê o UDNs atribuído a cada um dos dispositivos na árvore do dispositivo. Você também pode usar o método [**IUPnPRegistrar:: GetUniqueDeviceName**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-getuniquedevicename) para obter essas informações.

Quando o host do dispositivo requer um ponteiro para um objeto de serviço que implementa um serviço específico, ele invoca o método [**IUPnPDeviceControl:: GetServiceObject**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpdevicecontrol-getserviceobject) no objeto de controle de dispositivo. O host do dispositivo passa o UDN e a ID do serviço para o qual ele está solicitando um objeto de serviço e o endereço de um ponteiro [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) no qual o método deve retornar um ponteiro para o objeto de serviço. O parâmetro UDN é necessário porque o objeto de controle de dispositivo gerencia os serviços para toda a árvore de dispositivos, incluindo dispositivos aninhados. Se o host do dispositivo solicitar um dispositivo aninhado, **GetServiceObject** usará o UDN para identificá-lo.

 

 