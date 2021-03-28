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
# <a name="how-to-implement-custom-verbs-for-folders-through-desktopini"></a><span data-ttu-id="428db-104">Como implementar verbos personalizados para pastas por meio de Desktop.ini</span><span class="sxs-lookup"><span data-stu-id="428db-104">How to Implement Custom Verbs for Folders through Desktop.ini</span></span>

<span data-ttu-id="428db-105">No Windows 7 e posterior, você pode adicionar verbos a uma pasta usando Desktop.ini.</span><span class="sxs-lookup"><span data-stu-id="428db-105">In Windows 7 and later, you can add verbs to a folder by using Desktop.ini.</span></span> <span data-ttu-id="428db-106">Para obter mais informações sobre Desktop.ini arquivos, consulte [como personalizar pastas com Desktop.ini](how-to-customize-folders-with-desktop-ini.md).</span><span class="sxs-lookup"><span data-stu-id="428db-106">For more information about Desktop.ini files, see [How to Customize Folders with Desktop.ini](how-to-customize-folders-with-desktop-ini.md).</span></span>

> [!Note]  
> <span data-ttu-id="428db-107">Desktop.ini arquivos devem ser sempre marcados como ocultos do **sistema** para que  +   não sejam exibidos aos usuários.</span><span class="sxs-lookup"><span data-stu-id="428db-107">Desktop.ini files should always be marked **System** + **Hidden** so they won't be displayed to users.</span></span>

 

<span data-ttu-id="428db-108">Para adicionar verbos personalizados para pastas por meio de um arquivo Desktop.ini, execute as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="428db-108">To add custom verbs for folders through a Desktop.ini file, perform the following steps.</span></span>

## <a name="instructions"></a><span data-ttu-id="428db-109">Instruções</span><span class="sxs-lookup"><span data-stu-id="428db-109">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="428db-110">Etapa 1:</span><span class="sxs-lookup"><span data-stu-id="428db-110">Step 1:</span></span>

<span data-ttu-id="428db-111">Crie uma pasta que esteja marcada como **somente leitura** ou **sistema**.</span><span class="sxs-lookup"><span data-stu-id="428db-111">Create a folder that is marked **Read-only** or **System**.</span></span>

### <a name="step-2"></a><span data-ttu-id="428db-112">Etapa 2:</span><span class="sxs-lookup"><span data-stu-id="428db-112">Step 2:</span></span>

<span data-ttu-id="428db-113">Crie um arquivo de Desktop.ini que inclui um \[ . ShellClassInfo \] DirectoryClass = ProgID da pasta.</span><span class="sxs-lookup"><span data-stu-id="428db-113">Create a Desktop.ini file that includes a \[.ShellClassInfo\] DirectoryClass=Folder ProgID.</span></span>

### <a name="step-3"></a><span data-ttu-id="428db-114">Etapa 3:</span><span class="sxs-lookup"><span data-stu-id="428db-114">Step 3:</span></span>

<span data-ttu-id="428db-115">No registro, crie o ProgID de pasta **\_ \_ raiz de classes hKey** \\  com um valor de CanUseForDirectory.</span><span class="sxs-lookup"><span data-stu-id="428db-115">In the registry, create **HKEY\_CLASSES\_ROOT**\\**Folder ProgID** with a value of CanUseForDirectory.</span></span> <span data-ttu-id="428db-116">O valor CanUseForDirectory evita o uso indevido de ProgIDs que estão definidos para não participar da implementação de verbos personalizados para pastas por meio de Desktop.ini.</span><span class="sxs-lookup"><span data-stu-id="428db-116">The CanUseForDirectory value avoids the misuse of ProgIDs that are set not to participate in implementing custom verbs for folders through Desktop.ini.</span></span>

### <a name="step-4"></a><span data-ttu-id="428db-117">Etapa 4:</span><span class="sxs-lookup"><span data-stu-id="428db-117">Step 4:</span></span>

<span data-ttu-id="428db-118">Adicione verbos na subchave ProgID da **pasta** , por exemplo:</span><span class="sxs-lookup"><span data-stu-id="428db-118">Add verbs under the **Folder** ProgID subkey, for example:</span></span>

```
HKEY_CLASSES_ROOT
   CustomFolderType
      Shell
         MyVerb
            command
               (Default) = %SystemRoot%\system32\notepad.exe %1\desktop.ini
```

## <a name="remarks"></a><span data-ttu-id="428db-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="428db-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="428db-120">Esses verbos podem ser os verbos padrão; nesse caso, clicar duas vezes na pasta ativa o verbo.</span><span class="sxs-lookup"><span data-stu-id="428db-120">These verbs can be the default verbs, in which case double-clicking the folder activates the verb.</span></span>

 

 

 



