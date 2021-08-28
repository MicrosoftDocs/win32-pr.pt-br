---
description: O EFS (sistema de arquivos criptografados) fornece proteção criptográfica de arquivos individuais em volumes do sistema de arquivos NTFS usando um sistema de chave pública.
ms.assetid: 5f20109f-727d-44a9-90a1-0adc19b00d28
title: Criptografia de Arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61dbbfa82024bea13eab9e672b482ea18bc1051cd6e86b97d2a405351e3b078b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120107566"
---
# <a name="file-encryption"></a>Criptografia de Arquivo

O sistema de arquivos criptografados, ou EFS, fornece um nível adicional de segurança para arquivos e diretórios. Ele fornece proteção criptográfica de arquivos individuais em volumes do sistema de arquivos NTFS usando um sistema de chave pública.

normalmente, o controle de acesso aos objetos de arquivo e diretório fornecidos pelo modelo de segurança Windows é suficiente para proteger o acesso não autorizado a informações confidenciais. No entanto, se um laptop que contém dados confidenciais for perdido ou roubado, a proteção de segurança desses dados poderá ser comprometida. A criptografia dos arquivos aumenta a segurança.

Para determinar se um sistema de arquivos dá suporte à criptografia de arquivo para arquivos e diretórios, chame a função [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) e examine o sinalizador de bit de **\_ \_ criptografia de arquivo FS** . Observe que os seguintes itens não podem ser criptografados:

-   Arquivos compactados
-   Arquivos do sistema
-   Diretórios do sistema
-   Diretórios raiz
-   Transactions

Arquivos esparsos podem ser criptografados.

O TxF não oferece suporte à maioria das operações em arquivos EFS (sistema de arquivos criptografados). O único Operations TxF dá suporte a operações de leitura, como [**ReadEncryptedFileRaw**](/windows/desktop/api/WinBase/nf-winbase-readencryptedfileraw).

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                               | Descrição                                                                                                                                                              |
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Manipulando arquivos e diretórios criptografados](handling-encrypted-files-and-directories.md)<br/> | Um arquivo marcado como criptografado é criptografado pelo sistema de arquivos NTFS usando o driver de criptografia atual.<br/>                                                          |
| [Arquivos criptografados e chaves de usuário](encrypted-files-and-user-keys.md)<br/>                       | Lista as funções a serem usadas para criar uma nova chave, adicionar uma chave a um arquivo criptografado, consultar as chaves de um arquivo criptografado e remover chaves de um arquivo criptografado.<br/> |
| [Backup e restauração de arquivos criptografados](backup-and-restore-of-encrypted-files.md)<br/>       | As funções de criptografia brutas permitem o backup de arquivos criptografados.<br/>                                                                                                |



 

Para obter mais informações sobre criptografia, consulte [adicionando usuários a um arquivo criptografado](adding-users-to-an-encrypted-file.md).

Para obter mais informações sobre criptografia, consulte [criptografia](/windows/desktop/SecCrypto/cryptography-portal).

 

