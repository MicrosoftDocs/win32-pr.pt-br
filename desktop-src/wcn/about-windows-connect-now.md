---
title: sobre Conexão Fácil do Windows
description: o Conexão Fácil do Windows (WCN) fornece um mecanismo simples e seguro para dispositivos e pontos de acesso à rede (como impressoras, câmera e PCs) para conexão e troca de configurações.
ms.assetid: 5c654800-e58b-4a94-b7a6-9a603f540603
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c46e0acbf2d2eb728b0b62610040aaa08e06d466c5bbd5ab47237c46a8612ddf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119593706"
---
# <a name="about-windows-connect-now"></a>sobre Conexão Fácil do Windows

o Conexão Fácil do Windows (WCN) fornece um mecanismo simples e seguro para dispositivos e pontos de acesso à rede (como impressoras, câmera e PCs) para conexão e troca de configurações. Essa API é a implementação da Microsoft do protocolo/Wi-Fi (configuração protegida Wi-Fi) (WSC), que foi criado pela Aliança de Wi-Fi como uma solução para redes domésticas e pequenas empresas. Essa tecnologia não se destina a cenários empresariais.

> [!Note]  
> O nome da especificação foi alterado entre a versão 1.0 h e a versão 2. A especificação da versão 1.0 h foi denominada Wi-Fi configuração protegida (WPS). A partir da especificação da versão 2, a especificação é chamada de Wi-Fi configuração simples (WSC). Em nossa documentação, os termos WPS e WSC são usados de maneira intercambiável, a menos que sejam indicados.

 

Conexão Fácil do Windows permite que os aplicativos pesquisem dispositivos compatíveis com WCN usando a [API de descoberta de função](/previous-versions/windows/desktop/fundisc/fd-portal). O escopo de uma pesquisa pode ser limitado a um SSID, estado, categoria ou até mesmo ampliado para incluir todos os dispositivos compatíveis com o WCN. Depois que os dispositivos são localizados, a API WCN permite a comunicação com o dispositivo compatível com WCN para facilitar a configuração ou a conectividade.

 

 