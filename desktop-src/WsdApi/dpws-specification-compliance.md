---
description: Este tópico descreve como o WSDAPI implementa a funcionalidade facultativos na especificação do perfil de dispositivos para DPWS (serviços Web). Ele também descreve qual funcionalidade de DPWS foi omitida da implementação de WSDAPI.
ms.assetid: 54d51e56-8022-4696-b488-4b3a226224d8
title: Conformidade de especificação do DPWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ed26e57a0f7a94069e802f96f346a3a5eca67b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105813339"
---
# <a name="dpws-specification-compliance"></a>Conformidade de especificação do DPWS

Este tópico descreve como o WSDAPI implementa a funcionalidade facultativos na especificação do [perfil de dispositivos para DPWS (serviços Web](https://specs.xmlsoap.org/ws/2006/02/devprof/) ). Ele também descreve qual funcionalidade de DPWS foi omitida da implementação de WSDAPI.

A especificação DPWS fornece uma maneira consistente de mensagens com dispositivos. Ele também adiciona restrições específicas e recomendações que simplificam o processo de suporte a serviços da Web em hardware inserido.

A especificação DPWS descreve a funcionalidade facultativos usando os termos podem ou deve estar em uma determinada recomendação ou restrição de implementação. A funcionalidade omitida pode ser a funcionalidade descrita conforme necessário na especificação DPWS que não foi implementada pelo WSDAPI ou pode ser a funcionalidade que o WSDAPI implementou em um método diferente do especificado na especificação DPWS.

Este tópico segue o layout da seção DPWS por seção. Cada seção descreve como as restrições específicas, os requisitos e a funcionalidade facultativos são tratados pela implementação do WSDAPI. Este tópico é melhor lido em conjunto com a especificação DPWS.

## <a name="dpws-30-messaging"></a>Mensagens do DPWS 3,0

### <a name="dpws-31-uri-formats"></a>Formatos de URI DPWS 3,1

As restrições R0025 e R0027 restringem URIs a \_ octetos de tamanho máximo de URI \_ . O WSDAPI impõe essas duas restrições conforme especificado.

### <a name="dpws-32-udp-messaging"></a>Mensagens UDP do DPWS 3,2

A recomendação R0029 sugere que os pacotes UDP maiores que a MTU (unidade máxima de transferência) para UDP não devem ser enviados. O WSDAPI não implementa essa recomendação e permitirá que as implementações enviem e recebam mensagens de descoberta maiores do que a MTU.

### <a name="dpws-33-http-messaging"></a>Mensagens HTTP do DPWS 3,3

O R0001 requer que os serviços ofereçam suporte à transferência em partes. O WSDAPI aceita dados em bloco em mensagens de solicitação e enviará dados em partes em mensagens de solicitação.

R0012 e R0013 descrevem as partes necessárias da associação HTTP SOAP. Para R0012, o WSDAPI implementa a associação HTTP SOAP, mas não começará a ler a resposta HTTP até que o WSDAPI termine de enviar a solicitação HTTP. O WSDAPI implementa o padrão de troca de mensagens necessário no R0013, implementa o nó SOAP de resposta opcional em R0014 e não implementa o recurso de método Web opcional no R0015. O WSDAPI também dá suporte aos requisitos em R0030 e R0017.

### <a name="dpws-34-soap-envelope"></a>Envelope SOAP DPWS 3,4

O WSDAPI dá suporte a R0034 e impõe R0003 e R0026 por padrão. Mais especificamente, de acordo com R0003 e R0026, se WSDAPI receber um envelope SOAP maior do que \_ o tamanho máximo do envelope \_ sobre http, ele será rejeitado e a conexão será fechada.

### <a name="dpws-35-ws-addressing"></a>DPWS 3,5 WS-Addressing

R0004 reflete o uso recomendado da API do dispositivo em WSDAPI e é compatível com a API do cliente em WSDAPI. Como essa é uma recomendação, o WSDAPI permitirá que clientes e dispositivos usem URIs diferentes de `urn:uuid` URIs para seus pontos de extremidade de dispositivo para garantir a compatibilidade máxima. Como a API do dispositivo no WSDAPI não mantém o estado entre as inicializações, cabe a desenvolvedores de aplicativos usando a API do dispositivo em WSDAPI para garantir que R0005 e R0006 tenham suporte adequado. A API do cliente no WSDAPI assumirá que as identidades do dispositivo são exclusivas e persistentes, e a criação de funcionalidades na API do cliente em WSDAPI (como PnP-X) exigirá isso para reconhecer corretamente o dispositivo entre as reinicializações do dispositivo.

R0007 recomenda o uso de propriedades de referência em referências de ponto de extremidade. O WSDAPI ainda reconhecerá e aceitará pontos de extremidade com propriedades de referência, e os desenvolvedores poderão optar por usá-los, mas, por padrão, o WSDAPI não os preencherá em pontos de extremidade criados por ele. Da mesma forma, com R0042, quando o WSDAPI cria pontos de extremidade de serviço, ele usará um endereço de transporte HTTP ou HTTPS, mas não exigirá que os dispositivos usem endereços de transporte HTTP ou HTTPS em seus pontos de extremidade de serviço. O comportamento do cliente ao tentar se comunicar com um serviço que não usa HTTP ou HTTPS é indefinido.

Em caso de falhas, o R0031 restringe o ponto de extremidade de resposta e descreve a falha a ser enviada se a falha não for anônima. O WSDAPI força o ponto de extremidade de resposta a usar o valor correto ao enviar mensagens e haverá falha corretamente se o WSDAPI receber uma mensagem de solicitação com o ponto de extremidade de resposta incorreto. R0041 dá às implementações a opção de remover uma falha se o ponto de extremidade de resposta for inválido. Em vez de descartar a falha, o WSDAPI enviará a falha de volta ao canal de solicitação, endereçado ao ponto de extremidade anônimo, como um "melhor esforço" para se comunicar com o cliente.

Por fim, há duas restrições em cabeçalhos SOAP, R0019 e R0040, ambas em que o WSDAPI está em conformidade com e se aplica às mensagens recebidas.

### <a name="dpws-36-attachments"></a>Anexos do DPWS 3,6

O WSDAPI dá suporte a anexos e está em conformidade com o R0022. O WSDAPI também está em conformidade com o R0037. Ao enviar anexos, o WSDAPI sempre definirá a codificação de transferência de conteúdo como "binary" para todas as partes MIME. No entanto, o WSDAPI não impõe R0036. O comportamento de WSDAPI ao receber uma parte MIME com uma codificação de transferência de conteúdo não definida como "binary" é indefinido.

DPWS também define cláusulas de ordenação de parte MIME. Para R0038, o WSDAPI irá impor a ordenação de parte e rejeitará uma mensagem MIME se o envelope SOAP não for a primeira parte MIME. Para R0039, o WSDAPI sempre enviará o envelope SOAP como a primeira parte MIME.

## <a name="dpws-40-discovery"></a>Descoberta do DPWS 4,0

R1013 e R1001 diferenciam a descoberta de dispositivos e a descoberta de serviços. O WSDAPI está em conformidade com o R1013. A implementação de hospedagem está em conformidade com o R1001, mas o WSDAPI não impõe essa recomendação no cliente.

O DPWS também fornece diretrizes sobre tipos e regras de correspondência de escopo. O WSDAPI dá suporte a todas as regras de correspondência de escopo definidas no [WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf) , exceto LDAP. O WSDAPI também fornece um modelo extensível para definir regras de correspondência de escopo personalizadas, o que está em conformidade com o R1019. A API de hospedagem também fornecerá sempre o `wsdp:Device` tipo na descoberta por R1020, mas a API do cliente não precisa estar presente. Outros aplicativos criados em WSDAPI, como PnP-X, têm um requisito rígido para que o `wsdp:Device` tipo esteja presente na descoberta.

Para facilitar a descoberta e a associação, o WSDAPI dá suporte a R1009 e R1016. Por R1018, o WSDAPI ignorará o UDP Multicast não enviado para o endereço anônimo. R1015, R1021 e R1022 definem uma associação HTTP para a mensagem de investigação, que o WSDAPI dá suporte conforme descrito.

## <a name="dpws-50-description"></a>Descrição do DPWS 5,0

O WSDAPI impõe R2044 no cliente. No lado da hospedagem, o WSDAPI sempre fornecerá o `wsx:Metadata` elemento no corpo do envelope SOAP. O R2045 permite que os dispositivos ofereçam suporte a um subconjunto da funcionalidade [WS-Transfer](https://specs.xmlsoap.org/ws/2004/09/transfer/WS-Transfer.pdf) . A API de hospedagem sempre gerará a `wsa:ActionNotSupported` falha.

### <a name="dpws-51-characteristics"></a>Características do DPWS 5,1

DPWS descreve as características básicas para o dispositivo. Além das restrições descritas neste tópico, os limites de comprimento são definidos para cadeias de caracteres e URIs específicos. O WSDAPI impõe os limites de comprimento nesta seção de DPWS 5,1, antes de enviar a mensagem ou depois de analisar seu conteúdo.

DPWS também descreve as seções de metadados necessárias e o ciclo da versão de metadados. A implementação do cliente impõe a presença de metadados ThisModel e ThisDevice. A implementação de hospedagem também gerencia corretamente a versão de metadados e sempre fornece essas seções, conformidade com R2038, R2012, R2001, R2039, R2014 e R2002.

### <a name="dpws-52-hosting"></a>Hospedagem do DPWS 5,2

Esta seção descreve a hierarquia de serviços e metadados de relação. O WSDAPI não impõe a exclusividade da ServiceId conforme descrito nesta seção no cliente ou no lado do dispositivo.

O WSDAPI está em conformidade com R2040, e é possível que a implementação de hospedagem envie uma resposta de metadados sem nenhuma seção de relação se não houver serviços hospedados. A implementação do cliente aceita corretamente a resposta de metadados.

O R2029 permite várias seções de relação em uma resposta de metadados, que o WSDAPI aceitará corretamente. R2030 e R2042 descrevem o gerenciamento da versão de metadados, que é implementada corretamente na API de hospedagem.

### <a name="dpws-53-wsdl"></a>DPWS 5,3 WSDL

Se um serviço fornecer dados WSDL (Web Services Description Language), as implementações de cliente poderão obter a definição de serviço e manipular o serviço em tempo real. Isso é usado por clientes com associação tardia. A implementação do cliente WSDAPI aceitará o WSDL fornecido de um serviço, mas o cliente não o validará e o cliente não fornecerá um modelo de programação de associação tardia. A implementação de hospedagem pode ser usada para fornecer o WSDL, mas não é necessário que o host faça isso, pois os metadados de nível de serviço não são gerenciados pelo próprio host.

### <a name="dpws-54-ws-policy"></a>DPWS 5,4 WS-Policy

DPWS descreve as declarações de política a serem usadas para dispositivos. Como o WSDAPI não fornece e não interpreta o WSDL, ele não pode reconhecer e impor a política inserida em dados WSDL.

## <a name="dpws-60-eventing"></a>Eventos do DPWS 6,0

### <a name="dpws-61-subscription"></a>Assinatura do DPWS 6,1

O DPWS requer suporte para entrega por push. O WSDAPI implementa a entrega por push no lado do serviço, assim como está em conformidade com R3009 e R3010, e só aceitará o modo de entrega por push no lado do cliente. R3017 e R3018 exigem falhas específicas do serviço se ele não reconhece os `NotifyTo` `EndTo` endereços ou. O WSDAPI não valida esses endereços antecipadamente e não irá gerar essas falhas. No entanto, a implementação do cliente reconhecerá essas falhas corretamente. Da mesma forma, R3019 é opcional e o WSDAPI não implementa essa recomendação, mas a implementação do cliente reconhecerá corretamente a `SubscriptionEnd` mensagem e notificará a aplicação de uma falha de entrega.

### <a name="dpws-611-filtering"></a>Filtragem DPWS 6.1.1

O WSDAPI está em conformidade com o R3008 e implementa o `Action` filtro. Em conformidade com R3011 e R3012, o WSDAPI não gerará as falhas nas condições declaradas. O WSDAPI também implementa a falha descrita R3020 se não reconhecer as ações nas quais é solicitado a filtrar.

### <a name="dpws-62-subscription-duration-and-renewal"></a>Duração e renovação da assinatura do DPWS 6,2

O WSDAPI está em conformidade com R3005, R3006 e R3016. O WSDAPI sempre usará, `xs:duration` mas aceitará `xs:dateTime` se fornecido e, portanto, não emitirá a falha opcional em R3013. O WSDAPI dá suporte `GetStatus` e não emitirá a `wsa:ActionNotSupported` falha por R3015. O WSDAPI aceitará a `wsa:ActionNotSupported` falha se um serviço responder a uma `GetStatus` solicitação com ela.

## <a name="dpws-70-security"></a>Segurança do DPWS 7,0

DPWS descreve um modelo de segurança recomendado para dispositivos. O WSDAPI não implementa essas recomendações conforme descrito e não impõe as restrições nesta seção, conforme descrito.

## <a name="dpws-appendix-i"></a>DPWS apêndice I

O DPWS corrigi constantes globais de outras especificações para atender aos dispositivos. O WSDAPI usa as constantes desta seção e substitui as constantes padrão na implementação de [WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf) por essas constantes. Os aplicativos que usam WSDAPI para WS-Discovery serão associados às constantes definidas em DPWS, não às constantes definidas em [WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf).

 

 



