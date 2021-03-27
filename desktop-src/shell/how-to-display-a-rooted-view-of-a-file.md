---
description: Você pode usar uma extensão de namespace para permitir que os usuários procurem o conteúdo de um arquivo em vez de serem apresentados como uma pasta. As extensões dessa classificação normalmente são usadas para exibir o conteúdo dos membros de um tipo de arquivo.
title: Como exibir uma exibição com raiz de um arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30ee16f3ce50cd79800dd98aa53256591d1f79d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828294"
---
# <a name="how-to-display-a-rooted-view-of-a-file"></a><span data-ttu-id="e2374-104">Como exibir uma exibição com raiz de um arquivo</span><span class="sxs-lookup"><span data-stu-id="e2374-104">How to Display a Rooted View of a File</span></span>

<span data-ttu-id="e2374-105">Você pode usar uma extensão de namespace para permitir que os usuários procurem o conteúdo de um arquivo em vez de serem apresentados como uma pasta.</span><span class="sxs-lookup"><span data-stu-id="e2374-105">You can use a namespace extension to allow users to browse the contents of a file rather than have it presented as a folder.</span></span> <span data-ttu-id="e2374-106">As extensões dessa classificação normalmente são usadas para exibir o conteúdo dos membros de um [tipo de arquivo](fa-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="e2374-106">Extensions of this sort are typically used to display the contents of the members of a [file type](fa-file-types.md).</span></span> <span data-ttu-id="e2374-107">Por exemplo, os membros de um tipo de arquivo podem conter vários arquivos compactados ou imagens, organizados em uma hierarquia.</span><span class="sxs-lookup"><span data-stu-id="e2374-107">For instance, the members of a file type might contain multiple compressed files or images, organized in a hierarchy.</span></span> <span data-ttu-id="e2374-108">Em vez de escrever um aplicativo para permitir que o usuário exiba o conteúdo desse arquivo, você pode escrever uma extensão de namespace e deixar que o Windows Explorer manipule a exibição.</span><span class="sxs-lookup"><span data-stu-id="e2374-108">Rather than write an application to allow the user to view the contents of such a file, you can instead write a namespace extension and let Windows Explorer handle the display.</span></span>

<span data-ttu-id="e2374-109">Você deve usar uma exibição com raiz para que uma extensão exiba o conteúdo de um arquivo.</span><span class="sxs-lookup"><span data-stu-id="e2374-109">You must use a rooted view in order to have an extension display the contents of a file.</span></span> <span data-ttu-id="e2374-110">A maneira mais comum de fornecer uma exibição com raiz dos membros de um tipo de arquivo é definir um [verbo de menu de atalho](context.md) que inicia uma instância do Explorer.exe.</span><span class="sxs-lookup"><span data-stu-id="e2374-110">The most common way to provide a rooted view of the members of a file type is to define a [shortcut menu verb](context.md) that launches an instance of Explorer.exe.</span></span> <span data-ttu-id="e2374-111">Ao tornar esse verbo o verbo padrão, um clique duplo também abrirá uma exibição com raiz do arquivo.</span><span class="sxs-lookup"><span data-stu-id="e2374-111">By making this verb the default verb, a double-click will also open a rooted view of the file.</span></span> <span data-ttu-id="e2374-112">Você pode definir um verbo para todos os membros do tipo de arquivo [modificando o registro](context.md)ou definindo os verbos de forma dinâmica em uma base arquivo por arquivo implementando um [manipulador de menu de atalho](context-menu-handlers.md).</span><span class="sxs-lookup"><span data-stu-id="e2374-112">You can either define a verb for all members of the file type by [modifying the registry](context.md), or dynamically define verbs on a file-by-file basis by implementing a [shortcut menu handler](context-menu-handlers.md).</span></span>

## <a name="instructions"></a><span data-ttu-id="e2374-113">Instruções</span><span class="sxs-lookup"><span data-stu-id="e2374-113">Instructions</span></span>


<span data-ttu-id="e2374-114">O exemplo a seguir ilustra como usar o registro para fornecer uma exibição com raiz dos membros de um tipo de arquivo, modificando o registro.</span><span class="sxs-lookup"><span data-stu-id="e2374-114">The following example illustrates how to use the registry to provide a rooted view of the members of a file type by modifying the registry.</span></span> <span data-ttu-id="e2374-115">A entrada do registro de exemplo é uma modificação de um dos exemplos na [extensão de menus de atalho](context.md).</span><span class="sxs-lookup"><span data-stu-id="e2374-115">The sample registry entry is a modification of one of the examples in [Extending Shortcut Menus](context.md).</span></span> <span data-ttu-id="e2374-116">As entradas do registro definem arquivos com uma extensão de nome de arquivo. MYP como um tipo de arquivo e usam o verbo **procurar** para iniciar uma exibição com raiz dos membros desse tipo.</span><span class="sxs-lookup"><span data-stu-id="e2374-116">The registry entries define files with an .myp file name extension as a file type, and use the **browse** verb to launch a rooted view of members of that type.</span></span>

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
   MyProgram.1
      (Default) = MyProgram Application
      Shell
         (Default) = browse
         browse
            command
               (Default) = %SYSTEMROOT%\explorer.exe /e,/root,{Extension CLSID}, "%1"
```

<span data-ttu-id="e2374-117">Você pode usar o mesmo verbo para iniciar programaticamente uma exibição com raiz de um membro do tipo de arquivo chamando a função [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) .</span><span class="sxs-lookup"><span data-stu-id="e2374-117">You can use the same verb to programmatically launch a rooted view of a member of the file type by calling the [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) function.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e2374-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e2374-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e2374-119">Especificando o local de uma extensão de namespace</span><span class="sxs-lookup"><span data-stu-id="e2374-119">Specifying a Namespace Extension's Location</span></span>](nse-junction.md)
</dt> <dt>

[<span data-ttu-id="e2374-120">Como abrir uma exibição com raiz de um ponto de junção no registro</span><span class="sxs-lookup"><span data-stu-id="e2374-120">How to Open a Rooted View of a Junction Point Through the Registry</span></span>](how-to-use-a-junction-point-to-open-a-rooted-view.md)
</dt> <dt>

[<span data-ttu-id="e2374-121">Como abrir uma exibição com raiz de um ponto de junção por meio de um arquivo de atalho</span><span class="sxs-lookup"><span data-stu-id="e2374-121">How to Open a Rooted View of a Junction Point Through a Shortcut File</span></span>](how-to-use-a-shortcut-file-to-open-a-rooted-view.md)
</dt> <dt>

[<span data-ttu-id="e2374-122">**ShellExecute**</span><span class="sxs-lookup"><span data-stu-id="e2374-122">**ShellExecute**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea)
</dt> </dl>

 

 



