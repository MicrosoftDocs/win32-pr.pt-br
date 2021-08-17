---
description: O cliente deve enviar ao servidor uma resposta de desafio digest quando receber um desafio digest em resposta a uma solicitação de um recurso.
ms.assetid: a9a30255-a78a-41aa-9dfd-340902f4c550
title: Conteúdo de uma resposta de desafio digest
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af2a4fd199dfe9e97d69628adb0e6012bc4941929b9c1e96e00de8c42d53eba7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119141149"
---
# <a name="contents-of-a-digest-challenge-response"></a>Conteúdo de uma resposta de desafio digest

O cliente deve enviar ao servidor uma resposta de desafio digest quando receber um desafio digest em resposta a uma solicitação de um recurso. O cliente deve enviar a solicitação novamente, fornecendo um header de Autorização com a resposta de desafio. A tabela a seguir descreve as diretivas que comem uma resposta de desafio digest.



| Diretiva          | Descrição                                                                                                                                                                                                                |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nome de Usuário           | O nome da conta da [*entidade de segurança que*](/windows/desktop/SecGloss/s-gly) está solicitando o recurso.                                                                  |
| Realm              | O nome do domínio que contém a conta indicada pelo nome de usuário.                                                                                                                                                    |
| nonce              | O nonce recebido no desafio digest.                                                                                                                                                                                |
| uri                | O URI (Identificador de Recurso Universal) do recurso solicitado.                                                                                                                                                         |
| qop                | A [qualidade da proteção](quality-of-protection.md).                                                                                                                                                                    |
| Nc                 | A contagem de nonce. O número de vezes que o cliente enviou uma resposta de desafio usando o nonce. Para obter mais informações, consulte a diretiva nonce.                                                                              |
| cnonce             | Um valor codificado exclusivo gerado pelo cliente para cada resposta de desafio.                                                                                                                                                |
| resposta           | Um valor calculado de acordo com a especificação de Acesso Digest ([RFC 2617](https://www.ietf.org/rfc/rfc2617.txt)). Uma resposta precisa é a prova de que a senha do usuário é conhecida no lado do cliente. |
| algoritmo          | O algoritmo recebido no desafio Digest.                                                                                                                                                                            |
| Opaco             | O valor opaco recebido no desafio digest.                                                                                                                                                                         |
| (Somente SASL) codificação | Um dos valores de criptografia recebidos no desafio Digest. Para obter detalhes da criptografia, [consulte Qualidade de proteção e codificações.](quality-of-protection-and-ciphers.md)                                                             |



 

Microsoft Digest dá suporte aos seguintes formulários de nome de usuário/Realm:

-   Realm de nome de usuário
-   Domínio AccountName (simples)
-   UPN "" (em branco)
-   NetBIOS "" (em branco)

Embora os caracteres maiúsculas sejam compatíveis, para melhor desempenho que corresponde aos valores de hash digest pré-calculados do servidor, recomendamos o uso de caracteres minúsculos.

O uso de hashes pré-calculados é um novo recurso que permite que os operadores do sistema ignorem o uso de senhas criptografadas reversíveis no controlador de domínio. Um hash pré-calculado é formado para um usuário quando a senha do usuário é alterada.

Microsoft Digest gera a cadeia de caracteres de resposta de desafio digest para aplicativos cliente. Para obter detalhes, consulte [Gerando a resposta de desafio digest](generating-the-digest-challenge-response.md).

 

 
