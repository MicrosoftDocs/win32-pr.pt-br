---
title: Endereços Teredo
ms.assetid: e2e185c2-e53d-471d-aedb-54d75f9db0bb
description: 'Saiba mais sobre: endereços Teredo'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc08a53da2f710423d948e9479df2aeb08f20178
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297578"
---
# <a name="teredo-addresses"></a>Endereços Teredo

Um endereço Teredo consiste no seguinte:

-   **Prefixo Teredo**

    Os primeiros 32 bits são para o prefixo Teredo, que é o mesmo para todos os endereços Teredo. O Windows XP e o Windows Server 2003 usaram inicialmente o prefixo Teredo 3FFE: 831F::/32. O prefixo definido para Teredo na RFC 4380 é 2001::/32 e é o prefixo usado pelo Teredo no Windows Vista e no Windows Server 2008. Os computadores que executam o Windows XP e o Windows Server 2003 usarão o prefixo de Teredo 2001::/32 quando atualizados com o boletim de segurança da Microsoft MS06-064.

-   **Endereço IPv4 do servidor Teredo**

    Os próximos 32 bits contêm o endereço IPv4 público do servidor Teredo que ajudou a configurar esse endereço Teredo. Para obter mais informações, consulte "configuração inicial para clientes Teredo" neste artigo.

-   **Sinalizadores**

    Os próximos 16 bits para são reservados para sinalizadores Teredo. Para clientes Teredo baseados no Windows XP, o único sinalizador definido é o bit de ordem superior conhecido como o sinalizador de cone. O sinalizador de cone é definido quando o cliente Teredo está atrás de um NAT de cone. A determinação de se o NAT conectado à Internet é um cone NAT que ocorre durante a configuração inicial do cliente Teredo. Para obter mais informações, consulte "configuração inicial para clientes Teredo" neste artigo.

    Para clientes Teredo baseados no Windows Vista e no Windows Server 2008, bits não utilizados no campo sinalizadores fornecem um nível de proteção contra verificações de endereço por usuários mal-intencionados. Os 16 bits dentro do campo Flags para clientes Teredo baseados no Windows Vista e no Windows Server 2008 consistem no seguinte: CRAAAAUG AAAAAAAA. O bit C é para o sinalizador de cone. O bit R é reservado para uso futuro. O bit U é para o sinalizador universal/local (definido como 0). O G bit é um sinalizador individual/de grupo (definido como 0). Os bits a são definidos como um número gerado aleatoriamente de 12 bits. Usando um número aleatório para os bits, um usuário mal-intencionado que determinou o restante do endereço Teredo capturando a troca de configuração inicial dos pacotes entre o cliente Teredo e o servidor Teredo precisará tentar até 4.096 (212) endereços diferentes para determinar o endereço de um cliente Teredo durante uma verificação de endereço.

-   **Porta externa obscurecida**

    Os próximos 16 bits armazenam uma versão obscura da porta UDP externa correspondente a todo o tráfego Teredo para esse cliente Teredo. Quando o cliente Teredo envia seu pacote inicial para um servidor Teredo, a porta UDP de origem do pacote é mapeada pelo NAT para uma porta UDP externa diferente. O cliente Teredo mantém esse mapeamento de porta para que ele permaneça na tabela de conversão da NAT. Portanto, todo o tráfego Teredo para o host usa a mesma porta UDP mapeada e externa. A porta UDP externa é determinada pelo servidor Teredo da porta UDP de origem do pacote inicial de entrada enviado pelo cliente Teredo e enviada de volta para o cliente Teredo.

    A porta externa é obscurecida por XORing a porta externa com 0xFFFF. Por exemplo, a versão obscurecida da porta externa 5000 no formato hexadecimal é EC77 (5000 = 0x1388, 0x1388 XOR 0xFFFF = 0xEC77). Obscurecer a porta externa impede que os NATs traduzam a porta externa dentro do conteúdo dos pacotes que estão encaminhando.

-   **Endereço externo obscuro**

    Os últimos 32 bits armazenam uma versão obscura do endereço IPv4 externo correspondente a todo o tráfego Teredo para esse cliente Teredo. Assim como a porta externa, quando o cliente Teredo envia seu pacote inicial para um servidor Teredo, o endereço IP de origem do pacote é mapeado pelo NAT para um endereço externo (público) diferente. O cliente Teredo mantém esse mapeamento de endereço para que ele permaneça na tabela de conversão da NAT. Portanto, todo o tráfego de Teredo para o host usa o mesmo endereço IPv4 público, mapeado e externo. O endereço IPv4 externo é determinado pelo servidor Teredo do endereço IPv4 de origem do pacote inicial de entrada enviado pelo cliente Teredo e enviado de volta para o cliente Teredo.

    O endereço externo é obscurecido por XORing o endereço externo com 0xFFFFFFFF. Por exemplo, a versão obscurecida do endereço IPv4 público 131.107.0.1 em formato hexadecimal com dois-pontos é 7C94: FFFE (131.107.0.1 = 0x836B0001, 0x836B0001 XOR 0xFFFFFFFF = 0x7C94FFFE). Obscurecer o endereço externo impede que os NATs traduzam o endereço externo dentro do conteúdo dos pacotes que estão encaminhando.

 

 




