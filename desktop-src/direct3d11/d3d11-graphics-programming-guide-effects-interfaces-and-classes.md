---
title: Interfaces e classes em efeitos
description: Há várias maneiras de usar classes e interfaces nos efeitos 11.
ms.assetid: 526d477b-fc1f-4bd0-a620-ce9b78147f68
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b067b8e03b2d43ea44ccab6164424cbc84c7237
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366218"
---
# <a name="interfaces-and-classes-in-effects"></a><span data-ttu-id="05e6a-103">Interfaces e classes em efeitos</span><span class="sxs-lookup"><span data-stu-id="05e6a-103">Interfaces and Classes in Effects</span></span>

<span data-ttu-id="05e6a-104">Há várias maneiras de usar classes e interfaces nos efeitos 11.</span><span class="sxs-lookup"><span data-stu-id="05e6a-104">There are many ways to use classes and interfaces in Effects 11.</span></span> <span data-ttu-id="05e6a-105">Para a interface e a sintaxe de classe, consulte [interfaces e classes](/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl-dynamic-linking-class).</span><span class="sxs-lookup"><span data-stu-id="05e6a-105">For interface and class syntax, see [Interfaces and Classes](/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl-dynamic-linking-class).</span></span>

<span data-ttu-id="05e6a-106">As seções a seguir detalham como especificar instâncias de classe para um sombreador que usa interfaces.</span><span class="sxs-lookup"><span data-stu-id="05e6a-106">The following sections detail how to specify class instances to a shader which uses interfaces.</span></span> <span data-ttu-id="05e6a-107">Usaremos a seguinte interface e classes nos exemplos:</span><span class="sxs-lookup"><span data-stu-id="05e6a-107">We will use the following interface and classes in the examples:</span></span>


```
interface IColor
{
  float4 GetColor();
};

class CRed : IColor
{
  float4 GetColor() { return float4(1,0,0,1); }
};
class CGreen : IColor
{
  float4 GetColor() { return float4(0,1,0,1); }
};

CRed pRed;
CGreen pGreen;
IColor pIColor;
IColor pIColor2 = pRed;
```



<span data-ttu-id="05e6a-108">Observe que as instâncias de interface podem ser inicializadas para instâncias de classe.</span><span class="sxs-lookup"><span data-stu-id="05e6a-108">Note that interface instances can be initialized to class instances.</span></span> <span data-ttu-id="05e6a-109">Também há suporte para matrizes de instâncias de classe e de interface e elas podem ser inicializadas como no exemplo a seguir:</span><span class="sxs-lookup"><span data-stu-id="05e6a-109">Arrays of class and interface instances are also supported and they can be initialized as in the following example:</span></span>


```
CRed pRedArray[2];
IColor pIColor3 = pRedArray[1];
IColor pIColorArray[2] = {pRed, pGreen};
IColor pIColorArray2[2] = pRedArray;
```



## <a name="uniform-interface-parameters"></a><span data-ttu-id="05e6a-110">Parâmetros de interface uniforme</span><span class="sxs-lookup"><span data-stu-id="05e6a-110">Uniform Interface Parameters</span></span>

<span data-ttu-id="05e6a-111">Assim como outros tipos de dados uniformes, os parâmetros de interface uniformes devem ser especificados na chamada CompileShader.</span><span class="sxs-lookup"><span data-stu-id="05e6a-111">Just like other uniform data types, uniform interface parameters must be specified in the CompileShader call.</span></span> <span data-ttu-id="05e6a-112">Os parâmetros de interface podem ser atribuídos a instâncias de interface global ou a instâncias de classe global.</span><span class="sxs-lookup"><span data-stu-id="05e6a-112">Interface parameters can be assigned to global interface instances or global class instances.</span></span> <span data-ttu-id="05e6a-113">Quando atribuída a uma instância de interface global, o sombreador terá uma dependência na instância de interface, o que significa que ela deve ser definida como uma instância de classe.</span><span class="sxs-lookup"><span data-stu-id="05e6a-113">When assigned to a global interface instance, the shader will have a dependency on the interface instance, which means that it must be set to a class instance.</span></span> <span data-ttu-id="05e6a-114">Quando atribuídas a instâncias de classe global, o compilador especializa o sombreador (como com outros tipos de dados uniformes) para usar essa classe.</span><span class="sxs-lookup"><span data-stu-id="05e6a-114">When assigned to global class instances, the compiler specializes the shader (as with other uniform data types) to use that class.</span></span> <span data-ttu-id="05e6a-115">Isso é importante para dois cenários:</span><span class="sxs-lookup"><span data-stu-id="05e6a-115">This is important for two scenarios:</span></span>

