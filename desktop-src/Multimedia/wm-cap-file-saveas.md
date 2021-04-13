---
title: Mensagem de WM_CAP_FILE_SAVEAS (VFW. h)
description: A \_ \_ mensagem arquivo de salvamento da Cap do WM \_ copia o conteúdo do arquivo de captura para outro arquivo. Você pode enviar essa mensagem explicitamente ou usando a macro capFileSaveAs.
ms.assetid: fab37bee-3160-4ebc-b58f-46021ed49b55
keywords:
- Multimídia do Windows de mensagem WM_CAP_FILE_SAVEAS
topic_type:
- apiref
api_name:
- WM_CAP_FILE_SAVEAS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aca099fefab7ca0f4ef391b1b65e89938a947a01
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369416"
---
# <a name="wm_cap_file_saveas-message"></a>\_Mensagem de \_ salvamento de arquivo do WM Cap \_

A **mensagem \_ \_ arquivo de \_ salvamento da Cap do WM** copia o conteúdo do arquivo de captura para outro arquivo. Você pode enviar essa mensagem explicitamente ou usando a macro [**capFileSaveAs**](/windows/desktop/api/Vfw/nf-vfw-capfilesaveas) .


```C++
WM_CAP_FILE_SAVEAS 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*
</dt> <dd>

Ponteiro para a cadeia de caracteres terminada em nulo que contém o nome do arquivo de destino usado para copiar o arquivo.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará **true** se for bem-sucedido ou **false** caso contrário.

Se ocorrer um erro e uma função de retorno de chamada de erro for definida usando a mensagem de [**erro de retorno de chamada do WM \_ Cap \_ set \_ \_**](wm-cap-set-callback-error.md) , a função de retorno de chamada de erro será chamada.

## <a name="remarks"></a>Comentários

Essa mensagem não altera o nome ou o conteúdo do arquivo de captura atual.

Se a operação de cópia não for bem-sucedida devido a um erro de disco cheio, o arquivo de destino será excluído automaticamente.

Normalmente, um arquivo de captura é pré-alocado para o maior segmento de captura previsto e apenas uma parte dele pode ser usada para capturar dados. Essa mensagem copia apenas a parte do arquivo que contém os dados de captura.

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

 

 





