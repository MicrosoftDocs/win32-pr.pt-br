---
description: Identifica o número de identificação do SIM para dispositivos GSM.
ms.assetid: 980afba4-fc31-4da0-ba01-6eb8e3db0ac8
title: Elemento SimIccID (MBNProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SimIccID
api_type:
- Schema
ms.openlocfilehash: 8a6e4a20d93396337e2af0f0533486618dc707760f1ccd5c4f20f399cbdbf203
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119777856"
---
# <a name="simiccid-mbnprofile-element"></a>Elemento SimIccID (MBNProfile)

O elemento **SimIccID (MBNProfile)** identifica o número de identificação do sim para dispositivos GSM.

Esse elemento é opcional e é definido pelo serviço de banda larga móvel para uso interno. Um aplicativo não deve definir esse campo durante a criação ou atualização de um perfil.

``` syntax
<xs:element name="SimIccID"
    type="simIccIDType"
 />
```

O elemento **SimIccID** é definido pelo elemento [**MBNProfile**](schema-mbnprofile-element.md) .

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

 

 




