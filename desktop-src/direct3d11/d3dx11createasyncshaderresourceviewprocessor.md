---
title: Função D3DX11CreateAsyncShaderResourceViewProcessor (D3DX11async.h)
description: Observação A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para Windows 8 e não tem suporte para aplicativos da Windows Store.
ms.assetid: bd9349af-f433-47f9-b443-3049c32fc286
keywords:
- Função D3DX11CreateAsyncShaderResourceViewProcessor Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateAsyncShaderResourceViewProcessor
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 305705a4fd82b7f2267e3d56630b78c8c8d98473d946b1629e713162f4a6ae92
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118536565"
---
# <a name="d3dx11createasyncshaderresourceviewprocessor-function"></a>Função D3DX11CreateAsyncShaderResourceViewProcessor

> [!Note]  
> A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para Windows 8 e não tem suporte para aplicativos da Windows Store. Consulte Observações.

 

Crie um processador de dados que carregará um recurso e, em seguida, criará uma exibição sombreador-recurso para ele. Os processadores de dados são um componente do recurso de carregamento de dados assíncrono no D3DX11 que usa [**bombas de thread.**](id3dx11threadpump.md)

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DX11CreateAsyncShaderResourceViewProcessor(
  _In_  ID3D11Device           *pDevice,
  _In_  D3DX11_IMAGE_LOAD_INFO *pLoadInfo,
  _Out_ ID3DX11DataProcessor   **ppDataProcessor
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pDevice* \[ Em\]
</dt> <dd>

Tipo: **[ **ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\***

Ponteiro para o dispositivo Direct3D (consulte [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)) que será usado para criar um recurso e uma exibição de sombreador-recurso para esse recurso.

</dd> <dt>

*pLoadInfo* \[ Em\]
</dt> <dd>

Tipo: **[ **D3DX11 \_ IMAGE \_ LOAD \_ INFO**](d3dx11-image-load-info.md)\***

Opcional. Identifica as características de uma textura (consulte [**D3DX11 \_ IMAGE \_ LOAD \_ INFO**](d3dx11-image-load-info.md)) quando o processador de dados é criado; de definido como **NULL** para ler as características de uma textura quando a textura é carregada.

</dd> <dt>

*ppDataProcessor* \[ out\]
</dt> <dd>

Tipo: **[ **ID3DX11DataProcessor**](id3dx11dataprocessor.md)\*\***

Endereço de um ponteiro para um buffer que contém o processador de dados criado (consulte Interface [**ID3DX11DataProcessor**](id3dx11dataprocessor.md)).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

O valor de retorno é um dos valores listados em Códigos de Retorno [do Direct3D 11.](d3d11-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Comentários

Não há nenhuma implementação do carregador assíncrono fora do D3DX 10 e do D3DX 11.

Para aplicativos da Windows Store, os exemplos do DirectX (por exemplo, o exemplo de tutorial do [Direct3D](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) incluem o módulo **BasicLoader** que usa o modelo de programação assíncrona do Windows Runtime ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))).

Para aplicativos da área de trabalho Win32, você pode usar o [Runtime de Simultaneidade](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) para implementar algo semelhante ao modelo de programação assíncrona Windows Runtime.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX11async.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX11.lib</dt> </dl>    |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções D3DX](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

