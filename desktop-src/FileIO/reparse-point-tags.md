---
description: Cada ponto de nova análise tem uma marca de identificador para que você possa diferenciar com eficiência os diferentes tipos de pontos de nova análise, sem precisar examinar os dados definidos pelo usuário no ponto de nova análise.
ms.assetid: d02a2f50-d374-4149-bc04-49b7db052f62
title: Marcas de ponto de nova análise
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a53b65034347e2a2c07afcd6c1f03e31f73cef7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105756776"
---
# <a name="reparse-point-tags"></a>Marcas de ponto de nova análise

Cada ponto de nova análise tem uma marca de identificador para que você possa diferenciar com eficiência os diferentes tipos de pontos de nova análise, sem precisar examinar os dados definidos pelo usuário no ponto de nova análise. O sistema usa um conjunto de marcas predefinidas e um intervalo de marcas reservado para a Microsoft. Se você usar qualquer uma das marcas reservadas ao definir um ponto de nova análise, a operação falhará. As marcas não incluídas nesses intervalos não são reservadas e estão disponíveis para seu aplicativo.

Ao definir um ponto de nova análise, você deve marcar os dados a serem colocados no ponto de nova análise. Depois que o ponto de nova análise tiver sido estabelecido, um novo conjunto de operações falhará se a marca para os novos dados não corresponder à marca dos dados existentes. Se as marcas corresponderem, a operação set substituirá o ponto de nova análise existente.

Para recuperar a marca de ponto de nova análise, use a função [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea) . Se o membro **dwFileAttributes** incluir o atributo de **\_ \_ \_ ponto de nova análise de atributo de arquivo** , o membro **dwReserved0** especificará o ponto de nova análise.

## <a name="tag-contents"></a>Conteúdo da tag

As marcas de nova análise são armazenadas como valores **DWORD** . Os bits definem determinados atributos, conforme mostrado no diagrama a seguir.

``` syntax
   3 3 2 2 2 2 2 2 2 2 2 2 1 1 1 1 1 1 1 1 1 1
   1 0 9 8 7 6 5 4 3 2 1 0 9 8 7 6 5 4 3 2 1 0 9 8 7 6 5 4 3 2 1 0
  +-+-+-+-+-----------------------+-------------------------------+
  |M|R|N|R|     Reserved bits     |      Reparse tag value        |
  +-+-+-+-+-----------------------+-------------------------------+
```

Os baixos 16 bits determinam o tipo de ponto de nova análise. Os altos 16 bits têm 12 bits reservados para uso futuro e 4 bits que denotam atributos específicos das marcas e os dados representados pelo ponto de nova análise. A tabela a seguir descreve esses bits.



| bit | Descrição                                                                                                  |
|-----|--------------------------------------------------------------------------------------------------------------|
| M   | Microsoft de bits. Se esse bit estiver definido, a marca será de propriedade da Microsoft. Todas as outras marcas devem usar zero para este bit. |
| R   | Reservado deve ser zero para todas as marcas que não sejam da Microsoft.                                                           |
| N   | Bit alternativo de nome. Se esse bit for definido, o arquivo ou diretório representará outra entidade nomeada no sistema. |



 

As macros a seguir existem para auxiliar no teste de marcas:

-   [**IsReparseTagMicrosoft**](/windows/desktop/api/Winnt/nf-winnt-isreparsetagmicrosoft)
-   [**IsReparseTagNameSurrogate**](/windows/desktop/api/Winnt/nf-winnt-isreparsetagnamesurrogate)

Cada macro retornará um valor diferente de zero se o bit associado for definido.

A seguir estão os valores de marca de nova análise predefinidos da Microsoft; Eles são definidos em WinNT. h:

-   **IO_REPARSE_TAG_AF_UNIX**
-   **IO_REPARSE_TAG_APPEXECLINK**
-   **IO_REPARSE_TAG_CLOUD**
-   **IO_REPARSE_TAG_CLOUD_1**
-   **IO_REPARSE_TAG_CLOUD_2**
-   **IO_REPARSE_TAG_CLOUD_3**
-   **IO_REPARSE_TAG_CLOUD_4**
-   **IO_REPARSE_TAG_CLOUD_5**
-   **IO_REPARSE_TAG_CLOUD_6**
-   **IO_REPARSE_TAG_CLOUD_7**
-   **IO_REPARSE_TAG_CLOUD_8**
-   **IO_REPARSE_TAG_CLOUD_9**
-   **IO_REPARSE_TAG_CLOUD_A**
-   **IO_REPARSE_TAG_CLOUD_B**
-   **IO_REPARSE_TAG_CLOUD_C**
-   **IO_REPARSE_TAG_CLOUD_D**
-   **IO_REPARSE_TAG_CLOUD_E**
-   **IO_REPARSE_TAG_CLOUD_F**
-   **IO_REPARSE_TAG_CLOUD_MASK**
-   **IO_REPARSE_TAG_CSV**
-   **IO_REPARSE_TAG_DEDUP**
-   **IO_REPARSE_TAG_DFS**
-   **IO_REPARSE_TAG_DFSR**
-   **IO_REPARSE_TAG_FILE_PLACEHOLDER**
-   **IO_REPARSE_TAG_GLOBAL_REPARSE**
-   **IO_REPARSE_TAG_HSM**
-   **IO_REPARSE_TAG_HSM2**
-   **IO_REPARSE_TAG_MOUNT_POINT**
-   **IO_REPARSE_TAG_NFS**
-   **IO_REPARSE_TAG_ONEDRIVE**
-   **IO_REPARSE_TAG_PROJFS**
-   **IO_REPARSE_TAG_PROJFS_TOMBSTONE**
-   **IO_REPARSE_TAG_SIS**
-   **IO_REPARSE_TAG_STORAGE_SYNC**
-   **IO_REPARSE_TAG_SYMLINK**
-   **IO_REPARSE_TAG_UNHANDLED**
-   **IO_REPARSE_TAG_WCI**
-   **IO_REPARSE_TAG_WCI_1**
-   **IO_REPARSE_TAG_WCI_LINK**
-   **IO_REPARSE_TAG_WCI_LINK_1**
-   **IO_REPARSE_TAG_WCI_TOMBSTONE**
-   **IO_REPARSE_TAG_WIM**
-   **IO_REPARSE_TAG_WOF**

Para garantir a exclusividade das marcas, a Microsoft fornece um mecanismo para distribuir novas marcas. Para obter mais informações, consulte o [Kit de IFS (sistema de arquivos instalável)](https://www.microsoft.com/whdc/devtools/ifskit/reparse.mspx).

 

 



