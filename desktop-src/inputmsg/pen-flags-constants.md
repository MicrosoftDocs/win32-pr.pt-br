---
title: Sinalizadores de caneta
description: Os valores que podem aparecer no campo penFlags da estrutura de POINTER_PEN_INFO.
ms.assetid: BC3CE568-4090-4451-B780-18530C988305
topic_type:
- apiref
api_name:
- PEN_FLAG_NONE
- PEN_FLAG_BARREL
- PEN_FLAG_INVERTED
- PEN_FLAG_ERASER
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: acc1afb1d490a1831fdb1ecd5a090e457bae77ae2f08a1b94cabc81d12dbde9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118482401"
---
# <a name="pen-flags"></a>Sinalizadores de caneta

Os valores que podem aparecer no campo **penFlags** da estrutura de [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api) .

<dl> <dt>

<span id="PEN_FLAG_NONE"></span><span id="pen_flag_none"></span>**PEN_FLAG_NONE**
</dt> <dd> <dl> <dt>

0x00000000
</dt> <dt>



Não há nenhum sinalizador de caneta. Esse é o padrão.


</dt> </dl> </dd> <dt>

<span id="PEN_FLAG_BARREL"></span><span id="pen_flag_barrel"></span>**PEN_FLAG_BARREL**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



O botão de cilindro é pressionado.


</dt> </dl> </dd> <dt>

<span id="PEN_FLAG_INVERTED"></span><span id="pen_flag_inverted"></span>**PEN_FLAG_INVERTED**
</dt> <dd> <dl> <dt>

0x00000002
</dt> <dt>



A caneta está invertida.


</dt> </dl> </dd> <dt>

<span id="PEN_FLAG_ERASER"></span><span id="pen_flag_eraser"></span>**PEN_FLAG_ERASER**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



O botão de borracha é pressionado.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8 \[ somente aplicativos da área de trabalho\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[ somente aplicativos da área de trabalho\]<br/>                                 |
| parâmetro<br/>                   | <dl> <dt>WinUser. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Constantes](constants.md)
</dt> <dt>

[**POINTER_INFO**](/previous-versions/windows/desktop/api)
</dt> </dl>

 

 





