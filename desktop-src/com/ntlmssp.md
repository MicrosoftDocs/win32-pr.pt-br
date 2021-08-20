---
title: Ntlmssp
description: Ntlmssp
ms.assetid: ae434165-4429-4ef0-b083-60abdfc50de0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e786a586810a7404f242c9a129cbfccc03849a50f7ea6625288c7334e47e8787
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118105293"
---
# <a name="ntlmssp"></a>Ntlmssp

NTLMSSP, cujo identificador de serviço de autenticação é RPC C AUTHN WINNT, é um provedor de suporte de segurança que está disponível em todas as \_ \_ \_ versões do DCOM. Ele usa o protocolo NTLM para autenticação. O NTLM nunca transmite a senha do usuário para o servidor durante a autenticação. Portanto, o servidor não pode usar a senha durante a representação para acessar recursos de rede aos que o usuário teria acesso. Somente recursos locais podem ser acessados.

O NTLM funciona localmente e entre computadores. Ou seja, se o cliente e o servidor estão em computadores diferentes, o NTLM ainda poderá garantir que o cliente seja quem ele declara ser.

Com o NTLM, a identidade do cliente é representada por um nome de domínio, nome de usuário e uma senha ou token. Quando um servidor chama [**CoQueryClientBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryclientblanket), o nome de domínio e o nome de usuário do cliente são retornados. No entanto, quando um servidor chama [**CoImpersonateClient**](/windows/desktop/api/combaseapi/nf-combaseapi-coimpersonateclient), o token do cliente é retornado. Se não houver nenhuma relação de confiança entre o cliente e o servidor e se o servidor tiver uma conta local com o mesmo nome e senha que o cliente, essa conta será usada para representar o cliente.

O NTLM dá suporte à autenticação mútua entre threads e processos cruzados (somente localmente). Se o cliente especificar o nome principal do servidor no formulário de usuário de domínio em uma chamada \\ para [**IClientSecurity::SetBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket), a identidade do servidor deverá corresponder ao nome da entidade de segurança ou a chamada falhará. Se o cliente especificar **NULL,** a identidade do servidor não será verificada.

O NTLM também dá suporte ao nível de representação de delegado entre threads e processos cruzados (somente localmente).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Pacotes COM e de segurança](com-and-security-packages.md)
</dt> </dl>

 

 