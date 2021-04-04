---
description: O arquivo de recurso de concerto do produto original, MNP2000, contém um erro no arquivo Concert.txt.
ms.assetid: 4289bd0c-bdf3-4747-9287-94f737ce4f5c
title: Planejando um patch de atualização pequena
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f15f3667c6a18ab7a71e86997091bd76d4b15577
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "103837696"
---
# <a name="planning-a-small-update-patch"></a>Planejando um patch de atualização pequena

O arquivo de recurso de concerto do produto original, MNP2000, contém um erro no arquivo Concert.txt. Como Windows Installer foi usado para a instalação e a configuração do aplicativo, as correções secundárias para o aplicativo podem ser tratadas pela instalação de um pacote de patch de atualização pequeno. Uma [pequena atualização](small-updates.md) faz alterações em um ou mais arquivos de aplicativo que são muito menores para alterar o código do produto. O exemplo a seguir mostra como criar um pacote de patches Windows Installer que pode aplicar a pequena atualização e fornecer uma correção rápida para o produto MNP2000.

Para criar a atualização pequena, primeiro obtenha uma imagem totalmente descompactada do produto MNP2000 que inclui o erro em Concert.txt. A imagem deve incluir MNP2000.msi e todos os arquivos de origem descritos em [planejando a instalação](planning-the-installation.md). Na discussão a seguir, isso é chamado de imagem de destino. A imagem de destino deve ser totalmente descompactada porque o processo de criação de patches não pode gerar patches binários para arquivos compactados em gabinetes. Coloque o arquivo. msi e todos os arquivos de origem da imagem de destino em uma pasta chamada Target.

Em seguida, obtenha uma imagem totalmente descompactada do produto MNP2000 com um arquivo Concert.txt corrigido. Isso é chamado de imagem atualizada na discussão a seguir. Use uma ferramenta de edição de banco de dados de instalação, como orca, para atualizar o arquivo. msi. Por exemplo, se o tamanho da Concert.txt corrigida for menor do que o original, certifique-se de inserir o novo tamanho no campo FileSize da tabela de arquivos da imagem atualizada. Observe que, como o pacote foi alterado, você deve atribuir um novo código de pacote na propriedade [**Resumo do número de revisão**](revision-number-summary.md) . Coloque o arquivo. msi e todos os arquivos de origem da imagem atualizada em uma pasta chamada atualizado.

Para os fins deste exemplo, suponha que o tamanho do arquivo de Concert.txt seja alterado. Isso significa que os campos de FileSize nas tabelas de arquivos do destino e do banco de dados atualizado contêm diferentes.

A [tabela de arquivos](file-table.md) a seguir identifica o registro da imagem de destino.



| Arquivo        | Componente\_ | FileName    | FileSize | Versão | Idioma | Atributos | Sequência |
|-------------|-------------|-------------|----------|---------|----------|------------|----------|
| Concert.txt | Concerto     | Concert.txt | 1000     |         |          | 0          | 1        |



 

A tabela de arquivos a seguir identifica o registro da imagem atualizada.



| Arquivo        | Componente\_ | FileName    | FileSize | Versão | Idioma | Atributos | Sequência |
|-------------|-------------|-------------|----------|---------|----------|------------|----------|
| Concert.txt | Concerto     | Concert.txt | 900      |         |          | 0          | 1        |



 

> [!Note]
> O arquivo deve ter a mesma chave nas [tabelas de arquivos](file-table.md) da imagem de destino e da imagem atualizada. Os valores de cadeia de caracteres na coluna arquivo de ambas as tabelas devem ser idênticos. Letras maiúsculas e minúsculas também devem ser idênticas.
> 
> Siga as diretrizes descritas em [criando um pacote de patch](creating-a-patch-package.md). Não crie um pacote com chaves de [tabela de arquivos](file-table.md) que diferem somente por maiúsculas e minúsculas, pois [Msimsp.exe](msimsp-exe.md) e [Patchwiz.dll](patchwiz-dll.md) chamada Makecab.exe, que não diferencia maiúsculas de minúsculas e a geração de patch falha.

[Continuar](creating-a-patch-creation-properties-file.md)

 

 



