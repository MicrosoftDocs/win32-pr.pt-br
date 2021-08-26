---
title: Mensagem de PSM_HWNDTOINDEX (Prsht. h)
description: Usa o identificador de janela da página da folha de propriedades e retorna seu índice de base zero. Você pode enviar essa mensagem explicitamente ou usar a \_ macro PropSheet HwndToIndex.
ms.assetid: vs|controls|~\controls\propsheet\messages\psm_hwndtoindex.htm
keywords:
- controles de Windows de mensagem de PSM_HWNDTOINDEX
topic_type:
- apiref
api_name:
- PSM_HWNDTOINDEX
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ed61c958fb3a0b30ba7cf55d1040cac51caa67f460d329312fb0e798b016aec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119985826"
---
# <a name="psm_hwndtoindex-message"></a>Mensagem de PSM \_ HWNDTOINDEX

Usa o identificador de janela da página da folha de propriedades e retorna seu índice de base zero. Você pode enviar essa mensagem explicitamente ou usar a macro [**PropSheet \_ HwndToIndex**](/windows/desktop/api/Prsht/nf-prsht-propsheet_hwndtoindex) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador para a janela da página.

</dd> <dt>

*lParam* 
</dt> <dd>

Deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna o índice de base zero da página da folha de propriedades especificada por *wParam* , se for bem-sucedida. Caso contrário, ele retornará -1.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

 





