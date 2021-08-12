---
title: BM_SETIMAGE mensagem (Winuser.h)
description: Associa uma nova imagem (ícone ou bitmap) ao botão.
ms.assetid: bf05e684-63d0-4583-960b-f329edafb151
keywords:
- BM_SETIMAGE controles Windows mensagem
topic_type:
- apiref
api_name:
- BM_SETIMAGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b8948c73c04d3b01230a47ab91529764c9e20281e4f45803f71d82f59dedb14
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118674809"
---
# <a name="bm_setimage-message"></a>Mensagem \_ BM SETIMAGE

Associa uma nova imagem (ícone ou bitmap) ao botão.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O tipo de imagem a ser associado ao botão. Esse parâmetro pode ser um dos seguintes valores:

-   BITMAP \_ DE IMAGEM
-   ÍCONE DE \_ IMAGEM

</dd> <dt>

*lParam* 
</dt> <dd>

Um handle (**HICON** ou **HBITMAP**) para a imagem a ser associada ao botão.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno é um handle para a imagem associada anteriormente ao botão, se for o caso; caso contrário, será **NULL.**

## <a name="remarks"></a>Comentários

A aparência do texto, um ícone ou ambos em um controle de botão depende dos estilos [**BS \_ ICON**](button-styles.md) e [**\_ BS BITMAP**](button-styles.md) e se a mensagem **\_ BM SETIMAGE** é chamada. Os resultados possíveis são os seguinte:



| ÍCONE BS \_ ou Conjunto de \_ BITMAP BS? | BM \_ SETIMAGE chamado? | Result              |
|-----------------------------|----------------------|---------------------|
| Sim                         | Sim                  | Mostrar somente ícone.     |
| Não                          | Sim                  | Mostrar ícone e texto. |
| Sim                         | Não                   | Mostrar somente texto.     |
| Não                          | Não                   | Mostrar somente texto      |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**BM \_ GETIMAGE**](bm-getimage.md)
</dt> </dl>

 

 





