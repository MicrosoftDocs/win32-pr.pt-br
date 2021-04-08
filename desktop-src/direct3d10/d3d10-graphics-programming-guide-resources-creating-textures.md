---
description: Um recurso de textura é uma coleção estruturada de dados.
ms.assetid: 4c716be8-044e-4ed4-aeca-4379440826bd
title: Criando recursos de textura (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81f2ca200b566d17b02af56c48cb1227c41106ad
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920399"
---
# <a name="creating-texture-resources-direct3d-10"></a><span data-ttu-id="ab7fa-103">Criando recursos de textura (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="ab7fa-103">Creating Texture Resources (Direct3D 10)</span></span>

<span data-ttu-id="ab7fa-104">Um recurso de [textura](d3d10-graphics-programming-guide-resources-types.md) é uma coleção estruturada de dados.</span><span class="sxs-lookup"><span data-stu-id="ab7fa-104">A [texture](d3d10-graphics-programming-guide-resources-types.md) resource is a structured collection of data.</span></span> <span data-ttu-id="ab7fa-105">Normalmente, os valores de cor são armazenados em texturas e acessados durante a renderização pelo [pipeline](d3d10-graphics-programming-guide-pipeline-stages.md) em vários estágios para entrada e saída.</span><span class="sxs-lookup"><span data-stu-id="ab7fa-105">Typically, color values are stored in textures and accessed during rendering by the [pipeline](d3d10-graphics-programming-guide-pipeline-stages.md) at various stages for both input and output.</span></span> <span data-ttu-id="ab7fa-106">Criar texturas e definir como elas serão usadas é uma parte importante da renderização de cenas de aparência interessante no Direct3D 10.</span><span class="sxs-lookup"><span data-stu-id="ab7fa-106">Creating textures and defining how they will be used is an important part of rendering interesting-looking scenes in Direct3D 10.</span></span>

<span data-ttu-id="ab7fa-107">Embora as texturas normalmente contenham informações de cor, a criação de texturas usando o [**\_ formato dxgi**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) diferente permite que eles armazenem diferentes tipos de dados.</span><span class="sxs-lookup"><span data-stu-id="ab7fa-107">Even though textures typically contain color information, creating textures using different [**DXGI\_FORMAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) enables them to store different kinds of data.</span></span> <span data-ttu-id="ab7fa-108">Esses dados podem então ser aproveitados pelo pipeline do Direct3D 10 de maneiras não tradicionais.</span><span class="sxs-lookup"><span data-stu-id="ab7fa-108">This data can then be leveraged by the Direct3D 10 pipeline in non-traditional ways.</span></span>

<span data-ttu-id="ab7fa-109">Todas as texturas têm limites quanto à quantidade de memória consumida e quantas texels elas contêm.</span><span class="sxs-lookup"><span data-stu-id="ab7fa-109">All textures have limits on how much memory they consume, and how many texels they contain.</span></span> <span data-ttu-id="ab7fa-110">Esses limites são especificados pelas [constantes de recurso](d3d10-graphics-reference-resource-constants.md).</span><span class="sxs-lookup"><span data-stu-id="ab7fa-110">These limits are specified by [resource constants](d3d10-graphics-reference-resource-constants.md).</span></span>

-   [<span data-ttu-id="ab7fa-111">Criar uma textura de um arquivo</span><span class="sxs-lookup"><span data-stu-id="ab7fa-111">Create a Texture from a File</span></span>](#create-a-texture-from-a-file)
    -   [<span data-ttu-id="ab7fa-112">Criar textura e exibir separadamente</span><span class="sxs-lookup"><span data-stu-id="ab7fa-112">Create Texture and View Separately</span></span>](#create-texture-and-view-separately)
    -   [<span data-ttu-id="ab7fa-113">Criar textura e exibição simultaneamente</span><span class="sxs-lookup"><span data-stu-id="ab7fa-113">Create Texture and View Simultaneously</span></span>](#create-texture-and-view-simultaneously)
-   [<span data-ttu-id="ab7fa-114">Criando texturas vazias</span><span class="sxs-lookup"><span data-stu-id="ab7fa-114">Creating Empty Textures</span></span>](#creating-empty-textures)
    -   [<span data-ttu-id="ab7fa-115">Renderizando para uma textura</span><span class="sxs-lookup"><span data-stu-id="ab7fa-115">Rendering to a texture</span></span>](#rendering-to-a-texture)
    -   [<span data-ttu-id="ab7fa-116">Preenchendo texturas manualmente</span><span class="sxs-lookup"><span data-stu-id="ab7fa-116">Filling Textures Manually</span></span>](#filling-textures-manually)
-   [<span data-ttu-id="ab7fa-117">Vários Rendertargets</span><span class="sxs-lookup"><span data-stu-id="ab7fa-117">Multiple Rendertargets</span></span>](#multiple-rendertargets)
-   [<span data-ttu-id="ab7fa-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ab7fa-118">Related topics</span></span>](#related-topics)

## <a name="create-a-texture-from-a-file"></a><span data-ttu-id="ab7fa-119">Criar uma textura de um arquivo</span><span class="sxs-lookup"><span data-stu-id="ab7fa-119">Create a Texture from a File</span></span>

> [!Note]  
> <span data-ttu-id="ab7fa-120">A [biblioteca do utilitário D3DX](d3d10-graphics-reference-d3dx10.md) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.</span><span class="sxs-lookup"><span data-stu-id="ab7fa-120">The [D3DX utility library](d3d10-graphics-reference-d3dx10.md) is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="ab7fa-121">Quando você cria uma textura no Direct3D 10, também precisa criar uma [exibição](d3d10-graphics-programming-guide-resources-access-views.md).</span><span class="sxs-lookup"><span data-stu-id="ab7fa-121">When you create a texture in Direct3D 10, you also need to create a [view](d3d10-graphics-programming-guide-resources-access-views.md).</span></span> <span data-ttu-id="ab7fa-122">Uma exibição é um objeto que informa ao dispositivo como uma textura deve ser acessada durante a renderização.</span><span class="sxs-lookup"><span data-stu-id="ab7fa-122">A view is an object that tells the device how a texture should be accessed during rendering.</span></span> <span data-ttu-id="ab7fa-123">A maneira mais comum de acessar uma textura é ler usando um [sombreador](../direct3dhlsl/dx-graphics-hlsl.md).</span><span class="sxs-lookup"><span data-stu-id="ab7fa-123">The most common way to access a texture is to read from it using a [shader](../direct3dhlsl/dx-graphics-hlsl.md).</span></span> <span data-ttu-id="ab7fa-124">Uma exibição de recurso de sombreador informará um sombreador como ler de uma textura durante a renderização.</span><span class="sxs-lookup"><span data-stu-id="ab7fa-124">A shader-resource view will tell a shader how to read from a texture during rendering.</span></span> <span data-ttu-id="ab7fa-125">O tipo de exibição que uma textura usará deve ser especificado quando você criá-la.</span><span class="sxs-lookup"><span data-stu-id="ab7fa-125">The kind of view a texture will use must be specified when you create it.</span></span>

<span data-ttu-id="ab7fa-126">Criar uma textura e carregar seus dados iniciais pode ser feito de duas maneiras diferentes: criar uma textura e uma exibição separadamente ou criar a textura e a exibição ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="ab7fa-126">Creating a texture and loading its initial data can be done in two different ways: create a texture and view separately, or create both the texture and the view at the same time.</span></span> <span data-ttu-id="ab7fa-127">A API fornece as duas técnicas para que você possa escolher quais são as mais adequados às suas necessidades.</span><span class="sxs-lookup"><span data-stu-id="ab7fa-127">The API provides both techniques so you can choose which better suits your needs.</span></span>

### <a name="create-texture-and-view-separately"></a><span data-ttu-id="ab7fa-128">Criar textura e exibir separadamente</span><span class="sxs-lookup"><span data-stu-id="ab7fa-128">Create Texture and View Separately</span></span>

<span data-ttu-id="ab7fa-129">A maneira mais fácil de criar uma textura é carregá-la de um arquivo de imagem.</span><span class="sxs-lookup"><span data-stu-id="ab7fa-129">The easiest way to create a texture is to load it from an image file.</span></span> <span data-ttu-id="ab7fa-130">Para criar a textura, basta preencher uma estrutura e fornecer o nome da textura para [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md).</span><span class="sxs-lookup"><span data-stu-id="ab7fa-130">To create the texture, just fill in one structure and provide the texture's name to [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md).</span></span>


```
ID3D10Device *pDevice = NULL;
// Initialize D3D10 device...

D3DX10_IMAGE_LOAD_INFO loadInfo;
ZeroMemory( &loadInfo, sizeof(D3DX10_IMAGE_LOAD_INFO) );
loadInfo.BindFlags = D3D10_BIND_SHADER_RESOURCE;

ID3D10Resource *pTexture = NULL;
D3DX10CreateTextureFromFile( pDevice, L"sample.bmp", &loadInfo, NULL, &pTexture, NULL );
```



<span data-ttu-id="ab7fa-131">A função D3DX [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md) faz três coisas: primeiro, ela cria um objeto de textura Direct3D 10; em segundo lugar, ele lê o arquivo de imagem de entrada; em terceiro lugar, ele armazena os dados da imagem no objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="ab7fa-131">The D3DX function [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md) does three things: first, it creates a Direct3D 10 texture object; second, it reads the input image file; third, it stores the image data in the texture object.</span></span> <span data-ttu-id="ab7fa-132">No exemplo acima, um arquivo BMP é carregado, mas a função pode carregar uma variedade de tipos de arquivo.</span><span class="sxs-lookup"><span data-stu-id="ab7fa-132">In the sample above, a BMP file is loaded, but the function can load a variety of file types.</span></span>

<span data-ttu-id="ab7fa-133">O sinalizador BIND indica que a textura será criada como um recurso de sombreador que permite que um estágio de sombreador Leia a partir da textura durante a renderização.</span><span class="sxs-lookup"><span data-stu-id="ab7fa-133">The bind flag indicates the texture will be created as a shader resource which allows a shader stage to read from the texture during rendering.</span></span>

<span data-ttu-id="ab7fa-134">O exemplo acima não especifica todos os parâmetros de carregamento.</span><span class="sxs-lookup"><span data-stu-id="ab7fa-134">The above example does not specify all of the loading parameters.</span></span> <span data-ttu-id="ab7fa-135">Na verdade, geralmente é benéfico simplesmente zerar os parâmetros de carregamento, pois isso permite que o D3DX escolha os valores apropriados com base na imagem de entrada.</span><span class="sxs-lookup"><span data-stu-id="ab7fa-135">In fact, it's often beneficial to simply zero out the loading parameters as this enables D3DX to choose appropriate values based on the input image.</span></span> <span data-ttu-id="ab7fa-136">Se você quiser que a imagem de entrada determine todos os parâmetros com os quais a textura é criada, basta especificar **NULL** para o parâmetro **loadinfo** da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="ab7fa-136">If you want the input image to determine all of the parameters the texture is created with, simply specify **NULL** for the **loadInfo** parameter like this:</span></span>


```
D3DX10CreateTextureFromFile( pDevice, L"sample.bmp", NULL, NULL, &pTexture, NULL );
```



<span data-ttu-id="ab7fa-137">A especificação de **NULL** para as informações de carregamento é um atalho simples, mas poderoso.</span><span class="sxs-lookup"><span data-stu-id="ab7fa-137">Specifying **NULL** for the loading information is a simple yet powerful shortcut.</span></span>

<span data-ttu-id="ab7fa-138">Agora que uma textura foi criada, você precisa criar uma exibição de recurso de sombreador para que a textura possa ser associada como uma entrada a um sombreador.</span><span class="sxs-lookup"><span data-stu-id="ab7fa-138">Now that a texture has been created, you need to create a shader-resource view so that the texture can be bound as an input to a shader.</span></span> <span data-ttu-id="ab7fa-139">Como [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md) retorna um ponteiro para um recurso e não um ponteiro para uma textura, você precisa determinar o tipo exato de recurso que foi carregado e, em seguida, pode criar uma exibição de recurso de sombreador usando [**CreateShaderResourceView**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createshaderresourceview).</span><span class="sxs-lookup"><span data-stu-id="ab7fa-139">Since [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md) returns a pointer to a resource and not a pointer to a texture, you have to determine the exact type of resource that was loaded, and then you can create a shader-resource view using [**CreateShaderResourceView**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createshaderresourceview).</span></span>


```
D3D10_SHADER_RESOURCE_VIEW_DESC srvDesc;
D3D10_RESOURCE_DIMENSION type;
pTexture->GetType( &type );
switch( type )
{
    case D3D10_RESOURCE_DIMENSION_BUFFER:
    //...
    break;
    case D3D10_RESOURCE_DIMENSION_TEXTURE1D:
    //...
    break;
    case D3D10_RESOURCE_DIMENSION_TEXTURE2D:
    {
        D3D10_TEXTURE2D_DESC desc;
        ID3D10Texture2D *pTexture2D = (ID3D10Texture2D*)pTexture;
        pTexture2D->GetDesc( &desc );
        
        srvDesc.Format = desc.Format;
        srvDesc.ViewDimension = D3D10_SRV_DIMENSION_TEXTURE2D;
        srvDesc.Texture2D.MipLevels = desc.MipLevels;
        srvDesc.Texture2D.MostDetailedMip = desc.MipLevels -1;

    }
    break;
    case D3D10_RESOURCE_DIMENSION_TEXTURE3D:
    //...
    break;
    default:
    //...
    break;
}

ID3D10ShaderResourceView *pSRView = NULL;
pDevice->CreateShaderResourceView( pTexture, &srvDesc, &pSRView );
```



<span data-ttu-id="ab7fa-140">Embora o exemplo acima crie uma exibição de recurso de sombreador 2D, o código para criar outros tipos de modo de exibição de recurso de sombreador é muito semelhante.</span><span class="sxs-lookup"><span data-stu-id="ab7fa-140">Although the above sample creates a 2D shader-resource view, the code to create other shader-resource view types is very similar.</span></span> <span data-ttu-id="ab7fa-141">Qualquer estágio do sombreador agora pode usar essa textura como uma entrada.</span><span class="sxs-lookup"><span data-stu-id="ab7fa-141">Any shader stage can now use this texture as an input.</span></span>

<span data-ttu-id="ab7fa-142">Usar [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md) e [**CreateShaderResourceView**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createshaderresourceview) para criar uma textura e sua exibição associada é uma maneira de preparar uma textura para ser associada a um estágio do sombreador.</span><span class="sxs-lookup"><span data-stu-id="ab7fa-142">Using [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md) and [**CreateShaderResourceView**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createshaderresourceview) to create a texture and its associated view is one way to prepare a texture to be bound to a shader stage.</span></span> <span data-ttu-id="ab7fa-143">Outra maneira de fazer isso é criar a textura e sua exibição ao mesmo tempo, que é abordado na próxima seção.</span><span class="sxs-lookup"><span data-stu-id="ab7fa-143">Another way to do so is to create both the texture and its view at the same time, which is discussed in the next section.</span></span>

### <a name="create-texture-and-view-simultaneously"></a><span data-ttu-id="ab7fa-144">Criar textura e exibição simultaneamente</span><span class="sxs-lookup"><span data-stu-id="ab7fa-144">Create Texture and View Simultaneously</span></span>

<span data-ttu-id="ab7fa-145">O Direct3D 10 exige uma textura e uma exibição de recurso de sombreador para ler de uma textura durante o tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="ab7fa-145">Direct3D 10 requires both a texture and a shader-resource view to read from a texture during runtime.</span></span> <span data-ttu-id="ab7fa-146">Como a criação de uma textura e uma exibição de recurso de sombreador é uma tarefa comum, o D3DX fornece o [**D3DX10CreateShaderResourceViewFromFile**](d3dx10createshaderresourceviewfromfile.md) para fazer isso por você.</span><span class="sxs-lookup"><span data-stu-id="ab7fa-146">Since the creation of a texture and a shader-resource view is such a common task, D3DX provides the [**D3DX10CreateShaderResourceViewFromFile**](d3dx10createshaderresourceviewfromfile.md) to do it for you.</span></span>


```
D3DX10_IMAGE_LOAD_INFO loadInfo;
ZeroMemory( &loadInfo, sizeof(D3DX10_IMAGE_LOAD_INFO) );
loadInfo.BindFlags = D3D10_BIND_SHADER_RESOURCE;
loadInfo.Format = DXGI_FORMAT_BC1_UNORM;

ID3D10ShaderResourceView *pSRView = NULL;
D3DX10CreateShaderResourceViewFromFile( pDevice, L"sample.bmp", &loadInfo, NULL, &pSRView, NULL );
```



<span data-ttu-id="ab7fa-147">Com uma única chamada D3DX, o modo de exibição de recurso textura e sombreador são criados.</span><span class="sxs-lookup"><span data-stu-id="ab7fa-147">With a single D3DX call, both the texture and shader-resource view are created.</span></span> <span data-ttu-id="ab7fa-148">A funcionalidade do parâmetro **loadinfo** é inalterada; Você pode usá-lo para personalizar como a textura é criada ou derivar os parâmetros necessários do arquivo de entrada, especificando **NULL** para o parâmetro **loadinfo** .</span><span class="sxs-lookup"><span data-stu-id="ab7fa-148">The functionality of the **loadInfo** parameter is unchanged; you can use it to customize how the texture is created, or derive the necessary parameters from the input file by specifying **NULL** for the **loadInfo** parameter.</span></span>

<span data-ttu-id="ab7fa-149">O objeto [**ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview) retornado pela função [**D3DX10CreateShaderResourceViewFromFile**](d3dx10createshaderresourceviewfromfile.md) pode ser usado posteriormente para recuperar a interface [**ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource) original, se necessário.</span><span class="sxs-lookup"><span data-stu-id="ab7fa-149">The [**ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview) object returned by the [**D3DX10CreateShaderResourceViewFromFile**](d3dx10createshaderresourceviewfromfile.md) function can later be used to retrieve the original [**ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource) interface if it is needed.</span></span> <span data-ttu-id="ab7fa-150">Isso pode ser feito chamando o método [**getResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10view-getresource) .</span><span class="sxs-lookup"><span data-stu-id="ab7fa-150">This can be done by calling the [**GetResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10view-getresource) method.</span></span>

<span data-ttu-id="ab7fa-151">O D3DX fornece uma única função para criar uma textura e uma exibição de recurso de sombreador como um convienience; cabe a você decidir qual método de criação de uma textura e exibição é mais adequado às necessidades do seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ab7fa-151">D3DX provides a single function to create a texture and shader-resource view as a convienience; it is up to you to decide which method of creating a texture and view best suits the needs of your application.</span></span>

<span data-ttu-id="ab7fa-152">Agora que você sabe como criar uma textura e sua exibição de recurso de sombreador, a próxima seção mostrará como você pode fazer amostragem (leitura) dessa textura usando um sombreador.</span><span class="sxs-lookup"><span data-stu-id="ab7fa-152">Now that you know how to create a texture and its shader-resource view, the next section will show you how you can sample (read) from that texture using a shader.</span></span>

## <a name="creating-empty-textures"></a><span data-ttu-id="ab7fa-153">Criando texturas vazias</span><span class="sxs-lookup"><span data-stu-id="ab7fa-153">Creating Empty Textures</span></span>

<span data-ttu-id="ab7fa-154">Às vezes, os aplicativos desejarão criar uma textura e computar os dados a serem armazenados na textura ou usar o [pipeline](d3d10-graphics-programming-guide-pipeline-stages.md) de gráficos para renderizar para essa textura e, posteriormente, usar os resultados em outro processamento.</span><span class="sxs-lookup"><span data-stu-id="ab7fa-154">Sometimes applications will want to create a texture and compute the data to be stored in the texture, or use the graphics [pipeline](d3d10-graphics-programming-guide-pipeline-stages.md) to render to this texture and later use the results in other processing.</span></span> <span data-ttu-id="ab7fa-155">Essas texturas podem ser atualizadas pelo pipeline de gráficos ou pelo próprio aplicativo, dependendo do tipo de [**uso**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage) especificado para a textura quando ela foi criada.</span><span class="sxs-lookup"><span data-stu-id="ab7fa-155">These textures could be updated by the graphics pipeline or by the application itself, depending on what kind of [**usage**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage) was specified for the texture when it was created.</span></span>

### <a name="rendering-to-a-texture"></a><span data-ttu-id="ab7fa-156">Renderizando para uma textura</span><span class="sxs-lookup"><span data-stu-id="ab7fa-156">Rendering to a texture</span></span>

<span data-ttu-id="ab7fa-157">O caso mais comum de criar uma textura vazia para ser preenchida com dados durante o tempo de execução é o caso em que um aplicativo deseja renderizar para uma textura e, em seguida, usar os resultados da operação de renderização em uma passagem subsequente.</span><span class="sxs-lookup"><span data-stu-id="ab7fa-157">The most common case of creating an empty texture to be filled with data during runtime is the case where an application wants to render to a texture and then use the results of the rendering operation in a subsequent pass.</span></span> <span data-ttu-id="ab7fa-158">As texturas criadas com essa finalidade devem especificar o [**uso**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage)padrão.</span><span class="sxs-lookup"><span data-stu-id="ab7fa-158">Textures created with this purpose should specify default [**usage**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage).</span></span>

<span data-ttu-id="ab7fa-159">O exemplo de código a seguir cria uma textura vazia que o pipeline pode processar e, subsequentemente, usar como uma entrada para um [sombreador](../direct3dhlsl/dx-graphics-hlsl-using-shaders-10.md).</span><span class="sxs-lookup"><span data-stu-id="ab7fa-159">The following code sample creates an empty texture that the pipeline can render to and subsequently use as an input to a [shader](../direct3dhlsl/dx-graphics-hlsl-using-shaders-10.md).</span></span>


```
// Create the render target texture
D3D10_TEXTURE2D_DESC desc;
ZeroMemory( &desc, sizeof(desc) );
desc.Width = 256;
desc.Height = 256;
desc.MipLevels = 1;
desc.ArraySize = 1;
desc.Format = DXGI_FORMAT_R32G32B32A32_FLOAT;
desc.SampleDesc.Count = 1;
desc.Usage = D3D10_USAGE_DEFAULT;
desc.BindFlags = D3D10_BIND_RENDER_TARGET | D3D10_BIND_SHADER_RESOURCE;

ID3D10Texture2D *pRenderTarget = NULL;
pDevice->CreateTexture2D( &desc, NULL, &pRenderTarget );
```



<span data-ttu-id="ab7fa-160">A criação da textura exige que o aplicativo especifique algumas informações sobre as propriedades que a textura terá.</span><span class="sxs-lookup"><span data-stu-id="ab7fa-160">Creating the texture requires the application to specify some information about the properties the texture will have.</span></span> <span data-ttu-id="ab7fa-161">A largura e a altura da textura em texels são definidas como 256.</span><span class="sxs-lookup"><span data-stu-id="ab7fa-161">The width and height of the texture in texels is set to 256.</span></span> <span data-ttu-id="ab7fa-162">Para esse destino de renderização, um único nível de mipmap é tudo o que precisamos.</span><span class="sxs-lookup"><span data-stu-id="ab7fa-162">For this render target, a single mipmap level is all we need.</span></span> <span data-ttu-id="ab7fa-163">Somente um destino de renderização é necessário para que o tamanho da matriz seja definido como 1.</span><span class="sxs-lookup"><span data-stu-id="ab7fa-163">Only one render target is required so the array size is set to 1.</span></span> <span data-ttu-id="ab7fa-164">Cada Texel contém valores de ponto flutuante de 4 32 bits, que podem ser usados para armazenar informações muito precisas (consulte o [**\_ formato dxgi**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)).</span><span class="sxs-lookup"><span data-stu-id="ab7fa-164">Each texel contains four 32-bit floating point values, which can be used to store very precise information (see [**DXGI\_FORMAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)).</span></span> <span data-ttu-id="ab7fa-165">Um exemplo por pixel é tudo o que será necessário.</span><span class="sxs-lookup"><span data-stu-id="ab7fa-165">One sample per pixel is all that will be needed.</span></span> <span data-ttu-id="ab7fa-166">O uso é definido como padrão, pois isso permite o posicionamento mais eficiente do destino de renderização na memória.</span><span class="sxs-lookup"><span data-stu-id="ab7fa-166">The usage is set to default because this allows for the most efficient placement of the render target in memory.</span></span> <span data-ttu-id="ab7fa-167">Por fim, o fato de que a textura será associada como um destino de renderização e um recurso de sombreador em diferentes pontos no tempo é especificado.</span><span class="sxs-lookup"><span data-stu-id="ab7fa-167">Finally, the fact that the texture will be bound as a render target and a shader resource at different points in time is specified.</span></span>

<span data-ttu-id="ab7fa-168">As texturas não podem ser associadas diretamente para renderização no pipeline; Use uma exibição de destino de renderização, conforme mostrado no exemplo de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="ab7fa-168">Textures cannot be bound for rendering to the pipeline directly; use a render-target view as shown in the following code sample.</span></span>


```
D3D10_RENDER_TARGET_VIEW_DESC rtDesc;
rtDesc.Format = desc.Format;
rtDesc.ViewDimension = D3D10_RTV_DIMENSION_TEXTURE2D;
rtDesc.Texture2D.MipSlice = 0;

ID3D10RenderTargetView *pRenderTargetView = NULL;
pDevice->CreateRenderTargetView( pRenderTarget, &rtDesc, &pRenderTargetView );
```



<span data-ttu-id="ab7fa-169">O formato da exibição de destino de renderização é simplesmente definido como o formato da textura original.</span><span class="sxs-lookup"><span data-stu-id="ab7fa-169">The format of the render-target view is simply set to the format of the original texture.</span></span> <span data-ttu-id="ab7fa-170">As informações no recurso devem ser interpretadas como uma textura 2D e só queremos usar o primeiro nível de mipmap do destino de renderização.</span><span class="sxs-lookup"><span data-stu-id="ab7fa-170">The information in the resource should be interpreted as a 2D texture, and we only want to use the first mipmap level of the render target.</span></span>

<span data-ttu-id="ab7fa-171">Da mesma forma como uma exibição de destino de renderização deve ser criada para que o destino de renderização possa ser associado à saída para o pipeline, um modo de exibição de recurso de sombreador deve ser criado para que o destino de renderização possa ser associado ao pipeline como uma entrada.</span><span class="sxs-lookup"><span data-stu-id="ab7fa-171">Similarly to how a render-target view must be created so that the render target can be bound for output to the pipeline, a shader-resource view must be created so that the render target can be bound to the pipeline as an input.</span></span> <span data-ttu-id="ab7fa-172">O exemplo de código a seguir demonstra isso.</span><span class="sxs-lookup"><span data-stu-id="ab7fa-172">The following code sample demonstrates this.</span></span>


```
// Create the shader-resource view
D3D10_SHADER_RESOURCE_VIEW_DESC srDesc;
srDesc.Format = desc.Format;
srDesc.ViewDimension = D3D10_SRV_DIMENSION_TEXTURE2D;
srDesc.Texture2D.MostDetailedMip = 0;
srDesc.Texture2D.MipLevels = 1;

ID3D10ShaderResourceView *pShaderResView = NULL;
pDevice->CreateShaderResourceView( pRenderTarget, &srDesc, &pShaderResView );
```



<span data-ttu-id="ab7fa-173">Os parâmetros de sombreador – descrições de modo de exibição de recursos são muito semelhantes aos das descrições de exibição de destino de renderização e foram escolhidos pelos mesmos motivos.</span><span class="sxs-lookup"><span data-stu-id="ab7fa-173">The parameters of shader-resource view descriptions are very similar to those of render-target view descriptions and were chosen for the same reasons.</span></span>

### <a name="filling-textures-manually"></a><span data-ttu-id="ab7fa-174">Preenchendo texturas manualmente</span><span class="sxs-lookup"><span data-stu-id="ab7fa-174">Filling Textures Manually</span></span>

<span data-ttu-id="ab7fa-175">Às vezes, os aplicativos gostariam de calcular valores em tempo de execução, colocá-los em uma textura manualmente e, em seguida, fazer com que o [pipeline](d3d10-graphics-programming-guide-pipeline-stages.md) de gráficos Use essa textura em operações de renderização posteriores.</span><span class="sxs-lookup"><span data-stu-id="ab7fa-175">Sometimes applications would like to compute values at runtime, put them into a texture manually and then have the graphics [pipeline](d3d10-graphics-programming-guide-pipeline-stages.md) use this texture in later rendering operations.</span></span> <span data-ttu-id="ab7fa-176">Para fazer isso, o aplicativo deve criar uma textura vazia de forma a permitir que a CPU acesse a memória subjacente.</span><span class="sxs-lookup"><span data-stu-id="ab7fa-176">To do this, the application must create an empty texture in such a way to allow the CPU to access the underlying memory.</span></span> <span data-ttu-id="ab7fa-177">Isso é feito criando uma textura dinâmica e obtendo acesso à memória subjacente chamando um método específico.</span><span class="sxs-lookup"><span data-stu-id="ab7fa-177">This is done by creating a dynamic texture and gaining access to the underlying memory by calling a particular method.</span></span> <span data-ttu-id="ab7fa-178">O exemplo de código a seguir demonstra como fazer isso.</span><span class="sxs-lookup"><span data-stu-id="ab7fa-178">The following code sample demonstrates how to do this.</span></span>


```
D3D10_TEXTURE2D_DESC desc;
desc.Width = 256;
desc.Height = 256;
desc.MipLevels = desc.ArraySize = 1;
desc.Format = DXGI_FORMAT_R8G8B8A8_UNORM;
desc.SampleDesc.Count = 1;
desc.Usage = D3D10_USAGE_DYNAMIC;
desc.BindFlags = D3D10_BIND_SHADER_RESOURCE;
desc.CPUAccessFlags = D3D10_CPU_ACCESS_WRITE;
ID3D10Texture2D *pTexture = NULL;
pd3dDevice->CreateTexture2D( &desc, NULL, &pTexture );
```



<span data-ttu-id="ab7fa-179">Observe que o formato é definido como um 32 bits por pixel, em que cada componente é definido por 8 bits.</span><span class="sxs-lookup"><span data-stu-id="ab7fa-179">Note that the format is set to a 32 bits per pixel where each component is defined by 8 bits.</span></span> <span data-ttu-id="ab7fa-180">O parâmetro Usage é definido como dinâmico, enquanto os sinalizadores de associação são definidos para especificar que a textura será acessada por um sombreador.</span><span class="sxs-lookup"><span data-stu-id="ab7fa-180">The usage parameter is set to dynamic while the bind flags are set to specify the texture will be accessed by a shader.</span></span> <span data-ttu-id="ab7fa-181">O restante da descrição da textura é semelhante à criação de um destino de renderização.</span><span class="sxs-lookup"><span data-stu-id="ab7fa-181">The rest of the texture description is similar to creating a render target.</span></span>

<span data-ttu-id="ab7fa-182">O [**mapa**](/windows/desktop/api/D3D10/nf-d3d10-id3d10texture2d-map) de chamada permite que o aplicativo acesse a memória subjacente da textura.</span><span class="sxs-lookup"><span data-stu-id="ab7fa-182">Calling [**Map**](/windows/desktop/api/D3D10/nf-d3d10-id3d10texture2d-map) enables the application to access the underlying memory of the texture.</span></span> <span data-ttu-id="ab7fa-183">O ponteiro recuperado é usado para preencher a textura com dados.</span><span class="sxs-lookup"><span data-stu-id="ab7fa-183">The pointer retrieved is then used to fill the texture with data.</span></span> <span data-ttu-id="ab7fa-184">Isso pode ser visto no exemplo de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="ab7fa-184">This can be seen in the following code sample.</span></span>


```
D3D10_MAPPED_TEXTURE2D mappedTex;
pTexture->Map( D3D10CalcSubresource(0, 0, 1), D3D10_MAP_WRITE_DISCARD, 0, &mappedTex );

UCHAR* pTexels = (UCHAR*)mappedTex.pData;
for( UINT row = 0; row < desc.Height; row++ )
{
    UINT rowStart = row * mappedTex.RowPitch;
    for( UINT col = 0; col < desc.Width; col++ )
    {
        UINT colStart = col * 4;
        pTexels[rowStart + colStart + 0] = 255; // Red
        pTexels[rowStart + colStart + 1] = 128; // Green
        pTexels[rowStart + colStart + 2] = 64;  // Blue
        pTexels[rowStart + colStart + 3] = 32;  // Alpha
    }
}

pTexture->Unmap( D3D10CalcSubresource(0, 0, 1) );
```



## <a name="multiple-rendertargets"></a><span data-ttu-id="ab7fa-185">Vários Rendertargets</span><span class="sxs-lookup"><span data-stu-id="ab7fa-185">Multiple Rendertargets</span></span>

<span data-ttu-id="ab7fa-186">Até oito exibições de destino de renderização podem ser associadas ao pipeline de cada vez (com [**OMSetRenderTargets**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-omsetrendertargets)).</span><span class="sxs-lookup"><span data-stu-id="ab7fa-186">Up to eight render-target views can be bound to the pipeline at a time (with [**OMSetRenderTargets**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-omsetrendertargets)).</span></span> <span data-ttu-id="ab7fa-187">Para cada pixel (ou cada amostra se a multiamostragem estiver habilitada), a mesclagem é feita de forma independente para cada exibição de destino de renderização.</span><span class="sxs-lookup"><span data-stu-id="ab7fa-187">For each pixel (or each sample if multisampling is enabled), blending is done independently for each render-target view.</span></span> <span data-ttu-id="ab7fa-188">Duas das variáveis de estado de mistura-BlendEnable e RenderTargetWriteMask-são matrizes de oito, cada membro de matriz corresponde a uma exibição de destino de renderização.</span><span class="sxs-lookup"><span data-stu-id="ab7fa-188">Two of the blend state variables - BlendEnable and RenderTargetWriteMask - are arrays of eight, each array member corresponds to a render-target view.</span></span> <span data-ttu-id="ab7fa-189">Ao usar vários destinos de renderização, cada destino de renderização deve ser o mesmo [tipo de recurso](d3d10-graphics-programming-guide-resources-types.md) (buffer, textura 1D, matriz de textura 2D etc.) e deve ter a mesma dimensão (largura, altura, profundidade para texturas 3D e tamanho da matriz para matrizes de textura).</span><span class="sxs-lookup"><span data-stu-id="ab7fa-189">When using multiple render targets, each render target must be the same [resource type](d3d10-graphics-programming-guide-resources-types.md) (buffer, 1D texture, 2D texture array, etc.) and must have the same dimension (width, height, depth for 3D textures, and array size for texture arrays).</span></span> <span data-ttu-id="ab7fa-190">Se os destinos de renderização forem de várias amostras, eles deverão ter o mesmo número de amostras por pixel.</span><span class="sxs-lookup"><span data-stu-id="ab7fa-190">If the render targets are multisampled, then they must all have the same number of samples per pixel.</span></span>

<span data-ttu-id="ab7fa-191">Pode haver apenas um buffer de estêncil de profundidade ativo, independentemente de quantos destinos de renderização estão ativos.</span><span class="sxs-lookup"><span data-stu-id="ab7fa-191">There can only be one depth-stencil buffer active, regardless of how many render targets are active.</span></span> <span data-ttu-id="ab7fa-192">Ao usar matrizes de textura como destinos de renderização, todas as dimensões de exibição devem corresponder.</span><span class="sxs-lookup"><span data-stu-id="ab7fa-192">When using texture arrays as render targets, all view dimensions must match.</span></span> <span data-ttu-id="ab7fa-193">Os destinos de renderização não precisam ter o mesmo formato de textura.</span><span class="sxs-lookup"><span data-stu-id="ab7fa-193">The render targets do not need to have the same texture format.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ab7fa-194">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ab7fa-194">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ab7fa-195">Recursos (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="ab7fa-195">Resources (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 
