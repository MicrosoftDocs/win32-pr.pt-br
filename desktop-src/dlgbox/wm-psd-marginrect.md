---
title: WM_PSD_MARGINRECT mensagem (Commdlg.h)
description: Notifica o procedimento de gancho de uma caixa de diálogo Configuração de Página, PagePaintHook, de que a caixa de diálogo está prestes a desenhar o retângulo de margem da página de exemplo.
ms.assetid: 81c057ab-6faf-4dd8-8b0c-34a2753e572c
keywords:
- WM_PSD_MARGINRECT caixa de diálogo de mensagem
topic_type:
- apiref
api_name:
- WM_PSD_MARGINRECT
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09523258d1f67cfc4f35433a43a6b5a17db0be9dedaea87511c0c6d1327f82cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118985256"
---
# <a name="wm_psd_marginrect-message"></a>Mensagem WM \_ PSD \_ MARGINRECT

Notifica o procedimento de gancho de uma caixa de diálogo Configuração de Página, [**PagePaintHook,**](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook)que **a** caixa de diálogo está prestes a desenhar o retângulo de margem da página de exemplo.


```C++
#define WM_USER                  0x0400
#define WM_PSD_MARGINRECT       (WM_USER+3)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Um alça para o contexto do dispositivo para a página de exemplo.

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma [**estrutura RECT**](/previous-versions//dd162897(v=vs.85)) que contém as coordenadas, em pixels, do retângulo de margem.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se o procedimento de gancho retornar **TRUE**, a caixa de diálogo não desenhará o retângulo de margem na página de exemplo.

Se o procedimento de gancho retornar **FALSE**, a caixa de diálogo desenhará o retângulo de margem na página de exemplo.

## <a name="remarks"></a>Comentários

A **caixa de diálogo** Configuração de Página inclui uma imagem de uma página de exemplo que mostra como as seleções do usuário afetam a aparência da saída impressa. Ao chamar a [**função PageSetupDlg,**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) você pode fornecer um procedimento de gancho [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) para personalizar a aparência da página de exemplo. Sempre que a caixa de diálogo estiver prestes a desenhar o conteúdo da página de exemplo, a caixa de diálogo enviará uma sequência de mensagens para o procedimento de gancho.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Commdlg.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook)
</dt> <dt>

[**Pagesetupdlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85))
</dt> <dt>

[**WM \_ PSD \_ PAGESETUPDLG**](wm-psd-pagesetupdlg.md)
</dt> <dt>

**Conceitual**
</dt> <dt>

[Biblioteca de caixas de diálogo comuns](common-dialog-box-library.md)
</dt> </dl>

 

