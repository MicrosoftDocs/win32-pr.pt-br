---
description: O arquivo de recurso Concert do produto original, MNP2000, contém um erro no arquivo Concert.txt.
ms.assetid: 4289bd0c-bdf3-4747-9287-94f737ce4f5c
title: Planejando um pequeno patch de atualização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0aed6c947ee278e7c4856281790a9c392af38734c475e3d40561d72d805f6011
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119519536"
---
# <a name="planning-a-small-update-patch"></a>Planejando um pequeno patch de atualização

O arquivo de recurso Concert do produto original, MNP2000, contém um erro no arquivo Concert.txt. Como Windows instalador foi usado para a instalação e a instalação do aplicativo, correções secundárias para o aplicativo podem ser tratadas instalando um pequeno pacote de patch de atualização. Uma [pequena atualização faz](small-updates.md) alterações em um ou mais arquivos de aplicativo muito pequenos para alterar o código do produto. O exemplo a seguir mostra como criar um pacote de patch do Windows Installer que pode aplicar a pequena atualização e fornecer uma correção rápida ao produto MNP2000.

Para criar a pequena atualização, primeiro obtenha uma imagem totalmente descompactada do produto MNP2000 que inclui o erro no Concert.txt. A imagem deve incluir MNP2000.msi e todos os arquivos de origem descritos em [Planejando a instalação](planning-the-installation.md)do . Na discussão a seguir, isso é chamado de Imagem de destino. A imagem de destino deve ser totalmente descompactada porque o processo de criação de patch não pode gerar patches binários para arquivos compactados em gabinetes. Coloque o .msi arquivo e todos os arquivos de origem da imagem de destino em uma pasta chamada Destino.

Em seguida, obtenha uma imagem totalmente descompactada do produto MNP2000 com um arquivo Concert.txt que é corrigido. Isso é chamado de Imagem atualizada na discussão a seguir. Use uma ferramenta de edição de banco de dados de instalação, como Orca, para atualizar o .msi arquivo. Por exemplo, se o tamanho do arquivo Concert.txt for menor que o original, insira o novo tamanho no campo FileSize da tabela Arquivo da imagem atualizada. Observe que, como o pacote foi alterado, você deve atribuir um novo código de pacote na propriedade [**Resumo do Número de**](revision-number-summary.md) Revisão. Coloque o .msi arquivo e todos os arquivos de origem da imagem Atualizada em uma pasta chamada Atualizado.

Para os fins deste exemplo, suponha que o tamanho do arquivo Concert.txt alterações. Isso significa que os campos FileSize nas tabelas Arquivo do banco de dados de Destino e Atualizado contêm dados diferentes.

A Tabela [de Arquivos a](file-table.md) seguir identifica o registro da Imagem de Destino.



| Arquivo        | Componente\_ | FileName    | FileSize | Versão | Idioma | Atributos | Sequência |
|-------------|-------------|-------------|----------|---------|----------|------------|----------|
| Concert.txt | Concerto     | Concert.txt | 1000     |         |          | 0          | 1        |



 

A tabela de arquivos a seguir identifica o registro da Imagem Atualizada.



| Arquivo        | Componente\_ | FileName    | FileSize | Versão | Idioma | Atributos | Sequência |
|-------------|-------------|-------------|----------|---------|----------|------------|----------|
| Concert.txt | Concerto     | Concert.txt | 900      |         |          | 0          | 1        |



 

> [!Note]
> O arquivo deve ter a mesma chave nas [Tabelas](file-table.md) de Arquivos da imagem de destino e da imagem atualizada. Os valores de cadeia de caracteres na coluna Arquivo de ambas as tabelas devem ser idênticos. Maiúsculas e minúsculas também devem ser idênticas.
> 
> Siga as diretrizes descritas em [Criando um pacote de patch.](creating-a-patch-package.md) Não autor de um pacote com chaves de [](msimsp-exe.md) Tabela de Arquivos [](patchwiz-dll.md) que diferem apenas por caso, porqueMsimsp.exeePatchwiz.dllchamada Makecab.exe, que não diferencia maiúsculas de minúsculas e a geração de patch falha. [](file-table.md)

[Continuar](creating-a-patch-creation-properties-file.md)

 

 



