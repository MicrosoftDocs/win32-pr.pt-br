---
description: O protocolo CredSSP é um provedor de suporte de segurança que é implementado usando a interface de provedor de suporte de segurança (SSPI).
ms.assetid: b3006b89-d9fc-4444-a3c8-ad2698de501c
title: Provedor de suporte à segurança de credenciais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e9aa961f37043d84dc21280ea7d5ecb9c27c075
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164868"
---
# <a name="credential-security-support-provider"></a>Provedor de suporte à segurança de credenciais

O protocolo CredSSP é um provedor de suporte de segurança que é implementado usando a interface de provedor de suporte de segurança ([SSPI](sspi.md)). O CredSSP permite que um aplicativo delegue as credenciais do usuário do cliente para o servidor de destino para autenticação remota. O CredSSP fornece um canal de [protocolo de segurança de camada de transporte](transport-layer-security-protocol.md) criptografado. O cliente é autenticado pelo canal criptografado usando o protocolo Negotiate (SPNEGO) simples e protegido com o [Microsoft Kerberos](microsoft-kerberos.md) ou o [Microsoft NTLM](microsoft-ntlm.md).

> [!Caution]  
> Essa não é uma delegação restrita. O CredSSP passa as credenciais completas do usuário para o servidor sem nenhuma restrição.

 

Para obter informações sobre o SPNEGO, consulte [Microsoft Negotiate](microsoft-negotiate.md).

Depois que o cliente e o servidor são autenticados, o cliente passa as credenciais do usuário para o servidor. As credenciais são criptografadas duplamente nas chaves de sessão SPNEGO e TLS. O CredSSP dá suporte ao logon baseado em senha, bem como ao logon de cartão inteligente com base em [*X. 509*](/windows/desktop/SecGloss/x-gly) e PKINIT.

> [!IMPORTANT]
> O CredSSP não dá suporte a clientes WOW64.

 

Para obter mais informações sobre CredSSP, consulte os tópicos a seguir.



| Tópico                                                                         | Descrição                                                                                       |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [Configurações de Política de Grupo CredSSP](credssp-group-policy-settings.md)<br/> | A delegação de credenciais por CredSSP pode ser controlada usando configurações de política de grupo.<br/> |



 

 

