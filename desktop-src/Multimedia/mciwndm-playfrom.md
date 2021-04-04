---
title: Mensagem de MCIWNDM_PLAYFROM (VFW. h)
description: A \_ mensagem MCIWNDM PLAYFROM reproduz o conteúdo de um dispositivo MCI do local especificado até o final do conteúdo ou até que outro comando pare a reprodução. Você pode enviar essa mensagem explicitamente ou usando a macro MCIWndPlayFrom.
ms.assetid: 1c47f8eb-2a1b-4671-a9f8-fd6d59a5c7c6
keywords:
- Multimídia do Windows de mensagem MCIWNDM_PLAYFROM
topic_type:
- apiref
api_name:
- MCIWNDM_PLAYFROM
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c0fa1b3f4b3359e1609b3ba12009fe5879c304a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918101"
---
# <a name="mciwndm_playfrom-message"></a>\_Mensagem MCIWNDM PLAYFROM

A mensagem **MCIWNDM \_ PLAYFROM** reproduz o conteúdo de um dispositivo MCI do local especificado até o final do conteúdo ou até que outro comando pare a reprodução. Você pode enviar essa mensagem explicitamente ou usando a macro [**MCIWndPlayFrom**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfrom) .


```C++
MCIWNDM_PLAYFROM 
wParam = 0; 
lParam = (LPARAM) (LONG) lPos; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="lPos"></span><span id="lpos"></span><span id="LPOS"></span>*lPos*
</dt> <dd>

Local inicial. As unidades para o local inicial dependem do formato de hora atual.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará zero se for bem-sucedido ou um erro de outra forma.

## <a name="remarks"></a>Comentários

Você também pode especificar um local de início e de término para reprodução usando a macro [**MCIWndPlayFromTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MCIWndPlayFrom**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfrom)
</dt> <dt>

[**MCIWndPlayFromTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto)
</dt> </dl>

 

 





