---
title: Interface IDODownload
description: Usado para iniciar e gerenciar um download.
keywords:
- Interface IDODownload
topic_type:
- apiref
api_name:
- IDODownload
api_location:
- do.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: ec2f74ce7daae6f612297d21e15e6993fcd78382
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294102"
---
# <a name="idodownload-interface"></a><span data-ttu-id="11c75-104">Interface IDODownload</span><span class="sxs-lookup"><span data-stu-id="11c75-104">IDODownload interface</span></span>

<span data-ttu-id="11c75-105">A interface **IDODownload** é usada para iniciar e gerenciar um download.</span><span class="sxs-lookup"><span data-stu-id="11c75-105">The **IDODownload** interface is used to start and manage a download.</span></span>

## <a name="methods"></a><span data-ttu-id="11c75-106">Métodos</span><span class="sxs-lookup"><span data-stu-id="11c75-106">Methods</span></span>

<span data-ttu-id="11c75-107">A interface **IDODownload** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="11c75-107">The **IDODownload** interface has these methods.</span></span>

| <span data-ttu-id="11c75-108">Método</span><span class="sxs-lookup"><span data-stu-id="11c75-108">Method</span></span> | <span data-ttu-id="11c75-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="11c75-109">Description</span></span> |
| ---- |:---- |
| [<span data-ttu-id="11c75-110">IDODownload:: Abort</span><span class="sxs-lookup"><span data-stu-id="11c75-110">IDODownload::Abort</span></span>](./nf-do-idomanager-createdownload.md) | <span data-ttu-id="11c75-111">Anula o download.</span><span class="sxs-lookup"><span data-stu-id="11c75-111">Aborts the download.</span></span> |
| [<span data-ttu-id="11c75-112">IDODownload:: Finalize</span><span class="sxs-lookup"><span data-stu-id="11c75-112">IDODownload::Finalize</span></span>](./nf-do-idodownload-finalize.md) | <span data-ttu-id="11c75-113">Finaliza o download.</span><span class="sxs-lookup"><span data-stu-id="11c75-113">Finalizes the download.</span></span> |
| [<span data-ttu-id="11c75-114">IDODownload:: GetProperty</span><span class="sxs-lookup"><span data-stu-id="11c75-114">IDODownload::GetProperty</span></span>](./nf-do-idodownload-getproperty.md) | <span data-ttu-id="11c75-115">Recupera um ponteiro para uma **variante** que contém uma propriedade de download específica.</span><span class="sxs-lookup"><span data-stu-id="11c75-115">Retrieves a pointer to a **VARIANT** that contains a specific download property.</span></span> |
| [<span data-ttu-id="11c75-116">IDODownload:: GetStatus</span><span class="sxs-lookup"><span data-stu-id="11c75-116">IDODownload::GetStatus</span></span>](./nf-do-idodownload-getstatus.md) | <span data-ttu-id="11c75-117">Recupera um ponteiro para uma estrutura de **DO_DOWNLOAD_STATUS** que reflete o status atual do download.</span><span class="sxs-lookup"><span data-stu-id="11c75-117">Retrieves a pointer to a **DO_DOWNLOAD_STATUS** structure that reflects the current status of the download.</span></span> |
| [<span data-ttu-id="11c75-118">IDODownload::P ause</span><span class="sxs-lookup"><span data-stu-id="11c75-118">IDODownload::Pause</span></span>](./nf-do-idodownload-pause.md) | <span data-ttu-id="11c75-119">Pausa o download.</span><span class="sxs-lookup"><span data-stu-id="11c75-119">Pauses the download.</span></span> |
| [<span data-ttu-id="11c75-120">IDODownload:: SetProperty</span><span class="sxs-lookup"><span data-stu-id="11c75-120">IDODownload::SetProperty</span></span>](./nf-do-idodownload-setproperty.md) | <span data-ttu-id="11c75-121">Define uma propriedade de download.</span><span class="sxs-lookup"><span data-stu-id="11c75-121">Sets a download property.</span></span> |
| [<span data-ttu-id="11c75-122">IDODownload:: iniciar</span><span class="sxs-lookup"><span data-stu-id="11c75-122">IDODownload::Start</span></span>](./nf-do-idodownload-start.md) | <span data-ttu-id="11c75-123">Inicia ou retoma um download.</span><span class="sxs-lookup"><span data-stu-id="11c75-123">Starts or resumes a download.</span></span> |

## <a name="requirements"></a><span data-ttu-id="11c75-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="11c75-124">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="11c75-125">**Cliente mínimo com suporte**</span><span class="sxs-lookup"><span data-stu-id="11c75-125">**Minimum supported client**</span></span> | <span data-ttu-id="11c75-126">Somente aplicativos do Windows 10, versão 1809 \[ Win32\]</span><span class="sxs-lookup"><span data-stu-id="11c75-126">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="11c75-127">**Servidor mínimo com suporte**</span><span class="sxs-lookup"><span data-stu-id="11c75-127">**Minimum supported server**</span></span> | <span data-ttu-id="11c75-128">Somente aplicativos do Windows Server, versão 1809 \[ Win32\]</span><span class="sxs-lookup"><span data-stu-id="11c75-128">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="11c75-129">**Cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="11c75-129">**Header**</span></span> | <span data-ttu-id="11c75-130">Do. h</span><span class="sxs-lookup"><span data-stu-id="11c75-130">Do.h</span></span> |