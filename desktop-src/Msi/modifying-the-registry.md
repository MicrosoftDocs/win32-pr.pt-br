---
description: As chaves do Registro podem ser escritas no registro do sistema depois que todos os componentes selecionados e seus arquivos relacionados forem instalados.
ms.assetid: b3b39471-85b1-4361-94fd-19d0f0ee2b78
title: Modificando o Registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06f1bd6145811097fcaf74f0622ac35412891d6aa0007c4411099ade6afddd36
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082856"
---
# <a name="modifying-the-registry"></a>Modificando o Registro

As chaves do Registro podem ser escritas no registro do sistema depois que todos os componentes selecionados e seus arquivos relacionados forem instalados. As ações padrão relacionadas à modificação do registro devem ser sequenciadas após as ações padrão de instalação do arquivo porque as chaves do Registro não podem ser escritas, a menos que o componente e o arquivo correspondentes tenham sido instalados com êxito.

A [ação RegisterClassInfo](registerclassinfo-action.md) acessa a tabela [Classe](class-table.md) para registrar as informações de classe COM dos componentes instalados.

A [ação RegisterExtensionInfo](registerextensioninfo-action.md) [](extension-table.md) consulta a tabela Extension e a tabela [Verb](verb-table.md) e registra as extensões correspondentes e as informações de verbo-comando com o sistema operacional.

A [ação RegisterProgIdInfo](registerprogidinfo-action.md) gerencia o registro de informações do OLE ProgId com o sistema operacional.

A [ação RegisterMIMEInfo](registermimeinfo-action.md) processa a [tabela MIME](mime-table.md) para registrar a associação entre um tipo de contexto MIME, a extensão de nome de arquivo e o CLSID.

A [ação WriteRegistryValues](writeregistryvalues-action.md) processa a tabela do Registro e grava as chaves para todos os componentes que foram instalados localmente ou para executar da origem. [](registry-table.md) A tabela Registro permite que as chaves sejam escritas nos hives de registro **HKEY \_ CLASSES \_ ROOT,** **HKEY \_ CURRENT \_ USER,** **HKEY LOCAL \_ \_ MACHINE** e **HKEY \_ USERS.**

A [ação RemoveRegistryValues](removeregistryvalues-action.md) remove as chaves que foram marcadas para [](registry-table.md) serem excluídas na coluna Nome da tabela Registro ou [removeRegistry Table](removeregistry-table.md).

A [ação RegisterTypeLibraries](registertypelibraries-action.md) processa a [tabela TypeLib](typelib-table.md) e registra as bibliotecas de tipo instaladas no sistema.

 

 



