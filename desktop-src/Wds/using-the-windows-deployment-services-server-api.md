---
title: Uso da API de servidor de Serviços de Implantação do Windows
description: Em ambientes em que a solução padrão WDS (serviços de implantação do Windows) não pode ser usada, o servidor WDS expõe uma API que permite aos desenvolvedores escrever plug-ins, conhecidos como provedores, para lidar com solicitações de PXE (Preboot Execution Environment).
ms.assetid: 5e25654a-33c6-4c0f-acc3-e938d1f4a4e7
keywords:
- Serviços de implantação do Windows serviços de implantação do Windows, usando a API do servidor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3634dffa73eddc9b5db92be6bc807cccbc5248f
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2020
ms.locfileid: "103640338"
---
# <a name="using-the-windows-deployment-services-server-api"></a>Uso da API de servidor de Serviços de Implantação do Windows

Em ambientes em que a solução padrão WDS (serviços de implantação do Windows) não pode ser usada, o servidor WDS expõe uma API que permite aos desenvolvedores escrever plug-ins, conhecidos como provedores, para lidar com solicitações de PXE (Preboot Execution Environment). Os desenvolvedores devem aderir às seguintes diretrizes ao escrever provedores PXE para o WDS.

## <a name="install-the-wds-role-on-the-server"></a>Instalar a função do WDS no servidor

