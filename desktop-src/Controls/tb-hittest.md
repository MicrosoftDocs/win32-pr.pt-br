---
title: TB_HITTEST mensagem (Commctrl.h)
description: Determina onde um ponto está em um controle de barra de ferramentas.
ms.assetid: d08f3805-2042-470e-8f5a-8a6a681d1189
keywords:
- TB_HITTEST controles de Windows mensagem
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
ms.openlocfilehash: 8d89cecf1d1df5c370ab9a00ae1251df9df7ef919f9959b998407a9fb5881178
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119696156"
---
# <a name="tb_hittest-message"></a>Mensagem \_ TB HITTEST

Determina onde um ponto está em um controle de barra de ferramentas.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma [**estrutura POINT**](/previous-versions//dd162805(v=vs.85)) que contém a coordenada x do teste de acerto no membro **x** e a coordenada y do teste de acerto no **membro** y. As coordenadas são relativas à área de cliente da barra de ferramentas.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um valor inteiro. Se o valor de retorno for zero ou um valor positivo, ele será o índice baseado em zero do item nonseparator no qual o ponto está. Se o valor de retorno for negativo, o ponto não se enquadra em um botão. O valor absoluto do valor de retorno é o índice de um item separador ou o item nonseparator mais próximo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

