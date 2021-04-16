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
# <a name="how-to-assign-a-custom-icon-and-label-to-a-drive-letter"></a><span data-ttu-id="7d1c4-103">Como atribuir um ícone e um rótulo personalizados a uma letra da unidade</span><span class="sxs-lookup"><span data-stu-id="7d1c4-103">How to Assign a Custom Icon and Label to a Drive Letter</span></span>

<span data-ttu-id="7d1c4-104">Especifique um ícone e um rótulo personalizados para uma unidade.</span><span class="sxs-lookup"><span data-stu-id="7d1c4-104">Specify a custom icon and label for a drive.</span></span>

## <a name="instructions"></a><span data-ttu-id="7d1c4-105">Instruções</span><span class="sxs-lookup"><span data-stu-id="7d1c4-105">Instructions</span></span>

### <a name="step-1-replacing-the-standard-drive-icon-with-a-custom-icon-in-windows-2000"></a><span data-ttu-id="7d1c4-106">Etapa 1: substituindo o ícone de unidade padrão por um ícone personalizado no Windows 2000</span><span class="sxs-lookup"><span data-stu-id="7d1c4-106">Step 1: Replacing the standard drive icon with a custom icon in Windows 2000</span></span>

<span data-ttu-id="7d1c4-107">Para substituir o ícone de unidade padrão por um ícone personalizado no Windows 2000, adicione uma subchave chamada para a letra da unidade à chave a seguir.</span><span class="sxs-lookup"><span data-stu-id="7d1c4-107">To replace the standard drive icon with a custom icon in Windows 2000, add a subkey named for the drive letter to the following key.</span></span>

```
HKEY_CLASSES_ROOT
   Applications
      Explorer.exe
         Drives
```

<span data-ttu-id="7d1c4-108">O exemplo a seguir especifica um ícone e um rótulo personalizados para a unidade E:.</span><span class="sxs-lookup"><span data-stu-id="7d1c4-108">The following example specifies a custom icon and label for the E: drive.</span></span> <span data-ttu-id="7d1c4-109">O ícone está no arquivo C: \\ MyDir \\MyDrive.exe com um índice baseado em zero de três.</span><span class="sxs-lookup"><span data-stu-id="7d1c4-109">The icon is in the C:\\MyDir\\MyDrive.exe file with a zero-based index of three.</span></span>

<span data-ttu-id="7d1c4-110">Para o Windows 2000:</span><span class="sxs-lookup"><span data-stu-id="7d1c4-110">For Windows 2000:</span></span>

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

### <a name="step-2-replacing-the-standard-drive-icon-with-a-custom-icon-in-all-other-versions-of-windows"></a><span data-ttu-id="7d1c4-111">Etapa 2: substituindo o ícone da unidade padrão por um ícone personalizado em todas as outras versões do Windows</span><span class="sxs-lookup"><span data-stu-id="7d1c4-111">Step 2: Replacing the standard drive icon with a custom icon in all other versions of Windows</span></span>

<span data-ttu-id="7d1c4-112">Para substituir o ícone de unidade padrão por um ícone personalizado em todas as versões do Windows que não sejam o Windows 2000, adicione uma subchave chamada para a letra da unidade à chave a seguir.</span><span class="sxs-lookup"><span data-stu-id="7d1c4-112">To replace the standard drive icon with a custom icon in all versions of Windows other than Windows 2000, add a subkey named for the drive letter to the following key.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  DriveIcons
```

<span data-ttu-id="7d1c4-113">O exemplo a seguir especifica um ícone e um rótulo personalizados para a unidade E:.</span><span class="sxs-lookup"><span data-stu-id="7d1c4-113">The following example specifies a custom icon and label for the E: drive.</span></span> <span data-ttu-id="7d1c4-114">O ícone está no arquivo C: \\ MyDir \\MyDrive.exe com um índice baseado em zero de três.</span><span class="sxs-lookup"><span data-stu-id="7d1c4-114">The icon is in the C:\\MyDir\\MyDrive.exe file with a zero-based index of three.</span></span>

<span data-ttu-id="7d1c4-115">Para todas as outras versões do Windows:</span><span class="sxs-lookup"><span data-stu-id="7d1c4-115">For all other versions of Windows:</span></span>

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

### <a name="step-3-calling-the-shupdateimage-event"></a><span data-ttu-id="7d1c4-116">Etapa 3: chamando o evento SHUpdateImage</span><span class="sxs-lookup"><span data-stu-id="7d1c4-116">Step 3: Calling the SHUpdateImage Event</span></span>

<span data-ttu-id="7d1c4-117">Em todas as versões do Windows, se você alterar um tipo de arquivo ou ícone de unidade, também deverá chamar SHUpdateImage para notificar o Shell para atualizar os ícones que são exibidos no momento.</span><span class="sxs-lookup"><span data-stu-id="7d1c4-117">In all versions of Windows, if you change a file type or drive icon you must also call SHUpdateImage to notify the Shell to update any icons that are currently displayed.</span></span>

## <a name="remarks"></a><span data-ttu-id="7d1c4-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="7d1c4-118">Remarks</span></span>

<span data-ttu-id="7d1c4-119">A letra da unidade não deve ser seguida por dois-pontos (:).</span><span class="sxs-lookup"><span data-stu-id="7d1c4-119">The drive letter should not be followed by a colon (:).</span></span> <span data-ttu-id="7d1c4-120">Adicione uma subchave **DefaultIcon** à subchave da letra da unidade e defina seu valor padrão como uma cadeia de caracteres que contenha o local do ícone.</span><span class="sxs-lookup"><span data-stu-id="7d1c4-120">Add a **DefaultIcon** subkey to the drive letter subkey and set its default value to a string that contains the location of the icon.</span></span> <span data-ttu-id="7d1c4-121">A primeira parte da cadeia de caracteres contém o caminho totalmente qualificado do arquivo do ícone.</span><span class="sxs-lookup"><span data-stu-id="7d1c4-121">The first part of the string contains the fully-qualified path of the icon's file.</span></span> <span data-ttu-id="7d1c4-122">Se houver mais de um ícone no arquivo, o caminho será seguido por uma vírgula e, em seguida, pelo índice de base zero do ícone.</span><span class="sxs-lookup"><span data-stu-id="7d1c4-122">If there is more than one icon in the file, the path is followed by a comma, and then by the zero-based index of the icon.</span></span>

 

 



