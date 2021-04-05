---
title: Mensagem de MCIWNDM_PLAYTO (VFW. h)
description: A \_ mensagem MCIWNDM playto reproduz o conteúdo de um dispositivo MCI da posição atual para o local final especificado ou até que outro comando pare a reprodução.
ms.assetid: ed940ee7-7b96-47da-99d3-6697f8a2e3d5
keywords:
- Multimídia do Windows de mensagem MCIWNDM_PLAYTO
topic_type:
- apiref
api_name:
- MCIWNDM_PLAYTO
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cf0104204dc0306615ead91be036459cdf3c11d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086139"
---
# <a name="mciwndm_playto-message"></a>\_Mensagem de playto do MCIWNDM

A mensagem **MCIWNDM \_ playto** reproduz o conteúdo de um dispositivo MCI da posição atual para o local final especificado ou até que outro comando pare a reprodução. Se o local final especificado estiver além do fim do conteúdo, a reprodução será interrompida no final do conteúdo. Você pode enviar essa mensagem explicitamente ou usando a macro [**MCIWndPlayTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayto) .


```C++
MCIWNDM_PLAYTO 
wParam = 0; 
lParam = (LPARAM) (LONG) lEnd; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="lEnd"></span><span id="lend"></span><span id="LEND"></span>*Emprestar*
</dt> <dd>

Local final. As unidades para o local final dependem do formato de hora atual.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará zero se for bem-sucedido ou um erro de outra forma.

## <a name="remarks"></a>Comentários

Essa macro é definida usando as macros [**MCIWndSeek**](/windows/desktop/api/Vfw/nf-vfw-mciwndseek) e [**MCIWndPlayTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayto) , que, por sua vez, usam o comando [MCI \_ Seek](mci-seek.md) e a mensagem **MCIWNDM \_ playto** .

Você também pode especificar um local de início e de término para reprodução usando a macro [**MCIWndPlayFromTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[busca de MCI \_](mci-seek.md)
</dt> <dt>

[**MCIWndPlayFromTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto)
</dt> <dt>

[**MCIWndPlayTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayto)
</dt> <dt>

[**MCIWndSeek**](/windows/desktop/api/Vfw/nf-vfw-mciwndseek)
</dt> </dl>

 

 





