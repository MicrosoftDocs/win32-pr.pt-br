---
description: A tabela MsiPatchOldAssemblyFile relaciona um arquivo na tabela de arquivos com um nome de assembly na tabela MsiPatchOldAssemblyName. Vários nomes de assembly antigos podem ser associados a um único arquivo.
ms.assetid: a3c1e7fb-5f97-41db-bdc8-bd3ddb695c42
title: Tabela MsiPatchOldAssemblyFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c995e4f6d6622dd3d7d1c96c9ef1297a787b66d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105780510"
---
# <a name="msipatcholdassemblyfile-table"></a>Tabela MsiPatchOldAssemblyFile

A tabela MsiPatchOldAssemblyFile relaciona um arquivo na [tabela de arquivos](file-table.md) com um nome de assembly na [tabela MsiPatchOldAssemblyName](msipatcholdassemblyname-table.md). Vários nomes de assembly antigos podem ser associados a um único arquivo.

A tabela MsiPatchOldAssemblyFile tem as colunas a seguir.



| Coluna     | Tipo                         | Chave | Nullable |
|------------|------------------------------|-----|----------|
| Arquivo\_     | [Identificador](identifier.md) | S   | N        |
| Assembly\_ | [Identificador](identifier.md) | S   | N        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="File_"></span><span id="file_"></span><span id="FILE_"></span>Grupo\_
</dt> <dd>

Chave estrangeira para a [tabela de arquivos](file-table.md) que especifica o assembly a ser corrigido. Esta coluna faz parte da chave primária.

</dd> <dt>

<span id="Assembly_"></span><span id="assembly_"></span><span id="ASSEMBLY_"></span>)\_
</dt> <dd>

Chave estrangeira para a [tabela MsiPatchOldAssemblyName](msipatcholdassemblyname-table.md) que identifica um dos nomes de assembly antigos para o assembly. Esta coluna faz parte da chave primária.

</dd> </dl>

## <a name="remarks"></a>Comentários

Windows Installer usa a tabela MsiPatchOldAssemblyFile e a [tabela MsiPatchOldAssemblyName](msipatcholdassemblyname-table.md) ao corrigir assemblies instalados no GAC (cache de assembly global). Ao liberar uma versão mais recente de um assembly, o nome forte do assembly é alterado. Juntas, as duas tabelas identificam o nome antigo do assembly para um assembly atualizado. Isso permite que o instalador use o nome antigo do assembly para localizar o arquivo original no GAC e aplicar um patch binário. Sem essas informações, o instalador pode ter que acessar a fonte de instalação original para corrigir um assembly instalado no GAC.

A tabela MsiPatchOldAssemblyFile e a [tabela MsiPatchOldAssemblyName](msipatcholdassemblyname-table.md) não são geradas automaticamente pelo [PatchWiz](patchwiz-dll.md). O pacote de atualização especificado na [tabela UpgradedImages](upgradedimages-table-patchwiz-dll-.md) é necessário para conter essas tabelas para que o patch tenha essas informações.

## <a name="validation"></a>Validação

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
</dl>

 

 



