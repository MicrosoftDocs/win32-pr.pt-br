---
description: Um aplicativo que usa uma autoridade de backup para armazenar chaves de sessão geralmente segue estas etapas.
ms.assetid: 859310ed-6000-44c8-92f7-974326ce0fc9
title: Armazenando chaves de sessão usando uma autoridade de backup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d59906874f384d4eed9e20d6a781b14e3feba313
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104296794"
---
# <a name="storing-session-keys-using-a-backup-authority"></a>Armazenando chaves de sessão usando uma autoridade de backup

Um aplicativo que usa uma [*autoridade de backup*](../secgloss/b-gly.md) para armazenar chaves de sessão geralmente segue estas etapas.

**Para usar uma autoridade de backup**

1.  Criptografe o arquivo como de costume.
2.  Exporte a [*chave de sessão*](../secgloss/s-gly.md) usada para criptografar o arquivo em um blob de [*chave simples*](../secgloss/s-gly.md), especificando que sua própria [*chave pública de troca de chave*](../secgloss/k-gly.md) seja usada para criptografar o blob de chave. Armazene esse BLOB de chave com o arquivo criptografado.
3.  Exporte a chave de sessão novamente, desta vez especificando que a chave pública da autoridade de backup seja usada para criptografar o BLOB de chave. Envie esse BLOB de chave para a autoridade de backup, junto com a descrição da chave, o número de série e assim por diante.

Se um [*par de chaves*](../secgloss/k-gly.md) for perdido, as chaves poderão ser recuperadas da [*autoridade de backup*](../secgloss/b-gly.md) se a identidade do proprietário das chaves puder ser estabelecida. O procedimento para estabelecer a identidade é determinado pela política da autoridade de backup específica e não envolve o CryptoAPI.

Para o código necessário para criar uma chave de sessão e exportar essa chave para um [*blob de chave simples*](../secgloss/s-gly.md) que pode ser gravado em um arquivo de disco, consulte [o programa de exemplo C: exportando uma chave de sessão](example-c-program-exporting-a-session-key.md).

 

 
