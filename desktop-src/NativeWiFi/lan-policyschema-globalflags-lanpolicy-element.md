---
description: Contém as configurações globais para a configuração automática de redes com fio.
ms.assetid: 172cf15c-cd51-43d4-ae5d-f9460c2a40e2
title: Elemento globalFlags (LANPolicy)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- globalFlags
api_type:
- Schema
api_location: ''
ms.openlocfilehash: bfbfecbc1d60e34a913bb523f5af8c2ab25665fd689976c87725d392f6ea26c2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119801126"
---
# <a name="globalflags-lanpolicy-element"></a>Elemento globalFlags (LANPolicy)

O elemento globalFlags (LANPolicy) contém as configurações globais para a configuração automática de redes com fio.

``` syntax
<xs:element name="globalFlags">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="enableAutoConfig"
                type="boolean"
             />
            <xs:any
                processContents="lax"
                minOccurs="0"
                maxOccurs="unbounded"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

O elemento **globalFlags** é definido pelo elemento [**LANPolicy**](lan-policyschema-lanpolicy-element.md) .

## <a name="child-elements"></a>Elementos filho



| Elemento                                                                           | Type    | Descrição                                                                                                                                                                          |
|-----------------------------------------------------------------------------------|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**enableAutoConfig**](lan-policyschema-enableautoconfig-globalflags-element.md) | booleano | Especifica se os computadores usam o serviço de configuração automática interno para gerenciar conexões com redes com fio que exigem autenticação de camada 2 (como 802.1 X).<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Contexto de definição do elemento no esquema**
</dt> <dt>

[**LANPolicy**](lan-policyschema-lanpolicy-element.md)
</dt> <dt>

**Possível elemento pai imediato na instância de esquema**
</dt> <dt>

[**LANPolicy**](lan-policyschema-lanpolicy-element.md)
</dt> </dl>

 

 




