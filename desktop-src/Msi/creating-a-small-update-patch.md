---
description: Siga as diretrizes a seguir ao criar um patch para uma atualização Windows Installer pequena.
ms.assetid: 0e57c2aa-e86a-4161-9749-c7963182a6d5
title: Criando um patch de atualização pequena
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d948c871baed7fbc15545ed9669c9864ce954799
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105780961"
---
# <a name="creating-a-small-update-patch"></a><span data-ttu-id="6ac36-103">Criando um patch de atualização pequena</span><span class="sxs-lookup"><span data-stu-id="6ac36-103">Creating a Small Update Patch</span></span>

<span data-ttu-id="6ac36-104">Ao criar um patch para [pequenas atualizações](small-updates.md), os autores devem aderir às seguintes diretrizes:</span><span class="sxs-lookup"><span data-stu-id="6ac36-104">When creating a patch for [small updates](small-updates.md), authors should adhere to the following guidelines:</span></span>

-   <span data-ttu-id="6ac36-105">Patches de atualização pequenos devem ser projetados para uma única instalação de destino.</span><span class="sxs-lookup"><span data-stu-id="6ac36-105">Small update patches must be designed for a single, target installation.</span></span>
-   <span data-ttu-id="6ac36-106">Os patches de atualização pequenos devem usar a versão mais antiga como a instalação de destino.</span><span class="sxs-lookup"><span data-stu-id="6ac36-106">Small update patches should use the earliest version as the target installation.</span></span>
-   <span data-ttu-id="6ac36-107">Um patch de atualização pequeno deve substituir e tornar obsoleto qualquer patch de atualização pequeno anterior.</span><span class="sxs-lookup"><span data-stu-id="6ac36-107">A small update patch should replace and make obsolete any earlier small update patches.</span></span>

<span data-ttu-id="6ac36-108">O cenário a seguir ilustra quando um patch de atualização pequeno é o melhor.</span><span class="sxs-lookup"><span data-stu-id="6ac36-108">The following scenario illustrates when a small update patch is best.</span></span>

<span data-ttu-id="6ac36-109">Sua empresa envia a versão 1,0 do Myproduct.msi.</span><span class="sxs-lookup"><span data-stu-id="6ac36-109">Your company ships version 1.0 of Myproduct.msi.</span></span> <span data-ttu-id="6ac36-110">Logo em seguida, você envia um patch de [atualização pequeno](small-updates.md) para Myproduct.msi chamado QFE1.</span><span class="sxs-lookup"><span data-stu-id="6ac36-110">Shortly thereafter, you ship a [small update](small-updates.md) patch for Myproduct.msi called QFE1.</span></span> <span data-ttu-id="6ac36-111">Isso não altera a propriedade [**ProductCode**](productcode.md) ou a propriedade [**ProductVersion**](productversion.md) .</span><span class="sxs-lookup"><span data-stu-id="6ac36-111">This does not change the [**ProductCode**](productcode.md) property or the [**ProductVersion**](productversion.md) property.</span></span>

<span data-ttu-id="6ac36-112">Posteriormente, você cria um segundo patch de [atualização pequena](small-updates.md) para Myproduct.msi chamado QFE2.</span><span class="sxs-lookup"><span data-stu-id="6ac36-112">Later, you author a second [small update](small-updates.md) patch for Myproduct.msi called QFE2.</span></span> <span data-ttu-id="6ac36-113">Esse segundo patch deve ter como destino Myproduct.msi versão 1,0.</span><span class="sxs-lookup"><span data-stu-id="6ac36-113">This second patch must target Myproduct.msi version 1.0.</span></span> <span data-ttu-id="6ac36-114">Esse segundo patch não deve direcionar Myproduct.msi versão 1,0 e Myproduct.msi versão 1,0 + QFE1.</span><span class="sxs-lookup"><span data-stu-id="6ac36-114">This second patch must not target both Myproduct.msi version 1.0 and Myproduct.msi version 1.0 + QFE1.</span></span> <span data-ttu-id="6ac36-115">Quando QFE2 é aplicado, ele deve remover QFE1.</span><span class="sxs-lookup"><span data-stu-id="6ac36-115">When QFE2 is applied it should remove QFE1.</span></span>

 

 



