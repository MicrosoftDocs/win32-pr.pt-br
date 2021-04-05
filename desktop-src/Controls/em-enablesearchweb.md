---
title: Mensagem de EM_ENABLESEARCHWEB (CommCtrl. h)
description: Habilita ou desabilita o recurso "Pesquisar na Web" e a entrada do menu de contexto.
ms.assetid: 9393f03e-0719-458b-8122-616df738c417
keywords:
- Controles de EM_ENABLESEARCHWEB de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_ENABLESEARCHWEB
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fdb2638476027f0a7fe2bb1a66a3a00a330e28c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918707"
---
# <a name="em_enablesearchweb-message"></a>\_Mensagem em ENABLESEARCHWEB

Habilita ou desabilita o recurso "Pesquisar na Web" e a entrada do menu de contexto.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Um valor **true** indica que o recurso "Pesquisar na Web" está habilitado e um valor **false** indica que ele está desabilitado.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa mensagem não retorna um valor.

## <a name="remarks"></a>Comentários

Se você desabilitar "Pesquisar na Web" usando essa mensagem, a mensagem em [**\_ SEARCHWEB**](em-searchweb.md) não terá nenhum efeito.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 10, 1809\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2019\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>CommCtrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**em \_ SEARCHWEB**](em-searchweb.md)
</dt> </dl>

 

 





