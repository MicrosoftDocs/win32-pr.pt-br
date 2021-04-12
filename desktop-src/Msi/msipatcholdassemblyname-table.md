---
description: A tabela MsiPatchOldAssemblyName especifica o nome antigo de um assembly.
ms.assetid: e9f22ba1-6be4-4382-abe5-5cfdc68c0855
title: Tabela MsiPatchOldAssemblyName
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee301801efc1618f84794c48172aff47734b38d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297118"
---
# <a name="msipatcholdassemblyname-table"></a>Tabela MsiPatchOldAssemblyName

A tabela MsiPatchOldAssemblyName especifica o nome antigo de um assembly.

A tabela MsiPatchOldAssemblyName tem as colunas a seguir.



| Coluna   | Tipo                         | Chave | Nullable |
|----------|------------------------------|-----|----------|
| Assembly | [Identificador](identifier.md) | S   | N        |
| Nome     | [Text](text.md)             | S   | N        |
| Valor    | [Text](text.md)             | N   | N        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="Assembly"></span><span id="assembly"></span><span id="ASSEMBLY"></span>)
</dt> <dd>

Identificador exclusivo para o nome antigo do assembly. Essa chave é usada como um mapeamento entre esta e a [tabela MsiPatchOldAssemblyFile](msipatcholdassemblyfile-table.md).

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Nomes
</dt> <dd>

Nome do atributo associado ao valor especificado na coluna valor.

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valor
</dt> <dd>

Valor associado ao nome especificado na coluna nome.

</dd> </dl>

## <a name="remarks"></a>Comentários

Windows Installer usa a [tabela MsiPatchOldAssemblyFile](msipatcholdassemblyfile-table.md) e a tabela MsiPatchOldAssemblyName ao corrigir assemblies instalados no GAC (cache de assembly global). Ao liberar uma versão mais recente de um assembly, o nome forte do assembly é alterado. Juntas, as duas tabelas identificam o nome antigo do assembly para um assembly atualizado. Isso permite que o instalador use o nome antigo do assembly para localizar o arquivo original no GAC e aplicar um patch binário. Sem essas informações, o instalador pode ter que acessar a fonte de instalação original para corrigir um assembly instalado no GAC.

A [tabela MsiPatchOldAssemblyFile](msipatcholdassemblyfile-table.md) e a tabela MsiPatchOldAssemblyName não são geradas automaticamente pelo [PatchWiz](patchwiz-dll.md). O pacote de atualização especificado na [tabela UpgradedImages](upgradedimages-table-patchwiz-dll-.md) é necessário para conter essas tabelas para que o patch tenha essas informações.

## <a name="validation"></a>Validação

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
</dl>

 

 



