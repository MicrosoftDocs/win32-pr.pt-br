---
title: Mensagem de LVM_GETSUBITEMRECT (commctrl. h)
description: Recupera informações sobre o retângulo delimitador de um subitem em um controle de exibição de lista.
ms.assetid: 985876b2-6eb3-4c96-88ea-ddec67ef5b5a
keywords:
- Controles de LVM_GETSUBITEMRECT de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_GETSUBITEMRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd1184c52d60b86e008685b87c9f5555cf801b35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086159"
---
# <a name="lvm_getsubitemrect-message"></a>\_Mensagem GETSUBITEMRECT LVM

Recupera informações sobre o retângulo delimitador de um subitem em um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usando a macro [**ListView \_ GetSubItemRect**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getsubitemrect) (recomendado). Esta mensagem destina-se a ser usada somente com controles de exibição de lista que usam o estilo de [**\_ relatório LVS**](list-view-window-styles.md) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice do item pai do subitem.

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**Rect**](/previous-versions//dd162897(v=vs.85)) que receberá as informações de retângulo delimitador de subitem. Seus membros devem ser inicializados de acordo com as seguintes relações de membro/valor:



| Valor                                                                                                                             | Significado                                                                                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span id="top"></span><span id="TOP"></span><dl> <dt>**Início**</dt> </dl>    | O índice baseado em um do subitem.<br/>                                                                                    |
| <span id="left"></span><span id="LEFT"></span><dl> <dt>**mantida**</dt> </dl> | Valor do sinalizador (consulte comentários). Indica a parte do subitem de exibição de lista para o qual recuperar o retângulo delimitador.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornará zero se for bem-sucedido ou nenhum outro.

## <a name="remarks"></a>Comentários

A seguir estão os valores de sinalizador que podem ser definidos.



| Requisito | Valor |
|----------------|---------------------------------------------------------------------------------------------------------------------|
| **Valor de sinalizador** | **Significado**                                                                                                         |
| limites do LVIR \_   | Retorna o retângulo delimitador do item inteiro, incluindo o ícone e o rótulo.                                    |
| ícone de LVIR \_     | Retorna o retângulo delimitador do ícone ou ícone pequeno.                                                           |
| rótulo de LVIR \_    | Retorna o retângulo delimitador do item inteiro, incluindo o ícone e o rótulo. Isso é idêntico aos limites de LVIR \_ . |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

