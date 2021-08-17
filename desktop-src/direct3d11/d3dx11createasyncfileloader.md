---
title: Função D3DX11CreateAsyncFileLoader (D3DX11async. h)
description: observe que a biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida por Windows 8 e não tem suporte para aplicativos da loja Windows. Consulte Observações. Crie um carregador de arquivo assíncrono.
ms.assetid: ee24ac00-3636-4900-9b8a-27778c9a2152
keywords:
- Função D3DX11CreateAsyncFileLoader Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateAsyncFileLoader
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc5997d31765df1de78ed6323a0176be024a5e26bb2eb81a0556f2abedbf2e5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124861"
---
# <a name="d3dx11createasyncfileloader-function"></a>Função D3DX11CreateAsyncFileLoader

> [!Note]  
> a biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida por Windows 8 e não tem suporte para aplicativos da loja Windows. Consulte Observações.

 

Crie um carregador de arquivo assíncrono.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DX11CreateAsyncFileLoader(
  _In_  LPCTSTR           pFileName,
  _Out_ ID3DX11DataLoader **ppDataLoader
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pFileName* \[ no\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**

O nome do arquivo a ser carregado. Se as configurações do compilador exigirem Unicode, o tipo de dados LPCTSTR será resolvido para LPCWSTR. Caso contrário, o tipo de dados será resolvido para LPCSTR.

</dd> <dt>

*ppDataLoader* \[ fora\]
</dt> <dd>

Tipo: **[ **ID3DX11DataLoader**](id3dx11dataloader.md)\*\***

Endereço de um ponteiro para o carregador de dados assíncronos (consulte a [**interface ID3DX11DataLoader**](id3dx11dataloader.md)).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Comentários

Não há nenhuma implementação do carregador assíncrono fora do D3DX 10 e D3DX 11.

para aplicativos da Windows Store, os exemplos do DirectX (por exemplo, o [exemplo de tutorial do Direct3D](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) incluem o módulo **BasicLoader** que usa o Windows Runtime modelo de programação assíncrona ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))).

para aplicativos de área de trabalho Win32, você pode usar o [Tempo de Execução de Simultaneidade](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) para implementar algo semelhante ao modelo de programação Windows Runtime assíncrona.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX11async. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX11. lib</dt> </dl>    |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções D3DX](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

