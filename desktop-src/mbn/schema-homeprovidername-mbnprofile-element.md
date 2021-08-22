---
description: Identifica o nome do provedor de página inicial para o cartão SIM/dispositivo especificado.
ms.assetid: 05d65091-5a1d-427a-8f51-1e1b9d189571
title: Elemento HomeProviderName (MBNProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HomeProviderName
api_type:
- Schema
ms.openlocfilehash: 1868be18dc7acf9d5146f987658feb006714fbcc3db35883007afd01c308609e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035824"
---
# <a name="homeprovidername-mbnprofile-element"></a>Elemento HomeProviderName (MBNProfile)

O elemento **HomeProviderName (MBNProfile)** identifica o nome do provedor de Home para o cartão Sim/dispositivo especificado.

Esse elemento é opcional e é definido pelo serviço de banda larga móvel para uso interno. Um aplicativo não deve definir esse campo durante a criação ou atualização de um perfil.

``` syntax
<xs:element name="HomeProviderName"
    type="providerNameType"
 />
```

O elemento **HomeProviderName** é definido pelo elemento [**MBNProfile**](schema-mbnprofile-element.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[aplicativos UWP para aplicativos de área de trabalho Windows 7 \|\]<br/> |
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

 

 




