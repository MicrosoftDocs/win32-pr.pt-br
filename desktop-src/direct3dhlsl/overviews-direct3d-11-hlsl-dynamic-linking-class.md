---
title: Interfaces e classes
description: O vínculo de sombreador dinâmico usa interfaces e classes HLSL (linguagem de sombreamento de alto nível) que são sintaticamente semelhantes às suas contrapartes do C++.
ms.assetid: 124a358d-30ab-4efe-88ed-1ff277d17b25
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 71410caf7d80cb9dbcd0165c753d75cc8f5cbe00
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366449"
---
# <a name="interfaces-and-classes"></a><span data-ttu-id="c0ef1-103">Interfaces e classes</span><span class="sxs-lookup"><span data-stu-id="c0ef1-103">Interfaces and classes</span></span>

<span data-ttu-id="c0ef1-104">O vínculo de sombreador dinâmico usa interfaces e classes HLSL (linguagem de sombreamento de alto nível) que são sintaticamente semelhantes às suas contrapartes do C++.</span><span class="sxs-lookup"><span data-stu-id="c0ef1-104">Dynamic shader linkage makes use of high-level shader language (HLSL) interfaces and classes that are syntactically similar to their C++ counterparts.</span></span> <span data-ttu-id="c0ef1-105">Isso permite que os sombreadores façam referência a instâncias de interface abstratas em tempo de compilação e deixem a resolução dessas instâncias para classes concretas para o aplicativo em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="c0ef1-105">This allows shaders to reference abstract interface instances at compile time and leave resolution of those instances to concrete classes for the application at runtime.</span></span>

<span data-ttu-id="c0ef1-106">As seções a seguir detalham como configurar um sombreador para usar interfaces e classes e como inicializar instâncias de interface no código do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c0ef1-106">The following sections detail how to setup a shader to use interfaces and classes and how to initialize interface instances in application code.</span></span>

