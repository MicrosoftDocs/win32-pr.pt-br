---
title: Mensagem de TB_MAPACCELERATOR (commctrl. h)
description: Determina a ID do botão que corresponde ao caractere de acelerador especificado.
ms.assetid: 724b593d-39af-4301-b721-0332844677b1
keywords:
- Controles de TB_MAPACCELERATOR de mensagens do Windows
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
ms.openlocfilehash: 029584d9e1614a3a135da5ebd3f4f446795fd9ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644939"
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

## <a name="return-value"></a>Retornar valor

Retorna um valor diferente de zero se um dos botões tiver *wParam* como seu caractere de acelerador, ou zero caso contrário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **TB \_ MAPACCELERATORW** (Unicode) e **TB \_ MAPACCELERATORA** (ANSI)<br/>       |



 

 





