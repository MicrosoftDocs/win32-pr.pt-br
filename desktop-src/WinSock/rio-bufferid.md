---
description: Especifica um descritor de buffer registrado usado com as extensões de e/s registradas do Winsock.
ms.assetid: 87D0A3F6-A44C-4D7F-B276-7FD5DC2DE7A3
title: RIO_BUFFERID (Mswsockdef. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6bde67e14a1cb591922ddc180ab8f308b8429c2b36c5998d313876200cd3a26c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097546"
---
# <a name="rio_bufferid"></a>RIO \_ bufferid

O **typedef \_ bufferid de Rio** especifica um descritor de buffer registrado usado com as extensões de e/s registradas do Winsock.


```C++
typedef struct RIO_BUFFERID_t* RIO_BUFFERID, **PRIO_BUFFERID;
```



<dl> <dt>

**RIO \_ bufferid**
</dt> <dd>

Um tipo de dados que especifica um descritor de buffer registrado usado com solicitações de envio e recebimento.

</dd> </dl>

## <a name="remarks"></a>Comentários

As extensões de e/s registradas no Winsock operam principalmente em buffers registrados usando objetos do **rio \_ bufferid** . Um aplicativo obtém um **rio \_ bufferid** para um buffer existente usando a função [**RIORegisterBuffer**](/previous-versions/windows/desktop/legacy/hh437199(v=vs.85)) . Um aplicativo pode liberar um registro usando a função [**RIODeregisterBuffer**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioderegisterbuffer) .

Quando um buffer existente é registrado como um objeto **Rio de \_ bufferid** usando a função [**RIORegisterBuffer**](/previous-versions/windows/desktop/legacy/hh437199(v=vs.85)) , determinados recursos internos são alocados da memória física e o buffer de aplicativo existente será bloqueado na memória física. A função [**RIODeregisterBuffer**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioderegisterbuffer) é chamada para cancelar o registro do buffer, liberar esses recursos internos e permitir que o buffer seja desbloqueado e liberado da memória física.

O registro repetido e o cancelamento de registro de buffers de aplicativo usando as extensões de e/s registradas pelo Winsock podem causar uma degradação significativa no desempenho. As abordagens de gerenciamento de buffer a seguir devem ser consideradas ao criar um aplicativo usando as extensões de e/s registradas pelo Winsock para minimizar o registro repetido e o cancelamento de registro de buffers de aplicativo:

-   • Maximize a reutilização de buffers.
-   • Manter um pool limitado de buffers registrados não utilizados para uso pelo aplicativo.
-   • Manter um pool limitado de buffers registrados e executar cópias de buffer entre esses buffers registrados e outros buffers não registrados.

O **typedef \_ bufferid do Rio** é definido no arquivo de cabeçalho *Mswsockdef. h* , que é incluído automaticamente no arquivo de cabeçalho *mswsock. h* . O arquivo de cabeçalho *Mswsockdef. h* nunca deve ser usado diretamente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8 \[ somente aplicativos da área de trabalho\]<br/>                                                                  |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[ somente aplicativos da área de trabalho\]<br/>                                                        |
| Cabeçalho<br/>                   | <dl> <dt>Mswsockdef. h (incluir mswsock. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**RIO de \_ buf**](/windows/desktop/api/Mswsockdef/ns-mswsockdef-rio_buf)
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

 

 
