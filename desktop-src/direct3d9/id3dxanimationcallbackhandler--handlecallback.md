---
description: 'O aplicativo implementa esse método. Esse método é chamado quando ocorre um retorno de chamada para uma animação definida em uma das faixas durante uma chamada para ID3DXAnimationController:: AdvanceTime.'
ms.assetid: eb606fb0-d6b9-456d-97e1-b595306e6463
title: 'Método ID3DXAnimationCallbackHandler:: HandleCallback (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationCallbackHandler.HandleCallback
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 49de0adef71435dbcf35afae8cfa555999826a34
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105797596"
---
# <a name="id3dxanimationcallbackhandlerhandlecallback-method"></a>Método ID3DXAnimationCallbackHandler:: HandleCallback

O aplicativo implementa esse método. Esse método é chamado quando ocorre um retorno de chamada para uma animação definida em uma das faixas durante uma chamada para [**ID3DXAnimationController:: AdvanceTime**](id3dxanimationcontroller--advancetime.md).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT HandleCallback(
  [in] UINT   Track,
  [in] LPVOID pCallbackData
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Acompanhar* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Identificador do controle no qual o retorno de chamada ocorre.

</dd> <dt>

*pCallbackData* \[ no\]
</dt> <dd>

Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**

Ponteiro para dados de retorno de chamada de Propriedade do usuário.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Os valores de retorno desse método são implementados por um programador de aplicativos. Em geral, se nenhum erro ocorrer, Programe o método para retornar o D3D \_ OK. Caso contrário, Programe o método para retornar uma mensagem de erro apropriada de [D3DERR](d3derr.md) ou [**D3DXERR**](./d3dxerr.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXAnimationCallbackHandler](id3dxanimationcallbackhandler.md)
</dt> </dl>

 

 
