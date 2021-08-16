---
description: Especifica se o dispositivo de Banda Larga Móvel se conectará automaticamente a uma rede.
ms.assetid: a2673ac7-6d70-4005-9ac4-cf670eba26ae
title: Elemento AutoConnectOnInternet (MBNProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AutoConnectOnInternet
api_type:
- Schema
ms.openlocfilehash: 3a10804e91ee34125c25c320a49b5f7251f720ed9ce6c770c2aa4af5167a8511
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117881471"
---
# <a name="autoconnectoninternet-mbnprofile-element"></a>Elemento AutoConnectOnInternet (MBNProfile)

O **elemento AutoConnectOnInternet (MBNProfile)** especifica se o dispositivo de Banda Larga Móvel se conectará automaticamente a uma rede.

Se definido como **FALSE,** a lógica de conexão automática do serviço de Banda Larga Móvel não será usada se houver qualquer outra conectividade de rede disponível para o sistema. Se definido como **TRUE,** o serviço de Banda Larga Móvel tentará conectar automaticamente o dispositivo à rede com base na configuração de conexão automática definida no [**elemento ConnectionMode.**](schema-connectionmode-mbnprofile-element.md)

**Windows 8 e posterior:** Esse elemento foi preterido. Use o [**método WcmSetProperty com**](/windows/desktop/api/wcmapi/nf-wcmapi-wcmsetproperty) o parâmetro *Property* definido como **wcm global property \_ minimize \_ \_ \_ policy.**

``` syntax
<xs:element name="AutoConnectOnInternet"
    type="boolean"
 />
```

O **elemento AutoConnectOnInternet** é definido pelo [**elemento MBNProfile.**](schema-mbnprofile-element.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos UWP da área \| de trabalho\]<br/> |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                         |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Contexto de definição do elemento no esquema**
</dt> <dt>

[**MBNProfile**](schema-mbnprofile-element.md)
</dt> <dt>

**Possível elemento pai imediato na instância de esquema**
</dt> <dt>

[**MBNProfile**](schema-mbnprofile-element.md)
</dt> </dl>

 

