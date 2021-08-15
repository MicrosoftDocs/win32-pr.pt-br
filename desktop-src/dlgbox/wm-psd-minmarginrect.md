---
title: WM_PSD_MINMARGINRECT mensagem (Commdlg.h)
description: Notifica um procedimento de gancho PagePaintHook das coordenadas do retângulo de margem na página de exemplo. Uma caixa de diálogo Configuração de Página envia essa mensagem quando ela está prestes a desenhar o conteúdo da página de exemplo.
ms.assetid: 14977b52-7a6f-4c55-956a-716398a71613
keywords:
- WM_PSD_MINMARGINRECT caixa de diálogo da mensagem
topic_type:
- apiref
api_name:
- WM_PSD_MINMARGINRECT
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10557e3fc605fc86b1cfa1c7b44fd1e4d40ac399476c5b2c573f46db5c4103b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118503311"
---
# <a name="wm_psd_minmarginrect-message"></a>Mensagem WM \_ PSD \_ MINMARGINRECT

Notifica um procedimento [*de gancho PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) das coordenadas do retângulo de margem na página de exemplo. Uma **caixa de diálogo** Configuração de Página envia essa mensagem quando ela está prestes a desenhar o conteúdo da página de exemplo.


```C++
#define WM_USER                  0x0400
#define WM_PSD_MINMARGINRECT    (WM_USER+2)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Um alça para o contexto do dispositivo para a página de exemplo.

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma [**estrutura RECT**](/previous-versions//dd162897(v=vs.85)) que contém as coordenadas, em pixels, do retângulo de margem mínima.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se o procedimento de gancho retornar **TRUE**, a caixa de diálogo não enviará mais mensagens e não desenhará na página de exemplo até a próxima vez que o sistema precisar redesenhar a página de exemplo.

Se o procedimento de gancho retornar **FALSE**, a caixa de diálogo enviará as mensagens restantes da sequência de desenho.

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

 

