---
title: Bluetooth e opções de soquete
description: Bluetooth para Windows dá suporte às seguintes opções de soquete.
ms.assetid: e2e305c2-e749-4566-8e24-c07a7a29c612
keywords:
- Bluetooth opções de soquete e Bluetooth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 631eb2b041fcc320723155d4a5df1742e6c0dc79cb579815de141334906708e9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119588426"
---
# <a name="bluetooth-and-socket-options"></a>Bluetooth e opções de soquete

Bluetooth para Windows dá suporte às seguintes opções de soquete. As opções de soquete são definidas e consultadas usando as funções [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) e [**getsockopt,**](/windows/desktop/api/winsock/nf-winsock-getsockopt) respectivamente. Todas as opções a seguir podem ser usadas com a função **setsockopt,** mas apenas a opção **SO \_ BTH \_ MTU** está disponível para uso com a **função getsockopt.**

As seguintes configurações são necessárias para trabalhar com Bluetooth de soquete:

-   O *parâmetro s* deve ser um Bluetooth soquete.
-   O *parâmetro de* nível deve ser **\_ RFCOMM do SOL.**

## <a name="so_bth_authenticate"></a>PORTANTO, \_ A BTH \_ AUTHENTICATE

Para soquetes desconectados, **o SO \_ BTH \_ AUTHENTICATE** especifica que [](/windows/desktop/api/winsock2/nf-winsock2-accept) [**a**](/windows/desktop/api/winsock2/nf-winsock2-connect) autenticação é necessária para que uma operação de conexão ou aceitação seja concluída com êxito. Definir essa opção de soquete iniciará a autenticação ativamente durante o estabelecimento da conexão, se os dois Bluetooth dispositivos não foram autenticados anteriormente. A interface do usuário para troca de chave de acesso, se necessário, é fornecida pelo sistema operacional fora do contexto do aplicativo.

Para conexões de saída que exigem autenticação, a operação [**de**](/windows/desktop/api/winsock2/nf-winsock2-connect) conexão falhará com **WSAEACCES** se a autenticação não for bem-sucedida. Em resposta, o aplicativo pode solicitar que o usuário autenture os dois Bluetooth antes da conexão.

Para conexões de entrada, a conexão será rejeitada se a autenticação não puder ser estabelecida e retornar um **erro WSAEHOSTDOWN.** Para obter mais informações sobre como autenticar Bluetooth dispositivos, consulte [**BluetoothAuthenticateDevice**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothauthenticatedevice).

Para a **opção \_ soquete SO BTH \_ AUTHENTICATE,** *optval* é um ponteiro para ULONG bAuthenticate e deve ser **TRUE**; *optlen* é equivalente a "sizeof(ULONG)".

**Windows XP com SP2: SO \_ O BTH \_ AUTHENTICATE** inicia a autenticação para soquetes conectados e força a autenticação após a conexão para soquetes não conectados. Para conexões de entrada, a conexão será rejeitada se a autenticação não puder ser executada.

## <a name="so_bth_encrypt"></a>PORTANTO, \_ CRIPTOGRAFAR \_ BTH

Em soquetes não conectados, a **opção soquete SO \_ BTH \_ ENCRYPT** impõe criptografia para estabelecer uma conexão. A criptografia só está disponível para conexões autenticadas. Para conexões de entrada, uma conexão para a qual a criptografia não pode ser estabelecida é rejeitada automaticamente e retorna **WSAEHOSTDOWN** como o erro. Para conexões de saída, a [**função connect**](/windows/desktop/api/winsock2/nf-winsock2-connect) falhará **com WSAEACCES** se a criptografia não puder ser estabelecida. Em resposta, o aplicativo pode solicitar que o usuário autenture os dois Bluetooth antes da conexão. Para obter mais informações sobre como autenticar Bluetooth dispositivos, consulte [**BluetoothAuthenticateDevice**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothauthenticatedevice).

Para a opção \_ soquete SO BTH \_ ENCRYPT, *optval* é um ponteiro para ULONG **bEncrypt** e deve ser **TRUE**; *optlen* é equivalente a sizeof(ULONG).

**Windows XP com SP2:** Para um soquete conectado e autenticado, **SO \_ BTH \_ ENCRYPT inicia** a criptografia.

## <a name="so_bth_mtu"></a>SO \_ BTH \_ MTU

A **opção \_ soquete SO BTH \_ MTU** é uma opção avançada usada principalmente para validação. A **opção \_ SO BTH \_ MTU** obtém ou define mtu rfCOMM padrão (unidade de transmissão máxima) para negociação de conexão com um valor diferente do valor padrão do protocolo RFCOMM.

