---
title: Protocolo Kerberos V5
description: Protocolo Kerberos V5
ms.assetid: a53a1edf-f374-4cbf-8050-7cde45284157
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68d78c4bdc457007c04ad66163e2ebfd7f5397f9
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/20/2020
ms.locfileid: "105812052"
---
# <a name="kerberos-v5-protocol"></a>Protocolo Kerberos V5

O protocolo de autenticação Kerberos V5 tem um identificador de serviço de autenticação do RPC \_ C \_ Authn \_ GSS \_ Kerberos. O protocolo Kerberos define como os clientes interagem com um serviço de autenticação de rede e foi padronizado pelo IETF (Internet Engineering Task Force) em setembro de 1993, no documento [RFC 1510](https://www.ietf.org/rfc/rfc1510.txt). Os clientes obtêm tíquetes do centro de distribuição de chaves do Kerberos (KDC) e apresentam esses tíquetes para servidores quando as conexões são estabelecidas. Os tíquetes Kerberos representam as credenciais de rede do cliente.

Como o NTLM, o protocolo Kerberos usa o nome de domínio, o nome de usuário e a senha para representar a identidade do cliente. O tíquete Kerberos inicial obtido do KDC quando o usuário faz logon se baseia em um hash criptografado da senha do usuário. Esse tíquete inicial está armazenado em cache. Quando o usuário tenta se conectar a um servidor, o protocolo Kerberos verifica o cache de tíquete para um tíquete válido para esse servidor. Se um não estiver disponível, o tíquete inicial para o usuário será enviado ao KDC junto com uma solicitação de um tíquete para o servidor especificado. Esse tíquete de sessão é adicionado ao cache e pode ser usado para se conectar ao mesmo servidor até que o tíquete expire.

Quando um servidor chama [**CoQueryClientBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryclientblanket) usando o protocolo Kerberos, o nome de domínio e o nome de usuário do cliente são retornados. Quando um servidor chama [**CoImpersonateClient**](/windows/desktop/api/combaseapi/nf-combaseapi-coimpersonateclient), o token do cliente é retornado. Esses comportamentos são os mesmos que ao usar NTLM.

O protocolo Kerberos funciona nos limites do computador. Os computadores cliente e servidor devem estar em domínios e esses domínios devem ter uma relação de confiança.

O protocolo Kerberos requer autenticação mútua e dá suporte a ele remotamente. O cliente deve especificar o nome principal do servidor e a identidade do servidor deve corresponder exatamente ao nome principal. Se o cliente especificar **NULL** para o nome principal do servidor ou se o nome da entidade de segurança não corresponder ao servidor, a chamada falhará.

Com o protocolo Kerberos, os níveis de representação identificam, representam e delegam podem ser usados. Quando um servidor chama [**CoImpersonateClient**](/windows/desktop/api/combaseapi/nf-combaseapi-coimpersonateclient), o token retornado é válido fora do computador por um período de tempo entre 5 minutos e 8 horas. Após esse tempo, ele pode ser usado somente no computador servidor. Se um servidor for "Run as Activator" e a ativação for feita com o protocolo Kerberos, o token do servidor expirará entre 5 minutos e 8 horas após a ativação.

O protocolo de autenticação Kerberos V5 implementado pelo WindowsÂ dá suporte ao [encobrimento](cloaking.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Pacotes de segurança e COM](com-and-security-packages.md)
</dt> </dl>

 

 




