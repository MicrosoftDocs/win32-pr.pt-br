---
title: Extensões do servidor de políticas de rede
description: A API de Extensões NPS permite que os desenvolvedores de software escrevam DLLs de extensão que podem ser usadas para autenticação, autorização e contabilidade. A API de Extensões NPS dá suporte ao protocolo RADIUS (Remote Authentication Dial-In User Service).
ms.assetid: f459025f-fe5e-4ffa-a651-c70a4f8234ae
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8db32889f266861809a0637dd380eb9f5d2ba7265bdf16d6a9404ed96a5420a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120128766"
---
# <a name="network-policy-server-extensions"></a>Extensões do servidor de políticas de rede

> [!Note]  
> O IAS (Serviço de Autenticação da Internet) foi renomeado como NPS (Servidor de Políticas de Rede) a partir do Windows Server 2008. O conteúdo deste tópico se aplica a IAS e NPS. Em todo o texto, o NPS é usado para se referir a todas as versões do serviço, incluindo as versões originalmente conhecidas como IAS.

 

A API de Extensões NPS permite que os desenvolvedores de software escrevam DLLs de extensão que podem ser usadas para autenticação, autorização e contabilidade. A API de Extensões NPS dá suporte ao protocolo RADIUS (Remote Authentication Dial-In User Service).

As DLLs de extensão implementadas usando a API de Extensões nps podem fornecer controle de sessão e contabilidade aprimorados. Essas DLLs podem ser usadas para cenários como controlar o número de sessões de rede do usuário final, usar um servidor de estado e conectar-se a bancos de dados de autenticação de domínio e serviços do Active Directory. As DLLs de extensão podem expandir as autorizações de acesso remoto fornecidas pelo NPS adicionando suas próprias autorizações ao enviar uma resposta Accept de volta a um cliente de autenticação.

A API de Extensões NPS é aplicável em qualquer ambiente de computação em que ela melhoraria a eficiência para autenticar usuários discados por meio de um servidor remoto. Essa tecnologia é especialmente útil para ISPs (Provedores de Serviços de Internet).

## <a name="in-this-section"></a>Nesta seção

[Visão geral](/windows/desktop/Nps/ias-about-internet-authentication-service)

Informações gerais sobre RADIUS e a API de Extensões NPS.

[Usando](/windows/desktop/Nps/ias-using-internet-authentication-service)

Código de exemplo que demonstra como usar a API de Extensões do NPS.

[Referência](/windows/desktop/Nps/ias-internet-authentication-service-reference)

Documentação de tipos, funções e estruturas enumerados que compõem a API de Extensões do NPS.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Servidor de Política de Rede (Serviço de Autenticação da Internet)](portal.md)
</dt> <dt>

[Protocolo EAP (Extensible Authentication Protocol)](../eap/eap-start-page.md)
</dt> </dl>

 

 