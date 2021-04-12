---
title: O armazenamento aprimorado agora é opcional para o WINPE e o SKU do servidor
description: O armazenamento aprimorado agora é opcional para o WINPE e o SKU do servidor
ms.assetid: 8A6B6194-5867-4B76-BD7B-152FD8A7DD77
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7601ee35e6d4be35a39874dd85650f051c1c718
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/01/2020
ms.locfileid: "104294547"
---
# <a name="enhanced-storage-is-now-optional-for-winpe-and-server-sku"></a><span data-ttu-id="84eda-103">O armazenamento aprimorado agora é opcional para o WINPE e o SKU do servidor</span><span class="sxs-lookup"><span data-stu-id="84eda-103">Enhanced storage is now optional for WINPE and server SKU</span></span>

## <a name="platforms"></a><span data-ttu-id="84eda-104">Plataformas</span><span class="sxs-lookup"><span data-stu-id="84eda-104">Platforms</span></span>

<span data-ttu-id="84eda-105">**Clientes** – Windows 8</span><span class="sxs-lookup"><span data-stu-id="84eda-105">**Clients** – Windows 8</span></span>  
<span data-ttu-id="84eda-106">**Servidores** – Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="84eda-106">**Servers** – Windows Server 2012</span></span>  


## <a name="description"></a><span data-ttu-id="84eda-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="84eda-107">Description</span></span>

<span data-ttu-id="84eda-108">O armazenamento aprimorado estava sempre disponível em dispositivos USB do Windows 7.</span><span class="sxs-lookup"><span data-stu-id="84eda-108">Enhanced storage was always available in Windows 7 USB devices.</span></span> <span data-ttu-id="84eda-109">Com o lançamento do Windows 8, ele está disponível para todos os dispositivos de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="84eda-109">With the release of Windows 8, it is available for all storage devices.</span></span> <span data-ttu-id="84eda-110">Em dispositivos baseados em cliente, ele é habilitado por padrão; em dispositivos de servidor, ele é opcional e deve ser provisionado por meio de Ambiente de Pré-Instalação do Windows (WinPE).</span><span class="sxs-lookup"><span data-stu-id="84eda-110">In client-based devices, it is enabled by default; in server devices it is optional and must be provisioned through Windows Preinstallation Environment (WinPE).</span></span>

## <a name="manifestation"></a><span data-ttu-id="84eda-111">Manifestação</span><span class="sxs-lookup"><span data-stu-id="84eda-111">Manifestation</span></span>

<span data-ttu-id="84eda-112">O dispositivo do servidor falhará se o armazenamento avançado não estiver habilitado.</span><span class="sxs-lookup"><span data-stu-id="84eda-112">The server device will fail if enhanced storage is not enabled.</span></span>

<span data-ttu-id="84eda-113">Os dispositivos de inicialização devem ser provisionados por meio do WinPE com essa habilitação.</span><span class="sxs-lookup"><span data-stu-id="84eda-113">Boot devices must be provisioned through WinPE with this enabled.</span></span>

## <a name="solution"></a><span data-ttu-id="84eda-114">Solução</span><span class="sxs-lookup"><span data-stu-id="84eda-114">Solution</span></span>

<span data-ttu-id="84eda-115">Como o armazenamento avançado é opcional para o servidor de tempo de execução, os desenvolvedores devem adicioná-lo ao WinPE para provisionamento e ativação dessas unidades.</span><span class="sxs-lookup"><span data-stu-id="84eda-115">Because enhanced storage is optional for runtime server, developers must add it to WinPE for provisioning and activation of those drives.</span></span> <span data-ttu-id="84eda-116">Consulte o guia de implantação para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="84eda-116">See the deployment guide for details.</span></span>

<span data-ttu-id="84eda-117">Os administradores de servidor devem configurar explicitamente seu servidor para usar o armazenamento avançado.</span><span class="sxs-lookup"><span data-stu-id="84eda-117">Server administrators must then explicitly configure their server to use enhanced storage.</span></span>

 

 




