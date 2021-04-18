---
title: Método ISoftKbd GetSoftKeyboardColors (Softkbdc. h)
description: O método ISoftKbd GetSoftKeyboardColors recupera a cor do teclado flexível correspondente ao tipo de cor fornecido.
ms.assetid: d59d249c-a1c4-4d6a-add6-632be55a7549
keywords:
- Estrutura de serviços de texto do método GetSoftKeyboardColors
- Método GetSoftKeyboardColors de estrutura de serviços de texto, interface ISoftKbd
- Estrutura de serviços de texto da interface ISoftKbd, método GetSoftKeyboardColors
topic_type:
- apiref
api_name:
- ISoftKbd.GetSoftKeyboardColors
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f8f184dc04ddcbef18a9279000b1a68acd35bd3
ms.sourcegitcommit: d6bf2018c588c9782e1eed21b3cdea3523ec6955
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2021
ms.locfileid: "105758128"
---
# <a name="isoftkbdgetsoftkeyboardcolors-method"></a>Método ISoftKbd:: GetSoftKeyboardColors

O método **ISoftKbd:: GetSoftKeyboardColors** recupera a cor do teclado flexível correspondente ao tipo de cor fornecido.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetSoftKeyboardColors(
  [in]  COLORTYPE colorType,
  [out] COLORREF  *lpColor
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ColorType* \[ no\]
</dt> <dd>

Um valor que especifica o tipo de cor a ser recuperado para o teclado virtual. Os valores possíveis são definidos para a enumeração [**ColorType**](/windows/win32/api/icm/ne-icm-colortype) .

</dd> <dt>

*lpColor* \[ fora\]
</dt> <dd>

Ponteiro para um buffer no qual esse método recupera um valor de [**COLORREF**](/windows/desktop/gdi/colorref) de 32 bits especificando uma cor RGB.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Valor                                                                                        | Descrição                                  |
|----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | O método foi bem-sucedido.<br/>        |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Um dos parâmetros é inválido.<br/> |



 

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
</dt> <dt>

[**ISoftKbd::SetSoftKeyboardColors**](/windows/desktop/TSF/isoftkbd-setsoftkeyboardcolors)
</dt> <dt>

[**COLORtype**](/windows/win32/api/icm/ne-icm-colortype)
</dt> <dt>

[**COLORREF**](/windows/desktop/gdi/colorref)
</dt> </dl>

 

