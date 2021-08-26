---
description: Especifica um descritor de buffer registrado usado com as extensões de E/S registradas do Winsock.
ms.assetid: 87D0A3F6-A44C-4D7F-B276-7FD5DC2DE7A3
title: RIO_BUFFERID (Mswsockdef.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6bde67e14a1cb591922ddc180ab8f308b8429c2b36c5998d313876200cd3a26c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097546"
---
# <a name="rio_bufferid"></a>RIO \_ BUFFERID

O **typedef RIO \_ BUFFERID** especifica um descritor de buffer registrado usado com as extensões de E/S registradas do Winsock.


```C++
typedef struct RIO_BUFFERID_t* RIO_BUFFERID, **PRIO_BUFFERID;
```



<dl> <dt>

**RIO \_ BUFFERID**
</dt> <dd>

Um tipo de dados que especifica um descritor de buffer registrado usado com solicitações de envio e recebimento.

</dd> </dl>

## <a name="remarks"></a>Comentários

As extensões de E/S registradas do Winsock operam principalmente em buffers registrados usando **objetos RIO \_ BUFFERID.** Um aplicativo obtém um **\_ BUFFERID DE RIO** para um buffer existente usando a função [**RIORegisterBuffer.**](/previous-versions/windows/desktop/legacy/hh437199(v=vs.85)) Um aplicativo pode liberar um registro usando a [**função RIODeregisterBuffer.**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioderegisterbuffer)

Quando um buffer existente é registrado como um objeto **RIO \_ BUFFERID** usando a função [**RIORegisterBuffer,**](/previous-versions/windows/desktop/legacy/hh437199(v=vs.85)) determinados recursos internos são alocados da memória física e o buffer de aplicativo existente será bloqueado na memória física. A [**função RIODeregisterBuffer**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioderegisterbuffer) é chamada para desregisar o buffer, liberar esses recursos internos e permitir que o buffer seja desbloqueado e liberado da memória física.

O registro e o desregistramento repetidos de buffers de aplicativo usando as extensões de E/S registradas do Winsock podem causar degradação significativa do desempenho. As abordagens de gerenciamento de buffer a seguir devem ser consideradas ao criar um aplicativo usando as extensões de E/S registradas do Winsock para minimizar o registro repetido e o desregistramento de buffers de aplicativo:

-   • Maximizar a reutilização de buffers.
-   • Manter um pool limitado de buffers registrados não usado para uso pelo aplicativo.
-   • Manter um pool limitado de buffers registrados e executar cópias de buffer entre esses buffers registrados e outros buffers não registrados.

O **typedef RIO \_ BUFFERID** é definido no arquivo de header *Mswsockdef.h,* que é incluído automaticamente no arquivo de header *Mswsock.h.* O *arquivo de header Mswsockdef.h* nunca deve ser usado diretamente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8 somente aplicativos da área de trabalho\]<br/>                                                                  |
| Servidor mínimo com suporte<br/> | \[Windows Server 2012 somente aplicativos da área de trabalho\]<br/>                                                        |
| Cabeçalho<br/>                   | <dl> <dt>Mswsockdef.h (inclua Mswsock.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**RIO \_ BUF**](/windows/desktop/api/Mswsockdef/ns-mswsockdef-rio_buf)
</dt> <dt>

[**RIODeregisterBuffer**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioderegisterbuffer)
</dt> <dt>

[**RIOReceive**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioreceive)
</dt> <dt>

[**RIOReceiveEx**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioreceiveex)
</dt> <dt>

[**RIORegisterBuffer**](/previous-versions/windows/desktop/legacy/hh437199(v=vs.85))
</dt> <dt>

[**RIOSend**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riosend)
</dt> <dt>

[**RIOSendEx**](/previous-versions/windows/desktop/legacy/hh437216(v=vs.85))
</dt> </dl>

 

 
