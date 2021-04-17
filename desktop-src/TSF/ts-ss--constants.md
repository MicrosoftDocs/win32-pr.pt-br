---
title: Constantes de TS_SS_ (Textstor. h)
description: As \_ constantes TS SS \_ , definidas antes do tempo de execução na \_ estrutura de status TS, descrevem os Estados de documento estático.
ms.assetid: 17264527-946a-4648-a4eb-30db751602ab
topic_type:
- apiref
api_name:
- TS_SS_DISJOINTSEL
- TS_SS_REGIONS
- TS_SS_TRANSITORY
- TS_SS_NOHIDDENTEXT
- TS_SS_TKBAUTOCORRECTENABLE
- TS_SS_TKBPREDICTIONENABLE
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 773645b8a75b7e8eeafa40ed9fa95067743628d7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105760172"
---
# <a name="ts_ss_-constants"></a>Constantes do TS \_ SS \_ \*

As constantes do TS \_ SS \_ \* , definidas antes do tempo de execução na estrutura de [**\_ status do TS**](/windows/desktop/api/Textstor/ns-textstor-ts_status) , descrevem os Estados de documento estático.



| Constante/valor                                                                                                                                                                                                                                                      | Descrição                                                                                                    |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------|
| <span id="TS_SS_DISJOINTSEL"></span><span id="ts_ss_disjointsel"></span><dl> <dt>**TS \_ SS \_ DISJOINTSEL**</dt> <dt>(0x1)</dt> </dl>                             | O documento dá suporte a várias seleções.<br/>                                                          |
| <span id="TS_SS_REGIONS"></span><span id="ts_ss_regions"></span><dl> <dt>**TS \_ \_Regiões SS**</dt> <dt>(0x2)</dt> </dl>                                         | O documento pode conter várias regiões.<br/>                                                          |
| <span id="TS_SS_TRANSITORY"></span><span id="ts_ss_transitory"></span><dl> <dt>**TS \_ \_Transitória de SS**</dt> <dt>(0x4)</dt> </dl>                                | Espera-se que o documento tenha um pequeno ciclo de uso.<br/>                                               |
| <span id="TS_SS_NOHIDDENTEXT"></span><span id="ts_ss_nohiddentext"></span><dl> <dt>**TS \_ SS \_ NOHIDDENTEXT**</dt> <dt>(0x8)</dt> </dl>                          | O documento nunca conterá texto oculto.<br/>                                                        |
| <span id="TS_SS_TKBAUTOCORRECTENABLE"></span><span id="ts_ss_tkbautocorrectenable"></span><dl> <dt>**TS \_ SS \_ TKBAUTOCORRECTENABLE**</dt> <dt>(0x10)</dt> </dl> | **A partir do Windows 8:** O documento dá suporte à correção automática fornecida pelo teclado de toque.<br/>   |
| <span id="TS_SS_TKBPREDICTIONENABLE"></span><span id="ts_ss_tkbpredictionenable"></span><dl> <dt>**TS \_ SS \_ TKBPREDICTIONENABLE**</dt> <dt>(0x20)</dt> </dl>    | **A partir do Windows 8:** O documento dá suporte a sugestões de texto fornecidas pelo teclado de toque.<br/> |



## <a name="remarks"></a>Comentários

O membro **dwStaticFlags** da estrutura **de \_ status TS** usa essas constantes.

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

[**STATUS de TS \_**](/windows/desktop/api/Textstor/ns-textstor-ts_status)
</dt> <dt>

[**STATUS de TF \_**](/previous-versions/windows/desktop/legacy/ms629192(v=vs.85))
</dt> </dl>

 

