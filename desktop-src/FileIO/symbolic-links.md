---
description: Um link simbólico é um objeto do sistema de arquivos que aponta para outro objeto do sistema de arquivos. O objeto que está sendo apontado é chamado de destino.
ms.assetid: d6bf5df7-bc12-4dec-b116-95d9109f5eb4
title: Links simbólicos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f051beb7de0280ba42df782264cef385f8d01a20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105767653"
---
# <a name="symbolic-links"></a><span data-ttu-id="3732a-104">Links simbólicos</span><span class="sxs-lookup"><span data-stu-id="3732a-104">Symbolic Links</span></span>

<span data-ttu-id="3732a-105">Um link simbólico é um objeto do sistema de arquivos que aponta para outro objeto do sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="3732a-105">A symbolic link is a file-system object that points to another file system object.</span></span> <span data-ttu-id="3732a-106">O objeto que está sendo apontado é chamado de destino.</span><span class="sxs-lookup"><span data-stu-id="3732a-106">The object being pointed to is called the target.</span></span>

<span data-ttu-id="3732a-107">Links simbólicos são transparentes para os usuários; os links aparecem como arquivos ou diretórios normais e podem ser afetados pelo usuário ou aplicativo exatamente da mesma maneira.</span><span class="sxs-lookup"><span data-stu-id="3732a-107">Symbolic links are transparent to users; the links appear as normal files or directories, and can be acted upon by the user or application in exactly the same manner.</span></span>

<span data-ttu-id="3732a-108">Links simbólicos são projetados para auxiliar na migração e na compatibilidade de aplicativos com sistemas operacionais UNIX.</span><span class="sxs-lookup"><span data-stu-id="3732a-108">Symbolic links are designed to aid in migration and application compatibility with UNIX operating systems.</span></span> <span data-ttu-id="3732a-109">A Microsoft implementou seus links simbólicos para funcionar exatamente como links UNIX.</span><span class="sxs-lookup"><span data-stu-id="3732a-109">Microsoft has implemented its symbolic links to function just like UNIX links.</span></span>

<span data-ttu-id="3732a-110">Para obter mais informações, consulte os tópicos a seguir.</span><span class="sxs-lookup"><span data-stu-id="3732a-110">For more information, see the following topics.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="3732a-111">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="3732a-111">In this section</span></span>



| <span data-ttu-id="3732a-112">Tópico</span><span class="sxs-lookup"><span data-stu-id="3732a-112">Topic</span></span>                                                                                                             | <span data-ttu-id="3732a-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="3732a-113">Description</span></span>                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3732a-114">Efeitos de link simbólico em funções de sistemas de arquivos</span><span class="sxs-lookup"><span data-stu-id="3732a-114">Symbolic Link Effects on File Systems Functions</span></span>](symbolic-link-effects-on-file-systems-functions.md)<br/> | <span data-ttu-id="3732a-115">Como os links simbólicos afetam as funções de arquivo padrão que usam nomes de caminho para especificar um ou mais arquivos.</span><span class="sxs-lookup"><span data-stu-id="3732a-115">How symbolic links affect standard file functions that use path names to specify one or more files.</span></span><br/>                                        |
| [<span data-ttu-id="3732a-116">Considerações sobre programação</span><span class="sxs-lookup"><span data-stu-id="3732a-116">Programming Considerations</span></span>](symbolic-link-programming-considerations.md)<br/>                             | <span data-ttu-id="3732a-117">Considerações sobre programação para trabalhar com links simbólicos.</span><span class="sxs-lookup"><span data-stu-id="3732a-117">Programming considerations for working with symbolic links.</span></span><br/>                                                                                |
| [<span data-ttu-id="3732a-118">Criando links simbólicos</span><span class="sxs-lookup"><span data-stu-id="3732a-118">Creating Symbolic Links</span></span>](creating-symbolic-links.md)<br/>                                                 | <span data-ttu-id="3732a-119">Crie links simbólicos que usam um caminho absoluto ou relativo usando a função [**CreateSymbolicLink**](/windows/desktop/api/WinBase/nf-winbase-createsymboliclinka) .</span><span class="sxs-lookup"><span data-stu-id="3732a-119">Create symbolic links that use either an absolute or relative path by using the [**CreateSymbolicLink**](/windows/desktop/api/WinBase/nf-winbase-createsymboliclinka) function.</span></span><br/> |



 

## <a name="supported-operating-systems"></a><span data-ttu-id="3732a-120">Sistemas operacionais com suporte</span><span class="sxs-lookup"><span data-stu-id="3732a-120">Supported Operating Systems</span></span>

<span data-ttu-id="3732a-121">Links simbólicos estão disponíveis em NTFS a partir do Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="3732a-121">Symbolic links are available in NTFS starting with Windows Vista.</span></span>

 

 




