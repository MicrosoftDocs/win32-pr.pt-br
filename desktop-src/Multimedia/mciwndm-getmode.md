---
title: Mensagem de MCIWNDM_GETMODE (VFW. h)
description: A \_ mensagem MCIWNDM GetMode recupera o modo de operação atual de um dispositivo MCI. Os dispositivos MCI têm vários modos de operação, que são designados por constantes. Você pode enviar essa mensagem explicitamente ou usando a macro MCIWndGetMode.
ms.assetid: cc327281-434e-4047-9e15-c04a10953f47
keywords:
- Multimídia do Windows de mensagem MCIWNDM_GETMODE
topic_type:
- apiref
api_name:
- MCIWNDM_GETMODE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5daefea2c550a1d0cf807ae03840c38ae8b2567c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085144"
---
# <a name="mciwndm_getmode-message"></a>\_Mensagem MCIWNDM GETmode

A mensagem **MCIWNDM \_ GetMode** recupera o modo de operação atual de um dispositivo MCI. Os dispositivos MCI têm vários modos de operação, que são designados por constantes. Você pode enviar essa mensagem explicitamente ou usando a macro [**MCIWndGetMode**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetmode) .


```C++
MCIWNDM_GETMODE 
wParam = (WPARAM) (UINT) len; 
lParam = (LPARAM) (LPSTR) lp; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="len"></span><span id="LEN"></span>*Len*
</dt> <dd>

Tamanho, em bytes, do buffer.

</dd> <dt>

<span id="lp"></span><span id="LP"></span>*LP*
</dt> <dd>

Ponteiro para o buffer definido pelo aplicativo usado para retornar o modo.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retorna um inteiro correspondente à constante MCI que define o modo.

## <a name="remarks"></a>Comentários

Se a cadeia de caracteres terminada em nulo que descreve o modo for maior que o buffer, ela será truncada.

Nem todos os dispositivos podem operar em todos os modos. Por exemplo, o dispositivo MCIAVI é um dispositivo de reprodução; Ele não dá suporte ao modo de gravação. Os modos a seguir podem ser recuperados usando **MCIWNDM \_ GetMode**.



| Modo de operação | Constante MCI          |
|----------------|-----------------------|
| Não está pronto      | \_modo MCI \_ não \_ está pronto |
| Abrir           | \_modo MCI \_ aberto       |
| pausado         | \_pausa no modo MCI \_      |
| reproduzindo        | \_reprodução do modo MCI \_       |
| gravação      | \_registro do modo MCI \_     |
| buscando        | \_modo MCI \_ Seek       |
| interrompido        | \_parada do modo MCI \_       |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MCIWndGetMode**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetmode)
</dt> </dl>

 

 





