---
description: Preterido. O PenInputPanel foi substituído pelo painel de entrada de texto (TIP). Ocorre quando o foco de entrada é alterado antes que o objeto PenInputPanel pudesse inserir a entrada do usuário no controle anexado.
ms.assetid: a5928f78-29d6-40e8-8f87-17c188e51ba9
title: Evento PenInputPanel. InputFailed (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 198c2b466dc03357d9851d7c8a6b7f44c6bf6884
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105763258"
---
# <a name="peninputpanelinputfailed-event"></a>Evento PenInputPanel. InputFailed

Preterido. O [**PenInputPanel**](peninputpanel-class.md) foi substituído pelo painel de [entrada de texto (TIP)](text-input-panel-reference.md).

Ocorre quando o foco de entrada é alterado antes que o objeto [**PenInputPanel**](peninputpanel-class.md) pudesse inserir a entrada do usuário no controle anexado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT InputFailed(
  [in] long  hWnd,
  [in] long  Key,
  [in] BSTR  Text,
  [in] short ShiftKey
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*HWND* \[ no\]
</dt> <dd>

O identificador de janela do controle que invocou o objeto [**PenInputPanel**](peninputpanel-class.md) .

</dd> <dt>

*Chave* \[ no\]
</dt> <dd>

A chave virtual correspondente à chave foi pressionada.

</dd> <dt>

*Texto* \[ de no\]
</dt> <dd>

A cadeia de caracteres que deve ser inserida no controle representado pelo parâmetro *HWND* quando o evento **InputFailed** foi gerado.

Para obter mais informações sobre o tipo de dados BSTR, consulte [usando a biblioteca com](using-the-com-library.md).

</dd> <dt>

*ShiftKey* \[ no\]
</dt> <dd>

O estado dos modificadores de teclado, incluindo SHIFT, CAPS, CTRL e ALT.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se esse evento for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

O evento **InputFailed** ocorre quando o foco de entrada é alterado antes que a entrada do usuário seja inserida no controle anexado. Por exemplo, se o usuário inserir a tinta no painel de escrita, tocará em outro controle de edição antes que o reconhecedor tenha tido a oportunidade de concluir, esse evento será acionado.

Usando o identificador de janela passado para esse evento, você pode optar por inserir o texto por conta própria quando esse evento ocorrer.

> [!Note]  
> A partir do Microsoft Windows XP Tablet PC Edition 2005, o evento **InputFailed** não se aplica mais. O texto sempre é inserido antes do foco ser alterado.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]<br/>                                                       |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                           |
| parâmetro<br/>                   | <dl> <dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**PenInputPanel**](peninputpanel-class.md)
</dt> </dl>

 

 




