---
description: 'Saiba mais sobre: macros da API do gabinete'
ms.assetid: 85fade43-9fcb-4100-a734-8b36d132b2c0
title: Macros da API do gabinete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 390fa42e0293e5d47c405e8e99986538b8f26254
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104500754"
---
# <a name="cabinet-api-macros"></a><span data-ttu-id="f2abd-103">Macros da API do gabinete</span><span class="sxs-lookup"><span data-stu-id="f2abd-103">Cabinet API Macros</span></span>

<span data-ttu-id="f2abd-104">Esta seção detalha as macros usadas pela API do gabinete:</span><span class="sxs-lookup"><span data-stu-id="f2abd-104">This section details the macros used by the Cabinet API:</span></span>

## <a name="fci-macros"></a><span data-ttu-id="f2abd-105">FCI macros</span><span class="sxs-lookup"><span data-stu-id="f2abd-105">FCI Macros</span></span>

<span data-ttu-id="f2abd-106">As macros a seguir são usadas pelo FCI:</span><span class="sxs-lookup"><span data-stu-id="f2abd-106">The following macros are used by FCI:</span></span>



| <span data-ttu-id="f2abd-107">Macro</span><span class="sxs-lookup"><span data-stu-id="f2abd-107">Macro</span></span>                                              | <span data-ttu-id="f2abd-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="f2abd-108">Description</span></span>                                                                                    |
|----------------------------------------------------|------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f2abd-109">**FNFCIALLOC**</span><span class="sxs-lookup"><span data-stu-id="f2abd-109">**FNFCIALLOC**</span></span>](/windows/desktop/api/fci/nf-fci-fnfcialloc)                   | <span data-ttu-id="f2abd-110">Usado para alocar memória em um contexto de FCI.</span><span class="sxs-lookup"><span data-stu-id="f2abd-110">Used to allocate memory in an FCI context.</span></span><br/>                                          |
| [<span data-ttu-id="f2abd-111">**FNFCICLOSE**</span><span class="sxs-lookup"><span data-stu-id="f2abd-111">**FNFCICLOSE**</span></span>](/windows/desktop/api/fci/nf-fci-fnfciclose)                   | <span data-ttu-id="f2abd-112">Usado para fechar um arquivo.</span><span class="sxs-lookup"><span data-stu-id="f2abd-112">Used to close a file.</span></span><br/>                                                               |
| [<span data-ttu-id="f2abd-113">**FNFCIDELETE**</span><span class="sxs-lookup"><span data-stu-id="f2abd-113">**FNFCIDELETE**</span></span>](/windows/desktop/api/fci/nf-fci-fnfcidelete)                 | <span data-ttu-id="f2abd-114">Usado para excluir um arquivo.</span><span class="sxs-lookup"><span data-stu-id="f2abd-114">Used to delete a file.</span></span><br/>                                                              |
| [<span data-ttu-id="f2abd-115">**FNFCIFILEPLACED**</span><span class="sxs-lookup"><span data-stu-id="f2abd-115">**FNFCIFILEPLACED**</span></span>](/windows/desktop/api/fci/nf-fci-fnfcifileplaced)         | <span data-ttu-id="f2abd-116">Usado para notificar quando um arquivo é colocado no gabinete.</span><span class="sxs-lookup"><span data-stu-id="f2abd-116">Used to notify when a file is placed in the cabinet.</span></span><br/>                                |
| [<span data-ttu-id="f2abd-117">**FNFCIFREE**</span><span class="sxs-lookup"><span data-stu-id="f2abd-117">**FNFCIFREE**</span></span>](/windows/desktop/api/fci/nf-fci-fnfcifree)                     | <span data-ttu-id="f2abd-118">Usado para liberar a memória alocada anteriormente em um contexto de FCI.</span><span class="sxs-lookup"><span data-stu-id="f2abd-118">Used to free previously allocated memory in an FCI context.</span></span><br/>                         |
| [<span data-ttu-id="f2abd-119">**FNFCIGETNEXTCABINET**</span><span class="sxs-lookup"><span data-stu-id="f2abd-119">**FNFCIGETNEXTCABINET**</span></span>](/windows/desktop/api/fci/nf-fci-fnfcigetnextcabinet) | <span data-ttu-id="f2abd-120">Usado para solicitar informações para o próximo gabinete.</span><span class="sxs-lookup"><span data-stu-id="f2abd-120">Used to request information for the next cabinet.</span></span><br/>                                   |
| [<span data-ttu-id="f2abd-121">**FNFCIGETOPENINFO**</span><span class="sxs-lookup"><span data-stu-id="f2abd-121">**FNFCIGETOPENINFO**</span></span>](/windows/desktop/api/fci/nf-fci-fnfcigetopeninfo)       | <span data-ttu-id="f2abd-122">Usado para abrir um arquivo e recuperar a data, a hora e os atributos do arquivo.</span><span class="sxs-lookup"><span data-stu-id="f2abd-122">Used to open a file and retrieve file date, time, and attributes.</span></span><br/>                   |
| [<span data-ttu-id="f2abd-123">**FNFCIGETTEMPFILE**</span><span class="sxs-lookup"><span data-stu-id="f2abd-123">**FNFCIGETTEMPFILE**</span></span>](/windows/desktop/api/fci/nf-fci-fnfcigettempfile)       | <span data-ttu-id="f2abd-124">Usado para obter um nome de arquivo temporário.</span><span class="sxs-lookup"><span data-stu-id="f2abd-124">Used to obtain a temporary file name.</span></span><br/>                                               |
| [<span data-ttu-id="f2abd-125">**FNFCIOPEN**</span><span class="sxs-lookup"><span data-stu-id="f2abd-125">**FNFCIOPEN**</span></span>](/windows/desktop/api/fci/nf-fci-fnfciopen)                     | <span data-ttu-id="f2abd-126">Usado para abrir um arquivo em um contexto FCI.</span><span class="sxs-lookup"><span data-stu-id="f2abd-126">Used to open a file in an FCI context.</span></span><br/>                                              |
| [<span data-ttu-id="f2abd-127">**FNFCIREAD**</span><span class="sxs-lookup"><span data-stu-id="f2abd-127">**FNFCIREAD**</span></span>](/windows/desktop/api/fci/nf-fci-fnfciread)                     | <span data-ttu-id="f2abd-128">Usado para ler dados de um arquivo.</span><span class="sxs-lookup"><span data-stu-id="f2abd-128">Used to read data from a file.</span></span><br/>                                                      |
| [<span data-ttu-id="f2abd-129">**FNFCISEEK**</span><span class="sxs-lookup"><span data-stu-id="f2abd-129">**FNFCISEEK**</span></span>](/windows/desktop/api/fci/nf-fci-fnfciseek)                     | <span data-ttu-id="f2abd-130">Usado para mover um ponteiro de arquivo para um local especificado.</span><span class="sxs-lookup"><span data-stu-id="f2abd-130">Used to move a file pointer to a specified location.</span></span><br/>                                |
| [<span data-ttu-id="f2abd-131">**FNFCISTATUS**</span><span class="sxs-lookup"><span data-stu-id="f2abd-131">**FNFCISTATUS**</span></span>](/windows/desktop/api/fci/nf-fci-fnfcistatus)                 | <span data-ttu-id="f2abd-132">Usado para atualizar o usuário.</span><span class="sxs-lookup"><span data-stu-id="f2abd-132">Used to update the user.</span></span><br/>                                                            |
| [<span data-ttu-id="f2abd-133">**FNFCIWRITE**</span><span class="sxs-lookup"><span data-stu-id="f2abd-133">**FNFCIWRITE**</span></span>](/windows/desktop/api/fci/nf-fci-fnfciwrite)                   | <span data-ttu-id="f2abd-134">Usado para gravar dados em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="f2abd-134">Used to write data to a file.</span></span><br/>                                                       |
| [<span data-ttu-id="f2abd-135">**TCOMPfromLZXWindow**</span><span class="sxs-lookup"><span data-stu-id="f2abd-135">**TCOMPfromLZXWindow**</span></span>](/windows/desktop/api/fdi_fci_types/nf-fdi_fci_types-tcompfromlzxwindow)   | <span data-ttu-id="f2abd-136">Converte o tamanho do Windows em um valor de TCOMP LXZ para [**FCIAddFile**](/windows/desktop/api/Fci/nf-fci-fciaddfile).</span><span class="sxs-lookup"><span data-stu-id="f2abd-136">Converts windows size into an LXZ TCOMP value for [**FCIAddFile**](/windows/desktop/api/Fci/nf-fci-fciaddfile).</span></span><br/> |



 

