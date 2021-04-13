---
title: Mensagem de WM_CAP_FILE_SAVEDIB (VFW. h)
description: A \_ mensagem do arquivo SAVEDIB do WM Cap \_ \_ copia o quadro atual para um arquivo DIB. Você pode enviar essa mensagem explicitamente ou usando a macro capFileSaveDIB.
ms.assetid: bf6d343b-9236-4e68-bbda-2ed6e197a5cb
keywords:
- Multimídia do Windows de mensagem WM_CAP_FILE_SAVEDIB
topic_type:
- apiref
api_name:
- WM_CAP_FILE_SAVEDIB
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2155febfdac1b3f24133df47ce206c8e5ec33d3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455927"
---
# <a name="wm_cap_file_savedib-message"></a>\_ \_ Mensagem SAVEDIB do arquivo do WM Cap \_

A mensagem do **\_ \_ arquivo \_ SAVEDIB do WM Cap** copia o quadro atual para um arquivo DIB. Você pode enviar essa mensagem explicitamente ou usando a macro [**capFileSaveDIB**](/windows/desktop/api/Vfw/nf-vfw-capfilesavedib) .


```C++
WM_CAP_FILE_SAVEDIB 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*
</dt> <dd>

Ponteiro para a cadeia de caracteres terminada em nulo que contém o nome do arquivo DIB de destino.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará **true** se for bem-sucedido ou **false** caso contrário.

Se ocorrer um erro e uma função de retorno de chamada de erro for definida usando a mensagem de [**erro de retorno de chamada do WM \_ Cap \_ set \_ \_**](wm-cap-set-callback-error.md) , a função de retorno de chamada de erro será chamada.

## <a name="remarks"></a>Comentários

Se o driver de captura fornecer quadros em um formato compactado, essa chamada tentará descompactar o quadro antes de gravar o arquivo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Captura de vídeo](video-capture.md)
</dt> <dt>

[Mensagens de captura de vídeo](video-capture-messages.md)
</dt> </dl>

 

 





