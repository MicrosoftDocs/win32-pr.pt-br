---
title: Opções de Bluetooth e soquete
description: O Bluetooth para Windows dá suporte às seguintes opções de soquete.
ms.assetid: e2e305c2-e749-4566-8e24-c07a7a29c612
keywords:
- Opções de Bluetooth e soquete Bluetooth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84040a98c3dae1fec292e4f0a7086f11d1ee546c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917393"
---
# <a name="bluetooth-and-socket-options"></a>Opções de Bluetooth e soquete

O Bluetooth para Windows dá suporte às seguintes opções de soquete. As opções de soquete são definidas e consultadas usando as funções [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) e [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) , respectivamente. Todas as opções a seguir podem ser usadas com a função **setsockopt** , mas somente a **opção \_ BTH \_ MTU** está disponível para uso com a função **getsockopt** .

As configurações a seguir são necessárias para trabalhar com opções de soquete Bluetooth:

-   O parâmetro *s* deve ser um soquete Bluetooth.
-   O parâmetro *Level* deve ser **sol \_ RFCOMM**.

## <a name="so_bth_authenticate"></a>Portanto, \_ BTH \_ autenticar

Para os soquetes desconectados, a **\_ BTH \_ autenticar** especifica que a autenticação é necessária para que uma operação de [**conexão**](/windows/desktop/api/winsock2/nf-winsock2-connect) ou [**aceitação**](/windows/desktop/api/winsock2/nf-winsock2-accept) seja concluída com êxito. A definição dessa opção de soquete inicia ativamente a autenticação durante o estabelecimento da conexão, se os dois dispositivos Bluetooth não tiverem sido autenticados anteriormente. A interface do usuário para troca de chaves de acesso, se necessário, é fornecida pelo sistema operacional fora do contexto do aplicativo.

Para conexões de saída que exigem autenticação, a operação de [**conexão**](/windows/desktop/api/winsock2/nf-winsock2-connect) falha com **WSAEACCES** se a autenticação não for bem-sucedida. Em resposta, o aplicativo pode solicitar que o usuário autentique os dois dispositivos Bluetooth antes da conexão.

Para conexões de entrada, a conexão será rejeitada se a autenticação não puder ser estabelecida e retornar um erro **WSAEHOSTDOWN** . Para obter mais informações sobre como autenticar dispositivos Bluetooth, consulte [**BluetoothAuthenticateDevice**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothauthenticatedevice).

Para a **opção \_ BTH \_ Authenticate** Socket, *optval* é um ponteiro para o ULONG bAuthenticate e deve ser **true**; *optlen* é equivalente a "sizeof (ULong)".

**Windows XP com SP2: portanto \_ O BTH \_ Authenticate** inicia a autenticação para soquetes conectados e força a autenticação durante a conexão para soquetes não conectados. Para conexões de entrada, a conexão será rejeitada se a autenticação não puder ser executada.

## <a name="so_bth_encrypt"></a>\_BTH \_ criptografar

Em soquetes não conectados, a opção **\_ BTH \_ Encrypt** Socket impõe a criptografia para estabelecer uma conexão. A criptografia só está disponível para conexões autenticadas. Para conexões de entrada, uma conexão para a qual a criptografia não pode ser estabelecida é rejeitada automaticamente e retorna **WSAEHOSTDOWN** como o erro. Para conexões de saída, a função [**Connect**](/windows/desktop/api/winsock2/nf-winsock2-connect) falha com **WSAEACCES** se a criptografia não puder ser estabelecida. Em resposta, o aplicativo pode solicitar que o usuário autentique os dois dispositivos Bluetooth antes da conexão. Para obter mais informações sobre como autenticar dispositivos Bluetooth, consulte [**BluetoothAuthenticateDevice**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothauthenticatedevice).

Para a \_ opção BTH \_ Encrypt Socket, *optval* é um ponteiro para ULONG **bEncrypt** e deve ser **true**; *optlen* é equivalente a sizeof (ULong).

**Windows XP com SP2:** Para um soquete que está conectado e autenticado, **portanto, \_ BTH \_ criptografar** inicia a criptografia.

## <a name="so_bth_mtu"></a>\_BTH \_ MTU

A opção de soquete **\_ BTH \_ MTU** é uma opção avançada usada principalmente para validação. A **opção \_ BTH \_ MTU** Obtém ou define a MTU RFCOMM padrão (unidade de transmissão máxima) para negociação de conexão com um valor diferente do valor padrão do protocolo RFCOMM.

