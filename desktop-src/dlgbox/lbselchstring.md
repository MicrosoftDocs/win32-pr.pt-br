---
title: Mensagem de LBSELCHSTRING (Commdlg. h)
description: Uma caixa de diálogo abrir ou salvar como envia a mensagem registrada LBSELCHSTRING para o procedimento de gancho quando a seleção é alterada em qualquer uma das caixas de listagem ou caixas de combinação da caixa de diálogo.
ms.assetid: 3a8ebc63-b324-43ed-bb6f-34779f6043e7
keywords:
- Caixas de diálogo de mensagem LBSELCHSTRING
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
ms.openlocfilehash: 137429b8fa7eb29fb96ec579e0240c4c282d0766
ms.sourcegitcommit: 8e083a10b3a480dec8a8d74dbd5889f49dea15e4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/17/2021
ms.locfileid: "107590763"
---
# <a name="lbselchstring-message"></a>Mensagem LBSELCHSTRING

\[A partir do Windows Vista, as caixas de diálogo **abrir** e **salvar como** comuns foram substituídas pela [caixa de diálogo de item comum](/windows/win32/shell/common-file-dialog). Recomendamos que você use a API de caixa de diálogo de item comum em vez dessas caixas de diálogo da biblioteca de caixas de diálogo comuns.\]

Uma caixa de diálogo **abrir** ou **salvar como** envia a mensagem registrada **LBSELCHSTRING** para o procedimento de gancho quando a seleção é alterada em qualquer uma das caixas de listagem ou caixas de combinação da caixa de diálogo.


```C++
#define LBSELCHSTRING TEXT("commdlg_LBSelChangedNotify")
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O identificador da caixa de listagem ou da caixa de combinação na qual a seleção foi alterada.

</dd> <dt>

*lParam* 
</dt> <dd>

A palavra de ordem inferior Especifica o número de item da cadeia de caracteres selecionada na caixa de listagem ou na caixa de combinação. A palavra de ordem superior especifica o tipo de alteração de seleção. Esse parâmetro pode usar um dos valores a seguir.



| Valor                                                                                                                                                                                                                       | Significado                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="CD_LBSELCHANGE"></span><span id="cd_lbselchange"></span><dl> <dt>**CD \_ LBSELCHANGE**</dt> <dt>0</dt> </dl>     | O item é o único item selecionado em uma caixa de listagem de seleção única.<br/>      |
| <span id="CD_LBSELADD"></span><span id="cd_lbseladd"></span><dl> <dt>**CD \_ LBSELADD**</dt> <dt>2</dt> </dl>              | O item é um dos itens selecionados em uma caixa de listagem de seleção múltipla.<br/> |
| <span id="CD_LBSELSUB"></span><span id="cd_lbselsub"></span><dl> <dt>**CD \_ LBSELSUB**</dt> <dt>1</dt> </dl>              | O item não está mais selecionado em uma caixa de listagem de seleção múltipla.<br/>        |
| <span id="CD_LBSELNOITEMS"></span><span id="cd_lbselnoitems"></span><dl> <dt>**CD \_ LBSELNOITEMS**</dt> <dt>-1</dt> </dl> | Não existem itens em uma caixa de listagem de seleção múltipla.<br/>                        |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esta mensagem não tem nenhum valor de retorno.

## <a name="remarks"></a>Comentários

O procedimento de gancho deve especificar a constante **LBSELCHSTRING** em uma chamada para a função [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) para obter o identificador para a mensagem enviada pela caixa de diálogo.

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

 

