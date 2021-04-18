---
title: Mensagem de PSM_INSERTPAGE (Prsht. h)
description: Insere uma nova página em uma folha de propriedades existente. A página pode ser inserida em um índice especificado ou após uma página especificada. Você pode enviar essa mensagem explicitamente ou usando a macro PropSheet \_ InsertPage.
ms.assetid: 69d55e68-510d-45f1-93d6-ce2bf5dfdb6d
keywords:
- Controles de PSM_INSERTPAGE de mensagens do Windows
topic_type:
- apiref
api_name:
- PSM_INSERTPAGE
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: afdd58536a5cdd18d39a331df4b18c9bbae93842
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105749076"
---
# <a name="psm_insertpage-message"></a>Mensagem de PSM \_ INSERTPAGE

Insere uma nova página em uma folha de propriedades existente. A página pode ser inserida em um índice especificado ou após uma página especificada. Você pode enviar essa mensagem explicitamente ou usando a macro [**PropSheet \_ InsertPage**](/windows/desktop/api/Prsht/nf-prsht-propsheet_insertpage) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Onde a página deve ser inserida. Defina esse parâmetro como **NULL** para tornar a nova página a primeira página. Para especificar onde a nova página deve ser inserida, você pode passar um índice ou um identificador HPROPSHEETPAGE da página existente.



| Valor                                                                                                                                             | Significado                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt></dt><dt>índice</dt> do </dl>            | Se o parâmetro *wParam* for menor que MAXUSHORT (o maior inteiro curto não atribuído), o *wParam* especificará o índice de base zero para a nova página. Por exemplo, para transformar a página inserida na terceira página da folha de propriedades, defina *wParam* como 2. Para torná-la a primeira página, defina *wParam* como 0. Se *wParam* tiver um valor maior que o número de páginas e menor que MAXUSHORT, a página será anexada.<br/> |
| <dl> <dt></dt><dt>hpageInsertAfter</dt> </dl> | Se você definir o parâmetro *wParam* como um identificador HPROPSHEETPAGE da página existente, a nova página será inserida após ele.<br/>                                                                                                                                                                                                                                                                                          |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador para a página a ser inserida. A página deve ser criada primeiro por uma chamada para a função [**CreatePropertySheetPage**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor diferente de zero se a página tiver sido inserida com êxito ou zero caso contrário.

## <a name="remarks"></a>Comentários

As páginas após o ponto de inserção são deslocadas para a direita para acomodar a nova página.

A folha de propriedades não é redimensionada para se ajustar à nova página. Não torne a nova página maior do que a maior página da folha de propriedades.

Várias mensagens e uma chamada de função ocorrem enquanto a folha de propriedades está manipulando a lista de páginas. Enquanto essa ação está ocorrendo, a tentativa de modificar a lista de páginas terá resultados imprevisíveis. De acordo, você não deve usar a \_ mensagem de PSM INSERTPAGE em sua implementação do [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) ou ao manipular as notificações e mensagens do Windows a seguir.

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

Você pode adicionar ou remover páginas em resposta a essas notificações, desde que você retorne (via DWL \_ MSGRESULT) um valor diferente de zero para especificar a página nova desejada. No entanto, observe que, se você inserir uma página que está localizada antes da página atual (que tem um índice menor do que a página atual), [PSN \_ KILLACTIVE](psn-killactive.md) poderá ser enviada para a página errada.

> [!Note]  
> Não há suporte para esta mensagem ao usar o estilo de assistente Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

