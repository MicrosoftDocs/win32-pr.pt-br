---
title: Mensagem de WM_PSD_PAGESETUPDLG (Commdlg. h)
description: Notifica um procedimento de gancho PagePaintHook que a caixa de diálogo Configurar página está prestes a desenhar o conteúdo da página de exemplo. O procedimento de gancho pode usar essa mensagem para realizar tarefas de inicialização relacionadas ao desenho do conteúdo da página de exemplo.
ms.assetid: 0d95240b-7d77-4819-8e5c-cc25cd1b30f2
keywords:
- Caixas de diálogo de WM_PSD_PAGESETUPDLG mensagem
topic_type:
- apiref
api_name:
- WM_PSD_PAGESETUPDLG
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9706eff6d015dc31332d9f757c954081f0134b2b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369892"
---
# <a name="wm_psd_pagesetupdlg-message"></a>\_Mensagem PAGESETUPDLG do PSD do WM \_

Notifica um procedimento de gancho [**PagePaintHook**](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) que a caixa de diálogo **Configurar página** está prestes a desenhar o conteúdo da página de exemplo. O procedimento de gancho pode usar essa mensagem para realizar tarefas de inicialização relacionadas ao desenho do conteúdo da página de exemplo.


```C++
#define WM_USER                  0x0400
#define WM_PSD_PAGESETUPDLG     (WM_USER  )
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

A palavra de ordem inferior Especifica um valor que indica o tamanho do papel. Esse valor pode ser um dos valores **de \_ DMPAPER** listados na descrição da estrutura. A palavra de ordem superior especifica a orientação do papel ou do envelope e se a impressora é uma matriz de pontos ou HPPCL (linguagem de controle de impressora da Hewlett Packard). Esse parâmetro pode usar um dos valores a seguir.



| Valor                                                                             | Significado                                            |
|-----------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <dt>0x0001</dt> </dl> | Papel no modo paisagem (matriz de pontos)<br/>    |
| <dl> <dt>0x0003</dt> </dl> | Papel no modo paisagem (HPPCL)<br/>         |
| <dl> <dt>0x0005</dt> </dl> | Papel no modo retrato (matriz de pontos)<br/>     |
| <dl> <dt>0x0007</dt> </dl> | Papel no modo retrato (HPPCL)<br/>          |
| <dl> <dt>0x000b</dt> </dl> | Envelope no modo paisagem (HPPCL)<br/>      |
| <dl> <dt>0x000d</dt> </dl> | Envelope no modo retrato (matriz de pontos)<br/>  |
| <dl> <dt>0x0019</dt> </dl> | Envelope no modo paisagem (matriz de pontos)<br/> |
| <dl> <dt>0x001F</dt> </dl> | Envelope no modo retrato (HPPCL)<br/>       |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma estrutura [**PAGESETUPDLG**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga) que contém informações usadas para inicializar a caixa de diálogo **Configurar página** .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se o procedimento de gancho retornar **true**, a caixa de diálogo não enviará mais mensagens e não desenhará na página de exemplo até a próxima vez que o sistema precisar redesenhar a página de exemplo.

Se o procedimento de gancho retornar **false**, a caixa de diálogo enviará as mensagens restantes da sequência de desenho.

## <a name="remarks"></a>Comentários

A caixa de diálogo **Configurar página** inclui uma imagem de uma página de exemplo que mostra como as seleções do usuário afetam a aparência da saída impressa. Ao chamar a função [**PAGESETUPDLG**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) , você pode fornecer um procedimento de gancho de [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) para personalizar a aparência da página de exemplo. Sempre que a caixa de diálogo estiver prestes a desenhar o conteúdo da página de exemplo, a caixa de diálogo enviará uma sequência de mensagens para o procedimento de gancho.

As três primeiras mensagens de uma sequência de desenho (**WM \_ PSD \_ PAGESETUPDLG**, [**WM \_ PSD \_ FULLPAGERECT**](wm-psd-fullpagerect.md)ou [**WM \_ PSD \_ MINMARGINRECT**](wm-psd-minmarginrect.md)) fornecem informações que o procedimento de gancho pode usar para desenhar o conteúdo da página de exemplo. As mensagens restantes ([**WM \_ PSD \_ MARGINRECT**](wm-psd-marginrect.md), [**WM \_ PSD \_ GREEKTEXTRECT**](wm-psd-greektextrect.md), [**WM \_ PSD \_ ENVSTAMPRECT**](wm-psd-envstamprect.md), [**WM \_ PSD \_ YAFULLPAGERECT**](wm-psd-yafullpagerect.md)) notificam o procedimento de gancho que a caixa de diálogo está prestes a desenhar uma parte específica da página de exemplo. Isso permite que o procedimento de conexão desenhe partes da página de exemplo de forma seletiva.

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

[**PAGESETUPDLG**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga)
</dt> <dt>

[**\_ENVSTAMPRECT de PSD do WM \_**](wm-psd-envstamprect.md)
</dt> <dt>

[**\_FULLPAGERECT de PSD do WM \_**](wm-psd-fullpagerect.md)
</dt> <dt>

[**\_GREEKTEXTRECT de PSD do WM \_**](wm-psd-greektextrect.md)
</dt> <dt>

[**\_MARGINRECT de PSD do WM \_**](wm-psd-marginrect.md)
</dt> <dt>

[**\_MINMARGINRECT de PSD do WM \_**](wm-psd-minmarginrect.md)
</dt> <dt>

[**\_YAFULLPAGERECT de PSD do WM \_**](wm-psd-yafullpagerect.md)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Biblioteca de caixa de diálogo comum](common-dialog-box-library.md)
</dt> </dl>

 

