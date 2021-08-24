---
title: STM_SETIMAGE mensagem (Winuser.h)
description: Um aplicativo envia uma mensagem \_ STM SETIMAGE para associar uma nova imagem a um controle estático.
ms.assetid: d3e7c5d4-f621-40f6-9558-7fb699e8b489
keywords:
- STM_SETIMAGE controles de Windows mensagem
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
ms.openlocfilehash: d48cc8aeb5e28ac67a6bbe25636be1a2f6f9b89f225568be02e517e1ad04dc55
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119078450"
---
# <a name="stm_setimage-message"></a>Mensagem STM \_ SETIMAGE

Um aplicativo envia uma **mensagem \_ STM SETIMAGE** para associar uma nova imagem a um controle estático.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica o tipo de imagem a ser associado ao controle estático. Esse parâmetro pode ser um dos seguintes valores:



| Valor                                                                                                                                                                     | Significado                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| <span id="IMAGE_BITMAP"></span><span id="image_bitmap"></span><dl> <dt>**BITMAP \_ DE IMAGEM**</dt> </dl>                | Bitmap.<br/>            |
| <span id="IMAGE_CURSOR"></span><span id="image_cursor"></span><dl> <dt>**CURSOR \_ DE IMAGEM**</dt> </dl>                | Cursor.<br/>            |
| <span id="IMAGE_ENHMETAFILE"></span><span id="image_enhmetafile"></span><dl> <dt>**IMAGE \_ EN LTDAFILE**</dt> </dl> | Metadados aprimorados.<br/> |
| <span id="IMAGE_ICON"></span><span id="image_icon"></span><dl> <dt>**ÍCONE DE \_ IMAGEM**</dt> </dl>                      | Ícone.<br/>              |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Lidar com a imagem a ser associada ao controle estático.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno é um lidar com a imagem associada anteriormente ao controle estático, se for o caso; caso contrário, será **NULL.**

## <a name="remarks"></a>Comentários

Para associar uma imagem a um controle estático, o controle deve ter o estilo adequado. A tabela a seguir mostra o estilo necessário para cada tipo de imagem.



| Tipo de imagem         | Estilo de controle estático |
|--------------------|----------------------|
| BITMAP \_ DE IMAGEM      | SS \_ BITMAP           |
| CURSOR \_ DE IMAGEM      | ÍCONE DO \_ SS             |
| IMAGE \_ EN LTDAFILE | SS \_ EN LTDAFILE      |
| ÍCONE DE \_ IMAGEM        | ÍCONE DO \_ SS             |



 

> [!IMPORTANT]
>
> Na versão 6 dos controles do Microsoft Win32, um bitmap passado para um controle estático usando a mensagem **\_ STM SETIMAGE** era o mesmo bitmap retornado por uma mensagem **\_ SETIMAGE stm** subsequente. O cliente é responsável por excluir qualquer bitmap enviado a um controle estático.
>
> Com Windows XP, se o bitmap passado na mensagem **\_ STM SETIMAGE** contiver pixels com alfa diferente de zero, o controle estático recebe uma cópia do bitmap. Esse bitmap copiado é retornado pela próxima **mensagem \_ SETIMAGE do STM.** O código do cliente pode controlar independentemente os bitmaps passados para o controle estático, mas se ele não verificar e liberar os bitmaps retornados das mensagens **\_ STM SETIMAGE,** os bitmaps serão vazados.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**STM \_ GETIMAGE**](stm-getimage.md)
</dt> </dl>

 

 





