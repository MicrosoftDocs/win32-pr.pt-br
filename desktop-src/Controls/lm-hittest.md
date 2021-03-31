---
title: Mensagem de LM_HITTEST (commctrl. h)
description: Determina se o usuário clicou no link especificado.
ms.assetid: a84c0388-26e7-4eda-9c6c-c5f64142d67a
keywords:
- Controles de LM_HITTEST de mensagens do Windows
topic_type:
- apiref
api_name:
- LM_HITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c497800369203ac8ea7484371e1038ba15d6cc68
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824172"
---
# <a name="lm_hittest-message"></a>Mensagem de HITTEST do LM \_

Determina se o usuário clicou no link especificado.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser **NULL**.</dd> <dt>

*lParam* 
</dt> <dd>Ponteiro para uma estrutura <a href="/windows/win32/api/commctrl/ns-commctrl-lhittestinfo">**LHITTESTINFO**</a> a ser preenchida com informações sobre o link no qual o usuário clicou, caso exista. </dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna **true** se o usuário clicou em um link; caso contrário, retorna **false**.

## <a name="remarks"></a>Comentários

Se a mensagem de **\_ HITTEST do LM** for bem sucedido, o sistema preencherá o [**LITEM. iLink**](/windows/win32/api/commctrl/ns-commctrl-litem) e o **LITEM. szID**. Se a mensagem de **\_ HITTEST do LM** falhar, não assuma que todas as informações em **litem** são válidas.

> [!Note]  
> Para usar essa API, você deve fornecer um manifesto especificando Comclt32.dll versão 6,0. Para obter mais informações sobre manifestos, consulte [habilitando estilos visuais](cookbook-overview.md).

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





