---
title: Provedores de suporte de segurança (SSPs)
description: A partir do Windows 2000, o RPC dá suporte a uma variedade de provedores de segurança e pacotes.
ms.assetid: f82eba3d-412e-4cb6-9353-2e66bd0f377a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92cc5417dd6142c693005a1aab9d39738d108ae2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084838"
---
# <a name="security-support-providers-ssps"></a>Provedores de suporte de segurança (SSPs)

A partir do Windows 2000, o RPC dá suporte a uma variedade de provedores de segurança e pacotes. Estão incluídos:

-   **Pacote de segurança do protocolo Kerberos.** O protocolo Kerberos V5 é um pacote de segurança padrão do setor. Ele usa os nomes principais do fullsic.
-   **SSP DO SCHANNEL.** Esse SSP implementa o pacote de segurança do provedor de protocolo unificado da Microsoft, que unifica SSL, tecnologia de comunicação privada (PCT) e TLS (segurança de nível de transporte) em um pacote de segurança. Ele reconhece os nomes principais msstd e fullsic.
-   **Pacote de segurança NTLM.** Esse era o pacote de segurança principal para redes NTLM antes do Windows 2000.

Além disso, o Microsoft RPC fornece um *pseudo-SSP* que permite que os aplicativos negociem entre os SSPs reais. Esse pseudo SSP, chamado de Snego (mecanismo de negociação do GSS-API) simples, não fornece nenhum recurso de autenticação real. Seu único uso é ajudar os aplicativos a selecionar um SSP real. Atualmente, os programas cliente e servidor podem usar o Snego SSP para negociar entre o uso do pacote de segurança NTLM e o pacote de segurança do protocolo Kerberos. Para obter mais informações sobre como selecionar SSPs, consulte as [constantes de serviço de autenticação](authentication-service-constants.md).

Todos os SSPs que a Microsoft fornece, exceto SCHANNEL, reconhecem as credenciais de autenticação no formato fornecido pela estrutura de [**identidade de autenticação do Winnt da SEC \_ \_ \_**](/windows/desktop/api/Rpcdce/ns-rpcdce-sec_winnt_auth_identity_a) . Para obter detalhes, consulte [credenciais de autenticação de cliente](client-authentication-credentials.md). Para obter informações sobre como usar SSPs específicos, consulte [funções SSPI](/windows/desktop/SecMgmt/management-functions) e [usando o provedor de segurança Schannel](/windows/desktop/SecAuthN/secure-channel) na documentação de segurança do SDK (Software Development Kit) da plataforma.

 

 