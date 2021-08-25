---
title: Mensagem de LVM_GETINSERTMARKRECT (commctrl. h)
description: Recupera o retângulo que limita o ponto de inserção.
ms.assetid: 7b10229c-73ab-426c-8a8a-71258a33e248
keywords:
- controles de Windows de mensagem de LVM_GETINSERTMARKRECT
topic_type:
- apiref
api_name:
- LVM_GETINSERTMARKRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5832ce185a579432b341482847400e96d60869a64d3ff0a2cd599e2eecf6b20
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062596"
---
# <a name="lvm_getinsertmarkrect-message"></a>\_Mensagem GETINSERTMARKRECT LVM

Recupera o retângulo que limita o ponto de inserção.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Não usado; deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Ponteiro para uma estrutura <a href="/previous-versions//dd162897(v=vs.85)">**Rect**</a> que contém as coordenadas de um retângulo que limita o ponto de inserção.</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um dos valores a seguir.



| Código de retorno                                                                      | Descrição                          |
|----------------------------------------------------------------------------------|--------------------------------------|
| <dl> <dt>**0**</dt> </dl> | Nenhum ponto de inserção encontrado.<br/> |
| <dl> <dt>**1**</dt> </dl> | Ponto de inserção encontrado.<br/>    |



 

## <a name="remarks"></a>Comentários

> [!Note]  
> Para usar essa mensagem, você deve fornecer um manifesto especificando Comclt32.dll versão 6,0. Para obter mais informações sobre manifestos, consulte [habilitando estilos visuais](cookbook-overview.md).

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

