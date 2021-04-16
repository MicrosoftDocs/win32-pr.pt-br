---
description: Os materiais descrevem como os polígonos refletem a luz ou parecem emitir luz em uma cena 3D.
ms.assetid: vs|directx_sdk|~\materials.htm
title: Materiais (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64e75953fd5839e1b3e7b9cc89b7331147cdb585
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104566690"
---
# <a name="materials-direct3d-9"></a><span data-ttu-id="739a4-103">Materiais (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="739a4-103">Materials (Direct3D 9)</span></span>

<span data-ttu-id="739a4-104">Os materiais descrevem como os polígonos refletem a luz ou parecem emitir luz em uma cena 3D.</span><span class="sxs-lookup"><span data-stu-id="739a4-104">Materials describe how polygons reflect light or appear to emit light in a 3D scene.</span></span> <span data-ttu-id="739a4-105">As propriedades de material detalham a reflexão difusa de um material, a reflexão de ambiente, a emissão de luz e as características de realce especular.</span><span class="sxs-lookup"><span data-stu-id="739a4-105">Material properties detail a material's diffuse reflection, ambient reflection, light emission, and specular highlight characteristics.</span></span> <span data-ttu-id="739a4-106">O Direct3D usa a estrutura [**D3DMATERIAL9**](d3dmaterial9.md) para transportar todas as informações de propriedade de material.</span><span class="sxs-lookup"><span data-stu-id="739a4-106">Direct3D uses the [**D3DMATERIAL9**](d3dmaterial9.md) structure to carry all material property information.</span></span> <span data-ttu-id="739a4-107">Com exceção da propriedade especular, cada propriedade é descrita como uma cor RGBA que representa a quantidade de partes vermelha, verde e azul de um determinado tipo de luz que ele reflete e um fator de mistura alfa.</span><span class="sxs-lookup"><span data-stu-id="739a4-107">With the exception of the specular property, each property is described as an RGBA color that represents how much of the red, green, and blue parts of a given type of light it reflects, and an alpha blending factor.</span></span>

## <a name="diffuse-and-ambient-reflection"></a><span data-ttu-id="739a4-108">Difuso e reflexo de ambiente</span><span class="sxs-lookup"><span data-stu-id="739a4-108">Diffuse and Ambient Reflection</span></span>

<span data-ttu-id="739a4-109">Os membros difuso e de ambiente da estrutura [**D3DMATERIAL9**](d3dmaterial9.md) descrevem como um material reflete o ambiente e a luz difusa em uma cena.</span><span class="sxs-lookup"><span data-stu-id="739a4-109">The Diffuse and Ambient members of the [**D3DMATERIAL9**](d3dmaterial9.md) structure describe how a material reflects the ambient and diffuse light in a scene.</span></span> <span data-ttu-id="739a4-110">Como a maioria das cenas contém muito mais luz difusa do que a luz ambiente, a reflexão difusa desempenha a maior parte na determinação da cor.</span><span class="sxs-lookup"><span data-stu-id="739a4-110">Because most scenes contain much more diffuse light than ambient light, diffuse reflection plays the largest part in determining color.</span></span> <span data-ttu-id="739a4-111">Além disso, como a luz difusa é direcional, o ângulo de incidência para a luz difusa afeta a intensidade geral da reflexão.</span><span class="sxs-lookup"><span data-stu-id="739a4-111">Additionally, because diffuse light is directional, the angle of incidence for diffuse light affects the overall intensity of the reflection.</span></span> <span data-ttu-id="739a4-112">A reflexão difusa é maior quando a luz atinge um vértice paralelo ao vértice normal.</span><span class="sxs-lookup"><span data-stu-id="739a4-112">Diffuse reflection is greatest when the light strikes a vertex parallel to the vertex normal.</span></span> <span data-ttu-id="739a4-113">À medida que o ângulo aumenta, o efeito da reflexão difusa diminui.</span><span class="sxs-lookup"><span data-stu-id="739a4-113">As the angle increases, the effect of diffuse reflection diminishes.</span></span> <span data-ttu-id="739a4-114">A quantidade de luz refletida é o cosseno do ângulo entre a luz de entrada e o vértice normal, conforme mostrado na ilustração a seguir.</span><span class="sxs-lookup"><span data-stu-id="739a4-114">The amount of light reflected is the cosine of the angle between the incoming light and the vertex normal, as shown in the following illustration.</span></span>

![ilustração da quantidade de luz refletida](images/incident.png)

<span data-ttu-id="739a4-116">A reflexão de ambiente, como a luz ambiente, não é direcional.</span><span class="sxs-lookup"><span data-stu-id="739a4-116">Ambient reflection, like ambient light, is nondirectional.</span></span> <span data-ttu-id="739a4-117">A reflexão de ambiente tem um impacto menor na cor aparente de um objeto renderizado, mas afeta a cor geral e é mais perceptível quando pouco ou nenhuma luz difusa reflete o material.</span><span class="sxs-lookup"><span data-stu-id="739a4-117">Ambient reflection has a lesser impact on the apparent color of a rendered object, but it does affect the overall color and is most noticeable when little or no diffuse light reflects off the material.</span></span> <span data-ttu-id="739a4-118">A reflexão de ambiente de um material é afetada pela luz ambiente definida para uma cena chamando o método [**IDirect3DDevice9:: Setrenderingstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) com o \_ sinalizador de ambiente D3DRS.</span><span class="sxs-lookup"><span data-stu-id="739a4-118">A material's ambient reflection is affected by the ambient light set for a scene by calling the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method with the D3DRS\_AMBIENT flag.</span></span>

<span data-ttu-id="739a4-119">A forma difusa e a reflexão de ambiente funcionam em conjunto para determinar a cor percebida de um objeto e geralmente são valores idênticos.</span><span class="sxs-lookup"><span data-stu-id="739a4-119">Diffuse and ambient reflection work together to determine the perceived color of an object, and are usually identical values.</span></span> <span data-ttu-id="739a4-120">Por exemplo, para renderizar um objeto Blue crystalline, você cria um material que reflete apenas o componente azul da luz difusa e ambiente.</span><span class="sxs-lookup"><span data-stu-id="739a4-120">For example, to render a blue crystalline object, you create a material that reflects only the blue component of diffuse and ambient light.</span></span> <span data-ttu-id="739a4-121">Quando colocado em uma sala com uma luz branca, o cristal parece azul.</span><span class="sxs-lookup"><span data-stu-id="739a4-121">When placed in a room with a white light, the crystal appears to be blue.</span></span> <span data-ttu-id="739a4-122">No entanto, em uma sala que tem apenas uma luz vermelha, o mesmo cristal pareceria preto, porque seu material não reflete a luz vermelha.</span><span class="sxs-lookup"><span data-stu-id="739a4-122">However, in a room that has only red light, the same crystal would appear to be black, because its material doesn't reflect red light.</span></span>

## <a name="emission"></a><span data-ttu-id="739a4-123">Emissão</span><span class="sxs-lookup"><span data-stu-id="739a4-123">Emission</span></span>

<span data-ttu-id="739a4-124">Os materiais podem ser usados para fazer com que um objeto renderizado pareça ser Luminous.</span><span class="sxs-lookup"><span data-stu-id="739a4-124">Materials can be used to make a rendered object appear to be self-luminous.</span></span> <span data-ttu-id="739a4-125">O membro emissiva da estrutura [**D3DMATERIAL9**](d3dmaterial9.md) é usado para descrever a cor e a transparência da luz emitida.</span><span class="sxs-lookup"><span data-stu-id="739a4-125">The Emissive member of the [**D3DMATERIAL9**](d3dmaterial9.md) structure is used to describe the color and transparency of the emitted light.</span></span> <span data-ttu-id="739a4-126">A emissão afeta a cor de um objeto e pode, por exemplo, tornar um material escuro mais claro e adotar parte da cor emitida.</span><span class="sxs-lookup"><span data-stu-id="739a4-126">Emission affects an object's color and can, for example, make a dark material brighter and take on part of the emitted color.</span></span>

<span data-ttu-id="739a4-127">Você pode usar a propriedade emissiva de um material para adicionar a ilusão de que um objeto está emitindo luz, sem incorrer na sobrecarga computacional de adicionar uma luz à cena.</span><span class="sxs-lookup"><span data-stu-id="739a4-127">You can use a material's emissive property to add the illusion that an object is emitting light, without incurring the computational overhead of adding a light to the scene.</span></span> <span data-ttu-id="739a4-128">No caso do Crystal azul, a propriedade emissiva será útil se você quiser fazer com que o Crystal pareça acender, mas não convertê-la em outros objetos da cena.</span><span class="sxs-lookup"><span data-stu-id="739a4-128">In the case of the blue crystal, the emissive property is useful if you want to make the crystal appear to light up, but not cast light on other objects in the scene.</span></span> <span data-ttu-id="739a4-129">Lembre-se de que os materiais com as propriedades emissiva não emitem a luz que pode ser refletida por outros objetos em uma cena.</span><span class="sxs-lookup"><span data-stu-id="739a4-129">Remember, materials with emissive properties don't emit light that can be reflected by other objects in a scene.</span></span> <span data-ttu-id="739a4-130">Para atingir essa luz refletida, você precisa inserir uma luz adicional dentro da cena.</span><span class="sxs-lookup"><span data-stu-id="739a4-130">To achieve this reflected light, you need to place an additional light within the scene.</span></span>

## <a name="specular-reflection"></a><span data-ttu-id="739a4-131">Reflexão especular</span><span class="sxs-lookup"><span data-stu-id="739a4-131">Specular Reflection</span></span>

<span data-ttu-id="739a4-132">A reflexão especular cria destaques em objetos, fazendo com que eles pareçam brilhantes.</span><span class="sxs-lookup"><span data-stu-id="739a4-132">Specular reflection creates highlights on objects, making them appear shiny.</span></span> <span data-ttu-id="739a4-133">A estrutura [**D3DMATERIAL9**](d3dmaterial9.md) contém dois membros que descrevem a cor de realce especular, bem como a luminosidade geral do material.</span><span class="sxs-lookup"><span data-stu-id="739a4-133">The [**D3DMATERIAL9**](d3dmaterial9.md) structure contains two members that describe the specular highlight color as well as the material's overall shininess.</span></span> <span data-ttu-id="739a4-134">Você estabelece a cor dos destaques especulares Configurando o membro especular para a cor RGBA desejada-as cores mais comuns são brancas ou cinza claro.</span><span class="sxs-lookup"><span data-stu-id="739a4-134">You establish the color of the specular highlights by setting the Specular member to the desired RGBA color - the most common colors are white or light gray.</span></span> <span data-ttu-id="739a4-135">Os valores definidos no membro de energia controlam a nitidez dos efeitos especulares.</span><span class="sxs-lookup"><span data-stu-id="739a4-135">The values you set in the Power member control how sharp the specular effects are.</span></span>

<span data-ttu-id="739a4-136">Os destaques especulares podem criar efeitos consideráveis.</span><span class="sxs-lookup"><span data-stu-id="739a4-136">Specular highlights can create dramatic effects.</span></span> <span data-ttu-id="739a4-137">Desenhando novamente na analogia do cristal azul: um valor de potência maior cria destaques mais nítidos, fazendo com que o cristal pareça ser bastante brilhante.</span><span class="sxs-lookup"><span data-stu-id="739a4-137">Drawing again on the blue crystal analogy: a larger Power value creates sharper specular highlights, making the crystal appear to be quite shiny.</span></span> <span data-ttu-id="739a4-138">Valores menores aumentam a área do efeito, criando uma reflexão de graça que torna o cristal claro.</span><span class="sxs-lookup"><span data-stu-id="739a4-138">Smaller values increase the area of the effect, creating a dull reflection that make the crystal look frosty.</span></span> <span data-ttu-id="739a4-139">Para tornar um objeto realmente fosco, defina o membro de energia como zero e a cor em especular como preto.</span><span class="sxs-lookup"><span data-stu-id="739a4-139">To make an object truly matte, set the Power member to zero and the color in Specular to black.</span></span> <span data-ttu-id="739a4-140">Experimente diferentes níveis de reflexão para produzir uma aparência realista para suas necessidades.</span><span class="sxs-lookup"><span data-stu-id="739a4-140">Experiment with different levels of reflection to produce a realistic appearance for your needs.</span></span> <span data-ttu-id="739a4-141">A ilustração a seguir mostra dois modelos idênticos.</span><span class="sxs-lookup"><span data-stu-id="739a4-141">The following illustration shows two identical models.</span></span> <span data-ttu-id="739a4-142">Aquele à esquerda usa uma potência de reflexo especular de 10; o modelo à direita não tem nenhuma reflexão especular.</span><span class="sxs-lookup"><span data-stu-id="739a4-142">The one on the left uses a specular reflection power of 10; the model on the right has no specular reflection.</span></span>

![ilustração de modelos de reflexo especulares](images/spechigh.png)

## <a name="setting-material-properties"></a><span data-ttu-id="739a4-144">Definindo propriedades de material</span><span class="sxs-lookup"><span data-stu-id="739a4-144">Setting Material Properties</span></span>

<span data-ttu-id="739a4-145">Dispositivos de renderização de Direct3D podem ser renderizados com um conjunto de propriedades de material por vez.</span><span class="sxs-lookup"><span data-stu-id="739a4-145">Direct3D rendering devices can render with one set of material properties at a time.</span></span>

<span data-ttu-id="739a4-146">Em um aplicativo C++, você define as propriedades de material que o sistema usa ao preparar uma estrutura [**D3DMATERIAL9**](d3dmaterial9.md) e, em seguida, chamar o método [**IDirect3DDevice9:: SetMaterial**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setmaterial) .</span><span class="sxs-lookup"><span data-stu-id="739a4-146">In a C++ application, you set the material properties that the system uses by preparing a [**D3DMATERIAL9**](d3dmaterial9.md) structure, and then calling the [**IDirect3DDevice9::SetMaterial**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setmaterial) method.</span></span>

<span data-ttu-id="739a4-147">Para preparar a estrutura [**D3DMATERIAL9**](d3dmaterial9.md) para uso, defina as informações de propriedade na estrutura para criar o efeito desejado durante a renderização.</span><span class="sxs-lookup"><span data-stu-id="739a4-147">To prepare the [**D3DMATERIAL9**](d3dmaterial9.md) structure for use, set the property information in the structure to create the desired effect during rendering.</span></span> <span data-ttu-id="739a4-148">O exemplo de código a seguir configura a estrutura **D3DMATERIAL9** para um material roxo com destaques de especular branco nítido.</span><span class="sxs-lookup"><span data-stu-id="739a4-148">The following code example sets up the **D3DMATERIAL9** structure for a purple material with sharp white specular highlights.</span></span>


```
D3DMATERIAL9 mat;

// Set the RGBA for diffuse reflection.
mat.Diffuse.r = 0.5f;
mat.Diffuse.g = 0.0f;
mat.Diffuse.b = 0.5f;
mat.Diffuse.a = 1.0f;

// Set the RGBA for ambient reflection.
mat.Ambient.r = 0.5f;
mat.Ambient.g = 0.0f;
mat.Ambient.b = 0.5f;
mat.Ambient.a = 1.0f;

// Set the color and sharpness of specular highlights.
mat.Specular.r = 1.0f;
mat.Specular.g = 1.0f;
mat.Specular.b = 1.0f;
mat.Specular.a = 1.0f;
mat.Power = 50.0f;

// Set the RGBA for emissive color.
mat.Emissive.r = 0.0f;
mat.Emissive.g = 0.0f;
mat.Emissive.b = 0.0f;
mat.Emissive.a = 0.0f;
```



<span data-ttu-id="739a4-149">Depois de preparar a estrutura [**D3DMATERIAL9**](d3dmaterial9.md) , aplique as propriedades chamando o método [**IDirect3DDevice9:: SetMaterial**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setmaterial) do dispositivo de renderização.</span><span class="sxs-lookup"><span data-stu-id="739a4-149">After preparing the [**D3DMATERIAL9**](d3dmaterial9.md) structure, you apply the properties by calling the [**IDirect3DDevice9::SetMaterial**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setmaterial) method of the rendering device.</span></span> <span data-ttu-id="739a4-150">Esse método aceita o endereço de uma estrutura **D3DMATERIAL9** preparada como seu único parâmetro.</span><span class="sxs-lookup"><span data-stu-id="739a4-150">This method accepts the address of a prepared **D3DMATERIAL9** structure as its only parameter.</span></span> <span data-ttu-id="739a4-151">Você pode chamar **IDirect3DDevice9:: SetMaterial** com novas informações conforme necessário para atualizar as propriedades de material para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="739a4-151">You can call **IDirect3DDevice9::SetMaterial** with new information as needed to update the material properties for the device.</span></span> <span data-ttu-id="739a4-152">O exemplo de código a seguir mostra como isso pode parecer com o código.</span><span class="sxs-lookup"><span data-stu-id="739a4-152">The following code example shows how this might look in code.</span></span>


```
// This code example uses the material properties defined for 
// the mat variable earlier in this topic. The pd3dDev is assumed
// to be a valid pointer to an IDirect3DDevice9 interface.
HRESULT hr;
hr = pd3dDev->SetMaterial(&mat);
if(FAILED(hr))
{
    // Code to handle the error goes here.
}
```



<span data-ttu-id="739a4-153">Quando você cria um dispositivo Direct3D, o material atual é definido automaticamente como o padrão mostrado na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="739a4-153">When you create a Direct3D device, the current material is automatically set to the default shown in the following table.</span></span>



| <span data-ttu-id="739a4-154">Membro</span><span class="sxs-lookup"><span data-stu-id="739a4-154">Member</span></span>   | <span data-ttu-id="739a4-155">Valor</span><span class="sxs-lookup"><span data-stu-id="739a4-155">Value</span></span>                |
|----------|----------------------|
| <span data-ttu-id="739a4-156">Difusa</span><span class="sxs-lookup"><span data-stu-id="739a4-156">Diffuse</span></span>  | <span data-ttu-id="739a4-157">(R:0, G:0, B:0, A:0)</span><span class="sxs-lookup"><span data-stu-id="739a4-157">(R:0, G:0, B:0, A:0)</span></span> |
| <span data-ttu-id="739a4-158">Especular</span><span class="sxs-lookup"><span data-stu-id="739a4-158">Specular</span></span> | <span data-ttu-id="739a4-159">(R:0, G:0, B:0, A:0)</span><span class="sxs-lookup"><span data-stu-id="739a4-159">(R:0, G:0, B:0, A:0)</span></span> |
| <span data-ttu-id="739a4-160">Ambiente</span><span class="sxs-lookup"><span data-stu-id="739a4-160">Ambient</span></span>  | <span data-ttu-id="739a4-161">(R:0, G:0, B:0, A:0)</span><span class="sxs-lookup"><span data-stu-id="739a4-161">(R:0, G:0, B:0, A:0)</span></span> |
| <span data-ttu-id="739a4-162">Emissiva</span><span class="sxs-lookup"><span data-stu-id="739a4-162">Emissive</span></span> | <span data-ttu-id="739a4-163">(R:0, G:0, B:0, A:0)</span><span class="sxs-lookup"><span data-stu-id="739a4-163">(R:0, G:0, B:0, A:0)</span></span> |
| <span data-ttu-id="739a4-164">Energia</span><span class="sxs-lookup"><span data-stu-id="739a4-164">Power</span></span>    | <span data-ttu-id="739a4-165">(0,0)</span><span class="sxs-lookup"><span data-stu-id="739a4-165">(0.0)</span></span>                |



 

## <a name="retrieving-material-properties"></a><span data-ttu-id="739a4-166">Recuperando propriedades de material</span><span class="sxs-lookup"><span data-stu-id="739a4-166">Retrieving Material Properties</span></span>

<span data-ttu-id="739a4-167">Você recupera as propriedades de material que o dispositivo de renderização está usando no momento chamando o método [**IDirect3DDevice9:: GetMaterial**](/windows/desktop/api) para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="739a4-167">You retrieve the material properties that the rendering device is currently using by calling the [**IDirect3DDevice9::GetMaterial**](/windows/desktop/api) method for the device.</span></span> <span data-ttu-id="739a4-168">Ao contrário do método [**IDirect3DDevice9:: SetMaterial**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setmaterial) , o **IDirect3DDevice9:: GetMaterial** não requer preparação.</span><span class="sxs-lookup"><span data-stu-id="739a4-168">Unlike the [**IDirect3DDevice9::SetMaterial**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setmaterial) method, **IDirect3DDevice9::GetMaterial** doesn't require preparation.</span></span> <span data-ttu-id="739a4-169">O método **IDirect3DDevice9:: GetMaterial** aceita o endereço de uma estrutura [**D3DMATERIAL9**](d3dmaterial9.md) e preenche a estrutura fornecida com informações que descrevem as propriedades do material atual antes de retornar.</span><span class="sxs-lookup"><span data-stu-id="739a4-169">The **IDirect3DDevice9::GetMaterial** method accepts the address of a [**D3DMATERIAL9**](d3dmaterial9.md) structure, and fills the provided structure with information describing the current material properties before returning.</span></span>


```
// For this example, the pd3dDev variable is assumed to 
// be a valid pointer to an IDirect3DDevice9 interface.
HRESULT hr;
D3DMATERIAL9 mat;

hr = pd3dDev->GetMaterial(&mat);
if(FAILED(hr))
{
    // Code to handle the error goes here.
}
```



> [!Note]  
> <span data-ttu-id="739a4-170">Se o seu aplicativo não especificar as propriedades do material para renderização, o sistema usará um material padrão.</span><span class="sxs-lookup"><span data-stu-id="739a4-170">If your application does not specify material properties for rendering, the system uses a default material.</span></span> <span data-ttu-id="739a4-171">O material padrão reflete todas as difusos-branco, por exemplo, sem reflexão de ambiente ou especulação e nenhuma cor de emissiva.</span><span class="sxs-lookup"><span data-stu-id="739a4-171">The default material reflects all diffuse light - white, for example - with no ambient or specular reflection, and no emissive color.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="739a4-172">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="739a4-172">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="739a4-173">Luzes e materiais</span><span class="sxs-lookup"><span data-stu-id="739a4-173">Lights and Materials</span></span>](lights-and-materials.md)
</dt> </dl>

 

 
