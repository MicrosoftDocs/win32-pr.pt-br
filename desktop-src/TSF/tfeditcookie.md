---
title: TfEditCookie (msctf. h)
description: O tipo de dados TfEditCookie identifica uma sessão de edição que tem um bloqueio.
ms.assetid: 1de17286-5d56-4302-a144-5fe6ca7d5557
keywords:
- TfEditCookie
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69281bc38b5df6c22dd5306877aecdb8025af84a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008820"
---
# <a name="tfeditcookie"></a>TfEditCookie

O tipo de dados **TfEditCookie** identifica uma sessão de edição que tem um bloqueio.


```C++
typedef DWORD TfEditCookie;
```



## <a name="remarks"></a>Comentários

O tipo de dados **TfEditCookie** é fornecido pelo Gerenciador do TSF e é usado por um cliente (serviço de aplicativo ou de texto) para identificar uma sessão de edição com um bloqueio somente leitura ou de leitura/gravação em vários métodos.

Um valor de **TfEditCookie** é obtido de uma das maneiras a seguir.

-   O cliente chama [ITfDocumentMgr:: CreateContext](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-createcontext).
-   O Gerenciador do TSF chama o método ITfEditSession do cliente [::D oeditsession](/windows/desktop/api/Msctf/nf-msctf-itfeditsession-doeditsession) .
-   O Gerenciador do TSF chama o método [ITfCompositionSink:: OnCompositionTerminated](/windows/desktop/api/Msctf/nf-msctf-itfcompositionsink-oncompositionterminated) do cliente.
-   O Gerenciador do TSF chama o método [ITfCleanupContextSink:: OnCleanupContext](/windows/desktop/api/Msctf/nf-msctf-itfcleanupcontextsink-oncleanupcontext) do cliente.
-   O Gerenciador do TSF chama o método [ITfTextEditSink:: onendedit](/windows/desktop/api/Msctf/nf-msctf-itftexteditsink-onendedit) do cliente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Aplicativos do Windows 2000 Professional \[ Desktop aplicativos \| UWP\]<br/>                    |
| Servidor mínimo com suporte<br/> | Aplicativos da área de trabalho do Windows 2000 Server aplicativos \[ \| UWP\]<br/>                          |
| Redistribuível<br/>          | TSF 1,0 no Windows 2000 Professional<br/>                                      |
| parâmetro<br/>                   | <dl> <dt>Msctf. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>Msctf. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ITfCleanupContextSink::OnCleanupContext**](/windows/desktop/api/Msctf/nf-msctf-itfcleanupcontextsink-oncleanupcontext)
</dt> <dt>

[**ITfCompositionSink::OnCompositionTerminated**](/windows/desktop/api/Msctf/nf-msctf-itfcompositionsink-oncompositionterminated)
</dt> <dt>

[**ITfDocumentMgr:: CreateContext**](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-createcontext)
</dt> <dt>

[**ITfEditSession::D oEditSession**](/windows/desktop/api/Msctf/nf-msctf-itfeditsession-doeditsession)
</dt> <dt>

[**ITfTextEditSink:: onendedit**](/windows/desktop/api/Msctf/nf-msctf-itftexteditsink-onendedit)
</dt> </dl>

 

 





