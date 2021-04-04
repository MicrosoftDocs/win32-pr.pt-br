---
title: Mensagem de TTM_GETMAXTIPWIDTH (commctrl. h)
description: Recupera a largura máxima de uma janela de dica de ferramenta.
ms.assetid: 0f0a5403-fe2e-4e5a-96c2-a435827a5fd7
keywords:
- Controles de TTM_GETMAXTIPWIDTH de mensagens do Windows
topic_type:
- apiref
api_name:
- TTM_GETMAXTIPWIDTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f89c56692db9d451eb18db61af262cc0f3a715f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918468"
---
# <a name="ttm_getmaxtipwidth-message"></a>\_Mensagem TTM GETMAXTIPWIDTH

Recupera a largura máxima de uma janela de dica de ferramenta.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor **int** que representa a largura máxima da dica de ferramenta, em pixels. Se nenhuma largura máxima tiver sido definida anteriormente, a mensagem retornará-1.

## <a name="remarks"></a>Comentários

O valor máximo da largura da dica de ferramenta não indica a largura real da janela de dica de ferramenta. Em vez disso, se uma cadeia de dica de ferramenta exceder a largura máxima, o controle quebrará o texto em várias linhas, usando espaços para determinar as quebras de linha. Se o texto não puder ser segmentado em várias linhas, ele será exibido em uma única linha. O comprimento dessa linha pode exceder a largura máxima da dica de ferramenta.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**TTM \_ SETMAXTIPWIDTH**](ttm-setmaxtipwidth.md)
</dt> </dl>

 

 





