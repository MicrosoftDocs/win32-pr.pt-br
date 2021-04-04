---
title: Mensagem de LVM_GETOUTLINECOLOR (commctrl. h)
description: Recupera a cor da borda de um controle de exibição de lista se o \_ estilo de \_ janela estendida LVS ex BORDERSELECT for definido.
ms.assetid: cc9d69d1-1470-4eaa-8d54-e31b796cf685
keywords:
- Controles de LVM_GETOUTLINECOLOR de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_GETOUTLINECOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 489f21f2f6d4dcca2c79d92a13a85d7718a85693
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824669"
---
# <a name="lvm_getoutlinecolor-message"></a>\_Mensagem GETOUTLINECOLOR LVM

Recupera a cor da borda de um controle de exibição de lista se o estilo de janela estendida [**LVS \_ ex \_ BORDERSELECT**](extended-list-view-styles.md) for definido.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna uma estrutura **COLORREF** que contém a cor da borda de um controle de exibição de lista.

## <a name="remarks"></a>Comentários

> [!Note]  
> Para usar essa mensagem, você deve fornecer um manifesto especificando Comclt32.dll versão 6,0. Para obter mais informações sobre manifestos, consulte [habilitando estilos visuais](cookbook-overview.md).

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





