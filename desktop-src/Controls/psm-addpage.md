---
title: Mensagem de PSM_ADDPAGE (Prsht. h)
description: Adiciona uma nova página ao final de uma folha de propriedades existente. Você pode enviar essa mensagem explicitamente ou usando a macro PropSheet do \_ AddPage.
ms.assetid: 41f9a09e-6de6-466b-bdfa-c8c4e8f193e4
keywords:
- Controles de PSM_ADDPAGE de mensagens do Windows
topic_type:
- apiref
api_name:
- PSM_ADDPAGE
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c4d09e07dfa2be86e11fa33863f091732955714
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824637"
---
# <a name="psm_addpage-message"></a>Mensagem de PSM \_ ADDPAGE

Adiciona uma nova página ao final de uma folha de propriedades existente. Você pode enviar essa mensagem explicitamente ou usando a macro [**PropSheet do \_ AddPage**](/windows/desktop/api/Prsht/nf-prsht-propsheet_addpage) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador para a página a ser adicionada. A página deve ter sido criada por uma chamada anterior para a função [**CreatePropertySheetPage**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.

## <a name="remarks"></a>Comentários

A nova página não deve ser maior do que a maior página atualmente na folha de propriedades porque a folha de propriedades não é redimensionada para se ajustar à nova página.

Várias mensagens e uma chamada de função ocorrem enquanto a folha de propriedades está manipulando a lista de páginas. Enquanto essa ação está ocorrendo, a tentativa de modificar a lista de páginas terá resultados imprevisíveis. De acordo, você não deve usar a \_ mensagem de PSM ADDPAGE em sua implementação do [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) ou ao manipular as notificações e mensagens do Windows a seguir.

-   [PSN \_ aplicar](psn-apply.md)
-   [PSN \_ KILLACTIVE](psn-killactive.md)
-   [redefinição de PSN \_](psn-reset.md)
-   [PSN \_ SETactive](psn-setactive.md)
-   [**destruição do WM \_**](/windows/desktop/winmsg/wm-destroy)
-   [**INITDIALOG do WM \_**](/windows/desktop/dlgbox/wm-initdialog)

Se você precisar modificar uma página de folha de propriedades enquanto estiver manipulando uma dessas mensagens ou enquanto [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) estiver em operação, poste uma mensagem privada do Windows. Seu aplicativo não receberá essa mensagem até que o Gerenciador de folhas de propriedades tenha concluído suas tarefas. Em seguida, você pode modificar a lista de páginas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

