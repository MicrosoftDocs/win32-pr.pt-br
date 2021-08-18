---
description: Explica como estabelecer um contexto de segurança que proteja as comunicações entre um cliente e um servidor.
ms.assetid: eb1eadb2-14b2-4265-994a-dcea4208e650
title: Criando um contexto de segurança Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7373d2ed4f8cc385a2245e6971f8233aad052930d4995225abfda8eab0191aaf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008854"
---
# <a name="creating-an-schannel-security-context"></a>Criando um contexto de segurança Schannel

Para estabelecer um [*contexto de segurança*](/windows/desktop/SecGloss/s-gly) que proteja as comunicações entre um cliente e um servidor, ambos devem participar do seguinte processo de troca de informações:

## <a name="client"></a>Cliente

1.  O cliente chama a [**função InitializeSecurityContext (Geral).**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta)
2.  O Schannel começa a criar um contexto de segurança de acordo com as regras do protocolo de segurança selecionado. O código de retorno da função indica se o cliente deve chamar a função novamente. [**InitializeSecurityContext (Geral)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) pode retornar um token que representa o contexto.
3.  Se um token tiver sido retornado, o cliente o enviará ao servidor.
4.  Quando [**InitializeSecurityContext (Geral)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) retorna SEC \_ E \_ OK, o cliente é feito. Se a função retornar SEC \_ I \_ CONTINUE \_ NEEDED, o cliente deverá aguardar o servidor enviar um token. Quando o cliente tiver o token do servidor, ele deverá chamar a **função InitializeSecurityContext (Geral)** [*novamente.*](/windows/desktop/SecGloss/c-gly) (Volte para a etapa 2.)

## <a name="server"></a>Servidor

1.  O servidor aguarda um cliente enviar uma mensagem que contém um token de segurança. O servidor passa o token recebido do cliente para a [**função AcceptSecurityContext (Geral).**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext)
2.  O Schannel se baseia no contexto de segurança parcial representado pelo token. O Schannel retorna um token para o servidor e um código de retorno que indica se o servidor deve chamar a função novamente.
3.  Se um token tiver sido retornado, o servidor o enviará ao cliente.
4.  Quando [**AcceptSecurityContext (Geral)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) retorna SEC \_ E \_ OK, o servidor é feito. Se a função retornar SEC \_ I \_ CONTINUE \_ NEEDED, o servidor deverá aguardar até que o cliente envie um token. Quando o servidor tiver o token do cliente, ele deverá chamar a **função AcceptSecurityContext (Geral)** novamente. (Volte para a etapa 2.)

Se uma das funções retornar um valor diferente de SEC E OK, SEC I CONTINUE NEEDED ou SEC E INCOMPLETE MESSAGE (consulte o parágrafo \_ \_ a \_ \_ \_ \_ \_ \_ seguir), ocorreu um erro. O cliente e o servidor devem chamar a [**função DeleteSecurityContext**](/windows/desktop/api/Sspi/nf-sspi-deletesecuritycontext) para excluir o contexto de segurança parcialmente estabelecido.

Um caso especial que pode alterar o processamento do cliente e do servidor é quando pouca ou muita informação é enviada para o cliente ou servidor de outra parte. No caso de pouca informação, ambas as funções retornam SEC \_ E \_ INCOMPLETE \_ MESSAGE. Para obter informações sobre como reconhecer e lidar com informações insuficientes ou em excesso, consulte [Buffers extras retornados pelo Schannel.](extra-buffers-returned-by-schannel.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Executando a autenticação usando o Schannel](performing-authentication-using-schannel.md)
</dt> <dt>

[Mapeamento de certificados](mapping-certificates.md)
</dt> <dt>

[Validando manualmente as credenciais do Schannel](manually-validating-schannel-credentials.md)
</dt> </dl>

 

 
