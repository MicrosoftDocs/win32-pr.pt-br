---
description: Define um ponteiro para uma função de retorno de chamada opcional que calcula a porcentagem de cálculos de harmônica esférica (SH) concluídas e dá ao chamador a opção de anular o simulador.
ms.assetid: 0a47610d-fa4e-4094-9adb-4fd9306b8a12
title: 'Método ID3DXPRTEngine:: SetCallback (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.SetCallBack
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e9c2cfe710bc41ff71267e381fa0bf576688f9df
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105797676"
---
# <a name="id3dxprtenginesetcallback-method"></a>Método ID3DXPRTEngine:: SetCallback

Define um ponteiro para uma função de retorno de chamada opcional que calcula a porcentagem de cálculos de harmônica esférica (SH) concluídas e dá ao chamador a opção de anular o simulador.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetCallBack(
  [in] LPD3DXSHPRTSIMCB pCB,
  [in] FLOAT            Frequency,
  [in] LPVOID           lpUserContext
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pCB* \[ no\]
</dt> <dd>

Tipo: **[LPD3DXSHPRTSIMCB](lpd3dxshprtsimcb.md)**

Ponteiro para a função de retorno de chamada [LPD3DXSHPRTSIMCB](lpd3dxshprtsimcb.md) que computa a porcentagem de cálculos de SH concluídos. A função de retorno de chamada deve ser implementada para retornar S \_ OK para continuar executando o simulador. Qualquer outro valor anulará o simulador.

</dd> <dt>

*Frequência* \[ do no\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Frequência de chamadas de retorno de chamada. O inverso da frequência é aproximadamente o número de vezes que a função de retorno de chamada será chamada.

</dd> <dt>

*lpUserContext* \[ no\]
</dt> <dd>

Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**

Ponteiro para um valor definido pelo usuário que é passado para a função de retorno de chamada. Normalmente usado por um aplicativo para passar um ponteiro para uma estrutura de dados que fornece informações de contexto para a função de retorno de chamada.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

O valor de retorno é S \_ OK.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> </dl>

 

 
