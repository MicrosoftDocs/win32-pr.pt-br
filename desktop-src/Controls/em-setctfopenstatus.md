---
title: Mensagem de EM_SETCTFOPENSTATUS (RichEdit. h)
description: Abre ou fecha o teclado do TSF (estrutura de serviços de texto).
ms.assetid: 9bdabf5a-93db-4b0e-9528-807d262de866
keywords:
- Controles de EM_SETCTFOPENSTATUS de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_SETCTFOPENSTATUS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf4163a415f129dfc5d3f98aa06578d13bb462e5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009659"
---
# <a name="em_setctfopenstatus-message"></a>\_Mensagem em SETCTFOPENSTATUS

Abre ou fecha o teclado do TSF (estrutura de serviços de texto).

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Para ativar o teclado TSF, use **true**. Para desligar o teclado TSF, use **false**.

</dd> <dt>

*lParam* 
</dt> <dd>

Não usado; deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se for bem-sucedida, essa mensagem retornará **true**. Se não for bem-sucedida, essa mensagem retornará **false**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP com SP1\]<br/>                                  |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**em \_ GETCTFOPENSTATUS**](em-getctfopenstatus.md)
</dt> </dl>

 

 





