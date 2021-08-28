---
title: TLS_HANDLE
description: Representa um alça para um Área de Trabalho Remota de licença.
ms.assetid: 6da51660-a9fd-4e49-97e3-ba0829b1bbbf
ms.tgt_platform: multiple
keywords:
- TLS_HANDLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04daf14429a5b400267e664a615739fd14e8306e987f50726cfdb341522870a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119869446"
---
# <a name="tls_handle"></a>TLS \_ HANDLE

Representa um alça para um Área de Trabalho Remota de licença. Esse handle é retornado pela [**função TLSConnectToLsServer.**](tlsconnecttolsserver.md)

> [!Note]  
> Esse tipo de dados não tem nenhum arquivo de header associado. Para usá-lo, você deve defini-lo por conta própria, conforme mostrado neste tópico.

 


```C++
typedef HANDLE TLS_HANDLE;
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>       |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**TLSConnectToLsServer**](tlsconnecttolsserver.md)
</dt> <dt>

[**TLSDisconnectFromServer**](tlsdisconnectfromserver.md)
</dt> </dl>

 

 





