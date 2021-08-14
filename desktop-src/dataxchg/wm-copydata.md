---
title: WM_COPYDATA mensagem (Winuser.h)
description: Um aplicativo envia a mensagem WM \_ COPYDATA para passar dados para outro aplicativo.
ms.assetid: d937a260-9fd2-4450-a762-20120f589ab1
keywords:
- WM_COPYDATA de dados de Exchange
topic_type:
- apiref
api_name:
- WM_COPYDATA
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4eb91b2544bf0ebf0e8767a611b422de9aaaf1d73161e47c7bf27768f4acecb4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118304480"
---
# <a name="wm_copydata-message"></a>Mensagem WM \_ COPYDATA

Um aplicativo envia a **mensagem WM \_ COPYDATA** para passar dados para outro aplicativo.


```C++
#define WM_COPYDATA                     0x004A
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Um alça para a janela passando os dados.

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma [**estrutura COPYDATASTRUCT**](/windows/win32/api/winuser/ns-winuser-copydatastruct) que contém os dados a serem passados.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se o aplicativo receptor processa essa mensagem, ele deve retornar **TRUE**; caso contrário, ele deverá retornar **FALSE.**

## <a name="remarks"></a>Comentários

Os dados que estão sendo passados não devem conter ponteiros ou outras referências a objetos não acessíveis ao aplicativo que está recebendo os dados.

Enquanto essa mensagem está sendo enviada, os dados referenciados não devem ser alterados por outro thread do processo de envio.

O aplicativo receptor deve considerar os dados somente leitura. O *parâmetro lParam* é válido somente durante o processamento da mensagem. O aplicativo receptor não deve liberar a memória referenciada por *lParam*. Se o aplicativo receptor tiver que acessar os dados depois que [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) retornar, ele deverá copiar os dados para um buffer local.

## <a name="examples"></a>Exemplos

Para ver um exemplo, consulte [Usando Cópia de Dados](using-data-copy.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[**COPYDATASTRUCT**](/windows/win32/api/winuser/ns-winuser-copydatastruct)
</dt> </dl>

 

