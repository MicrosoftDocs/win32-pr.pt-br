---
title: Extensões do servidor de políticas de rede
description: A API de extensões do NPS permite que os desenvolvedores de software gravem DLLs de extensão que podem ser usadas para autenticação, autorização e contabilidade. A API de extensões do NPS dá suporte ao protocolo RADIUS (serviço RADIUS).
ms.assetid: f459025f-fe5e-4ffa-a651-c70a4f8234ae
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddd6f9bd0be7479726110b41d6060a7e5c836bb8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917531"
---
# <a name="network-policy-server-extensions"></a>Extensões do servidor de políticas de rede

> [!Note]  
> O IAS (serviço de autenticação da Internet) foi renomeado como NPS (servidor de políticas de rede) a partir do Windows Server 2008. O conteúdo deste tópico aplica-se ao IAS e ao NPS. Em todo o texto, o NPS é usado para fazer referência a todas as versões do serviço, incluindo as versões originalmente chamadas de IAS.

 

A API de extensões do NPS permite que os desenvolvedores de software gravem DLLs de extensão que podem ser usadas para autenticação, autorização e contabilidade. A API de extensões do NPS dá suporte ao protocolo RADIUS (serviço RADIUS).

As DLLs de extensão implementadas usando a API de extensões do NPS podem fornecer controle de sessão e contabilidade avançados. Essas DLLs podem ser usadas para cenários como controlar o número de sessões de rede do usuário final, usar um servidor de estado e conectar-se a bancos de dados de autenticação de domínio e serviços de Active Directory. As DLLs de extensão podem expandir as autorizações de acesso remoto fornecidas pelo NPS adicionando suas próprias autorizações ao enviar uma resposta de aceitação de volta a um cliente de autenticação.

A API de extensões do NPS é aplicável em qualquer ambiente computacional em que a eficiência seria aprimorada para autenticar usuários de discagem por meio de um servidor remoto. Essa tecnologia é especialmente útil para provedores de serviços de Internet (ISPs).

## <a name="in-this-section"></a>Nesta seção

[Visão geral](/windows/desktop/Nps/ias-about-internet-authentication-service)

Informações gerais sobre o RADIUS e a API de extensões do NPS.

[Usando](/windows/desktop/Nps/ias-using-internet-authentication-service)

Código de exemplo que demonstra como usar a API de extensões do NPS.

[Referência](/windows/desktop/Nps/ias-internet-authentication-service-reference)

Documentação de tipos enumerados, funções e estruturas que compõem a API de extensões do NPS.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Servidor de políticas de rede (serviço de autenticação da Internet)](portal.md)
</dt> <dt>

[Protocolo EAP (Extensible Authentication Protocol)](../eap/eap-start-page.md)
</dt> </dl>

 

 