1.  <span data-ttu-id="05e6a-116">Os sombreadores com um \_ destino 4 x podem usar parâmetros de interface se esses parâmetros forem uniformes e atribuídos a instâncias de classe global (portanto, nenhuma vinculação dinâmica é usada).</span><span class="sxs-lookup"><span data-stu-id="05e6a-116">Shaders with a 4\_x target can use interface parameters if these parameters are uniform and assigned to global class instances (so no dynamic linkage is used).</span></span>
2.  <span data-ttu-id="05e6a-117">Os usuários podem optar por ter muitos sombreadores especializados e compilados sem vínculo dinâmico ou poucos sombreadores compilados com vínculo dinâmico.</span><span class="sxs-lookup"><span data-stu-id="05e6a-117">Users can decide to have many compiled, specialized shaders with no dynamic linkage or few compiled shaders with dynamic linkage.</span></span>


```
float4 PSUniform( uniform IColor color ) : SV_Target
{
  return color;
}

technique11
{
  pass
  {
    SetPixelShader( CompileShader( ps_4_0, PSUniform(pRed) ) );
  }
  pass
  {
    SetPixelShader( CompileShader( ps_5_0, PSUniform(pIColor2) ) );
  }
}
```



<span data-ttu-id="05e6a-118">Se pIColor2 permanecer inalterado por meio da API, as duas passagens anteriores serão funcionalmente equivalentes, mas a primeira usará um \_ \_ sombreador estático PS 4 0 enquanto o segundo usa \_ um \_ sombreador PS 5 0 com vinculação dinâmica.</span><span class="sxs-lookup"><span data-stu-id="05e6a-118">If pIColor2 remains unchanged through the API, then the previous two passes are functionally equivalent, but the first uses a ps\_4\_0 static shader while the second uses a ps\_5\_0 shader with dynamic linkage.</span></span> <span data-ttu-id="05e6a-119">Se pIColor2 for alterado por meio da API de efeitos (consulte Definindo as instâncias de classe abaixo), o comportamento do sombreador de pixel na segunda passagem poderá ser alterado.</span><span class="sxs-lookup"><span data-stu-id="05e6a-119">If pIColor2 is changed through the effects API (see Setting Class Instances below), then the behavior of the pixel shader in the second pass may change.</span></span>

## <a name="non-uniform-interface-parameters"></a><span data-ttu-id="05e6a-120">Parâmetros de interface não uniforme</span><span class="sxs-lookup"><span data-stu-id="05e6a-120">Non-Uniform Interface Parameters</span></span>

<span data-ttu-id="05e6a-121">Os parâmetros de interface não uniformes criam dependências de interface para os sombreadores.</span><span class="sxs-lookup"><span data-stu-id="05e6a-121">Non-uniform interface parameters create interface dependencies for the shaders.</span></span> <span data-ttu-id="05e6a-122">Ao aplicar um sombreador com parâmetros de interface, esses parâmetros devem ser atribuídos com a chamada BindInterfaces.</span><span class="sxs-lookup"><span data-stu-id="05e6a-122">When applying a shader with interface parameters, these parameters must be assigned in with the BindInterfaces call.</span></span> <span data-ttu-id="05e6a-123">Instâncias de interface global e instâncias de classe global podem ser especificadas na chamada BindInterfaces.</span><span class="sxs-lookup"><span data-stu-id="05e6a-123">Global interface instances and global class instances can be specified in the BindInterfaces call.</span></span>


