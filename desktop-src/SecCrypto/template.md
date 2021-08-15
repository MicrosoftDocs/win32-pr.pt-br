---
description: Representa o modelo de extensão de certificado do certificado.
ms.assetid: 1ae9220a-f6b3-47c5-bd08-a36ffd84e1f9
title: Objeto de modelo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Template
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 53c7b06fa4194d0adb4124f3978787f5d1fce0ba88e78ef99dcd6ac162eca2c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118897317"
---
# <a name="template-object"></a>Objeto de modelo

\[O **objeto** Template está disponível para uso nos sistemas operacionais especificados na seção Requisitos. Em vez disso, use a [**Classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) no namespace [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) chamando o construtor que usa um OID como parâmetro e, em seguida, use o OID para Modelo de Certificado para recuperar o modelo de extensão de certificado.\]

O **objeto** Template representa o modelo de extensão de certificado do certificado.

## <a name="when-to-use"></a>Quando usar

O **objeto** Template é usado para executar as seguintes tarefas:

-   Determine se o modelo está marcado como crítico ou presente.
-   Recupere o [*OID (identificador de*](../secgloss/o-gly.md) objeto) ou o nome do modelo.
-   Recupere a versão secundária ou principal do modelo.

## <a name="members"></a>Membros

O **objeto** Template tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

O **objeto Template** tem essas propriedades.



| Propriedade                                                 | Tipo de acesso          | Descrição                                                                                            |
|:---------------------------------------------------------|:---------------------|:-------------------------------------------------------------------------------------------------------|
| [**Iscritical**](template-iscritical.md)<br/>     | Somente leitura<br/> | Recupera um valor booliana que indica se a extensão de modelo está marcada como crítica.<br/> |
| [**IsPresent**](template-ispresent.md)<br/>       | Somente leitura<br/> | Recupera um valor booliana que indica se a extensão de modelo está presente.<br/>         |
| [**MajorVersion**](template-majorversion.md)<br/> | Somente leitura<br/> | Recupera o número de versão principal do modelo.<br/>                                         |
| [**MinorVersion**](template-minorversion.md)<br/> | Somente leitura<br/> | Recupera o número de versão secundária do modelo.<br/>                                         |
| [**Nome**](template-name.md)<br/>                 | Somente leitura<br/> | Recupera uma cadeia de caracteres que contém o nome do modelo.<br/>                                  |
| [**Oid**](template-oid.md)<br/>                   | Somente leitura<br/> | Recupera um [**objeto OID**](oid.md) que identifica o **objeto Template.**<br/>             |



 

## <a name="remarks"></a>Comentários

O **objeto Template** não pode ser criado.

Um **objeto Template** é retornado pelo método [**Certificate.Template.**](certificate-template.md)

O CAPICOM usa duas versões diferentes de modelos de certificado. A tabela a seguir mostra o nome e o OID para cada versão do modelo de certificado.



| Versão | Nome                               | OID                    |
|---------|------------------------------------|------------------------|
| V1      | EXTENSÃO SzOID \_ ENROLL \_ \_ CERTTYPE | "1.3.6.1.4.1.311.20.2" |
| V2      | MODELO DE CERTIFICADO SZOID \_ \_       | "1.3.6.1.4.1.311.21.7" |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuível<br/> | CAPICOM 2.0 ou posterior no Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
