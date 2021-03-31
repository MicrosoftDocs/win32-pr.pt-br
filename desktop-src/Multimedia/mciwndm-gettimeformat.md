---
title: Mensagem de MCIWNDM_GETTIMEFORMAT (VFW. h)
description: A \_ mensagem MCIWNDM GETTIMEFORMAT recupera o formato de hora atual de um dispositivo MCI em dois formulários como um valor numérico e como uma cadeia de caracteres. Você pode enviar essa mensagem explicitamente ou usando a macro MCIWndGetTimeFormat.
ms.assetid: 01844872-5444-4f3b-92a3-64f80b94d3a0
keywords:
- Multimídia do Windows de mensagem MCIWNDM_GETTIMEFORMAT
topic_type:
- apiref
api_name:
- MCIWNDM_GETTIMEFORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a09f969c009ff23bc0951ed2efbc0dbf7aa95dda
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644334"
---
# <a name="mciwndm_gettimeformat-message"></a>\_Mensagem MCIWNDM GETTIMEFORMAT

A mensagem **MCIWNDM \_ GETTIMEFORMAT** recupera o formato de hora atual de um dispositivo MCI em duas formas: como um valor numérico e uma cadeia de caracteres. Você pode enviar essa mensagem explicitamente ou usando a macro [**MCIWndGetTimeFormat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgettimeformat) .


```C++
MCIWNDM_GETTIMEFORMAT 
wParam = (WPARAM) (UINT) len; 
lParam = (LPARAM) (LPSTR) lp; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="len"></span><span id="LEN"></span>*Len*
</dt> <dd>

Tamanho, em bytes, do buffer.

</dd> <dt>

<span id="lp"></span><span id="LP"></span>*LP*
</dt> <dd>

Ponteiro para um buffer para conter a forma de cadeia de caracteres terminada em nulo do formato de hora.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retorna um inteiro correspondente à constante MCI que define o formato de hora.

## <a name="remarks"></a>Comentários

Se a cadeia de caracteres de formato de hora for maior do que o buffer de retorno, MCIWnd truncará a cadeia de caracteres.

Um dispositivo MCI pode dar suporte a um ou mais dos seguintes formatos de hora.



| Formato de hora                      | Constante MCI               |
|----------------------------------|----------------------------|
| Bytes                            | \_bytes de formato MCI \_         |
| Intervalos                           | \_quadros de formato MCI \_        |
| Horas, minutos, segundos          | \_formato MCI \_ HMS           |
| Milissegundos                     | \_milissegundos do formato MCI \_  |
| Minutos, segundos, quadros         | \_formato MCI \_ MSF           |
| Exemplos                          | \_exemplos de formato MCI \_       |
| SMPTE 24                         | \_Formato MCI \_ SMPTE \_ 24     |
| SMPTE 25                         | \_Formato MCI \_ SMPTE \_ 25     |
| Remoção de 30 do SMPTE                    | \_Formato MCI \_ SMPTE \_ 30DROP |
| SMPTE 30 (não descartar)              | \_Formato MCI \_ SMPTE \_ 30     |
| Faixas, minutos, segundos, quadros | \_formato MCI \_ TMSF          |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**MCIWndGetTimeFormat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgettimeformat)
</dt> </dl>

 

 





