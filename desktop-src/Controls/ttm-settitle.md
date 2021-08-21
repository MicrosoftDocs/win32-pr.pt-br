---
title: Mensagem de TTM_SETTITLE (commctrl. h)
description: Adiciona um ícone padrão e uma cadeia de título a uma dica de ferramenta.
ms.assetid: e745a592-eef7-4e0d-8939-a48b52c4ab9f
keywords:
- controles de Windows de mensagem de TTM_SETTITLE
topic_type:
- apiref
api_name:
- TTM_SETTITLE
- TTM_SETTITLEA
- TTM_SETTITLEW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0e159ce522ea27361f93beaa96da06959fba6f92fedf5981dfd049ddc7f36cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118166349"
---
# <a name="ttm_settitle-message"></a>Mensagem do TTM \_ SETtitle

Adiciona um ícone padrão e uma cadeia de título a uma dica de ferramenta.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Defina *wParam* como um dos valores a seguir para especificar o ícone a ser exibido. a partir do Windows XP SP2 e posterior, esse parâmetro também pode conter um valor **HICON** . Um valor maior que TTI \_ é considerado um **HICON**.



| Valor                                                                                                                                                                      | Significado                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| <span id="TTI_NONE"></span><span id="tti_none"></span><dl> <dt>**TTI \_ nenhum**</dt> </dl>                             | Nenhum ícone.<br/>         |
| <span id="TTI_INFO"></span><span id="tti_info"></span><dl> <dt>**informações de TTI \_**</dt> </dl>                             | Ícone de informações.<br/>       |
| <span id="TTI_WARNING"></span><span id="tti_warning"></span><dl> <dt>**aviso de TTI \_**</dt> </dl>                    | Ícone de aviso:<br/>     |
| <span id="TTI_ERROR"></span><span id="tti_error"></span><dl> <dt>**erro de TTI \_**</dt> </dl>                          | Ícone de erro<br/>       |
| <span id="TTI_INFO_LARGE"></span><span id="tti_info_large"></span><dl> <dt>**TTI de \_ informações \_ grande**</dt> </dl>          | Ícone de erro grande<br/> |
| <span id="TTI_WARNING_LARGE"></span><span id="tti_warning_large"></span><dl> <dt>**TTI de \_ aviso \_ grande**</dt> </dl> | Ícone de erro grande<br/> |
| <span id="TTI_ERROR_LARGE"></span><span id="tti_error_large"></span><dl> <dt>**erro de TTI \_ \_ grande**</dt> </dl>       | Ícone de erro grande<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para a cadeia de caracteres de título. Você deve atribuir um valor a *lParam*.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará **true** se for bem-sucedido, **false** se não.

## <a name="remarks"></a>Comentários

O título de uma dica de ferramenta aparece acima do texto, em uma fonte diferente. Não é suficiente ter um título; a dica de ferramenta também deve ter texto ou não é exibida.

Quando *wParam* contém um **HICON**, uma cópia do ícone é criada pela janela de dica de ferramenta.

Ao chamar **TTM \_ SetTitle**, a cadeia de caracteres apontada por *lParam* não deve exceder 100 **TCHARs** de comprimento, incluindo o **nulo** de terminação.

## <a name="examples"></a>Exemplos

O exemplo a seguir mostra como adicionar um título e um ícone do sistema a uma dica de ferramenta.


```C++
// hwndTip is the handle of the tooltip window.
HICON hIcon = LoadIcon(NULL, IDI_INFORMATION);
SendMessage(hwndTip, TTM_SETTITLE, (WPARAM)hIcon, L"Title text");
DestroyIcon(hIcon);
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **TTM \_ SETTITLEW** (Unicode) e **TTM \_ settítuloa** (ANSI)<br/>                 |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Sobre os controles de dica de ferramenta](tooltip-controls.md)
</dt> </dl>

 

 





