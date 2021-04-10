---
title: Elemento SimpleCertSelection (CertSelection)
description: Saiba mais sobre o elemento SimpleCertSelection (CertSelection). Esse elemento determina como o usuário seleciona um certificado.
ms.assetid: 28454877-fd07-4b47-9544-f2b4e91c6651
keywords:
- Elemento SimpleCertSelection EAPHost
topic_type:
- apiref
api_name:
- SimpleCertSelection
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 30af9872f7583232e91b037c5b8961e18c7ce863
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104008377"
---
# <a name="simplecertselection-certselection-element"></a>Elemento SimpleCertSelection (CertSelection)

O elemento **SimpleCertSelection (CertSelection)** determina como o usuário seleciona um certificado.

``` syntax
<xs:element name="SimpleCertSelection"
    type="boolean"
 />
```

O elemento **SimpleCertSelection** é definido pelo tipo complexo [**CertSelection**](eaptlsconnectionpropertiesv1schema-certselection-complextype.md) .

## <a name="remarks"></a>Comentários

**SimpleCertSelection** é true por padrão. Se **SimpleCertSelection** for true, o EAP-TLS executará uma pesquisa de certificado simples sem nenhuma lista suspensa para a seleção de certificados. Se **SimpleCertSelection** for false, o EAP-TLS ilustrará para o usuário o certificado adequado a ser selecionado.

## <a name="requirements"></a>Requisitos



| Função | SO com suporte mínimo |
|------|----------------------|
| Cliente<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Contexto de definição do elemento no esquema**
</dt> <dt>

[**CertSelection**](eaptlsconnectionpropertiesv1schema-certselection-complextype.md)
</dt> <dt>

**Possível elemento pai imediato na instância de esquema**
</dt> <dt>

[**CertificateStore (CredentialsSourceParameters)**](eaptlsconnectionpropertiesv1schema-certificatestore-credentialssourceparameters-element.md)
</dt> <dt>


</dt> <dt>

[EAPHost e esquema herdado](eaphost-schemas.md)
</dt> <dt>

[Esquema eaptlsconnectionpropertiesv1](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[Elementos do esquema eaptlsconnectionpropertiesv1](eaptlsconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





