---
description: A tabela ModuleExclusion mantém uma lista de outros módulos de mesclagem que são incompatíveis no mesmo banco de dados do instalador.
ms.assetid: c28d9afa-152c-43b5-9892-7a38fae8c593
title: Tabela ModuleExclusion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8fb4cc136937d5a01bd16a42c138532dd524ee1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104370761"
---
# <a name="moduleexclusion-table"></a>Tabela ModuleExclusion

A tabela ModuleExclusion mantém uma lista de outros módulos de mesclagem que são incompatíveis no mesmo banco de dados do instalador. Esta tabela permite que uma ferramenta de mesclagem ou verificação Verifique se os módulos de mesclagem conflitantes não são mesclados no banco de dados do instalador do usuário. A ferramenta verifica através da referência cruzada desta tabela com a tabela ModuleSignature no banco de dados do instalador.

A tabela ModuleExclusion tem as colunas a seguir.



| Coluna             | Tipo                         | Chave | Nullable |
|--------------------|------------------------------|-----|----------|
| ModuleID           | [Identificador](identifier.md) | S   | N        |
| ModuleLanguage     | [Inteiro](integer.md)       | S   | N        |
| Exclusão excluída         | [Identificador](identifier.md) | S   | N        |
| ExcludedLanguage   | [Inteiro](integer.md)       | S   | N        |
| ExcludedMinVersion | [Versão](version.md)       |     | S        |
| ExcludedMaxVersion | [Versão](version.md)       |     | S        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="ModuleID"></span><span id="moduleid"></span><span id="MODULEID"></span>ModuleID
</dt> <dd>

Identificador do módulo de mesclagem. Essa é uma chave estrangeira na [tabela ModuleSignature](modulesignature-table.md).

</dd> <dt>

<span id="ModuleLanguage"></span><span id="modulelanguage"></span><span id="MODULELANGUAGE"></span>ModuleLanguage
</dt> <dd>

ID de idioma decimal do módulo de mesclagem em ModuleID. Essa é uma chave estrangeira na [tabela ModuleSignature](modulesignature-table.md).

</dd> <dt>

<span id="ExcludedID"></span><span id="excludedid"></span><span id="EXCLUDEDID"></span>Exclusão excluída
</dt> <dd>

Identificador de um módulo de mesclagem excluído.

</dd> <dt>

<span id="ExcludedLanguage"></span><span id="excludedlanguage"></span><span id="EXCLUDEDLANGUAGE"></span>ExcludedLanguage
</dt> <dd>

ID de idioma numérico do módulo de mesclagem em Excluídoid. A coluna ExcludedLanguage pode especificar a ID de idioma para um único idioma, como 1033 para inglês americano, ou especificar a ID de idioma para um grupo de idiomas, como 9 para qualquer inglês. A coluna ExcludedLanguage pode aceitar IDs de idioma negativas. O significado do valor na coluna ExcludedLanguage é o seguinte.



| ExcludedLanguage | Significado                                                              |
|------------------|----------------------------------------------------------------------|
| > 0           | Exclua as IDs de idioma especificadas por ExcludedLanguage.              |
| = 0              | Não exclua nenhuma ID de idioma.                                             |
| < 0           | Exclua todas as IDs de idioma, exceto aquelas especificadas por ExcludedLanguage. |



 

</dd> <dt>

<span id="ExcludedMinVersion"></span><span id="excludedminversion"></span><span id="EXCLUDEDMINVERSION"></span>ExcludedMinVersion
</dt> <dd>

Versão mínima excluída de um intervalo. Se o campo ExcludedMinVersion for nulo, todas as versões antes de ExcludedMaxVersion serão excluídas. Se ExcludedMinVersion e ExcludedMaxVersion forem nulos, não haverá nenhuma exclusão com base na versão.

</dd> <dt>

<span id="ExcludedMaxVersion"></span><span id="excludedmaxversion"></span><span id="EXCLUDEDMAXVERSION"></span>ExcludedMaxVersion
</dt> <dd>

Versão máxima excluída de um intervalo. Se o campo ExcludedMaxVersion for nulo, todas as versões após ExcludedMinVersion serão excluídas. Se ExcludedMinVersion e ExcludedMaxVersion forem nulos, não haverá nenhuma exclusão com base na versão.

</dd> </dl>

## <a name="validation"></a>Validação

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE25](ice25.md)  
</dl>

 

 



