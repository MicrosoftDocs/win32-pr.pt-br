---
title: Host de serviço
description: O host de serviço é o ambiente de tempo de execução para hospedar um serviço em um processo.
ms.assetid: 42e4d24d-5611-4561-b874-6dc3f3f88c73
keywords:
- Serviços Web do host de serviço para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0170f7dc0dfda99887b7d11d68d073517e0eb85f
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/12/2021
ms.locfileid: "105784653"
---
# <a name="service-host"></a>Host de serviço

O host de serviço é o ambiente de tempo de execução para hospedar um serviço em um processo.


Um serviço pode configurar um ou mais pontos de extremidade dentro de um host de serviço.

![Diagrama que mostra a estrutura de um host de serviço que contém um ponto de extremidade de serviço.](images/servicehost.png)

## <a name="creating-a-service-host"></a>Criando um host de serviço

Antes de criar um host de serviço, um serviço precisa definir seus pontos de extremidade. Um ponto de extremidade no host de serviço é especificado na estrutura de [**\_ ponto de \_ extremidade de serviço WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) e é definido pelas seguintes informações:

-   Um endereço, que é o URI físico no qual o serviço será hospedado.
-   Uma estrutura de [**\_ \_ tipo de canal do WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) que especifica o tipo do canal subjacente para o ponto de extremidade.
-   Uma estrutura de [**\_ \_ associação do WS Channel**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) que especifica a associação do canal.
-   Uma estrutura de [**\_ \_ Descrição de segurança do WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) que contém a descrição de segurança para o ponto de extremidade.
-   Uma estrutura de [**\_ \_ contrato de serviço WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_contract) que representa o [contrato de serviço](contract.md) para o ponto de extremidade.
-   Uma estrutura de [**retorno de chamada do WS \_ Service \_ Security \_**](/windows/desktop/api/WebServices/nc-webservices-ws_service_security_callback) que especifica uma função de retorno de chamada de autorização para o ponto de extremidade.
-   Uma estrutura de [**\_ propriedade de ponto de \_ extremidade \_ de serviço WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint_property) que contém uma matriz de propriedades de ponto de extremidade de serviço.

``` syntax
WS_SERVICE_ENDPOINT serviceEndpoint = {0};
const WS_SERVICE_ENDPOINT* serviceEndpoints[1];
serviceEndpoints[0] = &serviceEndpoint;
WS_STRING url = WS_STRING_VALUE(L"net.tcp://+/Example");

// Method based service contract for the service
static WS_SERVICE_CONTRACT calculatorContract = 
{
    &calculatorContractDescription, // comes from a generated header.
    NULL,
    &calculatorFunctions, // specified by the application
};

serviceEndpoint.address.url = &url;
serviceEndpoint.binding.channelBinding =  WS_TCP_CHANNEL_BINDING; 
serviceEndpoint.contract = &calculatorContract;  
serviceEndpoint.channelType = WS_CHANNEL_TYPE_DUPLEX_SESSION; 
serviceEndpoint.authorizationCallback = AuthorizationCallback; // Authorization callback.
```

Somente contratos unidirecionais têm suporte para SOAP sobre UDP, representado pela [**\_ Associação de \_ canal \_ do WS UDP**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) na enumeração de **associação do WS \_ Channel \_** .

Depois que um ponto de extremidade é definido, ele pode ser passado para a função [**WsCreateServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wscreateservicehost) , que usa uma matriz de ponteiros para estruturas de [**ponto de \_ \_ extremidade de serviço WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) .

``` syntax
HRESULT hr = WsCreateServiceHost (serviceEndpoints, 1, NULL, 0, &host, error);
```

Um aplicativo pode, opcionalmente, fornecer uma matriz de [**Propriedades de serviço**](/windows/desktop/api/WebServices/ns-webservices-ws_service_property) para [**WsCreateServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wscreateservicehost) para definir configurações personalizadas no host de serviço.

Um aplicativo abre o host de serviço para iniciar a aceitação de solicitações de cliente.

