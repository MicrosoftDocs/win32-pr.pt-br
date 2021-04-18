---
description: Explica o procedimento usado para armazenar uma chave de sessão.
ms.assetid: 9ab7f747-9c69-40b5-af78-163f3ba315bf
title: Armazenando uma chave de sessão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3b17de657ddba47dd77f68c1ee7a2adfdf93e7f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105789490"
---
# <a name="storing-a-session-key"></a>Armazenando uma chave de sessão

> [!Note]  
> Esta seção pressupõe que os usuários possuam um conjunto de [*pares de chaves públicas/privadas*](../secgloss/p-gly.md). As instruções e um exemplo para a criação de pares de chaves podem ser encontrados no [programa C de exemplo: Criando um contêiner de chave e gerando chaves](example-c-program-creating-a-key-container-and-generating-keys.md).

 

**Para armazenar uma chave de sessão**

1.  Crie um [*blob de chave*](../secgloss/k-gly.md) simples usando a função [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) . Isso transferirá a chave de sessão do CSP para o espaço de memória de um aplicativo. Especifique que uma chave pública do Exchange seja usada para assinar o BLOB de chave.
2.  Armazene o BLOB de chave assinado em disco. Supõe-se que todos os discos não sejam seguros.
3.  Quando a chave for necessária, leia o BLOB de chave do disco.
4.  Importe o BLOB de chave de volta para o CSP usando a função [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey) .

Para obter um exemplo de como criar uma [*chave de sessão*](../secgloss/s-gly.md) e exportar essa chave para um [*blob de chave simples*](../secgloss/s-gly.md) que pode ser gravado em um arquivo de disco, consulte [o programa de exemplo C: exportando uma chave de sessão](example-c-program-exporting-a-session-key.md).

Este procedimento fornece apenas a segurança mínima. Se a chave de sessão armazenada for usada para criptografar dados em uma data posterior, o procedimento anterior não fornecerá segurança adequada.

Para fornecer maior segurança, assine o BLOB de chave com uma chave privada do Exchange antes de armazená-lo no disco. Quando o BLOB de chave é lido posteriormente do disco, sua assinatura pode ser validada para garantir que o BLOB de chave esteja intacto.

Se o BLOB de chave não for assinado, qualquer pessoa com acesso ao disco ou outra mídia na qual a chave é armazenada poderá criar uma nova chave de sessão.

A nova chave de sessão pode ser criptografada com a [*chave de troca*](../secgloss/e-gly.md)de [*chave pública*](../secgloss/p-gly.md) do usuário original e essa nova chave pode ser substituída pelo original. Se o usuário utilizou inadvertidamente a chave de sessão substituída para criptografar arquivos e mensagens, o indivíduo que criou a chave substituta poderia descriptografá-los facilmente.

As assinaturas digitais são discutidas em detalhes em [hashes e assinaturas digitais](hashes-and-digital-signatures.md).

 

 
