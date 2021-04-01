---
title: Mensagem de MCIWNDM_NEW (VFW. h)
description: A \_ nova mensagem do MCIWNDM cria um novo arquivo para o dispositivo MCI atual. Você pode enviar essa mensagem explicitamente ou usando a macro MCIWndNew.
ms.assetid: 18b2340d-8303-415a-867f-bd346034db2a
keywords:
- Multimídia do Windows de mensagem MCIWNDM_NEW
topic_type:
- apiref
api_name:
- MCIWNDM_NEW
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 293323cd0404da45e648024b35b7f96ef60fea61
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644565"
---
# <a name="mciwndm_new-message"></a>MCIWNDM \_ nova mensagem

A **\_ nova** mensagem do MCIWNDM cria um novo arquivo para o dispositivo MCI atual. Você pode enviar essa mensagem explicitamente ou usando a macro [**MCIWndNew**](/windows/desktop/api/Vfw/nf-vfw-mciwndnew) .


```C++
MCIWNDM_NEW 
wParam = 0; 
lParam = (LPARAM) (LPVOID) lp; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="lp"></span><span id="LP"></span>*LP*
</dt> <dd>

Ponteiro para um buffer que contém o nome do dispositivo MCI que usará o arquivo.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará zero se for bem-sucedido ou um erro de outra forma.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MCIWndNew**](/windows/desktop/api/Vfw/nf-vfw-mciwndnew)
</dt> </dl>

 

 





