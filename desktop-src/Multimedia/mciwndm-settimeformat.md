---
title: Mensagem de MCIWNDM_SETTIMEFORMAT (VFW. h)
description: A \_ mensagem MCIWNDM SETTIMEFORMAT define o formato de hora de um dispositivo MCI. Você pode enviar essa mensagem explicitamente ou usando a macro MCIWndSetTimeFormat.
ms.assetid: 7de82094-6d35-44fd-88e7-ebd18a558cfd
keywords:
- Multimídia do Windows de mensagem MCIWNDM_SETTIMEFORMAT
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
ms.openlocfilehash: bcec1f0db5accad93211bf1eb6f1c9297e2b9f33
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499253"
---
# <a name="mciwndm_settimeformat-message"></a>\_Mensagem MCIWNDM SETTIMEFORMAT

A mensagem **MCIWNDM \_ SETTIMEFORMAT** define o formato de hora de um dispositivo MCI. Você pode enviar essa mensagem explicitamente ou usando a macro [**MCIWndSetTimeFormat**](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimeformat) .


```C++
MCIWNDM_SETTIMEFORMAT 
wParam = 0; 
lParam = (LPARAM) (LPSTR) lp; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="lp"></span><span id="LP"></span>*LP*
</dt> <dd>

Ponteiro para um buffer que contém a cadeia de caracteres terminada em nulo que indica o formato de hora. Especifique "frames" para definir o formato de hora como quadros ou "MS" para definir o formato de hora como milissegundos.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará zero se for bem-sucedido ou um erro de outra forma.

## <a name="remarks"></a>Comentários

Um aplicativo pode especificar formatos de hora diferentes de quadros ou milissegundos, desde que os formatos tenham suporte do dispositivo MCI. Formatos não contínuos, como trilhas e SMPTE, podem fazer com que o TrackBar se comporte incorretamente. Para esses formatos de tempo, talvez você queira desativar a barra de ferramentas usando a macro [**MCIWndChangeStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndchangestyles) e especificando o \_ estilo de janela MCIWNDF NOPLAYBAR.

Se você quiser definir o formato de hora como quadros ou milissegundos, também poderá usar a macro [**MCIWndUseFrames**](/windows/desktop/api/Vfw/nf-vfw-mciwnduseframes) ou [**MCIWndUseTime**](/windows/desktop/api/Vfw/nf-vfw-mciwndusetime) . Para obter uma lista de formatos de hora, consulte a macro [**MCIWndGetTimeFormat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgettimeformat) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



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

 

 





