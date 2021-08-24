---
title: Mensagem de WM_PSD_GREEKTEXTRECT (Commdlg. h)
description: Notifica o procedimento de gancho de uma caixa de diálogo de configuração de página, PagePaintHook, que a caixa de diálogo está prestes a desenhar o texto grego dentro do retângulo de margem da página de exemplo.
ms.assetid: ad0a200d-5626-4768-b3bd-73d4e3f0d548
keywords:
- Caixas de diálogo de WM_PSD_GREEKTEXTRECT mensagem
topic_type:
- apiref
api_name:
- WM_PSD_GREEKTEXTRECT
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c30e4873255a59a86da91b3145d0675f6940ce35081273696ce6c68b70a1560
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119726046"
---
# <a name="wm_psd_greektextrect-message"></a>\_Mensagem GREEKTEXTRECT do PSD do WM \_

Notifica o procedimento de gancho de uma caixa de diálogo de **configuração de página** , [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook), que a caixa de diálogo está prestes a desenhar o texto grego dentro do retângulo de margem da página de exemplo.


```C++
#define WM_USER                  0x0400
#define WM_PSD_GREEKTEXTRECT    (WM_USER+4)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Um identificador para o contexto do dispositivo para a página de exemplo.

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma estrutura [**Rect**](/previous-versions//dd162897(v=vs.85)) que contém as coordenadas, em pixels, do retângulo de texto grego.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se o procedimento de gancho retornar **true**, a caixa de diálogo não desenhará a parte do texto grego da página de exemplo.

Se o procedimento de gancho retornar **false**, a caixa de diálogo desenhará a parte do texto grego da página de exemplo.

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

 

