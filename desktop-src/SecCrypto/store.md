---
description: Fornece propriedades e métodos que você pode usar para escolher, gerenciar e usar os armazenamentos de certificados e os certificados nesses armazenamentos.
ms.assetid: de4eecf7-c03b-4733-ac29-d5b26b873dba
title: Armazenar objeto
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 1de500d10d6bd5493492b62a2abb618be3cdb19d48a89beaf7ab83d55a86ac28
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117972293"
---
# <a name="store-object"></a>Armazenar objeto

\[O **objeto** Store está disponível para uso nos sistemas operacionais especificados na seção Requisitos. Em vez disso, [**use a Classe X509Store**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) no namespace [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

O **objeto** Store fornece propriedades e métodos que você pode usar para escolher, gerenciar e usar os armazenamentos de [*certificados*](../secgloss/c-gly.md) e os certificados nesses armazenamentos. O CAPICOM pode usar armazenamentos Do Usuário Atual, Computador Local, Memória e Active Directory. Além disso, os armazenamentos são suportados por armazenamentos de certificados baseados em cartão inteligente. Os desenvolvedores devem estar cientes de que alguns métodos poderão falhar com alguns armazenamentos se tentarem operações para as quais o usuário não tem direitos.

## <a name="members"></a>Membros

O **objeto Store** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

O **objeto Store** tem esses métodos.



| Método                         | Descrição                                                                                                                                                                                                      |
|:-------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Adicionar**](store-add.md)       | Adiciona um [**objeto Certificate**](certificate.md) ao armazenamento de certificados aberto.<br/>                                                                                                                       |
| [**Perto**](store-close.md)   | Fecha um armazenamento de certificados aberto.<br/> **CAPICOM 2.0.0.3 e versões anteriores:** Não [**há**](store-close.md) suporte para o método Close.<br/>                                                               |
| [**Excluir**](store-delete.md) | Exclui o armazenamento de certificados representado pelo objeto [**Store**](certificate.md) atual.<br/> **CAPICOM 2.0.0.3 e versões anteriores:** Não [**há suporte**](store-delete.md) para o método Delete.<br/> |
| [**Exportação**](store-export.md) | Exporta o armazenamento de um [*BLOB codificado.*](../secgloss/b-gly.md)<br/>                                                                                                       |
| [**Importar**](store-import.md) | Importa um armazenamento exportado anteriormente.<br/>                                                                                                                                                                  |
| [**Carregar**](store-load.md)     | Importa objetos [**de certificado**](certificate.md) de um arquivo para o armazenamento.<br/>                                                                                                                        |
| [**Aberto**](store-open.md)     | Abre um armazenamento de certificados.<br/>                                                                                                                                                                            |
| [**Remover**](store-remove.md) | Remove um [**objeto Certificate**](certificate.md) de um armazenamento aberto.<br/>                                                                                                                               |



 

### <a name="properties"></a>Propriedades

O **objeto Store** tem essas propriedades.



| Propriedade                                              | Tipo de acesso          | Descrição                                                                                                                                                                                           |
|:------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Certificados**](store-certificates.md)<br/> | Somente leitura<br/> | Recupera a [**coleção Certificados**](certificates.md) do armazenamento. Essa é a propriedade padrão.<br/>                                                                                  |
| [**Local**](store-location.md)<br/>         | Somente leitura<br/> | Recupera o local do armazenamento de certificados que esse objeto representa.<br/> **CAPICOM 2.0.0.3 e versões anteriores:** Não [**há**](store-location.md) suporte para a propriedade Location.<br/> |
| [**Nome**](store-name.md)<br/>                 | Somente leitura<br/> | Recupera o nome do armazenamento de certificados que esse objeto representa.<br/> **CAPICOM 2.0.0.3 e versões anteriores:** Não [**há suporte**](store-name.md) para a propriedade Name.<br/>             |



 

## <a name="remarks"></a>Comentários

O **objeto Store** pode ser criado e é seguro para scripts. O ProgID para o **objeto Store** é CAPICOM. Store.2.

**CAPICOM 1. *x*:** o ProgID para o **objeto Store** é CAPICOM. Store.1.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuível<br/> | CAPICOM 2.0 ou posterior no Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objetos de criptografia**](cryptography-objects.md)
</dt> </dl>

 

 
