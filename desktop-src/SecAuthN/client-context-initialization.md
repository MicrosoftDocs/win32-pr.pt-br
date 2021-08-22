---
description: Inicialização de contexto do cliente
ms.assetid: 0c8aad3e-e726-49ce-8fc9-94dbd60cc5cb
title: Inicialização de contexto do cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0c0f2912de57487c1f30fdac1ef40740553947b993ef6f5179a028625f132af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119141179"
---
# <a name="client-context-initialization"></a>Inicialização de contexto do cliente

Para estabelecer uma conexão segura, o [](/windows/desktop/SecGloss/c-gly) cliente adquire um lidar com credenciais de saída antes de enviar uma solicitação de autenticação para o servidor. O servidor cria um contexto de segurança para o cliente da solicitação de autenticação. Há duas funções SSPI do lado do cliente envolvidas na configuração de autenticação:

-   [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) obtém uma referência às credenciais de logon [*obtidas anteriormente.*](/windows/desktop/SecGloss/c-gly)
-   [**InitializeSecurityContext (Geral)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) cria os tokens de segurança da solicitação de autenticação inicial.

O código para esse processo pode ser visto na **função GenClientContext** em [Using SSPI](using-sspi-with-a-windows-sockets-client.md)with a Windows Sockets Client .

Se um programa cliente precisar usar credenciais além de suas próprias credenciais de logon, como um nome de usuário diferente, nome de domínio e senha, ele as fornece na [**chamada AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) com uma estrutura DE IDENTIDADE [**\_ WINNT \_ AUTH \_**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) da SEC especificando as credenciais adicionais. Para obter mais informações sobre funções de credenciais, consulte [Gerenciamento de credenciais.](authentication-functions.md)

> [!Note]  
> O **membro Flags** da estrutura DE IDENTIDADE DE [**\_ \_ AUTH \_**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) DO WINNT SEC pode ser definido como SEC \_ WINNT AUTH IDENTITY ANSI quando as cadeias de caracteres na estrutura são \_ \_ \_ ASCI ou OEM. As cadeias de caracteres ANSI podem ser usadas com o membro Flags da estrutura DE IDENTIDADE DE **\_ \_ AUTH \_** DO WINNT DA SEC definida como SEC WINNT AUTH IDENTITY UNICODE se eles são **convertidos** primeiro em Unicode usando a \_ função \_ \_ \_ [**MultiByteToWideChar.**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) [](/windows/desktop/SecGloss/u-gly)

 

Para iniciar a primeira etapa da autenticação, o cliente chama [**InitializeSecurityContext (Geral)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) para obter um token de segurança inicial a ser enviado em uma mensagem de solicitação de conexão para o servidor.

O cliente usa as informações de token de segurança recebidas no descritor de buffer de saída para gerar uma mensagem a ser enviada ao servidor. A construção da mensagem, em termos de posicionamento de vários buffers e assim por diante, faz parte do protocolo do aplicativo e deve ser compreendida por ambas as partes. [](/windows/desktop/SecGloss/a-gly)

O cliente verifica o status de retorno de [**InitializeSecurityContext (Geral)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) para ver se a autenticação será concluída em uma única chamada. Um status de retorno de SEC \_ I CONTINUE NEEDED indica que o protocolo de segurança requer várias mensagens de \_ \_ autenticação. Para obter mais informações sobre funções de contexto, consulte [Gerenciamento de contexto.](authentication-functions.md)

 

 
