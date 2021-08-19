---
title: Mensagem de TBM_GETPTICS (commctrl. h)
description: Recupera o endereço de uma matriz que contém as posições das marcas de escala para um TrackBar.
ms.assetid: d15a4b4d-2ced-40a4-9351-ed7ecc5a5751
keywords:
- controles de Windows de mensagem de TBM_GETPTICS
topic_type:
- apiref
api_name:
- TBM_GETPTICS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f67bc6f1e5f67f262559d1c63401f1c19f8680798beae92d8847d4908f7cbe2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119078070"
---
# <a name="tbm_getptics-message"></a>\_Mensagem tbm GETPTICS

Recupera o endereço de uma matriz que contém as posições das marcas de escala para um TrackBar.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna o endereço de uma matriz de valores **DWORD** . Os elementos da matriz especificam as posições lógicas das marcas de escala do TrackBar, sem incluir as primeiras e as últimas marcas de escala criadas pelo TrackBar. As posições lógicas podem ser qualquer um dos valores inteiros na faixa de TrackBar de mínimo para máximo de posições do controle deslizante.

## <a name="remarks"></a>Comentários

O número de elementos na matriz é dois menores que a contagem de tiques retornada pela mensagem [**tbm \_ GETNUMTICS**](tbm-getnumtics.md) . Observe que os valores na matriz podem incluir posições duplicadas e podem não estar em ordem sequencial. O ponteiro retornado é válido até que você altere as marcas de escala do TrackBar.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





