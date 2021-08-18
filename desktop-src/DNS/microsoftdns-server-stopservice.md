---
title: Método StopService da classe MicrosoftDNS_Server
description: O método StopService interrompe o servidor DNS.
ms.assetid: 80637d5b-e43a-4710-b3ab-eec246587788
keywords:
- DNS do método StopService
- Método StopService DNS, classe MicrosoftDNS_Server
- MicrosoftDNS_Server de classe de DNS, método StopService
topic_type:
- apiref
api_name:
- MicrosoftDNS_Server.StopService
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d42a443e22d382dd6e7f6ec9d528d0a1f57c6062ba0e03742033c494b75cd8a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119076740"
---
# <a name="stopservice-method-of-the-microsoftdns_server-class"></a>Método StopService da classe de \_ servidor MicrosoftDNS

O método **StopService** interrompe o servidor DNS.

## <a name="syntax"></a>Sintaxe


```mof
uint32 StopService();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

\_O êxito do erro indica que o serviço foi interrompido com êxito. Qualquer outro valor é um código de erro.

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

[**Método StartService da classe de \_ servidor MicrosoftDNS**](microsoftdns-server-startservice.md)
</dt> <dt>

[**Método StartScavenging da classe de \_ servidor MicrosoftDNS**](microsoftdns-server-startscavenging.md)
</dt> <dt>

[**Método getdistinguiname da classe de \_ servidor MicrosoftDNS**](microsoftdns-server-getdistinguishedname.md)
</dt> </dl>

 

 





