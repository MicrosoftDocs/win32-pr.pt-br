---
description: A tabela ModuleSignature é uma tabela necessária.
ms.assetid: 09802282-72ad-43f1-8cce-4cdc68b01e87
title: Tabela ModuleSignature
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d75e3bb013472c49d18fa44b840ce07b11728faf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104505924"
---
# <a name="modulesignature-table"></a>Tabela ModuleSignature

A tabela ModuleSignature é uma tabela necessária. Ele contém todas as informações necessárias para identificar um módulo de mesclagem. A ferramenta de mesclagem adicionará essa tabela ao arquivo. msi se ainda não existir uma. A tabela ModuleSignature em um módulo de mesclagem tem apenas uma linha que contém ModuleID, idioma e versão. No entanto, a tabela ModuleSignature em um arquivo. msi tem uma linha que contém essas informações para cada arquivo. msm que foi mesclado nela.

Ferramentas de mesclagem e verificação Verifique a tabela ModuleSignature em arquivos. msi para determinar se ele tem todos os módulos de mesclagem dependentes exigidos pelo módulo de mesclagem atual (consulte a [tabela ModuleDependency](moduledependency-table.md)) e se o pacote de instalação foi mesclado anteriormente com quaisquer módulos de mesclagem conflitantes (consulte a [tabela ModuleExclusion](moduleexclusion-table.md)).

A tabela ModuleSignature tem as colunas a seguir.



| Coluna   | Tipo                         | Chave | Nullable |
|----------|------------------------------|-----|----------|
| ModuleID | [Identificador](identifier.md) | S   | N        |
| Idioma | [Inteiro](integer.md)       | S   | N        |
| Versão  | [Versão](version.md)       |     | N        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="ModuleID"></span><span id="moduleid"></span><span id="MODULEID"></span>ModuleID
</dt> <dd>

Um identificador que identifica exclusivamente o módulo de mesclagem. Dois módulos de mesclagem não podem ter a mesma ModuleID, a menos que o módulo de mesclagem seja totalmente compatível com o seu antecessor. Você pode criar um GUID para esse campo usando um utilitário como o GUIDGEN. A coluna ModuleID é uma chave primária para a tabela e, portanto, deve seguir a Convenção de nomenclatura na [nomenclatura de chaves primárias em bancos de dados do módulo de mesclagem](naming-primary-keys-in-merge-module-databases.md). Por exemplo, se o nome legível do módulo de mesclagem for MyLibrary e o GUID for {880DE2F0-CDD8-11D1-A849-006097ABDE17}, a entrada na coluna ModuleID se tornará MyLibrary. 880DE2F0 \_ CDD8 \_ 11D1 \_ A849 \_ 006097ABDE17.

</dd> <dt>

<span id="Language"></span><span id="language"></span><span id="LANGUAGE"></span>Idioma
</dt> <dd>

O identificador de idioma especifica o idioma padrão para o módulo de mesclagem. O identificador de idioma está em formato decimal, por exemplo, o inglês dos EUA é 1033. O idioma usado pelo módulo de mesclagem pode ser alterado com a aplicação de uma transformação ao módulo de mesclagem antes da mesclagem.

</dd> <dt>

<span id="Version"></span><span id="version"></span><span id="VERSION"></span>Versão
</dt> <dd>

O campo versão contém uma cadeia de caracteres que descreve as versões principal e secundária do módulo de mesclagem.

</dd> </dl>

## <a name="validation"></a>Validação

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE25](ice25.md)  
</dl>

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Vários módulos de mesclagem de idioma](multiple-language-merge-modules.md)
</dt> </dl>

 

 



