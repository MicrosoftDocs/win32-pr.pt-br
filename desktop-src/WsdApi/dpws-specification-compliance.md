---
description: Este tópico descreve como o WSDAPI implementa a funcionalidade eletiva na especificação do DPWS (Perfil de Dispositivos para Serviços Web). Ele também descreve qual funcionalidade do DPWS foi omitida da implementação do WSDAPI.
ms.assetid: 54d51e56-8022-4696-b488-4b3a226224d8
title: Conformidade da especificação do DPWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce59ba29e8e36fd5030732c0b61a2dfd164d9c887bdd9881a775c8b1ce6ec353
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119130819"
---
# <a name="dpws-specification-compliance"></a>Conformidade da especificação do DPWS

Este tópico descreve como o WSDAPI implementa a funcionalidade eletiva na especificação do DPWS (Perfil de Dispositivos para [Serviços Web).](https://specs.xmlsoap.org/ws/2006/02/devprof/) Ele também descreve qual funcionalidade do DPWS foi omitida da implementação do WSDAPI.

A especificação do DPWS fornece uma maneira consistente de enviar mensagens com dispositivos. Ele também adiciona restrições e recomendações específicas que simplificam o processo de suporte a serviços Web em hardware inserido.

A especificação do DPWS descreve a funcionalidade eletiva usando os termos MAY ou SHOULD em uma determinada recomendação ou restrição de implementação. A funcionalidade omitida pode ser a funcionalidade descrita como OBRIGATÓRIO na especificação do DPWS que não foi implementada pelo WSDAPI ou pode ser uma funcionalidade que o WSDAPI implementou em um método outro no especificado na especificação do DPWS.

Este tópico segue o layout da seção DPWS por seção. Cada seção descreve como restrições específicas, requisitos e funcionalidade eletiva são tratados pela implementação do WSDAPI. Este tópico é melhor lido em tandem com a especificação do DPWS.

## <a name="dpws-30-messaging"></a>Mensagens do DPWS 3.0

### <a name="dpws-31-uri-formats"></a>Formatos de URI do DPWS 3.1

Restrições R0025 e R0027 restringem URIs a \_ octetos MAX URI \_ SIZE. O WSDAPI impõe essas duas restrições conforme especificado.

### <a name="dpws-32-udp-messaging"></a>Mensagens UDP do DPWS 3.2

A recomendação R0029 sugere que pacotes UDP maiores que a MTU (unidade de transferência máxima) para UDP não devem ser enviados. O WSDAPI não implementa essa recomendação e permitirá que as implementações enviem e recebam mensagens de descoberta maiores do que a MTU.

### <a name="dpws-33-http-messaging"></a>Mensagens HTTP do DPWS 3.3

R0001 exige que os serviços deem suporte à transferência em partes. O WSDAPI aceita dados em partes em mensagens de solicitação e enviará dados em partes em mensagens de solicitação.

R0012 e R0013 descrevem as partes necessárias da associação HTTP SOAP. Para R0012, o WSDAPI implementa a associação HTTP SOAP, mas não começará a ler a resposta HTTP até que o WSDAPI tenha terminado de enviar a solicitação HTTP. O WSDAPI implementa o padrão de troca de mensagens necessário em R0013, implementa o nó SOAP de resposta opcional em R0014 e não implementa o recurso de método Web opcional em R0015. O WSDAPI também dá suporte aos requisitos em R0030 e R0017.

### <a name="dpws-34-soap-envelope"></a>DPWS 3.4 SOAP Envelope

O WSDAPI dá suporte a R0034 e impõe R0003 e R0026 por padrão. Mais especificamente, de acordo com R0003 e R0026, se o WSDAPI receber um envelope SOAP maior que MAX ENVELOPE SIZE sobre HTTP, ele será rejeitado e a conexão será \_ \_ fechada.

### <a name="dpws-35-ws-addressing"></a>DPWS 3.5 WS-Addressing

R0004 reflete o uso recomendado da API do dispositivo no WSDAPI e tem suporte da API do cliente no WSDAPI. Como essa é uma recomendação, o WSDAPI permitirá que clientes e dispositivos usem URIs diferentes de URIs para seus pontos de extremidade de dispositivo para garantir a `urn:uuid` máxima compatibilidade. Como a API do dispositivo no WSDAPI não persiste o estado entre inicializações, é responsabilidade dos desenvolvedores de aplicativos usar a API do dispositivo no WSDAPI para garantir que R0005 e R0006 sejam adequadamente suportados. A API do cliente no WSDAPI assumirá que as identidades de dispositivo são exclusivas e persistentes, e a funcionalidade que se baseia na API do cliente no WSDAPI (como PnP-X) exigirá isso para reconhecer corretamente o dispositivo nas reinicializações do dispositivo.

R0007 recomenda o uso de propriedades de referência em referências de ponto de extremidade. O WSDAPI ainda reconhecerá e aceitará pontos de extremidade com propriedades de referência, e os desenvolvedores podem optar por usá-los, mas, por padrão, o WSDAPI não os preencherá nos pontos de extremidade que cria. Da mesma forma, com R0042, quando o WSDAPI cria pontos de extremidade de serviço, ele usará um endereço de transporte HTTP ou HTTPS, mas não exigirá que os dispositivos usem endereços de transporte HTTP ou HTTPS em seus pontos de extremidade de serviço. O comportamento do cliente ao tentar se comunicar com um serviço que não usa HTTP ou HTTPS é indefinido.

Em caso de falhas, R0031 restringe o ponto de extremidade de resposta e descreve a falha a ser enviada se a falha não for anônima. O WSDAPI força o ponto de extremidade de resposta a usar o valor correto ao enviar mensagens e falha corretamente se o WSDAPI receber uma mensagem de solicitação com o ponto de extremidade de resposta incorreto. R0041 oferece às implementações a opção de soltar uma falha se o ponto de extremidade de resposta for inválido. Em vez de soltar a falha, o WSDAPI enviará a falha de volta no canal de solicitação, endereçado ao ponto de extremidade anônimo, como um "melhor esforço" para se comunicar com o cliente.

Por fim, há duas restrições nos títulos SOAP, R0019 e R0040, ambas as quais o WSDAPI está em conformidade com e impõe as mensagens recebidas.

### <a name="dpws-36-attachments"></a>Anexos DPWS 3.6

O WSDAPI dá suporte a anexos e está em conformidade com R0022. O WSDAPI também está em conformidade com R0037. Ao enviar anexos, o WSDAPI sempre definirá a Codificação de Transferência de Conteúdo como "binária" para todas as partes mime. No entanto, o WSDAPI não impõe R0036. O comportamento do WSDAPI ao receber uma parte MIME com uma Codificação de Transferência de Conteúdo não definida como "binário" é indefinido.

O DPWS também define cláusulas de ordenação de partes mime. Para R0038, o WSDAPI imporá a ordenação de parte e rejeitará uma mensagem MIME se o envelope SOAP não for a primeira parte MIME. Para R0039, o WSDAPI sempre enviará o envelope SOAP como a primeira parte mime.

## <a name="dpws-40-discovery"></a>Descoberta do DPWS 4.0

R1013 e R1001 diferenciam a descoberta de dispositivos e a descoberta de serviço. O WSDAPI está em conformidade com R1013. A implementação de hospedagem está em conformidade com R1001, mas o WSDAPI não impõe essa recomendação ao cliente.

O DPWS também fornece diretrizes sobre tipos e regras de correspondência de escopo. O WSDAPI dá suporte a todas as regras de correspondência de escopo [definidas no WS-Discovery,](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf) exceto LDAP. O WSDAPI também fornece um modelo extensível para definir regras de correspondência de escopo personalizadas, de acordo com o R1019. A API de hospedagem também sempre fornecerá o tipo na descoberta por R1020, mas a API do cliente não `wsdp:Device` exige que ela está presente. Outros aplicativos com base no WSDAPI, como PnP-X, têm um requisito rígido para o tipo estar `wsdp:Device` presente na descoberta.

Para facilitar a descoberta e a associação, o WSDAPI dá suporte a R1009 e R1016. Por R1018, o WSDAPI ignorará o UDP multicast não enviado para o endereço anônimo. R1015, R1021 e R1022 definem uma associação HTTP para a mensagem Probe, à qual o WSDAPI dá suporte conforme descrito.

## <a name="dpws-50-description"></a>Descrição do DPWS 5.0

O WSDAPI impõe R2044 no cliente. No lado da hospedagem, o WSDAPI só fornecerá o `wsx:Metadata` elemento no corpo do envelope SOAP. O R2045 permite que os dispositivos deem suporte a um subconjunto da [funcionalidade WS-Transfer.](https://specs.xmlsoap.org/ws/2004/09/transfer/WS-Transfer.pdf) A API de hospedagem sempre gerará a `wsa:ActionNotSupported` falha.

### <a name="dpws-51-characteristics"></a>Características do DPWS 5.1

O DPWS descreve as características básicas do dispositivo. Além das restrições descritas neste tópico, os limites de comprimento são definidos para cadeias de caracteres e URIs específicos. O WSDAPI impõe os limites de comprimento nesta seção 5.1 do DPWS, antes de enviar a mensagem ou depois de analisar seu conteúdo.

O DPWS também descreve as seções de metadados necessárias e o ciclo da versão de metadados. A implementação do cliente impõe a presença de metadados ThisModel e ThisDevice. A implementação de hospedagem também gerencia corretamente a versão de metadados e sempre fornece essas seções, em conformidade com R2038, R2012, R2001, R2039, R2014 e R2002.

### <a name="dpws-52-hosting"></a>Hospedagem do DPWS 5.2

Esta seção descreve a hierarquia de serviços e metadados de relação. O WSDAPI não impõe a exclusividade da ServiceId, conforme descrito nesta seção no lado do cliente ou do dispositivo.

O WSDAPI está em conformidade com o R2040 e é possível que a implementação de hospedagem envie uma resposta de metadados sem nenhuma seção de relação se não houver serviços hospedados. A implementação do cliente aceita corretamente a resposta de metadados.

O R2029 permite várias seções de relação em uma resposta de metadados, que o WSDAPI aceitará corretamente. R2030 e R2042 descrevem o gerenciamento da versão de metadados, que é implementada corretamente na API de hospedagem.

### <a name="dpws-53-wsdl"></a>DPWS 5.3 WSDL

Se um serviço fornece dados WSDL (Linguagem de Descrição dos Serviços Web), as implementações do cliente podem obter a definição do serviço e manipular o serviço em tempo real. Isso é usado por clientes com limite tardia. A implementação do cliente WSDAPI aceitará o WSDL fornecido de um serviço, mas o cliente não o valida e o cliente não fornece um modelo de programação com limite tardia. A implementação de hospedagem pode ser usada para fornecer WSDL, mas o host não precisa fazer isso, pois os metadados de nível de serviço não são gerenciados pelo próprio host.

### <a name="dpws-54-ws-policy"></a>DPWS 5.4 WS-Policy

O DPWS descreve as declarações de política a serem usadas para dispositivos. Como o WSDAPI não fornece e não interpreta o WSDL, ele não pode reconhecer e impor a política inserida em dados WSDL.

## <a name="dpws-60-eventing"></a>Evento DPWS 6.0

### <a name="dpws-61-subscription"></a>Assinatura do DPWS 6.1

O DPWS requer suporte para entrega por push. O WSDAPI implementa a entrega por push no lado do serviço, em conformidade com R3009 e R3010 e aceitará apenas o modo de entrega por push no lado do cliente. R3017 e R3018 exigirão falhas específicas do serviço se ele não reconhecer os `NotifyTo` `EndTo` endereços ou . O WSDAPI não valida esses endereços antecipadamente e não gerará essas falhas. No entanto, a implementação do cliente reconhecerá essas falhas corretamente. Da mesma forma, O R3019 é opcional e o WSDAPI não implementa essa recomendação, mas a implementação do cliente reconhecerá corretamente a mensagem e notificará a aplicação de uma falha `SubscriptionEnd` de entrega.

### <a name="dpws-611-filtering"></a>Filtragem do DPWS 6.1.1

O WSDAPI está em conformidade com R3008 e implementa o `Action` filtro. Em conformidade com R3011 e R3012, o WSDAPI não gerará as falhas nas condições declarados. O WSDAPI também implementa a falha descrita em R3020 se não reconhecer as ações nas quais é solicitado a filtrar.

### <a name="dpws-62-subscription-duration-and-renewal"></a>Duração e renovação da assinatura do DPWS 6.2

O WSDAPI está em conformidade com R3005, R3006 e R3016. O WSDAPI sempre usará, mas aceitará se fornecido e, portanto, não emitirá a falha `xs:duration` `xs:dateTime` opcional no R3013. O WSDAPI dá `GetStatus` suporte e não emitirá a falha por `wsa:ActionNotSupported` R3015. O WSDAPI aceitará `wsa:ActionNotSupported` a falha se um serviço responder a uma `GetStatus` solicitação com ele.

## <a name="dpws-70-security"></a>Segurança do DPWS 7.0

O DPWS descreve um modelo de segurança recomendado para dispositivos. O WSDAPI não implementa essas recomendações conforme descrito e não impõe as restrições nesta seção, conforme descrito.

## <a name="dpws-appendix-i"></a>Apêndice I do DPWS

O DPWS corrigi as constantes globais de outras especificações para atender aos dispositivos. O WSDAPI usa as constantes desta seção e substitui as constantes padrão na implementação [do WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf) por essas constantes. Os aplicativos que usam o WSDAPI para WS-Discovery serão vinculados às constantes definidas no DPWS, não às constantes definidas no [WS-Discovery.](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf)

 

 



