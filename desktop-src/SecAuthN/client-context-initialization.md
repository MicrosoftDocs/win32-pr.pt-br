---
description: Inicialização do contexto do cliente
ms.assetid: 0c8aad3e-e726-49ce-8fc9-94dbd60cc5cb
title: Inicialização do contexto do cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 615ce5c157371f1ebfec685d6227bd11a1d76531
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091328"
---
# <a name="client-context-initialization"></a>Inicialização do contexto do cliente

Para estabelecer uma conexão segura, o cliente adquire um identificador de [*credenciais*](/windows/desktop/SecGloss/c-gly) de saída antes de enviar uma solicitação de autenticação para o servidor. O servidor cria um contexto de segurança para o cliente a partir da solicitação de autenticação. Há duas funções SSPI do lado do cliente envolvidas na configuração de autenticação:

-   [**Falha AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) Obtém uma referência às [*credenciais*](/windows/desktop/SecGloss/c-gly)de logon obtidas anteriormente.
-   [**InitializeSecurityContext (geral)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) cria os tokens de segurança de solicitação de autenticação inicial.

O código para esse processo pode ser visto na função **GenClientContext** no [uso de SSPI com um cliente do Windows Sockets](using-sspi-with-a-windows-sockets-client.md).

Se um programa cliente precisar usar credenciais além de suas próprias credenciais de logon, como um nome de usuário diferente, um nome de domínio e uma senha, ele as fornecerá na chamada [**falha AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) com uma estrutura de [**\_ \_ \_ identidade de autenticação WinNT SEC**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) especificando as credenciais adicionais. Para obter mais informações sobre as funções de credenciais, consulte [Gerenciamento de credenciais](authentication-functions.md).

> [!Note]  
> O membro **flags** da estrutura [**de \_ \_ \_ identidade de autenticação do Winnt da SEC**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) pode ser definido como SEC de identidade de autenticação do \_ WinNT \_ \_ \_ ANSI quando as cadeias de caracteres na estrutura são asci ou OEM. As cadeias de caracteres ANSI podem ser usadas com o membro **flags** da estrutura de identidade de autenticação do Winnt da SEC definida como SEC identidade de autenticação do **\_ \_ \_** \_ WinNT \_ \_ \_ Unicode, se elas forem convertidas primeiro em [*Unicode*](/windows/desktop/SecGloss/u-gly) usando a função [**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) .

 

Para iniciar o primeiro segmento da autenticação, o cliente chama [**InitializeSecurityContext (geral)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) para obter um token de segurança inicial a ser enviado em uma mensagem de solicitação de conexão para o servidor.

O cliente usa as informações de token de segurança recebidas no descritor de buffer de saída para gerar uma mensagem a ser enviada ao servidor. A construção da mensagem, em termos de posicionamento de vários buffers e assim por diante, faz parte do [*protocolo de aplicativo*](/windows/desktop/SecGloss/a-gly) e deve ser compreendida por ambas as partes.

O cliente verifica o status de retorno de [**InitializeSecurityContext (geral)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) para ver se a autenticação será concluída em uma única chamada. Um status de retorno de s \_ I \_ continue \_ necessário indica que o protocolo de segurança requer várias mensagens de autenticação. Para obter mais informações sobre funções de contexto, consulte [Gerenciamento de contexto](authentication-functions.md).

 

 