## <a name="fdi-macros"></a><span data-ttu-id="f2abd-137">Macros FDI</span><span class="sxs-lookup"><span data-stu-id="f2abd-137">FDI Macros</span></span>

<span data-ttu-id="f2abd-138">As macros a seguir são usadas por FDI:</span><span class="sxs-lookup"><span data-stu-id="f2abd-138">The following macros are used by FDI:</span></span>



| <span data-ttu-id="f2abd-139">Macro</span><span class="sxs-lookup"><span data-stu-id="f2abd-139">Macro</span></span>                              | <span data-ttu-id="f2abd-140">Descrição</span><span class="sxs-lookup"><span data-stu-id="f2abd-140">Description</span></span>                                                                         |
|------------------------------------|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="f2abd-141">**FNALLOC**</span><span class="sxs-lookup"><span data-stu-id="f2abd-141">**FNALLOC**</span></span>](/windows/desktop/api/fdi/nf-fdi-fnalloc)         | <span data-ttu-id="f2abd-142">Usado para alocar memória em um contexto FDI.</span><span class="sxs-lookup"><span data-stu-id="f2abd-142">Used to allocate memory in an FDI context.</span></span><br/>                               |
| [<span data-ttu-id="f2abd-143">**FNCLOSE**</span><span class="sxs-lookup"><span data-stu-id="f2abd-143">**FNCLOSE**</span></span>](/windows/desktop/api/fdi/nf-fdi-fnclose)         | <span data-ttu-id="f2abd-144">Usado para fechar um arquivo em um contexto FDI.</span><span class="sxs-lookup"><span data-stu-id="f2abd-144">Used to close a file in an FDI context.</span></span><br/>                                  |
| [<span data-ttu-id="f2abd-145">**FNFDINOTIFY**</span><span class="sxs-lookup"><span data-stu-id="f2abd-145">**FNFDINOTIFY**</span></span>](/windows/desktop/api/fdi/nf-fdi-fnfdinotify) | <span data-ttu-id="f2abd-146">Usado para atualizar o aplicativo no status do decodificador.</span><span class="sxs-lookup"><span data-stu-id="f2abd-146">Used to update the application on the status of the decoder.</span></span><br/>             |
| [<span data-ttu-id="f2abd-147">**FNFREE**</span><span class="sxs-lookup"><span data-stu-id="f2abd-147">**FNFREE**</span></span>](/windows/desktop/api/fdi/nf-fdi-fnfree)           | <span data-ttu-id="f2abd-148">Usado para liberar a memória alocada anteriormente em um contexto FDI.</span><span class="sxs-lookup"><span data-stu-id="f2abd-148">Used to free previously allocated memory in an FDI context.</span></span><br/>              |
| [<span data-ttu-id="f2abd-149">**FNOPEN**</span><span class="sxs-lookup"><span data-stu-id="f2abd-149">**FNOPEN**</span></span>](/windows/desktop/api/fdi/nf-fdi-fnopen)           | <span data-ttu-id="f2abd-150">Usado para abrir um arquivo em um contexto FDI.</span><span class="sxs-lookup"><span data-stu-id="f2abd-150">Used to open a file in an FDI context.</span></span><br/>                                   |
| [<span data-ttu-id="f2abd-151">**FNREAD**</span><span class="sxs-lookup"><span data-stu-id="f2abd-151">**FNREAD**</span></span>](/windows/desktop/api/fdi/nf-fdi-fnread)           | <span data-ttu-id="f2abd-152">Usado para ler dados de um arquivo em um contexto FDI.</span><span class="sxs-lookup"><span data-stu-id="f2abd-152">Used to read data from a file in an FDI context.</span></span><br/>                         |
| [<span data-ttu-id="f2abd-153">**FNSEEK**</span><span class="sxs-lookup"><span data-stu-id="f2abd-153">**FNSEEK**</span></span>](/windows/desktop/api/fdi/nf-fdi-fnseek)           | <span data-ttu-id="f2abd-154">Usado para mover um ponteiro de arquivo para o local especificado em um contexto FDI.</span><span class="sxs-lookup"><span data-stu-id="f2abd-154">Used to move a file pointer to the specified location in an FDI context.</span></span><br/> |
| [<span data-ttu-id="f2abd-155">**FNWRITE**</span><span class="sxs-lookup"><span data-stu-id="f2abd-155">**FNWRITE**</span></span>](/windows/desktop/api/fdi/nf-fdi-fnwrite)         | <span data-ttu-id="f2abd-156">Usado para gravar dados em um arquivo em um contexto FDI.</span><span class="sxs-lookup"><span data-stu-id="f2abd-156">Used to write data to a file in an FDI context.</span></span><br/>                          |



 

## <a name="related-topics"></a><span data-ttu-id="f2abd-157">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f2abd-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f2abd-158">Referência de API de gabinete</span><span class="sxs-lookup"><span data-stu-id="f2abd-158">Cabinet API Reference</span></span>](cabinet-api-reference.md)
</dt> <dt>

[<span data-ttu-id="f2abd-159">Usando a API do gabinete</span><span class="sxs-lookup"><span data-stu-id="f2abd-159">Using the Cabinet API</span></span>](using-the-cabinet-api.md)
</dt> </dl>

 

 




