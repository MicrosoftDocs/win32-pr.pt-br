---
title: PSM_ADDPAGE mensagem (Prsht.h)
description: Adiciona uma nova página ao final de uma folha de propriedades existente. Você pode enviar essa mensagem explicitamente ou usando a \_ macro PropSheet AddPage.
ms.assetid: 41f9a09e-6de6-466b-bdfa-c8c4e8f193e4
keywords:
- PSM_ADDPAGE controles de Windows mensagem
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
ms.openlocfilehash: d17e9da965e5e45c6fe11bc319436c00663fdc6348d3d2457b3c15472f6f3868
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118169822"
---
# <a name="psm_addpage-message"></a>Mensagem ADDPAGE do PSM \_

Adiciona uma nova página ao final de uma folha de propriedades existente. Você pode enviar essa mensagem explicitamente ou usando a [**macro \_ PropSheet AddPage.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_addpage)

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Lidar com a página a ser acrescentada. A página deve ter sido criada por uma chamada anterior para a [**função CreatePropertySheetPage.**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna **TRUE se** for bem-sucedido ou FALSE **caso** contrário.

## <a name="remarks"></a>Comentários

A nova página não deve ser maior do que a maior página atualmente na folha de propriedades porque a folha de propriedades não é reessada para se ajustar à nova página.

Várias mensagens e uma chamada de função ocorrem enquanto a folha de propriedades está manipulando a lista de páginas. Enquanto essa ação estiver ocorrendo, tentar modificar a lista de páginas terá resultados imprevisíveis. Da mesma forma, você não deve usar a mensagem ADDPAGE do PSM em sua implementação de \_ [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) ou ao lidar com as seguintes notificações e Windows mensagens.

-   [PSN \_ APPLY](psn-apply.md)
-   [PSN \_ KILLACTIVE](psn-killactive.md)
-   [PSN \_ RESET](psn-reset.md)
-   [PSN \_ SETACTIVE](psn-setactive.md)
-   [**WM \_ DESTROY**](/windows/desktop/winmsg/wm-destroy)
-   [**WM \_ INITDIALOG**](/windows/desktop/dlgbox/wm-initdialog)

Se você precisar modificar uma página de folha de propriedades enquanto estiver tratando uma dessas mensagens ou enquanto [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) estiver em operação, poste uma mensagem Windows privada. Seu aplicativo não receberá essa mensagem até que o gerenciador de planilhas de propriedades tenha concluído suas tarefas. Em seguida, você pode modificar a lista de páginas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |



 

