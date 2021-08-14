---
description: Salva um buffer de PRT (transferência de radiante de computação) em disco.
ms.assetid: 1fca69bd-6729-45af-981f-b7480c741bc2
title: Função D3DXSavePRTBufferToFile (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSavePRTBufferToFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0bfa3d06970d138ff1c868403c20bb41cf14f0a5cbb7116cbe0f0843a51258dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118524526"
---
# <a name="d3dxsaveprtbuffertofile-function"></a>Função D3DXSavePRTBufferToFile

Salva um buffer de PRT (transferência de radiante de computação) em disco.

## <a name="syntax"></a>Sintaxe

```cpp
HRESULT D3DXSavePRTBufferToFile(
  _In_ LPCSTR          pFileName,
  _In_ LPD3DXPRTBUFFER pBuffer
);
```

## <a name="parameters"></a>Parâmetros

*pFileName* \[ no\]

Tipo: **[LPCSTR](../winprog/windows-data-types.md)**

Nome do arquivo no qual o buffer deve ser salvo.

*pBuffer* \[ no\]

Tipo: **[LPD3DXPRTBUFFER](id3dxprtbuffer.md)**

Endereço de um ponteiro para o objeto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) de entrada.

## <a name="return-value"></a>Valor retornado

Tipo: **[HRESULT](../com/structure-of-com-error-codes.md)**

Se o método for bem sucedido, o valor de retorno será **D3D \_ OK**. Se o método falhar, o valor de retorno poderá ser **D3DERR \_ INVALIDCALL**.

## <a name="remarks"></a>Comentários

A configuração do compilador também determina a versão da função. Se o Unicode estiver definido, a chamada de função será resolvida como [D3DXSavePRTBufferToFileW](). Caso contrário, a chamada de função será resolvida como **D3DXSavePRTBufferToFileA**.

O formato de arquivo PRT é um arquivo binário na forma de um cabeçalho e em um bloco de dados.

```cpp
struct PRTHeader
{
    UINT NumSamples;
    UINT NumCoeffs;
    UINT NumChannels;
    UINT TexWidth;
    UINT TexHeight;
    UINT bIsTex;
};
```

Para o caso de *bIsTex* ser diferente de zero, *NumSamples* deve ser igual `TexWidth * TexHeight` .

O bloco de dados que segue o cabeçalho é de `NumSamples * NumCoeffs * NumChannels * sizeof(float)` bytes.

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |

## <a name="see-also"></a>Confira também

[Funções de transferência radiante preputadas](dx9-graphics-reference-d3dx-functions-prt.md)
