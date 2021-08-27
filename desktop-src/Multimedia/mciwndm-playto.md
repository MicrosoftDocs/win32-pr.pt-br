---
title: MCIWNDM_PLAYTO mensagem (Vfw.h)
description: A mensagem PLAYTO MCIWNDM reproduz o conteúdo de um dispositivo MCI da posição atual para o local final especificado ou até que outro comando pare \_ a reprodução.
ms.assetid: ed940ee7-7b96-47da-99d3-6697f8a2e3d5
keywords:
- MCIWNDM_PLAYTO mensagem Windows Multimídia
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
ms.openlocfilehash: 61004706c8dfacb05ad47c6ddf261ac813d58f5076dfdd4e134896b3f8c646e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037936"
---
# <a name="mciwndm_playto-message"></a>Mensagem MCIWNDM \_ PLAYTO

A **mensagem \_ PLAYTO MCIWNDM** reproduz o conteúdo de um dispositivo MCI da posição atual para o local final especificado ou até que outro comando pare a reprodução. Se o local final especificado estiver além do final do conteúdo, a reprodução será interrompida no final do conteúdo. Você pode enviar essa mensagem explicitamente ou usando a macro [**MCIWndPlayTo.**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayto)


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

Retornará zero se for bem-sucedido ou um erro, caso contrário.

## <a name="remarks"></a>Comentários

Essa macro é definida usando as macros [**MCIWndSeek**](/windows/desktop/api/Vfw/nf-vfw-mciwndseek) e [**MCIWndPlayTo,**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayto) que, por sua vez, usam o comando [MCI \_ SEEK](mci-seek.md) e a mensagem **\_ PLAYTO MCIWNDM.**

Você também pode especificar um local inicial e final para reprodução usando a macro [**MCIWndPlayFromTo.**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[MCI \_ SEEK](mci-seek.md)
</dt> <dt>

[**MCIWndPlayFromTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto)
</dt> <dt>

[**MCIWndPlayTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayto)
</dt> <dt>

[**MCIWndSeek**](/windows/desktop/api/Vfw/nf-vfw-mciwndseek)
</dt> </dl>

 

 