Como a MTU RFCOMM é afetada pela MTU L2CAP subjacente e pelos mínimos e máximos do protocolo e do aplicativo, o valor padrão para **SO \_ BTH \_ MTU** é apenas um ponto de partida para negociação com o par remoto e a MTU negociada final provavelmente variará do padrão. Definir o **valor \_ de \_ MTU so BTH** pode afetar negativamente a produtividade e, como tal, qualquer modificação deve ser executada com conhecimento do protocolo Bluetooth subjacente.

A **opção \_ soquete SO BTH \_ MTU** pode ser executada em soquetes conectados, mas não terá efeito se a negociação já tiver sido concluída. Defini-lo no soquete de escuta (servidor) não tem nenhum efeito.

A quantidade de dados que um aplicativo pode enviar ou receber em uma única chamada de soquete não é afetada pela MTU; A MTU afeta apenas como o provedor de serviços Windows Soquetes subjacente segmenta pacotes para transporte. A MTU proposta e a MTU negociadas devem estar entre **RFCOMM \_ MIN \_ MTU** e **RFCOMM \_ MAX \_ MTU**, conforme definido no arquivo de título Ws2bth.h.

Para a **opção \_ soquete SO BTH \_ MTU,** *optval* é um ponteiro para ULONG mtu; *optlen* é equivalente a "sizeof(ULONG)".

## <a name="so_bth_mtu_max"></a>PORTANTO, \_ BTH \_ MTU \_ MAX

A **opção \_ soquete SO BTH \_ MTU \_ MAX** é uma opção avançada usada principalmente para validação. A **opção \_ soquete SO BTH \_ MTU \_ MAX** define o máximo de MTU RFCOMM (unidade de transmissão máxima) para negociação de conexão. As conexões com uma MTU RFCOMM igual ou maior que esse valor falham durante o [**processo de aceitação**](/windows/desktop/api/winsock2/nf-winsock2-connect) / [**de**](/windows/desktop/api/winsock2/nf-winsock2-accept) conexão. Ao definir essa opção de soquete é permitida para um soquete conectado, ela não terá efeito se a negociação tiver sido concluída. Definir essa opção de soquete em um soquete de escuta propaga o valor para todas as conexões de entrada. O valor max MTU deve estar entre **RFCOMM \_ MIN \_ MTU** e **RFCOMM \_ MAX \_ MTU**, conforme definido no arquivo de título Ws2bth.h.

Para a **opção \_ soquete SO BTH \_ MTU \_ MAX,** *optval* é um ponteiro para ULONG max \_ mtu; *optlen* é equivalente a "sizeof(ULONG)".

## <a name="so_bth_mtu_min"></a>SO \_ BTH \_ MTU \_ MIN

A **opção \_ soquete SO BTH \_ MTU \_ MIN** é uma opção avançada usada principalmente para validação. A **opção \_ soquete SO BTH \_ MTU \_ MIN** define o mínimo de MTU RFCOMM (unidade de transmissão máxima) para negociação de conexão. As conexões com uma MTU RFCOMM menor que esse valor falham durante o [**processo de aceitação**](/windows/desktop/api/winsock2/nf-winsock2-connect) / [**de**](/windows/desktop/api/winsock2/nf-winsock2-accept) conexão. Ao definir essa opção de soquete é permitida para um soquete conectado, ela não terá efeito se a negociação tiver sido concluída. Definir essa opção de soquete em um soquete de escuta propaga o valor para todas as conexões de entrada.

Somente um soquete de escuta pode revisar a MTU para baixo, portanto, se o valor proposto pelo soquete de conexão for menor que o valor definido para **SO \_ BTH \_ MTU \_ MIN** no soquete de escuta, a conexão será recusada. A MTU mínima deve estar entre **RFCOMM \_ MIN \_ MTU** e **RFCOMM \_ MAX \_ MTU**, conforme definido no arquivo de título Ws2bth.h.

Para a opção \_ soquete SO BTH \_ MTU \_ MIN, *optval* é um ponteiro para ULONG min \_ mtu; *optlen* é equivalente a "sizeof(ULONG)".

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[**Getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt)
</dt> <dt>

[**Setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt)
</dt> <dt>

[**BluetoothAuthenticateDevice**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothauthenticatedevice)
</dt> <dt>

[**Conectar**](/windows/desktop/api/winsock2/nf-winsock2-connect)
</dt> <dt>

[**Aceitar**](/windows/desktop/api/winsock2/nf-winsock2-accept)
</dt> </dl>

 

 