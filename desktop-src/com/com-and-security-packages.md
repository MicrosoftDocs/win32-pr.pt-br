---
title: Pacotes de segurança e COM
description: O Windows dá suporte a NTLMSSP (provedor de suporte de segurança do LAN Manager), ao protocolo de autenticação Kerberos V5 e ao pacote de segurança Schannel, que fornece os protocolos PCT 1,0, SSL 2,0, SSL 3,0 e TLS 1,0.
ms.assetid: a0c095a8-93b7-4350-aac6-a9a066cccffd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6720ddd56869c5ce93ae70eb313fbe12c140b42
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105788757"
---
# <a name="com-and-security-packages"></a>Pacotes de segurança e COM

O Windows dá suporte a NTLMSSP (provedor de suporte de segurança do LAN Manager), ao protocolo de autenticação Kerberos V5 e ao pacote de segurança Schannel, que fornece os protocolos PCT 1,0, SSL 2,0, SSL 3,0 e TLS 1,0. Também há suporte para Snego, que verifica os pacotes de segurança disponíveis e seleciona o mais apropriado.

A tabela a seguir mostra os níveis de autenticação com suporte nos vários pacotes de segurança.



| Autenticação de servidor/cliente                                                                                           | Suporte ao pacote de segurança                                         |
|------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| Nem pode obter o nome do outro.<br/>                                                                      | Nenhum<br/>                                                  |
| O cliente pode autenticar o servidor, mas não vice-versa.<br/>                                                 | SChannel<br/>                                              |
| O cliente não pode descobrir o servidor, mas o servidor pode obter a ID de usuário do cliente.<br/>                    | NTLMSSP<br/>                                               |
| Autenticação mútua: o cliente e o servidor podem saber o nome do outro, se a permissão for concedida.<br/> | NTLMSSP (localmente), protocolo Kerberos V5 e Schannel<br/> |



 

Para obter mais informações sobre esses pacotes de segurança, consulte os seguintes tópicos nesta seção:

-   [NTLMSSP](ntlmssp.md)
-   [Protocolo Kerberos V5](kerberos-v5-protocol.md)
-   [Schannel](schannel.md)
-   [Snego](snego.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Segurança em COM](security-in-com.md)
</dt> </dl>

 

 





