---
description: Inicia uma técnica ativa.
ms.assetid: 6598d77b-8b53-4f2d-aa43-adf358ad486d
title: 'Método ID3DXEffect:: Begin (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.Begin
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 4f4e41830b0bb4507e3969c327c84a85c5336e5f07389fa12e05f3a92f4089a4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119675456"
---
# <a name="id3dxeffectbegin-method"></a>Método ID3DXEffect:: Begin

Inicia uma técnica ativa.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Begin(
  [out] UINT  *pPasses,
  [in]  DWORD Flags
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pPasses* \[ fora\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)\***

Ponteiro para um valor retornado que indica o número de passagens necessárias para renderizar a técnica atual.

</dd> <dt>

*Sinalizadores* \[ de no\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

DWORD que determina se o estado modificado por um efeito é salvo e restaurado. O valor padrão 0 especifica que **ID3DXEffect:: Begin** e [**ID3DXEffect:: End**](id3dxeffect--end.md) salvará e restaurará todos os Estados modificados pelo efeito (incluindo constantes de sombreador de pixel e Vertex). Sinalizadores válidos podem ser vistos nos [sinalizadores de salvar e restaurar de estado do efeito](d3dxfx.md).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será D3D \_ OK. Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Comentários

Um aplicativo define uma técnica ativa no sistema de efeitos chamando **ID3DXEffect:: Begin**. O sistema de efeitos responde capturando todo o estado do pipeline que pode ser alterado pela técnica em um bloco de estado. Um aplicativo sinaliza o final de uma técnica chamando [**ID3DXEffect:: End**](id3dxeffect--end.md), que usa o bloco de estado para restaurar o estado original. O sistema de efeitos, portanto, cuida do salvamento do estado quando uma técnica se torna ativa e restaura o estado quando uma técnica termina. Se você optar por desabilitar essa funcionalidade de salvar e restaurar, consulte [D3DXFX \_ DONOTSAVESAMPLERSTATE](d3dxfx.md).

No par **ID3DXEffect:: Begin** e [**ID3DXEffect:: End**](id3dxeffect--end.md) , um aplicativo usa [**ID3DXEffect:: BeginPass**](id3dxeffect--beginpass.md) para definir a passagem ativa, [**ID3DXEffect:: CommitChanges**](id3dxeffect--commitchanges.md) se alguma alteração de estado ocorreu depois que a passagem foi ativada e [**ID3DXEffect:: endpass**](id3dxeffect--endpass.md) para encerrar a passagem ativa.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> </dl>

 

 
