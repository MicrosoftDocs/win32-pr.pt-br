---
title: Mensagem LBSELCHSTRING (Commdlg.h)
description: Uma caixa de diálogo Abrir ou Salvar como envia a mensagem registrada LBSELCHSTRING ao procedimento de gancho quando a seleção muda em qualquer uma das caixas de listagem ou caixas de combinação da caixa de diálogo.
ms.assetid: 3a8ebc63-b324-43ed-bb6f-34779f6043e7
keywords:
- Caixas de diálogo da mensagem LBSELCHSTRING
topic_type:
- apiref
api_name:
- LBSELCHSTRING
- LBSELCHSTRINGA
- LBSELCHSTRINGW
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62d61f88bd7cb6a84a94a3d8a246e6045f88a305
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/27/2021
ms.locfileid: "110550041"
---
# <a name="lbselchstring-message"></a>Mensagem LBSELCHSTRING

\[Começando com o Windows Vista, as **caixas** de **diálogo** Abrir e Salvar como comuns foram superadas pela caixa de diálogo Item [Comum](../shell/common-file-dialog.md). Recomendamos que você use a API de Diálogo de Item Comum em vez dessas caixas de diálogo da Biblioteca de Caixas de Diálogo Comuns.\]

Uma  caixa **de** diálogo Abrir ou Salvar como envia a mensagem registrada **LBSELCHSTRING** ao procedimento de gancho quando a seleção muda em qualquer uma das caixas de listagem ou caixas de combinação da caixa de diálogo.


```C++
#define LBSELCHSTRING TEXT("commdlg_LBSelChangedNotify")
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O identificador da caixa de listagem ou caixa de combinação na qual a seleção foi alterada.

</dd> <dt>

*lParam* 
</dt> <dd>

A palavra de ordem baixa especifica o número do item da cadeia de caracteres selecionada na caixa de listagem ou caixa de combinação. A palavra de ordem alta especifica o tipo de alteração de seleção. Esse parâmetro pode usar um dos valores a seguir.



| Valor                                                                                                                                                                                                                       | Significado                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="CD_LBSELCHANGE"></span><span id="cd_lbselchange"></span><dl> <dt>**CD \_ LBSELCHANGE**</dt> <dt>0</dt> </dl>     | O item é o único item selecionado em uma caixa de listagem de seleção única.<br/>      |
| <span id="CD_LBSELADD"></span><span id="cd_lbseladd"></span><dl> <dt>**CD \_ LBSELADD**</dt> <dt>2</dt> </dl>              | O item é um dos itens selecionados em uma caixa de listagem de seleção múltipla.<br/> |
| <span id="CD_LBSELSUB"></span><span id="cd_lbselsub"></span><dl> <dt>**CD \_ LBSELSUB**</dt> <dt>1</dt> </dl>              | O item não está mais selecionado em uma caixa de listagem de seleção múltipla.<br/>        |
| <span id="CD_LBSELNOITEMS"></span><span id="cd_lbselnoitems"></span><dl> <dt>**CD \_ LBSELNOITEMS**</dt> <dt>-1</dt> </dl> | Nenhum item existe em uma caixa de listagem de seleção múltipla.<br/>                        |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa mensagem não tem nenhum valor de retorno.

## <a name="remarks"></a>Comentários

O procedimento de gancho deve especificar a constante **LBSELCHSTRING** em uma chamada para a função [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) para obter o identificador da mensagem enviada pela caixa de diálogo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Commdlg. h (incluir Windows. h)</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **LBSELCHSTRINGW** (Unicode) e **LBSELCHSTRINGA** (ANSI)<br/>                                    |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**\_SELCHANGE CDN**](cdn-selchange.md)
</dt> <dt>

[**\_TYPECHANGE CDN**](cdn-typechange.md)
</dt> <dt>

[**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Biblioteca de caixa de diálogo comum](common-dialog-box-library.md)
</dt> </dl>

