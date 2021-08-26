---
title: HDM_CREATEDRAGIMAGE mensagem (Commctrl.h)
description: Cria uma versão semi transparente da imagem de um item para uso como uma imagem de arrastar. Você pode enviar essa mensagem explicitamente ou usar a macro \_ CreateDragImage do header.
ms.assetid: 1b9dc515-d327-4634-a424-cc15a32f0f7c
keywords:
- HDM_CREATEDRAGIMAGE controles de Windows mensagem
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
ms.openlocfilehash: 1507f3e72ce75394aaad834fe5c0d876fc579a671ad8f2df00865b2278ad6e32
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047226"
---
# <a name="hdm_createdragimage-message"></a>Mensagem HDM \_ CREATEDRAGIMAGE

Cria uma versão semi transparente da imagem de um item para uso como uma imagem de arrastar. Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ CreateDragImage do header.**](/windows/desktop/api/Commctrl/nf-commctrl-header_createdragimage)

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O índice baseado em zero do item dentro do controle de header. A imagem atribuída a esse item é a base para a imagem transparente.

</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um alça para uma lista de imagens que contém a nova imagem como seu único elemento.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





