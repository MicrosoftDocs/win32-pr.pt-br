---
description: Fornece propriedades e métodos que você pode usar para escolher, gerenciar e usar repositórios de certificados e os certificados nesses armazenamentos.
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
ms.openlocfilehash: 4e8a14fcecf0ded2e4e1a56e2b98e4ac4838b776
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750493"
---
# <a name="store-object"></a>Armazenar objeto

\[O objeto **Store** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Em vez disso, use a [**classe X509Store**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

O objeto **Store** fornece propriedades e métodos que você pode usar para escolher, gerenciar e usar [*repositórios de certificados*](../secgloss/c-gly.md) e os certificados nesses armazenamentos. O CAPICOM pode usar armazenamentos de usuário, máquina local, memória e Active Directory atuais. Além disso, os repositórios oferecem suporte a repositórios de certificados baseados em cartão inteligente. Os desenvolvedores devem estar cientes de que alguns métodos podem falhar com algumas lojas se forem tentadas operações para as quais o usuário não tem direitos.

## <a name="members"></a>Membros

O objeto **Store** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

O objeto **Store** tem esses métodos.



| Método                         | Descrição                                                                                                                                                                                                      |
|:-------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Agrega**](store-add.md)       | Adiciona um objeto de [**certificado**](certificate.md) ao repositório de certificados aberto.<br/>                                                                                                                       |
| [**Fechar**](store-close.md)   | Fecha um repositório de certificados aberto.<br/> **CAPICOM 2.0.0.3 e anteriores:** Não há suporte para o método [**Close**](store-close.md) .<br/>                                                               |
| [**Apagar**](store-delete.md) | Exclui o repositório de certificados representado pelo objeto de [**armazenamento**](certificate.md) atual.<br/> **CAPICOM 2.0.0.3 e anteriores:** Não há suporte para o método [**delete**](store-delete.md) .<br/> |
| [**Exportação**](store-export.md) | Exporta o repositório de um [*blob*](../secgloss/b-gly.md)codificado.<br/>                                                                                                       |
| [**Importar**](store-import.md) | Importa um repositório exportado anteriormente.<br/>                                                                                                                                                                  |
| [**Carregar**](store-load.md)     | Importa objetos de [**certificado**](certificate.md) de um arquivo para o repositório.<br/>                                                                                                                        |
| [**Aberto**](store-open.md)     | Abre um repositório de certificados.<br/>                                                                                                                                                                            |
| [**Remover**](store-remove.md) | Remove um objeto de [**certificado**](certificate.md) de um armazenamento aberto.<br/>                                                                                                                               |



 

### <a name="properties"></a>Propriedades

O objeto **Store** tem essas propriedades.



| Propriedade                                              | Tipo de acesso          | Descrição                                                                                                                                                                                           |
|:------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Certificados**](store-certificates.md)<br/> | Somente leitura<br/> | Recupera a coleção de [**certificados**](certificates.md) do repositório. Essa é a propriedade padrão.<br/>                                                                                  |
| [**Local**](store-location.md)<br/>         | Somente leitura<br/> | Recupera o local do repositório de certificados que este objeto representa.<br/> **CAPICOM 2.0.0.3 e anteriores:** Não há suporte para a propriedade [**Location**](store-location.md) .<br/> |
| [**Nome**](store-name.md)<br/>                 | Somente leitura<br/> | Recupera o nome do repositório de certificados que este objeto representa.<br/> **CAPICOM 2.0.0.3 e anteriores:** Não há suporte para a propriedade [**Name**](store-name.md) .<br/>             |



 

## <a name="remarks"></a>Comentários

O objeto **Store** pode ser criado e é seguro para scripts. O ProgID do objeto de **armazenamento** é CAPICOM. Store. 2.

**CAPICOM 1. *x*:** o ProgID do objeto da **loja** é CAPICOM. Store. 1.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuível<br/> | CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objetos de criptografia**](cryptography-objects.md)
</dt> </dl>

 

 
