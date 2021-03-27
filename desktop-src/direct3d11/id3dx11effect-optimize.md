---
title: Método ID3DX11Effect Optimize (D3dx11effect. h)
description: Minimize a quantidade de memória necessária para um efeito.
ms.assetid: fa1d0769-6746-44f6-9979-31a534646884
keywords:
- Otimizar o método Direct3D 11
- Otimizar método Direct3D 11, interface ID3DX11Effect
- Interface ID3DX11Effect Direct3D 11, método Optimize
topic_type:
- apiref
api_name:
- ID3DX11Effect.Optimize
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33fd6d200f6b22af46e648040e8299f40ec9ebae
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104989367"
---
# <a name="id3dx11effectoptimize-method"></a>Método ID3DX11Effect:: Optimize

Minimize a quantidade de memória necessária para um efeito.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Optimize();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Retorna um dos seguintes [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Comentários

Um efeito usa o espaço de memória de duas maneiras diferentes: armazenar as informações exigidas pelo tempo de execução para executar um efeito e armazenar os metadados necessários para refletir informações de volta para um aplicativo usando a API. Você pode minimizar a quantidade de memória exigida por um efeito chamando **ID3DX11Effect:: Optimize** , que remove os metadados de reflexão da memória. Os métodos de API para ler variáveis não funcionarão mais quando os dados de reflexão tiverem sido removidos.

Os métodos a seguir falharão depois que optimize for chamado em um efeito.

-   [**ID3DX11Effect::GetConstantBufferByIndex**](id3dx11effect-getconstantbufferbyindex.md)
-   [**ID3DX11Effect::GetConstantBufferByName**](id3dx11effect-getconstantbufferbyname.md)
-   [**ID3DX11Effect:: GetDesc**](id3dx11effect-getdesc.md)
-   [**ID3DX11Effect:: GetDevice**](id3dx11effect-getdevice.md)
-   [**ID3DX11Effect::GetTechniqueByIndex**](id3dx11effect-gettechniquebyindex.md)
-   [**ID3DX11Effect::GetTechniqueByName**](id3dx11effect-gettechniquebyname.md)
-   [**ID3DX11Effect::GetVariableByIndex**](id3dx11effect-getvariablebyindex.md)
-   [**ID3DX11Effect::GetVariableByName**](id3dx11effect-getvariablebyname.md)
-   [**ID3DX11Effect::GetVariableBySemantic**](id3dx11effect-getvariablebysemantic.md)

> [!Note]  
> As referências recuperadas com esses métodos antes de chamar **ID3DX11Effect:: Optimize** ainda são válidas após **ID3DX11Effect:: Optimize** ser chamado. Isso permite que o aplicativo obtenha todas as variáveis, técnicas e passes que usará, chame optimize e, em seguida, use o efeito.

 

> [!Note]  
> O SDK do DirectX não fornece nenhum binário compilado para efeitos. Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos. Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Biblioteca<br/> | <dl> <dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DX11Effect](id3dx11effect.md)
</dt> </dl>

 

 





