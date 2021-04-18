---
title: Mensagem de PSM_GETCURRENTPAGEHWND (Prsht. h)
description: Recupera um identificador para a janela da página atual de uma folha de propriedades. Você pode enviar essa mensagem explicitamente ou usando a macro PropSheet \_ GetCurrentPageHwnd.
ms.assetid: 1f2d0af9-5853-48e7-b827-483be032b6ca
keywords:
- Controles de PSM_GETCURRENTPAGEHWND de mensagens do Windows
topic_type:
- apiref
api_name:
- PSM_GETCURRENTPAGEHWND
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae9ac89e6bc60317f2caf31ea92754d10983e11a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105755831"
---
# <a name="psm_getcurrentpagehwnd-message"></a>Mensagem de PSM \_ GETCURRENTPAGEHWND

Recupera um identificador para a janela da página atual de uma folha de propriedades. Você pode enviar essa mensagem explicitamente ou usando a macro [**PropSheet \_ GetCurrentPageHwnd**](/windows/desktop/api/Prsht/nf-prsht-propsheet_getcurrentpagehwnd) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um identificador para a janela da página da folha de propriedades atual.

## <a name="remarks"></a>Comentários

Use a **mensagem \_ GETCURRENTPAGEHWND de PSM** com folhas de propriedades sem janela restrita para determinar quando destruir a caixa de diálogo. Quando o usuário clica no botão **OK** ou **Cancelar** , o **PSM \_ GETCURRENTPAGEHWND** retorna **NULL** e, em seguida, você pode usar a função [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) para destruir a caixa de diálogo.

> [!Note]  
> Não há suporte para esta mensagem ao usar o estilo de assistente Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Folha**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta)
</dt> </dl>

 

