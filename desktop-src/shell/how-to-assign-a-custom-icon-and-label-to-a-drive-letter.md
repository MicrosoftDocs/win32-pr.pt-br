---
description: Especifique um ícone e um rótulo personalizados para uma unidade.
ms.assetid: B6EF7F84-7747-4689-B740-A91CA8E394D7
title: Atribuir um ícone e um rótulo personalizados a uma letra da unidade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 848c076db443c502a667d67e0b7b49ce51db4ce6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967920"
---
# <a name="how-to-assign-a-custom-icon-and-label-to-a-drive-letter"></a>Como atribuir um ícone e um rótulo personalizados a uma letra da unidade

Especifique um ícone e um rótulo personalizados para uma unidade.

## <a name="instructions"></a>Instruções

### <a name="step-1-replacing-the-standard-drive-icon-with-a-custom-icon-in-windows-2000"></a>Etapa 1: substituindo o ícone de unidade padrão por um ícone personalizado no Windows 2000

Para substituir o ícone de unidade padrão por um ícone personalizado no Windows 2000, adicione uma subchave chamada para a letra da unidade à chave a seguir.

```
HKEY_CLASSES_ROOT
   Applications
      Explorer.exe
         Drives
```

O exemplo a seguir especifica um ícone e um rótulo personalizados para a unidade E:. O ícone está no arquivo C: \\ MyDir \\MyDrive.exe com um índice baseado em zero de três.

Para o Windows 2000:

```
HKEY_CLASSES_ROOT
   Applications
      Explorer.exe
         Drives
            E
               DefaultIcon
                  (Default) = C:\MyDir\MyDrive.exe,3
               DefaultLabel
                  (Default) = MyDrive
```

### <a name="step-2-replacing-the-standard-drive-icon-with-a-custom-icon-in-all-other-versions-of-windows"></a>Etapa 2: substituindo o ícone da unidade padrão por um ícone personalizado em todas as outras versões do Windows

Para substituir o ícone de unidade padrão por um ícone personalizado em todas as versões do Windows que não sejam o Windows 2000, adicione uma subchave chamada para a letra da unidade à chave a seguir.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  DriveIcons
```

O exemplo a seguir especifica um ícone e um rótulo personalizados para a unidade E:. O ícone está no arquivo C: \\ MyDir \\MyDrive.exe com um índice baseado em zero de três.

Para todas as outras versões do Windows:

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  DriveIcons
                     E
                        DefaultIcon
                           (Default) = C:\MyDir\MyDrive.exe,3
                        DefaultLabel
                           (Default) = MyDrive
```

### <a name="step-3-calling-the-shupdateimage-event"></a>Etapa 3: chamando o evento SHUpdateImage

Em todas as versões do Windows, se você alterar um tipo de arquivo ou ícone de unidade, também deverá chamar SHUpdateImage para notificar o Shell para atualizar os ícones que são exibidos no momento.

## <a name="remarks"></a>Comentários

A letra da unidade não deve ser seguida por dois-pontos (:). Adicione uma subchave **DefaultIcon** à subchave da letra da unidade e defina seu valor padrão como uma cadeia de caracteres que contenha o local do ícone. A primeira parte da cadeia de caracteres contém o caminho totalmente qualificado do arquivo do ícone. Se houver mais de um ícone no arquivo, o caminho será seguido por uma vírgula e, em seguida, pelo índice de base zero do ícone.

 

 



