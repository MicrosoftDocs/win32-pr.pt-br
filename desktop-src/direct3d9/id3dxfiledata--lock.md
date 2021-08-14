---
description: Acessa os dados do arquivo. x.
ms.assetid: 0e92914b-47b3-4a88-87ba-ce3c14282dbb
title: 'Método ID3DXFileData:: Lock (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileData.Lock
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: c052f570b3206c5a0661a4cf4ab38b259fb476f4eda1322df80e709608d09bf5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118520703"
---
# <a name="id3dxfiledatalock-method"></a>Método ID3DXFileData:: Lock

Acessa os dados do arquivo. x.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Lock(
  [in]       SIZE_T *pSize,
  [in] const VOID   **ppData
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*psize* \[ no\]
</dt> <dd>

Tipo: **[ **tamanho \_ T**](../winprog/windows-data-types.md)\***

Ponteiro para o tamanho dos dados do arquivo. x.

</dd> <dt>

*ppData* \[ no\]
</dt> <dd>

Tipo: **const void \* \***

Endereço de um ponteiro para receber o ponteiro de interface do objeto de dados do arquivo [**ID3DXFileData**](id3dxfiledata.md) . Consulte Observações.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será S \_ OK. Se o método falhar, o seguinte valor será retornado: D3DXFERR \_ BADVALUE.

## <a name="remarks"></a>Comentários

O ponteiro *ppData* só é válido durante um **ID3DXFileData:: Lock** ... [**ID3DXFileData:: desbloquear**](id3dxfiledata--unlock.md) sequência. Você pode fazer várias chamadas de bloqueio. No entanto, você deve garantir que o número de chamadas de bloqueio corresponda ao número de chamadas de desbloqueio.

Como os dados de arquivo não têm garantia de serem alinhados corretamente com limites de byte, você deve acessar *ppData* com ponteiros não alinhados.

Não há garantia de que os valores de parâmetro retornados sejam válidos devido à possível corrupção de arquivo; Portanto, seu código deve verificar os valores de parâmetro retornados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Xof. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXFileData](id3dxfiledata.md)
</dt> </dl>

 

 
