---
title: Vinculação dinâmica
description: Os desenvolvedores de gráficos às vezes criam sombreadores grandes e de uso geral que podem ser usados por uma ampla variedade de itens de cena.
ms.assetid: 2f5f7852-0f0a-4fad-a412-9a0d634c73b6
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d5cd10bab8e2b4a28458cad1050847e0184ce43b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636022"
---
# <a name="dynamic-linking"></a><span data-ttu-id="0d1ca-103">Vinculação dinâmica</span><span class="sxs-lookup"><span data-stu-id="0d1ca-103">Dynamic Linking</span></span>

<span data-ttu-id="0d1ca-104">Os desenvolvedores de gráficos às vezes criam sombreadores grandes e de uso geral que podem ser usados por uma ampla variedade de itens de cena.</span><span class="sxs-lookup"><span data-stu-id="0d1ca-104">Graphics developers sometimes create large, general-purpose shaders that can be used by a wide variety of scene items.</span></span> <span data-ttu-id="0d1ca-105">Em tempo de execução, o sombreador Executa condicionalmente o código apropriado para a situação em questão.</span><span class="sxs-lookup"><span data-stu-id="0d1ca-105">At runtime, the shader conditionally runs code appropriate for the given situation.</span></span> <span data-ttu-id="0d1ca-106">Infelizmente, esses sombreadores grandes de uso geral usam GPRs (registros de uso geral) de forma ineficiente e podem ser muito mais lentos do que os sombreadores menores e mais direcionados.</span><span class="sxs-lookup"><span data-stu-id="0d1ca-106">Unfortunately, these large, general-purpose shaders use general-purpose registers (GPRs) inefficiently, and can be much slower than smaller, more targeted shaders.</span></span>

<span data-ttu-id="0d1ca-107">O modelo de sombreador 5 aborda esse problema de desempenho introduzindo a vinculação dinâmica de sombreador.</span><span class="sxs-lookup"><span data-stu-id="0d1ca-107">Shader model 5 addresses this performance problem by introducing dynamic shader linking.</span></span> <span data-ttu-id="0d1ca-108">A vinculação dinâmica separa os fragmentos de código do sombreador usando interfaces e funções virtuais e permite que o aplicativo selecione o fragmento a ser usado no momento do desenho.</span><span class="sxs-lookup"><span data-stu-id="0d1ca-108">Dynamic linking separates shader code fragments by using interfaces and virtual functions and allows the application to select the fragment to use at draw time.</span></span> <span data-ttu-id="0d1ca-109">Isso melhora o desempenho ligando apenas o código do sombreador necessário e não todo o sombreador de uso geral grande.</span><span class="sxs-lookup"><span data-stu-id="0d1ca-109">This improves performance by binding only the shader code needed and not the entire large, general-purpose shader.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="0d1ca-110">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="0d1ca-110">In This Section</span></span>



| <span data-ttu-id="0d1ca-111">Item</span><span class="sxs-lookup"><span data-stu-id="0d1ca-111">Item</span></span>                                                                                                                                                                                                                                                                                                                         | <span data-ttu-id="0d1ca-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="0d1ca-112">Description</span></span>                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d1ca-113"><span id="Storing_Variables_and_Types_for_Shaders_to_Share"></span><span id="storing_variables_and_types_for_shaders_to_share"></span><span id="STORING_VARIABLES_AND_TYPES_FOR_SHADERS_TO_SHARE"></span>[Armazenando variáveis e tipos de sombreadores para compartilhar](storing-variables-and-types-for-shaders-to-share.md)</span><span class="sxs-lookup"><span data-stu-id="0d1ca-113"><span id="Storing_Variables_and_Types_for_Shaders_to_Share"></span><span id="storing_variables_and_types_for_shaders_to_share"></span><span id="STORING_VARIABLES_AND_TYPES_FOR_SHADERS_TO_SHARE"></span>[Storing Variables and Types for Shaders to Share](storing-variables-and-types-for-shaders-to-share.md)</span></span><br/> | <span data-ttu-id="0d1ca-114">Descreve o objeto de vinculação de classe para armazenar variáveis e tipos que vários sombreadores podem compartilhar.</span><span class="sxs-lookup"><span data-stu-id="0d1ca-114">Describes the class linkage object for storing variables and types that multiple shaders can share.</span></span><br/> |
| <span data-ttu-id="0d1ca-115"><span id="Interfaces_and_Classes"></span><span id="interfaces_and_classes"></span><span id="INTERFACES_AND_CLASSES"></span>[Interfaces e classes](overviews-direct3d-11-hlsl-dynamic-linking-class.md)</span><span class="sxs-lookup"><span data-stu-id="0d1ca-115"><span id="Interfaces_and_Classes"></span><span id="interfaces_and_classes"></span><span id="INTERFACES_AND_CLASSES"></span>[Interfaces and Classes](overviews-direct3d-11-hlsl-dynamic-linking-class.md)</span></span><br/>                                                                                                         | <span data-ttu-id="0d1ca-116">Descreve como usar interfaces e classes HLSL para implementar a vinculação dinâmica.</span><span class="sxs-lookup"><span data-stu-id="0d1ca-116">Describes using HLSL interfaces and classes to implement dynamic linking.</span></span><br/>                           |
| <span data-ttu-id="0d1ca-117"><span id="Interface_Usage_Restrictions"></span><span id="interface_usage_restrictions"></span><span id="INTERFACE_USAGE_RESTRICTIONS"></span>[Restrições de uso de interface](overviews-direct3d-11-hlsl-dynamic-linking-expression.md)</span><span class="sxs-lookup"><span data-stu-id="0d1ca-117"><span id="Interface_Usage_Restrictions"></span><span id="interface_usage_restrictions"></span><span id="INTERFACE_USAGE_RESTRICTIONS"></span>[Interface Usage Restrictions](overviews-direct3d-11-hlsl-dynamic-linking-expression.md)</span></span><br/>                                                                            | <span data-ttu-id="0d1ca-118">Descreve as restrições sobre o uso de interfaces no código de sombreador.</span><span class="sxs-lookup"><span data-stu-id="0d1ca-118">Describes restrictions on the use of interfaces in shader code.</span></span><br/>                                     |



 

## <a name="related-topics"></a><span data-ttu-id="0d1ca-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0d1ca-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0d1ca-120">HLSL</span><span class="sxs-lookup"><span data-stu-id="0d1ca-120">HLSL</span></span>](overviews-direct3d-11-hlsl.md)
</dt> </dl>

 

 





