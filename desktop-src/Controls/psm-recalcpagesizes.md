---
title: Mensagem de PSM_RECALCPAGESIZES (Prsht. h)
description: Recalcula o tamanho da página de uma folha de propriedades padrão ou do assistente depois que as páginas são adicionadas ou removidas. Você pode enviar essa mensagem explicitamente ou usar a \_ macro PropSheet RecalcPageSizes.
ms.assetid: 42257ea3-0471-4c67-adcd-01cd2669a51e
keywords:
- Controles de PSM_RECALCPAGESIZES de mensagens do Windows
topic_type:
- apiref
api_name:
- PSM_RECALCPAGESIZES
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18ae2030f432e8c52ed6208be34d429b4579edb6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105752941"
---
# <a name="psm_recalcpagesizes-message"></a>Mensagem de PSM \_ RECALCPAGESIZES

Recalcula o tamanho da página de uma folha de propriedades padrão ou do assistente depois que as páginas são adicionadas ou removidas. Você pode enviar essa mensagem explicitamente ou usar a macro [**PropSheet \_ RecalcPageSizes**](/windows/desktop/api/Prsht/nf-prsht-propsheet_recalcpagesizes) .

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

Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.

## <a name="remarks"></a>Comentários

Quando uma folha de propriedades é criada, ela é dimensionada para se ajustar à coleção inicial de páginas. Para manter a compatibilidade com versões anteriores dos controles comuns, as folhas de propriedades e os assistentes não são automaticamente redimensionados quando as páginas são adicionadas ou removidas posteriormente. Com os controles comuns [versão 5,80](common-control-versions.md), os aplicativos devem enviar uma mensagem de **PSM \_ RECALCPAGESIZES** depois de adicionar ou remover páginas com [**PSM \_ ADDPAGE**](psm-addpage.md), [**PSM \_ INSERTPAGE**](psm-insertpage.md), [**PSM \_ REMOVEPAGE**](psm-removepage.md)ou suas macros equivalentes. Ele garante que a folha de propriedades seja dimensionada corretamente para sua coleção atual de páginas. Se essa mensagem não for enviada, algumas páginas da folha de propriedades poderão ser truncadas ou muito grandes.

> [!Note]  
> Não há suporte para esta mensagem ao usar o estilo de assistente Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

 





