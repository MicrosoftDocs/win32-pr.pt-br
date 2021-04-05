---
description: Um diretório que contém um ou mais diretórios é o pai do diretório ou dos diretórios contidos, e cada diretório contido é um filho do diretório pai. A estrutura hierárquica de diretórios é conhecida como árvore de diretórios.
ms.assetid: e8a7bf82-0f3c-4ad9-9d10-25c4d69733dc
title: Sobre o gerenciamento de diretório
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02e3a90b6cc99a480f798e632512770c904291a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827159"
---
# <a name="about-directory-management"></a><span data-ttu-id="3eff2-104">Sobre o gerenciamento de diretório</span><span class="sxs-lookup"><span data-stu-id="3eff2-104">About Directory Management</span></span>

<span data-ttu-id="3eff2-105">Um diretório que contém um ou mais diretórios é o *pai* do diretório ou dos diretórios contidos, e cada diretório contido é um *filho* do diretório pai.</span><span class="sxs-lookup"><span data-stu-id="3eff2-105">A directory that contains one or more directories is the *parent* of the contained directory or directories, and each contained directory is a *child* of the parent directory.</span></span> <span data-ttu-id="3eff2-106">A estrutura hierárquica de diretórios é conhecida como árvore de *diretórios*.</span><span class="sxs-lookup"><span data-stu-id="3eff2-106">The hierarchical structure of directories is referred to as a *directory tree*.</span></span>

<span data-ttu-id="3eff2-107">O sistema de arquivos NTFS implementa o link lógico entre um diretório e os arquivos que ele contém como uma *tabela de entrada de diretório*.</span><span class="sxs-lookup"><span data-stu-id="3eff2-107">The NTFS file system implements the logical link between a directory and the files it contains as a *directory entry table*.</span></span> <span data-ttu-id="3eff2-108">Quando um arquivo é movido para um diretório, uma entrada é criada na tabela para o arquivo movido e o nome do arquivo é colocado na entrada.</span><span class="sxs-lookup"><span data-stu-id="3eff2-108">When a file is moved into a directory, an entry is created in the table for the moved file and the name of the file is placed in the entry.</span></span> <span data-ttu-id="3eff2-109">Quando um arquivo contido em um diretório é excluído, o nome e a entrada correspondentes ao arquivo excluído também são excluídos da tabela.</span><span class="sxs-lookup"><span data-stu-id="3eff2-109">When a file contained in a directory is deleted, the name and entry corresponding to the deleted file is also deleted from the table.</span></span> <span data-ttu-id="3eff2-110">Mais de uma entrada para um único arquivo pode existir em uma tabela de entrada de diretório.</span><span class="sxs-lookup"><span data-stu-id="3eff2-110">More than one entry for a single file can exist in a directory entry table.</span></span> <span data-ttu-id="3eff2-111">Se uma entrada adicional for criada na tabela para um arquivo, essa entrada será referida como um *link físico* para esse arquivo.</span><span class="sxs-lookup"><span data-stu-id="3eff2-111">If an additional entry is created in the table for a file, that entry is referred to as a *hard link* to that file.</span></span> <span data-ttu-id="3eff2-112">Não há nenhum limite para o número de links físicos que podem ser criados para um único arquivo.</span><span class="sxs-lookup"><span data-stu-id="3eff2-112">There is no limit to the number of hard links that can be created for a single file.</span></span>

<span data-ttu-id="3eff2-113">Os diretórios também podem conter junções e pontos de nova análise.</span><span class="sxs-lookup"><span data-stu-id="3eff2-113">Directories can also contain junctions and reparse points.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="3eff2-114">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="3eff2-114">In this section</span></span>



| <span data-ttu-id="3eff2-115">Tópico</span><span class="sxs-lookup"><span data-stu-id="3eff2-115">Topic</span></span>                                                                                 | <span data-ttu-id="3eff2-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="3eff2-116">Description</span></span>                                                                                            |
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3eff2-117">Criando e excluindo diretórios</span><span class="sxs-lookup"><span data-stu-id="3eff2-117">Creating and Deleting Directories</span></span>](creating-and-deleting-directories.md)<br/> | <span data-ttu-id="3eff2-118">Um aplicativo pode criar e excluir diretórios programaticamente.</span><span class="sxs-lookup"><span data-stu-id="3eff2-118">An application can programmatically create and delete directories.</span></span><br/>                          |
| [<span data-ttu-id="3eff2-119">Identificadores de diretório</span><span class="sxs-lookup"><span data-stu-id="3eff2-119">Directory Handles</span></span>](obtaining-a-handle-to-a-directory.md)<br/>                 | <span data-ttu-id="3eff2-120">Sempre que um processo cria ou abre um objeto de diretório, ele recebe um identificador para o objeto.</span><span class="sxs-lookup"><span data-stu-id="3eff2-120">Whenever a process creates or opens a directory object, it receives a handle to the object.</span></span><br/> |
| [<span data-ttu-id="3eff2-121">Pontos de reanálise</span><span class="sxs-lookup"><span data-stu-id="3eff2-121">Reparse Points</span></span>](reparse-points.md)<br/>                                       | <span data-ttu-id="3eff2-122">Descreve pontos de nova análise.</span><span class="sxs-lookup"><span data-stu-id="3eff2-122">Describes reparse points.</span></span><br/>                                                                   |



 

## <a name="related-topics"></a><span data-ttu-id="3eff2-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3eff2-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3eff2-124">Referência de gerenciamento de diretório</span><span class="sxs-lookup"><span data-stu-id="3eff2-124">Directory Management Reference</span></span>](directory-management-reference.md)
</dt> </dl>

 

 




