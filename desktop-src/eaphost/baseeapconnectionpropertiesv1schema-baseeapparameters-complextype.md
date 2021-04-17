---
title: Tipo complexo BaseEapParameters – Propriedades de conexão
description: Define o elemento de espaço reservado para o tipo de método e a configuração específica do método.
ms.assetid: 510debce-545c-4ce1-965b-e4b2185b7983
keywords:
- BaseEapParameters tipo complexo EAPHost
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
ms.openlocfilehash: f3bfb9f6c833900967525467202421cf94166405
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/16/2021
ms.locfileid: "105790507"
---
# <a name="baseeapparameters-complex-type---connection-properties"></a>Tipo complexo BaseEapParameters – Propriedades de conexão

O tipo complexo **BaseEapParameters** define o elemento de espaço reservado para o tipo de método e a configuração específica do método.

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



| Elemento                                                                            | Type    | Description                                     |
|------------------------------------------------------------------------------------|---------|-------------------------------------------------|
| [**Type**](baseeapconnectionpropertiesv1schema-type-baseeapparameters-element.md) | Número inteiro | Qualquer instância de esquema é permitida aqui.<br/> |



## <a name="remarks"></a>Comentários

Em **BaseEapParameters** , o método pode definir os elementos constituintes. O método também executa a validação de esquema nos elementos no **BaseEapParameters**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[EAPHost e esquema herdado](eaphost-schemas.md)
</dt> <dt>

[Esquema baseeapconnectionpropertiesv1](baseeapconnectionpropertiesv1schema-schema.md)
</dt> </dl>

 

 





