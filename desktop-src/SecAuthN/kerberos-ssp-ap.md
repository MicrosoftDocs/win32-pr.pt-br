---
description: O pacote de autenticação Kerberos é usado ao fazer logon em uma rede; os logons locais são tratados por MSV1 \_ 0.
ms.assetid: 43970c99-53f1-43c1-9d9f-65573572f731
title: SSP/PA Kerberos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d14565c8c6526d9cab34d7b9ddec9a0a04ff8de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011143"
---
# <a name="kerberos-sspap"></a>SSP/PA Kerberos

O pacote de autenticação [*Kerberos*](../secgloss/k-gly.md) é usado ao fazer logon em uma rede; os logons locais são tratados por MSV1 \_ 0.

Quando um usuário faz logon usando uma conta de rede, por padrão, o Kerberos tenta se conectar ao [*centro de distribuição de chaves*](../secgloss/k-gly.md) do Kerberos (KDC) no controlador de domínio e obter um tíquete de concessão de TÍQUETE (TGT) usando os dados de logon fornecidos pelo usuário.

Se um KDC Kerberos não estiver disponível, o Windows usará \_ o MSV1 0 e a autenticação de passagem, conforme descrito no [pacote de autenticação do MSV1 \_ 0](msv1-0-authentication-package.md).

O pacote de autenticação Kerberos dá suporte à versão 5, revisão 6 do protocolo Kerberos. Esse protocolo é baseado no [RFC 4120](https://www.ietf.org/rfc/rfc4120.txt)da Internet. Para obter mais informações, consulte o site da IETF:

[https://www.ietf.org](https://www.ietf.org/)

Para obter mais informações sobre o Kerberos, consulte [Microsoft Kerberos](microsoft-kerberos.md).

## <a name="kerberos-credential-formats"></a>Formatos de credencial Kerberos

As [*credenciais*](../secgloss/c-gly.md) de usuário atribuídas pelo pacote de autenticação Kerberos após uma tentativa de logon bem-sucedida são um tíquete e uma chave de criptografia temporária, geralmente chamada de [*chave de sessão*](../secgloss/s-gly.md). O tíquete contém uma cópia criptografada das credenciais do cliente e da chave de sessão.

 

 
