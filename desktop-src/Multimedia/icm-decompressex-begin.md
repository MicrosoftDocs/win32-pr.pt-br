---
title: Mensagem de ICM_DECOMPRESSEX_BEGIN (VFW. h)
description: A \_ mensagem ICM DECOMPRESSEX \_ begin notifica um driver de compactação de vídeo para se preparar para descompactar dados.
ms.assetid: 35298274-91b5-4df0-b4b0-4a71d6a49990
keywords:
- Multimídia do Windows de mensagem ICM_DECOMPRESSEX_BEGIN
topic_type:
- apiref
api_name:
- ICM_DECOMPRESSEX_BEGIN
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77ea082c91d48a9964348b762ce13631cd80af30
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645013"
---
# <a name="icm_decompressex_begin-message"></a>\_Iniciar mensagem de DECOMPRESSEX de ICM \_

A mensagem **ICM \_ DECOMPRESSEX \_ begin** notifica um driver de compactação de vídeo para se preparar para descompactar dados.


```C++
ICM_DECOMPRESSEX_BEGIN 
wParam = (DWORD_PTR) (LPVOID) &icdex; 
lParam = sizeof(ICDECOMPRESSEX); 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="icdex"></span><span id="ICDEX"></span>*icdex*
</dt> <dd>

Ponteiro para uma estrutura [**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex) que contém os formatos de entrada e saída.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Tamanho, em bytes, de [**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex).

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará ICERR \_ OK se a descompactação especificada for suportada ou ICERR \_ BADFORMAT do contrário.

## <a name="remarks"></a>Comentários

Quando o driver recebe essa mensagem, ele deve alocar buffers e realizar operações demoradas para que possa processar mensagens [**\_ DECOMPRESSEX de ICM**](icm-decompressex.md) com eficiência.

Se você quiser que o driver descompacte os dados diretamente na tela, envie a mensagem de [**\_ \_ início de desenho ICM**](icm-draw-begin.md) .

As mensagens **ICM \_ DECOMPRESSEX \_ begin** e [**ICM \_ DECOMPRESSEX \_ end**](icm-decompressex-end.md) não são aninhadas. Se o driver receber o **ICM \_ DECOMPRESSEX \_ begin** antes da descompactação ser interrompida com o **ICM \_ DECOMPRESSEX \_ end**, ele deverá reiniciar a descompactação com novos parâmetros.

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

 

 





