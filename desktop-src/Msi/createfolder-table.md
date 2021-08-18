---
description: A tabela CreateFolder contém referências a pastas que precisam ser criadas explicitamente para um componente específico.
ms.assetid: b17b470b-6971-4124-8ec3-73914fdea95f
title: Tabela CreateFolder
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c4cb926f6df388241a9c779328346a6e1bfb9fba4b365afce778c6e0b7a2548
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120045086"
---
# <a name="createfolder-table"></a>Tabela CreateFolder

A tabela CreateFolder contém referências a pastas que precisam ser criadas explicitamente para um componente específico.

A tabela CreateFolder tem as seguintes colunas.



| Coluna      | Tipo                         | Chave | Nullable |
|-------------|------------------------------|-----|----------|
| Diretório\_ | [Identificador](identifier.md) | Y   | N        |
| Componente\_ | [Identificador](identifier.md) | Y   | N        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="Directory_"></span><span id="directory_"></span><span id="DIRECTORY_"></span>Diretório\_
</dt> <dd>

Chave externa na primeira coluna da [tabela Diretório](directory-table.md).

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_
</dt> <dd>

Chave externa na primeira coluna da [tabela Componente](component-table.md).

</dd> </dl>

## <a name="remarks"></a>Comentários

As pastas nesta tabela são criadas quando o componente é instalado. É feita uma tentativa de remover essas pastas somente quando o componente é desinstalado ou movido para o run-from-source. Nenhuma remoção automática será disparada se as pastas se tornarem vazias. Por outro lado, as pastas criadas pelo instalador, mas não listadas nesta tabela, são removidas quando ficam vazias.

Como as pastas criadas pelo instalador são excluídas quando ficam vazias, você deve criar uma entrada na tabela CreateFolder para instalar um componente que consiste em uma pasta vazia.

Essa tabela é referenciada quando a [ação CreateFolders](createfolders-action.md) ou [a ação RemoveFolders](removefolders-action.md) é chamada.

Para obter informações sobre como proteger uma pasta, consulte Tabela [MsiLockPermissionsEx](msilockpermissionsex-table.md) e [Tabela LockPermissions](lockpermissions-table.md).

## <a name="validation"></a>Validação

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE18](ice18.md)  
[ICE32](ice32.md)  
[ICE55](ice55.md)  
</dl>

 

 



