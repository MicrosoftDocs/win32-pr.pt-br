---
description: A tabela RemoveRegistry contém as informações de registro que o aplicativo precisa excluir do registro do sistema.
ms.assetid: 8be382f1-f5ab-4a9d-bf0e-05275310c5b5
title: Tabela RemoveRegistry
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8de39edd15484ac4bcda675ec8bffaca0540a0ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103921965"
---
# <a name="removeregistry-table"></a>Tabela RemoveRegistry

A tabela RemoveRegistry contém as informações de registro que o aplicativo precisa excluir do registro do sistema.

A tabela RemoveRegistry tem as colunas a seguir.



| Coluna         | Tipo                         | Chave | Nullable |
|----------------|------------------------------|-----|----------|
| RemoveRegistry | [Identificador](identifier.md) | S   | N        |
| Root           | [Inteiro](integer.md)       | N   | N        |
| Chave            | [RegPath](regpath.md)       | N   | N        |
| Nome           | [Binário](formatted.md)   | N   | S        |
| Componente\_    | [Identificador](identifier.md) | N   | N        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="RemoveRegistry"></span><span id="removeregistry"></span><span id="REMOVEREGISTRY"></span>RemoveRegistry
</dt> <dd>

A chave para esta tabela.

</dd> <dt>

<span id="Root"></span><span id="root"></span><span id="ROOT"></span>Básica
</dt> <dd>

A chave raiz predefinida para o valor do registro.



| Constante                          | Hexadecimal | Decimal | Chave raiz                                                                                                                                                                                                           |
|-----------------------------------|-------------|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| (nenhum)                            | \- 0x001    | -1      | **HKEY \_ O instalador do \_ usuário atual** define essa chave enquanto faz uma instalação por usuário.<br/>                                                                                                                    |
| (nenhum)                            | -0x001      | -1      | **HKEY \_ O instalador do \_ computador local** define essa chave enquanto faz uma instalação de todos os usuários com [**AllUsers**](allusers.md) definido como 1.<br/>                                                                       |
| **msidbRegistryRootClassesRoot**  | 0x000       | 0       | **HKEY \_ \_Raiz de classes** o instalador remove o valor do hive de **\\ \\ classes de software HKCU** durante instalações no [contexto de instalação](installation-context.md)por usuário e por máquina.<br/> |
| **msidbRegistryRootCurrentUser**  | 0x001       | 1       | **HKEY \_ Current \_ User**                                                                                                                                                                                            |
| **msidbRegistryRootLocalMachine** | 0x002       | 2       | **\_máquina local \_ HKEY**                                                                                                                                                                                           |
| **msidbRegistryRootUsers**        | 0x003       | 3       | **usuários de HKEY \_**                                                                                                                                                                                                    |



 

</dd> <dt>

<span id="Key"></span><span id="key"></span><span id="KEY"></span>Chaves
</dt> <dd>

A chave localizável para o valor do registro.

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Nomes
</dt> <dd>

O nome do valor do registro localizável.

A cadeia de caracteres a seguir na coluna Name tem um significado especial.



| String | Significado                                                                                                    |
|--------|------------------------------------------------------------------------------------------------------------|
| "-"    | A chave deve ser excluída, se presente, com todos os seus valores e subchaves, quando o componente é instalado. |



 

Observe que a [tabela de registro](registry-table.md) deve ser usada para criar ou remover uma chave do registro quando o componente é removido.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_
</dt> <dd>

Chave externa na primeira coluna da tabela de [componentes](component-table.md) que faz referência ao componente que controla a exclusão do valor do registro.

</dd> </dl>

## <a name="remarks"></a>Comentários

As informações do registro são excluídas do registro do sistema quando o componente correspondente foi selecionado para ser instalado localmente ou executado da origem.

Essa tabela é referida quando a [ação RemoveRegistryValues](removeregistryvalues-action.md) é executada.

## <a name="validation"></a>Validação

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE46](ice46.md)  
[ICE69](ice69.md)  
</dl>

 

 




