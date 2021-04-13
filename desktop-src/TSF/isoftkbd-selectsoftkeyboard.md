---
title: Método ISoftKbd SelectSoftKeyboard (Softkbdc. h)
description: O método ISoftKbd SelectSoftKeyboard seleciona o teclado virtual especificado.
ms.assetid: 7e85d346-3741-457d-aadd-11d3a6710e85
keywords:
- Estrutura de serviços de texto do método SelectSoftKeyboard
- Método SelectSoftKeyboard de estrutura de serviços de texto, interface ISoftKbd
- Estrutura de serviços de texto da interface ISoftKbd, método SelectSoftKeyboard
topic_type:
- apiref
api_name:
- ISoftKbd.SelectSoftKeyboard
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbda9399297e9776e7fbd7cecb364fd7f6cd4604
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499620"
---
# <a name="isoftkbdselectsoftkeyboard-method"></a>Método ISoftKbd:: SelectSoftKeyboard

O método **ISoftKbd:: SelectSoftKeyboard** seleciona o teclado virtual especificado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SelectSoftKeyboard(
  [in] DWORD dwKeyboardId
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*dwKeyboardId* \[ no\]
</dt> <dd>

Identificador do teclado virtual a ser selecionado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Valor                                                                                        | Descrição                                         |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | O método foi bem-sucedido.<br/>               |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | O parâmetro *dwKeyboardId* é inválido.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                             |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                   |
| Redistribuível<br/>          | TSF 1,0 no Windows 2000 Professional<br/>                                        |
| parâmetro<br/>                   | <dl> <dt>Softkbdc. h</dt> </dl>  |
| INSERI<br/>                      | <dl> <dt>Softkbd. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Softkbd.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ISoftKbd**](isoftkbd.md)
</dt> </dl>

 

 