-   [<span data-ttu-id="c0ef1-107">Declarando interfaces</span><span class="sxs-lookup"><span data-stu-id="c0ef1-107">Declaring Interfaces</span></span>](#declaring-interfaces)
-   [<span data-ttu-id="c0ef1-108">Classes declaradoras</span><span class="sxs-lookup"><span data-stu-id="c0ef1-108">Declaring Classes</span></span>](#declaring-classes)
-   [<span data-ttu-id="c0ef1-109">Declarações de instância de interface em um sombreador</span><span class="sxs-lookup"><span data-stu-id="c0ef1-109">Interface Instance Declarations in a Shader</span></span>](#interface-instance-declarations-in-a-shader)
-   [<span data-ttu-id="c0ef1-110">Declarações de instância de classe em um sombreador</span><span class="sxs-lookup"><span data-stu-id="c0ef1-110">Class Instance Declarations in a Shader</span></span>](#class-instance-declarations-in-a-shader)
-   [<span data-ttu-id="c0ef1-111">Inicializando instâncias de interface em um aplicativo</span><span class="sxs-lookup"><span data-stu-id="c0ef1-111">Initializing Interface Instances in an Application</span></span>](#initializing-interface-instances-in-an-application)
-   [<span data-ttu-id="c0ef1-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c0ef1-112">Related topics</span></span>](#related-topics)

## <a name="declaring-interfaces"></a><span data-ttu-id="c0ef1-113">Declarando interfaces</span><span class="sxs-lookup"><span data-stu-id="c0ef1-113">Declaring interfaces</span></span>

<span data-ttu-id="c0ef1-114">Uma interface funciona de maneira semelhante a uma classe base abstrata em C++.</span><span class="sxs-lookup"><span data-stu-id="c0ef1-114">An interface functions in a similar manner to an abstract base class in C++.</span></span> <span data-ttu-id="c0ef1-115">Uma interface é declarada em um sombreador usando a palavra-chave interface e contém apenas declarações de método.</span><span class="sxs-lookup"><span data-stu-id="c0ef1-115">An interface is declared in a shader using the interface keyword and only contains method declarations.</span></span> <span data-ttu-id="c0ef1-116">Os métodos declarados em uma interface serão todos métodos virtuais em todas as classes derivadas da interface.</span><span class="sxs-lookup"><span data-stu-id="c0ef1-116">The methods declared in an interface will all be virtual methods in any classes derived from the interface.</span></span> <span data-ttu-id="c0ef1-117">Classes derivadas devem implementar todos os métodos declarados em uma interface.</span><span class="sxs-lookup"><span data-stu-id="c0ef1-117">Derived classes must implement all methods declared in an interface.</span></span> <span data-ttu-id="c0ef1-118">Observe que as interfaces são a única maneira de declarar métodos virtuais, não há nenhuma palavra-chave virtual como em C++ e as classes Connot declaram métodos virtuais.</span><span class="sxs-lookup"><span data-stu-id="c0ef1-118">Note that interfaces are the only way to declare virtual methods, there is no virtual keyword as in C++, and classes connot declare virtual methods.</span></span>

<span data-ttu-id="c0ef1-119">O código de sombreador de exemplo a seguir declara duas interfaces.</span><span class="sxs-lookup"><span data-stu-id="c0ef1-119">The following example shader code declares two interfaces.</span></span>


```
interface iBaseLight
{
   float3 IlluminateAmbient(float3 vNormal);
   float3 IlluminateDiffuse(float3 vNormal);
   float3 IlluminateSpecular(float3 vNormal, int specularPower );
};       

interface iBaseMaterial
{
   float3 GetAmbientColor(float2 vTexcoord);
   
   float3 GetDiffuseColor(float2 vTexcoord);

   int GetSpecularPower();

};
      
```



## <a name="declaring-classes"></a><span data-ttu-id="c0ef1-120">Declarando Classes</span><span class="sxs-lookup"><span data-stu-id="c0ef1-120">Declaring Classes</span></span>

<span data-ttu-id="c0ef1-121">Uma classe se comporta de forma semelhante às classes em C++.</span><span class="sxs-lookup"><span data-stu-id="c0ef1-121">A class behaves in a similar manner to classes in C++.</span></span> <span data-ttu-id="c0ef1-122">Uma classe é declarada com a palavra-chave class e pode conter variáveis e métodos de membro.</span><span class="sxs-lookup"><span data-stu-id="c0ef1-122">A class is declared with the class keyword and can contain member variables and methods.</span></span> <span data-ttu-id="c0ef1-123">Uma classe pode herdar de zero ou uma classe e zero ou mais interfaces.</span><span class="sxs-lookup"><span data-stu-id="c0ef1-123">A class can inherit from zero or one class and zero or more interfaces.</span></span> <span data-ttu-id="c0ef1-124">As classes devem implementar ou herdar implementações para todas as interfaces em sua cadeia de herança ou a classe não pode ser instanciada.</span><span class="sxs-lookup"><span data-stu-id="c0ef1-124">Classes must implement or inherit implementations for all interfaces in its inheritance chain or the class cannot be instantiated.</span></span>

<span data-ttu-id="c0ef1-125">O código de sombreador de exemplo a seguir ilustra a derivação de uma classe de uma interface e de outra classe.</span><span class="sxs-lookup"><span data-stu-id="c0ef1-125">The following example shader code illustrates deriving a class from an interface and from another class.</span></span>


```
class cAmbientLight : iBaseLight
{
   float3            m_vLightColor;     
   bool     m_bEnable;
   float3 IlluminateAmbient(float3 vNormal);
   float3 IlluminateDiffuse(float3 vNormal);
   float3 IlluminateSpecular(float3 vNormal, int specularPower );
};

class cHemiAmbientLight : cAmbientLight
{
   float4   m_vGroundColor;
   float4   m_vDirUp;
   float3 IlluminateAmbient(float3 vNormal);
};        
      
```



## <a name="interface-instance-declarations-in-a-shader"></a><span data-ttu-id="c0ef1-126">Declarações de instância de interface em um sombreador</span><span class="sxs-lookup"><span data-stu-id="c0ef1-126">Interface Instance Declarations in a Shader</span></span>

<span data-ttu-id="c0ef1-127">Uma instância de interface age como um espaço reservado para instâncias de classe que fornecem uma implementação dos métodos da interface.</span><span class="sxs-lookup"><span data-stu-id="c0ef1-127">An interface instance acts as a place holder for class instances that provide an implementation of the interface's methods.</span></span> <span data-ttu-id="c0ef1-128">O uso de uma instância de uma interface permite que o código do sombreador chame um método sem saber qual implementação desse método será invocada.</span><span class="sxs-lookup"><span data-stu-id="c0ef1-128">Using an instance of an interface allows shader code to call a method without knowing which implementation of that method will be invoked.</span></span> <span data-ttu-id="c0ef1-129">O código do sombreador declara uma ou mais instâncias para cada interface que ela define.</span><span class="sxs-lookup"><span data-stu-id="c0ef1-129">Shader code declares one or more instances for each interface it defines.</span></span> <span data-ttu-id="c0ef1-130">Essas instâncias são usadas no código de sombreador de maneira semelhante aos ponteiros de classe base do C++.</span><span class="sxs-lookup"><span data-stu-id="c0ef1-130">These instances are used in shader code in a similar manner to C++ base class pointers.</span></span>

<span data-ttu-id="c0ef1-131">O código de sombreador de exemplo a seguir ilustra a declaração de várias instâncias de interface e o uso deles no código do sombreador.</span><span class="sxs-lookup"><span data-stu-id="c0ef1-131">The following example shader code illustrates declaring several interface instances and using them in shader code.</span></span>


```
// Declare interface instances
iBaseLight     g_abstractAmbientLighting;
iBaseLight     g_abstractDirectLighting;
iBaseMaterial  g_abstractMaterial;

struct PS_INPUT
{
    float4 vPosition : SV_POSITION;
    float3 vNormal   : NORMAL;
    float2 vTexcoord : TEXCOORD0;
};

float4 PSMain( PS_INPUT Input ) : SV_TARGET
{ 
    float3 Ambient = (float3)0.0f;       
    Ambient = g_abstractMaterial.GetAmbientColor( Input.vTexcoord ) *         
        g_abstractAmbientLighting.IlluminateAmbient( Input.vNormal );

    float3 Diffuse = (float3)0.0f;  
    Diffuse += g_abstractMaterial.GetDiffuseColor( Input.vTexcoord ) * 
        g_abstractDirectLighting.IlluminateDiffuse( Input.vNormal );

    float3 Specular = (float3)0.0f;   
    Specular += g_abstractDirectLighting.IlluminateSpecular( Input.vNormal, 
        g_abstractMaterial.GetSpecularPower() );
     
    float3 Lighting = saturate( Ambient + Diffuse + Specular );
     
    return float4(Lighting,1.0f); 
}
```



## <a name="class-instance-declarations-in-a-shader"></a><span data-ttu-id="c0ef1-132">Declarações de instância de classe em um sombreador</span><span class="sxs-lookup"><span data-stu-id="c0ef1-132">Class Instance Declarations in a Shader</span></span>

<span data-ttu-id="c0ef1-133">Cada classe que será usada no lugar de uma instância de interface deve ser declarada como uma variável em um buffer de constante ou criada pelo aplicativo em tempo de execução usando o método [**ID3D11ClassLinkage:: CreateClassInstance**](/windows/desktop/api/d3d11/nf-d3d11-id3d11classlinkage-createclassinstance) .</span><span class="sxs-lookup"><span data-stu-id="c0ef1-133">Each class that will be used in place of an interface instance must either be declared as a variable in a constant buffer or created by the application at runtime using the [**ID3D11ClassLinkage::CreateClassInstance**](/windows/desktop/api/d3d11/nf-d3d11-id3d11classlinkage-createclassinstance) method.</span></span> <span data-ttu-id="c0ef1-134">As instâncias de interface serão apontadas em instâncias de classe no código do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c0ef1-134">Interface instances will be pointed at class instances in the application code.</span></span> <span data-ttu-id="c0ef1-135">As instâncias de classe podem ser referenciadas no código de sombreador como qualquer outra variável, mas uma classe derivada de uma interface normalmente será usada apenas com uma instância de interface e não será referenciada pelo código de sombreador diretamente.</span><span class="sxs-lookup"><span data-stu-id="c0ef1-135">Class instances can be referenced in shader code like any other variable, but a class that is derived from an interface will typically only be used with an interface instance and will not be referenced by shader code directly.</span></span>

<span data-ttu-id="c0ef1-136">O código de sombreador de exemplo a seguir ilustra a declaração de várias instâncias de classe.</span><span class="sxs-lookup"><span data-stu-id="c0ef1-136">The following example shader code illustrates declaring several class instances.</span></span>


```
cbuffer cbPerFrame : register( b0 )
{
   cAmbientLight     g_ambientLight;
   cHemiAmbientLight g_hemiAmbientLight;
   cDirectionalLight g_directionalLight;
   cEnvironmentLight g_environmentLight;
   float4            g_vEyeDir;   
};        
      
```



## <a name="initializing-interface-instances-in-an-application"></a><span data-ttu-id="c0ef1-137">Inicializando instâncias de interface em um aplicativo</span><span class="sxs-lookup"><span data-stu-id="c0ef1-137">Initializing Interface Instances in an Application</span></span>

<span data-ttu-id="c0ef1-138">As instâncias de interface são inicializadas no código do aplicativo passando uma matriz de vínculo dinâmico que contém atribuições de interface para um dos métodos [**ID3D11DeviceContext**](/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext) setshadr.</span><span class="sxs-lookup"><span data-stu-id="c0ef1-138">Interface instances are initialized in application code by passing a dynamic linkage array containing interface assignments to one of the [**ID3D11DeviceContext**](/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext) SetShader methods.</span></span>

<span data-ttu-id="c0ef1-139">Para criar uma matriz de vinculação dinâmica, use as etapas a seguir</span><span class="sxs-lookup"><span data-stu-id="c0ef1-139">To create a dynamic linkage array use the following steps</span></span>

1.  <span data-ttu-id="c0ef1-140">Crie um objeto de vinculação de classe usando [**CreateClassLinkage**](/windows/win32/api/d3d11/nf-d3d11-id3d11device-createclasslinkage).</span><span class="sxs-lookup"><span data-stu-id="c0ef1-140">Create a class linkage object using [**CreateClassLinkage**](/windows/win32/api/d3d11/nf-d3d11-id3d11device-createclasslinkage).</span></span>
    ```
    ID3D11ClassLinkage* g_pPSClassLinkage = NULL;            
    pd3dDevice->CreateClassLinkage( &g_pPSClassLinkage );
              
    ```

    

2.  <span data-ttu-id="c0ef1-141">Crie o sombreador que usará a vinculação de classe dinâmica, passando o objeto de vinculação de classe como um parâmetro para a função CREATE do sombreador.</span><span class="sxs-lookup"><span data-stu-id="c0ef1-141">Create the shader that will be using dynamic class linking, passing the class linkage object as a parameter to the shader's create function.</span></span>
    ```
    pd3dDevice->CreatePixelShader( pPixelShaderBuffer->GetBufferPointer(),
        pPixelShaderBuffer->GetBufferSize(), g_pPSClassLinkage, &g_pPixelShader ) );            
              
    ```

    

3.  <span data-ttu-id="c0ef1-142">Crie um objeto [**ID3D11ShaderReflection**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflection) usando a função [**D3DReflect**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dreflect) .</span><span class="sxs-lookup"><span data-stu-id="c0ef1-142">Create a [**ID3D11ShaderReflection**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflection) object using the [**D3DReflect**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dreflect) function.</span></span>
    ```
    ID3D11ShaderReflection* pReflector = NULL; 
    D3DReflect( pPixelShaderBuffer->GetBufferPointer(),                  
        pPixelShaderBuffer->GetBufferSize(), 
        IID_ID3D11ShaderReflection, (void**) &pReflector) );            
              
    ```

    

4.  <span data-ttu-id="c0ef1-143">Use o objeto de reflexo do sombreador para obter o número de instâncias de interface no sombreador usando o método [**ID3D11ShaderReflection:: GetNumInterfaceSlots**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflection-getnuminterfaceslots) .</span><span class="sxs-lookup"><span data-stu-id="c0ef1-143">Use the shader reflection object to get the number of interface instances in the shader using the [**ID3D11ShaderReflection::GetNumInterfaceSlots**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflection-getnuminterfaceslots) method.</span></span>
    ```
    g_iNumPSInterfaces = pReflector->GetNumInterfaceSlots();             
              
    ```

    

5.  <span data-ttu-id="c0ef1-144">Crie uma matriz grande o suficiente para manter o número de instâncias de interface no sombreador.</span><span class="sxs-lookup"><span data-stu-id="c0ef1-144">Create an array large enough to hold the number of interface instances in the shader.</span></span>
    ```
    ID3D11ClassInstance** g_dynamicLinkageArray = NULL;            
    g_dynamicLinkageArray = 
        (ID3D11ClassInstance**) malloc( sizeof(ID3D11ClassInstance*) * g_iNumPSInterfaces );            
              
    ```

    

6.  <span data-ttu-id="c0ef1-145">Determine o índice na matriz que corresponde a cada instância de interface usando [**ID3D11ShaderReflection:: GetVariableByName**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflection-getvariablebyname) e [**ID3D11ShaderReflectionVariable:: GetInterfaceSlot**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflectionvariable-getinterfaceslot).</span><span class="sxs-lookup"><span data-stu-id="c0ef1-145">Determine the index in the array that corresponds to each interface instance using [**ID3D11ShaderReflection::GetVariableByName**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflection-getvariablebyname) and [**ID3D11ShaderReflectionVariable::GetInterfaceSlot**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflectionvariable-getinterfaceslot).</span></span>
    ```
    ID3D11ShaderReflectionVariable* pAmbientLightingVar = 
        pReflector->GetVariableByName("g_abstractAmbientLighting");
        g_iAmbientLightingOffset = pAmbientLightingVar->GetInterfaceSlot(0);            
              
    ```

    

7.  <span data-ttu-id="c0ef1-146">Obtenha uma instância de classe para cada objeto de classe derivado de uma interface no sombreador usando [**ID3D11ClassLinkage:: GetClassInstance**](/windows/desktop/api/d3d11/nf-d3d11-id3d11classlinkage-getclassinstance).</span><span class="sxs-lookup"><span data-stu-id="c0ef1-146">Get a class instance for each class object derived from an interface in the shader using [**ID3D11ClassLinkage::GetClassInstance**](/windows/desktop/api/d3d11/nf-d3d11-id3d11classlinkage-getclassinstance).</span></span>
    ```
    g_pPSClassLinkage->GetClassInstance( "g_hemiAmbientLight", 0, 
        &g_pHemiAmbientLightClass );            
              
    ```

    

8.  <span data-ttu-id="c0ef1-147">Defina instâncias de interface para instâncias de classe definindo a entrada correspondente na matriz de vinculação dinâmica.</span><span class="sxs-lookup"><span data-stu-id="c0ef1-147">Set interface instances to class instances by setting the corresponding entry in the dynamic linkage array.</span></span>
    ```
    g_dynamicLinkageArray[g_iAmbientLightingOffset] = g_pHemiAmbientLightClass;            
              
    ```

    

9.  <span data-ttu-id="c0ef1-148">Passe a matriz de vinculação dinâmica como um parâmetro para uma chamada setshadr.</span><span class="sxs-lookup"><span data-stu-id="c0ef1-148">Pass the dynamic linkage array as a parameter to a SetShader call.</span></span>
    ```
    pd3dImmediateContext->PSSetShader( g_pPixelShader, g_dynamicLinkageArray, g_iNumPSInterfaces );            
              
    ```

    

## <a name="related-topics"></a><span data-ttu-id="c0ef1-149">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c0ef1-149">Related topics</span></span>

[<span data-ttu-id="c0ef1-150">Vinculação dinâmica</span><span class="sxs-lookup"><span data-stu-id="c0ef1-150">Dynamic Linking</span></span>](overviews-direct3d-11-hlsl-dynamic-linking.md)