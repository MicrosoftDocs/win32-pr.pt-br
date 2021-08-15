---
title: PSM_SETNEXTTEXT mensagem (Prsht.h)
description: Define o texto do botão Próximo em um assistente. Você pode enviar essa mensagem explicitamente ou usando a macro \_ PropSheet SetNextText.
ms.assetid: 4608425e-1724-4d0b-b0f6-9fec147a85f6
keywords:
- PSM_SETNEXTTEXT controles de Windows mensagem
topic_type:
- apiref
api_name:
- PSM_SETNEXTTEXT
- PSM_SETNEXTTEXTW
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d177acb2f2c96e12f5dc4b460ee88149ad81f9b4f79cc3505f776d8f1f92551
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118410076"
---
# <a name="psm_setnexttext-message"></a>Mensagem SETNEXTTEXT do PSM \_

Define o texto do **botão Próximo** em um assistente. Você pode enviar essa mensagem explicitamente ou usando a [**macro \_ PropSheet SetNextText.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setnexttext)

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para um buffer que contém o texto.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Nenhum valor de retorno significativo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **PSM \_ SETNEXTTEXTW** (Unicode)<br/>                                         |



 

 





