---
title: O que a instalação deve fazer
description: Os novos atributos referenciados na etapa 3 devem ser referenciados por seu OID porque o nome do novo atributo não está presente no cache de esquema neste ponto.
ms.assetid: 57da8740-7646-4ca9-ba8d-832e4f520b13
ms.tgt_platform: multiple
keywords:
- O que a instalação deve fazer AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5724a7acbb4d0bf8ef3008fa48e2f10fcc04a324
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103915927"
---
# <a name="what-the-installation-must-do"></a><span data-ttu-id="1f8a3-104">O que a instalação deve fazer</span><span class="sxs-lookup"><span data-stu-id="1f8a3-104">What the Installation Must Do</span></span>

<span data-ttu-id="1f8a3-105">Os aplicativos que estendem o esquema devem aplicar atualizações conforme descrito no procedimento a seguir.</span><span class="sxs-lookup"><span data-stu-id="1f8a3-105">Applications that extend the schema, must apply updates as described in the following procedure.</span></span>

<span data-ttu-id="1f8a3-106">**Para aplicar atualizações ao estender o esquema**</span><span class="sxs-lookup"><span data-stu-id="1f8a3-106">**To apply updates when extending the schema**</span></span>

1.  <span data-ttu-id="1f8a3-107">Adicione os novos atributos.</span><span class="sxs-lookup"><span data-stu-id="1f8a3-107">Add the new attributes.</span></span>
2.  <span data-ttu-id="1f8a3-108">Adicione as novas classes.</span><span class="sxs-lookup"><span data-stu-id="1f8a3-108">Add the new classes.</span></span>
3.  <span data-ttu-id="1f8a3-109">Adicione os novos atributos às classes.</span><span class="sxs-lookup"><span data-stu-id="1f8a3-109">Add the new attributes to classes.</span></span>
4.  <span data-ttu-id="1f8a3-110">Disparar uma recarga de cache.</span><span class="sxs-lookup"><span data-stu-id="1f8a3-110">Trigger a cache reload.</span></span>

<span data-ttu-id="1f8a3-111">Os novos atributos referenciados na etapa 3 devem ser referenciados por seu OID porque o nome do novo atributo não está presente no cache de esquema neste ponto.</span><span class="sxs-lookup"><span data-stu-id="1f8a3-111">New attributes referenced in Step 3 must be referred to by its OID because the new attribute name is not present in the schema cache at this point.</span></span>

<span data-ttu-id="1f8a3-112">A etapa 4 é desnecessária se as extensões não forem usadas imediatamente; as extensões serão exibidas no cache de esquema em aproximadamente 5 minutos, dependendo da carga do sistema.</span><span class="sxs-lookup"><span data-stu-id="1f8a3-112">Step 4 is unnecessary if the extensions will not be used immediately; the extensions will appear in the schema cache in approximately 5 minutes, depending on system load.</span></span> <span data-ttu-id="1f8a3-113">Para obter mais informações sobre o cache de esquema e como disparar uma recarga de cache, consulte [atualizando o cache de esquema](updating-the-schema-cache.md).</span><span class="sxs-lookup"><span data-stu-id="1f8a3-113">For more information about the schema cache and how to trigger a cache reload, see [Updating the Schema Cache](updating-the-schema-cache.md).</span></span>

 

 




