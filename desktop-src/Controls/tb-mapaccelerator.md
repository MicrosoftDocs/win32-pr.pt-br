---
title: Mensagem de TB_MAPACCELERATOR (commctrl. h)
description: Determina a ID do botão que corresponde ao caractere de acelerador especificado.
ms.assetid: 724b593d-39af-4301-b721-0332844677b1
keywords:
- controles de Windows de mensagem de TB_MAPACCELERATOR
topic_type:
- apiref
api_name:
- TB_MAPACCELERATOR
- TB_MAPACCELERATORA
- TB_MAPACCELERATORW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f905ccf5ea01e3c06cb87a160a44598c2c4a7790c972f4ee83b245e3ed5c0111
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118168080"
---
# <a name="tb_mapaccelerator-message"></a>TB de \_ mensagem MAPACCELERATOR

Determina a ID do botão que corresponde ao caractere de acelerador especificado.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* \[ no\]
</dt> <dd>

O caractere do acelerador.

</dd> <dt>

*lParam* \[ fora\]
</dt> <dd>

Ponteiro para um **uint**. No retorno, se for bem-sucedido, esse parâmetro manterá a ID do botão que tem *wParam* como seu caractere de acelerador.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um valor diferente de zero se um dos botões tiver *wParam* como seu caractere de acelerador, ou zero caso contrário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **TB \_ MAPACCELERATORW** (Unicode) e **TB \_ MAPACCELERATORA** (ANSI)<br/>       |



 

 





