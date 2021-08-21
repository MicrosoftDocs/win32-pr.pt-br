---
description: Salva um buffer de PRT (transferência de radiance pré-compactado) compactado no disco.
ms.assetid: cc94a83e-f755-411d-a993-4529c5d53cd5
title: Função D3DXSavePRTCompBufferToFile (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSavePRTCompBufferToFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a62bd164ce8eb8175c62658b19dd5ce6282d6c75b081db45f8b0af4994322579
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118524506"
---
# <a name="d3dxsaveprtcompbuffertofile-function"></a>Função D3DXSavePRTCompBufferToFile

Salva um buffer de PRT (transferência de radiance pré-compactado) compactado no disco.

## <a name="syntax"></a>Sintaxe

```cpp
HRESULT D3DXSavePRTCompBufferToFile(
  _In_ LPCSTR              pFileName,
  _In_ LPD3DXPRTCOMPBUFFER pBuffer
);
```

## <a name="parameters"></a>Parâmetros

*pFileName* \[ Em\]

Tipo: **[LPCSTR](../winprog/windows-data-types.md)**

Nome do arquivo no qual o buffer compactado deve ser salvo.

*pBuffer* \[ Em\]

Tipo: **[LPD3DXPRTCOMPBUFFER](id3dxprtcompbuffer.md)**

Endereço de um ponteiro para o objeto [**ID3DXPRTCompBuffer de**](id3dxprtcompbuffer.md) entrada.

## <a name="return-value"></a>Valor retornado

Tipo: **[HRESULT](../com/structure-of-com-error-codes.md)**

Se o método for bem-sucedido, o valor de retorno será **D3D \_ OK.** Se o método falhar, o valor de retorno poderá ser **D3DERR \_ INVALIDCALL.**

## <a name="remarks"></a>Comentários

A configuração do compilador também determina a versão da função. Se Unicode for definido, a chamada de função será resolvida para [D3DXSavePRTCompBufferToFileW.]() Caso contrário, a chamada de função será resolvida **para D3DXSavePRTCompBufferToFileA.**

O formato de arquivo PCA é um arquivo binário na forma de um header e, em seguida, dois ou três blocos de dados.

```cpp
struct PRTCompressHeader
{
    UINT NumSamples;
    UINT NumCoeffs;
    UINT NumChannels;
    UINT TexWidth;
    UINT TexHeight;
    UINT bIsTex;
    UINT NumClusters;
    UINT NumPCA;
};
```

Para o caso de *bIsTex* ser não zero, *NumSamples* deve ser igual a `TexWidth * TexHeight` .

O bloco de dados base que segue o header é `NumCoeffs * NumChannels * (NumPCA + 1) * NumClusters * sizeof(float)` bytes.

A seguir está o bloco de dados de pesos pcA, que é `NumPCA * NumSamples * sizeof(float)` bytes.

Se *NumClusters* for maior que 1, o arquivo terminará com o bloco de dados de IDs de cluster de `NumSamples * sizeof(UINT)` bytes.

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |

## <a name="see-also"></a>Confira também

[Funções de transferência de Radiance pré-comutadas](dx9-graphics-reference-d3dx-functions-prt.md)