-   O WDS (serviços de implantação do Windows) é a versão revisada do RIS (serviços de instalação remota), você precisará da função de servidor do WDS para implementar o servidor PXE do WDS e os provedores.
-   O WDS substitui o RIS como o componente padrão a partir do Windows Server 2008 e do Windows Server 2003 com Service Pack 2 (SP2).
-   Você deve atualizar o servidor RIS para o WDS no Windows Server 2003 com Service Pack 1 (SP1). Você pode instalar a função de servidor do WDS com o [WAIK (Kit de instalação automatizada do Windows)](https://www.microsoft.com/download/details.aspx?id=10333).

## <a name="register-providers"></a>Registrar provedores

-   Registre a DLL (biblioteca de vínculo dinâmico) do provedor durante a instalação e insira o provedor na lista ordenada de provedores registrados.
    > [!Note]  
    > Ao instalar um provedor novo ou modificado, será necessário reiniciar o serviço WDS PXE para que as alterações entrem em vigor.

     

-   Use a função [**PxeProviderRegister**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeproviderregister) para registrar o provedor e adicioná-lo à lista. Use a função [**PxeProviderUnRegister**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeproviderunregister) para cancelar o registro de um provedor registrado e removê-lo da lista.
-   Especifique a sequência do provedor na lista ordenada. O índice de um provedor na lista não pode ser garantido porque outro provedor pode ser registrado posteriormente antes dele. Para inserir o provedor na lista antes ou depois de outro provedor registrado, primeiro use a função [**PxeProviderQueryIndex**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeproviderqueryindex) para obter o índice do provedor registrado e, em seguida, registre o novo provedor ao especificar um valor de índice maior ou menor.
-   A instalação pode armazenar informações de configuração do provedor na chave do registro retornada quando o provedor é registrado. O endereço da chave do registro é recebido pelo *phProviderKey* de [**PxeProviderRegister**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeproviderregister). O provedor recebe um identificador para essa mesma chave como o parâmetro *hProviderKey* para seu retorno de chamada [*PxeProviderInitialize*](pxeproviderinitialize.md) . O provedor deve armazenar o endereço dessa chave.
-   Sempre instale a DLL (biblioteca de vínculo dinâmico) do provedor na pasta arquivos de programas do servidor.

## <a name="initialize"></a>Inicializar

-   Inclua uma DLL que exporta a função de retorno de chamada [*PxeProviderInitialize*](pxeproviderinitialize.md) no provedor. Cada provedor requer um retorno de chamada *PxeProviderInitialize* . Quando o WDS carrega um provedor, ele chama a função *PxeProviderInitialize* do provedor e passa um identificador para a mesma chave que é usada para armazenar informações de configuração durante o registro do provedor.
-   Quando o retorno de chamada [*PxeProviderInitialize*](pxeproviderinitialize.md) retorna e é bem-sucedido, o provedor deve ser totalmente inicializado e pronto para processar solicitações.
-   Registre cada retorno de chamada no provedor durante o processamento da função [*PxeProviderInitialize*](pxeproviderinitialize.md) . Os retornos de chamada devem ser registrados com a função [**PxeRegisterCallback**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeregistercallback) .
-   Inicialize todos os recursos internos do provedor dentro do processamento de sua função [*PxeProviderInitialize*](pxeproviderinitialize.md) .

## <a name="shutdown"></a>Desligar

-   Implemente o retorno de chamada [*PxeProviderShutdown*](pxeprovidershutdown.md) . Todo provedor precisa ter um retorno de chamada *PxeProviderShutdown*.
-   A função de retorno de chamada [*PxeProviderShutdown*](pxeprovidershutdown.md) deve desligar completamente o provedor e liberar todos os seus recursos.
-   Depois que o retorno de chamada [*PxeProviderShutdown*](pxeprovidershutdown.md) retorna, o identificador *hProvider* passado para a função [*PxeProviderInitialize*](pxeproviderinitialize.md) não é mais válido e não deve ser usado para chamar o WDS.
-   Registre o retorno de chamada [*PxeProviderShutdown*](pxeprovidershutdown.md) chamando a função [**PxeRegisterCallback**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeregistercallback) com o **\_ \_ desligamento de retorno de chamada PXE** durante o processamento do retorno de chamada [*PxeProviderInitialize*](pxeproviderinitialize.md) . Não chame o retorno de chamada *PxeProviderShutdown* se a função *PxeProviderInitialize* falhar.

## <a name="handle-request-packet"></a>Processar pacote de solicitação

Implemente o retorno de chamada [*PxeProviderRecvRequest*](pxeproviderrecvrequest.md) para o provedor. Todo provedor precisa ter um retorno de chamada *PxeProviderRecvRequest* . Quando o WDS recebe uma solicitação, ele chama o retorno de chamada *PxeProviderRecvRequest* para o primeiro provedor na lista de provedores registrados.

-   Se o provedor processar essa solicitação de forma síncrona, a função [*PxeProviderRecvRequest*](pxeproviderrecvrequest.md) deverá retornar um valor **de \_ êxito de erro**. Se e somente se o provedor processar essa solicitação de forma assíncrona, o retorno de chamada *PxeProviderRecvRequest* deverá retornar o **erro e \_ /s \_ pendente** e chamará a função [**PxeAsyncRecvDone**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeasyncrecvdone) quando a solicitação tiver sido processada.
-   O retorno de chamada [*PxeProviderRecvRequest*](pxeproviderrecvrequest.md) e a função [**PxeAsyncRecvDone**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeasyncrecvdone) retorna o endereço de uma enumeração de **\_ \_ ação de inicialização PXE** que descreve a ação realizada pelo provedor para manipular a solicitação.

    Há quatro maneiras de um provedor lidar com uma solicitação:

    -   O provedor responde ao cliente com um pacote de resposta DHCP padrão que contém um caminho para o programa de inicialização de rede. Retornar o valor de **\_ \_ NBP da BA PXE** para a enumeração significa que o provedor processou com êxito o pacote de solicitação e concluiu a solicitação enviando um pacote de resposta chamando as funções [**PxePacketAllocate**](/windows/win32/api/WdsPxe/nf-wdspxe-pxepacketallocate) e [**PxeSendReply**](/windows/win32/api/WdsPxe/nf-wdspxe-pxesendreply) .
    -   O provedor responde ao cliente com um pacote de resposta personalizado que não está em conformidade com o DHCP. Retornar o **valor \_ \_ personalizado de Ba do PXE** para enum significa que o provedor processou com êxito o pacote de solicitação e concluiu a solicitação enviando um pacote de resposta personalizado chamando as funções [**PxePacketAllocate**](/windows/win32/api/WdsPxe/nf-wdspxe-pxepacketallocate) e [**PxeSendReply**](/windows/win32/api/WdsPxe/nf-wdspxe-pxesendreply) .
    -   O provedor determina que a solicitação deve ser ignorada. Retornar o valor de **\_ \_ ignorar BA do PXE** para a enumeração significa que o provedor liberou todos os recursos associados à solicitação e a solicitação não é passada para o próximo provedor na lista de provedores registrados. Os provedores podem usar essa opção se detectarem que um pacote de solicitação é inválido.
    -   O provedor recusa a atender à solicitação. Retornar o valor de **\_ \_ rejeição de Ba do PXE** para a enumeração instrui o sistema a passar a solicitação para o próximo provedor na lista de provedores registrados. Se esse for o último provedor na lista, isso liberará todos os recursos associados à solicitação e a solicitação será ignorada.
    -   Registre o retorno de chamada [*PxeProviderRecvRequest*](pxeproviderrecvrequest.md) chamando a função [**PxeRegisterCallback**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeregistercallback) com a solicitação de **recebimento de retorno de \_ chamada \_ \_ PXE** durante o processamento do retorno de chamada [*PxeProviderInitialize*](pxeproviderinitialize.md) .

## <a name="generate-response-packet"></a>Gerar pacote de resposta

-   Use a API para gravar provedores para lidar com solicitações DHCP e gerar pacotes de resposta.
-   A função [**PxeProviderSetAttribute**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeprovidersetattribute) especifica os atributos usados pelo provedor para filtrar os pacotes. Os atributos do provedor podem ser especificados para que o provedor Veja todos os pacotes, o provedor vê apenas os pacotes DHCP ou o provedor vê somente os pacotes DHCP que especificam a opção de identificador de classe de fornecedor DHCP (60) como "PXEClient".
-   A função [**PxeDhcpIsValid**](/windows/win32/api/WdsPxe/nf-wdspxe-pxedhcpisvalid) verifica se um pacote é um pacote DHCP válido. Os provedores podem usar a função **PxeDhcpIsValid** para verificar se um pacote do cliente é um pacote DHCP quando o conjunto de filtros com a função [**PxeProviderSetAttribute**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeprovidersetattribute) é definido para receber todos os pacotes para determinar se um pacote especificado é um pacote DHCP válido.
-   A função [**PxeDhcpInitialize**](/windows/win32/api/WdsPxe/nf-wdspxe-pxedhcpinitialize) Inicializa um pacote de resposta como um pacote de resposta DHCP baseado nas informações de um pacote recebido do cliente. A função [*PxeProviderInitialize*](pxeproviderinitialize.md) pega o endereço de um pacote DHCP válido recebido do cliente no retorno de chamada [*PxeProviderRecvRequest*](pxeproviderrecvrequest.md) . A função **PxeDhcpInitialize** usa um ponteiro para um pacote de resposta alocado com a função [**PxePacketAllocate**](/windows/win32/api/WdsPxe/nf-wdspxe-pxepacketallocate) .
-   A função [**PxeDhcpGetOptionValue**](/windows/win32/api/WdsPxe/nf-wdspxe-pxedhcpgetoptionvalue) recupera um valor de opção de um pacote DHCP. A função [**PxeDhcpGetVendorOptionValue**](/windows/win32/api/WdsPxe/nf-wdspxe-pxedhcpgetvendoroptionvalue) recupera um valor de opção do campo informações específicas do fornecedor (43) de um pacote DHCP.
-   O provedor pode então popular o pacote de resposta com informações e usar a função [**PxeSendReply**](/windows/win32/api/WdsPxe/nf-wdspxe-pxesendreply) para enviar o pacote de resposta ao cliente. A função [**PxeDhcpAppendOption**](/windows/win32/api/WdsPxe/nf-wdspxe-pxedhcpappendoption) acrescenta uma opção DHCP ao pacote de resposta.
-   Um provedor que responde às solicitações do cliente enviando um pacote deve alocar o pacote de resposta usando a função [**PxePacketAllocate**](/windows/win32/api/WdsPxe/nf-wdspxe-pxepacketallocate) . O provedor pode então popular o pacote de resposta com informações e usar a função [**PxeSendReply**](/windows/win32/api/WdsPxe/nf-wdspxe-pxesendreply) para enviar o pacote de resposta ao cliente.
-   Quando a memória alocada não for mais necessária, o provedor deverá liberá-la usando a função [**PxePacketFree**](/windows/win32/api/WdsPxe/nf-wdspxe-pxepacketfree) .

## <a name="enumerate-registered-providers"></a>Enumerar provedores registrados

-   Use a API para gravar provedores que enumerem e verifiquem outros provedores registrados na lista.
-   A função [**PxeGetServerInfo**](/windows/win32/api/WdsPxe/nf-wdspxe-pxegetserverinfo) retorna informações sobre o servidor PXE. A função **PxeGetServerInfo** retorna um **bool** que indica se o rastreamento está habilitado para o servidor. **Verdadeiro** indica que o rastreamento está habilitado.
-   A função [**PxeProviderEnumFirst**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeproviderenumfirst) inicia um provedor de enumerationof na lista de provedores registrados. A função **PxeProviderEnumFirst** inicia a enumeração e retorna o endereço do identificador que deve ser usado ao chamar a função [**PxeProviderEnumNext**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeproviderenumnext) . A função **PxeProviderEnumNext** retorna uma estrutura de [**\_ provedor PXE**](/windows/win32/api/wdspxe/ns-wdspxe-pxe_provider) que contém as informações sobre o provedor. A função [**PxeProviderFreeInfo**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeproviderfreeinfo) libera a memória que foi alocada para a estrutura **do \_ provedor PXE** pela função **PxeProviderEnumNext** . A função [**PxeProviderEnumClose**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeproviderenumclose) fecha a enumeração de provedores na lista de provedores registrados.

## <a name="handle-service-control-codes"></a>Manipular códigos de controle de serviço

-   Quando uma mensagem de controle de serviço é recebida, o WDS chama o retorno de chamada [*PxeProviderServiceControl*](pxeproviderservicecontrol.md) .
-   O provedor pode definir uma função de retorno de chamada [*PxeProviderServiceControl*](pxeproviderservicecontrol.md) para manipular mensagens de controle de serviço.
-   Registre o retorno de chamada [*PxeProviderServiceControl*](pxeproviderservicecontrol.md) chamando a função [**PxeRegisterCallback**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeregistercallback) com o controle de **serviço de retorno de \_ chamada \_ \_ PXE** durante o processamento do retorno de chamada [*PxeProviderInitialize*](pxeproviderinitialize.md) .

## <a name="add-trace-entries-to-pxe-log"></a>Adicionar entradas de rastreamento ao log PXE

-   A função [**PxeTrace**](/windows/win32/api/WdsPxe/nf-wdspxe-pxetrace) adiciona uma entrada de rastreamento ao log PXE. O WDSPXE fornece rastreamento para ajudar os administradores na solução de problemas. Os provedores podem registrar entradas de rastreamento de diferentes níveis de severidade. Os administradores podem configurar o WDSPXE para registrar somente as entradas para determinados níveis de gravidade.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre a API dos serviços de implantação do Windows](about-the-windows-deployment-services-api.md)
</dt> <dt>

[Uso da API de cliente de Serviços de Implantação do Windows](using-the-windows-deployment-services-client-api.md)
</dt> </dl>

 

 




