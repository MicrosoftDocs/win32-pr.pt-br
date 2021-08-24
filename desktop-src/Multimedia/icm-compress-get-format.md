---
title: Mensagem de ICM_COMPRESS_GET_FORMAT (VFW. h)
description: o ICM \_ compactar \_ obter \_ mensagem de formato solicita o formato de saída dos dados compactados de um driver de compactação de vídeo. Você pode enviar essa mensagem explicitamente ou usando a macro ICCompressGetFormat.
ms.assetid: ac12d415-bad5-4838-b206-09c8097d3fd9
keywords:
- mensagem de ICM_COMPRESS_GET_FORMAT Windows multimídia
topic_type:
- apiref
api_name:
- ICM_COMPRESS_GET_FORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ac1bf9b3c9a3ae0535da008786bf8baef19c8b51e27446b84e4b95805a1c4a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119785026"
---
# <a name="icm_compress_get_format-message"></a>ICM \_ COMPACTar a \_ \_ mensagem obter formato

o **ICM \_ compactar \_ obter \_** mensagem de formato solicita o formato de saída dos dados compactados de um driver de compactação de vídeo. Você pode enviar essa mensagem explicitamente ou usando a macro [**ICCompressGetFormat**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetformat) .


```C++
ICM_COMPRESS_GET_FORMAT 
wParam = (DWORD_PTR) (LPVOID) lpbiInput; 
lParam = (DWORD_PTR) (LPVOID) lpbiOutput; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*
</dt> <dd>

Ponteiro para uma estrutura [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) que contém o formato de entrada.

</dd> <dt>

<span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*lpbiOutput*
</dt> <dd>

Ponteiro para uma estrutura [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) para conter o formato de saída. Você pode especificar zero para esse parâmetro para solicitar apenas o tamanho do formato de saída, como na macro [**ICCompressGetFormatSize**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetformatsize) .

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Se *lpbiOutput* for zero, retornará o tamanho da estrutura.

Se *lpbiOutput* for diferente de zero, retornará ICERR \_ OK se for bem-sucedido ou um erro de outra forma.

## <a name="remarks"></a>Comentários

Se *lpbiOutput* for diferente de zero, o driver deverá preencher a estrutura [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) com o formato de saída padrão correspondente ao formato de entrada especificado para *lpbiInput*. Se o compressor puder produzir vários formatos, o formato padrão deverá ser o que preserva a maior quantidade de informações.

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

 

