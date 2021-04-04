---
title: Mensagem de TB_HITTEST (commctrl. h)
description: Determina onde um ponto reside em um controle ToolBar.
ms.assetid: d08f3805-2042-470e-8f5a-8a6a681d1189
keywords:
- Controles de TB_HITTEST de mensagens do Windows
topic_type:
- apiref
api_name:
- TB_HITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6264bc0191f091d3819081ddd67e428b64c84570
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918268"
---
# <a name="tb_hittest-message"></a>\_Mensagem HITTEST TB

Determina onde um ponto reside em um controle ToolBar.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura de [**ponto**](/previous-versions//dd162805(v=vs.85)) que contém a coordenada x do teste de clique no membro **x** e a coordenada y do teste de clique no membro **y** . As coordenadas são relativas à área do cliente da barra de ferramentas.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor inteiro. Se o valor de retorno for zero ou um valor positivo, ele será o índice de base zero do item não separador no qual o ponto está. Se o valor de retorno for negativo, o ponto não se situa em um botão. O valor absoluto do valor de retorno é o índice de um item separador ou o item não separador mais próximo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

