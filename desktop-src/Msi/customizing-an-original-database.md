---
description: Faça uma cópia do pacote de instalação Windows instalador de exemplo MNP2000.msi renomeie essa cópia MNP2000t.msi.
ms.assetid: 1251d377-7143-4a6b-81d0-0915f952be10
title: Personalização de um banco de dados original
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f02f176bb24b1792d9184ebc662a45c9dbfdb8df385b3fb481967c9c8a099a6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075036"
---
# <a name="customizing-an-original-database"></a>Personalização de um banco de dados original

Faça uma cópia do pacote de instalação Windows instalador de exemplo MNP2000.msi renomeie essa cópia MNP2000t.msi. Nas etapas a seguir, você personalizará esse arquivo usando um editor de tabela de banco de dados, como Orca, que é fornecido com o SDK ou outro editor de banco de dados.

Inclua o novo arquivo de recurso para a lista de telefone, Phone.txt, na pasta Bloco de notas com os outros arquivos de origem.



| Arquivo      | Descrição                             | Caminho para a origem                 | Caminho para o destino                               |
|-----------|-----------------------------------------|--------------------------------|----------------------------------------------|
| phone.txt | Um recurso para o recurso Telefone \_ List. | C: \\ Exemplo \\ Bloco de notas \\phone.txt | \[ProgramFilesFolder \] \\ Red Park \_ \\phone.txt |



 

Use o editor de banco de dados para adicionar um registro à [tabela](file-table.md) Arquivo MNP2000t.msi para o novo arquivo.

[File Table](file-table.md)



| Arquivo      | Componente\_ | FileName  | FileSize | Versão | Idioma | Atributos | Sequência |
|-----------|-------------|-----------|----------|---------|----------|------------|----------|
| Phone.txt | Telefone       | Phone.txt | 1000     |         |          | 0          | 1        |



 

Conforme explicado na seção: Usando transformar para adicionar recursos, a transformação deve adicionar um ou mais novos [componentes](using-transforms-to-add-resources.md)ao banco de dados de instalação para conter o novo recurso de lista de telefone. Use o editor de banco de dados para adicionar o seguinte registro à [tabela Componente](component-table.md) do MNP2000t.msi.

O Telefone componente deve ser identificado com um GUID de ID de [componente exclusivo.](guid.md) Se você estiver reproduzindo o exemplo, não reutilizar o mesmo GUID de ID de componente como na tabela a seguir. Em vez disso, use um utilitário como Guidgen.exe para gerar um novo GUID. Certifique-se de usar uma cadeia de caracteres GUID consistente com o Windows de [dados guid](guid.md) do instalador.

[Tabela de componentes](component-table.md)



| Componente | Componentid                            | Diretório\_ | Atributos | Condição | Keypath   |
|-----------|----------------------------------------|-------------|------------|-----------|-----------|
| Telefone     | {D152A1EC-9F7A-4E45-B0DC-ED6EE5D829F8} | NOTEPADDIR  | 2          |           | Phone.txt |



 

Use o editor de banco de dados para modificar os dados na [tabela Recurso](feature-table.md) do MNP2000t.msi. Insira 0 na coluna Nível do registro de recurso De porta. Isso desabilita o recurso Gate e seus recursos filho e oculta esses recursos da interface do usuário. Observe que, como a [**propriedade INSTALLLEVEL**](installlevel.md) está definida como 3 na tabela [Propriedade](property-table.md), o instalador não instala recursos com um Nível 0. Adicione um registro para o novo recurso Telefone \_ List.

[Tabela de recursos](feature-table.md)



| Recurso     | Pai do \_ recurso | Título         | Descrição                | Exibir | Nível | Diretório\_ | Atributos |
|-------------|-----------------|---------------|----------------------------|---------|-------|-------------|------------|
| Artes        |                 | Artes          | Eventos de eventos de parque no Red Park.   | 20      | 3     | NOTEPADDIR  | 0          |
| Beisebol    | Esporte           | Beisebol      | Jogos de beisebol             | 17      | 3     | SPORTDIR    | 32         |
| Concerto     | Artes            | Concerto       | Eventos de show no Red Park | 21      | 3     | KANDIR     | 2          |
| Dança       | Artes            | Dança         | Eventos de música no Red Park   | 23      | 3     | KANDIR     | 2          |
| Futebol    | Esporte           | Futebol      | Jogos de futebol             | 19      | 3     | SPORTDIR    | 2          |
| Porta        |                 | Porta          | Admissões do Red Park      | 6       | 0     | NOTEPADDIR  | 0          |
| Ajuda        | Bloco de notas         | Ajuda          | Arquivo de ajuda.                 | 5       | 3     | NOTEPADDIR  | 1          |
| Janeiro     | Porta            | Janeiro       | Admissões de janeiro         | 10      | 3     | MONDIR      | 2          |
| NewYears    | Janeiro         | Dia dos Novos Anos | Admissões de Dia dos Novos Anos   | 11      | 3     | HOLDIR      | 2          |
| Bloco de notas     |                 | Bloco de notas       | Bloco de notas Editor             | 1       | 3     | NOTEPADDIR  | 0          |
| Leiame      | Bloco de notas         | Leiame        | Arquivo Leiame                | 3       | 3     | NOTEPADDIR  | 0          |
| Esporte       |                 | Eventos de esporte  | Eventos de esporte no Red Park   | 14      | 3     | NOTEPADDIR  | 0          |
| \_Telefone Lista |                 | Telefone Lista    | Telefone Lista                 | 24      | 3     | NOTEPADDIR  | 0          |



 

Adicione o seguinte registro à [tabela FeatureComponents](featurecomponents-table.md) do MNP2000t.msi.

[Tabela FeatureComponents](featurecomponents-table.md)



| Recurso\_   | Componente\_ |
|-------------|-------------|
| \_Telefone Lista | Telefone       |



 

Adicione um novo registro na tabela [Atalho para](shortcut-table.md) criar um atalho para o recurso Telefone \_ Listagem.

[Tabela de atalho](shortcut-table.md)



| Atalho | Diretório\_ | Nome      | Componente\_ | Destino          | Argumentos | Descrição | Tecla de acesso | Ícone\_ | IconIndex | ShowCmd | WkDir |
|----------|-------------|-----------|-------------|-----------------|-----------|-------------|--------|--------|-----------|---------|-------|
| sPhone   | MENUDIR     | Phone.txt | Telefone       | \[\#Phone.txt\] |           |             |        |        |           |         |       |



 

[Continuar](generating-a-customization-transform.md)

 

 



