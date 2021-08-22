---
title: Enumerando recursos
description: Este tópico discute as funções usadas para obter listas de recursos.
ms.assetid: 388deaa1-3b04-43fa-aad2-8b52376d570c
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: 6d3fbe60e3013fbeabdb21d74999040b51c42be2a1bb4521cda28a976bfe7aa5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119034334"
---
# <a name="enumerating-resources"></a>Enumerando recursos

Em determinadas situações, talvez você queira descobrir o conteúdo do recurso de um módulo PE (executável portátil) desconhecido. O Windows SDK fornece funções de enumeração de recursos que permitem que seu aplicativo obtenha listas de tipos de recursos, nomes e idiomas em um módulo especificado.

* As [**funções EnumResourceTypeW**](/windows/win32/api/Winbase/nf-winbase-enumresourcetypesw) [**e EnumResourceTypesExW**](/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcetypesexw) fornecem uma lista de tipos de recursos encontrados no módulo.
* As [**funções EnumResourceNamesW**](/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcenamesw) [**e EnumResourceNamesExW**](/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcenamesexw) fornecem o nome de cada recurso dentro de um determinado tipo.
* As [**funções EnumResourceLanguagesW**](/windows/win32/api/Winbase/nf-winbase-enumresourcelanguagesw) [**e EnumResourceLanguagesExW**](/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcelanguagesexw) fornecem o idioma de cada recurso de um determinado nome e tipo. 

Essas funções e suas funções de retorno de chamada associadas permitem que seu aplicativo crie uma lista de todos os recursos em um módulo. Esse processo é descrito em [Criando uma lista de recursos](using-resources.md).

## <a name="-see-also"></a>-see-also

[Msistuff.exe aplicativo de exemplo](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/sysmgmt/msi/msistuff)
