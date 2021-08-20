---
description: Define um ponteiro para uma função de retorno de chamada opcional que computa o percentual de cálculos de sh (harmônicos esféricos) concluídos e fornece ao chamador a opção de anular o simulador.
ms.assetid: 0a47610d-fa4e-4094-9adb-4fd9306b8a12
title: Método ID3DXPRTEngine::SetCallBack (D3DX9Mesh.h)
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
ms.openlocfilehash: e1ed2570c45380ce4faa0be42ddb9231d6420940dd9a6d669d6f2540154dc644
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119847353"
---
# <a name="id3dxprtenginesetcallback-method"></a>Método ID3DXPRTEngine::SetCallBack

Define um ponteiro para uma função de retorno de chamada opcional que computa o percentual de cálculos de sh (harmônicos esféricos) concluídos e fornece ao chamador a opção de anular o simulador.

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

*pCB* \[ Em\]
</dt> <dd>

Tipo: **[LPD3DXSHPRTSIMCB](lpd3dxshprtsimcb.md)**

Ponteiro para a função de retorno de chamada [LPD3DXSHPRTSIMCB](lpd3dxshprtsimcb.md) que calcula o percentual de cálculos sh concluídos. A função de retorno de chamada deve ser implementada para retornar S \_ OK para continuar executando o simulador. Qualquer outro valor anulará o simulador.

</dd> <dt>

*Frequência* \[ Em\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Frequência de chamadas de retorno de chamada. O inverso de Frequency é aproximadamente o número de vezes que a função de retorno de chamada será chamada.

</dd> <dt>

*lpUserContext* \[ Em\]
</dt> <dd>

Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**

Ponteiro para um valor definido pelo usuário que é passado para a função de retorno de chamada. Normalmente usado por um aplicativo para passar um ponteiro para uma estrutura de dados que fornece informações de contexto para a função de retorno de chamada.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

O valor de retorno é S \_ OK.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> </dl>

 

 
