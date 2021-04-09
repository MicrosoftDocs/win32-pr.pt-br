---
title: Mensagem de PSM_HWNDTOINDEX (Prsht. h)
description: Usa o identificador de janela da página da folha de propriedades e retorna seu índice de base zero. Você pode enviar essa mensagem explicitamente ou usar a \_ macro PropSheet HwndToIndex.
ms.assetid: vs|controls|~\controls\propsheet\messages\psm_hwndtoindex.htm
keywords:
- Controles de PSM_HWNDTOINDEX de mensagens do Windows
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
ms.openlocfilehash: d6632d331a6f271e339663a23210d0b399fb669b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085728"
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

## <a name="return-value"></a>Retornar valor

Retorna o índice de base zero da página da folha de propriedades especificada por *wParam* , se for bem-sucedida. Caso contrário, ele retornará -1.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

 





