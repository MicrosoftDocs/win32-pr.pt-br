---
title: Método isoptimized ID3DX11Effect (D3dx11effect. h)
description: Teste um efeito para ver se os metadados de reflexão foram removidos da memória.
ms.assetid: fb0a876b-7419-45b7-97fe-8352dd97d8c5
keywords:
- Método isoptimized Direct3D 11
- Método isoptimized Direct3D 11, interface ID3DX11Effect
- Interface ID3DX11Effect Direct3D 11, método isoptimized
topic_type:
- apiref
api_name:
- ID3DX11Effect.IsOptimized
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18be8901a58715e3bd8aaaa49ae40be07e7e9dc8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298757"
---
# <a name="id3dx11effectisoptimized-method"></a>Método ID3DX11Effect:: isoptimized

Teste um efeito para ver se os metadados de reflexão foram removidos da memória.

## <a name="syntax"></a>Sintaxe


```C++
BOOL IsOptimized();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Tipo: **[ **bool**](/windows/desktop/WinProg/windows-data-types)**

**True** se o efeito for otimizado; caso contrário, **false**.

## <a name="remarks"></a>Comentários

Um efeito usa o espaço de memória de duas maneiras diferentes: armazenar as informações exigidas pelo tempo de execução para executar um efeito e armazenar os metadados necessários para refletir informações de volta para um aplicativo usando a API. Você pode minimizar a quantidade de memória exigida por um efeito chamando [**ID3DX11Effect:: Optimize**](id3dx11effect-optimize.md) , que remove os metadados de reflexão da memória. É claro que os métodos de API para ler variáveis não funcionarão mais quando os dados de reflexão tiverem sido removidos.

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

 

