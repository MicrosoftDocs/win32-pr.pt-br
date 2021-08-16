---
title: MCIWNDM_GETTIMEFORMAT mensagem (Vfw.h)
description: A mensagem GETTIMEFORMAT MCIWNDM recupera o formato de hora atual de um dispositivo MCI em duas formas como um valor numérico e \_ como uma cadeia de caracteres. Você pode enviar essa mensagem explicitamente ou usando a macro MCIWndGetTimeFormat.
ms.assetid: 01844872-5444-4f3b-92a3-64f80b94d3a0
keywords:
- MCIWNDM_GETTIMEFORMAT mensagem Windows Multimídia
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
ms.openlocfilehash: 3badb7c7722db6444d3bd928535790876e0a128e69e50323cea3fe39c2dd987a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117985904"
---
# <a name="mciwndm_gettimeformat-message"></a>Mensagem GETTIMEFORMAT MCIWNDM \_

A **mensagem \_ GETTIMEFORMAT MCIWNDM** recupera o formato de hora atual de um dispositivo MCI de duas formas: como um valor numérico e como uma cadeia de caracteres. Você pode enviar essa mensagem explicitamente ou usando a macro [**MCIWndGetTimeFormat.**](/windows/desktop/api/Vfw/nf-vfw-mciwndgettimeformat)


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

<span id="lp"></span><span id="LP"></span>*Lp*
</dt> <dd>

Ponteiro para um buffer para conter a forma de cadeia de caracteres terminada em nulo do formato de hora.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retorna um inteiro correspondente à constante MCI que define o formato de hora.

## <a name="remarks"></a>Comentários

Se a cadeia de caracteres de formato de tempo for maior que o buffer de retorno, o MCIWnd truncará a cadeia de caracteres.

Um dispositivo MCI pode dar suporte a um ou mais dos formatos de hora a seguir.



| Formato de hora                      | Constante MCI               |
|----------------------------------|----------------------------|
| Bytes                            | BYTES DE FORMATO \_ MCI \_         |
| Quadros                           | QUADROS DE FORMATO MCI \_ \_        |
| Horas, minutos, segundos          | FORMATO MCI \_ \_ HMS           |
| Milissegundos                     | FORMATO MCI \_ \_ MILISSEGUNDOS  |
| Minutos, segundos, quadros         | \_MSF DE \_ FORMATO MCI           |
| Exemplos                          | EXEMPLOS DE FORMATO MCI \_ \_       |
| SMPTE 24                         | FORMATO MCI \_ \_ SMPTE \_ 24     |
| SMPTE 25                         | FORMATO MCI \_ \_ SMPTE \_ 25     |
| SMPTE 30 drop                    | MCI \_ FORMAT \_ SMPTE \_ 30DROP |
| SMPTE 30 (não drop)              | FORMATO MCI \_ \_ SMPTE \_ 30     |
| Faixas, minutos, segundos, quadros | TMSF DE \_ \_ FORMATO MCI          |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MCIWndGetTimeFormat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgettimeformat)
</dt> </dl>

 

 





