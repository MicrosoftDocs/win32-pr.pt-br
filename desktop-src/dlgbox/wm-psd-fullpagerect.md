---
title: Mensagem de WM_PSD_FULLPAGERECT (Commdlg. h)
description: Notifica um procedimento de gancho PagePaintHook das coordenadas do retângulo da página de exemplo na caixa de diálogo Configurar página. A caixa de diálogo envia essa mensagem quando está prestes a desenhar o conteúdo da página de exemplo.
ms.assetid: 88ca1d60-3335-480a-b874-c6f248a3c23a
keywords:
- Caixas de diálogo de WM_PSD_FULLPAGERECT mensagem
topic_type:
- apiref
api_name:
- WM_PSD_FULLPAGERECT
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0b3d49ca34775657fbb626823fe68632ad963abc29a99ff5aa99dce69753e17
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118280366"
---
# <a name="wm_psd_fullpagerect-message"></a>\_Mensagem FULLPAGERECT do PSD do WM \_

Notifica um procedimento de gancho [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) das coordenadas do retângulo da página de exemplo na caixa de diálogo **Configurar página** . A caixa de diálogo envia essa mensagem quando está prestes a desenhar o conteúdo da página de exemplo.


```C++
#define WM_USER                  0x0400
#define WM_PSD_FULLPAGERECT     (WM_USER+1)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Um identificador para o contexto do dispositivo para a página de exemplo.

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma estrutura [**Rect**](/previous-versions//dd162897(v=vs.85)) que contém as coordenadas, em pixels, da página de exemplo.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se o procedimento de gancho retornar **true**, a caixa de diálogo não enviará mais mensagens e não desenhará na página de exemplo até a próxima vez que o sistema precisar redesenhar a página de exemplo.

Se o procedimento de gancho retornar **false**, a caixa de diálogo enviará as mensagens restantes da sequência de desenho.

## <a name="remarks"></a>Comentários

A caixa de diálogo **Configurar página** inclui uma imagem de uma página de exemplo que mostra como as seleções do usuário afetam a aparência da saída impressa. Ao chamar a função [**PAGESETUPDLG**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) , você pode fornecer um procedimento de gancho de [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) para personalizar a aparência da página de exemplo. Sempre que a caixa de diálogo estiver prestes a desenhar o conteúdo da página de exemplo, a caixa de diálogo enviará uma sequência de mensagens para o procedimento de gancho.

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

[*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook)
</dt> <dt>

[**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85))
</dt> <dt>

[**\_PAGESETUPDLG de PSD do WM \_**](wm-psd-pagesetupdlg.md)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Biblioteca de caixa de diálogo comum](common-dialog-box-library.md)
</dt> </dl>

 

