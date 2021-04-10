---
title: Sobre o Windows Connect agora
description: O WCN (Windows Connect Now) fornece um mecanismo simples e seguro para dispositivos e pontos de acesso à rede (como impressoras, câmera e computadores) para conexão e troca de configurações.
ms.assetid: 5c654800-e58b-4a94-b7a6-9a603f540603
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0118c6a053c480a36138f8dae850ee0862501944
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084816"
---
# <a name="about-windows-connect-now"></a>Sobre o Windows Connect agora

O WCN (Windows Connect Now) fornece um mecanismo simples e seguro para dispositivos e pontos de acesso à rede (como impressoras, câmera e computadores) para conexão e troca de configurações. Essa API é a implementação da Microsoft do protocolo/Wi-Fi (configuração protegida Wi-Fi) (WSC), que foi criado pela Aliança de Wi-Fi como uma solução para redes domésticas e pequenas empresas. Essa tecnologia não se destina a cenários empresariais.

> [!Note]  
> O nome da especificação foi alterado entre a versão 1.0 h e a versão 2. A especificação da versão 1.0 h foi denominada Wi-Fi configuração protegida (WPS). A partir da especificação da versão 2, a especificação é chamada de Wi-Fi configuração simples (WSC). Em nossa documentação, os termos WPS e WSC são usados de maneira intercambiável, a menos que sejam indicados.

 

Agora, o Windows Connect permite que os aplicativos pesquisem dispositivos compatíveis com WCN usando a [API de descoberta de função](/previous-versions/windows/desktop/fundisc/fd-portal). O escopo de uma pesquisa pode ser limitado a um SSID, estado, categoria ou até mesmo ampliado para incluir todos os dispositivos compatíveis com o WCN. Depois que os dispositivos são localizados, a API WCN permite a comunicação com o dispositivo compatível com WCN para facilitar a configuração ou a conectividade.

 

 