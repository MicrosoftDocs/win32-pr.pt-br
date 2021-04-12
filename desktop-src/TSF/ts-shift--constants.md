---
title: Constantes de TS_SHIFT_ (Textstor. h)
description: As \_ constantes TS SHIFT \_ são usadas pela interface IAnchor para manipulação de texto oculto e contagem de caracteres.
ms.assetid: 93329238-f6e8-432e-9167-550a02b33b46
topic_type:
- apiref
api_name:
- TS_SHIFT_COUNT_HIDDEN
- TS_SHIFT_HALT_HIDDEN
- TS_SHIFT_HALT_VISIBLE
- TS_SHIFT_COUNT_ONLY
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98f3a11463aea1633079d771bf6a8b333475865e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369634"
---
# <a name="ts_shift_-constants"></a>Constantes do TS \_ SHIFT \_ \*

As \_ constantes TS SHIFT \_ \* são usadas pela interface **IAnchor** para manipulação de texto oculto e contagem de caracteres.



| Constante/valor                                                                                                                                                                                                                                       | Descrição                                                                                                                                                                                                                                     |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TS_SHIFT_COUNT_HIDDEN"></span><span id="ts_shift_count_hidden"></span><dl> <dt>**TS \_ Contagem de DESLOCAMENTOs \_ \_ oculta**</dt> <dt>(0x1)</dt> </dl> | Especifica que a âncora será deslocada para o próximo limite de região, incluindo o limite de uma região de texto oculta. Se não estiver definido, a âncora será deslocada após qualquer texto oculto adjacente até que uma região de texto visível seja encontrada.<br/> |
| <span id="TS_SHIFT_HALT_HIDDEN"></span><span id="ts_shift_halt_hidden"></span><dl> <dt>**TS \_ ALTERNAR \_ parada \_ oculta**</dt> <dt>(0x2)</dt> </dl>    | Não usado.<br/>                                                                                                                                                                                                                            |
| <span id="TS_SHIFT_HALT_VISIBLE"></span><span id="ts_shift_halt_visible"></span><dl> <dt>**TS \_ Parada de deslocamento \_ \_ visível**</dt> <dt>(0x4)</dt> </dl> | Não usado.<br/>                                                                                                                                                                                                                            |
| <span id="TS_SHIFT_COUNT_ONLY"></span><span id="ts_shift_count_only"></span><dl> <dt>**TS \_ 0x8 \_ ( \_ somente contagem de deslocamento**</dt> <dt>)</dt> </dl>       | A âncora não é deslocada.<br/>                                                                                                                                                                                                           |



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

[IAnchor::ShiftRegion](/windows/desktop/api/Textstor/nf-textstor-ianchor-shiftregion)
</dt> </dl>

 

 





