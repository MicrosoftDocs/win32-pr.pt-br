---
title: Mensagem de ICM_DRAW_BEGIN (VFW. h)
description: A \_ mensagem de início de desenho ICM \_ Notifica um driver de renderização para se preparar para desenhar dados.
ms.assetid: e5ecd7dd-376b-422c-bbb8-4e7c41e3cac8
keywords:
- Multimídia do Windows de mensagem ICM_DRAW_BEGIN
topic_type:
- apiref
api_name:
- ICM_DRAW_BEGIN
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db7b9e20a0b0621038e1c7e092a871a6727566cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918952"
---
# <a name="icm_draw_begin-message"></a>Mensagem de início de \_ desenho ICM \_

A mensagem de **\_ \_ início de desenho ICM** notifica um driver de renderização para se preparar para desenhar dados.


```C++
ICM_DRAW_BEGIN 
wParam = (DWORD) (LPVOID) &icdrwBgn; 
lParam = sizeof(ICDRAW); 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="icdrwBgn"></span><span id="icdrwbgn"></span><span id="ICDRWBGN"></span>*icdrwBgn*
</dt> <dd>

Ponteiro para uma estrutura [**ICDRAWBEGIN**](/windows/desktop/api/Vfw/ns-vfw-icdrawbegin) que contém o formato de entrada.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Tamanho, em bytes, de **ICDRAWBEGIN**.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará ICERR \_ OK se o driver der suporte a desenhar os dados na tela na maneira e no formato especificados, ou então um código de erro. Os possíveis valores de erro incluem o seguinte.



| Valor               | Significado                                                                       |
|---------------------|-------------------------------------------------------------------------------|
| ICERR \_ BADFORMAT    | Não há suporte para o formato de entrada ou saída.                                      |
| ICERR \_ sem suporte | O driver não é desenhado diretamente na tela ou não oferece suporte a essa mensagem. |



 

## <a name="remarks"></a>Comentários

Se você quiser que o driver Descompacte dados em um buffer, envie a mensagem de [**\_ \_ início de descompactação ICM**](icm-decompress-begin.md) .

As mensagens de final **ICM \_ draw \_ begin** e [**ICM \_ draw \_**](icm-draw-end.md) não são aninhadas. Se o driver receber o **início de ICM e \_ \_ começar** antes que a descompactação seja interrompida com a **\_ \_ extremidade de desenho ICM**, ela deverá reiniciar a descompactação com novos parâmetros.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Gerenciador de compactação de vídeo](video-compression-manager.md)
</dt> <dt>

[Mensagens de compactação de vídeo](video-compression-messages.md)
</dt> </dl>

 

 





