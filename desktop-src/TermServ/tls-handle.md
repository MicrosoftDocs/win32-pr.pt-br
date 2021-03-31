---
title: TLS_HANDLE
description: Representa um identificador para um servidor de licença Área de Trabalho Remota.
ms.assetid: 6da51660-a9fd-4e49-97e3-ba0829b1bbbf
ms.tgt_platform: multiple
keywords:
- TLS_HANDLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09764072b42e14aea2d1b8242dbc3cbb044442b2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644453"
---
# <a name="tls_handle"></a>identificador de TLS \_

Representa um identificador para um servidor de licença Área de Trabalho Remota. Esse identificador é retornado pela função [**TLSConnectToLsServer**](tlsconnecttolsserver.md) .

> [!Note]  
> Este tipo de dados não tem nenhum arquivo de cabeçalho associado. Para usá-lo, você deve defini-lo por conta própria, conforme mostrado neste tópico.

 


```C++
typedef HANDLE TLS_HANDLE;
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>       |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**TLSConnectToLsServer**](tlsconnecttolsserver.md)
</dt> <dt>

[**TLSDisconnectFromServer**](tlsdisconnectfromserver.md)
</dt> </dl>

 

 





