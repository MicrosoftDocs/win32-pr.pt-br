---
title: Pacotes COM e de segurança
description: O Windows dá suporte ao NTLMSSP (Provedor de Suporte de Segurança do LAN Manager), ao protocolo de autenticação Kerberos v5 e ao pacote de segurança Schannel, que fornece os protocolos PCT 1.0, SSL 2.0, SSL 3.0 e TLS 1.0.
ms.assetid: a0c095a8-93b7-4350-aac6-a9a066cccffd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15ec80a1ea610725716da3640b6e38b2fd0f3282ce6ce778e632c6a5c8e72c8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048714"
---
# <a name="com-and-security-packages"></a>Pacotes COM e de segurança

O Windows dá suporte ao NTLMSSP (Provedor de Suporte de Segurança do LAN Manager), ao protocolo de autenticação Kerberos v5 e ao pacote de segurança Schannel, que fornece os protocolos PCT 1.0, SSL 2.0, SSL 3.0 e TLS 1.0. Também há suporte para o Snego, que verifica os pacotes de segurança disponíveis e seleciona o mais apropriado.

A tabela a seguir mostra os níveis de autenticação com suporte pelos vários pacotes de segurança.



| Autenticação de servidor/cliente                                                                                           | Suporte a pacotes de segurança                                         |
|------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| Nenhum dos dois pode obter o nome do outro.<br/>                                                                      | Nenhum<br/>                                                  |
| O cliente pode autenticar o servidor, mas não vice-versa.<br/>                                                 | SChannel<br/>                                              |
| O cliente não pode descobrir o servidor, mas o servidor pode obter a ID de usuário do cliente.<br/>                    | Ntlmssp<br/>                                               |
| Autenticação mútua: o cliente e o servidor podem saber o nome do outro, se a permissão for concedida.<br/> | NTLMSSP (localmente), protocolo Kerberos v5 e Schannel<br/> |



 

Para obter mais informações sobre esses pacotes de segurança, consulte os seguintes tópicos nesta seção:

-   [Ntlmssp](ntlmssp.md)
-   [Protocolo Kerberos v5](kerberos-v5-protocol.md)
-   [Schannel](schannel.md)
-   [Snego](snego.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Segurança em COM](security-in-com.md)
</dt> </dl>

 

 





