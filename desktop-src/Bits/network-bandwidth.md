---
title: Largura de Banda de Rede
description: As transferências em segundo plano usam apenas largura de banda de rede ociosa em um esforço para preservar a experiência interativa do usuário com outros aplicativos de rede, como o Internet Explorer.
ms.assetid: c0b92a33-7afc-4250-8549-54cc46013239
ms.topic: article
ms.date: 10/09/2018
ms.openlocfilehash: 39a38a0efd5f2caea432fc9d13f7a958b6bcd407
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007783"
---
# <a name="network-bandwidth"></a>Largura de Banda de Rede

As transferências em segundo plano usam apenas largura de banda de rede ociosa em um esforço para preservar a experiência interativa do usuário com outros aplicativos de rede, como navegadores da Web. O BITS ajusta seu uso da largura de banda à medida que o usuário aumenta ou diminui seu uso da largura de banda. Observe que o BITS ainda transfere uma pequena quantidade de dados durante o alto uso da rede para garantir que os trabalhos do BITS façam progresso.

O BITS monitora o tráfego de rede no IGD (dispositivo de gateway de Internet) ou na NIC (placa de interface de rede) do cliente e usa apenas a parte ociosa da largura de banda da rede. O BITS também permite [LEDBAT](https://blogs.technet.microsoft.com/networking/2018/07/25/ledbat/) em conexões http para ajudar a aliviar o congestionamento da rede.

Se o BITS usar a placa de interface de rede para medir o tráfego e não houver aplicativos de rede em execução no cliente, o BITS consumirá a maior parte da largura de banda disponível. Isso não significa que a rede além do cliente está ociosa; a rede pode estar com capacidade total.

Isso pode ser um problema se o cliente tiver um adaptador de rede rápido, mas a conexão de Internet completa estiver por meio de um link lento (como um roteador DSL) porque o BITS competirá pela largura de banda completa em vez de usar apenas a largura de banda disponível no link lento; O BITS não tem visibilidade do tráfego de rede além do cliente.

Um dispositivo de gateway que dá suporte a contadores pode eliminar esse problema porque o BITS mediria o tráfego no link lento e usaria a largura de banda adequadamente. Se o dispositivo não oferecer suporte a contadores, você poderá reduzir o impacto desse tipo de conexão, usando a política **MaxInternetBandwidth** para limitar a largura de banda que o bits usa no computador cliente. Para obter detalhes, consulte [políticas de grupo](group-policies.md).

Se o computador contiver várias interfaces de rede, como um modem, uma VPN (rede virtual privada) e várias placas de interface de rede (NIC), o BITS chamará a função auxiliar de IP, [**GetBestInterfaceEx**](/windows/desktop/api/iphlpapi/nf-iphlpapi-getbestinterfaceex), para determinar a interface que tem a melhor rota para o endereço IP especificado. Em seguida, o BITS monitorará o uso da largura de banda nessa interface.

## <a name="using-an-internet-gateway-device-igd-to-determine-usage"></a>Usando um IGD (dispositivo de gateway de Internet) para determinar o uso

Para usar um dispositivo de gateway, o dispositivo deve dar suporte a contadores de bytes (o dispositivo deve responder às ações GetTotalBytesSent e GetTotalBytesReceived) e o Universal Plug and Play (UPnP) deve estar habilitado.

Os BITS usarão a placa de interface de rede se:

-   O dispositivo de gateway não dá suporte aos contadores
-   O UPnP não está habilitado
-   O servidor está dentro da mesma sub-rede
-   O dispositivo de gateway não retorna os dados do contador em menos de 200 tiques

Se o usuário usar um perfil de rede pública, o perfil deverá permitir UPnP. Por padrão, os perfis de rede privada e de domínio permitem UPnP.

Se uma conexão VPN for usada, o BITS usará o primeiro dispositivo que o UPnP retorna.