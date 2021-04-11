---
description: Habilita a escalabilidade de porta local para um soquete.
ms.assetid: c5142baf-9e2d-4c06-8719-9090fd2d9487
title: SO_PORT_SCALABILITY (Ws2def. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 565caeb472ac5cb15061d32b47a048a9a210885e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090356"
---
# <a name="so_port_scalability"></a>Portanto \_ , \_ escalabilidade de porta

A opção de soquete de **\_ \_ escalabilidade de porta,** permite a escalabilidade de porta local para um soquete.

<dl> <dt>

<span id="SO_PORT_SCALABILITY"></span><span id="so_port_scalability"></span>**Portanto \_ , \_ escalabilidade de porta**
</dt> <dd> <dl> <dt>

0x3006
</dt> <dt>



A opção de soquete de **\_ \_ escalabilidade de porta,** permite a escalabilidade de porta local, permitindo que a alocação de porta seja maximizada alocando portas curinga várias vezes para pares de porta de endereço local diferentes em um computador local.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentários

Observação: em plataformas em que tanto \_ a \_ escalabilidade de porta quanto a \_ reutilização de \_ UNICASTPORT têm suporte, prefira usar para \_ reutilizar o \_ UNICASTPORT.

Os ambientes de servidor proxy têm problemas de escalabilidade devido à disponibilidade limitada da porta local. Uma maneira de contornar isso é adicionar mais endereços IP ao computador. No entanto, por padrão, as portas curinga usadas com a função [**BIND**](/windows/desktop/api/winsock/nf-winsock-bind) são limitadas ao tamanho do intervalo de portas dinâmicas no computador local (até 64K portas, mas geralmente menos), independentemente do número de endereços IP no computador local. Trabalhar em conjunto com isso requer que o aplicativo Mantenha seu próprio pool de portas com a reserva de porta ou usando heurística.

Para evitar que todos os aplicativos que exigem escalabilidade gerenciem seu próprio pool de portas e para permitir maior escalabilidade enquanto mantém a compatibilidade de aplicativos, o Windows Server 2008 introduziu a opção de soquete de **\_ \_ escalabilidade de porta** para ajudar a maximizar a alocação de portas curinga. A alocação de porta é maximizada, permitindo que um aplicativo aloque portas curinga para cada par de porta e endereço local exclusivos. Portanto, se um computador local tiver quatro endereços IP, até 256 de portas curinga (64 K portas × 4 endereços IP) poderão ser alocados por solicitações de função de [**ligação**](/windows/desktop/api/winsock/nf-winsock-bind) curinga.

Quando a opção de soquete de **\_ \_ escalabilidade de porta** for definida em um soquete e uma chamada para a função de [**Associação**](/windows/desktop/api/winsock/nf-winsock-bind) for feita para um endereço especificado e uma porta curinga (o parâmetro *Name* for definido com um endereço específico e uma porta 0), o Winsock alocará uma porta para o endereço especificado. Essa alocação será baseada em todos os endereços IP e portas possíveis/por endereço no computador local. Se uma porta curinga for adquirida usando a opção de **\_ \_ escalabilidade de porta** , essa porta não poderá ser alocada por outro soquete sem a opção de **\_ \_ escalabilidade de porta** . Essa restrição está em vigor para evitar problemas de compatibilidade com versões anteriores com aplicativos que assumem que uma porta local curinga não pode ser reutilizada. Observe que isso significa que os aplicativos que adquirem um grande número de portas usando a **\_ \_ escalabilidade de porta** podem não usar aplicativos herdados de portas. Se todas as portas efêmeras disponíveis tiverem sido adquiridas para pelo menos um endereço com a **\_ \_ escalabilidade de porta** , nenhuma outra alocação de porta curinga será possível sem a opção de soquete.

Para ter qualquer efeito, a opção de **\_ \_ escalabilidade de porta de so** deve ser definida antes que a função de [**Associação**](/windows/desktop/api/winsock/nf-winsock-bind) seja chamada. Um exemplo de como isso seria usado em um computador com dois endereços é descrito abaixo:

-   A função [**Socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) é chamada por um processo para criar um soquete.
-   A função [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) é chamada para habilitar a opção de soquete de **\_ \_ escalabilidade de porta, portanto,** no soquete recém-criado.
-   A função [**BIND**](/windows/desktop/api/winsock/nf-winsock-bind) é chamada para fazer uma ligação em um dos endereços IP do computador local e na porta 0.
-   Em seguida, a função [**Connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect) é chamada para se conectar a um endereço IP remoto. O soquete é usado pelo aplicativo conforme necessário.
-   Uma função de [**soquete**](/windows/desktop/api/Winsock2/nf-winsock2-socket) é chamada pelo mesmo processo (possivelmente um thread diferente) para criar um segundo soquete.
-   A função [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) é chamada para habilitar a opção de soquete de **\_ \_ escalabilidade de porta, portanto,** no segundo soquete recém-criado.
-   A função [**BIND**](/windows/desktop/api/winsock/nf-winsock-bind) é chamada com o segundo endereço IP do computador local e a porta 0. Mesmo quando todas as portas tiverem sido alocadas anteriormente, essa chamada terá êxito porque há vários endereços IP disponíveis no computador local e a opção de soquete de **\_ \_ escalabilidade de porta, portanto,** foi definida em ambos os soquetes no mesmo processo.
-   Em seguida, a função [**Connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect) é chamada para se conectar a um endereço IP remoto. O segundo soquete é usado pelo aplicativo, conforme necessário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                |
| parâmetro<br/>                   | <dl> <dt>Ws2def. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt)
</dt> <dt>

[**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt)
</dt> <dt>

[**Opções de soquete de soquete de SOL \_**](sol-socket-socket-options.md)
</dt> <dt>

[**Opções de soquete**](socket-options.md)
</dt> </dl>

 

 




