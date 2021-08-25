---
title: EM_EXLINEFROMCHAR mensagem (Richedit.h)
description: Determina qual linha contém o caractere especificado em um controle de edição rico.
ms.assetid: 497482fb-9640-4063-a9f5-e0691b65225d
keywords:
- EM_EXLINEFROMCHAR controles de Windows mensagem
topic_type:
- apiref
api_name:
- EM_EXLINEFROMCHAR
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c41f5fbe540a4d765a48292d4ffd5b4af5849681dd1a82f4512b79348a6249d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119915636"
---
# <a name="em_exlinefromchar-message"></a>Mensagem EM \_ EXLINEFROMCHAR

Determina qual linha contém o caractere especificado em um controle de edição rico.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Esse parâmetro não é usado; ele deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Índice baseado em zero do caractere.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Essa mensagem retorna o índice baseado em zero da linha.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



 

 





