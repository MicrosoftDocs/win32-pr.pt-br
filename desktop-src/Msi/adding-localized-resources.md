---
description: Dependendo do aplicativo, a localização pode exigir a modificação ou a adição de recursos, como arquivos ou chaves do Registro.
ms.assetid: f5af0ecd-cb57-4858-88b4-4608893004f6
title: Adicionando recursos localizados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de37bfd3c216018f6c4a6f6866206020576153e55383a9d6b36e67533bbb3b6f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829236"
---
# <a name="adding-localized-resources"></a>Adicionando recursos localizados

Dependendo do aplicativo, a localização pode exigir a modificação ou a adição de recursos, como arquivos ou chaves do Registro. A localização do aplicativo de exemplo MNP2000 requer a adição de um arquivo adicional ao pacote, ao Fre.txt e às versões em francês de dois arquivos existentes: Help.txt e Readme.txt.

A melhor prática nesse caso é localizar o pacote de modo que as versões em inglês e francês possam coexistir com segurança no computador. Isso inclui nunca instalar dois arquivos diferentes com nomes de arquivo idênticos no mesmo diretório. Como Help.txt e Readme.txt têm nomes de arquivo idênticos nas duas versões de idioma, o pacote francês deve instalar esses arquivos em um diretório diferente do inglês.

O pacote francês instala Help.txt em um novo subdiretório da pasta RedPark, francês. Como a adição de Fre.txt adiciona um recurso ao componente de Ajuda original, o código do componente da Ajuda deve ser diferente nos pacotes em francês e inglês. Consulte as regras para códigos de componente em [Alterando o código do componente.](changing-the-component-code.md)

O pacote francês instala Readme.txt no diretório francês para que esse nome de arquivo não entre em conflito com a versão em inglês. O arquivo Readme.txt é instalado com o componente Bloco de notas, mas as regras de componente não exigem a alteração do código do componente. Neste exemplo, o código do componente Bloco de notas não deve ser alteração porque RedPark.exe, os valores do Registro especificados na tabela do Registro [,](registry-table.md)são compartilhados por ambas as versões de idioma. Consulte [Adicionando informações do Registro](adding-registry-information.md).

Remova as versões em inglês Help.txt e Readme.txt dos arquivos de origem e adicione as novas versões em francês do Help.txt, Readme.txt e Fre.txt. O pacote localizado deve mapear a instalação de arquivos da origem para o destino da seguinte forma.



| Arquivo        | Descrição                  | Caminho para a origem                   | Caminho para o destino                                         |
|-------------|------------------------------|----------------------------------|--------------------------------------------------------|
| Redpark.exe | Arquivo executável do editor de texto. | C: \\ Exemplo \\ Bloco de notas \\Redpark.exe | \[ProgramFilesFolder \] \\ Red Park Em \_ francês \\ \\Redpark.exe |
| Readme.txt  | Um arquivo informacional.       | C: \\ Exemplo \\ Bloco de notas \\Readme.txt  | \[ProgramFilesFolder \] \\ Red Park Em \_ francês \\ \\Readme.txt  |
| Help.txt    | Manual de ajuda                  | C: \\ Exemplo \\ Bloco de notas \\Help.txt    | \[ProgramFilesFolder \] \\ Red Park Em \_ francês \\ \\Help.txt    |
| Fre.txt     | Lista de telefones                   | C: \\ Exemplo \\ Bloco de notas \\Fre.txt     | \[ProgramFilesFolder \] \\ Red Park Em \_ francês \\ \\Fre.txt     |



 

Use o editor de banco de dados Orca fornecido com o SDK ou outro editor para abrir a tabela Diretório e adicionar um registro para a instalação do novo diretório, francês.

[Tabela de diretórios](directory-table.md)



