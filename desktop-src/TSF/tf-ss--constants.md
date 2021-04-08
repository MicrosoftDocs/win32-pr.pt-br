---
title: Constantes de TF_SS_ (msctf. h)
description: O TF \_ SS \_ \ Constants, definido antes do tempo de execução na estrutura de status de TF \_ , descreve os Estados de documento estático.
ms.assetid: 371aeeda-f081-4506-ba51-79c6a8bc8768
topic_type:
- apiref
api_name:
- TF_SS_DISJOINTSEL
- TF_SS_REGIONS
- TF_SS_TRANSITORY
- TF_SS_TKBAUTOCORRECTENABLE
- TF_SS_TKBPREDICTIONENABLE
api_location:
- Msctf.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1028b78e74ed10c572feb904baa8ec395087ee3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009472"
---
# <a name="tf_ss_-constants"></a>Constantes de TF \_ SS \_ \*

As \_ constantes TF SS \_ \* , definidas antes do tempo de execução na estrutura de [**\_ status de TF**](/previous-versions/windows/desktop/legacy/ms629192(v=vs.85)) , descrevem os Estados de documento estático.



| Constante/valor                                                                                                                                                                                                                                                                              | Descrição                                                                                                    |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------|
| <span id="TF_SS_DISJOINTSEL"></span><span id="tf_ss_disjointsel"></span><dl> <dt>**TF \_ SS \_ DISJOINTSEL**</dt> <dt>(TS \_ SS \_ DISJOINTSEL)</dt> </dl>                                     | O documento dá suporte a várias seleções.<br/>                                                          |
| <span id="TF_SS_REGIONS"></span><span id="tf_ss_regions"></span><dl> <dt>**TF \_ \_regiões do SS**</dt> <dt>( \_ regiões do TS SS \_ )</dt> </dl>                                                     | O documento pode conter várias regiões.<br/>                                                          |
| <span id="TF_SS_TRANSITORY"></span><span id="tf_ss_transitory"></span><dl> <dt>**TF \_ \_transitório de SS**</dt> <dt>(transitório de TS \_ SS \_ )</dt> </dl>                                         | Espera-se que o documento tenha um pequeno ciclo de uso.<br/>                                               |
| <span id="TF_SS_TKBAUTOCORRECTENABLE"></span><span id="tf_ss_tkbautocorrectenable"></span><dl> <dt>**TF \_ SS \_ TKBAUTOCORRECTENABLE**</dt> <dt>(TS \_ SS \_ TKBAUTOCORRECTENABLE)</dt> </dl> | **A partir do Windows 8:** O documento dá suporte à correção automática fornecida pelo teclado de toque.<br/>   |
| <span id="TF_SS_TKBPREDICTIONENABLE"></span><span id="tf_ss_tkbpredictionenable"></span><dl> <dt>**TF \_ SS \_ TKBPREDICTIONENABLE**</dt> <dt>(TS \_ SS \_ TKBPREDICTIONENABLE)</dt> </dl>     | **A partir do Windows 8:** O documento dá suporte a sugestões de texto fornecidas pelo teclado de toque.<br/> |



## <a name="remarks"></a>Comentários

O membro **dwStaticFlags** da estrutura de \_ status tf usa essas constantes.

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

[**STATUS de TF \_**](/previous-versions/windows/desktop/legacy/ms629192(v=vs.85))
</dt> </dl>

 

