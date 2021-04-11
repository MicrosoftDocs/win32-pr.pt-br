---
description: Funções usadas para gerenciar pastas montadas.
ms.assetid: 2624500b-11d6-4892-97d7-22efa450f681
title: Funções de pasta montadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3e984b9bee902f11af9d7b2b956ea0681cd6e7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104296865"
---
# <a name="mounted-folder-functions"></a><span data-ttu-id="e2761-103">Funções de pasta montadas</span><span class="sxs-lookup"><span data-stu-id="e2761-103">Mounted Folder Functions</span></span>

<span data-ttu-id="e2761-104">As funções de pasta montadas podem ser divididas em três grupos: funções de finalidade geral, funções usadas para examinar volumes e funções usadas para examinar um volume para pastas montadas.</span><span class="sxs-lookup"><span data-stu-id="e2761-104">The mounted folder functions can be divided into three groups: general-purpose functions, functions used to scan for volumes, and functions used to scan a volume for mounted folders.</span></span>

## <a name="general-purpose-mounted-folder-functions"></a><span data-ttu-id="e2761-105">General-Purpose funções de pasta montadas</span><span class="sxs-lookup"><span data-stu-id="e2761-105">General-Purpose Mounted Folder Functions</span></span>



| <span data-ttu-id="e2761-106">Função</span><span class="sxs-lookup"><span data-stu-id="e2761-106">Function</span></span>                                                                     | <span data-ttu-id="e2761-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="e2761-107">Description</span></span>                                                                                                                                                 |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e2761-108">**DeleteVolumeMountPoint**</span><span class="sxs-lookup"><span data-stu-id="e2761-108">**DeleteVolumeMountPoint**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-deletevolumemountpointw)                     | <span data-ttu-id="e2761-109">Exclui uma letra da unidade ou uma pasta montada.</span><span class="sxs-lookup"><span data-stu-id="e2761-109">Deletes a drive letter or mounted folder.</span></span>                                                                                                                   |
| [<span data-ttu-id="e2761-110">**GetVolumeNameForVolumeMountPoint**</span><span class="sxs-lookup"><span data-stu-id="e2761-110">**GetVolumeNameForVolumeMountPoint**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-getvolumenameforvolumemountpointw) | <span data-ttu-id="e2761-111">Recupera o caminho do volume GUID do volume que está associado ao ponto de montagem do volume especificado (letra da unidade, caminho do GUID do volume ou pasta montada).</span><span class="sxs-lookup"><span data-stu-id="e2761-111">Retrieves the volume GUID path for the volume that is associated with the specified volume mount point (drive letter, volume GUID path, or mounted folder).</span></span> |
| [<span data-ttu-id="e2761-112">**GetVolumePathName**</span><span class="sxs-lookup"><span data-stu-id="e2761-112">**GetVolumePathName**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-getvolumepathnamew)                               | <span data-ttu-id="e2761-113">Recupera a pasta montada que está associada ao volume especificado.</span><span class="sxs-lookup"><span data-stu-id="e2761-113">Retrieves the mounted folder that is associated with the specified volume.</span></span>                                                                                  |
| [<span data-ttu-id="e2761-114">**SetVolumeMountPoint**</span><span class="sxs-lookup"><span data-stu-id="e2761-114">**SetVolumeMountPoint**</span></span>](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa)                           | <span data-ttu-id="e2761-115">Associa um volume com uma letra de unidade ou um diretório em outro volume.</span><span class="sxs-lookup"><span data-stu-id="e2761-115">Associates a volume with a drive letter or a directory on another volume.</span></span>                                                                                   |



 

## <a name="volume-scanning-functions"></a><span data-ttu-id="e2761-116">Funções de Volume-Scanning</span><span class="sxs-lookup"><span data-stu-id="e2761-116">Volume-Scanning Functions</span></span>



