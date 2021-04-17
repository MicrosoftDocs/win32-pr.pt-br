---
title: Mensagem de ICM_COMPRESS_FRAMES_INFO (VFW. h)
description: A \_ mensagem de informações de quadros de compactação ICM \_ \_ Notifica um driver de compactação para definir os parâmetros para a compactação pendente.
ms.assetid: d2f6f3b7-dff6-4fef-a642-cb77b00119af
keywords:
- Multimídia do Windows de mensagem ICM_COMPRESS_FRAMES_INFO
topic_type:
- apiref
api_name:
- ICM_COMPRESS_FRAMES_INFO
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbb6df0eab7706ebfc03a5e3069d4323be26ecdb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455729"
---
# <a name="icm_compress_frames_info-message"></a>\_Mensagem de \_ informações de quadros de COMPACTação ICM \_

A mensagem de **\_ informações de \_ quadros \_ de compactação ICM** notifica um driver de compactação para definir os parâmetros para a compactação pendente.


```C++
ICM_COMPRESS_FRAMES_INFO 
wParam = (DWORD) (LPVOID) &icf; 
lParam = sizeof(ICCOMPRESSFRAMES); 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="icf"></span><span id="ICF"></span>*ICF*
</dt> <dd>

Ponteiro para uma estrutura [**ICCOMPRESSFRAMES**](/windows/desktop/api/Vfw/ns-vfw-iccompressframes) . Os membros **GetData** e **PutData** dessa estrutura não são usados com esta mensagem.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Tamanho, em bytes, de [**ICCOMPRESSFRAMES**](/windows/desktop/api/Vfw/ns-vfw-iccompressframes).

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará ICERR \_ OK se for bem-sucedido ou um erro de outra forma.

## <a name="remarks"></a>Comentários

Um compressor pode usar essa mensagem para determinar a quantidade de espaço a ser alocada para cada quadro durante a compactação.

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

 

 





