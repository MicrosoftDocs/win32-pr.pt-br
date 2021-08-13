---
title: Função D3DX11CreateThreadPump (D3DX11core. h)
description: observe que a biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida por Windows 8 e não tem suporte para aplicativos da loja Windows. Consulte Observações. Criar uma bomba de thread.
ms.assetid: 8983a2e2-185f-43c0-baf0-a4c883d91220
keywords:
- Função D3DX11CreateThreadPump Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateThreadPump
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a3a19c338b330604caae9ce5a1e7f7222664b0521f9874c3eff07ff1fc8a4f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118536097"
---
# <a name="d3dx11createthreadpump-function"></a>Função D3DX11CreateThreadPump

> [!Note]  
> a biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida por Windows 8 e não tem suporte para aplicativos da loja Windows. Consulte Observações.

 

Criar uma bomba de thread.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DX11CreateThreadPump(
  _In_  UINT              cIoThreads,
  _In_  UINT              cProcThreads,
  _Out_ ID3DX11ThreadPump **ppThreadPump
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*cIoThreads* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

O número de threads de e/s a serem criados. Se 0 for especificado, o Direct3D tentará calcular o número ideal de threads com base na configuração de hardware.

</dd> <dt>

*cProcThreads* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

O número de threads de processo a serem criados. Se 0 for especificado, o Direct3D tentará calcular o número ideal de threads com base na configuração de hardware.

</dd> <dt>

*ppThreadPump* \[ fora\]
</dt> <dd>

Tipo: **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\*\***

A bomba de thread criada. Consulte a [**interface ID3DX11ThreadPump**](id3dx11threadpump.md).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Comentários

Uma bomba de thread é um objeto com uso intensivo de recursos. Somente uma bomba de thread deve ser criada por aplicativo.

Não há nenhuma implementação do carregador assíncrono fora do D3DX 10 e D3DX 11.

para aplicativos da Windows Store, os exemplos do DirectX (por exemplo, o [exemplo de tutorial do Direct3D](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) incluem o módulo **BasicLoader** que usa o Windows Runtime modelo de programação assíncrona ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))).

para aplicativos de área de trabalho Win32, você pode usar o [Tempo de Execução de Simultaneidade](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) para implementar algo semelhante ao modelo de programação Windows Runtime assíncrona.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX11core. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX11. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções D3DX](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

