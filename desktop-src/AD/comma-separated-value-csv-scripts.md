---
title: Scripts de valores separados por vírgulas (CSV)
description: O Windows 2000 inclui um utilitário de linha de comando, CSVDE, para importar objetos de diretório usando arquivos. csv e exportar objetos de diretório como arquivos. csv.
ms.assetid: fda242eb-7561-444f-b560-94bd87fe4e39
ms.tgt_platform: multiple
keywords:
- ANÚNCIO de scripts de valores separados por vírgula
- Scripts, AD de valor separado por vírgula
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec737f971bd7e462b8f6f0ef6e9e3df786a207cf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103634802"
---
# <a name="comma-separated-value-csv-scripts"></a><span data-ttu-id="6a254-105">Scripts de valores separados por vírgulas (CSV)</span><span class="sxs-lookup"><span data-stu-id="6a254-105">Comma-separated Value (CSV) Scripts</span></span>

<span data-ttu-id="6a254-106">O Windows 2000 inclui um utilitário de linha de comando, CSVDE, para importar objetos de diretório usando arquivos. csv e exportar objetos de diretório como arquivos. csv.</span><span class="sxs-lookup"><span data-stu-id="6a254-106">Windows 2000 includes a command-line utility, CSVDE, to import directory objects using .csv files and export directory objects as .csv files.</span></span> <span data-ttu-id="6a254-107">Os scripts CSV são criados para facilitar o uso.</span><span class="sxs-lookup"><span data-stu-id="6a254-107">CSV scripts are created for ease-of-use.</span></span> <span data-ttu-id="6a254-108">A primeira linha no script identifica os atributos nas linhas a seguir.</span><span class="sxs-lookup"><span data-stu-id="6a254-108">The first line in the script identifies the attributes in the lines that follow.</span></span> <span data-ttu-id="6a254-109">As colunas são separadas por vírgulas.</span><span class="sxs-lookup"><span data-stu-id="6a254-109">Columns are separated by commas.</span></span> <span data-ttu-id="6a254-110">O formato de arquivo é compatível com o formato Microsoft Excel. csv, para que os arquivos sejam facilmente criados.</span><span class="sxs-lookup"><span data-stu-id="6a254-110">The file format is compatible with the Microsoft Excel .csv format, so that files are easily created.</span></span> <span data-ttu-id="6a254-111">Use o Excel ou qualquer outra ferramenta que possa ler e gravar arquivos. csv.</span><span class="sxs-lookup"><span data-stu-id="6a254-111">Use Excel or any other tool that can read and write .csv files.</span></span> <span data-ttu-id="6a254-112">O CSVDE dá suporte a Unicode.</span><span class="sxs-lookup"><span data-stu-id="6a254-112">CSVDE supports Unicode.</span></span>

## <a name="example-csv-file"></a><span data-ttu-id="6a254-113">Exemplo de arquivo CSV</span><span class="sxs-lookup"><span data-stu-id="6a254-113">Example CSV File</span></span>

<span data-ttu-id="6a254-114">O exemplo de código a seguir é um arquivo CSV que adiciona uma classe auxiliar.</span><span class="sxs-lookup"><span data-stu-id="6a254-114">The following code example is a CSV file that adds an auxiliary class.</span></span>

``` syntax
DN,adminDisplayName,cn,defaultHidingValue,defaultObjectCategory,description,governsID,lDAPDisplayName,mayContain,mustContain,distinguishedName,objectCategory,objectClass,objectClassCategory,possSuperiors,name,rDNAttID,schemaIDGUID,subClassOf,auxiliaryClass,defaultSecurityDescriptor
"CN=My-Test-Auxiliary-Class1,CN=Schema,CN=Configuration,DC=myorg,DC=mytest,DC=Fabrikam,DC=com",My-Test-Auxiliary-Class1,My-Test-Auxiliary-Class1,FALSE,"CN=My-Test-Auxiliary-Class1,CN=Schema,CN=Configuration,DC=myorg,DC=mytest,DC=Fabrikam,DC=com",Test class used to show how to add an auxiliary class.,1.2.840.113556.1.4.7000.159.24.10.611.11,myTestAuxiliaryClass1,myTestAttributeDNString,description;myTestAttributeUnicodeString,"CN=My-Test-Auxiliary-Class1,CN=Schema,CN=Configuration,DC=myorg,DC=mytest,DC=fabrikam,DC=com","CN=Class-Schema,CN=Schema,CN=Configuration,DC=myorg,DC=mytest,DC=fabrikam,DC=com",classSchema,3,domainDNS;container,My-Test-Auxiliary-Class1,cn,X'9a6b3176c5dbd2118bd00000f875b660',top,,
```

 

 




