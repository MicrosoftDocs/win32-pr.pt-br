---
title: NTLMSSP
description: NTLMSSP
ms.assetid: ae434165-4429-4ef0-b083-60abdfc50de0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 706c788f103d3d616b5a3087522b5f06b417e972
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "105788922"
---
# <a name="ntlmssp"></a>NTLMSSP

NTLMSSP, cujo identificador de serviço de autenticação é RPC \_ C \_ Authn \_ WinNT, é um provedor de suporte de segurança que está disponível em todas as versões do DCOM. Ele usa o protocolo NTLM para autenticação. O NTLM nunca transmite realmente a senha do usuário para o servidor durante a autenticação. Portanto, o servidor não pode usar a senha durante a representação para acessar os recursos de rede aos quais o usuário teria acesso. Somente recursos locais podem ser acessados.

O NTLM funciona tanto localmente quanto entre computadores. Ou seja, se o cliente e o servidor estiverem em computadores diferentes, o NTLM ainda poderá garantir que o cliente seja quem alega ser.

Com o NTLM, a identidade do cliente é representada por um nome de domínio, nome de usuário e senha ou token. Quando um servidor chama [**CoQueryClientBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryclientblanket), o nome de domínio e o nome de usuário do cliente são retornados. No entanto, quando um servidor chama [**CoImpersonateClient**](/windows/desktop/api/combaseapi/nf-combaseapi-coimpersonateclient), o token do cliente é retornado. Se não houver nenhuma relação de confiança entre o cliente e o servidor e se o servidor tiver uma conta local com o mesmo nome e senha que o cliente, essa conta será usada para representar o cliente.

O NTLM dá suporte à autenticação mútua entre threads e processos cruzados (somente localmente). Se o cliente especificar o nome da entidade de segurança do servidor no formato \\ usuário do domínio em uma chamada para [**IClientSecurity:: setampla**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket), a identidade do servidor deverá corresponder ao nome principal ou a chamada falhará. Se o cliente especificar **NULL**, a identidade do servidor não será verificada.

O NTLM adicionalmente dá suporte ao nível de representação entre threads e processos cruzados (somente localmente).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Pacotes de segurança e COM](com-and-security-packages.md)
</dt> </dl>

 

 