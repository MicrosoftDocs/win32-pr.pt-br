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
ms.openlocfilehash: fedd64979ad74ceac3f6d54af58c57d8d8b2b134
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750492"
---
# <a name="template-object"></a>Objeto de modelo

\[O objeto de **modelo** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Em vez disso, use a [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) chamando o construtor que usa um OID como parâmetro e, em seguida, use o OID para o modelo de certificado para recuperar o modelo de extensão de certificado.\]

O objeto de **modelo** representa o modelo de extensão de certificado do certificado.

## <a name="when-to-use"></a>Quando usar

O objeto de **modelo** é usado para executar as seguintes tarefas:

-   Determine se o modelo está marcado como crítico ou presente.
-   Recupere o [*identificador de objeto*](../secgloss/o-gly.md) (OID) ou o nome do modelo.
-   Recupere a versão secundária ou principal do modelo.

## <a name="members"></a>Membros

O objeto de **modelo** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

O objeto de **modelo** tem essas propriedades.



| Propriedade                                                 | Tipo de acesso          | Descrição                                                                                            |
|:---------------------------------------------------------|:---------------------|:-------------------------------------------------------------------------------------------------------|
| [**IsCritical**](template-iscritical.md)<br/>     | Somente leitura<br/> | Recupera um valor booliano que indica se a extensão do modelo está marcada como crítica.<br/> |
| [**IsPresent**](template-ispresent.md)<br/>       | Somente leitura<br/> | Recupera um valor booliano que indica se a extensão do modelo está presente.<br/>         |
| [**MajorVersion**](template-majorversion.md)<br/> | Somente leitura<br/> | Recupera o número de versão principal do modelo.<br/>                                         |
| [**MinorVersion**](template-minorversion.md)<br/> | Somente leitura<br/> | Recupera o número de versão secundária do modelo.<br/>                                         |
| [**Nome**](template-name.md)<br/>                 | Somente leitura<br/> | Recupera uma cadeia de caracteres que contém o nome do modelo.<br/>                                  |
| [**OIDs**](template-oid.md)<br/>                   | Somente leitura<br/> | Recupera um objeto [**OID**](oid.md) que identifica o objeto de **modelo** .<br/>             |



 

## <a name="remarks"></a>Comentários

Não é possível criar o objeto de **modelo** .

Um objeto de **modelo** é retornado pelo método [**Certificate. Template**](certificate-template.md) .

O CAPICOM usa duas versões diferentes dos modelos de certificado. A tabela a seguir mostra o nome e o OID para cada versão do modelo de certificado.



| Versão | Nome                               | OID                    |
|---------|------------------------------------|------------------------|
| V1      | \_ \_ extensão certtype de registro szOID \_ | "1.3.6.1.4.1.311.20.2" |
| V2      | \_modelo de certificado szOID \_       | "1.3.6.1.4.1.311.21.7" |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuível<br/> | CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
