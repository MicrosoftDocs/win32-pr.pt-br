---
description: ICEM09 verifica se o módulo de mesclagem lida com segurança com diretórios predefinidos.
ms.assetid: 747ae5ee-adc1-4aa7-8239-2379f76bfd0f
title: ICEM09
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30542ead9a47ab5e92074227b1ae47fa6de0e643
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122887400"
---
# <a name="icem09"></a>ICEM09

ICEM09 verifica se o módulo de mesclagem lida com segurança com diretórios predefinidos. Ele faz isso verificando se nenhum componente no módulo instala um diretório em um diretório de sistema predefinido, como "ProgramFilesFolder" ou "StartMenuFolder". Em vez disso, os módulos devem usar diretórios com nomes exclusivos (criados com a convenção de nomenização do módulo de mesclagem) e usar ações personalizadas para direcionar o diretório de destino apropriado. Essa abordagem impede que os módulos conflitam com uma estrutura de diretório existente no banco de dados final. ICEM09 verifica se as ações personalizadas necessárias para que essa técnica funcione não existem (para que a ferramenta de mesclagem possa gerá-las) ou existem no formato correto (para que funcionem conforme o esperado).

A falha ao corrigir um aviso ou erro relatado pelo ICEM09 pode causar problemas para os clientes do módulo de mesclagem. As linhas da tabela de diretório com chaves primárias, como ProgramFilesFolder, geralmente existem em um banco de dados; portanto, se os componentes em seu módulo instalarem diretamente em diretórios predefinidos, como ProgramFilesFolder, as entradas de diretório no módulo poderão colidir com linhas já existentes. Essa condição exigirá que o usuário do módulo divida os arquivos de origem do módulo para corresponder ao diretório de origem existente.

## <a name="result"></a>Result

ICEM09 relata um erro ou aviso quando um componente de módulo instala um diretório em um diretório do sistema pré-definido, causando um possível conflito de nome com a estrutura de diretório existente.

## <a name="example"></a>Exemplo

ICEM09 posta os avisos a seguir para um módulo que contém as entradas de banco de dados mostradas.

``` syntax
Warning: The component 'Component1.<GUID>' installs directly into the pre-defined 
directory 'ProgramFilesFolder'. It is recommended that merge modules alias 
all such directories to unique names.
```

Renomeie o diretório do módulo de mesclagem para que ele não faça a Windows do instalador e, portanto, seja exclusivo. Em seguida, de definir uma propriedade de mesmo nome para o valor do diretório Windows Instalador. Quando a resolução de diretório ocorre, o diretório tem uma propriedade de mesmo nome, portanto, o local de instalação do diretório é o valor da propriedade . Os arquivos se movem do local de origem distinto para o mesmo local de destino. Esse processo deve remover completamente os conflitos de mesclagem.

``` syntax
Warning: The 'ModuleInstallExecuteSequence' table contains a type 51 action 
(StartMenuFolder.<GUID>) for a pre-defined directory, but this action 
does not have sequence number '1'
```

Se a ação não tiver o número de sequência 1, ela poderá não ser mesclada no banco de dados de destino no início da sequência o suficiente para funcionar com eficiência.

Para corrigir esse aviso, de definido o número da sequência como 1. Observe que a maioria das ferramentas de mesclagem atuais (mas não algumas versões mais antigas) gerará essas ações personalizadas no momento da mesclagem, portanto, nem sempre é necessário criar explicitamente as ações no módulo de mesclagem.

``` syntax
Warning: The 'CustomAction' table contains a type 51 action (MyAppDataFolderAction) 
for a pre-defined directory, but the name is not the same as the target directory. 
Many merge tools will generate duplicate actions."
```

Como a coluna CustomAction é a chave primária da tabela CustomAction, algumas ferramentas de mesclagem podem gerar ações duplicadas porque o nome da ação pré-criar é diferente.

Para corrigir esse aviso, nomeia a ação da mesma forma que o diretório de destino. Observe que a maioria das ferramentas de mesclagem atuais (mas não algumas versões mais antigas) gera essas ações personalizadas no momento da mesclagem, portanto, nem sempre é necessário criar explicitamente as ações no módulo de mesclagem.

[Tabela de diretórios](directory-table.md)



| Diretório          | Pai do \_ Diretório | Defaultdir |
|--------------------|-------------------|------------|
| Programfilesfolder | Directory1        | A          |
| StartMenuFolder    | Directory2        | B:C        |
| AppDataFolder      | Directory3        | D          |
| MyPicturesFolder   | Directory4        | E          |



 

[Tabela de componentes](component-table.md)



| Componente               | Diretório          |
|-------------------------|--------------------|
| Component1. &lt; GUID&gt; | Programfilesfolder |
| Component2. &lt; GUID&gt; | StartMenuFolder    |
| Component3. &lt; GUID&gt; | AppDataFolder      |
| Component4. &lt; GUID&gt; | MyPicturesFolder   |



 

[Tabela CustomAction](customaction-table.md)



| CustomAction                 | Type | Fonte                       | Destino              |
|------------------------------|------|------------------------------|---------------------|
| StartMenuFolder. &lt; GUID&gt; | 51   | StartMenuFolder. &lt; GUID&gt; | \[StartMenuFolder\] |
| MyAppDataFolderAction        | 51   | AppDataFolder. &lt; GUID&gt;   | \[AppDataFolder\]   |



 

[Tabela ModuleInstallExecuteSequence](moduleinstallexecutesequence-table.md)



| Ação                       | Sequência | BaseAction | Depois | Condição |
|------------------------------|----------|------------|-------|-----------|
| StartMenuFolder. &lt; GUID&gt; | 100      |            |       |           |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência ice do módulo de mesclagem](merge-module-ice-reference.md)
</dt> </dl>

 

 



