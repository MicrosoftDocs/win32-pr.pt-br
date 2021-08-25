---
description: Um arquivo marcado como criptografado é criptografado pelo sistema de arquivos NTFS usando o driver de criptografia atual.
ms.assetid: 166bfb8c-b97d-4cc7-bf6b-399837cb8ad0
title: Manipulando arquivos e diretórios criptografados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf1a3a7b4a2d38aa2f4e012ccb96d01712f280879ff578afdb5c69392ab826a5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119927786"
---
# <a name="handling-encrypted-files-and-directories"></a>Manipulando arquivos e diretórios criptografados

Um programador ou usuário pode marcar um diretório ou arquivo como criptografado. Um arquivo marcado como criptografado é criptografado pelo sistema de arquivos NTFS usando o driver de criptografia atual. Se, em uma data posterior, o arquivo for marcado como não criptografado, ele será descriptografado e deixado em um estado de texto sem formatação (não seguro).

Os diretórios não são criptografados. Em vez disso, por padrão, em um diretório "criptografado", todos os arquivos novos no diretório são criptografados na criação. Um usuário deve alterar especificamente o status de um novo arquivo para descriptografado se o usuário não quiser que o arquivo seja criptografado. Um diretório criptografado está visível. Para tornar um diretório inacessível para outros usuários, use os métodos padrão de controle de acesso.

As funções de criptografia não podem ser usadas com a [API de backup](/windows/desktop/Backup/backup).

Para criptografar um novo arquivo, use a função [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) com o sinalizador **\_ \_ criptografado atributo de arquivo** . Para criptografar um arquivo existente, use a função [**EncryptFile**](/windows/desktop/api/WinBase/nf-winbase-encryptfilea) . Todos os fluxos de dados no arquivo são criptografados. Se o arquivo já estiver criptografado, o **EncryptFile** não fará nada, mas retornará um valor diferente de zero, que indica êxito. Se o arquivo estiver compactado, o **EncryptFile** descompacta o arquivo antes de criptografá-lo.

Para descriptografar um arquivo criptografado, use a função [**DecryptFile**](/windows/desktop/api/WinBase/nf-winbase-decryptfilea) . Se o arquivo não estiver criptografado, **descriptografafile** não fará nada, mas retornará um valor diferente de zero indicando êxito.

A função [**EncryptionDisable**](/windows/desktop/api/WinEfs/nf-winefs-encryptiondisable) desabilita ou habilita a criptografia do diretório indicado e os arquivos contidos nele. Ele não afeta a criptografia de subdiretórios abaixo do diretório indicado.

Para recuperar o status de criptografia de um arquivo, use a função [**FileEncryptionStatus**](/windows/desktop/api/WinBase/nf-winbase-fileencryptionstatusa) . Como alternativa, chame a função [**GetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa) e examine o **sinalizador \_ \_ criptografado atributo de arquivo** no valor de retorno.

[**CopyFile**](/windows/desktop/api/WinBase/nf-winbase-copyfile) e [**CopyFileEx**](/windows/desktop/api/WinBase/nf-winbase-copyfileexa) tentam criptografar o arquivo de destino com as chaves usadas na criptografia do arquivo de origem. Se isso não puder ser feito, ambas as funções tentarão criptografar o arquivo de destino com chaves padrão. Se ambos os métodos não puderem ser feitos, **CopyFile** e **CopyFileEx** falharão com um erro de **\_ \_ falha na criptografia de erro** . Se você quiser que o **CopyFileEx** conclua a operação de cópia mesmo quando o arquivo de destino não puder ser criptografado, inclua o sinalizador de **\_ destino copiar arquivo \_ permitir \_ descriptografado \_** no valor do parâmetro *dwCopyFlags* em sua chamada para **CopyFileEx**.

 

 
