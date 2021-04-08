---
title: Mensagem de PSM_INDEXTOHWND (Prsht. h)
description: Usa o índice de uma página de folha de propriedades e retorna seu identificador de janela. Você pode enviar essa mensagem explicitamente ou usar a \_ macro PropSheet IndexToHwnd.
ms.assetid: 93b46b4c-47f9-4ce8-8797-f3d4bd5248e9
keywords:
- Controles de PSM_INDEXTOHWND de mensagens do Windows
topic_type:
- apiref
api_name:
- PSM_INDEXTOHWND
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 788b1dd0e7312f301051d9a57fcdec43f3f2f72a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086083"
---
# <a name="psm_indextohwnd-message"></a>Mensagem de PSM \_ INDEXTOHWND

Usa o índice de uma página de folha de propriedades e retorna seu identificador de janela. Você pode enviar essa mensagem explicitamente ou usar a macro [**PropSheet \_ IndexToHwnd**](/windows/desktop/api/Prsht/nf-prsht-propsheet_indextohwnd) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de base zero da página.

</dd> <dt>

*lParam* 
</dt> <dd>

Deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna o identificador para a janela da página da folha de propriedades especificada por *wParam* , se for bem-sucedida. Caso contrário, retornará zero.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

 





