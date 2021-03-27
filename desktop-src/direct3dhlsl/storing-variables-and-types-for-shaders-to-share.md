---
title: Armazenando variáveis e tipos de sombreadores para compartilhar
description: O objeto de vinculação de classe é um namespace para variáveis e tipos que vários sombreadores podem compartilhar.
ms.assetid: 8b61677b-a466-4646-b0b2-19097669f8c3
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4f9423154cd42de28b2d447776fe21a7b8e57620
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104967218"
---
# <a name="storing-variables-and-types-for-shaders-to-share"></a><span data-ttu-id="78c95-103">Armazenando variáveis e tipos de sombreadores para compartilhar</span><span class="sxs-lookup"><span data-stu-id="78c95-103">Storing Variables and Types for Shaders to Share</span></span>

<span data-ttu-id="78c95-104">O objeto de vinculação de classe é um namespace para variáveis e tipos que vários sombreadores podem compartilhar.</span><span class="sxs-lookup"><span data-stu-id="78c95-104">The class linkage object is a namespace for variables and types that multiple shaders can share.</span></span> <span data-ttu-id="78c95-105">Quando você passa um objeto de vinculação de classe em uma chamada para criar um sombreador, o tempo de execução reúne uma lista de variáveis e tipos que podem implementar cada interface no sombreador e armazena os nomes dessas variáveis e tipos no objeto de vinculação de classe.</span><span class="sxs-lookup"><span data-stu-id="78c95-105">When you pass a class linkage object in a call to create a shader, the runtime gathers a list of variables and types that can implement each interface in the shader and stores the names of those variables and types in the class linkage object.</span></span>

<span data-ttu-id="78c95-106">Portanto, quando você chama o método [**ID3D11ClassLinkage:: GetClassInstance**](/windows/desktop/api/d3d11/nf-d3d11-id3d11classlinkage-getclassinstance) para gerar instâncias de classe do objeto de vinculação de classe, o tempo de execução pode recuperar a variável ou o tipo que corresponde ao nome que é fornecido em cada sombreador (se esse nome for válido para um determinado sombreador) e criado com o objeto de vinculação de classe fornecido.</span><span class="sxs-lookup"><span data-stu-id="78c95-106">Therefore, when you call the [**ID3D11ClassLinkage::GetClassInstance**](/windows/desktop/api/d3d11/nf-d3d11-id3d11classlinkage-getclassinstance) method to generate class instances from the class linkage object, the runtime can retrieve the variable or type that corresponds to the name that is provided in each shader (if that name is valid for a given shader) and that is created with the given class linkage object.</span></span>

<span data-ttu-id="78c95-107">Por exemplo, suponha que você tenha uma classe **leve** que implementa uma interface de **cor** e use essa classe no sombreador de vértice e no sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="78c95-107">For example, suppose you have a **Light** class that implements a **Color** interface, and you use this class in your vertex shader and pixel shader.</span></span> <span data-ttu-id="78c95-108">Quando você cria um sombreador (por exemplo, chamando [**ID3D11Device:: CreatePixelShader**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createpixelshader)), o tempo de execução determina que o tipo de classe **Light** está disponível em sombreadores de vértices e de pixel e adiciona o tipo de classe **Light** ao objeto de vinculação de classe.</span><span class="sxs-lookup"><span data-stu-id="78c95-108">When you create a shader (for example, by calling [**ID3D11Device::CreatePixelShader**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createpixelshader)), the runtime determines that the **Light** class type is available in both vertex and pixel shaders and adds the **Light** class type to the class linkage object.</span></span> <span data-ttu-id="78c95-109">Em seguida, você pode criar uma instância **clara** em um local desejado, associar os recursos para os dois sombreadores e passar essa instância na matriz de instâncias de classe ao definir o sombreador para o dispositivo (por exemplo, chamando [**ID3D11DeviceContext::P ssetshader**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-pssetshader)).</span><span class="sxs-lookup"><span data-stu-id="78c95-109">You can then create a **Light** instance at a location that you want, bind the resources for both shaders, and pass this instance in the class instances array when you set the shader to the device (for example, by calling [**ID3D11DeviceContext::PSSetShader**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-pssetshader)).</span></span> <span data-ttu-id="78c95-110">Em seguida, o tempo de execução executa a seguinte sequência:</span><span class="sxs-lookup"><span data-stu-id="78c95-110">The runtime then performs the following sequence:</span></span>

1.  <span data-ttu-id="78c95-111">Verifica se a instância foi criada com o mesmo objeto de vinculação de classe.</span><span class="sxs-lookup"><span data-stu-id="78c95-111">Verifies that the instance was created with the same class linkage object.</span></span>
2.  <span data-ttu-id="78c95-112">Verifica se o tipo de classe **leve** é disponível em sombreadores de vértice e de pixel.</span><span class="sxs-lookup"><span data-stu-id="78c95-112">Verifies that the **Light** class type is availabe in both vertex and pixel shaders.</span></span>
3.  <span data-ttu-id="78c95-113">Seleciona as tabelas de funções corretas, que podem ser diferentes para os sombreadores de vértice e pixel.</span><span class="sxs-lookup"><span data-stu-id="78c95-113">Selects the correct function tables, which can be different for the vertex and pixel shaders.</span></span>
4.  <span data-ttu-id="78c95-114">Envia os deslocamentos que a instância fornece.</span><span class="sxs-lookup"><span data-stu-id="78c95-114">Sends down the offsets that the instance provides.</span></span>

<span data-ttu-id="78c95-115">O objeto de vinculação de classe é, em última instância, um repositório de tipos e nomes de variáveis.</span><span class="sxs-lookup"><span data-stu-id="78c95-115">The class linkage object is ultimately a repository of type and variable names.</span></span> <span data-ttu-id="78c95-116">O número máximo de nomes disponíveis para cada item (tipo e variável) é 64K.</span><span class="sxs-lookup"><span data-stu-id="78c95-116">The maximum number of names available for each item (type and variable) is 64K.</span></span> <span data-ttu-id="78c95-117">Quanto mais longos forem os nomes de tipo e variável, maior será o requisito de armazenamento para os metadados da interface armazenados por sombreador.</span><span class="sxs-lookup"><span data-stu-id="78c95-117">The longer the type and variable names are, the higher the storage requirement is for the interface metadata that is stored per shader.</span></span> <span data-ttu-id="78c95-118">Isso ocorre porque o tempo de execução deve armazenar um mapeamento para esses nomes para cada sombreador.</span><span class="sxs-lookup"><span data-stu-id="78c95-118">This is because the runtime must store a mapping for these names for each shader.</span></span>

## <a name="related-topics"></a><span data-ttu-id="78c95-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="78c95-119">Related Topics</span></span>

[<span data-ttu-id="78c95-120">Vinculação dinâmica</span><span class="sxs-lookup"><span data-stu-id="78c95-120">Dynamic Linking</span></span>](overviews-direct3d-11-hlsl-dynamic-linking.md)


## <a name="related-topics"></a><span data-ttu-id="78c95-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="78c95-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="78c95-122">Vinculação dinâmica</span><span class="sxs-lookup"><span data-stu-id="78c95-122">Dynamic Linking</span></span>](overviews-direct3d-11-hlsl-dynamic-linking.md)
</dt> </dl>

 

 