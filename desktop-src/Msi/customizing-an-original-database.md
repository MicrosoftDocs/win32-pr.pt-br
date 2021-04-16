---
description: Faça uma cópia do pacote de instalação do Windows Installer de exemplo MNP2000.msi e renomeie essa cópia MNP2000t.msi.
ms.assetid: 1251d377-7143-4a6b-81d0-0915f952be10
title: Personalizando um banco de dados original
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3222ebce146e891c7b16c70eb78f0f26b95727c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105757522"
---
# <a name="customizing-an-original-database"></a>Personalizando um banco de dados original

Faça uma cópia do pacote de instalação do Windows Installer de exemplo MNP2000.msi e renomeie essa cópia MNP2000t.msi. Nas etapas a seguir, você personalizará esse arquivo usando um editor de tabela de banco de dados, como o orca, fornecido com o SDK ou outro editor de banco de dados.

Inclua o novo arquivo de recurso para a lista de telefones, Phone.txt, na pasta do bloco de notas com os outros arquivos de origem.



| Arquivo      | Descrição                             | Caminho para a origem                 | Caminho para o destino                               |
|-----------|-----------------------------------------|--------------------------------|----------------------------------------------|
| phone.txt | Um recurso para o \_ recurso de lista telefônica. | C: \\phone.txt do bloco de notas de exemplo \\ \\ | \[\] \\phone.txt de \_ estacionamento \\ vermelho ProgramFilesFolder |



 

Use seu editor de banco de dados para adicionar um registro à [tabela de arquivos](file-table.md) de MNP2000t.msi para o novo arquivo.

[File Table](file-table.md)



| Arquivo      | Componente\_ | FileName  | FileSize | Versão | Idioma | Atributos | Sequência |
|-----------|-------------|-----------|----------|---------|----------|------------|----------|
| Phone.txt | Telefone       | Phone.txt | 1000     |         |          | 0          | 1        |



 

Conforme explicado na seção: [usando transformações para adicionar recursos](using-transforms-to-add-resources.md), a transformação deve adicionar um ou mais novos componentes ao banco de dados de instalação para conter o novo recurso de lista telefônica. Use o editor de banco de dados para adicionar o seguinte registro à [tabela de componentes](component-table.md) do MNP2000t.msi.

O componente do telefone deve ser identificado com um [GUID](guid.md)de ID de componente exclusivo. Se você estiver reproduzindo o exemplo, não reutilize o mesmo GUID de ID de componente da tabela a seguir. Em vez disso, use um utilitário como Guidgen.exe para gerar um novo GUID. Certifique-se de usar uma cadeia de caracteres GUID consistente com o tipo de dados Windows Installer [GUID](guid.md) .

[Tabela de componentes](component-table.md)



| Componente | ComponentId                            | Diretório\_ | Atributos | Condição | KeyPath   |
|-----------|----------------------------------------|-------------|------------|-----------|-----------|
| Telefone     | {D152A1EC-9F7A-4E45-B0DC-ED6EE5D829F8} | NOTEPADDIR  | 2          |           | Phone.txt |



 

Use o seu editor de banco de dados para modificar a [tabela de recursos](feature-table.md) da MNP2000t.msi. Insira 0 na coluna nível do registro de recurso portão. Isso desabilita o recurso de portão e seus recursos filho e oculta esses recursos da interface do usuário. Observe que, como a propriedade [**INSTALLLEVEL**](installlevel.md) é definida como 3 na [tabela de propriedades](property-table.md), o instalador não instala recursos com um nível de 0. Adicione um registro para o novo recurso de lista de telefones \_ .

[Tabela de recursos](feature-table.md)



| Recurso     | Pai do recurso \_ | Título         | Descrição                | Monitor | Nível | Diretório\_ | Atributos |
|-------------|-----------------|---------------|----------------------------|---------|-------|-------------|------------|
| Artes        |                 | Artes          | Eventos de artes no parque vermelho.   | 20      | 3     | NOTEPADDIR  | 0          |
| Beisebol    | Esporte           | Beisebol      | Jogos de beisebol             | 17      | 3     | SPORTDIR    | 32         |
| Concerto     | Artes            | Concerto       | Eventos de concerto em Parque vermelho | 21      | 3     | ARTSDIR     | 2          |
| Dance       | Artes            | Dance         | Eventos da dança no parque vermelho   | 23      | 3     | ARTSDIR     | 2          |
| Comemorar    | Esporte           | Comemorar      | Jogos de futebol             | 19      | 3     | SPORTDIR    | 2          |
| Check        |                 | Check          | Admissões do Parque vermelho      | 6       | 0     | NOTEPADDIR  | 0          |
| Ajuda        | Bloco de notas         | Ajuda          | Arquivo de ajuda.                 | 5       | 3     | NOTEPADDIR  | 1          |
| Janeiro     | Check            | Janeiro       | Inmissões de janeiro         | 10      | 3     | MONDIR      | 2          |
| NewYears    | Janeiro         | Ano novo | Novos dias de admissão no ano   | 11      | 3     | HOLDIR      | 2          |
| Bloco de notas     |                 | Bloco de notas       | Editor do bloco de notas             | 1       | 3     | NOTEPADDIR  | 0          |
| Leiame      | Bloco de notas         | Leiame        | Arquivo Leiame                | 3       | 3     | NOTEPADDIR  | 0          |
| Esporte       |                 | Eventos de esporte  | Eventos de esporte no parque vermelho   | 14      | 3     | NOTEPADDIR  | 0          |
| Lista de telefones \_ |                 | Lista de telefones    | Lista de telefones                 | 24      | 3     | NOTEPADDIR  | 0          |



 

Adicione o seguinte registro à [tabela FeatureComponents](featurecomponents-table.md) de MNP2000t.msi.

[Tabela FeatureComponents](featurecomponents-table.md)



| Recurso\_   | Componente\_ |
|-------------|-------------|
| Lista de telefones \_ | Telefone       |



 

Adicione um novo registro na [tabela de atalho](shortcut-table.md) para criar um atalho para o recurso de \_ lista telefônica.

[Tabela de atalho](shortcut-table.md)



| Atalho | Diretório\_ | Nome      | Componente\_ | Destino          | Argumentos | Descrição | Tecla de acesso | ícone\_ | IconIndex | ShowCmd | WkDir |
|----------|-------------|-----------|-------------|-----------------|-----------|-------------|--------|--------|-----------|---------|-------|
| aprimorar   | MENUDIR     | Phone.txt | Telefone       | \[\#Phone.txt\] |           |             |        |        |           |         |       |



 

[Continuar](generating-a-customization-transform.md)

 

 



