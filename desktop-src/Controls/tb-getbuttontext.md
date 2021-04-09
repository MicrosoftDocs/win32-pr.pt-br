---
title: Mensagem de TB_GETBUTTONTEXT (commctrl. h)
description: Recupera o texto de exibição de um botão em uma barra de ferramentas.
ms.assetid: 16dd7181-a404-4056-b084-05f49f5a4b14
keywords:
- Controles de TB_GETBUTTONTEXT de mensagens do Windows
topic_type:
- apiref
api_name:
- TB_GETBUTTONTEXT
- TB_GETBUTTONTEXTA
- TB_GETBUTTONTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ac0b238574cc136f41959b57f3f0e1ec13e3ea1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085723"
---
# <a name="tb_getbuttontext-message"></a>TB de \_ mensagem GETBUTTONTEXT

Recupera o texto de exibição de um botão em uma barra de ferramentas.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador de comando do botão cujo texto deve ser recuperado.

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para um buffer que recebe o texto do botão.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna o comprimento, em caracteres, da cadeia de caracteres apontada por *lParam*. O comprimento não inclui o caractere nulo de terminação. Se não for bem-sucedida, o valor de retorno será-1.

## <a name="remarks"></a>Comentários

**Aviso de segurança:** Usar essa mensagem incorretamente pode comprometer a segurança do seu programa. Essa mensagem não fornece uma maneira de saber o tamanho do buffer. Se você usar essa mensagem, primeiro chame a mensagem transmitindo **NULL** no *lParam*; isso retorna o número de caracteres, excluindo **NULL** que são necessários. Em seguida, chame a mensagem uma segunda vez para recuperar a cadeia de caracteres. Você deve examinar as [considerações de segurança: controles do Microsoft Windows](sec-comctls.md) antes de continuar.

A cadeia de caracteres retornada corresponde ao texto que é exibido no momento pelo botão.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **TB \_ GETBUTTONTEXTW** (Unicode) e **TB \_ GETBUTTONTEXTA** (ANSI)<br/>         |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**TB de \_ GETBUTTONINFO**](tb-getbuttoninfo.md)
</dt> <dt>

[**TB \_ GETstring**](tb-getstring.md)
</dt> <dt>

[**TB de \_ SETBUTTONINFO**](tb-setbuttoninfo.md)
</dt> </dl>

 

 





