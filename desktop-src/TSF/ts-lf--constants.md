---
title: Constantes de TS_LF_ (Textstor. h)
description: As \_ constantes TS LF = \_ especificam o tipo de bloqueio de documento.
ms.assetid: f0bb6ef9-a8fc-4331-9210-6c5ba1721a73
topic_type:
- apiref
api_name:
- TS_LF_SYNC
- TS_LF_READ
- TS_LF_READWRITE
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6240511fd95e91a7f22477f631178dfab528f1e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105780129"
---
# <a name="ts_lf_-constants"></a>Constantes de TS \_ LF \_ \*

As \_ constantes TS LF \_ \* especificam o tipo de bloqueio de documento.



| Constante/valor                                                                                                                                                                                                                    | Descrição                                                                               |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------|
| <span id="TS_LF_SYNC"></span><span id="ts_lf_sync"></span><dl> <dt>**TS \_ \_Sincronização de LF**</dt> <dt>(0x1)</dt> </dl>                | O documento terá um bloqueio síncrono se esse sinalizador for combinado com outros sinalizadores.<br/> |
| <span id="TS_LF_READ"></span><span id="ts_lf_read"></span><dl> <dt>**TS \_ LF de \_ leitura**</dt> <dt>(0x2)</dt> </dl>                | O documento tem um bloqueio somente leitura e não pode ser modificado.<br/>                      |
| <span id="TS_LF_READWRITE"></span><span id="ts_lf_readwrite"></span><dl> <dt>**TS \_ LF \_ ReadWrite**</dt> <dt>(0x6)</dt> </dl> | O documento tem um bloqueio de leitura/gravação e pode ser modificado.<br/>                        |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                              |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                    |
| Redistribuível<br/>          | TSF 1,0 no Windows 2000 Professional<br/>                                         |
| parâmetro<br/>                   | <dl> <dt>Textstor. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>Textstor. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Bloqueios de documentos](document-locks.md)
</dt> <dt>

[ITextStoreACP:: RequestLock](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestlock)
</dt> <dt>

[ITextStoreACPSink:: OnLockGranted](/windows/desktop/api/Textstor/nf-textstor-itextstoreacpsink-onlockgranted)
</dt> <dt>

[ITextStoreAnchor:: RequestLock](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestlock)
</dt> <dt>

[ITextStoreAnchorSink:: OnLockGranted](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchorsink-onlockgranted)
</dt> </dl>

 

 





