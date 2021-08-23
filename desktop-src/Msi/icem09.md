---
description: ICEM09 verifica se o módulo de mesclagem trata com segurança os diretórios predefinidos.
ms.assetid: 747ae5ee-adc1-4aa7-8239-2379f76bfd0f
title: ICEM09
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e4d2af38903d2e704d49b48f932818d8dfaeeb1e12588c007d4af05c297642c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894486"
---
# <a name="icem09"></a>ICEM09

ICEM09 verifica se o módulo de mesclagem trata com segurança os diretórios predefinidos. Ele faz isso verificando se nenhum componente no módulo instala um diretório em um diretório de sistema predefinido, como "ProgramFilesFolder" ou "StartMenuFolder". Em vez disso, os módulos devem usar diretórios com nomes exclusivos (criados com a Convenção de nomenclatura do módulo de mesclagem) e usar ações personalizadas para direcionar o diretório de destino apropriado. Essa abordagem impede que os módulos entrem em conflito com uma estrutura de diretório existente no banco de dados final. ICEM09 verifica se as ações personalizadas necessárias para que essa técnica funcione não existem (para que a ferramenta de mesclagem possa gerá-las) ou exista no formato correto (para que funcionem conforme o esperado).

Falha ao corrigir um aviso ou erro relatado pelo ICEM09 pode causar problemas para os clientes do seu módulo de mesclagem. As linhas da tabela de diretório com chaves primárias, como ProgramFilesFolder, geralmente existem em um banco de dados; Portanto, se os componentes em seu módulo forem instalados diretamente em diretórios predefinidos, como ProgramFilesFolder, as entradas de diretório no módulo poderão colidir com linhas já existentes. Essa condição exige que o usuário do seu módulo divida os arquivos de origem do seu módulo para corresponder ao diretório de origem existente.

## <a name="result"></a>Resultado

O ICEM09 relata um erro ou aviso quando um componente de módulo instala um diretório em um diretório de sistema predefinido, causando um conflito de nome possível com a estrutura de diretório existente.

## <a name="example"></a>Exemplo

ICEM09 posta os seguintes avisos para um módulo que contém as entradas de banco de dados mostradas.

``` syntax
Warning: The component 'Component1.<GUID>' installs directly into the pre-defined 
directory 'ProgramFilesFolder'. It is recommended that merge modules alias 
all such directories to unique names.
```

renomeie o diretório do módulo de mesclagem para que ele não corresponda a uma propriedade Windows Installer e, portanto, seja exclusivo. em seguida, defina uma propriedade com o mesmo nome para o valor do diretório Windows Installer. Quando ocorre a resolução de diretório, o diretório tem uma propriedade de mesmo nome, portanto, o local de instalação do diretório é o valor da propriedade. Os arquivos são movidos do local de origem distinto para o mesmo local de destino. Esse processo deve remover completamente os conflitos de mesclagem.

``` syntax
Warning: The 'ModuleInstallExecuteSequence' table contains a type 51 action 
(StartMenuFolder.<GUID>) for a pre-defined directory, but this action 
does not have sequence number '1'
```

Se a ação não tiver o número de sequência 1, ela não poderá ser mesclada ao banco de dados de destino desde o início suficiente na sequência para funcionar com eficiência.

Para corrigir esse aviso, defina o número de sequência como 1. Observe que a maioria das ferramentas de mesclagem atuais (mas não algumas versões mais antigas) gerará essas ações personalizadas no momento da mesclagem, de modo que nem sempre é necessário criar explicitamente as ações no módulo de mesclagem.

``` syntax
Warning: The 'CustomAction' table contains a type 51 action (MyAppDataFolderAction) 
for a pre-defined directory, but the name is not the same as the target directory. 
Many merge tools will generate duplicate actions."
```

Como a coluna CustomAction é a chave primária da tabela CustomAction, algumas ferramentas de mesclagem podem gerar ações duplicadas porque o nome da ação previamente criada é diferente.

Para corrigir esse aviso, nomeie a ação da mesma forma que o diretório de destino. Observe que a maioria das ferramentas de mesclagem atuais (mas não algumas versões mais antigas) gera essas ações personalizadas no momento da mesclagem, de modo que nem sempre é necessário criar explicitamente as ações no módulo de mesclagem.

[Tabela de diretórios](directory-table.md)



| Diretório          | Pai do diretório \_ | DefaultDir |
|--------------------|-------------------|------------|
| ProgramFilesFolder | Directory1        | Um          |
| StartMenuFolder    | Directory2        | B:C        |
| AppDataFolder      | Directory3        | D          |
| MyPicturesFolder   | Directory4        | E          |



 

[Tabela de componentes](component-table.md)



| Componente               | Diretório          |
|-------------------------|--------------------|
| Component1.<GUID> | ProgramFilesFolder |
| Component2.<GUID> | StartMenuFolder    |
| Component3.<GUID> | AppDataFolder      |
| Component4.<GUID> | MyPicturesFolder   |



 

[Tabela CustomAction](customaction-table.md)



| CustomAction                 | Tipo | Fonte                       | Destino              |
|------------------------------|------|------------------------------|---------------------|
| StartMenuFolder.<GUID> | 51   | StartMenuFolder.<GUID> | \[StartMenuFolder\] |
| MyAppDataFolderAction        | 51   | AppDataFolder.<GUID>   | \[AppDataFolder\]   |



 

[Tabela ModuleInstallExecuteSequence](moduleinstallexecutesequence-table.md)



| Ação                       | Sequência | Baseaction | Depois | Condição |
|------------------------------|----------|------------|-------|-----------|
| StartMenuFolder.<GUID> | 100      |            |       |           |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ICE do módulo de mesclagem](merge-module-ice-reference.md)
</dt> </dl>

 

 



