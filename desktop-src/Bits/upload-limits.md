---
title: Limites de carregamento
description: Para limitar o tamanho dos carregamentos, defina a propriedade de extensão do IIS BITSMaximumUploadSize.
ms.assetid: 01ad2f32-18be-43a5-a07f-e6f28f7a471b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 647aeefe82cf9c3ab035bc3e233c4157f471110b
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/20/2020
ms.locfileid: "104453852"
---
# <a name="upload-limits"></a><span data-ttu-id="e1cd8-103">Limites de carregamento</span><span class="sxs-lookup"><span data-stu-id="e1cd8-103">Upload Limits</span></span>

<span data-ttu-id="e1cd8-104">Para limitar o tamanho dos carregamentos, defina a propriedade de extensão do IIS [**BITSMaximumUploadSize**](bits-iis-extension-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="e1cd8-104">To limit the size of uploads, set the [**BITSMaximumUploadSize**](bits-iis-extension-properties.md) IIS extension property.</span></span> <span data-ttu-id="e1cd8-105">No IIS 7, você também pode precisar modificar o atributo **maxAllowedContentLength** .</span><span class="sxs-lookup"><span data-stu-id="e1cd8-105">In IIS 7, you may also have to modify the **maxAllowedContentLength** attribute.</span></span> <span data-ttu-id="e1cd8-106">Por padrão, o limite de carregamento do IIS 7 é 30 milhões bytes.</span><span class="sxs-lookup"><span data-stu-id="e1cd8-106">By default, the IIS 7 upload limit is 30 million bytes.</span></span> <span data-ttu-id="e1cd8-107">Para obter detalhes e informações sobre como alterar o padrão do IIS, consulte [KB942074](https://support.microsoft.com//kb/942074).</span><span class="sxs-lookup"><span data-stu-id="e1cd8-107">For details and information on changing the IIS default, see [KB942074](https://support.microsoft.com//kb/942074).</span></span>

 

 




