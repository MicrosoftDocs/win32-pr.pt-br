---
title: Método StartScavenging da classe MicrosoftDNS_Server
description: O método StartScavenging inicia a eliminação de registros obsoletos nas zonas sujeitas à eliminação.
ms.assetid: ee1bc0e0-9334-4971-a524-4bb8a9015b5b
keywords:
- DNS do método StartScavenging
- Método StartScavenging DNS, classe MicrosoftDNS_Server
- MicrosoftDNS_Server classe DNS, método StartScavenging
topic_type:
- apiref
api_name:
- MicrosoftDNS_Server.StartScavenging
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6173021ca49dc73b7ec89f60b097b2179078a774c9a40c26fda2c41b2ad25f2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119874766"
---
# <a name="startscavenging-method-of-the-microsoftdns_server-class"></a>Método StartScavenging da classe de \_ servidor MicrosoftDNS

O método **StartScavenging** inicia a eliminação de registros obsoletos nas zonas sujeitas à eliminação.

## <a name="syntax"></a>Sintaxe


```mof
uint32 StartScavenging();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

\_O êxito do erro indica que a limpeza foi iniciada com êxito. Qualquer outro valor é um código de erro.

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

[**Método StopService da classe de \_ servidor MicrosoftDNS**](microsoftdns-server-stopservice.md)
</dt> <dt>

[**Método getdistinguiname da classe de \_ servidor MicrosoftDNS**](microsoftdns-server-getdistinguishedname.md)
</dt> </dl>

 

 





