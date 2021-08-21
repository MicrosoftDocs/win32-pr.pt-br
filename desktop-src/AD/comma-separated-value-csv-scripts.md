---
title: Scripts de valores separados por vírgulas (CSV)
description: o Windows 2000 inclui um utilitário de linha de comando, CSVDE, para importar objetos de diretório usando arquivos .csv e exportar objetos de diretório como arquivos .csv.
ms.assetid: fda242eb-7561-444f-b560-94bd87fe4e39
ms.tgt_platform: multiple
keywords:
- ANÚNCIO de scripts de valores separados por vírgula
- Scripts, AD de valor separado por vírgula
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3764593303f7f2a81c524df16665c74afd1c83909e8286511090ee6c84323bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118022442"
---
# <a name="comma-separated-value-csv-scripts"></a>Scripts de valores separados por vírgulas (CSV)

o Windows 2000 inclui um utilitário de linha de comando, CSVDE, para importar objetos de diretório usando arquivos .csv e exportar objetos de diretório como arquivos .csv. Os scripts CSV são criados para facilitar o uso. A primeira linha no script identifica os atributos nas linhas a seguir. As colunas são separadas por vírgulas. o formato de arquivo é compatível com o formato de .csv Microsoft Excel, para que os arquivos sejam facilmente criados. Use Excel ou qualquer outra ferramenta que possa ler e gravar arquivos .csv. O CSVDE dá suporte a Unicode.

## <a name="example-csv-file"></a>Exemplo de arquivo CSV

O exemplo de código a seguir é um arquivo CSV que adiciona uma classe auxiliar.

``` syntax
DN,adminDisplayName,cn,defaultHidingValue,defaultObjectCategory,description,governsID,lDAPDisplayName,mayContain,mustContain,distinguishedName,objectCategory,objectClass,objectClassCategory,possSuperiors,name,rDNAttID,schemaIDGUID,subClassOf,auxiliaryClass,defaultSecurityDescriptor
"CN=My-Test-Auxiliary-Class1,CN=Schema,CN=Configuration,DC=myorg,DC=mytest,DC=Fabrikam,DC=com",My-Test-Auxiliary-Class1,My-Test-Auxiliary-Class1,FALSE,"CN=My-Test-Auxiliary-Class1,CN=Schema,CN=Configuration,DC=myorg,DC=mytest,DC=Fabrikam,DC=com",Test class used to show how to add an auxiliary class.,1.2.840.113556.1.4.7000.159.24.10.611.11,myTestAuxiliaryClass1,myTestAttributeDNString,description;myTestAttributeUnicodeString,"CN=My-Test-Auxiliary-Class1,CN=Schema,CN=Configuration,DC=myorg,DC=mytest,DC=fabrikam,DC=com","CN=Class-Schema,CN=Schema,CN=Configuration,DC=myorg,DC=mytest,DC=fabrikam,DC=com",classSchema,3,domainDNS;container,My-Test-Auxiliary-Class1,cn,X'9a6b3176c5dbd2118bd00000f875b660',top,,
```

 

 




