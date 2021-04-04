---
title: Mensagem de LVM_SETOUTLINECOLOR (commctrl. h)
description: Define a cor da borda de um controle de exibição de lista se o \_ estilo de \_ janela estendida LVS ex BORDERSELECT for definido.
ms.assetid: c2b606fa-8d47-4192-94b7-d01c3cfdc514
keywords:
- Controles de LVM_SETOUTLINECOLOR de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_SETOUTLINECOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 776cb13479e4d091d394941844691c117a4ebbef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824167"
---
# <a name="lvm_setoutlinecolor-message"></a>\_Mensagem SETOUTLINECOLOR LVM

Define a cor da borda de um controle de exibição de lista se o estilo de janela estendida [**LVS \_ ex \_ BORDERSELECT**](extended-list-view-styles.md) for definido.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Estrutura **COLORREF** que especifica a cor para definir a borda.</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna a estrutura **COLORREF** que contém a cor da estrutura de tópicos.

## <a name="remarks"></a>Comentários

> [!Note]  
> Para usar essa mensagem, você deve fornecer um manifesto especificando Comclt32.dll versão 6,0. Para obter mais informações sobre manifestos, consulte [habilitando estilos visuais](cookbook-overview.md).

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





