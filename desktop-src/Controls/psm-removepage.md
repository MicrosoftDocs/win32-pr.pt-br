---
title: Mensagem de PSM_REMOVEPAGE (Prsht. h)
description: Remove uma página de uma folha de propriedades. Você pode enviar essa mensagem explicitamente ou usando a macro PropSheet \_ RemovePage.
ms.assetid: 2f387e97-4db4-4ad5-8600-7325da674e33
keywords:
- Controles de PSM_REMOVEPAGE de mensagens do Windows
topic_type:
- apiref
api_name:
- PSM_REMOVEPAGE
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cae1611e1ed9540fce23d20681f44849903e5c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824634"
---
# <a name="psm_removepage-message"></a>Mensagem de PSM \_ REMOVEPAGE

Remove uma página de uma folha de propriedades. Você pode enviar essa mensagem explicitamente ou usando a macro [**PropSheet \_ RemovePage**](/windows/desktop/api/Prsht/nf-prsht-propsheet_removepage) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de base zero da página a ser removida.

</dd> <dt>

*lParam* 
</dt> <dd>

O identificador de HPROPSHEETPAGE da página a ser removida.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Sem valor de retorno.

## <a name="remarks"></a>Comentários

Um aplicativo pode especificar o índice ou o identificador, ou ambos. Se ambos forem especificados, *lParam* terá precedência.

O envio de **PSM \_ REMOVEPAGE** destrói a página da folha de propriedades que está sendo removida.

Várias mensagens e uma chamada de função ocorrem enquanto a folha de propriedades está manipulando a lista de páginas. Enquanto essa ação está ocorrendo, a tentativa de modificar a lista de páginas terá resultados imprevisíveis. De acordo, você não deve usar a mensagem de **PSM \_ REMOVEPAGE** em sua implementação do [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) ou ao manipular as notificações e mensagens do Windows a seguir.

-   [PSN \_ aplicar](psn-apply.md)
-   [PSN \_ KILLACTIVE](psn-killactive.md)
-   [redefinição de PSN \_](psn-reset.md)
-   [PSN \_ SETactive](psn-setactive.md)
-   [**destruição do WM \_**](/windows/desktop/winmsg/wm-destroy)
-   [**INITDIALOG do WM \_**](/windows/desktop/dlgbox/wm-initdialog)

Se você precisar modificar uma página de folha de propriedades enquanto estiver manipulando uma dessas mensagens ou enquanto [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) estiver em operação, poste uma mensagem privada do Windows. Seu aplicativo não receberá essa mensagem até que o Gerenciador de folhas de propriedades tenha concluído suas tarefas. Em seguida, você pode modificar a lista de páginas.

As notificações a seguir também são afetadas pela modificação da folha de propriedades.

-   [PSN \_ WIZBACK](psn-wizback.md)
-   [PSN \_ WIZNEXT](psn-wiznext.md)

Você pode adicionar ou remover páginas em resposta a essas notificações, desde que você retorne (via DWL \_ MSGRESULT) um valor diferente de zero para especificar a página nova desejada. No entanto, observe que se você remover uma página que está localizada antes da página atual (que tem um índice menor do que a página atual), [PSN \_ KILLACTIVE](psn-killactive.md) poderá ser enviada para a página errada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

