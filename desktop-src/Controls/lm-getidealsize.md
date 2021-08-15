---
title: LM_GETIDEALSIZE mensagem (Commctrl.h)
description: LM_GETIDEALSIZE mensagem – recupera a altura preferencial de um link para a largura atual do controle.
ms.assetid: 63aad7eb-26ee-41d2-90d4-65fdcf0f182a
keywords:
- LM_GETIDEALSIZE controles de Windows mensagem
topic_type:
- apiref
api_name:
- LM_GETIDEALSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 035a919aabeb5d07587c7d9e4fc97e5edc728de4ec8fc476448dca62658f1ce3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118958365"
---
# <a name="lm_getidealsize-message"></a>Mensagem \_ GETIDEALSIZE lm

Recupera a altura preferencial de um link para a largura atual do controle.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Largura máxima do link, em pixels.</dd> <dt>

*lParam* \[ out\]
</dt> <dd>Quando essa mensagem retorna, contém um ponteiro para uma <a href="/previous-versions//dd145106(v=vs.85)">**estrutura SIZE.**</a> O **membro** cy dessa estrutura indica a altura ideal do controle para a largura determinada. Ele ajusta o membro **cx** para a quantidade de espaço realmente necessária.</dd> </dl>

## <a name="return-value"></a>Valor retornado

Inteiro que representa a altura preferencial do texto do link, em pixels.

## <a name="remarks"></a>Comentários

> [!Note]  
> Para usar essa API, você deve fornecer um manifesto que especifique Comclt32.dll versão 6.0. Para obter mais informações sobre manifestos, consulte [Habilitando estilos visuais.](cookbook-overview.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

