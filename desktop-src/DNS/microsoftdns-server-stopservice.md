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
ms.openlocfilehash: f811533c66185304c5c674fdfff2eda8cf5bef69
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455330"
---
# <a name="stopservice-method-of-the-microsoftdns_server-class"></a>Método StopService da classe de \_ servidor MicrosoftDNS

O método **StopService** interrompe o servidor DNS.

## <a name="syntax"></a>Sintaxe


```mof
uint32 StopService();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

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

 

 





