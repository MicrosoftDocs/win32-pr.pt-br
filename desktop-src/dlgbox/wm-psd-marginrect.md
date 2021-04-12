---
title: Mensagem de WM_PSD_MARGINRECT (Commdlg. h)
description: Notifica o procedimento de gancho de uma caixa de diálogo de configuração de página, PagePaintHook, que a caixa de diálogo está prestes a desenhar o retângulo de margem da página de exemplo.
ms.assetid: 81c057ab-6faf-4dd8-8b0c-34a2753e572c
keywords:
- Caixas de diálogo de WM_PSD_MARGINRECT mensagem
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
ms.openlocfilehash: 4718cfbe16db53378544d9fca0ab44ade23ffb3f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455563"
---
# <a name="wm_psd_marginrect-message"></a>\_Mensagem MARGINRECT do PSD do WM \_

Notifica o procedimento de gancho de uma caixa de diálogo de **configuração de página** , [**PagePaintHook**](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook), que a caixa de diálogo está prestes a desenhar o retângulo de margem da página de exemplo.


```C++
#define WM_USER                  0x0400
#define WM_PSD_MARGINRECT       (WM_USER+3)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Um identificador para o contexto do dispositivo para a página de exemplo.

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma estrutura [**Rect**](/previous-versions//dd162897(v=vs.85)) que contém as coordenadas, em pixels, do retângulo da margem.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se o procedimento de gancho retornar **true**, a caixa de diálogo não desenhará o retângulo de margem na página de exemplo.

Se o procedimento de gancho retornar **false**, a caixa de diálogo desenhará o retângulo de margem na página de exemplo.

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

 

