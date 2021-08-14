---
description: A tabela ModuleExclusion mantém uma lista de outros módulos de mesclagem incompatíveis no mesmo banco de dados do instalador.
ms.assetid: c28d9afa-152c-43b5-9892-7a38fae8c593
title: Tabela ModuleExclusion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 008d10e65d81b5668821e1a999cf08f5a10c55db3372a4b0230d560462a977c9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996436"
---
# <a name="moduleexclusion-table"></a>Tabela ModuleExclusion

A tabela ModuleExclusion mantém uma lista de outros módulos de mesclagem incompatíveis no mesmo banco de dados do instalador. Essa tabela permite que uma ferramenta de mesclagem ou verificação verifique se os módulos de mesclagem conflitantes não são mesclados no banco de dados do instalador do usuário. A ferramenta verifica fazendo referência cruzada a esta tabela com a tabela ModuleSignature no banco de dados do instalador.

A tabela ModuleExclusion tem as seguintes colunas.



| Coluna             | Tipo                         | Chave | Nullable |
|--------------------|------------------------------|-----|----------|
| ModuleID           | [Identificador](identifier.md) | Y   | N        |
| ModuleLanguage     | [Inteiro](integer.md)       | Y   | N        |
| ExcludedID         | [Identificador](identifier.md) | Y   | N        |
| ExcludedLanguage   | [Inteiro](integer.md)       | Y   | N        |
| ExcludedMinVersion | [Versão](version.md)       |     | Y        |
| ExcludedMaxVersion | [Versão](version.md)       |     | Y        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="ModuleID"></span><span id="moduleid"></span><span id="MODULEID"></span>Moduleid
</dt> <dd>

Identificador do módulo de mesclagem. Essa é uma chave estrangeira na [tabela ModuleSignature](modulesignature-table.md).

</dd> <dt>

<span id="ModuleLanguage"></span><span id="modulelanguage"></span><span id="MODULELANGUAGE"></span>ModuleLanguage
</dt> <dd>

ID da linguagem decimal do módulo de mesclagem em ModuleID. Essa é uma chave estrangeira na [tabela ModuleSignature](modulesignature-table.md).

</dd> <dt>

<span id="ExcludedID"></span><span id="excludedid"></span><span id="EXCLUDEDID"></span>ExcludedID
</dt> <dd>

Identificador de um módulo de mesclagem excluído.

</dd> <dt>

<span id="ExcludedLanguage"></span><span id="excludedlanguage"></span><span id="EXCLUDEDLANGUAGE"></span>ExcludedLanguage
</dt> <dd>

ID de idioma numérico do módulo de mesclagem em ExcludedID. A coluna ExcludedLanguage pode especificar a ID do idioma para um único idioma, como 1033 para inglês dos EUA, ou especificar a ID do idioma para um grupo de idiomas, como 9 para qualquer inglês. A coluna ExcludedLanguage pode aceitar IDs de idioma negativas. O significado do valor na coluna ExcludedLanguage é o seguinte.



| ExcludedLanguage | Significado                                                              |
|------------------|----------------------------------------------------------------------|
| > 0           | Exclua as IDs de idioma especificadas por ExcludedLanguage.              |
| = 0              | Não exclua nenhuma ID de idioma.                                             |
| < 0           | Exclua todas as IDs de idioma, exceto aquelas especificadas por ExcludedLanguage. |



 

</dd> <dt>

<span id="ExcludedMinVersion"></span><span id="excludedminversion"></span><span id="EXCLUDEDMINVERSION"></span>ExcludedMinVersion
</dt> <dd>

Versão mínima excluída de um intervalo. Se o campo ExcludedMinVersion for Null, todas as versões antes de ExcludedMaxVersion serão excluídas. Se ExcludedMinVersion e ExcludedMaxVersion são Nulos, não haverá exclusão com base na versão.

</dd> <dt>

<span id="ExcludedMaxVersion"></span><span id="excludedmaxversion"></span><span id="EXCLUDEDMAXVERSION"></span>ExcludedMaxVersion
</dt> <dd>

Versão máxima excluída de um intervalo. Se o campo ExcludedMaxVersion for Null, todas as versões após ExcludedMinVersion serão excluídas. Se ExcludedMinVersion e ExcludedMaxVersion são Nulos, não haverá exclusão com base na versão.

</dd> </dl>

## <a name="validation"></a>Validação

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE25](ice25.md)  
</dl>

 

 