```
float4 PSAbstract( IColor color ) : SV_Target
{
  return color;
}

PixelShader pPSAbstract = CompileShader( ps_5_0, PSAbstract(pRed) );

technique11
{
  pass
  {
    SetPixelShader( BindInterfaces( pPSAbstract, pRed ) );
  }
  pass
  {
    SetPixelShader( BindInterfaces( pPSAbstract, pIColor2 ) );
  }
}
```



<span data-ttu-id="05e6a-124">Se pIColor2 permanecer inalterado por meio da API, as duas passagens anteriores serão funcionalmente equivalentes e ambos usarão vínculo dinâmico.</span><span class="sxs-lookup"><span data-stu-id="05e6a-124">If pIColor2 remains unchanged through the API, then the previous two passes are functionally equivalent and both use dynamic linkage.</span></span> <span data-ttu-id="05e6a-125">Se pIColor2 for alterado por meio da API de efeitos (consulte Definindo as instâncias de classe abaixo), o comportamento do sombreador de pixel na segunda passagem poderá ser alterado.</span><span class="sxs-lookup"><span data-stu-id="05e6a-125">If pIColor2 is changed through the effects API (see Setting Class Instances below), then the behavior of the pixel shader in the second pass may change.</span></span>

## <a name="setting-class-instances"></a><span data-ttu-id="05e6a-126">Definindo instâncias de classe</span><span class="sxs-lookup"><span data-stu-id="05e6a-126">Setting Class Instances</span></span>

<span data-ttu-id="05e6a-127">Ao definir um sombreador com ligação de sombreador dinâmico para o dispositivo Direct3D 11, as instâncias de classe também devem ser especificadas.</span><span class="sxs-lookup"><span data-stu-id="05e6a-127">When setting a shader with dynamic shader linkage to the Direct3D 11 device, class instances must also be specified.</span></span> <span data-ttu-id="05e6a-128">É um erro definir esse sombreador com uma instância de classe **nula** .</span><span class="sxs-lookup"><span data-stu-id="05e6a-128">It is an error to set such a shader with a **NULL** class instance.</span></span> <span data-ttu-id="05e6a-129">Portanto, todas as instâncias de interface que um sombreador referencia deve ter uma instância de classe associada.</span><span class="sxs-lookup"><span data-stu-id="05e6a-129">Therefore, all interface instances which a shader references must have an associated class instance.</span></span>

<span data-ttu-id="05e6a-130">O exemplo a seguir mostra como obter uma variável de instância de classe de um efeito e defini-la como uma variável de interface:</span><span class="sxs-lookup"><span data-stu-id="05e6a-130">The following example shows how to get a class instance variable from an effect and set it to an interface variable:</span></span>


```
ID3DX11EffectPass* pPass = pEffect->GetTechniqueByIndex(0)->GetPassByIndex(1);

ID3DX11EffectInterfaceVariable* pIface = pEffect->GetVariableByName( "pIColor2" )->AsInterface();
ID3DX11EffectClassInstanceVariable* pCI = pEffect->GetVariableByName( "pGreen" )->AsClassInstance();
pIface->SetClassInstance( pCI );
pPass->Apply( 0, pDeviceContext );

// Apply the same pass with a different class instance
pCI = pEffect->GetVariableByName( "pRedArray" )->GetElement(1)->AsClassInstance();
pIface->SetClassInstance( pCI );
pPass->Apply( 0, pDeviceContext );
```



## <a name="related-topics"></a><span data-ttu-id="05e6a-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="05e6a-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="05e6a-132">Efeitos (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="05e6a-132">Effects (Direct3D 11)</span></span>](d3d11-graphics-programming-guide-effects.md)
</dt> </dl>

 

 