Como o RFCOMM MTU é afetado pelo MTU L2CAP subjacente e pelos mínimos e máximos de protocolo e de aplicativo, o valor padrão para o **\_ \_ MTU de BTH** é apenas um ponto de partida para a negociação com o par remoto, e o MTU negociado final provavelmente vai variar do padrão. Definir o valor de **\_ \_ MTU BTH** pode afetar negativamente a taxa de transferência e, dessa forma, qualquer modificação deve ser executada com o conhecimento do protocolo Bluetooth subjacente.

A opção Soquete de **\_ \_ MTU de BTH** pode ser executada em soquetes conectados, mas não tem efeito se a negociação já tiver sido concluída. Configurá-lo no soquete de escuta (servidor) não tem nenhum efeito.

A quantidade de dados que um aplicativo pode enviar ou receber em uma única chamada de soquete não é afetada pelo MTU; O MTU afeta apenas como o provedor de serviço Windows Sockets subjacente segmenta pacotes para transporte. O MTU proposto e o MTU, por fim, negociados devem estar entre **RFCOMM \_ min \_ MTU** e **RFCOMM \_ Max \_ MTU**, conforme definido no arquivo de cabeçalho Ws2bth. h.

Para a opção de soquete **\_ BTH \_ MTU** , *optval* é um ponteiro para MTU de ULong; *optlen* é equivalente a "sizeof (ULong)".

## <a name="so_bth_mtu_max"></a>Portanto, \_ BTH \_ MTU \_ Max

A opção de soquete **\_ BTH \_ MTU \_ Max** é uma opção avançada usada principalmente para validação. A opção de soquete **\_ BTH \_ MTU \_ Max** define a MTU máxima de RFCOMM (unidade de transmissão máxima) para negociação de conexão. As conexões com um MTU RFCOMM igual ou maior que esse valor falham durante o processo de aceitação de [**conexão**](/windows/desktop/api/winsock2/nf-winsock2-connect) / [](/windows/desktop/api/winsock2/nf-winsock2-accept) . Embora a definição dessa opção de soquete seja permitida para um Soquete conectado, ela não terá efeito se a negociação tiver sido concluída. Definir essa opção de soquete em um soquete de escuta propaga o valor para todas as conexões de entrada. O valor de MTU máximo deve estar entre **RFCOMM \_ min \_ MTU** e **RFCOMM \_ Max \_ MTU**, conforme definido no arquivo de cabeçalho Ws2bth. h.

Para a opção de soquete **\_ \_ \_ máximo BTH MTU** , *optval* é um ponteiro para MTU máximo ULONG \_ ; *optlen* é equivalente a "sizeof (ULong)".

## <a name="so_bth_mtu_min"></a>\_BTH \_ MTU \_ mín.

A opção de soquete **\_ BTH \_ MTU \_ min** é uma opção avançada usada principalmente para validação. A **opção \_ BTH \_ MTU \_ min** Socket define a MTU de RFCOMM mínima (unidade de transmissão máxima) para negociação de conexão. As conexões com um MTU RFCOMM menor que esse valor falham durante o processo de aceitação de [**conexão**](/windows/desktop/api/winsock2/nf-winsock2-connect) / [](/windows/desktop/api/winsock2/nf-winsock2-accept) . Embora a definição dessa opção de soquete seja permitida para um Soquete conectado, ela não terá efeito se a negociação tiver sido concluída. Definir essa opção de soquete em um soquete de escuta propaga o valor para todas as conexões de entrada.

Somente um soquete de escuta pode revisar o MTU para baixo, portanto, se o valor proposto pelo soquete de conexão for menor que o valor definido para o **\_ BTH \_ MTU \_ min** no soquete de escuta, a conexão será recusada. A MTU mínima deve estar entre **RFCOMM \_ min \_ MTU** e **RFCOMM \_ Max \_ MTU**, conforme definido no arquivo de cabeçalho Ws2bth. h.

Para a \_ opção de \_ soquete BTH MTU \_ min, *optval* é um ponteiro para MTU mínimo de ULong \_ ; *optlen* é equivalente a "sizeof (ULong)".

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt)
</dt> <dt>

[**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt)
</dt> <dt>

[**BluetoothAuthenticateDevice**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothauthenticatedevice)
</dt> <dt>

[**conectar**](/windows/desktop/api/winsock2/nf-winsock2-connect)
</dt> <dt>

[**aceitar**](/windows/desktop/api/winsock2/nf-winsock2-accept)
</dt> </dl>

 

 