| <span data-ttu-id="e2761-117">Função</span><span class="sxs-lookup"><span data-stu-id="e2761-117">Function</span></span>                                   | <span data-ttu-id="e2761-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="e2761-118">Description</span></span>                                                                                                                                    |
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e2761-119">**FindFirstVolume**</span><span class="sxs-lookup"><span data-stu-id="e2761-119">**FindFirstVolume**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew) | <span data-ttu-id="e2761-120">Retorna o nome de um volume em um computador.</span><span class="sxs-lookup"><span data-stu-id="e2761-120">Returns the name of a volume on a computer.</span></span> <span data-ttu-id="e2761-121">[**FindFirstVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew) é usado para começar a enumerar os volumes de um computador.</span><span class="sxs-lookup"><span data-stu-id="e2761-121">[**FindFirstVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew) is used to begin enumerating the volumes of a computer.</span></span> |
| [<span data-ttu-id="e2761-122">**FindNextVolume**</span><span class="sxs-lookup"><span data-stu-id="e2761-122">**FindNextVolume**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-findnextvolumew)   | <span data-ttu-id="e2761-123">Continua uma pesquisa de volume iniciada por uma chamada para [**FindFirstVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew).</span><span class="sxs-lookup"><span data-stu-id="e2761-123">Continues a volume search started by a call to [**FindFirstVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew).</span></span>                                                     |
| [<span data-ttu-id="e2761-124">**FindVolumeClose**</span><span class="sxs-lookup"><span data-stu-id="e2761-124">**FindVolumeClose**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-findvolumeclose) | <span data-ttu-id="e2761-125">Fecha uma pesquisa de volumes.</span><span class="sxs-lookup"><span data-stu-id="e2761-125">Closes a search for volumes.</span></span>                                                                                                                   |



 

## <a name="mounted-folder-scanning-functions"></a><span data-ttu-id="e2761-126">Funções de verificação de pasta montadas</span><span class="sxs-lookup"><span data-stu-id="e2761-126">Mounted Folder Scanning Functions</span></span>



| <span data-ttu-id="e2761-127">Função</span><span class="sxs-lookup"><span data-stu-id="e2761-127">Function</span></span>                                                       | <span data-ttu-id="e2761-128">Descrição</span><span class="sxs-lookup"><span data-stu-id="e2761-128">Description</span></span>                                                                                                                                                                               |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e2761-129">**FindFirstVolumeMountPoint**</span><span class="sxs-lookup"><span data-stu-id="e2761-129">**FindFirstVolumeMountPoint**</span></span>](/windows/desktop/api/WinBase/nf-winbase-findfirstvolumemountpointa) | <span data-ttu-id="e2761-130">Recupera o nome de uma pasta montada no volume especificado.</span><span class="sxs-lookup"><span data-stu-id="e2761-130">Retrieves the name of a mounted folder on the specified volume.</span></span> <span data-ttu-id="e2761-131">[**FindFirstVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-findfirstvolumemountpointa) é usado para começar a verificar as pastas montadas em um volume.</span><span class="sxs-lookup"><span data-stu-id="e2761-131">[**FindFirstVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-findfirstvolumemountpointa) is used to begin scanning the mounted folders on a volume.</span></span> |
| [<span data-ttu-id="e2761-132">**FindNextVolumeMountPoint**</span><span class="sxs-lookup"><span data-stu-id="e2761-132">**FindNextVolumeMountPoint**</span></span>](/windows/desktop/api/WinBase/nf-winbase-findnextvolumemountpointa)   | <span data-ttu-id="e2761-133">Continua uma pesquisa de pasta montada iniciada por uma chamada para [**FindFirstVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-findfirstvolumemountpointa).</span><span class="sxs-lookup"><span data-stu-id="e2761-133">Continues a mounted folder search started by a call to [**FindFirstVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-findfirstvolumemountpointa).</span></span>                                                                    |
| [<span data-ttu-id="e2761-134">**FindVolumeMountPointClose**</span><span class="sxs-lookup"><span data-stu-id="e2761-134">**FindVolumeMountPointClose**</span></span>](/windows/desktop/api/WinBase/nf-winbase-findvolumemountpointclose) | <span data-ttu-id="e2761-135">Fecha uma pesquisa de pastas montadas.</span><span class="sxs-lookup"><span data-stu-id="e2761-135">Closes a search for mounted folders.</span></span>                                                                                                                                                      |



 

 

 



