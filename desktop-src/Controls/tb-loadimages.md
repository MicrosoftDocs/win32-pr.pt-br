---
title: TB_LOADIMAGES mensagem (Commctrl.h)
description: Carrega imagens de botão definidas pelo sistema na lista de imagens de um controle de barra de ferramentas.
ms.assetid: 61146f43-9fd9-4fe3-b85c-cf465f2de769
keywords:
- TB_LOADIMAGES controles de Windows mensagem
topic_type:
- apiref
api_name:
- TB_LOADIMAGES
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df2cfae5e1658dec2652eb68cae4283dd0df697ad055434f1290cc0da7c2b485
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118168192"
---
# <a name="tb_loadimages-message"></a>Mensagem \_ LOADIMAGES de TB

Carrega imagens de botão definidas pelo sistema na lista de imagens de um controle de barra de ferramentas.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador de uma lista de imagens de botão definida pelo sistema. Esse parâmetro pode ser definido como um dos valores a seguir.



| Valor                                                                                                                                                                                | Significado                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span id="IDB_HIST_LARGE_COLOR"></span><span id="idb_hist_large_color"></span><dl> <dt>**COR GRANDE \_ DO HIST \_ DO IDB \_**</dt> </dl> | Windows Bitmaps do Explorer em grande tamanho.<br/>                                  |
| <span id="IDB_HIST_SMALL_COLOR"></span><span id="idb_hist_small_color"></span><dl> <dt>**COR PEQUENA \_ DO HIST \_ DO IDB \_**</dt> </dl> | Windows Bitmaps do Explorer em tamanho pequeno.<br/>                                  |
| <span id="IDB_STD_LARGE_COLOR"></span><span id="idb_std_large_color"></span><dl> <dt>**COR GRANDE \_ DO STD \_ do \_ IDB**</dt> </dl>    | Bitmaps padrão em grande tamanho.<br/>                                          |
| <span id="IDB_STD_SMALL_COLOR"></span><span id="idb_std_small_color"></span><dl> <dt>**COR PEQUENA \_ DO STD \_ do \_ IDB**</dt> </dl>    | Bitmaps padrão em tamanho pequeno.<br/>                                          |
| <span id="IDB_VIEW_LARGE_COLOR"></span><span id="idb_view_large_color"></span><dl> <dt>**COR GRANDE \_ DA \_ EXIBIÇÃO DO IDB \_**</dt> </dl> | Exibir bitmaps em grande tamanho.<br/>                                              |
| <span id="IDB_VIEW_SMALL_COLOR"></span><span id="idb_view_small_color"></span><dl> <dt>**COR PEQUENA \_ DA \_ EXIBIÇÃO DO IDB \_**</dt> </dl> | Exibir bitmaps em tamanho pequeno.<br/>                                              |
| <span id="IDB_HIST_NORMAL"></span><span id="idb_hist_normal"></span><dl> <dt>**IDB \_ HIST \_ NORMAL**</dt> </dl>                 | Windows Botões de viagem do Explorer e bitmaps favoritos em estado normal.<br/>   |
| <span id="IDB_HIST_HOT"></span><span id="idb_hist_hot"></span><dl> <dt>**IDB \_ HIST \_ HOT**</dt> </dl>                          | Windows Botões de viagem do Explorer e bitmaps favoritos em estado quente.<br/>      |
| <span id="IDB_HIST_DISABLED"></span><span id="idb_hist_disabled"></span><dl> <dt>**HIST DO IDB \_ \_ DESABILITADO**</dt> </dl>           | Windows Botões de viagem do Explorer e bitmaps favoritos no estado desabilitado.<br/> |
| <span id="IDB_HIST_PRESSED"></span><span id="idb_hist_pressed"></span><dl> <dt>**HIST DO IDB \_ \_ PRESSIONADO**</dt> </dl>              | Windows Botões de viagem do Explorer e bitmaps favoritos no estado pressionado.<br/>  |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Alça de instância. Esse parâmetro deve ser definido como HINST \_ COMMCTRL.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

A contagem de imagens na lista de imagens. Retornará zero se a barra de ferramentas não tiver nenhuma lista de imagens ou se a lista de imagens existente estiver vazia.

## <a name="remarks"></a>Comentários

Você deve usar os valores de índice de imagem adequados ao preparar estruturas [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) antes de enviar a mensagem [**\_ ADDBUTTONS**](tb-addbuttons.md) de TB. Para ver uma lista de valores de índice de imagem para esses bitmaps predefinidos, consulte Valores de índice de imagem de botão padrão da barra de [ferramentas](toolbar-standard-button-image-index-values.md).

## <a name="examples"></a>Exemplos

O código de exemplo a seguir carrega as imagens de cor pequenas padrão do sistema.


```C++
// hWndToobar is the window handle of the toolbar control.
SendMessage(hWndToolbar, TB_LOADIMAGES, (WPARAM)IDB_STD_SMALL_COLOR, (LPARAM)HINST_COMMCTRL);
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**TB \_ ADDBITMAP**](tb-addbitmap.md)
</dt> </dl>

 

 





