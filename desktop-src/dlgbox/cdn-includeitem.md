---
title: CDN_INCLUDEITEM código de notificação (Commdlg. h)
description: Enviado por uma caixa de diálogo abrir ou salvar como para determinar se a caixa de diálogo deve exibir um item na lista de itens de uma pasta do Shell.
ms.assetid: 0972a78d-e058-4bac-85bd-fbd4c3885552
keywords:
- Caixas de diálogo CDN_INCLUDEITEM código de notificação
topic_type:
- apiref
api_name:
- CDN_INCLUDEITEM
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 445ea8626d7ecc6c1c72cd13eebfc9811ae229b772787eae2625224d830bc25e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117721074"
---
# <a name="cdn_includeitem-notification-code"></a>CDN \_ Código de notificação do INCLUDEITEM

\[a partir do Windows Vista, as caixas de diálogo **abrir** e **salvar como** comuns foram substituídas pela [caixa de diálogo de Item comum](../shell/common-file-dialog.md). Recomendamos que você use a API de caixa de diálogo de item comum em vez dessas caixas de diálogo da biblioteca de caixas de diálogo comuns.\]

Enviado por uma caixa de diálogo **abrir** ou **salvar como** para determinar se a caixa de diálogo deve exibir um item na lista de itens de uma pasta do Shell. quando o usuário abre uma pasta, a caixa de diálogo envia uma notificação **CDN \_ INCLUDEITEM** para cada item na pasta. A caixa de diálogo enviará essa notificação somente se o sinalizador **OFN \_ ENABLEINCLUDENOTIFY** tiver sido definido quando a caixa de diálogo foi criada.

Seu procedimento de gancho [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) recebe essa mensagem na forma de uma mensagem de [**\_ notificação do WM**](../controls/wm-notify.md) .


```C++
#define CDN_FIRST               (0U-601U)
#define CDN_INCLUDEITEM         (CDN_FIRST - 0x0007)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma estrutura [**OFNOTIFYEX**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifyexa) .

a estrutura [**OFNOTIFYEX**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifyexa) contém uma estrutura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) cujo membro de **código** indica a mensagem de notificação **CDN \_ INCLUDEITEM** .

O membro **PSF** da estrutura [**OFNOTIFYEX**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifyexa) é um ponteiro para uma interface para a pasta cujos itens estão sendo enumerados. O membro **PIDL** é um ponteiro para uma lista de identificadores de item que identifica o item relativo à pasta.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se o procedimento de gancho [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) retornar zero, a caixa de diálogo excluirá o item da lista de itens.

Para incluir o item, retorne um valor diferente de zero do procedimento de gancho.

## <a name="remarks"></a>Comentários

a caixa de diálogo sempre inclui itens que têm os atributos **SFGAO \_ FILESYSTEM** e **SFGAO \_ FILESYSANCESTOR** , independentemente do valor retornado por **CDN \_ INCLUDEITEM**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Commdlg. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**GetOpenFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[**GetSaveFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)
</dt> <dt>

[**OFNOTIFYEX**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifyexa)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Biblioteca de caixa de diálogo comum](common-dialog-box-library.md)
</dt> </dl>

