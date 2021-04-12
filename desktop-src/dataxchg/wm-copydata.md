---
title: Mensagem de WM_COPYDATA (WinUser. h)
description: Um aplicativo envia a mensagem do WM \_ CopyData para passar dados para outro aplicativo.
ms.assetid: d937a260-9fd2-4450-a762-20120f589ab1
keywords:
- Troca de dados de mensagem WM_COPYDATA
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
ms.openlocfilehash: 8160c88b11fa109e8bbfaa06f0f6c45c9b7daed0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455300"
---
# <a name="wm_copydata-message"></a>Mensagem do WM \_ CopyData

Um aplicativo envia a mensagem do **WM \_ CopyData** para passar dados para outro aplicativo.


```C++
#define WM_COPYDATA                     0x004A
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Um identificador para a janela que passa os dados.

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma estrutura [**COPYDATASTRUCT**](/windows/win32/api/winuser/ns-winuser-copydatastruct) que contém os dados a serem passados.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se o aplicativo de recebimento processar essa mensagem, ele deverá retornar **true**; caso contrário, ele deve retornar **false**.

## <a name="remarks"></a>Comentários

Os dados que estão sendo passados não devem conter ponteiros ou outras referências a objetos não acessíveis para o aplicativo que está recebendo os dados.

Enquanto essa mensagem está sendo enviada, os dados referenciados não devem ser alterados por outro thread do processo de envio.

O aplicativo de recebimento deve considerar os dados como somente leitura. O parâmetro *lParam* é válido somente durante o processamento da mensagem. O aplicativo de recebimento não deve liberar a memória referenciada pelo *lParam*. Se o aplicativo de recebimento precisar acessar os dados após o [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) retornar, ele deverá copiar os dados em um buffer local.

## <a name="examples"></a>Exemplos

Para obter um exemplo, consulte [usando a cópia de dados](using-data-copy.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[**COPYDATASTRUCT**](/windows/win32/api/winuser/ns-winuser-copydatastruct)
</dt> </dl>

 

