---
title: Considerações de segurança de host de dispositivo
description: O uso do host de dispositivo cria problemas de segurança.
ms.assetid: 7cb445ea-5df4-4030-babd-62527b4d6210
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b5a51b90bff33949a33cd9fa1046deb1916ab30
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104454136"
---
# <a name="device-host-security-considerations"></a>Considerações de segurança de host de dispositivo

O uso do host de dispositivo cria problemas de segurança devido ao seguinte:

-   Os dispositivos hospedados em um computador que executa o Windows XP enviam anúncios em todas as redes.
-   Os dispositivos hospedados em um computador que executa o Windows XP permitem o controle de dispositivos de todas as redes.

Isso aumenta o risco para os consumidores domésticos, pois dispositivos como um player de mídia ou um sistema HVAC ou de iluminação hospedado em um computador que executa o Windows XP estão visíveis e podem ser controlados a partir de pontos de controle fora do início.

Ao criar um dispositivo hospedado, você precisa levar em consideração alguns problemas de segurança.

-   Para reduzir o escopo de descoberta e ataque de dispositivos baseados em UPnP, a TTL de todas as mensagens SSDP é 1. Isso significa que um dispositivo registrado só é descoberto por pontos de controle na mesma rede. Você pode configurar uma TTL mais alta no registro.
-   O registro de um dispositivo que não está em execução requer o registro prévio do Device. dll com COM, o que exige privilégio de administrador.
-   O registro de um dispositivo em execução requer privilégio de administrador, serviço local ou sistema local.
-   Quando o host do dispositivo é iniciado, ele é executado como [LocalService](/windows/desktop/Services/localservice-account). Isso dá ao dispositivo a capacidade de gerar auditorias e ler a chave do registro **HKEY \_ local \_ Machine** . O dispositivo tem acesso ao **HKEY \_ Current \_ User**. A conta LocalService pode usar recursos para os quais o LocalService recebeu acesso, bem como aqueles que concedem acesso ao AuthenticatedUser. O dispositivo restringiu o acesso ao sistema de arquivos.
-   As ACLs do sistema de arquivos devem ser atualizadas para permitir o acesso de [LocalService](/windows/desktop/Services/localservice-account) ao diretório de recursos.
-   Se o dispositivo precisar ter mais acesso de segurança, você poderá criar seu próprio processo para o dispositivo e registrá-lo usando [**IUPnPRegistrar:: RegisterRunningDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerrunningdevice).

 

 