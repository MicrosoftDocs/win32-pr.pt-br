---
title: WM_CAP_FILE_SAVEAS mensagem (Vfw.h)
description: A mensagem WM \_ CAP \_ FILE \_ SAVEAS copia o conteúdo do arquivo de captura para outro arquivo. Você pode enviar essa mensagem explicitamente ou usando a macro capFileSaveAs.
ms.assetid: fab37bee-3160-4ebc-b58f-46021ed49b55
keywords:
- WM_CAP_FILE_SAVEAS mensagem Windows Multimídia
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
ms.openlocfilehash: a200b8e73d81072961ec4e6aa7c8e1dd989bf2d8c3e0480c75908a8761ee93b1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119687006"
---
# <a name="wm_cap_file_saveas-message"></a>Mensagem WM \_ CAP \_ FILE \_ SAVEAS

A **mensagem WM CAP FILE \_ \_ \_ SAVEAS** copia o conteúdo do arquivo de captura para outro arquivo. Você pode enviar essa mensagem explicitamente ou usando a [**macro capFileSaveAs.**](/windows/desktop/api/Vfw/nf-vfw-capfilesaveas)


```C++
WM_CAP_FILE_SAVEAS 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*Szname*
</dt> <dd>

Ponteiro para a cadeia de caracteres terminada em nulo que contém o nome do arquivo de destino usado para copiar o arquivo.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará **TRUE se** for bem-sucedido **ou FALSE** caso contrário.

Se ocorrer um erro e uma função de retorno de chamada de erro for definida usando a mensagem [**WM \_ CAP SET \_ \_ CALLBACK \_ ERROR,**](wm-cap-set-callback-error.md) a função de retorno de chamada de erro será chamada.

## <a name="remarks"></a>Comentários

Essa mensagem não altera o nome ou o conteúdo do arquivo de captura atual.

Se a operação de cópia não for bem-sucedida devido a um erro de disco completo, o arquivo de destino será excluído automaticamente.

Normalmente, um arquivo de captura é pré-alocado para o maior segmento de captura previsto e apenas uma parte dele pode ser usada para capturar dados. Essa mensagem copia apenas a parte do arquivo que contém os dados de captura.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Captura de vídeo](video-capture.md)
</dt> <dt>

[Mensagens de captura de vídeo](video-capture-messages.md)
</dt> </dl>

 

 





