---
title: Tipo Complexo BaseEapParameters – Propriedades do usuário
description: Define o elemento que especificou o método herdado selecionado e as credenciais específicas do método.
ms.assetid: bc42e536-f741-4821-8453-6c0631daad3e
keywords:
- Tipo complexo BaseEapParameters EAPHost
topic_type:
- apiref
api_name:
- BaseEapParameters
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 80ae1dc749d1c31ee11809b530fe1b04a59ce3e4e4dc76e84323b7dc078ec44a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119978286"
---
# <a name="baseeapparameters-complex-type---user-properties"></a>Tipo Complexo BaseEapParameters – Propriedades do usuário

O **tipo complexo BaseEapParameters** define o elemento que especificou o método herdado selecionado e as credenciais específicas do método.

O método pode definir os elementos constituintes **dentro de BaseEapParameters**; o método também executa a validação de esquema nos elementos em **BaseEapParameters**.

``` syntax
<xs:complexType name="BaseEapParameters">
    <xs:sequence>
        <xs:element name="Type"
            type="integer"
         />
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##any"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>Elementos filho



| Elemento                                                                      | Type    | Descrição                                                                                               |
|------------------------------------------------------------------------------|---------|-----------------------------------------------------------------------------------------------------------|
| [**Type**](baseeapuserpropertiesv1schema-type-baseeapparameters-element.md) | Número inteiro | Define o elemento de espaço reservado para o tipo de método selecionado e credenciais específicas do método. <br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[EAPHost e esquema herdado](eaphost-schemas.md)
</dt> <dt>

[Esquema baseeapuserpropertiesv1](baseeapuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





