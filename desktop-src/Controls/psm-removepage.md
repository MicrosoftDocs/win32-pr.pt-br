---
title: PSM_REMOVEPAGE mensagem (Prsht.h)
description: Remove uma página de uma folha de propriedades. Você pode enviar essa mensagem explicitamente ou usando a \_ macro RemovePage do PropSheet.
ms.assetid: 2f387e97-4db4-4ad5-8600-7325da674e33
keywords:
- PSM_REMOVEPAGE controles de Windows mensagem
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
ms.openlocfilehash: 5e1493fe8a4f6a3b8e8ac93103d27e67ae984221bdc6efd584130879d17249c0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088606"
---
# <a name="psm_removepage-message"></a>Mensagem REMOVEPAGE do PSM \_

Remove uma página de uma folha de propriedades. Você pode enviar essa mensagem explicitamente ou usando a [**macro \_ RemovePage do PropSheet.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_removepage)

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice baseado em zero da página a ser removida.

</dd> <dt>

*lParam* 
</dt> <dd>

O alça HPROPSHEETPAGE da página a ser removida.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Sem valor de retorno.

## <a name="remarks"></a>Comentários

Um aplicativo pode especificar o índice ou o alça ou ambos. Se ambos são especificados, *lParam* tem precedência.

Enviar **\_ REMOVEPAGE do PSM** destrói a página de folha de propriedades que está sendo removida.

Várias mensagens e uma chamada de função ocorrem enquanto a folha de propriedades está manipulando a lista de páginas. Enquanto essa ação estiver ocorrendo, tentar modificar a lista de páginas terá resultados imprevisíveis. Da mesma forma, você não deve usar a mensagem **\_ REMOVEPAGE do PSM** em sua implementação de [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) ou ao lidar com as seguintes notificações e Windows mensagens.

-   [PSN \_ APPLY](psn-apply.md)
-   [PSN \_ KILLACTIVE](psn-killactive.md)
-   [PSN \_ RESET](psn-reset.md)
-   [PSN \_ SETACTIVE](psn-setactive.md)
-   [**WM \_ DESTROY**](/windows/desktop/winmsg/wm-destroy)
-   [**WM \_ INITDIALOG**](/windows/desktop/dlgbox/wm-initdialog)

Se você precisar modificar uma página de folha de propriedades enquanto estiver tratando uma dessas mensagens ou enquanto [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) estiver em operação, poste uma mensagem Windows privada. Seu aplicativo não receberá essa mensagem até que o gerenciador de planilhas de propriedades tenha concluído suas tarefas. Em seguida, você pode modificar a lista de páginas.

As notificações a seguir também são afetadas pela modificação da folha de propriedades.

-   [PSN \_ WIZBACK](psn-wizback.md)
-   [PSN \_ WIZNEXT](psn-wiznext.md)

Você pode adicionar ou remover páginas em resposta a essas notificações, desde que retorne (por meio de DWL MSGRESULT) um valor não zero para especificar a nova página \_ desejada. No entanto, observe que, se você remover uma página localizada antes da página atual (que tem um índice menor do que a página atual), o [PSN \_ KILLACTIVE](psn-killactive.md) poderá ser enviado para a página errada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |



 

