---
title: Mensagem de ICM_DECOMPRESS (VFW. h)
description: A \_ mensagem de DEScompactação ICM notifica um driver de descompactação de vídeo para descompactar um quadro de dados em um buffer definido pelo aplicativo.
ms.assetid: 666f2ebf-80a5-4846-861d-c79c3001c5a0
keywords:
- Multimídia do Windows de mensagem ICM_DECOMPRESS
topic_type:
- apiref
api_name:
- ICM_DECOMPRESS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c890a8ca15202f57fdaa02922e364af75f7b952
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009638"
---
# <a name="icm_decompress-message"></a>\_Mensagem de DEScompactação ICM

A mensagem de **\_ descompactação ICM** notifica um driver de descompactação de vídeo para descompactar um quadro de dados em um buffer definido pelo aplicativo.


```C++
ICM_DECOMPRESS 
wParam = (DWORD) (LPVOID) &icd; 
lParam = sizeof(ICDECOMPRESS); 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="icd"></span><span id="ICD"></span>*ICD*
</dt> <dd>

Ponteiro para uma estrutura [**ICDECOMPRESS**](/windows/desktop/api/Vfw/ns-vfw-icdecompress) .

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Tamanho, em bytes, de [**ICDECOMPRESS**](/windows/desktop/api/Vfw/ns-vfw-icdecompress).

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará ICERR \_ OK se for bem-sucedido ou um erro de outra forma.

## <a name="remarks"></a>Comentários

Se você quiser que o driver descompacte os dados diretamente na tela, envie a mensagem [**ICM \_ draw**](icm-draw.md) .

O driver retornará um erro se essa mensagem for recebida antes da mensagem de [**início do ICM \_ descompactar \_**](icm-decompress-begin.md) .

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

 

 





