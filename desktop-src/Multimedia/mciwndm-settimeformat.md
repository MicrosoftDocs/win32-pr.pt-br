---
title: MCIWNDM_SETTIMEFORMAT mensagem (Vfw.h)
description: A mensagem MCIWNDM \_ SETTIMEFORMAT define o formato de hora de um dispositivo MCI. Você pode enviar essa mensagem explicitamente ou usando a macro MCIWndSetTimeFormat.
ms.assetid: 7de82094-6d35-44fd-88e7-ebd18a558cfd
keywords:
- MCIWNDM_SETTIMEFORMAT mensagem Windows Multimídia
topic_type:
- apiref
api_name:
- MCIWNDM_SETTIMEFORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79620aecba07b11ed63dfc43fd2d70b41728586b36649b4b13aace9d1364197c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117802890"
---
# <a name="mciwndm_settimeformat-message"></a>Mensagem MCIWNDM \_ SETTIMEFORMAT

A **mensagem MCIWNDM \_ SETTIMEFORMAT** define o formato de hora de um dispositivo MCI. Você pode enviar essa mensagem explicitamente ou usando a macro [**MCIWndSetTimeFormat.**](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimeformat)


```C++
MCIWNDM_SETTIMEFORMAT 
wParam = 0; 
lParam = (LPARAM) (LPSTR) lp; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="lp"></span><span id="LP"></span>*Lp*
</dt> <dd>

Ponteiro para um buffer que contém a cadeia de caracteres terminada em nulo que indica o formato de hora. Especifique "quadros" para definir o formato de hora como quadros ou "ms" para definir o formato de hora como milissegundos.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará zero se for bem-sucedido ou um erro, caso contrário.

## <a name="remarks"></a>Comentários

Um aplicativo pode especificar formatos de tempo diferentes de quadros ou milissegundos, desde que os formatos sejam suportados pelo dispositivo MCI. Formatos nãocontinuos, como faixas e SMPTE, podem fazer com que a barra de faixa se comporte de maneira desinstante. Para esses formatos de hora, talvez você queira desativar a barra de ferramentas usando a macro [**MCIWndChangeStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndchangestyles) e especificando o estilo de janela MCIWNDF \_ NOPLAYBAR.

Se você quiser definir o formato de tempo como quadros ou milissegundos, também poderá usar a macro [**MCIWndUseFrames**](/windows/desktop/api/Vfw/nf-vfw-mciwnduseframes) ou [**MCIWndUseTime.**](/windows/desktop/api/Vfw/nf-vfw-mciwndusetime) Para ver uma lista de formatos de hora, consulte a macro [**MCIWndGetTimeFormat.**](/windows/desktop/api/Vfw/nf-vfw-mciwndgettimeformat)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MCIWndChangeStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndchangestyles)
</dt> <dt>

[**MCIWndGetTimeFormat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgettimeformat)
</dt> <dt>

[**MCIWndSetTimeFormat**](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimeformat)
</dt> <dt>

[**MCIWndUseFrames**](/windows/desktop/api/Vfw/nf-vfw-mciwnduseframes)
</dt> <dt>

[**MCIWndUseTime**](/windows/desktop/api/Vfw/nf-vfw-mciwndusetime)
</dt> </dl>

 

 





