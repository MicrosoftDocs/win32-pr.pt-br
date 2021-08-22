---
title: CCM_SETWINDOWTHEME mensagem (Commctrl.h)
description: Define o estilo visual de um controle.
ms.assetid: 0200fa11-847f-477c-92e0-790b4d1ca0ef
keywords:
- CCM_SETWINDOWTHEME controles Windows mensagem
topic_type:
- apiref
api_name:
- CCM_SETWINDOWTHEME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4656290a861247dc474e46cb396314f762f0084f45ae60d32198aa7bb464f8d6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119320046"
---
# <a name="ccm_setwindowtheme-message"></a>Mensagem CCM \_ SETWINDOWTHEME

Define o estilo visual de um controle.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma cadeia de caracteres Unicode que contém o estilo visual de controle a ser definido.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno não é usado.

## <a name="remarks"></a>Comentários

> [!Note]  
> Para usar essa mensagem, você deve fornecer um manifesto especificando Comclt32.dll versão 6.0. Para obter mais informações sobre manifestos, consulte [Habilitando estilos visuais.](cookbook-overview.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





