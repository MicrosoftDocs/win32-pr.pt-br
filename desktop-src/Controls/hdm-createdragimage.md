---
title: Mensagem de HDM_CREATEDRAGIMAGE (commctrl. h)
description: Cria uma versão semitransparente da imagem de um item para uso como uma imagem de arrastar. Você pode enviar essa mensagem explicitamente ou usar a \_ macro CreateDragImage do cabeçalho.
ms.assetid: 1b9dc515-d327-4634-a424-cc15a32f0f7c
keywords:
- Controles de HDM_CREATEDRAGIMAGE de mensagens do Windows
topic_type:
- apiref
api_name:
- HDM_CREATEDRAGIMAGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9e801ad9771205b5f2e6df8e37bb0a0ad7f0bc6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009526"
---
# <a name="hdm_createdragimage-message"></a>\_Mensagem HDM CREATEDRAGIMAGE

Cria uma versão semitransparente da imagem de um item para uso como uma imagem de arrastar. Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ CreateDragImage do cabeçalho**](/windows/desktop/api/Commctrl/nf-commctrl-header_createdragimage) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O índice de base zero do item dentro do controle de cabeçalho. A imagem atribuída a esse item é a base para a imagem transparente.

</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um identificador para uma lista de imagens que contém a nova imagem como seu único elemento.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





