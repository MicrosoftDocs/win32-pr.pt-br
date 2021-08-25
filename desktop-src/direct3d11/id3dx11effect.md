---
title: Interface ID3DX11Effect (D3dx11effect.h)
description: Uma interface ID3DX11Effect gerencia um conjunto de objetos de estado, recursos e sombreadores para implementar um efeito de renderização.
ms.assetid: 34429d51-6b45-4a62-bce1-50c4da02edac
keywords:
- ID3DX11 Interface de efeito Direct3D 11
- ID3DX11A interface de efeito Direct3D 11 , descrita
topic_type:
- apiref
api_name:
- ID3DX11Effect
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4270059d02aec10905ea8aed7754bfb3a34c6897
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479142"
---
# <a name="id3dx11effect-interface"></a>Interface ID3DX11Effect

Uma **interface ID3DX11Effect** gerencia um conjunto de objetos de estado, recursos e sombreadores para implementar um efeito de renderização.

## <a name="members"></a>Membros

A interface **ID3DX11Effect** herda da interface [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **ID3DX11Effect** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ID3DX11Effect** tem esses métodos.



| Método                                                                     | Descrição                                                                               |
|:---------------------------------------------------------------------------|:------------------------------------------------------------------------------------------|
| [**CloneEffect**](id3dx11effect-cloneeffect.md)                           | Cria uma cópia de uma interface de efeito.<br/>                                         |
| [**GetClassLinkage**](id3dx11effect-getclasslinkage.md)                   | Obtém uma interface de vinculação de classe.<br/>                                                |
| [**GetConstantBufferByIndex**](id3dx11effect-getconstantbufferbyindex.md) | Obter um buffer constante por índice.<br/>                                                |
| [**GetConstantBufferByName**](id3dx11effect-getconstantbufferbyname.md)   | Obter um buffer constante por nome.<br/>                                                 |
| [**GetDesc**](id3dx11effect-getdesc.md)                                   | Obter uma descrição de efeito.<br/>                                                     |
| [**GetDevice**](id3dx11effect-getdevice.md)                               | Obter o dispositivo que criou o efeito.<br/>                                        |
| [**GetGroupByIndex**](id3dx11effect-getgroupbyindex.md)                   | Obtém um grupo de efeitos por índice.<br/>                                                 |
| [**GetGroupByName**](id3dx11effect-getgroupbyname.md)                     | Obtém um grupo de efeitos por nome.<br/>                                                  |
| [**GetTechniqueByIndex**](id3dx11effect-gettechniquebyindex.md)           | Obter uma técnica por índice.<br/>                                                      |
| [**GetTechniqueByName**](id3dx11effect-gettechniquebyname.md)             | Obter uma técnica por nome.<br/>                                                       |
| [**GetVariableByIndex**](id3dx11effect-getvariablebyindex.md)             | Obter uma variável por índice.<br/>                                                       |
| [**GetVariableByName**](id3dx11effect-getvariablebyname.md)               | Obter uma variável por nome.<br/>                                                        |
| [**GetVariableBySemantic**](id3dx11effect-getvariablebysemantic.md)       | Obter uma variável por semântica.<br/>                                                    |
| [**IsOptimized**](id3dx11effect-isoptimized.md)                           | Teste um efeito para ver se os metadados de reflexão foram removidos da memória.<br/> |
| [**IsValid**](id3dx11effect-isvalid.md)                                   | Teste um efeito para ver se ele contém sintaxe válida.<br/>                             |
| [**Otimizar**](id3dx11effect-optimize.md)                                 | Minimize a quantidade de memória necessária para um efeito.<br/>                          |



 

## <a name="remarks"></a>Comentários

Um efeito é criado chamando [**D3DX11CreateEffectFromMemory**](d3dx11createeffectfrommemory.md).

O sistema de efeito reúne as informações necessárias para renderização em um efeito que contém: objetos de estado para atribuir alterações de estado em grupos, recursos para fornecer dados de entrada e armazenar dados de saída e programas que controlam como a renderização é feita chamada sombreadores.

> [!Note]  
> O SDK do DirectX não fornece binários compilados para efeitos. Você deve usar a origem efeitos 11 para criar seu aplicativo do tipo efeitos. Para obter mais informações sobre como usar a origem dos Efeitos 11, consulte [Diferenças entre efeitos 10 e efeitos 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

> [!Note]
>
> Se você chamar [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) em um objeto **ID3DX11Effect** para recuperar a interface [**IUnknown,**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **QueryInterface** retornará E \_ NOINTERFACE. Para resolver esse problema, use o seguinte código:
>
> <span codelanguage=""></span>
>
> 
| | | <pre><code>    IUnknown* pIUnknown = (IUnknown*)pEffect;&gt;     pIUnknown-&gt;AddRef();</code></pre> | 

>
> 
>
>  

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|-------------|-------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Biblioteca<br/> | <dl> <dt>N/A (uma biblioteca effects 11 está disponível online como fonte compartilhada.)</dt> </dl> |

## <a name="see-also"></a>Confira também

[Effects 11 Interfaces](d3d11-graphics-reference-effects11-interfaces.md)

[D3DX Interfaces](d3d11-graphics-reference-d3dx11-interfaces.md)
