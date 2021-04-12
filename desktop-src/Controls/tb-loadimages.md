---
title: Mensagem de TB_LOADIMAGES (commctrl. h)
description: Carrega imagens de botão definidas pelo sistema em uma lista de imagens de controle da barra de ferramentas.
ms.assetid: 61146f43-9fd9-4fe3-b85c-cf465f2de769
keywords:
- Controles de TB_LOADIMAGES de mensagens do Windows
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
ms.openlocfilehash: b0b0ba6bf75855a0b81ac56438489d7eced3d589
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455604"
---
# <a name="tb_loadimages-message"></a>\_Mensagem de LOADimages TB

Carrega imagens de botão definidas pelo sistema em uma lista de imagens de controle da barra de ferramentas.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador de uma lista de imagens de botões definida pelo sistema. Esse parâmetro pode ser definido como um dos valores a seguir.



| Valor                                                                                                                                                                                | Significado                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span id="IDB_HIST_LARGE_COLOR"></span><span id="idb_hist_large_color"></span><dl> <dt>**\_ \_ cor grande do sua de idb \_**</dt> </dl> | Bitmaps do Windows Explorer em tamanho grande.<br/>                                  |
| <span id="IDB_HIST_SMALL_COLOR"></span><span id="idb_hist_small_color"></span><dl> <dt>**\_ \_ cor pequena do sua de idb \_**</dt> </dl> | Bitmaps do Windows Explorer em tamanho pequeno.<br/>                                  |
| <span id="IDB_STD_LARGE_COLOR"></span><span id="idb_std_large_color"></span><dl> <dt>**\_ \_ cor grande do idb padrão \_**</dt> </dl>    | Bitmaps padrão em tamanho grande.<br/>                                          |
| <span id="IDB_STD_SMALL_COLOR"></span><span id="idb_std_small_color"></span><dl> <dt>**cor do IDB \_ std \_ Small \_**</dt> </dl>    | Bitmaps padrão em tamanho pequeno.<br/>                                          |
| <span id="IDB_VIEW_LARGE_COLOR"></span><span id="idb_view_large_color"></span><dl> <dt>**\_ \_ cor grande de exibição de idb \_**</dt> </dl> | Exibir bitmaps em tamanho grande.<br/>                                              |
| <span id="IDB_VIEW_SMALL_COLOR"></span><span id="idb_view_small_color"></span><dl> <dt>**\_ \_ cor pequena da exibição idb \_**</dt> </dl> | Exibir bitmaps em tamanho pequeno.<br/>                                              |
| <span id="IDB_HIST_NORMAL"></span><span id="idb_hist_normal"></span><dl> <dt>**sua de IDB \_ \_ normal**</dt> </dl>                 | Os botões de viagem do Windows Explorer e os bitmaps de favoritos em estado normal.<br/>   |
| <span id="IDB_HIST_HOT"></span><span id="idb_hist_hot"></span><dl> <dt>**sua de IDB \_ \_**</dt> </dl>                          | Os botões de viagem do Windows Explorer e os bitmaps de favoritos estão em estado ativo.<br/>      |
| <span id="IDB_HIST_DISABLED"></span><span id="idb_hist_disabled"></span><dl> <dt>**sua de IDB \_ \_ desabilitado**</dt> </dl>           | Os botões de viagem do Windows Explorer e os bitmaps de favoritos no estado desabilitado.<br/> |
| <span id="IDB_HIST_PRESSED"></span><span id="idb_hist_pressed"></span><dl> <dt>**sua de IDB \_ \_ pressionado**</dt> </dl>              | Os botões de viagem do Windows Explorer e os bitmaps de favoritos no estado pressionado.<br/>  |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador de instância. Esse parâmetro deve ser definido como HINST \_ COMMCTRL.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

A contagem de imagens na lista de imagens. Retornará zero se a barra de ferramentas não tiver nenhuma lista de imagens ou se a lista de imagens existente estiver vazia.

## <a name="remarks"></a>Comentários

Você deve usar os valores de índice de imagem apropriados ao preparar estruturas [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) antes de enviar a mensagem de [**\_ hiperbotãos de TB**](tb-addbuttons.md) . Para obter uma lista de valores de índice de imagem para esses bitmaps predefinidos, consulte [valores de índice de imagem de botão padrão da barra de ferramentas](toolbar-standard-button-image-index-values.md).

## <a name="examples"></a>Exemplos

O código de exemplo a seguir carrega as imagens de cores pequenas do sistema padrão.


```C++
// hWndToobar is the window handle of the toolbar control.
SendMessage(hWndToolbar, TB_LOADIMAGES, (WPARAM)IDB_STD_SMALL_COLOR, (LPARAM)HINST_COMMCTRL);
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**rebitmap de TB \_**](tb-addbitmap.md)
</dt> </dl>

 

 





