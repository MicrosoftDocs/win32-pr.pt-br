---
title: Método ISoftKbd EnumSoftKeyboard (Softkbdc. h)
description: O método ISoftKbd EnumSoftKeyboard enumera os teclados suaves possíveis que dão suporte ao idioma especificado.
ms.assetid: c71f99e5-c4c2-4b09-a58f-d3f4348d0c5d
keywords:
- Estrutura de serviços de texto do método EnumSoftKeyboard
- Método EnumSoftKeyboard de estrutura de serviços de texto, interface ISoftKbd
- Estrutura de serviços de texto da interface ISoftKbd, método EnumSoftKeyboard
topic_type:
- apiref
api_name:
- ISoftKbd.EnumSoftKeyboard
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ecdb083684163798a68674628a8b1abc2460268
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455574"
---
# <a name="isoftkbdenumsoftkeyboard-method"></a>Método ISoftKbd:: EnumSoftKeyboard

O método **ISoftKbd:: EnumSoftKeyboard** enumera os teclados Soft possíveis que dão suporte ao idioma especificado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT EnumSoftKeyboard(
  [in]  LANGID langid,
  [out] DWORD  *lpdwKeyboard
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*LangID* \[ no\]
</dt> <dd>

Identificador de idioma.

</dd> <dt>

*lpdwKeyboard* \[ fora\]
</dt> <dd>

Ponteiro para um buffer no qual esse método recupera identificadores dos teclados Soft disponíveis.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Valor                                                                                        | Descrição                                   |
|----------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | O método foi bem-sucedido.<br/>         |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | O parâmetro *LangID* é inválido.<br/> |



 

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

 

 





