---
title: TTM_GETMAXTIPWIDTH mensagem (Commctrl.h)
description: Recupera a largura máxima de uma janela de dica de ferramenta.
ms.assetid: 0f0a5403-fe2e-4e5a-96c2-a435827a5fd7
keywords:
- TTM_GETMAXTIPWIDTH controles de Windows mensagem
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
ms.openlocfilehash: bce561b254645932b214b48879aa0be04deb31b32e8dc591fc3183ec39871273
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119751046"
---
# <a name="ttm_getmaxtipwidth-message"></a>Mensagem TTM \_ GETMAXTIPWIDTH

Recupera a largura máxima de uma janela de dica de ferramenta.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um **valor INT** que representa a largura máxima da dica de ferramenta, em pixels. Se nenhuma largura máxima tiver sido definida anteriormente, a mensagem retornará -1.

## <a name="remarks"></a>Comentários

O valor máximo de largura da dica de ferramenta não indica a largura real de uma janela de dica de ferramenta. Em vez disso, se uma cadeia de caracteres de dica de ferramenta exceder a largura máxima, o controle divide o texto em várias linhas, usando espaços para determinar quebras de linha. Se o texto não puder ser segmentado em várias linhas, ele será exibido em uma única linha. O comprimento dessa linha pode exceder a largura máxima da dica de ferramenta.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**TTM \_ SETMAXTIPWIDTH**](ttm-setmaxtipwidth.md)
</dt> </dl>

 

 





