---
description: Como excluir um aplicativo da caixa de diálogo abrir com para o tipo de arquivo não associado.
title: Como excluir um aplicativo da caixa de diálogo abrir com para tipos de arquivo não associados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9443416e95fca112623d487bf58f4fce1d51d13d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104560557"
---
# <a name="how-to-exclude-an-application-from-the-open-with-dialog-box-for-unassociated-file-types"></a><span data-ttu-id="c1c8e-103">Como excluir um aplicativo da caixa de diálogo abrir com para tipos de arquivo não associados</span><span class="sxs-lookup"><span data-stu-id="c1c8e-103">How to Exclude an Application from the Open With Dialog Box for Unassociated File Types</span></span>

<span data-ttu-id="c1c8e-104">Quando um usuário tenta abrir um arquivo que não é membro de nenhum tipo de arquivo registrado (ou seja, um tipo de arquivo desconhecido) ou quando um usuário seleciona **abrir com** ou **abrir com-> escolher programa padrão** no menu de atalho de um arquivo, o Shell apresenta um submenu ou caixa de diálogo que permite ao usuário especificar o programa usado para abrir o arquivo.</span><span class="sxs-lookup"><span data-stu-id="c1c8e-104">When a user attempts to open a file that is not a member of any registered file type (that is, an unknown file type), or when a user selects **Open with** or **Open with -> Choose default program** from a file's shortcut menu, the Shell presents a submenu or dialog box that enables the user to specify the program used to open the file.</span></span>

<span data-ttu-id="c1c8e-105">Por padrão, qualquer aplicativo registrado como uma subchave de aplicativos **\_ \_ raiz de classes hKey** \\  é apresentado na caixa de diálogo **abrir com** .</span><span class="sxs-lookup"><span data-stu-id="c1c8e-105">By default, any application registered as a subkey of **HKEY\_CLASSES\_ROOT**\\**Applications** is presented in the **Open with** dialog box.</span></span> <span data-ttu-id="c1c8e-106">Esses aplicativos são apresentados em **abrir com** , independentemente de o aplicativo estar registrado para lidar com o tipo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="c1c8e-106">These applications are presented in **Open with** regardless of whether the application is registered to handle the file type.</span></span>

<span data-ttu-id="c1c8e-107">Para impedir que um aplicativo apareça na caixa de diálogo **abrir com** quando o aplicativo não deve ou não pode ser usado para abrir determinados tipos de arquivo, use uma das duas técnicas descritas neste tópico.</span><span class="sxs-lookup"><span data-stu-id="c1c8e-107">To prevent an application from appearing in the **Open with** dialog box when the application should not or cannot be used to open certain file types, use one of the two techniques described in this topic.</span></span>

## <a name="instructions"></a><span data-ttu-id="c1c8e-108">Instruções</span><span class="sxs-lookup"><span data-stu-id="c1c8e-108">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="c1c8e-109">Etapa 1:</span><span class="sxs-lookup"><span data-stu-id="c1c8e-109">Step 1:</span></span>

<span data-ttu-id="c1c8e-110">Adicione uma entrada NoOpenWith à subchave do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c1c8e-110">Add a NoOpenWith entry to the application's subkey.</span></span> <span data-ttu-id="c1c8e-111">Quando um aplicativo usa um tipo de arquivo, o Windows registra essas informações para criar a lista de **programas recomendados** .</span><span class="sxs-lookup"><span data-stu-id="c1c8e-111">When an application uses a file type, Windows records that information to build the **Recommended Programs** list.</span></span> <span data-ttu-id="c1c8e-112">Essa lista é apresentada no submenu **abrir com** , conforme mostrado na captura de tela a seguir.</span><span class="sxs-lookup"><span data-stu-id="c1c8e-112">This list is presented in the **Open with** submenu as shown in the following screen shot.</span></span>

![captura de tela do menu de atalho com o submenu abrir com mostrado](images/file-assoc/openwithsubmenu.png)

<span data-ttu-id="c1c8e-114">Esses aplicativos recomendados também são mostrados na parte **programas recomendados** da caixa de diálogo **abrir com** , conforme mostrado na captura de tela a seguir.</span><span class="sxs-lookup"><span data-stu-id="c1c8e-114">These recommended applications are also shown in the **Recommended Programs** portion of the **Open with** dialog box as shown in the following screen shot.</span></span>

![captura de tela da caixa de diálogo abrir com com programas recomendados](images/file-assoc/openwithdialog.png)

> [!Note]  
> <span data-ttu-id="c1c8e-116">Se um aplicativo se registrou em [OpenWithList](fa-file-types.md) ou OpenWithProgIDs para o tipo de arquivo, ele será exibido na lista de **programas recomendados** , mesmo que a entrada NoOpenWith esteja definida.</span><span class="sxs-lookup"><span data-stu-id="c1c8e-116">If an application has registered itself in the [OpenWithList](fa-file-types.md) or OpenWithProgIDs for the file type, it will appear in the **Recommended Programs** list even if the NoOpenWith entry is set.</span></span> <span data-ttu-id="c1c8e-117">Além disso, lembre-se de que, independentemente de um aplicativo ser oferecido em uma lista de programas recomendados, um usuário pode navegar manualmente para qualquer arquivo executável.</span><span class="sxs-lookup"><span data-stu-id="c1c8e-117">Also, remember that regardless of whether an application is offered in a list of recommended programs, a user can manually browse to any executable file.</span></span>

 

<span data-ttu-id="c1c8e-118">Os aplicativos podem desabilitar esse controle especificando um valor de NoOpenWith sob a subchave do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c1c8e-118">Applications can disable this tracking by specifying a NoOpenWith value under the application's subkey.</span></span>

