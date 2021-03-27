---
description: No Windows 7 e posterior, você pode usar a subchave ExtendedSubCommandsKey para criar menus em cascata estendidos.
ms.assetid: 6E8B4FB7-D4DB-4DBC-AF6F-59D02CB6AB13
title: Criar menus em cascata com a entrada de registro ExtendedSubCommandsKey
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 220a38825ae250a0d58d30bc7de93f290f819eb8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103662160"
---
# <a name="how-to-create-cascading-menus-with-the-extendedsubcommandskey-registry-entry"></a><span data-ttu-id="47208-103">Como criar menus em cascata com a entrada de registro ExtendedSubCommandsKey</span><span class="sxs-lookup"><span data-stu-id="47208-103">How to Create Cascading Menus with the ExtendedSubCommandsKey Registry Entry</span></span>

<span data-ttu-id="47208-104">No Windows 7 e posterior, você pode usar a subchave **ExtendedSubCommandsKey** para criar menus em cascata estendidos.</span><span class="sxs-lookup"><span data-stu-id="47208-104">In Windows 7 and later, you can use the **ExtendedSubCommandsKey** subkey to create extended cascading menus.</span></span>

<span data-ttu-id="47208-105">A captura de tela a seguir é um exemplo de um menu estendido em cascata.</span><span class="sxs-lookup"><span data-stu-id="47208-105">The following screen shot is an example of an extended cascading menu.</span></span>

![captura de tela mostrando o menu em cascata estendida para dispositivos](images/file-assoc/extendedsubcommandskey.png)

<span data-ttu-id="47208-107">Como **a \_ \_ raiz das classes hKey** é uma combinação de **HKEY \_ Current \_ User** e **HKEY \_ local \_ Machine**, você pode registrar os subverbors na subchave **HKEY \_ Current \_ User** \\ **software** \\ **classes** .</span><span class="sxs-lookup"><span data-stu-id="47208-107">Because **HKEY\_CLASSES\_ROOT** is a combination of **HKEY\_CURRENT\_USER** and **HKEY\_LOCAL\_MACHINE**, you can register the subverbs under the **HKEY\_CURRENT\_USER**\\**Software**\\**Classes** subkey.</span></span> <span data-ttu-id="47208-108">A vantagem disso é que a permissão elevada não é necessária.</span><span class="sxs-lookup"><span data-stu-id="47208-108">The advantage of doing so is that elevated permission is not required.</span></span> <span data-ttu-id="47208-109">Outras associações de arquivo podem reutilizar esse conjunto inteiro de verbos especificando a mesma subchave **ExtendedSubCommandsKey** .</span><span class="sxs-lookup"><span data-stu-id="47208-109">Other file associations can reuse this entire set of verbs by specifying the same **ExtendedSubCommandsKey** subkey.</span></span> <span data-ttu-id="47208-110">Se você não precisar reutilizar esse conjunto de verbos, poderá listar os verbos sob o pai.</span><span class="sxs-lookup"><span data-stu-id="47208-110">If you do not need to reuse this set of verbs, you can list the verbs under the parent.</span></span> <span data-ttu-id="47208-111">Nesse caso, verifique se o valor padrão do pai está vazio, conforme ilustrado no exemplo de entrada do registro nesta seção.</span><span class="sxs-lookup"><span data-stu-id="47208-111">In this case, make sure the default value of the parent is empty, as illustrated in the registry entry example in this section.</span></span>

## <a name="instructions"></a><span data-ttu-id="47208-112">Instruções</span><span class="sxs-lookup"><span data-stu-id="47208-112">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="47208-113">Etapa 1:</span><span class="sxs-lookup"><span data-stu-id="47208-113">Step 1:</span></span>

<span data-ttu-id="47208-114">Crie uma subchave em **HKEY \_ classes \_ raiz** \\ *ProgID* \\ **shell** \\ *CascadeMenuKey* e dê ao CascadeMenuKey um nome como *CascadeTest*, por exemplo.</span><span class="sxs-lookup"><span data-stu-id="47208-114">Create a subkey under **HKEY\_CLASSES\_ROOT**\\*ProgID*\\**shell**\\*CascadeMenuKey* and give the CascadeMenuKey a name such as *CascadeTest*, for example.</span></span> <span data-ttu-id="47208-115">Em seguida, adicione uma entrada MUIVerb do tipo **reg \_ sz** e dê a ele um nome como Test Cascade menu 2, conforme ilustrado no exemplo de registro a seguir.</span><span class="sxs-lookup"><span data-stu-id="47208-115">Then add a MUIVerb entry of **REG\_SZ** type and give it a name such as Test Cascade Menu 2, as illustrated in the following registry example.</span></span>

