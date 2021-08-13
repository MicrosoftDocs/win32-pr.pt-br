---
title: MCIWNDM_GETMODE mensagem (Vfw.h)
description: A mensagem GETMODE MCIWNDM \_ recupera o modo de operação atual de um dispositivo MCI. Os dispositivos MCI têm vários modos de operação, que são designados por constantes. Você pode enviar essa mensagem explicitamente ou usando a macro MCIWndGetMode.
ms.assetid: cc327281-434e-4047-9e15-c04a10953f47
keywords:
- MCIWNDM_GETMODE mensagem Windows Multimídia
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
ms.openlocfilehash: 645d7a660df8d22cb2adb70a775d5431eb31dc986b502bb4dbb36b1963ce06f8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119429266"
---
# <a name="mciwndm_getmode-message"></a>Mensagem GETMODE MCIWNDM \_

A **mensagem \_ GETMODE MCIWNDM** recupera o modo de operação atual de um dispositivo MCI. Os dispositivos MCI têm vários modos de operação, que são designados por constantes. Você pode enviar essa mensagem explicitamente ou usando a [**macro MCIWndGetMode.**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetmode)


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

<span id="lp"></span><span id="LP"></span>*Lp*
</dt> <dd>

Ponteiro para o buffer definido pelo aplicativo usado para retornar o modo.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retorna um inteiro correspondente à constante MCI que define o modo.

## <a name="remarks"></a>Comentários

Se a cadeia de caracteres terminada em nulo que descreve o modo for maior que o buffer, ela será truncada.

Nem todos os dispositivos podem operar em todos os modos. Por exemplo, o dispositivo MCIAVI é um dispositivo de reprodução; ele não dá suporte ao modo de gravação. Os modos a seguir podem ser recuperados usando **MCIWNDM \_ GETMODE.**



| Modo de operação | Constante MCI          |
|----------------|-----------------------|
| não pronto      | MODO MCI \_ \_ NÃO \_ PRONTO |
| Abrir           | MODO MCI \_ \_ ABERTO       |
| pausado         | PAUSA DO MODO MCI \_ \_      |
| reproduzindo        | REPRODUÇÃO DO MODO MCI \_ \_       |
| gravação      | REGISTRO DE MODO MCI \_ \_     |
| buscando        | MCI \_ MODE \_ SEEK       |
| stopped        | PARADA NO MODO MCI \_ \_       |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MCIWndGetMode**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetmode)
</dt> </dl>

 

 