<span data-ttu-id="c1c8e-119">A entrada NoOpenWith é um valor **\_ sz do reg** vazio, conforme mostrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="c1c8e-119">The NoOpenWith entry is an empty **REG\_SZ** value as shown in the following example.</span></span>

```
HKEY_CLASSES_ROOT
   Applications
      MyProgram.exe
         NoOpenWith
```

<span data-ttu-id="c1c8e-120">A definição da entrada NoOpenWith também tem estes efeitos:</span><span class="sxs-lookup"><span data-stu-id="c1c8e-120">Setting the NoOpenWith entry also has these effects:</span></span>

-   <span data-ttu-id="c1c8e-121">Impede a fixação de um arquivo na lista de atalhos do aplicativo por meio de arrastar e soltar, a menos que o aplicativo esteja especificamente registrado para lidar com esse tipo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="c1c8e-121">Prevents pinning a file to the application's Jump List through drag-and-drop, unless the application is specifically registered to handle that file type.</span></span>
-   <span data-ttu-id="c1c8e-122">Impede que a caixa de diálogo arquivo comum e qualquer chamada para a função [**SHAddToRecentDocs**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs) adicione qualquer arquivo à lista de atalhos do aplicativo, a menos que o aplicativo esteja especificamente registrado para lidar com esse tipo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="c1c8e-122">Prevents the common file dialog box and any call to the [**SHAddToRecentDocs**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs) function from adding any file to the application's Jump List, unless the application is specifically registered to handle that file type.</span></span>

### <a name="step-2"></a><span data-ttu-id="c1c8e-123">Etapa 2:</span><span class="sxs-lookup"><span data-stu-id="c1c8e-123">Step 2:</span></span>

<span data-ttu-id="c1c8e-124">A segunda maneira de impedir que um aplicativo apareça na caixa de diálogo **abrir com** é usar a subchave **SupportedTypes** para listar explicitamente as extensões dos tipos de arquivos que o aplicativo pode abrir.</span><span class="sxs-lookup"><span data-stu-id="c1c8e-124">The second way to prevent an application from appearing in the **Open with** dialog box is to use the **SupportedTypes** subkey to explicitly list the extensions of file types that the application can open.</span></span> <span data-ttu-id="c1c8e-125">Isso impede que o aplicativo apareça na caixa de diálogo **abrir com** para os tipos de arquivo que não podem ser abertos.</span><span class="sxs-lookup"><span data-stu-id="c1c8e-125">This prevents the application from appearing in the **Open with** dialog box for file types that it cannot open.</span></span> <span data-ttu-id="c1c8e-126">Ele também faz com que o aplicativo apareça na lista de **programas recomendados** , conforme discutido anteriormente.</span><span class="sxs-lookup"><span data-stu-id="c1c8e-126">It also causes the application to appear in the **Recommended Programs** list as discussed previously.</span></span>

<span data-ttu-id="c1c8e-127">Esse método é particularmente útil se um aplicativo pode salvar um arquivo como um determinado tipo de arquivo, mas não pode abrir esse tipo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="c1c8e-127">This method is particularly useful if an application can save a file as a certain file type but cannot open that file type.</span></span> <span data-ttu-id="c1c8e-128">Um aplicativo também deve definir o \_ sinalizador FOS DONTADDTORECENT por meio de [**IFileDialog:: SetOptions**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setoptions) ao chamar a caixa de diálogo **salvar** .</span><span class="sxs-lookup"><span data-stu-id="c1c8e-128">An application should also set the FOS\_DONTADDTORECENT flag through [**IFileDialog::SetOptions**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setoptions) when calling the **Save** dialog box.</span></span> <span data-ttu-id="c1c8e-129">Isso impede que o item seja adicionado às partes **recentes** ou **frequentes** de uma lista de atalhos.</span><span class="sxs-lookup"><span data-stu-id="c1c8e-129">This keeps the item from being added to the **Recent** or **Frequent** portions of a Jump List.</span></span> <span data-ttu-id="c1c8e-130">Ele também impede que o aplicativo seja acompanhado em [OpenWithList](fa-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="c1c8e-130">It also blocks the application from being tracked under [OpenWithList](fa-file-types.md).</span></span>

<span data-ttu-id="c1c8e-131">Cada extensão com suporte é adicionada como uma entrada na subchave **SupportedTypes** , conforme mostrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="c1c8e-131">Each supported extension is added as an entry under the **SupportedTypes** subkey as shown in the following example.</span></span> <span data-ttu-id="c1c8e-132">As entradas são do tipo **reg \_ sz** ou **reg \_ NULL**, sem valores associados.</span><span class="sxs-lookup"><span data-stu-id="c1c8e-132">The entries are of type **REG\_SZ** or **REG\_NULL**, with no associated values.</span></span>

```
HKEY_CLASSES_ROOT
   Applications
      ApplicationName
         SupportedTypes
            .ext1
            .ext2
            .ext3
```

<span data-ttu-id="c1c8e-133">Se uma subchave **SupportedTypes** for fornecida, somente os arquivos com essas extensões estarão qualificados para fixação na lista de atalhos do aplicativo ou para serem rastreados na lista de destinos **recentes** ou **frequentes** de um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c1c8e-133">If a **SupportedTypes** subkey is provided, only files with those extensions are eligible for pinning to the application's Jump List or for being tracked in an application's **Recent** or **Frequent** destinations list.</span></span>

<span data-ttu-id="c1c8e-134">A entrada NoOpenWith substitui a subchave **SupportedTypes** e oculta o aplicativo na caixa de diálogo **abrir com** .</span><span class="sxs-lookup"><span data-stu-id="c1c8e-134">The NoOpenWith entry overrides the **SupportedTypes** subkey and hides the application in the **Open with** dialog box.</span></span>

 

 
