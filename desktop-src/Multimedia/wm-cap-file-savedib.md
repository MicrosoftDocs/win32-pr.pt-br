---
title: WM_CAP_FILE_SAVEDIB mensagem (Vfw.h)
description: A mensagem WM \_ CAP \_ FILE \_ SAVEDIB copia o quadro atual para um arquivo DIB. Você pode enviar essa mensagem explicitamente ou usando a macro capFileSaveDIB.
ms.assetid: bf6d343b-9236-4e68-bbda-2ed6e197a5cb
keywords:
- WM_CAP_FILE_SAVEDIB mensagem Windows Multimídia
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
ms.openlocfilehash: 66d6dd9b8675e1fb8625349afc4b3f86347d71d605407d5c99fbca291ade744d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119803806"
---
# <a name="wm_cap_file_savedib-message"></a>Mensagem WM \_ CAP \_ FILE \_ SAVEDIB

A **mensagem WM CAP FILE \_ \_ \_ SAVEDIB** copia o quadro atual para um arquivo DIB. Você pode enviar essa mensagem explicitamente ou usando a [**macro capFileSaveDIB.**](/windows/desktop/api/Vfw/nf-vfw-capfilesavedib)


```C++
WM_CAP_FILE_SAVEDIB 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*Szname*
</dt> <dd>

Ponteiro para a cadeia de caracteres terminada em nulo que contém o nome do arquivo DIB de destino.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará **TRUE se** for bem-sucedido **ou FALSE** caso contrário.

Se ocorrer um erro e uma função de retorno de chamada de erro for definida usando a mensagem [**WM \_ CAP SET \_ \_ CALLBACK \_ ERROR,**](wm-cap-set-callback-error.md) a função de retorno de chamada de erro será chamada.

## <a name="remarks"></a>Comentários

Se o driver de captura fornece quadros em um formato compactado, essa chamada tenta descompactar o quadro antes de escrever o arquivo.

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

 

 





