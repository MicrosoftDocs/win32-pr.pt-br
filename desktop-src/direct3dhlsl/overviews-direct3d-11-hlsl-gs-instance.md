---
title: Como fazer uma instância de um sombreador de geometria
description: A instanciação do sombreador de geometria permite que várias execuções do mesmo sombreador de geometria sejam executadas por primitivo.
ms.assetid: e3d8616b-7129-40e9-99fc-2852914a80b0
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7858de7d8526a9468d3ebd0a07d57777983a66db
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104988523"
---
# <a name="how-to-instance-a-geometry-shader"></a><span data-ttu-id="29a42-103">Como: instância de um sombreador de geometria</span><span class="sxs-lookup"><span data-stu-id="29a42-103">How To: Instance a Geometry Shader</span></span>

<span data-ttu-id="29a42-104">A instanciação do sombreador de geometria permite que várias execuções do mesmo sombreador de geometria sejam executadas por primitivo.</span><span class="sxs-lookup"><span data-stu-id="29a42-104">Geometry shader instancing allows multiple executions of the same geometry shader to be executed per primitive.</span></span> <span data-ttu-id="29a42-105">Para fazer uma instância de um sombreador de geometria, adicione um atributo de instância à função principal de sombreador e identifique um parâmetro de índice de instância no corpo da função de sombreador.</span><span class="sxs-lookup"><span data-stu-id="29a42-105">To instance a geometry shader, add an instance attribute to the main shader function and identify an instance index parameter in the shader function body.</span></span>

<span data-ttu-id="29a42-106">Para fazer uma instância de um sombreador geometry:</span><span class="sxs-lookup"><span data-stu-id="29a42-106">To Instance a Geometry Shader:</span></span>

1.  <span data-ttu-id="29a42-107">Adicione o [atributo de instância](sm5-attributes-instance.md) à função principal.</span><span class="sxs-lookup"><span data-stu-id="29a42-107">Add the [instance attribute](sm5-attributes-instance.md) to the main function.</span></span>

    ```
    [instance(24)]
    ```

    

    <span data-ttu-id="29a42-108">Isso define o número de instâncias (um máximo de 32) a serem executadas para cada primitiva.</span><span class="sxs-lookup"><span data-stu-id="29a42-108">This defines the number of instances (a maximum of 32) to be run for each primitive.</span></span>

2.  <span data-ttu-id="29a42-109">Anexe o valor do sistema [ \_ GSInstanceID VA](sv-gsinstanceid.md) a uma variável na lista de parâmetros de função que pode ser usada para rastrear a ID da instância que está sendo executada.</span><span class="sxs-lookup"><span data-stu-id="29a42-109">Attach the [SV\_GSInstanceID](sv-gsinstanceid.md) system value to a variable in the function parameter list that can be used to track the ID of the instance being executed.</span></span>
    ```
    uint InstanceID : SV_GSInstanceID
    ```

    

3.  <span data-ttu-id="29a42-110">Compile e crie o sombreador da mesma forma que faria com qualquer outro sombreador de geometria.</span><span class="sxs-lookup"><span data-stu-id="29a42-110">Compile and create the shader just as you would any other geometry shader.</span></span>

<span data-ttu-id="29a42-111">Outros detalhes incluem:</span><span class="sxs-lookup"><span data-stu-id="29a42-111">Other details include:</span></span>

-   <span data-ttu-id="29a42-112">A contagem máxima de instâncias é 32.</span><span class="sxs-lookup"><span data-stu-id="29a42-112">The maximum instance count is 32.</span></span>
-   <span data-ttu-id="29a42-113">A contagem máxima de vértices é uma contagem máxima de vértice por instância.</span><span class="sxs-lookup"><span data-stu-id="29a42-113">The maximum vertex count is a per-instance maximum vertex count.</span></span>
-   <span data-ttu-id="29a42-114">Cada invocação de instância (como qualquer invocação de sombreador de geometria) aumenta a contagem de invocação e gera um RestartStrip implícito ().</span><span class="sxs-lookup"><span data-stu-id="29a42-114">Each instance invocation (like any geometry shader invocation) increases the invocation count and generates an implicit RestartStrip().</span></span>

## <a name="related-topics"></a><span data-ttu-id="29a42-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="29a42-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="29a42-116">Recursos do sombreador de geometria</span><span class="sxs-lookup"><span data-stu-id="29a42-116">Geometry Shader Features</span></span>](overviews-direct3d-11-hlsl-gs-features.md)
</dt> </dl>

 

 




