---
description: Depois de receber um desafio do servidor, o cliente cria a resposta de desafio de resumo chamando a função InitializeSecurityContext (Digest).
ms.assetid: b26b5676-a614-4017-a4e5-a5395292a667
title: Gerando a resposta de desafio de resumo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b577334348745425db23d3de41431ba4e37b7af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829768"
---
# <a name="generating-the-digest-challenge-response"></a>Gerando a resposta de desafio de resumo

Depois de receber um desafio do servidor, o cliente cria a resposta de desafio de resumo chamando a função [**InitializeSecurityContext (Digest)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) . Essa função gera uma impressão digital de [*hash*](/windows/desktop/SecGloss/h-gly) MD5 usando informações sobre o recurso e os dados solicitados do desafio e gera um token de segurança que representa um [*contexto de segurança*](/windows/desktop/SecGloss/s-gly)parcial. Para concluir a autenticação, o cliente deve retornar o token para o servidor que emitiu o desafio.

A tabela a seguir descreve os parâmetros da [*função*](/windows/desktop/SecGloss/c-gly) [**InitializeSecurityContext (Digest)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) e os valores a serem fornecidos ao construir uma resposta de desafio de resumo.



| Parâmetro                  | Descrição                                                                                                                                                                                               |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *fContextReq*<br/>   | Os atributos de contexto de segurança solicitados pelo cliente. Para obter mais informações, consulte requisitos de contexto de resposta de desafio Digest.<br/>                                                             |
| *pszTargetName*<br/> | HTTP: cadeia de caracteres terminada em nulo que especifica a URL de destino.<br/> SASL: cadeia de caracteres terminada em nulo que especifica o destino DNS/SPN.<br/>                                                         |
| *pInput*<br/>        | Buffers que contêm informações exigidas pelo SSP de resumo. Para obter mais informações, consulte [buffers de entrada para a resposta de desafio de resumo](input-buffers-for-the-digest-challenge-response.md).<br/> |
| *pfContextAttr*<br/> | Recebe os atributos com suporte do contexto de segurança retornado. Para obter mais informações, consulte requisitos de contexto de resposta de desafio Digest.<br/>                                                  |
| *pOutput*<br/>       | Endereço de um \_ buffer de tipo de token SECBUFFER que recebe um token de segurança para enviar de volta para o servidor.<br/>                                                                                           |



 

## <a name="digest-challenge-response-context-requirements"></a>Requisitos de contexto de resposta de desafio Digest

Os requisitos de contexto são sinalizadores que determinam:

-   Se Microsoft Digest funciona como um mecanismo SASL ou protocolo de autenticação HTTP.
-   A qualidade de proteção com suporte do [*contexto de segurança*](/windows/desktop/SecGloss/s-gly) compartilhado pelo cliente e servidor.

Por padrão, o Microsoft Digest funciona como um mecanismo SASL.

Os requisitos de contexto são especificados como sinalizadores passados para o parâmetro *fContextReq* da função [**InitializeSecurityContext**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) . Os sinalizadores afetam a qualidade de proteção do contexto de segurança, controlando a diretiva QoP na resposta de desafio.

Por padrão, a diretiva QoP é definida como "auth". Para gerar uma resposta de desafio que define QoP como "auth-int", deve ocorrer o seguinte:

1.  O desafio Digest deve ter uma diretiva QoP definida como "auth-int".
2.  O cliente deve especificar um ou mais dos seguintes sinalizadores:

    -   \_integridade do req do ISC \_
    -   \_detecção de \_ repetição de req do ISC \_
    -   \_detecção de \_ sequência de req do ISC \_

Somente para SASL: gere uma resposta de desafio com a diretiva QoP definida como "auth-conf" especificando o \_ \_ sinalizador confidenciality do ISC. Como esse sinalizador não é válido para autenticação HTTP, ele não pode ser usado com o \_ sinalizador http req do ISC \_ .

## <a name="verifying-the-quality-of-protection"></a>Verificando a qualidade da proteção

O cliente deve examinar os sinalizadores de atributos de contexto de segurança retornados no parâmetro *pfContextAttr* da função [**InitializeSecurityContext**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) . O cliente deve enviar a resposta de desafio para o servidor somente se a qualidade de proteção indicada pelos sinalizadores for suficiente para suas finalidades. Os sinalizadores relevantes podem ser qualquer combinação do seguinte:

-   integridade da ISC \_ RET \_
-   detecção de repetição da ISC \_ RET \_ \_
-   detecção de sequência do ISC \_ RET \_ \_
-   \_ \_ Confidencialidade da ISC (somente contextos SASL)

Para obter mais informações sobre a diretiva QoP, consulte [qualidade de proteção e codificações](quality-of-protection-and-ciphers.md).

Para obter mais informações sobre diretivas de resposta de desafio, consulte [conteúdo de uma resposta de desafio de resumo](contents-of-a-digest-challenge-response.md).

 