``` syntax
WsOpenServiceHost(serviceHost, NULL, NULL);
```

Depois de abrir o host de serviço, o aplicativo poderá fechá-lo se não houver mais operações que o exijam. Observe que isso não libera seus recursos e que pode ser reaberto com uma chamada subsequente para [**WsResetServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wsresetservicehost).

``` syntax
WsCloseServiceHost(serviceHost, NULL, NULL);
```

Depois de fechar o host de serviço, um aplicativo pode redefinir o host de serviço para reutilização.

``` syntax
WsResetServiceHost(serviceHost, NULL);
```

Quando o aplicativo é feito com o host de serviço, ele pode liberar os recursos associados ao host de serviço chamando a função [**WsFreeServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wsfreeservicehost) . Observe que [**WsCloseServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wscloseservicehost) deve ser chamado antes de chamar essa função.

``` syntax
WsFreeServiceHost(serviceHost, NULL);
```

Para obter informações sobre como anexar um estado personalizado ao host de serviço, consulte [estado do host do usuário](user-host-state.md)

Para obter informações sobre autorização em um host de serviço para um determinado ponto de extremidade, consulte [autorização de serviço](service-authorization.md).

Para Iinformation sobre como implementar operações de serviço e contratos de serviço para um serviço, consulte os tópicos [operações de serviço](server-side-service-operations.md) e [contrato de serviço](contract.md).

## <a name="security"></a>Segurança

Um aplicativo pode usar as propriedades de acompanhamento para controlar a quantidade de recursos alocados pelo host de serviço em nome do aplicativo:

-   [**WS \_ Propriedade de ponto de extremidade de serviço \_ \_ \_ máximo \_ aceitando \_ canais**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id),
-   [**WS \_ Propriedade de ponto de extremidade de serviço- \_ \_ \_ \_ simultaneidade máxima**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id),
-   [**WS \_ Propriedade de ponto de extremidade de serviço \_ \_ máximo de \_ \_ canais**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id),
-   [**WS \_ \_ \_ \_ \_ \_ \_ tamanho máximo do heap de corpo da propriedade de ponto de extremidade de serviço**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id),
-   [**WS \_ Propriedade de ponto de extremidade de serviço \_ \_ \_ tamanho máximo do \_ \_ pool \_ de chamadas**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id),
-   [**WS \_ Propriedade de ponto de extremidade de serviço \_ \_ \_ tamanho máximo do \_ \_ pool \_ de canais**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id).

Os padrões seguros são escolhidos para cada uma dessas propriedades, um aplicativo deve ser cuidadoso se quiser modificar essas propriedades. Além das propriedades mencionadas acima, as propriedades de [canal](channel.md), de [ouvinte](listener.md) e de [mensagem](message.md) específicas também podem ser modificadas pelo aplicativo. Consulte as considerações de segurança desses componentes antes de modificar qualquer uma dessas configurações.

Além disso, as seguintes considerações de design de aplicativo devem ser avaliadas cuidadosamente ao usar a API de host do serviço WWSAPI:

-   Ao usar MEX, os aplicativos devem ter cuidado para não divulgar dados confidenciais. Como uma mitigação, se a natureza dos dados expostos por meio de MEX for confidencial, os aplicativos poderão optar por configurar o ponto de extremidade MEX com uma associação segura que exija autenticação no mínimo e implementar a autorização como parte do ponto de extremidade usando o [**retorno de chamada de \_ segurança do serviço \_ \_ WS**](/windows/desktop/api/WebServices/nc-webservices-ws_service_security_callback).
-   Por padrão, as informações de erro avançadas por meio de falhas estão desabilitadas no host de serviço pela propriedade de [**divulgação de falha de \_ Propriedade do serviço \_ \_ \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_service_property_id) . É mediante a vontade do aplicativo enviar informações de erro avançadas como parte da falha. No entanto, isso pode resultar em divulgação de informações e, portanto, é recomendável que essa configuração seja alterada apenas para cenários de depuração.
-   Além da validação executada para o perfil básico 2,0 e a serialização XML, o host de serviço não executa nenhuma validação no conteúdo de dados recebido como parte dos parâmetros de operação de serviço. É responsabilidade do aplicativo executar todas as validações de parâmetro por conta própria.
-   A autorização não é implementada como parte do host de serviço. No entanto, os aplicativos podem implementar seu próprio esquema de autorização usando a [**\_ \_ Descrição de segurança do WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) e o retorno de [**\_ \_ \_ chamada de segurança do serviço WS**](/windows/desktop/api/WebServices/nc-webservices-ws_service_security_callback).
-   É responsabilidade do aplicativo usar associações seguras em seu ponto de extremidade. O host de serviço não fornece nenhuma segurança além do que está configurado no ponto de extremidade.

