---
title: Função D3DX11CreateAsyncTextureInfoProcessor (D3DX11tex. h)
description: observe que a biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida por Windows 8 e não tem suporte para aplicativos da loja Windows. Consulte Observações. Crie um processador de dados para ser usado com uma bomba de thread. | Função D3DX11CreateAsyncTextureInfoProcessor (D3DX11tex. h)
ms.assetid: 87de73a5-21f7-4abd-b83a-65c6761681c3
keywords:
- Função D3DX11CreateAsyncTextureInfoProcessor Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateAsyncTextureInfoProcessor
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da992c258fe79bd1ed81274495e884339f40aed337fcf11665ec27110afaf422
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118536255"
---
# <a name="d3dx11createasynctextureinfoprocessor-function"></a>Função D3DX11CreateAsyncTextureInfoProcessor

> [!Note]  
> a biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida por Windows 8 e não tem suporte para aplicativos da loja Windows. Consulte Observações.

 

Crie um processador de dados para ser usado com uma [**bomba de thread**](id3dx11threadpump.md).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DX11CreateAsyncTextureInfoProcessor(
  _In_  D3DX11_IMAGE_INFO    *pImageInfo,
  _Out_ ID3DX11DataProcessor **ppDataProcessor
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pImageInfo* \[ no\]
</dt> <dd>

Tipo: **[ **D3DX11 \_ Image \_ info**](d3dx11-image-info.md)\***

Opcional. Identifica as características de uma textura (consulte [**\_ \_ informações de imagem D3DX11**](d3dx11-image-info.md)) quando o processador de dados é criado; defina isso como **nulo** para ler as características de uma textura quando a textura for carregada.

</dd> <dt>

*ppDataProcessor* \[ fora\]
</dt> <dd>

Tipo: **[ **ID3DX11DataProcessor**](id3dx11dataprocessor.md)\*\***

Endereço de um ponteiro para um buffer que contém o processador de dados criado (consulte a [**interface ID3DX11DataProcessor**](id3dx11dataprocessor.md)).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Comentários

Essa API cria uma interface de processador de dados; [**D3DX11CreateAsyncTextureProcessor**](d3dx11createasynctextureprocessor.md) cria a interface do processador de dados e carrega a textura.

Não há nenhuma implementação do carregador assíncrono fora do D3DX 10 e D3DX 11.

para aplicativos da Windows Store, os exemplos do DirectX (por exemplo, o [exemplo de tutorial do Direct3D](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) incluem o módulo **BasicLoader** que usa o Windows Runtime modelo de programação assíncrona ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))).

para aplicativos de área de trabalho Win32, você pode usar o [Tempo de Execução de Simultaneidade](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) para implementar algo semelhante ao modelo de programação Windows Runtime assíncrona.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX11tex. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX11. lib</dt> </dl>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções D3DX](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

