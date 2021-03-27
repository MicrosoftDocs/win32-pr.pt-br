---
title: Arquitetura de memória unificada
description: Consultar se há suporte para a uma (arquitetura de memória unificada) pode ajudar a determinar como lidar com alguns recursos.
ms.assetid: E43892F9-E7CD-4D18-BDDE-3C4F03F8F4EA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99baeab51838b9b3382884a681ec9b579fa700a0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916023"
---
# <a name="unified-memory-architecture"></a><span data-ttu-id="4e593-103">Arquitetura de memória unificada</span><span class="sxs-lookup"><span data-stu-id="4e593-103">Unified Memory Architecture</span></span>

<span data-ttu-id="4e593-104">Consultar se há suporte para a uma (arquitetura de memória unificada) pode ajudar a determinar como lidar com alguns recursos.</span><span class="sxs-lookup"><span data-stu-id="4e593-104">Querying for whether Unified Memory Architecture (UMA) is supported can help determine how to handle some resources.</span></span>

<span data-ttu-id="4e593-105">Um booliano, definido pelo driver, pode ser lido na estrutura [**D3D11 de \_ dados do recurso \_ \_ D3D11 \_ OPTIONS2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2) para determinar se o hardware dá suporte a uma.</span><span class="sxs-lookup"><span data-stu-id="4e593-105">A boolean, set by the driver, can be read from the [**D3D11\_FEATURE\_DATA\_D3D11\_OPTIONS2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2) structure to determine if the hardware supports UMA.</span></span>

<span data-ttu-id="4e593-106">Os aplicativos em execução em uma pode querer ter mais recursos com acesso à CPU habilitado do que se não estiverem disponíveis.</span><span class="sxs-lookup"><span data-stu-id="4e593-106">Applications running on UMA may want to have more resources with CPU access enabled than if it is not available.</span></span> <span data-ttu-id="4e593-107">Uma a permite que os aplicativos evitem copiar dados de recursos, em vez de permanecerem eficientes exclusivamente para adaptadores de elementos gráficos não pertencentes a uma.</span><span class="sxs-lookup"><span data-stu-id="4e593-107">UMA enables applications to avoiding copying resource data around, instead of staying efficient solely for non-UMA graphics adapters.</span></span> [<span data-ttu-id="4e593-108">Recursos do Direct3D 11,3</span><span class="sxs-lookup"><span data-stu-id="4e593-108">Direct3D 11.3 Features</span></span>](direct3d-11-3-features.md)

## <a name="related-topics"></a><span data-ttu-id="4e593-109">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4e593-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4e593-110">Recursos do Direct3D 11,3</span><span class="sxs-lookup"><span data-stu-id="4e593-110">Direct3D 11.3 Features</span></span>](direct3d-11-3-features.md)
</dt> </dl>

 

 




