---
title: Considerações sobre segurança do host do dispositivo
description: Usar o host do dispositivo cria problemas de segurança.
ms.assetid: 7cb445ea-5df4-4030-babd-62527b4d6210
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb4e8cdce90cdc5801010833db4cb97c49487c16a3926bf235f126f33e1078f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120008086"
---
# <a name="device-host-security-considerations"></a>Considerações sobre segurança do host do dispositivo

O uso do host do dispositivo cria problemas de segurança devido ao seguinte:

-   Dispositivos hospedados em um computador que executa Windows XP envia anúncios em todas as redes.
-   Dispositivos hospedados em um computador que executa Windows XP permitem o controle de dispositivos de todas as redes.

Isso aumenta o risco para os consumidores de casa, porque dispositivos como um player de mídia ou uma iluminação ponte ou sistema HVAC hospedado em um computador que executa o Windows XP estão visíveis e podem ser controlados de pontos de controle fora da casa.

Ao criar um dispositivo hospedado, você precisa levar em consideração alguns problemas de segurança.

-   Para reduzir o escopo de descoberta e ataque de dispositivos baseados em UPnP, o TTL de todas as mensagens SSDP é 1. Isso significa que um dispositivo registrado só é descoberto por pontos de controle na mesma rede. Você pode configurar um TTL mais alto no Registro.
-   Registrar um dispositivo não em execução requer o registro antecipado do dispositivo .dll com COM, o que requer privilégio de administrador.
-   O registro de um dispositivo em execução requer privilégios de Administrador, Serviço Local ou Sistema Local.
-   Quando o host do dispositivo é iniciado, ele é executado como [LocalService.](/windows/desktop/Services/localservice-account) Isso dá ao dispositivo a capacidade de gerar auditorias e ler a **chave do registro HKEY LOCAL \_ \_ MACHINE.** O dispositivo tem acesso ao **HKEY \_ CURRENT \_ USER.** A conta LocalService pode usar recursos aos quais LocalService recebeu acesso, bem como aqueles que concedem acesso a AuthenticatedUser. O dispositivo tem acesso restrito ao sistema de arquivos.
-   As ACLs do sistema de arquivos devem ser atualizadas para permitir [o acesso de LocalService](/windows/desktop/Services/localservice-account) ao diretório de recursos.
-   Se o dispositivo precisa ter mais acesso à segurança, você pode criar seu próprio processo para o dispositivo e registrá-lo usando [**IUPnPRegistrar::RegisterRunningDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerrunningdevice).

 

 