---
description: No Windows 7 e posterior, você pode usar a entrada subcomandos no registro para criar menus em cascata usando o procedimento fornecido neste tópico.
title: Criar menus em cascata com a entrada de registro de subcomandos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8b1168daae5ea927f079c66eb436c099f8b3d96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988986"
---
# <a name="how-to-create-cascading-menus-with-the-subcommands-registry-entry"></a><span data-ttu-id="e2cb6-103">Como criar menus em cascata com a entrada de registro de subcomandos</span><span class="sxs-lookup"><span data-stu-id="e2cb6-103">How to Create Cascading Menus with the SubCommands Registry Entry</span></span>

<span data-ttu-id="e2cb6-104">No Windows 7 e posterior, você pode usar a entrada subcomandos no registro para criar menus em cascata usando o procedimento fornecido neste tópico.</span><span class="sxs-lookup"><span data-stu-id="e2cb6-104">In Windows 7 and later, you can use the SubCommands entry in the registry to create cascading menus by using the procedure given in this topic.</span></span>

## <a name="instructions"></a><span data-ttu-id="e2cb6-105">Instruções</span><span class="sxs-lookup"><span data-stu-id="e2cb6-105">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="e2cb6-106">Etapa 1:</span><span class="sxs-lookup"><span data-stu-id="e2cb6-106">Step 1:</span></span>

<span data-ttu-id="e2cb6-107">Crie uma nova subchave em **HKEY \_ classes \_ raiz** \\ *ProgID* \\ **shell**, em que *ProgID* é o tipo de arquivo para o qual você deseja adicionar um menu em cascata.</span><span class="sxs-lookup"><span data-stu-id="e2cb6-107">Create a new subkey under **HKEY\_CLASSES\_ROOT**\\*ProgID*\\**shell**, where *ProgID* is the file type for which you want to add a cascading menu.</span></span> <span data-ttu-id="e2cb6-108">Você pode nomear essa nova subchave como desejar.</span><span class="sxs-lookup"><span data-stu-id="e2cb6-108">You can name this new subkey anything you'd like.</span></span> <span data-ttu-id="e2cb6-109">Para o restante deste tópico, vamos chamá-lo de *CascadeMenu*, conforme mostrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="e2cb6-109">For the remainder of this topic, we'll call it *CascadeMenu*, as shown in the following example.</span></span>

```
HKEY_CLASSES_ROOT
   ProgID
      shell
         CascadeMenu
```

### <a name="step-2"></a><span data-ttu-id="e2cb6-110">Etapa 2:</span><span class="sxs-lookup"><span data-stu-id="e2cb6-110">Step 2:</span></span>

<span data-ttu-id="e2cb6-111">Adicione uma entrada denominada "MUIVerb", do tipo **reg \_ sz** ou **reg \_ Expand \_ sz**, à subchave *CascadeMenu* .</span><span class="sxs-lookup"><span data-stu-id="e2cb6-111">Add an entry named "MUIVerb", of type **REG\_SZ** or **REG\_EXPAND\_SZ**, to the *CascadeMenu* subkey.</span></span> <span data-ttu-id="e2cb6-112">Atribua essa entrada a um valor de cadeia de caracteres como "menu de teste em cascata".</span><span class="sxs-lookup"><span data-stu-id="e2cb6-112">Assign this entry a string value such as "Test Cascade Menu".</span></span> <span data-ttu-id="e2cb6-113">Normalmente, essa cadeia de caracteres é fornecida como uma referência de recurso no formato " @file , recurso".</span><span class="sxs-lookup"><span data-stu-id="e2cb6-113">Normally, this string is provided as a resource reference in the form "@file, resource".</span></span> <span data-ttu-id="e2cb6-114">O valor (padrão) da subchave *CascadeMenu* não deve ser definido.</span><span class="sxs-lookup"><span data-stu-id="e2cb6-114">The (Default) value for the *CascadeMenu* subkey should not be set.</span></span>

```
HKEY_CLASSES_ROOT
   ProgID
      shell
         CascadeMenu
            (Default)
            MUIVerb = Test Cascade Menu
```

### <a name="step-3"></a><span data-ttu-id="e2cb6-115">Etapa 3:</span><span class="sxs-lookup"><span data-stu-id="e2cb6-115">Step 3:</span></span>

<span data-ttu-id="e2cb6-116">Adicione uma entrada denominada "subcomandos", do tipo **reg \_ sz** ou **reg \_ Expand \_ sz**, à subchave *CascadeMenu* .</span><span class="sxs-lookup"><span data-stu-id="e2cb6-116">Add an entry named "SubCommands", of type **REG\_SZ** or **REG\_EXPAND\_SZ**, to the *CascadeMenu* subkey.</span></span> <span data-ttu-id="e2cb6-117">Atribua essa entrada a uma lista delimitada por ponto-e-vírgula dos verbos que devem aparecer no menu, na ordem desejada de aparência.</span><span class="sxs-lookup"><span data-stu-id="e2cb6-117">Assign this entry a semicolon-delimited list of the verbs that should appear on the menu, in their desired order of appearance.</span></span>

```
HKEY_CLASSES_ROOT
   ProgID
      Shell
         CascadeMenu
            SubCommands = Windows.delete;Windows.properties;Windows.rename;Windows.cut;Windows.copy;Windows.paste
```

### <a name="step-4"></a><span data-ttu-id="e2cb6-118">Etapa 4:</span><span class="sxs-lookup"><span data-stu-id="e2cb6-118">Step 4:</span></span>

<span data-ttu-id="e2cb6-119">Preencha a subchave **CommandStore** com implementações de verbo para qualquer método de implementação de verbo estático personalizado que você usou em sua entrada de subcomandos; por exemplo:</span><span class="sxs-lookup"><span data-stu-id="e2cb6-119">Populate the **CommandStore** subkey with verb implementations for any custom static verb implementation methods that you've used in your SubCommands entry; for example:</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  CommandStore
                     Shell
                        VerbName
                           command
                              (Default) = notepad.exe %1
```

## <a name="related-topics"></a><span data-ttu-id="e2cb6-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e2cb6-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e2cb6-121">Criando menus em cascata estáticos</span><span class="sxs-lookup"><span data-stu-id="e2cb6-121">Creating Static Cascading Menus</span></span>](creating-static-cascading-menus.md)
</dt> </dl>

 

 



