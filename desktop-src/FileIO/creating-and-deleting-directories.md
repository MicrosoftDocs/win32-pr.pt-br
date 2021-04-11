---
description: Um aplicativo pode criar e excluir diretórios programaticamente.
ms.assetid: 52d1d8a8-e5a7-44f5-9bf2-2a496ef79d32
title: Criando e excluindo diretórios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 140547594271e13bc78bfa78336f167f228879a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091023"
---
# <a name="creating-and-deleting-directories"></a><span data-ttu-id="c0e18-103">Criando e excluindo diretórios</span><span class="sxs-lookup"><span data-stu-id="c0e18-103">Creating and Deleting Directories</span></span>

<span data-ttu-id="c0e18-104">Um aplicativo pode criar e excluir diretórios programaticamente.</span><span class="sxs-lookup"><span data-stu-id="c0e18-104">An application can programmatically create and delete directories.</span></span>

<span data-ttu-id="c0e18-105">Para criar um novo diretório, use a função [**CreateDirectory**](/windows/desktop/api/FileAPI/nf-fileapi-createdirectorya), [**CreateDirectoryEx**](/windows/desktop/api/WinBase/nf-winbase-createdirectoryexa)ou [**CreateDirectoryTransacted**](/windows/desktop/api/WinBase/nf-winbase-createdirectorytransacteda) .</span><span class="sxs-lookup"><span data-stu-id="c0e18-105">To create a new directory, use the [**CreateDirectory**](/windows/desktop/api/FileAPI/nf-fileapi-createdirectorya), [**CreateDirectoryEx**](/windows/desktop/api/WinBase/nf-winbase-createdirectoryexa), or [**CreateDirectoryTransacted**](/windows/desktop/api/WinBase/nf-winbase-createdirectorytransacteda) function.</span></span> <span data-ttu-id="c0e18-106">Um diretório recebe o nome especificado quando ele é criado.</span><span class="sxs-lookup"><span data-stu-id="c0e18-106">A directory is given the name specified when it is created.</span></span> <span data-ttu-id="c0e18-107">As convenções para nomear um diretório seguem as convenções para nomear um arquivo.</span><span class="sxs-lookup"><span data-stu-id="c0e18-107">The conventions for naming a directory follow the conventions for naming a file.</span></span> <span data-ttu-id="c0e18-108">Para obter uma descrição dessas convenções, consulte [nomeando um arquivo](naming-a-file.md).</span><span class="sxs-lookup"><span data-stu-id="c0e18-108">For a description of these conventions, see [Naming a File](naming-a-file.md).</span></span>

<span data-ttu-id="c0e18-109">Para excluir um diretório existente, use a função [**RemoveDirectory**](/windows/desktop/api/FileAPI/nf-fileapi-removedirectorya) ou [**RemoveDirectoryTransacted**](/windows/desktop/api/WinBase/nf-winbase-removedirectorytransacteda) .</span><span class="sxs-lookup"><span data-stu-id="c0e18-109">To delete an existing directory, use the [**RemoveDirectory**](/windows/desktop/api/FileAPI/nf-fileapi-removedirectorya) or [**RemoveDirectoryTransacted**](/windows/desktop/api/WinBase/nf-winbase-removedirectorytransacteda) function.</span></span> <span data-ttu-id="c0e18-110">Antes de remover um diretório, você deve garantir que o diretório esteja vazio e que você tenha o privilégio de acesso de exclusão para o diretório.</span><span class="sxs-lookup"><span data-stu-id="c0e18-110">Before removing a directory, you must ensure that the directory is empty and that you have the delete access privilege for the directory.</span></span> <span data-ttu-id="c0e18-111">Para fazer o último, chame a função [**GetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) .</span><span class="sxs-lookup"><span data-stu-id="c0e18-111">To do the latter, call the [**GetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) function.</span></span>

 

 
