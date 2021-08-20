---
title: ICM_COMPRESS_FRAMES_INFO mensagem (Vfw.h)
description: A ICM COMPRESS FRAMES INFO notifica um driver de compactação para definir os parâmetros para \_ \_ a \_ compactação pendente.
ms.assetid: d2f6f3b7-dff6-4fef-a642-cb77b00119af
keywords:
- ICM_COMPRESS_FRAMES_INFO mensagem Windows Multimídia
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
ms.openlocfilehash: 2382a930b0ce12e212adf78ddaf3c7e1b3300e47597b4671d0eae223cb536f73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118140907"
---
# <a name="icm_compress_frames_info-message"></a>\_ICM Mensagem COMPRESS \_ FRAMES \_ INFO

A **ICM \_ COMPRESS \_ FRAMES \_ INFO** notifica um driver de compactação para definir os parâmetros para a compactação pendente.


```C++
ICM_COMPRESS_FRAMES_INFO 
wParam = (DWORD) (LPVOID) &icf; 
lParam = sizeof(ICCOMPRESSFRAMES); 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="icf"></span><span id="ICF"></span>*Icf*
</dt> <dd>

Ponteiro para uma [**estrutura ICCOMPRESSFRAMES.**](/windows/desktop/api/Vfw/ns-vfw-iccompressframes) Os **membros GetData** e **PutData** dessa estrutura não são usados com essa mensagem.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*Lparam*
</dt> <dd>

Tamanho, em bytes, [**de ICCOMPRESSFRAMES.**](/windows/desktop/api/Vfw/ns-vfw-iccompressframes)

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará ICERR \_ OK se for bem-sucedido ou se um erro for o contrário.

## <a name="remarks"></a>Comentários

Um grupo pode usar essa mensagem para determinar quanto espaço alocar para cada quadro durante a compactação.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Gerenciador de Compactação de Vídeo](video-compression-manager.md)
</dt> <dt>

[Mensagens de compactação de vídeo](video-compression-messages.md)
</dt> </dl>

 

 





