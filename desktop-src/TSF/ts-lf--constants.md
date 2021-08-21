---
title: TS_LF_ constantes (Textstor.h)
description: As constantes TS \_ LF \_ \ especificam o tipo de bloqueio de documento.
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
ms.openlocfilehash: c6944c8ee1d4ce7fd382c0c63be1af459ec79ed7bbc0832dd8ed2ce1351cc3b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118873626"
---
# <a name="ts_lf_-constants"></a>Constantes \_ TS LF \_ \*

As constantes TS \_ LF \_ \* especificam o tipo de bloqueio de documento.



| Constante/valor                                                                                                                                                                                                                    | Descrição                                                                               |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------|
| <span id="TS_LF_SYNC"></span><span id="ts_lf_sync"></span><dl> <dt>**TS \_ LF \_ SYNC**</dt> <dt>( 0x1 )</dt> </dl>                | O documento terá um bloqueio síncrono se esse sinalizador for combinado com outros sinalizadores.<br/> |
| <span id="TS_LF_READ"></span><span id="ts_lf_read"></span><dl> <dt>**TS \_ LF \_ READ**</dt> <dt>( 0x2 )</dt> </dl>                | O documento tem um bloqueio somente leitura e não pode ser modificado.<br/>                      |
| <span id="TS_LF_READWRITE"></span><span id="ts_lf_readwrite"></span><dl> <dt>**TS \_ LF \_ READWRITE**</dt> <dt>( 0x6 )</dt> </dl> | O documento tem um bloqueio de leitura/gravação e pode ser modificado.<br/>                        |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                              |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                    |
| Redistribuível<br/>          | TSF 1.0 no Windows 2000 Professional<br/>                                         |
| Cabeçalho<br/>                   | <dl> <dt>Textstor.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Textstor.idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Bloqueios de documento](document-locks.md)
</dt> <dt>

[ITextStoreACP::RequestLock](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestlock)
</dt> <dt>

[ITextStoreACPSink::OnLockGranted](/windows/desktop/api/Textstor/nf-textstor-itextstoreacpsink-onlockgranted)
</dt> <dt>

[ITextStoreAnchor::RequestLock](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestlock)
</dt> <dt>

[ITextStoreAnchorSink::OnLockGranted](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchorsink-onlockgranted)
</dt> </dl>

 

 





