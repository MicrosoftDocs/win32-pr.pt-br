---
description: Contém definições de termos de segurança que começam com a letra I.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: af511aed-88f5-4b12-ad44-317925297f70
title: I (Glossário de segurança)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1d3e727128c2494f313bdffc879b5c5e47a28ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011360"
---
# <a name="i-security-glossary"></a>I (Glossário de segurança)

[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) F [G](g-gly.md) [H](h-gly.md) i J [K](k-gly.md) [L](l-gly.md) [M](m-gly.md) [N](n-gly.md) [O](o-gly.md) [P](p-gly.md) Q [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z

<dl> <dt>

<span id="_security_iis_gly"></span><span id="_SECURITY_IIS_GLY"></span>**IIS**
</dt> <dd>

Serviços de software que dão suporte à criação, configuração e gerenciamento de sites, juntamente com outras funções de Internet. Os Serviços de Informações da Internet incluem o protocolo NNTP (rede de transferência de notícias), o protocolo FTP (FTP) e o protocolo SMTP. O IIS incorpora várias funções de segurança, permite aplicativos CGI e fornece servidores de Gopher e FTP.

</dd> <dt>

<span id="_security_impersonation_gly"></span><span id="_SECURITY_IMPERSONATION_GLY"></span>**representação**
</dt> <dd>

Um mecanismo que permite a execução de um processo do servidor usando as credenciais de segurança do cliente ou outro usuário usando as credenciais. Quando o servidor está representando o cliente, todas as operações executadas pelo servidor são executadas usando as credenciais do cliente (representando o usuário). A representação não permite que o servidor acesse recursos remotos em nome do cliente. Isso requer delegação.

</dd> <dt>

<span id="_security_impersonation_token_gly"></span><span id="_SECURITY_IMPERSONATION_TOKEN_GLY"></span>**token de representação**
</dt> <dd>

Um token de acesso que foi criado para capturar as informações de segurança de um processo de cliente, permitindo que um servidor "represente" o processo do cliente em operações de segurança.

Consulte também [*token de acesso*](a-gly.md) e [*token primário*](p-gly.md).

</dd> <dt>

<span id="_security_initialization_vector_gly"></span><span id="_SECURITY_INITIALIZATION_VECTOR_GLY"></span>**vetor de inicialização**
</dt> <dd>

(IV) uma sequência de bytes aleatórios acrescentados à frente do texto não criptografado antes da criptografia por uma codificação de bloco. Adicionar o vetor de inicialização ao início do texto não criptografado elimina a possibilidade de que o texto cifrado inicial seja o mesmo para duas mensagens. Por exemplo, se as mensagens são sempre iniciadas com um cabeçalho comum (um timbre ou uma linha "de"), seu texto cifrado inicial sempre será o mesmo, supondo que o mesmo algoritmo criptográfico e a chave simétrica foram usados. A adição de um vetor de inicialização aleatório elimina isso de acontecer.

</dd> <dt>

<span id="_security_inner_data_gly"></span><span id="_SECURITY_INNER_DATA_GLY"></span>**dados internos**
</dt> <dd>

Todos os dados codificados usados como a mensagem para outra mensagem codificada. Por exemplo, uma mensagem envelopada e seu valor de hash podem ser os dados internos de uma segunda mensagem.

</dd> <dt>

<span id="_security_inner_content_gly"></span><span id="_SECURITY_INNER_CONTENT_GLY"></span>**conteúdo interno**
</dt> <dd>

Dados aprimorados, como com uma assinatura digital. Esse termo é usado principalmente ao discutir dados aprimorados em uma \# mensagem PKCS 7.

</dd> <dt>

<span id="_security_integrity_gly"></span><span id="_SECURITY_INTEGRITY_GLY"></span>**verifica**
</dt> <dd>

A integridade e a precisão de uma mensagem após ela ser enviada ou armazenada.

</dd> <dt>

<span id="_security_integrity_sid_gly"></span><span id="_SECURITY_INTEGRITY_SID_GLY"></span>**SID de integridade**
</dt> <dd>

Um SID ( [*identificador de segurança*](s-gly.md) ) que representa um nível de integridade. Um SID de integridade na SACL ( [*lista de controle de acesso do sistema*](s-gly.md) ) do descritor de segurança de um objeto especifica o nível de integridade do objeto. Os SIDs de integridade em um token de acesso especificam o nível de integridade do token.

</dd> <dt>

<span id="_security_interrupt_request_level_gly"></span><span id="_SECURITY_INTERRUPT_REQUEST_LEVEL_GLY"></span>**IRQL**
</dt> <dd>

Um IRQL (nível de solicitação de interrupção) define a prioridade de hardware na qual um processador opera em um determinado momento. Na Windows Driver Model, um thread em execução em um IRQL baixo pode ser interrompido para executar o código em um IRQL mais alto.

</dd> <dt>

<span id="_security_iv_gly"></span><span id="_SECURITY_IV_GLY"></span>**IV**
</dt> <dd>

Consulte *vetor de inicialização*.

</dd> </dl>

 

 



