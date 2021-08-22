---
title: Método StartService da classe MicrosoftDNS_Server
description: O método StartService inicia o servidor DNS.
ms.assetid: f6343a34-9d1b-4f82-897e-289650af6be9
keywords:
- Método StartService DNS
- Método StartService DNS, classe MicrosoftDNS_Server
- MicrosoftDNS_Server de classe de DNS, método StartService
topic_type:
- apiref
api_name:
- MicrosoftDNS_Server.StartService
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5e74de96ad24ff16ea2c2effaef78003011f5d6bd5d421336084ac5c7701f79
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119432636"
---
# <a name="startservice-method-of-the-microsoftdns_server-class"></a>Método StartService da classe de \_ servidor MicrosoftDNS

O método **StartService** inicia o servidor DNS.

## <a name="syntax"></a>Sintaxe


```mof
uint32 StartService();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

\_O êxito do erro indica que o serviço foi iniciado com êxito. Qualquer outro valor é um código de erro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                              |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                   |
| Namespace<br/>                | \\MicrosoftDNS raiz<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov. mof</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_Servidor MicrosoftDNS**](microsoftdns-server.md)
</dt> <dt>

[**Método StopService da classe de \_ servidor MicrosoftDNS**](microsoftdns-server-stopservice.md)
</dt> <dt>

[**Método StartScavenging da classe de \_ servidor MicrosoftDNS**](microsoftdns-server-startscavenging.md)
</dt> <dt>

[**Método getdistinguiname da classe de \_ servidor MicrosoftDNS**](microsoftdns-server-getdistinguishedname.md)
</dt> </dl>

 

 





