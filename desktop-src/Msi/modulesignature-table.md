---
description: A Tabela ModuleSignature é uma tabela necessária.
ms.assetid: 09802282-72ad-43f1-8cce-4cdc68b01e87
title: Tabela ModuleSignature
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92f269215fef06af5eeacc80f1356c2ad2226c20075c1d09f1e128c062438508
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118945334"
---
# <a name="modulesignature-table"></a>Tabela ModuleSignature

A Tabela ModuleSignature é uma tabela necessária. Ele contém todas as informações necessárias para identificar um módulo de mesclagem. A ferramenta de mesclagem adiciona essa tabela ao arquivo .msi se ainda não existir uma. A tabela ModuleSignature em um módulo de mesclagem tem apenas uma linha que contém ModuleID, Language e Version. No entanto, a tabela ModuleSignature em um arquivo .msi tem uma linha que contém essas informações para cada arquivo .msm que foi mesclado a ele.

As ferramentas de mesclagem e verificação verificam a tabela ModuleSignature em arquivos .msi para determinar se ela tem todos os módulos de mesclagem dependentes exigidos pelo módulo de mesclagem atual (consulte [ModuleDependency Table](moduledependency-table.md)) e se o pacote de instalação foi mesclado anteriormente com módulos de mesclagem conflitantes (consulte [ModuleExclusion Table](moduleexclusion-table.md)).

A tabela ModuleSignature tem as seguintes colunas.



| Coluna   | Tipo                         | Chave | Nullable |
|----------|------------------------------|-----|----------|
| ModuleID | [Identificador](identifier.md) | Y   | N        |
| Idioma | [Inteiro](integer.md)       | Y   | N        |
| Versão  | [Versão](version.md)       |     | N        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="ModuleID"></span><span id="moduleid"></span><span id="MODULEID"></span>Moduleid
</dt> <dd>

Um identificador que identifica exclusivamente o módulo de mesclagem. Dois módulos de mesclagem não podem ter a mesma ModuleID, a menos que o módulo de mesclagem seja totalmente compatível com versões anteriores com seu antecessor. Você pode criar um GUID para esse campo usando um utilitário como GUIDGEN. A coluna ModuleID é uma chave primária para a tabela e, portanto, ela deve seguir a convenção de nomen por nomenu em Nomeando chaves primárias em bancos de dados [de módulo de mesclagem.](naming-primary-keys-in-merge-module-databases.md) Por exemplo, se o nome acessível do módulo de mesclagem for MyLibrary e o GUID for {880DE2F0-CDD8-11D1-A849-006097ABDE17}, a entrada na coluna ModuleID se tornará MyLibrary.880DE2F0 \_ CDD8 \_ 11D1 \_ A849 \_ 006097ABDE17.

</dd> <dt>

<span id="Language"></span><span id="language"></span><span id="LANGUAGE"></span>Língua
</dt> <dd>

O Identificador de idioma especifica o idioma padrão para o módulo de mesclagem. O identificador de idioma está em formato decimal, por exemplo, o inglês dos EUA é 1033. O idioma usado pelo módulo de mesclagem pode ser alterado aplicando uma transformação ao módulo de mesclagem antes da mesclagem.

</dd> <dt>

<span id="Version"></span><span id="version"></span><span id="VERSION"></span>Versão
</dt> <dd>

O campo Versão contém uma cadeia de caracteres que descreve as versões principais e secundárias do módulo de mesclagem.

</dd> </dl>

## <a name="validation"></a>Validação

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE25](ice25.md)  
</dl>

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Módulos de mesclagem de vários idiomas](multiple-language-merge-modules.md)
</dt> </dl>

 

 