Os seguintes elementos de API são usados com o host de serviço.

| Callback                                                                             | Description                                                                     |
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [**\_retorno de \_ chamada de canal de aceitação de serviço WS \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_service_accept_channel_callback) | Chamado quando um canal é aceito em um ouvinte de ponto de extremidade pelo host de serviço. |
| [**\_retorno de \_ chamada de canal de fechamento de serviço WS \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_service_close_channel_callback)   | Chamado quando um canal é fechado ou anulado em um ponto de extremidade.                     |



 



| Enumeração                                                                    | Descrição                                                                                 |
|--------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [**ID da Propriedade do ponto de extremidade do \_ serviço WS \_ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id) | Parâmetros opcionais para configurar [**um \_ ponto de \_ extremidade de serviço WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint). |
| [**\_estado do \_ host de serviço WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_service_host_state)                      | Os Estados em que um host de serviço pode estar.                                                   |
| [**\_ID da \_ Propriedade do serviço WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_service_property_id)                    | Parâmetros opcionais para configurar o host de serviço.                                       |



 



| Função                                                     | Descrição                                                                                  |
|--------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [**WsAbortServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wsabortservicehost)             | Interrompe e descontinua as operações atuais no host de serviço.                          |
| [**WsCloseServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wscloseservicehost)             | Fecha todos os ouvintes para que nenhum novo canal seja aceito do cliente.                   |
| [**WsCreateServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wscreateservicehost)           | Cria um host de serviço.                                                                      |
| [**WsFreeServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wsfreeservicehost)               | Libera a memória associada a um objeto de host de serviço.                                   |
| [**WsGetServiceHostProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetservicehostproperty) | Recupera uma propriedade de host de serviço especificada.                                                 |
| [**WsOpenServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wsopenservicehost)               | Abre um host de serviço para comunicação e inicia os ouvintes em todos os pontos de extremidade.        |
| [**WsResetServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wsresetservicehost)             | Redefine o host de serviço para reutilização e redefine o canal subjacente e os ouvintes para reutilização. |



 



| Handle                                       | Description                                      |
|----------------------------------------------|--------------------------------------------------|
| [**\_host de serviço WS \_**](ws-service-host.md) | Um tipo opaco usado para fazer referência a um host de serviço. |



 



| Estrutura                                                                              | Description                                                                     |
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [**ponto de extremidade de \_ serviço WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint)                                   | Representa um ponto de extremidade individual em um host de serviço.                            |
| [**\_propriedade de \_ ponto de extremidade de serviço WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint_property)                | Especifica uma configuração específica do serviço.                                           |
| [**\_Propriedade do serviço WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_service_property)                                   | Especifica uma configuração específica do serviço.                                           |
| [**\_retorno de \_ chamada de aceitação de Propriedade do serviço WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_service_property_accept_callback) | Especifica o retorno de chamada que é chamado quando um canal é aceito com êxito. |
| [**\_retorno de \_ chamada de fechamento da propriedade de serviço WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_service_property_close_callback)   | Especifica o retorno de chamada que é chamado quando um canal está prestes a ser fechado.    |



 

 

 




