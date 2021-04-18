---
description: A tabela ModuleDependency mantém uma lista de outros módulos de mesclagem que são necessários para que esse módulo de mesclagem opere corretamente.
ms.assetid: 36418331-bec7-40c9-8fdf-fe4b958a1443
title: Tabela ModuleDependency
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bb0c550f8c5ae480a07ca10401d1d3b67c496ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105758774"
---
# <a name="moduledependency-table"></a>Tabela ModuleDependency

A tabela ModuleDependency mantém uma lista de outros módulos de mesclagem que são necessários para que esse módulo de mesclagem opere corretamente. Esta tabela habilita uma ferramenta de mesclagem ou verificação para garantir que os módulos de mesclagem necessários sejam incluídos no banco de dados do instalador do usuário. A ferramenta verifica através da referência cruzada desta tabela com a tabela ModuleSignature no banco de dados do instalador.

A tabela ModuleDependency tem as colunas a seguir.



| Coluna           | Tipo                         | Chave | Nullable |
|------------------|------------------------------|-----|----------|
| ModuleID         | [Identificador](identifier.md) | S   | N        |
| ModuleLanguage   | [Inteiro](integer.md)       | S   | N        |
| Requeridoid       | [Identificador](identifier.md) | S   | N        |
| RequiredLanguage | [Inteiro](integer.md)       | S   | N        |
| RequiredVersion  | [Versão](version.md)       |     | S        |



 

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

<span id="RequiredID"></span><span id="requiredid"></span><span id="REQUIREDID"></span>Requeridoid
</dt> <dd>

Identificador do módulo de mesclagem exigido pelo módulo de mesclagem em ModuleID.

</dd> <dt>

<span id="RequiredLanguage"></span><span id="requiredlanguage"></span><span id="REQUIREDLANGUAGE"></span>RequiredLanguage
</dt> <dd>

ID de idioma numérico do módulo de mesclagem em requeridoid. A coluna RequiredLanguage pode especificar a ID de idioma para um único idioma, como 1033 para inglês americano, ou especificar a ID de idioma para um grupo de idiomas, como 9 para qualquer inglês. Se o campo contiver uma ID de idioma de grupo, qualquer módulo de mesclagem com um código de idioma nesse grupo satisfizer a dependência. Se o RequiredLanguage for definido como 0, qualquer módulo de mesclagem preenchendo os outros requisitos atenderá à dependência.

</dd> <dt>

<span id="RequiredVersion"></span><span id="requiredversion"></span><span id="REQUIREDVERSION"></span>RequiredVersion
</dt> <dd>

Versão do módulo de mesclagem em requeridoid. Se esse campo for nulo, qualquer versão preencherá a dependência.

</dd> </dl>

## <a name="validation"></a>Validação

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE25](ice25.md)  
</dl>

 

 



