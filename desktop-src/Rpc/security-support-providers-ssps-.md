---
title: Provedores de suporte de segurança (SSPs)
description: a partir do Windows 2000, o RPC dá suporte a uma variedade de provedores de segurança e pacotes.
ms.assetid: f82eba3d-412e-4cb6-9353-2e66bd0f377a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37e71f088a9366f76b499203997ffdf635a27c3aca7af5c7fc4314453fe1fa79
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120017986"
---
# <a name="security-support-providers-ssps"></a>Provedores de suporte de segurança (SSPs)

a partir do Windows 2000, o RPC dá suporte a uma variedade de provedores de segurança e pacotes. Elas incluem:

-   **Pacote de segurança do protocolo Kerberos.** O protocolo Kerberos V5 é um pacote de segurança padrão do setor. Ele usa os nomes principais do fullsic.
-   **SSP DO SCHANNEL.** Esse SSP implementa o pacote de segurança do provedor de protocolo unificado da Microsoft, que unifica SSL, tecnologia de comunicação privada (PCT) e TLS (segurança de nível de transporte) em um pacote de segurança. Ele reconhece os nomes principais msstd e fullsic.
-   **Pacote de segurança NTLM.** esse era o pacote de segurança principal para redes NTLM antes de Windows 2000.

Além disso, o Microsoft RPC fornece um *pseudo-SSP* que permite que os aplicativos negociem entre os SSPs reais. Esse pseudo SSP, chamado de Snego (mecanismo de negociação do GSS-API) simples, não fornece nenhum recurso de autenticação real. Seu único uso é ajudar os aplicativos a selecionar um SSP real. Atualmente, os programas cliente e servidor podem usar o Snego SSP para negociar entre o uso do pacote de segurança NTLM e o pacote de segurança do protocolo Kerberos. Para obter mais informações sobre como selecionar SSPs, consulte as [constantes de serviço de autenticação](authentication-service-constants.md).

Todos os SSPs que a Microsoft fornece, exceto SCHANNEL, reconhecem as credenciais de autenticação no formato fornecido pela estrutura de [**identidade de autenticação do Winnt da SEC \_ \_ \_**](/windows/desktop/api/Rpcdce/ns-rpcdce-sec_winnt_auth_identity_a) . Para obter detalhes, consulte [credenciais de autenticação de cliente](client-authentication-credentials.md). Para obter informações sobre como usar SSPs específicos, consulte [funções SSPI](/windows/desktop/SecMgmt/management-functions) e [usando o provedor de segurança Schannel](/windows/desktop/SecAuthN/secure-channel) na documentação de segurança do SDK (Software Development Kit) da plataforma.

 

 