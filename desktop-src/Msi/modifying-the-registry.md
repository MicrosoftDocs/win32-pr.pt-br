---
description: As chaves do registro podem ser gravadas no registro do sistema depois que todos os componentes selecionados e seus arquivos relacionados tiverem sido instalados.
ms.assetid: b3b39471-85b1-4361-94fd-19d0f0ee2b78
title: Modificando o registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff6ff79ce340b0487c179cb37e44dff9f42e4be8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297354"
---
# <a name="modifying-the-registry"></a>Modificando o registro

As chaves do registro podem ser gravadas no registro do sistema depois que todos os componentes selecionados e seus arquivos relacionados tiverem sido instalados. As ações padrão relacionadas à modificação do registro devem ser sequenciadas após as ações padrão de instalação de arquivo, pois as chaves do registro não podem ser gravadas, a menos que o componente e o arquivo correspondentes tenham sido instalados com êxito.

A [ação RegisterClassInfo](registerclassinfo-action.md) acessa a [tabela de classes](class-table.md) para registrar as informações de classe com dos componentes instalados.

A [ação RegisterExtensionInfo](registerextensioninfo-action.md) consulta a [tabela de extensão](extension-table.md) e a [tabela de verbos](verb-table.md) e registra as extensões correspondentes e as informações de verbo de comando com o sistema operacional.

A [ação RegisterProgIdInfo](registerprogidinfo-action.md) gerencia o registro de informações de ProgID de OLE com o sistema operacional.

A [ação RegisterMIMEInfo](registermimeinfo-action.md) processa a [tabela MIME](mime-table.md) para registrar a associação entre um tipo de contexto MIME, a extensão de nome de arquivo e o CLSID.

A [ação WriteRegistryValues](writeregistryvalues-action.md) processa a [tabela do registro](registry-table.md) e grava as chaves para todos os componentes que foram instalados localmente ou para serem executados a partir da origem. A tabela de registro permite que as chaves sejam gravadas nas seções de **classe HKEY, \_ \_ raiz**, **HKEY \_ Current \_ User**, **HKEY \_ local \_ Machine** e **HKEY \_ Users** Registry.

A [ação RemoveRegistryValues](removeregistryvalues-action.md) remove as chaves que foram marcadas para serem excluídas na coluna Name da [tabela de registro](registry-table.md) ou na [tabela RemoveRegistry](removeregistry-table.md).

A [ação RegisterTypeLibraries](registertypelibraries-action.md) processa a [tabela Typelib](typelib-table.md) e registra as bibliotecas de tipos instaladas com o sistema.

 

 



