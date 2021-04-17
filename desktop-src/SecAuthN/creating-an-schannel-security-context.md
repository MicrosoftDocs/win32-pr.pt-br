---
description: Explica como estabelecer um contexto de segurança que protege as comunicações entre um cliente e um servidor.
ms.assetid: eb1eadb2-14b2-4265-994a-dcea4208e650
title: Criando um contexto de segurança Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23e364e6319fbaddb50bffaf59541af9e8f43bfb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105748467"
---
# <a name="creating-an-schannel-security-context"></a>Criando um contexto de segurança Schannel

Para estabelecer um [*contexto de segurança*](/windows/desktop/SecGloss/s-gly) que protegerá as comunicações entre um cliente e um servidor, ambos devem participar do seguinte processo de troca de informações:

## <a name="client"></a>Cliente

1.  O cliente chama a função [**InitializeSecurityContext (geral)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) .
2.  O Schannel começa a criar um contexto de segurança de acordo com as regras do protocolo de segurança selecionado. O código de retorno da função indica se o cliente deve chamar a função novamente. [**InitializeSecurityContext (geral)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) pode retornar um token que representa o contexto.
3.  Se um token for retornado, o cliente o enviará ao servidor.
4.  Quando [**InitializeSecurityContext (geral)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) retorna s \_ E \_ OK, o cliente é concluído. Se a função retornar s \_ \_ , continuaria \_ necessário, o cliente deverá aguardar até que o servidor envie um token para ele. Quando o cliente tem o token do servidor, ele deve chamar a função **InitializeSecurityContext (geral)** [](/windows/desktop/SecGloss/c-gly) novamente. (Volte para a etapa 2.)

## <a name="server"></a>Servidor

1.  O servidor aguarda que um cliente envie uma mensagem que contém um token de segurança. O servidor passa o token recebido do cliente para a função [**AcceptSecurityContext (geral)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) .
2.  O Schannel se baseia no contexto de segurança parcial representado pelo token. O Schannel retorna um token para o servidor e um código de retorno que indica se o servidor deve chamar a função novamente.
3.  Se um token foi retornado, o servidor o envia para o cliente.
4.  Quando [**AcceptSecurityContext (geral)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) retorna s \_ E \_ OK, o servidor é concluído. Se a função retornar s \_ \_ , continuaria \_ necessário, o servidor deverá aguardar até que o cliente envie um token. Quando o servidor tem o token do cliente, ele deve chamar a função **AcceptSecurityContext (geral)** novamente. (Volte para a etapa 2.)

Se uma das funções retornar um valor diferente de s \_ e \_ OK, a opção s \_ \_ continuaria \_ necessária \_ ou \_ a mensagem s E incompleta \_ (consulte o parágrafo a seguir) ocorreu um erro. O cliente e o servidor devem chamar a função [**DeleteSecurityContext**](/windows/desktop/api/Sspi/nf-sspi-deletesecuritycontext) para excluir o contexto de segurança parcialmente estabelecido.

Um caso especial que pode alterar o processamento de cliente e servidor é quando muitas informações são enviadas para o cliente ou para o servidor da outra parte. No caso de poucas informações, ambas as funções retornam a \_ mensagem s E \_ incompletas \_ . Para obter informações sobre como reconhecer e manipular informações insuficientes ou em excesso, consulte [buffers extras retornados pelo Schannel](extra-buffers-returned-by-schannel.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Executando a autenticação usando Schannel](performing-authentication-using-schannel.md)
</dt> <dt>

[Mapeando certificados](mapping-certificates.md)
</dt> <dt>

[Validando manualmente as credenciais do Schannel](manually-validating-schannel-credentials.md)
</dt> </dl>

 

 
