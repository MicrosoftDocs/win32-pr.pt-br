---
title: Mensagem de LVM_ENABLEGROUPVIEW (commctrl. h)
description: Habilita ou desabilita se os itens em um controle de exibição de lista são exibidos como um grupo.
ms.assetid: 783a5e23-d1cb-4523-a6d2-b2cf93fa7f62
keywords:
- Controles de LVM_ENABLEGROUPVIEW de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_ENABLEGROUPVIEW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1d546e1236fa4f0800c0353810beb5b427ba4fb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008872"
---
# <a name="lvm_enablegroupview-message"></a>\_Mensagem ENABLEGROUPVIEW LVM

Habilita ou desabilita se os itens em um controle de exibição de lista são exibidos como um grupo.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Um **bool** que indica se um controle de exibição de lista deve ser habilitado para agrupar itens exibidos. Use **true** para habilitar o agrupamento, **false** para desabilitá-lo. </dd> <dt>

*lParam* 
</dt> <dd>Deve ser **NULL**.</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um dos valores a seguir.



| Código de retorno                                                                       | Descrição                                                                                  |
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <dt>**0**</dt> </dl>  | A capacidade de exibir itens de exibição de lista como um grupo já está habilitada ou desabilitada.<br/> |
| <dl> <dt>**1**</dt> </dl>  | O estado do controle foi alterado com êxito.<br/>                                |
| <dl> <dt>**-1**</dt> </dl> | Falha na operação.<br/>                                                             |



 

## <a name="remarks"></a>Comentários

**LVM \_** Não há suporte para ENABLEGROUPVIEW no estilo [**LVS \_ OWNERDATA**](list-view-window-styles.md) .

> [!Note]  
> Para usar essa mensagem, você deve fornecer um manifesto especificando Comclt32.dll versão 6,0. Para obter mais informações sobre manifestos, consulte [habilitando estilos visuais](cookbook-overview.md).

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





