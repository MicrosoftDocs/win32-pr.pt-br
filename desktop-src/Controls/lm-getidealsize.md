---
title: Mensagem de LM_GETIDEALSIZE (commctrl. h)
description: Recupera a altura preferida de um link para a largura atual do controle.
ms.assetid: 63aad7eb-26ee-41d2-90d4-65fdcf0f182a
keywords:
- Controles de LM_GETIDEALSIZE de mensagens do Windows
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
ms.openlocfilehash: c138e22982116a3b7173f586d96c70cfc91194c3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454643"
---
# <a name="lm_getidealsize-message"></a>\_Mensagem GETIDEALSIZE de LM

Recupera a altura preferida de um link para a largura atual do controle.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Largura máxima do link, em pixels.</dd> <dt>

*lParam* \[ fora\]
</dt> <dd>Quando essa mensagem retorna, contém um ponteiro para uma estrutura de <a href="/previous-versions//dd145106(v=vs.85)">**tamanho**</a> . O membro **CY** desta estrutura indica a altura ideal do controle para a largura especificada. Ele ajusta o membro do **CX** para a quantidade de espaço realmente necessária.</dd> </dl>

## <a name="return-value"></a>Retornar valor

Inteiro que representa a altura preferida do texto do link, em pixels.

## <a name="remarks"></a>Comentários

> [!Note]  
> Para usar essa API, você deve fornecer um manifesto que especifique Comclt32.dll versão 6,0. Para obter mais informações sobre manifestos, consulte [habilitando estilos visuais](cookbook-overview.md).

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

