---
description: Cancela o registro de um AppBar removendo-o da lista interna do sistema. O sistema não envia mais mensagens de notificação para o AppBar ou impede que outros aplicativos usem a área de tela usada pelo AppBar.
title: Mensagem de ABM_REMOVE (shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 3da73a52-3dbb-4133-a9bd-86540e1c4154
api_name:
- ABM_REMOVE
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: c32fd2c7a12fc8146a01d3722b31b46bad01f61b526397806a5121b7381b069e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117861703"
---
# <a name="abm_remove-message"></a>ABM \_ remover mensagem

Cancela o registro de um AppBar removendo-o da lista interna do sistema. O sistema não envia mais mensagens de notificação para o AppBar ou impede que outros aplicativos usem a área de tela usada pelo AppBar.


```C++
                SHAppBarMessage(ABM_REMOVE, pabd); 
            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pabd* 
</dt> <dd>

Um ponteiro para uma estrutura [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) que contém o identificador para o AppBar para cancelar o registro. Você deve especificar os membros **cbSize** e **HWND** ao enviar esta mensagem; todos os outros membros são ignorados.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Sempre retorna **true**.

## <a name="remarks"></a>Comentários

Essa mensagem faz com que o sistema envie a mensagem de notificação do [**ABN \_ POSCHANGED**](abn-poschanged.md) para todos os appbars.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho XP\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Shellapi. h</dt> </dl> |



 

 




