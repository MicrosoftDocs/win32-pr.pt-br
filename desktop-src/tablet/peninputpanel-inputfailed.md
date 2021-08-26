---
description: Preterido. O PenInputPanel foi substituído pelo TIP (Painel de Entrada de Texto). Ocorre quando o foco de entrada muda antes que o objeto PenInputPanel possa inserir a entrada do usuário no controle anexado.
ms.assetid: a5928f78-29d6-40e8-8f87-17c188e51ba9
title: Evento PenInputPanel.InputFailed (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2cc3234c73fc8ba47faa7d1f2ec89477a1bfb86b7c2abda263aff227c5961f1e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119934756"
---
# <a name="peninputpanelinputfailed-event"></a>Evento PenInputPanel.InputFailed

Preterido. O [**PenInputPanel**](peninputpanel-class.md) foi substituído pelo TIP (Painel de [Entrada de Texto).](text-input-panel-reference.md)

Ocorre quando o foco de entrada muda antes que [**o objeto PenInputPanel**](peninputpanel-class.md) possa inserir a entrada do usuário no controle anexado.

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

*hWnd* \[ Em\]
</dt> <dd>

O identificador de janela do controle que invocou o [**objeto PenInputPanel.**](peninputpanel-class.md)

</dd> <dt>

*Chave* \[ Em\]
</dt> <dd>

A chave virtual correspondente à tecla pressionada.

</dd> <dt>

*Texto* \[ Em\]
</dt> <dd>

A cadeia de caracteres que deve ser inserida no controle representado pelo parâmetro *hWnd* quando **o evento InputFailed** foi gerado.

Para obter mais informações sobre o tipo de dados BSTR, consulte [Usando a biblioteca COM](using-the-com-library.md).

</dd> <dt>

*ShiftKey* \[ Em\]
</dt> <dd>

O estado dos modificadores de teclado, incluindo SHIFT, CAPS, CTRL e ALT.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se esse evento for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="remarks"></a>Comentários

O **evento InputFailed** ocorre quando o foco de entrada muda antes da entrada do usuário ser inserida no controle anexado. Por exemplo, se o usuário inserir tinta no painel de escrita, tocará em outro controle de edição antes que o reconhecedor tenha a oportunidade de concluir, esse evento será a disparo.

Usando o alça de janela passado para esse evento, você pode optar por inserir o texto por conta própria quando esse evento ocorrer.

> [!Note]  
> A partir do Microsoft Windows XP Tablet PC Edition 2005, o **evento InputFailed** não se aplica mais. O texto sempre é inserido antes das alterações de foco.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do XP Tablet PC \[ Edition\]<br/>                                                       |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                           |
| Cabeçalho<br/>                   | <dl> <dt>Msinkaut.h (também requer Msinkaut \_ i.c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Peninputpanel**](peninputpanel-class.md)
</dt> </dl>

 

 




