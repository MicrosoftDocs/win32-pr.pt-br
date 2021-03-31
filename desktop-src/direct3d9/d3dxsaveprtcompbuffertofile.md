---
description: Salva um buffer de PRT (transferência radiante em cluster) compactado em disco.
ms.assetid: cc94a83e-f755-411d-a993-4529c5d53cd5
title: Função D3DXSavePRTCompBufferToFile (D3DX9Mesh. h)
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
ms.openlocfilehash: d06629185637ce6fa0d7d33d5454282d2bbb8ec2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103930584"
---
# <a name="d3dxsaveprtcompbuffertofile-function"></a>Função D3DXSavePRTCompBufferToFile

Salva um buffer de PRT (transferência radiante em cluster) compactado em disco.

## <a name="syntax"></a>Sintaxe

```cpp
HRESULT D3DXSavePRTCompBufferToFile(
  _In_ LPCSTR              pFileName,
  _In_ LPD3DXPRTCOMPBUFFER pBuffer
);
```

## <a name="parameters"></a>Parâmetros

*pFileName* \[ no\]

Tipo: **[LPCSTR](../winprog/windows-data-types.md)**

Nome do arquivo no qual o buffer compactado deve ser salvo.

*pBuffer* \[ no\]

Tipo: **[LPD3DXPRTCOMPBUFFER](id3dxprtcompbuffer.md)**

Endereço de um ponteiro para o objeto [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) de entrada.

## <a name="return-value"></a>Retornar valor

Tipo: **[HRESULT](../com/structure-of-com-error-codes.md)**

Se o método for bem sucedido, o valor de retorno será **D3D \_ OK**. Se o método falhar, o valor de retorno poderá ser **D3DERR \_ INVALIDCALL**.

## <a name="remarks"></a>Comentários

A configuração do compilador também determina a versão da função. Se o Unicode estiver definido, a chamada de função será resolvida como [D3DXSavePRTCompBufferToFileW](). Caso contrário, a chamada de função será resolvida como **D3DXSavePRTCompBufferToFileA**.

O formato de arquivo do PCA é um arquivo binário na forma de um cabeçalho e dois ou três blocos de dados.

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

Para o caso de *bIsTex* ser diferente de zero, *NumSamples* deve ser igual `TexWidth * TexHeight` .

O bloco de dados base que segue o cabeçalho é de `NumCoeffs * NumChannels * (NumPCA + 1) * NumClusters * sizeof(float)` bytes.

Depois disso, está o bloco de dados de pesos do PCA, que é de `NumPCA * NumSamples * sizeof(float)` bytes.

Se *NumClusters* for maior que 1, o arquivo terminará com o bloco de dados de IDs de cluster de `NumSamples * sizeof(UINT)` bytes.

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |

## <a name="see-also"></a>Confira também

[Funções de transferência radiante preputadas](dx9-graphics-reference-d3dx-functions-prt.md)
