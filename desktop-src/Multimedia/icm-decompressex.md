---
title: Mensagem de ICM_DECOMPRESSEX (VFW. h)
description: A \_ mensagem ICM DECOMPRESSEX notifica um driver de compactação de vídeo para descompactar um quadro de dados diretamente na tela, descompactar para um DIB de cabeça para baixo ou descompactar imagens descritas com retângulos de origem e de destino.
ms.assetid: ed253280-c246-4e86-91f1-ad1e1132d732
keywords:
- Multimídia do Windows de mensagem ICM_DECOMPRESSEX
topic_type:
- apiref
api_name:
- ICM_DECOMPRESSEX
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d33451547bc598250a97e73682712e157aa13a5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009637"
---
# <a name="icm_decompressex-message"></a>\_Mensagem DECOMPRESSEX de ICM

A mensagem **ICM \_ DECOMPRESSEX** notifica um driver de compactação de vídeo para descompactar um quadro de dados diretamente na tela, descompactar para um DIB de cabeça para baixo ou descompactar imagens descritas com retângulos de origem e de destino.


```C++
ICM_DECOMPRESSEX 
wParam = (DWORD_PTR) (LPVOID) &icdex; 
lParam = sizeof(ICDECOMPRESSEX); 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="icdex"></span><span id="ICDEX"></span>*icdex*
</dt> <dd>

Ponteiro para uma estrutura [**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex) .

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Tamanho, em bytes, de [**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex).

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará ICERR \_ OK se for bem-sucedido ou um erro de outra forma.

## <a name="remarks"></a>Comentários

Essa mensagem é semelhante à [**\_ descompactação de ICM**](icm-decompress.md) , exceto pelo fato de que ela usa a estrutura [**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex) para definir suas informações de descompactação.

Se você quiser que o driver descompacte os dados diretamente na tela, envie a mensagem [**ICM \_ draw**](icm-draw.md) .

O driver retornará um erro se essa mensagem for recebida antes da mensagem de [**\_ \_ início de DECOMPRESSEX do ICM**](icm-decompressex-begin.md) .

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

 

 





