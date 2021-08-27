---
title: RB_GETBANDMARGINS mensagem (Commctrl.h)
description: Recupera as margens de uma banda.
ms.assetid: 262f4180-53f9-428f-9360-75b762470270
keywords:
- RB_GETBANDMARGINS controles de Windows mensagem
topic_type:
- apiref
api_name:
- RB_GETBANDMARGINS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7975e843417b8a47d90d011ad9a4b5367abdad2aa096f1a9652ba1cf704ddebf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120085096"
---
# <a name="rb_getbandmargins-message"></a>Mensagem \_ GETBANDMARGINS RB

Recupera as margens de uma banda.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma [**estrutura MARGINS**](/windows/desktop/api/Uxtheme/ns-uxtheme-margins) que recebe as margens recuperadas.

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
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





