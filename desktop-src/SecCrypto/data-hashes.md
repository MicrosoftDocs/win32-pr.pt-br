---
description: Um hash de um texto ou outra cadeia de caracteres de bytes é um valor de comprimento fixo associado, estatisticamente exclusivo.
ms.assetid: e54d5a3b-cae1-47dd-a565-7bf1ccef7f52
title: Hashes de dados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2a998c2172f6bd3b48bb3cdc94f1ed2207384606950dd9d6e8b6f3152149eaf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117767764"
---
# <a name="data-hashes"></a>Hashes de dados

Um [*hash*](../secgloss/h-gly.md) de um texto ou outra cadeia de caracteres de bytes é um valor de comprimento fixo associado, estatisticamente exclusivo. Em alguns documentos, um *hash* de um texto também é chamado de resumo; no entanto, nesta documentação o termo hash sempre será usado. As funções de CryptoAPI fornecem um meio para criar um hash para qualquer texto ou outra cadeia de caracteres de bytes. Esse hash, em seguida, pode ser usado como um identificador exclusivo de seus dados associados.

Para garantir a [*integridade*](../secgloss/i-gly.md) de um texto, um [*hash*](../secgloss/h-gly.md) de um texto pode ser enviado para acompanhar o texto. O receptor pode então calcular um hash nos dados recebidos e comparar o hash calculado com o hash recebido. Se as duas corresponderem, os dados recebidos deverão ser iguais aos dados dos quais o hash recebido foi criado.

Para obter um valor de hash, crie um objeto de hash usando [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash). Esse objeto acumulará os dados a serem verificados. Os dados são então adicionados ao objeto de hash com a função [**CryptHashData**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata) .

Depois que o último bloco de dados é adicionado ao hash, a função [**CryptGetHashParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgethashparam) é usada para obter o valor de hash dos dados.

É fornecida mais segurança ao destruir o objeto de hash com [**CryptDestroyHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroyhash) assim que o valor de hash tiver sido obtido.

 

 
