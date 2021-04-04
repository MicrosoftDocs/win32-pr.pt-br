---
description: Funções usadas no gerenciamento de diretório.
ms.assetid: 5517b0e7-2264-4173-8e10-ff7626458bfa
title: Funções de gerenciamento de diretório
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00bc10d0f8d7caddc1ea821c397e16edf600d92c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171145"
---
# <a name="directory-management-functions"></a><span data-ttu-id="f4678-103">Funções de gerenciamento de diretório</span><span class="sxs-lookup"><span data-stu-id="f4678-103">Directory Management Functions</span></span>

<span data-ttu-id="f4678-104">As funções a seguir são usadas no gerenciamento de diretório.</span><span class="sxs-lookup"><span data-stu-id="f4678-104">The following functions are used in directory management.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="f4678-105">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="f4678-105">In this section</span></span>



| <span data-ttu-id="f4678-106">Função</span><span class="sxs-lookup"><span data-stu-id="f4678-106">Function</span></span>                                                                      | <span data-ttu-id="f4678-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="f4678-107">Description</span></span>                                                                                                                                                               |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f4678-108">**CreateDirectory**</span><span class="sxs-lookup"><span data-stu-id="f4678-108">**CreateDirectory**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-createdirectorya)<br/>                         | <span data-ttu-id="f4678-109">Cria um novo diretório.</span><span class="sxs-lookup"><span data-stu-id="f4678-109">Creates a new directory.</span></span><br/>                                                                                                                                       |
| [<span data-ttu-id="f4678-110">**CreateDirectoryEx**</span><span class="sxs-lookup"><span data-stu-id="f4678-110">**CreateDirectoryEx**</span></span>](/windows/desktop/api/WinBase/nf-winbase-createdirectoryexa)<br/>                     | <span data-ttu-id="f4678-111">Cria um novo diretório com os atributos de um diretório de modelo especificado.</span><span class="sxs-lookup"><span data-stu-id="f4678-111">Creates a new directory with the attributes of a specified template directory.</span></span><br/>                                                                                 |
| [<span data-ttu-id="f4678-112">**CreateDirectoryTransacted**</span><span class="sxs-lookup"><span data-stu-id="f4678-112">**CreateDirectoryTransacted**</span></span>](/windows/desktop/api/WinBase/nf-winbase-createdirectorytransacteda)<br/>     | <span data-ttu-id="f4678-113">Cria um novo diretório como uma operação transacionada, com os atributos de um diretório de modelo especificado.</span><span class="sxs-lookup"><span data-stu-id="f4678-113">Creates a new directory as a transacted operation, with the attributes of a specified template directory.</span></span><br/>                                                      |
| [<span data-ttu-id="f4678-114">**FindCloseChangeNotification**</span><span class="sxs-lookup"><span data-stu-id="f4678-114">**FindCloseChangeNotification**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-findclosechangenotification)<br/> | <span data-ttu-id="f4678-115">Interrompe o monitoramento do identificador de notificação de alteração.</span><span class="sxs-lookup"><span data-stu-id="f4678-115">Stops change notification handle monitoring.</span></span><br/>                                                                                                                   |
| [<span data-ttu-id="f4678-116">**FindFirstChangeNotification**</span><span class="sxs-lookup"><span data-stu-id="f4678-116">**FindFirstChangeNotification**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-findfirstchangenotificationa)<br/> | <span data-ttu-id="f4678-117">Cria um identificador de notificação de alteração e configura as condições de filtro de notificação de alteração iniciais.</span><span class="sxs-lookup"><span data-stu-id="f4678-117">Creates a change notification handle and sets up initial change notification filter conditions.</span></span><br/>                                                                |
| [<span data-ttu-id="f4678-118">**FindNextChangeNotification**</span><span class="sxs-lookup"><span data-stu-id="f4678-118">**FindNextChangeNotification**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-findnextchangenotification)<br/>   | <span data-ttu-id="f4678-119">Solicita que o sistema operacional sinalize um identificador de notificação de alteração na próxima vez que detectar uma alteração apropriada.</span><span class="sxs-lookup"><span data-stu-id="f4678-119">Requests that the operating system signal a change notification handle the next time it detects an appropriate change.</span></span><br/>                                         |
| [<span data-ttu-id="f4678-120">**GetCurrentDirectory**</span><span class="sxs-lookup"><span data-stu-id="f4678-120">**GetCurrentDirectory**</span></span>](/windows/desktop/api/WinBase/nf-winbase-getcurrentdirectory)<br/>                 | <span data-ttu-id="f4678-121">Recupera o diretório atual para o processo atual.</span><span class="sxs-lookup"><span data-stu-id="f4678-121">Retrieves the current directory for the current process.</span></span><br/>                                                                                                       |
| [<span data-ttu-id="f4678-122">**ReadDirectoryChangesExW**</span><span class="sxs-lookup"><span data-stu-id="f4678-122">**ReadDirectoryChangesExW**</span></span>](/windows/desktop/api/WinBase/nf-winbase-readdirectorychangesexw)<br/>         | <span data-ttu-id="f4678-123">Recupera informações que descrevem as alterações no diretório especificado, que pode incluir informações estendidas se esse tipo de informação for especificado.</span><span class="sxs-lookup"><span data-stu-id="f4678-123">Retrieves information that describes the changes within the specified directory, which can include extended information if that information type is specified.</span></span><br/> |
| [<span data-ttu-id="f4678-124">**ReadDirectoryChangesW**</span><span class="sxs-lookup"><span data-stu-id="f4678-124">**ReadDirectoryChangesW**</span></span>](/windows/desktop/api/WinBase/nf-winbase-readdirectorychangesw)<br/>             | <span data-ttu-id="f4678-125">Recupera informações que descrevem as alterações no diretório especificado.</span><span class="sxs-lookup"><span data-stu-id="f4678-125">Retrieves information that describes the changes within the specified directory.</span></span><br/>                                                                               |
| [<span data-ttu-id="f4678-126">**RemoveDirectory**</span><span class="sxs-lookup"><span data-stu-id="f4678-126">**RemoveDirectory**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-removedirectorya)<br/>                         | <span data-ttu-id="f4678-127">Exclui um diretório vazio existente.</span><span class="sxs-lookup"><span data-stu-id="f4678-127">Deletes an existing empty directory.</span></span><br/>                                                                                                                           |
| [<span data-ttu-id="f4678-128">**RemoveDirectoryTransacted**</span><span class="sxs-lookup"><span data-stu-id="f4678-128">**RemoveDirectoryTransacted**</span></span>](/windows/desktop/api/WinBase/nf-winbase-removedirectorytransacteda)<br/>     | <span data-ttu-id="f4678-129">Exclui um diretório vazio existente como uma operação transacionada.</span><span class="sxs-lookup"><span data-stu-id="f4678-129">Deletes an existing empty directory as a transacted operation.</span></span><br/>                                                                                                 |
| [<span data-ttu-id="f4678-130">**SetCurrentDirectory**</span><span class="sxs-lookup"><span data-stu-id="f4678-130">**SetCurrentDirectory**</span></span>](/windows/desktop/api/WinBase/nf-winbase-setcurrentdirectory)<br/>                 | <span data-ttu-id="f4678-131">Altera o diretório atual para o processo atual.</span><span class="sxs-lookup"><span data-stu-id="f4678-131">Changes the current directory for the current process.</span></span><br/>                                                                                                         |



 

 

 




