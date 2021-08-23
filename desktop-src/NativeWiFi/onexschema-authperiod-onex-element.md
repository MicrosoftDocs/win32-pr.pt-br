---
description: Especifica o período máximo de tempo, em segundos, no qual um cliente aguarda uma resposta do autenticador.
ms.assetid: 5cb2e164-913f-4c35-854f-aac8ed180c46
title: Elemento authPeriod (OneX)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- authPeriod
api_type:
- Schema
api_location: ''
ms.openlocfilehash: ccaef08f65baffa0d7b9a921afd9db78a6ac6c6dd1d0bf4fd8075454fe38be21
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119684850"
---
# <a name="authperiod-onex-element"></a>Elemento authPeriod (OneX)

O elemento authPeriod (OneX) especifica o período máximo de tempo, em segundos, no qual um cliente aguarda uma resposta do autenticador. Se uma resposta não for recebida dentro do período especificado, o cliente assumirá que não há nenhum autenticador presente na rede.

Esse elemento é opcional. Quando authPeriod não é especificado em um perfil, um valor de 18 segundos é usado.

**Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** Esse elemento será ignorado se estiver presente em um perfil.

``` syntax
<xs:element name="authPeriod">
    <xs:simpleType>
        <xs:restriction
            base="integer"
        >
            <xs:enumeration
                value="1"
             />
            <xs:enumeration
                value="3600"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

O **elemento authPeriod** é definido pelo [**elemento OneX.**](onexschema-onex-element.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Contexto de definição do elemento no esquema**
</dt> <dt>

[**Onex**](onexschema-onex-element.md)
</dt> <dt>

**Possível elemento pai imediato na instância de esquema**
</dt> <dt>

[**Onex**](onexschema-onex-element.md)
</dt> </dl>

 

 




