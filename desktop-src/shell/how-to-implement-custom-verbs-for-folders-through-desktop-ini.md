---
description: No Windows 7 e posterior, você pode adicionar verbos a uma pasta usando Desktop.ini. Para obter mais informações sobre Desktop.ini arquivos, consulte Como Personalizar pastas com Desktop.ini.
ms.assetid: F03AB35D-FBFE-46C2-A37F-F70C18219B9A
title: Como implementar verbos personalizados para pastas por meio de Desktop.ini
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 133726133abe884863a0b4d2abc0cc76aab1310a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967899"
---
# <a name="how-to-implement-custom-verbs-for-folders-through-desktopini"></a>Como implementar verbos personalizados para pastas por meio de Desktop.ini

No Windows 7 e posterior, você pode adicionar verbos a uma pasta usando Desktop.ini. Para obter mais informações sobre Desktop.ini arquivos, consulte [como personalizar pastas com Desktop.ini](how-to-customize-folders-with-desktop-ini.md).

> [!Note]  
> Desktop.ini arquivos devem ser sempre marcados como ocultos do **sistema** para que  +   não sejam exibidos aos usuários.

 

Para adicionar verbos personalizados para pastas por meio de um arquivo Desktop.ini, execute as etapas a seguir.

## <a name="instructions"></a>Instruções

### <a name="step-1"></a>Etapa 1:

Crie uma pasta que esteja marcada como **somente leitura** ou **sistema**.

### <a name="step-2"></a>Etapa 2:

Crie um arquivo de Desktop.ini que inclui um \[ . ShellClassInfo \] DirectoryClass = ProgID da pasta.

### <a name="step-3"></a>Etapa 3:

No registro, crie o ProgID de pasta **\_ \_ raiz de classes hKey** \\  com um valor de CanUseForDirectory. O valor CanUseForDirectory evita o uso indevido de ProgIDs que estão definidos para não participar da implementação de verbos personalizados para pastas por meio de Desktop.ini.

### <a name="step-4"></a>Etapa 4:

Adicione verbos na subchave ProgID da **pasta** , por exemplo:

```
HKEY_CLASSES_ROOT
   CustomFolderType
      Shell
         MyVerb
            command
               (Default) = %SystemRoot%\system32\notepad.exe %1\desktop.ini
```

## <a name="remarks"></a>Comentários

> [!Note]  
> Esses verbos podem ser os verbos padrão; nesse caso, clicar duas vezes na pasta ativa o verbo.

 

 

 



