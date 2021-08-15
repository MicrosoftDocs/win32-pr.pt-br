---
title: Endereços Teredo
ms.assetid: e2e185c2-e53d-471d-aedb-54d75f9db0bb
description: 'Saiba mais sobre: Endereços Teredo'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08a8b283d2bab6c9ba091ecc3b37c6218fadb0face78e04b807be03d68b814d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118354132"
---
# <a name="teredo-addresses"></a>Endereços Teredo

Um endereço Teredo consiste no seguinte:

-   **Prefixo teredo**

    Os primeiros 32 bits são para o prefixo Teredo, que é o mesmo para todos os endereços Teredo. Windows XP e Windows Server 2003 usaram inicialmente o prefixo 3FFE:831F::/32 Teredo. O prefixo definido para Teredo no RFC 4380 é 2001::/32 e é o prefixo usado pelo Teredo no Windows Vista e Windows Server 2008. Computadores que executam Windows XP e Windows Server 2003 usarão o prefixo 2001::/32 Teredo quando atualizados com o Boletim de Segurança da Microsoft MS06-064.

-   **Endereço IPv4 do servidor Teredo**

    Os próximos 32 bits contêm o endereço público IPv4 do servidor Teredo que ajudou a configurar esse endereço Teredo. Para obter mais informações, consulte "Configuração inicial para clientes Teredo" neste artigo.

-   **Sinalizadores**

    Os próximos 16 bits para são reservados para sinalizadores Teredo. Para Windows clientes Teredo baseados em XP, o único sinalizador definido é o bit de ordem alta conhecido como sinalizador Cone. O sinalizador Cone é definido quando o cliente Teredo está atrás de um NAT de cone. A determinação de se o NAT conectado à Internet é um NAT de casinha ocorre durante a configuração inicial do cliente Teredo. Para obter mais informações, consulte "Configuração inicial para clientes Teredo" neste artigo.

    Para Windows clientes Teredo baseados no Windows e Windows Server 2008, os bits nãoutilados no campo Sinalizadores fornecem um nível de proteção contra verificações de endereço por usuários mal-intencionados. Os 16 bits dentro do campo Sinalizadores para clientes Teredo baseados em Windows Vista e Windows Server 2008 consistem no seguinte: CRAAAAUG AAAAAAAAA. O bit C é para o sinalizador Cone. O bit R é reservado para uso futuro. O bit U é para o sinalizador Universal/Local (definido como 0). O bit G é o sinalizador Individual/Grupo (definido como 0). Os bits A são definidos como um número gerado aleatoriamente de 12 bits. Usando um número aleatório para os bits A, um usuário mal-intencionado que determinou o restante do endereço Teredo capturando a troca de configuração inicial de pacotes entre o cliente Teredo e o servidor Teredo terá que tentar até 4.096 (212) endereços diferentes para determinar o endereço de um cliente Teredo durante uma verificação de endereço.

-   **Porta externa obscurecida**

    Os próximos 16 bits armazenam uma versão obscurecida da porta UDP externa correspondente a todo o tráfego Teredo para esse cliente Teredo. Quando o cliente Teredo envia seu pacote inicial para um servidor Teredo, a porta UDP de origem do pacote é mapeada pelo NAT para uma porta UDP externa diferente. O cliente Teredo mantém esse mapeamento de porta para que ele permaneça na tabela de tradução da NAT. Portanto, todo o tráfego Teredo para o host usa a mesma porta UDP externa mapeada. A porta UDP externa é determinada pelo servidor Teredo da porta UDP de origem do pacote inicial de entrada enviado pelo cliente Teredo e enviado de volta para o cliente Teredo.

    A porta externa é obscurecida por XORing na porta externa com 0xFFFF. Por exemplo, a versão obscurecida da porta externa 5000 no formato hexadecimal é EC77 (5000 = 0x1388, 0x1388 XOR 0xFFFF = 0xEC77). A obscuração da porta externa impede que os NATs translatam a porta externa dentro do payload dos pacotes que eles estão encaminhando.

-   **Endereço externo obscurecido**

    Os últimos 32 bits armazenam uma versão obscurecida do endereço IPv4 externo correspondente a todo o tráfego Teredo para esse cliente Teredo. Assim como a porta externa, quando o cliente Teredo envia seu pacote inicial para um servidor Teredo, o endereço IP de origem do pacote é mapeado pelo NAT para um endereço externo (público) diferente. O cliente Teredo mantém esse mapeamento de endereço para que ele permaneça na tabela de tradução da NAT. Portanto, todo o tráfego Teredo para o host usa o mesmo endereço IPv4 público, mapeado, externo. O endereço IPv4 externo é determinado pelo servidor Teredo do endereço IPv4 de origem do pacote inicial de entrada enviado pelo cliente Teredo e enviado de volta para o cliente Teredo.

    O endereço externo é obscurecido por XORing no endereço externo com 0xFFFFFFFF. Por exemplo, a versão obscurecida do endereço IPv4 público 131.107.0.1 no formato hexadecimal de dois-pontos é 7C94:FFFE (131.107.0.1 = 0x836B0001, 0x836B0001 XOR 0xFFFFFFFF = 0x7C94FFFE). A obscuração do endereço externo impede que os NATs translatam o endereço externo dentro do payload dos pacotes que eles estão encaminhando.

 

 




