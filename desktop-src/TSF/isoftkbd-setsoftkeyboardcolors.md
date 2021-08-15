---
title: Método ISoftKbd SetSoftKeyboardColors (Softkbdc. h)
description: O método ISoftKbd SetSoftKeyboardColors define a cor do teclado flexível para o tipo de cor especificado.
ms.assetid: 1abbff35-a5ef-4119-9367-60b6e0961c59
keywords:
- Estrutura de serviços de texto do método SetSoftKeyboardColors
- Método SetSoftKeyboardColors de estrutura de serviços de texto, interface ISoftKbd
- Estrutura de serviços de texto da interface ISoftKbd, método SetSoftKeyboardColors
topic_type:
- apiref
api_name:
- ISoftKbd.SetSoftKeyboardColors
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b572d62895a4f5df503df3ed78bfcf931af331ded25596267f0dd5b4286a4c4b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118877367"
---
# <a name="isoftkbdsetsoftkeyboardcolors-method"></a>Método ISoftKbd:: SetSoftKeyboardColors

O método **ISoftKbd:: SetSoftKeyboardColors** define a cor do teclado flexível para o tipo de cor especificado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetSoftKeyboardColors(
  [in] COLORTYPE colorType,
  [in] COLORREF  Color
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ColorType* \[ no\]
</dt> <dd>

Um valor que especifica o tipo de cor para o teclado virtual. Os valores possíveis são definidos para a enumeração [**ColorType**](/windows/win32/api/icm/ne-icm-colortype) .

</dd> <dt>

*Cor* \[ do no\]
</dt> <dd>

Um valor de [**COLORREF**](/windows/desktop/gdi/colorref) de 32 bits especificando uma cor RGB.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

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
| Redistribuível<br/>          | TSF 1,0 em Windows 2000 Professional<br/>                                        |
| Cabeçalho<br/>                   | <dl> <dt>Softkbdc. h</dt> </dl>  |
| INSERI<br/>                      | <dl> <dt>Softkbd. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Softkbd.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ISoftKbd**](isoftkbd.md)
</dt> <dt>

[**ISoftKbd::GetSoftKeyboardColors**](isoftkbd-getsoftkeyboardcolors.md)
</dt> <dt>

[**COLORtype**](/windows/win32/api/icm/ne-icm-colortype)
</dt> <dt>

[**COLORREF**](/windows/desktop/gdi/colorref)
</dt> </dl>

 

