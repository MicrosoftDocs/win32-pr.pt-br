---
title: Tipo complexo CertSelection
description: Saiba mais sobre o tipo complexo CertSelection. Esse tipo determina como o usuário seleciona um certificado.
ms.assetid: f5a37258-8ab0-4736-9721-6c2800769c74
keywords:
- CertSelection tipo complexo EAPHost
topic_type:
- apiref
api_name:
- CertSelection
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ba22df8dca61696f214e495542319168183dd2bf
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104294506"
---
# <a name="certselection-complex-type"></a>Tipo complexo CertSelection

O tipo complexo **CertSelection** determina como o usuário seleciona um certificado.

``` syntax
<xs:complexType name="CertSelection">
    <xs:sequence>
        <xs:element name="SimpleCertSelection"
            type="boolean"
            minOccurs="0"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>Elementos filho



| Elemento                                                                                                     | Type    | Descrição                                                                                                                                                                                                                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------------|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SimpleCertSelection**](eaptlsconnectionpropertiesv1schema-simplecertselection-certselection-element.md) | booleano | É TRUE por padrão. Se [**SimpleCertSelection**](eaptlsconnectionpropertiesv1schema-simplecertselection-certselection-element.md) for true, o EAP-TLS executará uma pesquisa de certificado simples sem nenhuma lista suspensa para a seleção de certificados. Se **SimpleCertSelection** for false, o EAP-TLS ilustrará para o usuário o certificado adequado a ser selecionado.<br/> |



## <a name="requirements"></a>Requisitos



| Função | Versão mínima do sistema operacional com suporte |
|------|------------------------------|
| Cliente<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[EAPHost e esquema herdado](eaphost-schemas.md)
</dt> <dt>

[Esquema eaptlsconnectionpropertiesv1](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[Tipos complexos de esquema eaptlsconnectionpropertiesv1](eaptlsconnectionpropertiesv1schema-complex-types.md)
</dt> </dl>

 

 





