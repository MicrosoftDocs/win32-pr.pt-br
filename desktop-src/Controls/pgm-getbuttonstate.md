---
title: Mensagem de PGM_GETBUTTONSTATE (commctrl. h)
description: Recupera o estado do botão especificado em um controle de pager. Você pode enviar essa mensagem explicitamente ou usar a \_ macro Getbuttonstate do pager.
ms.assetid: 58f99b67-fef7-4695-86e2-0579a2f6de2f
keywords:
- Controles de PGM_GETBUTTONSTATE de mensagens do Windows
topic_type:
- apiref
api_name:
- PGM_GETBUTTONSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d8c9eebbc0aa91651a01de1fe193544f0c8afcf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918788"
---
# <a name="pgm_getbuttonstate-message"></a>Mensagem do PGM \_ GETbuttonstate

Recupera o estado do botão especificado em um controle de pager. Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ getbuttonstate do pager**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getbuttonstate) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

Indica para qual botão recuperar o estado. Esse valor pode ser um dos seguintes:



| Valor                                                                                                                                                                     | Significado                                                                                                                                                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PGB_TOPORLEFT"></span><span id="pgb_toporleft"></span><dl> <dt>**PGB \_ TOPORLEFT**</dt> </dl>             | Indica o botão superior em um controle de pager [**\_ Vert PGS**](pager-control-styles.md) ou o botão esquerdo em um controle [**PGS \_ na horizontal**](pager-control-styles.md) pager. <br/>     |
| <span id="PGB_BOTTOMORRIGHT"></span><span id="pgb_bottomorright"></span><dl> <dt>**PGB \_ BOTTOMORRIGHT**</dt> </dl> | Indica o botão inferior em um controle de pager [**\_ Vert PGS**](pager-control-styles.md) ou o botão direito em um controle [**PGS \_ na horizontal**](pager-control-styles.md) pager. <br/> |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna o estado do botão especificado em *lParam*. Esse será um ou mais dos seguintes valores (se mais de um valor for retornado, eles serão combinados usando um OR bit a bit):



| Código de retorno                                                                                   | Descrição                                 |
|-----------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <dt>**PGF \_ invisível**</dt> </dl> | O botão não está visível. <br/>      |
| <dl> <dt>**PGF \_ normal**</dt> </dl>    | O botão está em estado normal. <br/>  |
| <dl> <dt>**PGF \_ cinza**</dt> </dl>    | O botão está em estado acinzentado. <br/>  |
| <dl> <dt>**PGF \_ pressionado**</dt> </dl> | O botão está no estado pressionado. <br/> |
| <dl> <dt>**PGF \_ quente**</dt> </dl>       | O botão está em estado ativo. <br/>     |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





