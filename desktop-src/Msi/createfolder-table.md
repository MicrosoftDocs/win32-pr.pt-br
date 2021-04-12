---
description: A tabela CreateFolder contém referências a pastas que precisam ser criadas explicitamente para um componente específico.
ms.assetid: b17b470b-6971-4124-8ec3-73914fdea95f
title: Tabela CreateFolder
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc286b32b48e0db9e5b991ab10af663c51538bf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170665"
---
# <a name="createfolder-table"></a>Tabela CreateFolder

A tabela CreateFolder contém referências a pastas que precisam ser criadas explicitamente para um componente específico.

A tabela CreateFolder tem as colunas a seguir.



| Coluna      | Tipo                         | Chave | Nullable |
|-------------|------------------------------|-----|----------|
| Diretório\_ | [Identificador](identifier.md) | S   | N        |
| Componente\_ | [Identificador](identifier.md) | S   | N        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="Directory_"></span><span id="directory_"></span><span id="DIRECTORY_"></span>Active\_
</dt> <dd>

Chave externa na primeira coluna da tabela de [diretórios](directory-table.md).

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_
</dt> <dd>

Chave externa na primeira coluna da tabela de [componentes](component-table.md).

</dd> </dl>

## <a name="remarks"></a>Comentários

As pastas nesta tabela são criadas quando o componente é instalado. É feita uma tentativa de remover essas pastas somente quando o componente é desinstalado ou movido para a execução da fonte. Nenhuma remoção automática será disparada se as pastas ficarem vazias. Por outro lado, as pastas criadas pelo instalador, mas não listadas nesta tabela, são removidas quando ficam vazias.

Como as pastas criadas pelo instalador são excluídas quando se tornam vazias, você deve criar uma entrada na tabela CreateFolder para instalar um componente que consiste em uma pasta vazia.

Essa tabela é referida quando a ação [Createfolders](createfolders-action.md) ou a ação [RemoveFolders](removefolders-action.md) é chamada.

Para obter informações sobre como proteger uma pasta, consulte a [tabela MsiLockPermissionsEx](msilockpermissionsex-table.md) e a [Tabela LockPermissions](lockpermissions-table.md).

## <a name="validation"></a>Validação

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE18](ice18.md)  
[ICE32](ice32.md)  
[ICE55](ice55.md)  
</dl>

 

 



