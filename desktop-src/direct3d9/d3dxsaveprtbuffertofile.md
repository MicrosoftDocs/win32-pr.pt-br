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
ms.openlocfilehash: b796ee24be44bf65be7df938bdfe85d6784cc5f3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105759865"
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

## <a name="return-value"></a>Retornar valor

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