```
HKEY_CLASSES_ROOT
   txtfile
      shell
         CascadeTest
            MUIVerb = Test Cascade Menu 2
```

### <a name="step-2"></a><span data-ttu-id="47208-116">Etapa 2:</span><span class="sxs-lookup"><span data-stu-id="47208-116">Step 2:</span></span>

<span data-ttu-id="47208-117">Na subchave *CascadeTest* que você criou, adicione uma subchave **ExtendedSubCommandsKey** e, em seguida, adicione os subcomandos de documento (do tipo **reg \_ sz**); por exemplo:</span><span class="sxs-lookup"><span data-stu-id="47208-117">Under the *CascadeTest* subkey that you created, add an **ExtendedSubCommandsKey** subkey, and then add the document subcommands (of type **REG\_SZ**); for example:</span></span>

```
HKEY_CLASSES_ROOT
   txtfile
      Shell
         Test Cascade Menu 2
            (Default)
            ExtendedSubCommandsKey
               Layout
               Properties
               Select all
```

<span data-ttu-id="47208-118">Verifique se o valor padrão da subchave *Test Cascade do menu 2* está vazio e mostrado como **(valor não definido)**.</span><span class="sxs-lookup"><span data-stu-id="47208-118">Ensure that the default value of the *Test Cascade Menu 2* subkey is empty, and shown as **(value not set)**.</span></span>

### <a name="step-3"></a><span data-ttu-id="47208-119">Etapa 3:</span><span class="sxs-lookup"><span data-stu-id="47208-119">Step 3:</span></span>

<span data-ttu-id="47208-120">Preencha os subverbos usando qualquer uma das seguintes implementações de verbo estático.</span><span class="sxs-lookup"><span data-stu-id="47208-120">Populate the subverbs using any of the following static verb implementations.</span></span> <span data-ttu-id="47208-121">Observe que a subchave CommandFlags representa os valores de EXPCMDFLAGS.</span><span class="sxs-lookup"><span data-stu-id="47208-121">Note that the CommandFlags subkey represents EXPCMDFLAGS values.</span></span> <span data-ttu-id="47208-122">Se você quiser adicionar um separador antes ou depois do item de menu em cascata, use ECF \_ SEPARATORBEFORE (0x20) ou ECF \_ SEPARATORAFTER (0x40).</span><span class="sxs-lookup"><span data-stu-id="47208-122">If you want to add a separator before or after the cascade menu item, use ECF\_SEPARATORBEFORE (0x20) or ECF\_SEPARATORAFTER (0x40).</span></span> <span data-ttu-id="47208-123">Para obter uma descrição desses sinalizadores do Windows 7 e posterior, consulte [**IExplorerCommand:: GetFlags**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-getflags).</span><span class="sxs-lookup"><span data-stu-id="47208-123">For a description of these Windows 7 and later flags, see [**IExplorerCommand::GetFlags**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-getflags).</span></span> <span data-ttu-id="47208-124">ECF \_ SEPARATORBEFORE funciona apenas para os itens de menu de nível superior.</span><span class="sxs-lookup"><span data-stu-id="47208-124">ECF\_SEPARATORBEFORE works only for the top level menu items.</span></span> <span data-ttu-id="47208-125">MUIVerb é do tipo **reg \_ sz** e CommandFlags é do tipo **reg \_ DWORD**.</span><span class="sxs-lookup"><span data-stu-id="47208-125">MUIVerb is of type **REG\_SZ**, and CommandFlags is of type **REG\_DWORD**.</span></span>

```
HKEY_CLASSES_ROOT
   txtile
      Shell
         Test Cascade Menu 2
            (Default)
            ExtendedSubCommandsKey
               Shell
                  cmd1
                     MUIVerb = Notepad
                     command
                        (Default) = %SystemRoot%\system32\notepad.exe %1
                  cmd2
                     MUIVerb = Wordpad
                     CommandFlags = 0x20
                     command
                        (Default) = C:\Program Files\Windows NT\Accessories\wordpad.exe %1
```

## <a name="remarks"></a><span data-ttu-id="47208-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="47208-126">Remarks</span></span>

<span data-ttu-id="47208-127">A captura de tela a seguir é uma ilustração dos exemplos de entrada de chave do registro anterior.</span><span class="sxs-lookup"><span data-stu-id="47208-127">The following screen shot is an illustration of the previous registry key entry examples.</span></span>

![captura de tela mostrando um exemplo de um menu em cascata mostrando as opções do bloco de notas e do WordPad](images/file-assoc/testcascademenu2.png)

 

 



