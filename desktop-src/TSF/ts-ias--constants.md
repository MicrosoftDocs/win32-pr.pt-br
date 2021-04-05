---
title: Constantes de TS_IAS_ (Textstor. h)
description: As constantes do TS \_ ias \_ \ são usadas como sinalizadores de campo de bits para controlar a inserção de texto ou de objetos inseridos em uma seleção ou ponto de inserção.
ms.assetid: 58e0d13c-d90c-41d2-bd93-4eba5fe0a69a
topic_type:
- apiref
api_name:
- TS_IAS_NOQUERY
- TS_IAS_QUERYONLY
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d59584295567c586ebd8db7e5f63366fd8272f0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085601"
---
# <a name="ts_ias_-constants"></a>Constantes do TS \_ ias \_ \*

As \_ constantes TS ias \_ \* são usadas como sinalizadores de campo de bits para controlar a inserção de texto ou de objetos inseridos em uma seleção ou ponto de inserção.



| Constante/valor                                                                                                                                                                                                                       | Descrição                                                                                                                                   |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TS_IAS_NOQUERY"></span><span id="ts_ias_noquery"></span><dl> <dt>**TS \_ \_NoConsulta do IAS**</dt> <dt>(0x1)</dt> </dl>       | O texto é inserido e o ponteiro de intervalo é definido como **nulo** na saída. Não pode ser combinado com o \_ sinalizador TS QUERYONLY do IAS \_ .<br/>          |
| <span id="TS_IAS_QUERYONLY"></span><span id="ts_ias_queryonly"></span><dl> <dt>**TS \_ \_QUERYONLY**</dt> <dt>(0X2) do</dt> ias </dl> | Não execute a inserção. O chamador requer apenas o ponteiro de intervalo a ser definido. Não pode ser combinado com o \_ \_ sinalizador noquery ias TS.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                              |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                    |
| Redistribuível<br/>          | TSF 1,0 no Windows 2000 Professional<br/>                                         |
| parâmetro<br/>                   | <dl> <dt>Textstor. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>Textstor. idl</dt> </dl> |



 

 





