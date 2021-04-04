---
title: Elemento CredentialsBlob (EapHostUserCredentials)
description: É usado quando a configuração do método é um BLOB binário em vez de no formato de texto XML.
ms.assetid: 9d03374b-74f6-428e-8d3e-f8dccf51884e
keywords:
- Elemento CredentialsBlob EAPHost
topic_type:
- apiref
api_name:
- CredentialsBlob
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1fe7514c3aff50a7ecddadb3d8073a37b6c770eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085342"
---
# <a name="credentialsblob-eaphostusercredentials-element"></a>Elemento CredentialsBlob (EapHostUserCredentials)

O elemento **CredentialsBlob (EapHostUserCredentials)** é usado quando a configuração do método é um blob binário em vez de no formato de texto XML.

``` syntax
<xs:element name="CredentialsBlob"
    type="hexBinary"
 />
```

O elemento **CredentialsBlob** é definido pelo elemento [**EapHostUserCredentials**](eaphostusercredentialsschema-eaphostusercredentials-element.md) .

## <a name="remarks"></a>Comentários

As [**credenciais**](eaphostusercredentialsschema-credentials-eaphostusercredentials-element.md) e os elementos **CredentialsBlob** não podem ser usados simultaneamente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Contexto de definição do elemento no esquema**
</dt> <dt>

[**EapHostUserCredentials**](eaphostusercredentialsschema-eaphostusercredentials-element.md)
</dt> <dt>

**Possível elemento pai imediato na instância de esquema**
</dt> <dt>

[**EapHostUserCredentials**](eaphostusercredentialsschema-eaphostusercredentials-element.md)
</dt> <dt>

[EAPHost e esquema herdado](eaphost-schemas.md)
</dt> <dt>

[Esquema eaphostusercredentials](eaphostusercredentialsschema-schema.md)
</dt> </dl>

 

 





