---
title: Constantes de TF_SD_ (msctf. h)
description: As \_ constantes TF SD \_ \ descrevem o status do documento.
ms.assetid: 953d39cd-8af1-4c86-8fb8-8b8ec917c631
topic_type:
- apiref
api_name:
- TF_SD_READONLY
- TF_SD_LOADING
api_location:
- Msctf.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12ed0d68c8a8afd9299b908eb81a04a31fbd3d85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085230"
---
# <a name="tf_sd_-constants"></a>TF \_ as \_ \* constantes do SD

As \_ constantes TF SD \_ \* descrevem o status do documento.



| Constante/valor                                                                                                                                                                                                                              | Descrição                                                  |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------|
| <span id="TF_SD_READONLY"></span><span id="tf_sd_readonly"></span><dl> <dt>**TF \_ SD \_ ReadOnly**</dt> <dt>(TS \_ SD \_ ReadOnly)</dt> </dl> | O documento é somente leitura e não pode ser modificado.<br/> |
| <span id="TF_SD_LOADING"></span><span id="tf_sd_loading"></span><dl> <dt>**TF \_ \_carregamento de SD**</dt> <dt>( \_ carregamento de TS SD \_ )</dt> </dl>     | O documento está sendo carregado e pode estar incompleto.<br/>    |



## <a name="remarks"></a>Comentários

O membro **dwDynamicFlags** da estrutura [de \_ status tf](/previous-versions/windows/desktop/legacy/ms629192(v=vs.85)) usa essas constantes.

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

[STATUS de TF \_](/previous-versions/windows/desktop/legacy/ms629192(v=vs.85))
</dt> <dt>

[Constantes de TS \_ SD \_ \*](ts-sd--constants.md)
</dt> <dt>

[ITfContextOwner:: GetStatus](/windows/desktop/api/Msctf/nf-msctf-itfcontextowner-getstatus)
</dt> <dt>

[ITfContextOwnerServices:: OnStatusChange](/windows/desktop/api/Msctf/nf-msctf-itfcontextownerservices-onstatuschange)
</dt> <dt>

[ITextStoreACP:: GetStatus](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getstatus)
</dt> <dt>

[ITfStatusSunk:: OnStatusChange](/windows/desktop/api/Msctf/nf-msctf-itfstatussink-onstatuschange)
</dt> </dl>

 

