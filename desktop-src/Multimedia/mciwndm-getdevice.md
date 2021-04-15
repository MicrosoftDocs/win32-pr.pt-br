---
title: Mensagem de MCIWNDM_GETDEVICE (VFW. h)
description: A \_ mensagem GETdevice do MCIWNDM recupera o nome do dispositivo MCI aberto no momento. Você pode enviar essa mensagem explicitamente ou usando a macro MCIWndGetDevice.
ms.assetid: e69a73a6-a927-4536-98c7-ee7d5b16668a
keywords:
- Multimídia do Windows de mensagem MCIWNDM_GETDEVICE
topic_type:
- apiref
api_name:
- MCIWNDM_GETDEVICE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32664508a577db9d5a077e3cb4fd00aab34fbdf3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454752"
---
# <a name="mciwndm_getdevice-message"></a>Mensagem do MCIWNDM \_ GETdevice

A **mensagem \_ GetDevice do MCIWNDM** recupera o nome do dispositivo MCI aberto no momento. Você pode enviar essa mensagem explicitamente ou usando a macro [**MCIWndGetDevice**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdevice) .


```C++
MCIWNDM_GETDEVICE 
wParam = (WPARAM) (UINT) len; 
lParam = (LPARAM) (LPVOID) lp; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="len"></span><span id="LEN"></span>*Len*
</dt> <dd>

Tamanho, em bytes, do buffer.

</dd> <dt>

<span id="lp"></span><span id="LP"></span>*LP*
</dt> <dd>

Ponteiro para um buffer definido pelo aplicativo para retornar o nome do dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará zero se for bem-sucedido ou um valor diferente de zero, caso contrário.

## <a name="remarks"></a>Comentários

Se a cadeia de caracteres terminada em nulo que contém o nome do dispositivo for maior do que o buffer, MCIWnd o truncará.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



 

 





