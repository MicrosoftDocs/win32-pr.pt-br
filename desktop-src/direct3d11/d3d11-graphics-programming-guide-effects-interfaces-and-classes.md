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
# <a name="interfaces-and-classes-in-effects"></a>Interfaces e classes em efeitos

Há várias maneiras de usar classes e interfaces nos efeitos 11. Para a interface e a sintaxe de classe, consulte [interfaces e classes](/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl-dynamic-linking-class).

As seções a seguir detalham como especificar instâncias de classe para um sombreador que usa interfaces. Usaremos a seguinte interface e classes nos exemplos:


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



Observe que as instâncias de interface podem ser inicializadas para instâncias de classe. Também há suporte para matrizes de instâncias de classe e de interface e elas podem ser inicializadas como no exemplo a seguir:


```
CRed pRedArray[2];
IColor pIColor3 = pRedArray[1];
IColor pIColorArray[2] = {pRed, pGreen};
IColor pIColorArray2[2] = pRedArray;
```



## <a name="uniform-interface-parameters"></a>Parâmetros de interface uniforme

Assim como outros tipos de dados uniformes, os parâmetros de interface uniformes devem ser especificados na chamada CompileShader. Os parâmetros de interface podem ser atribuídos a instâncias de interface global ou a instâncias de classe global. Quando atribuída a uma instância de interface global, o sombreador terá uma dependência na instância de interface, o que significa que ela deve ser definida como uma instância de classe. Quando atribuídas a instâncias de classe global, o compilador especializa o sombreador (como com outros tipos de dados uniformes) para usar essa classe. Isso é importante para dois cenários:

1.  Os sombreadores com um \_ destino 4 x podem usar parâmetros de interface se esses parâmetros forem uniformes e atribuídos a instâncias de classe global (portanto, nenhuma vinculação dinâmica é usada).
2.  Os usuários podem optar por ter muitos sombreadores especializados e compilados sem vínculo dinâmico ou poucos sombreadores compilados com vínculo dinâmico.


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



Se pIColor2 permanecer inalterado por meio da API, as duas passagens anteriores serão funcionalmente equivalentes, mas a primeira usará um \_ \_ sombreador estático PS 4 0 enquanto o segundo usa \_ um \_ sombreador PS 5 0 com vinculação dinâmica. Se pIColor2 for alterado por meio da API de efeitos (consulte Definindo as instâncias de classe abaixo), o comportamento do sombreador de pixel na segunda passagem poderá ser alterado.

## <a name="non-uniform-interface-parameters"></a>Parâmetros de interface não uniforme

Os parâmetros de interface não uniformes criam dependências de interface para os sombreadores. Ao aplicar um sombreador com parâmetros de interface, esses parâmetros devem ser atribuídos com a chamada BindInterfaces. Instâncias de interface global e instâncias de classe global podem ser especificadas na chamada BindInterfaces.


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



Se pIColor2 permanecer inalterado por meio da API, as duas passagens anteriores serão funcionalmente equivalentes e ambos usarão vínculo dinâmico. Se pIColor2 for alterado por meio da API de efeitos (consulte Definindo as instâncias de classe abaixo), o comportamento do sombreador de pixel na segunda passagem poderá ser alterado.

## <a name="setting-class-instances"></a>Definindo instâncias de classe

Ao definir um sombreador com ligação de sombreador dinâmico para o dispositivo Direct3D 11, as instâncias de classe também devem ser especificadas. É um erro definir esse sombreador com uma instância de classe **nula** . Portanto, todas as instâncias de interface que um sombreador referencia deve ter uma instância de classe associada.

O exemplo a seguir mostra como obter uma variável de instância de classe de um efeito e defini-la como uma variável de interface:


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



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Efeitos (Direct3D 11)](d3d11-graphics-programming-guide-effects.md)
</dt> </dl>

 

 