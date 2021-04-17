---
description: Representa uma coleção de objetos OID.
ms.assetid: 2c4ff87a-58e1-46aa-9680-29062b05308c
title: Objeto OIDs
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OIDs
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 894689c214d8b7d352a2453d2d62c847866b9bc5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105770451"
---
# <a name="oids-object"></a>Objeto OIDs

\[O objeto **OIDs** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Em vez disso, use a [**classe OidCollection**](/dotnet/api/system.security.cryptography.oidcollection?view=netcore-3.1) no namespace [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

O objeto **OIDs** representa uma coleção de objetos [**OID**](oid.md) . Cada objeto de [**OID**](oid.md) representa um único identificador de objeto.

## <a name="when-to-use"></a>Quando usar

O objeto **OIDs** é usado para executar as seguintes tarefas:

-   Adicionar ou remover um objeto [**OID**](oid.md) da coleção.
-   Limpe todos os objetos [**OID**](oid.md) da coleção.
-   Recupere o número de identificadores de objeto na coleção.
-   Recupere um objeto [**OID**](oid.md) específico da coleção.
-   Iterar pela coleção.

## <a name="members"></a>Membros

O objeto **OIDs** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

O objeto **OIDs** tem esses métodos.



| Método                        | Descrição                                                                  |
|:------------------------------|:-----------------------------------------------------------------------------|
| [**Agrega**](oids-add.md)       | Adiciona um objeto [**OID**](oid.md) à coleção.<br/>              |
| [**Formatação**](oids-clear.md)   | Limpa todos os objetos [**OID**](oid.md) da coleção.<br/>        |
| [**Remover**](oids-remove.md) | Remove um objeto [**OID**](oid.md) indexado da coleção.<br/> |



 

### <a name="properties"></a>Propriedades

O objeto **OIDs** tem essas propriedades.



| Propriedade                                     | Tipo de acesso          | Descrição                                                                                                                                                                                                                     |
|:---------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](oids-newenum.md)<br/> | Somente leitura<br/> | Recupera uma interface [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) em um objeto que pode ser usado para enumerar a coleção. Essa propriedade é oculta em Visual Basic Scripting Edition (VBScript).<br/> |
| [**Contar**](oids-count.md)<br/>       | Somente leitura<br/> | Recupera o número de objetos [**OID**](oid.md) na coleção.<br/>                                                                                                                                                |
| [**Item**](oids-item.md)<br/>         | Somente leitura<br/> | Recupera um objeto [**OID**](oid.md) indexado da coleção. Essa é a propriedade padrão.<br/>                                                                                                                    |



 

## <a name="remarks"></a>Comentários

Não é possível criar o objeto **OIDs** .

O objeto **OIDs** é usado pelas seguintes propriedades:

-   [**CertificateStatus.ApplicationPolicies**](certificatestatus-applicationpolicies.md)
-   [**CertificateStatus.CertificatePolicies**](certificatestatus-certificatepolicies.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuível<br/> | CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
