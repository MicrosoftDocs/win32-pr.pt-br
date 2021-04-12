---
description: O cliente deve enviar ao servidor uma resposta de desafio de resumo quando recebe um desafio de resumo em resposta a uma solicitação de um recurso.
ms.assetid: a9a30255-a78a-41aa-9dfd-340902f4c550
title: Conteúdo de uma resposta de desafio de resumo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7168a7e6a468ecc7d573ef0bd853ec6db255b19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170027"
---
# <a name="contents-of-a-digest-challenge-response"></a>Conteúdo de uma resposta de desafio de resumo

O cliente deve enviar ao servidor uma resposta de desafio de resumo quando recebe um desafio de resumo em resposta a uma solicitação de um recurso. O cliente deve enviar a solicitação novamente, fornecendo um cabeçalho de autorização com a resposta de desafio. A tabela a seguir descreve as diretivas que compõem uma resposta de desafio resumida.



| Diretiva          | Descrição                                                                                                                                                                                                                |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nome de Usuário           | O nome da conta da [*entidade de segurança*](/windows/desktop/SecGloss/s-gly) que está solicitando o recurso.                                                                  |
| Realm              | O nome do domínio que contém a conta indicada pelo nome de usuário.                                                                                                                                                    |
| nonce              | O nonce recebido no desafio de resumo.                                                                                                                                                                                |
| uri                | O URI (identificador de recurso universal) do recurso solicitado.                                                                                                                                                         |
| qop                | A [qualidade da proteção](quality-of-protection.md).                                                                                                                                                                    |
| NC                 | A contagem de nonce. O número de vezes que o cliente enviou uma resposta de desafio usando o nonce. Para obter mais informações, consulte a diretiva nonce.                                                                              |
| cnonce             | Um valor codificado exclusivo gerado pelo cliente para cada resposta de desafio.                                                                                                                                                |
| resposta           | Um valor calculado de acordo com a especificação de acesso Digest ([RFC 2617](https://www.ietf.org/rfc/rfc2617.txt)). Uma resposta precisa é uma prova conclusiva de que a senha do usuário é conhecida no lado do cliente. |
| algoritmo          | O algoritmo recebido no desafio de resumo.                                                                                                                                                                            |
| opaco             | O valor opaco recebido no desafio de resumo.                                                                                                                                                                         |
| (SASL somente) Cipher | Um dos valores de codificação recebidos no desafio de resumo. Para obter detalhes de codificação, consulte [qualidade de proteção e codificações](quality-of-protection-and-ciphers.md).                                                             |



 

O Microsoft Digest dá suporte às seguintes formas de nome de usuário/realm:

-   Realm de nome de usuário
-   Domínio AccountName (simples)
-   UPN "" (em branco)
-   NetBIOS "" (em branco)

Embora haja suporte para caracteres maiúsculos, para melhor desempenho que atendam aos valores de hash de resumo precalculados do servidor, é recomendável usar caracteres minúsculos.

O uso de hashes pré-calculados é um novo recurso que permite que os operadores do sistema ignorem o uso de senhas criptografadas reversível no controlador de domínio. Um hash precalculado é formado para um usuário quando a senha do usuário é alterada.

Microsoft Digest gera a cadeia de caracteres de resposta de desafio Digest para aplicativos cliente. Para obter detalhes, consulte [gerando a resposta de desafio de resumo](generating-the-digest-challenge-response.md).

 

 
