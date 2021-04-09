---
description: A autenticação HTTP usando Microsoft Digest requer três buffers de entrada para gerar uma resposta de desafio. A tabela a seguir resume esses buffers.
ms.assetid: 0df02be2-f42e-46d0-a206-765adf3d7a72
title: Buffers de entrada para a resposta de desafio de resumo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 982923782b13e37a5e3531717dabf47016c60932
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089949"
---
# <a name="input-buffers-for-the-digest-challenge-response"></a>Buffers de entrada para a resposta de desafio de resumo

A autenticação HTTP usando Microsoft Digest requer três buffers de entrada para gerar uma resposta de desafio. A tabela a seguir resume esses buffers.



| Número do buffer | Contém                                                                                                                                             | Tipo de buffer                                                 |
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| 0             | Desafio recebido do servidor                                                                                                                   | \_token SECBUFFER                                            |
| 1             | Método HTTP                                                                                                                                          | parâmetros de SECBUFFER \_                                           |
| 2             | H (entidade)                                                                                                                                            | parâmetros de SECBUFFER \_                                           |
| 3             | O SPN ( [*nome da entidade de serviço*](../secgloss/s-gly.md) ) do servidor de destino. | **SECBUFFER \_ \_host de destino** \| **SECBUFFER \_ ReadOnly**      |
| 4             | Valores de token de associações de canal                                                                                                                        | **SECBUFFER \_ \_associações de canal** \| **SECBUFFER \_ ReadOnly** |



 

O buffer zero contém o desafio de resumo recebido do servidor em resposta à solicitação inicial para um recurso protegido por acesso.

O buffer 1 contém a representação de cadeia de caracteres do método, como "GET" ou "POST". O método é usado no cálculo de a2, conforme descrito em [RFC 2617](https://www.ietf.org/rfc/rfc2617.txt).

Buffer 2 é o hash [*MD5*](../secgloss/m-gly.md) do corpo da entidade da mensagem, conforme descrito em RFC 2617.

O buffer 3 contém o SPN do servidor de destino na formatação UTF-8 quando Digest é usado com associações de canal.

O buffer 4 contém o valor do token de associação de canal quando Digest é usado com associações de canal.

## <a name="input-buffers-for-sasl"></a>Buffers de entrada para SASL

Somente buffer de fornecimento zero. Para compatibilidade com outros SSPs, você pode chamar [**InitializeSecurityContext (Digest)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) sem um desafio de servidor válido. Nesse caso, o parâmetro *pInput* deve ser definido como **NULL**.

 

 
