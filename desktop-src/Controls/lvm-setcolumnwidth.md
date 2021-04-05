---
title: Mensagem de LVM_SETCOLUMNWIDTH (commctrl. h)
description: Altera a largura de uma coluna no modo de exibição de relatório ou a largura de todas as colunas no modo de exibição de lista. Você pode enviar essa mensagem explicitamente ou usar a \_ macro SetColumnWidth do ListView.
ms.assetid: 309aebfb-9fed-4c77-acbb-ea905b32b0e2
keywords:
- Controles de LVM_SETCOLUMNWIDTH de mensagens do Windows
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
ms.openlocfilehash: 529e989b3d66562acc7b6f91c3b3b06527235e8e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085169"
---
# <a name="lvm_setcolumnwidth-message"></a>\_Mensagem SETCOLUMNWIDTH LVM

Altera a largura de uma coluna no modo de exibição de relatório ou a largura de todas as colunas no modo de exibição de lista. Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ SetColumnWidth do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setcolumnwidth) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de base zero de uma coluna válida. Para o modo de exibição de lista, esse parâmetro deve ser definido como zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Nova largura da coluna, em pixels. Para o modo de exibição de relatório, há suporte para os seguintes valores especiais:



| Valor                                                                                                                                                                                           | Significado                                                                                                                                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LVSCW_AUTOSIZE"></span><span id="lvscw_autosize"></span><dl> <dt>**\_dimensionamento automático de LVSCW**</dt> </dl>                                | Dimensiona automaticamente a coluna.<br/>                                                                                                                                           |
| <span id="LVSCW_AUTOSIZE_USEHEADER"></span><span id="lvscw_autosize_useheader"></span><dl> <dt>**LVSCW \_ AUTOSIZE \_ USEHEADER**</dt> </dl> | Dimensiona automaticamente a coluna para caber no texto do cabeçalho. Se você usar esse valor com a última coluna, sua largura será definida para preencher a largura restante do controle de exibição de lista.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.

## <a name="remarks"></a>Comentários

Suponha que você tenha um controle de exibição de lista de duas colunas com uma largura de 500 pixels. Se a largura da coluna zero for definida como 200 pixels e você enviar essa mensagem com *wParam* = 1 e *lParam* = LVSCW \_ AUTOSIZE \_ USEHEADER, a segunda (e última) coluna terá 300 pixels de largura.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





