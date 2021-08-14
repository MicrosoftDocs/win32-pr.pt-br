---
description: O aplicativo implementa esse método. Esse método é chamado quando ocorre um retorno de chamada para um conjunto de animação em uma das faixas durante uma chamada para ID3DXAnimationController::AdvanceTime.
ms.assetid: eb606fb0-d6b9-456d-97e1-b595306e6463
title: Método ID3DXAnimationCallbackHandler::HandleCallback (D3dx9anim.h)
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
ms.openlocfilehash: 12fcfa0feba1d239cf72c37e78fec63140dda4f954e7c48dffd643dcca4400c9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119279206"
---
# <a name="id3dxanimationcallbackhandlerhandlecallback-method"></a>Método ID3DXAnimationCallbackHandler::HandleCallback

O aplicativo implementa esse método. Esse método é chamado quando ocorre um retorno de chamada para um conjunto de animação em uma das faixas durante uma chamada para [**ID3DXAnimationController::AdvanceTime**](id3dxanimationcontroller--advancetime.md).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT HandleCallback(
  [in] UINT   Track,
  [in] LPVOID pCallbackData
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Acompanhar* \[ Em\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Identificador da faixa na qual o retorno de chamada ocorre.

</dd> <dt>

*pCallbackData* \[ Em\]
</dt> <dd>

Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**

Ponteiro para dados de retorno de chamada de propriedade do usuário.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Os valores de retorno desse método são implementados por um programador de aplicativos. Em geral, se nenhum erro ocorrer, programe o método para retornar D3D \_ OK. Caso contrário, programe o método para retornar uma mensagem de erro apropriada de [D3DERR](d3derr.md) ou [**D3DXERR**](./d3dxerr.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXAnimationCallbackHandler](id3dxanimationcallbackhandler.md)
</dt> </dl>

 

 
