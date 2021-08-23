---
title: WM_PSD_YAFULLPAGERECT mensagem (Commdlg.h)
description: Notifica o procedimento de gancho de uma caixa de diálogo Configuração de Página, PagePaintHook, de que a caixa de diálogo está prestes a desenhar a parte de endereço de retorno de uma página de exemplo de envelope.
ms.assetid: 1f6aea69-a1bd-41ea-b508-44b4f5c38757
keywords:
- WM_PSD_YAFULLPAGERECT caixa de diálogo da mensagem
topic_type:
- apiref
api_name:
- WM_PSD_YAFULLPAGERECT
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62cfbd187cb3db5a27579b428c352be1da1a4bdf91f3336ed41511fe59d75d23
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119787356"
---
# <a name="wm_psd_yafullpagerect-message"></a>Mensagem WM \_ PSD \_ YAFULLPAGERECT

Notifica o procedimento de gancho de uma caixa de diálogo Configuração de Página, [*PagePaintHook,*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook)que **a** caixa de diálogo está prestes a desenhar a parte de endereço de retorno de uma página de exemplo de envelope.


```C++
#define WM_USER                  0x0400
#define WM_PSD_YAFULLPAGERECT   (WM_USER+6)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Um alça para o contexto do dispositivo para a página de exemplo.

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma [**estrutura RECT**](/previous-versions//dd162897(v=vs.85)) que contém as coordenadas, em pixels, da página de exemplo.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se o procedimento de gancho retornar **TRUE,** a caixa de diálogo não desenhará a parte de endereço de retorno de uma página de exemplo de envelope.

Se o procedimento de gancho retornar **FALSE,** a caixa de diálogo desenhará a parte de endereço de retorno de uma página de exemplo de envelope.

Se o tipo de papel não for um envelope, o valor de retorno não terá nenhum efeito.

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

 

