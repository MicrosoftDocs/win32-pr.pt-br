---
title: Mensagem de STM_SETIMAGE (WinUser. h)
description: Um aplicativo envia uma \_ mensagem STM SetImage para associar uma nova imagem a um controle estático.
ms.assetid: d3e7c5d4-f621-40f6-9558-7fb699e8b489
keywords:
- Controles de STM_SETIMAGE de mensagens do Windows
topic_type:
- apiref
api_name:
- STM_SETIMAGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27c4f9c216d2e987727a1e2fa9bc6de12a823d52
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918118"
---
# <a name="stm_setimage-message"></a>\_Mensagem de imagem STM

Um aplicativo envia uma mensagem **STM \_ SetImage** para associar uma nova imagem a um controle estático.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica o tipo de imagem a ser associado ao controle estático. Esse parâmetro pode ser um dos seguintes valores:



| Valor                                                                                                                                                                     | Significado                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| <span id="IMAGE_BITMAP"></span><span id="image_bitmap"></span><dl> <dt>**BITMAP de imagem \_**</dt> </dl>                | Bitmap.<br/>            |
| <span id="IMAGE_CURSOR"></span><span id="image_cursor"></span><dl> <dt>**CURSOR de imagem \_**</dt> </dl>                | Posição.<br/>            |
| <span id="IMAGE_ENHMETAFILE"></span><span id="image_enhmetafile"></span><dl> <dt>**ENHMETAFILE de imagem \_**</dt> </dl> | Metarquivo avançado.<br/> |
| <span id="IMAGE_ICON"></span><span id="image_icon"></span><dl> <dt>**ícone de imagem \_**</dt> </dl>                      | Cone.<br/>              |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Manipule a imagem a ser associada ao controle estático.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de retorno é um identificador para a imagem associada anteriormente ao controle estático, se houver; caso contrário, será **nulo**.

## <a name="remarks"></a>Comentários

Para associar uma imagem a um controle estático, o controle deve ter o estilo adequado. A tabela a seguir mostra o estilo necessário para cada tipo de imagem.



| Tipo de imagem         | Estilo de controle estático |
|--------------------|----------------------|
| BITMAP de imagem \_      | \_bitmap SS           |
| CURSOR de imagem \_      | \_ícone SS             |
| ENHMETAFILE de imagem \_ | \_ENHMETAFILE SS      |
| ícone de imagem \_        | \_ícone SS             |



 

> [!IMPORTANT]
>
> Na versão 6 dos controles Microsoft Win32, um bitmap passado para um controle estático usando a mensagem **STM \_ SetImage** era o mesmo bitmap retornado por uma mensagem **STM \_ SetImage** subsequente. O cliente é responsável por excluir qualquer bitmap enviado para um controle estático.
>
> Com o Windows XP, se o bitmap passado na mensagem **STM \_ SetImage** contiver pixels com alfa diferente de zero, o controle estático usará uma cópia do bitmap. Esse bitmap copiado é retornado pela próxima mensagem do **STM \_ SetImage** . O código do cliente pode rastrear de forma independente os bitmaps passados para o controle estático, mas se ele não verificar e liberar os bitmaps retornados de mensagens **\_ SetImage de STM** , os bitmaps serão vazados.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**STM \_ GETimage**](stm-getimage.md)
</dt> </dl>

 

 