| Diretório                                        | Pai do \_ Diretório                                | Defaultdir        |
|--------------------------------------------------|--------------------------------------------------|-------------------|
| [**Targetdir**](targetdir.md)                   |                                                  | SourceDir         |
| [**Programfilesfolder**](programfilesfolder.md) | [**Targetdir**](targetdir.md)                   | .                 |
| KANDIR                                          | NOTEPADDIR                                       | Feiras:Eventos       |
| HOLDIR                                           | MONDIR                                           | .:Holidays        |
| MENUDIR                                          | NOTEPADDIR                                       | Menu              |
| MONDIR                                           | NOTEPADDIR                                       | Porta              |
| NOTEPADDIR                                       | [**Programfilesfolder**](programfilesfolder.md) | Red \_ Park:Bloco de notas |
| SPORTDIR                                         | NOTEPADDIR                                       | Sports:Events     |
| FRENCHDIR                                        | NOTEPADDIR                                       | Francês:.          |



 

Use o editor de tabela para alterar o ComponentId do componente ajuda no MNPFren.msi para um novo GUID.

[Tabela de componentes](component-table.md)



| Componente | Componentid                            | Diretório\_ | Atributos | Condição | Keypath      |
|-----------|----------------------------------------|-------------|------------|-----------|--------------|
| Beisebol  | {F54ABAC0-33F2-11D3-91D7-00C04FD70856} | SPORTDIR    | 2          |           | Baseball.txt |
| Concerto   | {76FA7A80-33F6-11D3-91D8-00C04FD70856} | KANDIR     | 2          |           | Concert.txt  |
| Dança     | {CCF834A1-33F8-11D3-91D8-00C04FD70856} | KANDIR     | 2          |           | Dance.txt    |
| Futebol  | {CCF834A0-33F8-11D3-91D8-00C04FD70856} | SPORTDIR    | 2          |           | Football.txt |
| Ajuda      | {9ED21229-FE3C-4FE9-B01D-57E00224FD0B} | NOTEPADDIR  | 2          |           | Help.txt     |
| Janeiro   | {CF0BC690-33C9-11D3-91D6-00C04FD70856} | MONDIR      | 2          |           | January.txt  |
| NewYears  | {A42D9140-33D8-11D3-91D6-00C04FD70856} | HOLDIR      | 2          |           | NewYears.txt |
| Bloco de notas   | {19BED232-30AB-11D3-91D3-00C04FD70856} | FRENCHDIR   | 2          |           | Redpark.exe  |



 

Use o editor de tabela para adicionar Fre.txt à [tabela de arquivos](file-table.md) de MNPFren.msi. Insira o LANGid para francês no campo idioma para os arquivos localizados. Todas as outras coisas são iguais, se o arquivo que está sendo instalado tiver um idioma diferente do arquivo no computador, o instalador favorecerá o arquivo com o idioma que corresponde ao produto que está sendo instalado. Os arquivos neutros de idioma são tratados como apenas outra linguagem, de modo que o produto que está sendo instalado é favorecedo novamente. Para obter mais informações, consulte [regras de controle de versão de arquivo](file-versioning-rules.md).

[File Table](file-table.md)



| Arquivo         | Componente\_ | FileName     | FileSize | Versão | Idioma | Atributos | Sequência |
|--------------|-------------|--------------|----------|---------|----------|------------|----------|
| Baseball.txt | Beisebol    | Baseball.txt | 1000     |         |          | 0          | 1        |
| Concert.txt  | Concerto     | Concert.txt  | 1000     |         |          | 0          | 1        |
| Dance.txt    | Dance       | Dance.txt    | 1000     |         |          | 0          | 1        |
| Football.txt | Comemorar    | Football.txt | 1000     |         |          | 0          | 1        |
| Help.txt     | Ajuda        | Help.txt     | 1000     |         | 1036     | 0          | 1        |
| January.txt  | Janeiro     | January.txt  | 1000     |         |          | 0          | 1        |
| NewYears.txt | NewYears    | NewYears.txt | 1000     |         |          | 0          | 1        |
| Redpark.exe  | Bloco de notas     | Redpark.exe  | 45328    |         |          | 0          | 1        |
| Readme.txt   | Bloco de notas     | Readme.txt   | 1000     |         | 1036     | 0          | 1        |
| Fre.txt      | Ajuda        | Fre.txt      | 1000     |         | 1036     | 0          | 1        |



 

Isso conclui a localização de exemplo.

 

 



