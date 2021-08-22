---
description: A tabela RemoveRegistry contém as informações do Registro que o aplicativo precisa excluir do registro do sistema.
ms.assetid: 8be382f1-f5ab-4a9d-bf0e-05275310c5b5
title: RemoveRegistry Table
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 170dc727eef47ac214f7a7f42af7f487f53ad0b9a0658182420b28eb5224e38d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119314876"
---
# <a name="removeregistry-table"></a>RemoveRegistry Table

A tabela RemoveRegistry contém as informações do Registro que o aplicativo precisa excluir do registro do sistema.

A tabela RemoveRegistry tem as seguintes colunas.



| Coluna         | Tipo                         | Chave | Nullable |
|----------------|------------------------------|-----|----------|
| RemoveRegistry | [Identificador](identifier.md) | Y   | N        |
| Root           | [Inteiro](integer.md)       | N   | N        |
| Chave            | [RegPath](regpath.md)       | N   | N        |
| Name           | [Formatado](formatted.md)   | N   | Y        |
| Componente\_    | [Identificador](identifier.md) | N   | N        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="RemoveRegistry"></span><span id="removeregistry"></span><span id="REMOVEREGISTRY"></span>RemoveRegistry
</dt> <dd>

A chave para esta tabela.

</dd> <dt>

<span id="Root"></span><span id="root"></span><span id="ROOT"></span>Raiz
</dt> <dd>

A chave raiz predefinida para o valor do Registro.



| Constante                          | Hexadecimal | Decimal | Chave raiz                                                                                                                                                                                                           |
|-----------------------------------|-------------|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| (nenhum)                            | \- 0x001    | -1      | **HKEY \_ O \_ INSTALADOR DE** USUÁRIO ATUAL define essa chave ao fazer uma instalação por usuário.<br/>                                                                                                                    |
| (nenhum)                            | -0x001      | -1      | **HKEY \_ O \_ instalador DE** COMPUTADOR LOCAL define essa chave ao fazer uma instalação de todos os usuários com [**ALLUSERS**](allusers.md) definido como 1.<br/>                                                                       |
| **msidbRegistryRootClassesRoot**  | 0x000       | 0       | **HKEY \_ CLASSES \_ ROOT** O instalador remove o valor do hive classes **de \\ software \\ HKCU** durante instalações no contexto de instalação por usuário e [por computador](installation-context.md).<br/> |
| **msidbRegistryRootCurrentUser**  | 0x001       | 1       | **USUÁRIO ATUAL DO HKEY \_ \_**                                                                                                                                                                                            |
| **msidbRegistryRootLocalMachine** | 0x002       | 2       | **COMPUTADOR LOCAL HKEY \_ \_**                                                                                                                                                                                           |
| **msidbRegistryRootUsers**        | 0x003       | 3       | **USUÁRIOS \_ DO HKEY**                                                                                                                                                                                                    |



 

</dd> <dt>

<span id="Key"></span><span id="key"></span><span id="KEY"></span>Chave
</dt> <dd>

A chave localizável para o valor do Registro.

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Nome
</dt> <dd>

O nome do valor do Registro localizável.

A cadeia de caracteres a seguir na coluna Nome tem significância especial.



| String | Significado                                                                                                    |
|--------|------------------------------------------------------------------------------------------------------------|
| "-"    | A chave deve ser excluída, se presente, com todos os seus valores e subkeys, quando o componente for instalado. |



 

Observe que a [tabela do Registro](registry-table.md) deve ser usada para criar ou remover uma chave do Registro quando o componente é removido.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_
</dt> <dd>

Chave externa na primeira coluna da tabela [Componente que](component-table.md) referencia o componente que controla a exclusão do valor do Registro.

</dd> </dl>

## <a name="remarks"></a>Comentários

As informações do Registro são excluídas do registro do sistema quando o componente correspondente foi selecionado para ser instalado localmente ou executado da origem.

Essa tabela é referenciada quando a [ação RemoveRegistryValues](removeregistryvalues-action.md) é executada.

## <a name="validation"></a>Validação

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE46](ice46.md)  
[ICE69](ice69.md)  
</dl>

 

 




