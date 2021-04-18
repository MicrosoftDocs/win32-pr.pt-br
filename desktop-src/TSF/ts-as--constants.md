---
title: Constantes de TS_AS_ (Textstor. h)
description: Os sinalizadores a seguir especificam os eventos que chamam os métodos AdviseSink.
ms.assetid: 8f406b67-f846-4712-b4be-811dbcc6ad55
topic_type:
- apiref
api_name:
- TS_AS_TEXT_CHANGE
- TS_AS_SEL_CHANGE
- TS_AS_LAYOUT_CHANGE
- TS_AS_ATTR_CHANGE
- TS_AS_STATUS_CHANGE
- TS_AS_ALL_SINKS
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c7b36bdc2c3b559693503b2a8e408a0782855f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105758124"
---
# <a name="ts_as_-constants"></a>TS \_ como \_ \* constantes

Os sinalizadores a seguir especificam os eventos que chamam os métodos **AdviseSink** .



| Constante/valor                                                                                                                                                                                                                                                                                                                                         | Descrição                                                          |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------|
| <span id="TS_AS_TEXT_CHANGE"></span><span id="ts_as_text_change"></span><dl> <dt>**TS \_ \_ \_ Alteração de texto as**</dt> <dt>(0x1)</dt> </dl>                                                                                                               | O texto é alterado no documento.<br/>                          |
| <span id="TS_AS_SEL_CHANGE"></span><span id="ts_as_sel_change"></span><dl> <dt>**TS \_ \_ \_ Alteração de SEL**</dt> <dt>(0x2)</dt> </dl>                                                                                                                  | O texto é selecionado no documento.<br/>                         |
| <span id="TS_AS_LAYOUT_CHANGE"></span><span id="ts_as_layout_change"></span><dl> <dt>**TS \_ COMO \_ \_ alteração de layout**</dt> <dt>(0x4)</dt> </dl>                                                                                                         | O layout do documento é alterado.<br/>                    |
| <span id="TS_AS_ATTR_CHANGE"></span><span id="ts_as_attr_change"></span><dl> <dt>**TS \_ COMO \_ \_ alteração de attr**</dt> <dt>(0x8)</dt> </dl>                                                                                                               | Os atributos do documento são alterados.<br/>                |
| <span id="TS_AS_STATUS_CHANGE"></span><span id="ts_as_status_change"></span><dl> <dt>**TS \_ COMO \_ \_ alteração de status**</dt> <dt>(0x10)</dt> </dl>                                                                                                        | O status do documento é alterado.<br/>                    |
| <span id="TS_AS_ALL_SINKS"></span><span id="ts_as_all_sinks"></span><dl> <dt>**TS \_ COMO \_ todos os \_ coletores**</dt> <dt>(TS \_ como \_ texto \_ alteram \| o TS \_ como SEL alterar TS como alteração de layout TS como attr, altere \_ \_ \| \_ \_ \_ \| \_ \_ \_ \| TS \_ como alteração de \_ status \_ )</dt> </dl> | Um dos quatro eventos anteriores ocorreu no documento.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                              |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                    |
| Redistribuível<br/>          | TSF 1,0 no Windows 2000 Professional<br/>                                         |
| parâmetro<br/>                   | <dl> <dt>Textstor. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>Textstor. idl</dt> </dl> |



 

 





