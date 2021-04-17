---
description: Especifica o método de transmissão usado para EAPOL-Start mensagens.
ms.assetid: 8d49d19a-8122-4191-bb46-92a2016bcfee
title: Elemento suplicable (OneX)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- supplicantMode
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 33d58bd247a220ca93ed4d2a05886be107afd4c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105775681"
---
# <a name="supplicantmode-onex-element"></a>Elemento suplicable (OneX)

O elemento suplicable (OneX) especifica o método de transmissão usado para EAPOL-Start mensagens. A tabela a seguir descreve os valores possíveis.



| Valor               | Descrição                                                                                                                                                              |
|---------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| inhibitTransmission | EAPOL-Start mensagens não são transmitidas. Válido somente para perfis de LAN com fio.                                                                                             |
| includeLearning     | O cliente determina quando enviar EAPOL-Start pacotes com base na capacidade de rede. EAPOL-Start mensagens são enviadas somente quando necessário. Válido somente para perfis de LAN com fio. |
| conformidade           | EAPOL-Start mensagens são transmitidas conforme especificado pelo 802.1 X. Válido para perfis de LAN com e sem fio.                                                             |



 

Esse elemento é opcional. Quando suplicamode não é especificado em um perfil, um valor de `compliant` é usado para perfis de LAN com e sem fio.

**Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** Esse elemento será ignorado se estiver presente em um perfil.

``` syntax
<xs:element name="supplicantMode">
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="inhibitTransmission"
             />
            <xs:enumeration
                value="includeLearning"
             />
            <xs:enumeration
                value="compliant"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

O elemento **suplicamode** é definido pelo elemento [**Onex**](onexschema-onex-element.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Contexto de definição do elemento no esquema**
</dt> <dt>

[**802.1x**](onexschema-onex-element.md)
</dt> <dt>

**Possível elemento pai imediato na instância de esquema**
</dt> <dt>

[**802.1x**](onexschema-onex-element.md)
</dt> </dl>

 

 




