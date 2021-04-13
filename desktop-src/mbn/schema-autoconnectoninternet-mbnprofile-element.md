---
description: Especifica se o dispositivo de banda larga móvel se conectará automaticamente a uma rede.
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
ms.openlocfilehash: fd08e93572d7d0af8b490ac079e3057413c469ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164576"
---
# <a name="autoconnectoninternet-mbnprofile-element"></a>Elemento AutoConnectOnInternet (MBNProfile)

O elemento **AutoConnectOnInternet (MBNProfile)** especifica se o dispositivo de banda larga móvel se conectará automaticamente a uma rede.

Se definido como **false**, a lógica de conexão automática do serviço de banda larga móvel não será usada se houver qualquer outra conectividade de rede disponível para o sistema. Se definido como **true**, o serviço de banda larga móvel tentará conectar automaticamente o dispositivo à rede com base na configuração de conexão automática definida no elemento [**ConnectionMode**](schema-connectionmode-mbnprofile-element.md) .

**Windows 8 e posterior:** Este elemento foi preterido. Use o método [**WcmSetProperty**](/windows/desktop/api/wcmapi/nf-wcmapi-wcmsetproperty) com o parâmetro *Property* definido como **WCM \_ \_ propriedade global \_ minimizar \_ política** em vez disso.

``` syntax
<xs:element name="AutoConnectOnInternet"
    type="boolean"
 />
```

O elemento **AutoConnectOnInternet** é definido pelo elemento [**MBNProfile**](schema-mbnprofile-element.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------|
| Cliente mínimo com suporte<br/> | Aplicativos de \[ aplicativos da área de trabalho do Windows 7 \| UWP\]<br/> |
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

 

