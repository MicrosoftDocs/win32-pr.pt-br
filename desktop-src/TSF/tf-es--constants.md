---
title: Constantes de TF_ES_ (msctf. h)
description: A seguir estão as constantes usadas pelo método ITfContext RequestEditSession.
ms.assetid: 5498329f-3302-4f66-bdec-cab7db0cdc0e
topic_type:
- apiref
api_name:
- TF_ES_ASYNCDONTCARE
- TF_ES_SYNC
- TF_ES_READ
- TF_ES_READWRITE
- TF_ES_ASYNC
api_location:
- Msctf.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa8ed96adc1d6f6d66671e91f7a70bce856663e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105760349"
---
# <a name="tf_es_-constants"></a>Constantes de TF \_ es \_ \*

Veja a seguir as constantes usadas pelo método [ITfContext:: RequestEditSession](/windows/desktop/api/Msctf/nf-msctf-itfcontext-requesteditsession) .



| Constante/valor                                                                                                                                                                                                                              | Descrição                                                                                                                                                                                                                                                                                                                                             |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_ES_ASYNCDONTCARE"></span><span id="tf_es_asyncdontcare"></span><dl> <dt>**TF \_ ES \_ ASYNCDONTCARE**</dt> <dt>(0)</dt> </dl> | A sessão de edição pode ocorrer de forma síncrona ou assíncrona, a critério do gerente. O gerente tentará agendar uma sessão de edição síncrona para melhorar o desempenho. Esse valor não pode ser combinado com os \_ valores de sincronização de TF es \_ Async ou TF \_ es \_ .<br/>                                                                         |
| <span id="TF_ES_SYNC"></span><span id="tf_es_sync"></span><dl> <dt>**TF \_ ES \_ sincronização**</dt> <dt>(0x1)</dt> </dl>                          | A sessão de edição deve ser síncrona, ou a solicitação falhará (com TF \_ E \_ síncrona). Esse sinalizador só deve ser usado em situações documentadas (como tratamento de pressionamentos de teclas), em que pode ser esperado ter sucesso. Caso contrário, a chamada provavelmente falhará. Esse valor não pode ser combinado com os \_ \_ valores assíncronos de TF es ASYNCDONTCARE ou TF \_ es \_ .<br/> |
| <span id="TF_ES_READ"></span><span id="tf_es_read"></span><dl> <dt>**TF \_ ES \_ leitura**</dt> <dt>(0x2)</dt> </dl>                          | Solicita acesso somente leitura ao contexto.<br/>                                                                                                                                                                                                                                                                                                    |
| <span id="TF_ES_READWRITE"></span><span id="tf_es_readwrite"></span><dl> <dt>**TF \_ ES \_ ReadWrite**</dt> <dt>(0x6)</dt> </dl>           | Solicita acesso de leitura/gravação ao contexto.<br/>                                                                                                                                                                                                                                                                                                   |
| <span id="TF_ES_ASYNC"></span><span id="tf_es_async"></span><dl> <dt>**TF \_ S \_ Async**</dt> <dt>(0x8)</dt> </dl>                       | A sessão de edição deve ser assíncrona ou a solicitação falhará. Esse valor não pode ser combinado com os \_ valores de sincronização TF es \_ ASYNCDONTCARE ou TF \_ es \_ .<br/>                                                                                                                                                                                         |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                 |
| Redistribuível<br/>          | TSF 1,0 no Windows 2000 Professional<br/>                                      |
| parâmetro<br/>                   | <dl> <dt>Msctf. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>Msctf. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ITfContext:: RequestEditSession](/windows/desktop/api/Msctf/nf-msctf-itfcontext-requesteditsession)
</dt> </dl>

 

 





