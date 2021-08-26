---
title: LVM_SETCOLUMNWIDTH mensagem (Commctrl.h)
description: Altera a largura de uma coluna no modo de exibição de relatório ou a largura de todas as colunas no modo de exibição de lista. Você pode enviar essa mensagem explicitamente ou usar a \_ macro ListView SetColumnWidth.
ms.assetid: 309aebfb-9fed-4c77-acbb-ea905b32b0e2
keywords:
- LVM_SETCOLUMNWIDTH controles de Windows mensagem
topic_type:
- apiref
api_name:
- LVM_SETCOLUMNWIDTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a127706d6a47444ee59f1434478aadb5170f9ac7a919dca6fd6151de33486d0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120077286"
---
# <a name="lvm_setcolumnwidth-message"></a>Mensagem LVM \_ SETCOLUMNWIDTH

Altera a largura de uma coluna no modo de exibição de relatório ou a largura de todas as colunas no modo de exibição de lista. Você pode enviar essa mensagem explicitamente ou usar a macro [**\_ ListView SetColumnWidth.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setcolumnwidth)

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice baseado em zero de uma coluna válida. Para o modo de exibição de lista, esse parâmetro deve ser definido como zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Nova largura da coluna, em pixels. Para o modo de exibição de relatório, há suporte para os seguintes valores especiais:



| Valor                                                                                                                                                                                           | Significado                                                                                                                                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LVSCW_AUTOSIZE"></span><span id="lvscw_autosize"></span><dl> <dt>**LVSCW \_ AUTOSIZE**</dt> </dl>                                | Tamanhos automáticos da coluna.<br/>                                                                                                                                           |
| <span id="LVSCW_AUTOSIZE_USEHEADER"></span><span id="lvscw_autosize_useheader"></span><dl> <dt>**LVSCW \_ AUTOSIZE \_ USEHEADER**</dt> </dl> | Tamanhos automáticos da coluna para ajustar o texto do header. Se você usar esse valor com a última coluna, sua largura será definida para preencher a largura restante do controle de exibição de lista.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna **TRUE se** for bem-sucedido ou FALSE **caso** contrário.

## <a name="remarks"></a>Comentários

Suponha que você tenha um controle de exibição de lista de 2 colunas com uma largura de 500 pixels. Se a largura da coluna zero for definida como 200 pixels e você enviar essa mensagem com *wParam* = 1 e *lParam* = LVSCW \_ AUTOSIZE USEHEADER, a segunda (e última) coluna terá \_ 300 pixels de largura.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





