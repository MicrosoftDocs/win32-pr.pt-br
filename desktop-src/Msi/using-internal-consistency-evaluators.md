---
description: Para validar um banco de dados, use uma ferramenta de validação especial para mesclar um arquivo .file que contém os ICEs (Avaliadores de Consistência Interna) em seu banco de dados, executar os ICEs e relatar os resultados.
ms.assetid: bdf38673-ee3d-47d8-ad6e-562cd5626918
title: Usando avaliadores de consistência interna
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdd0964b43bdf237c01b2645ca9556ed5560cefd2b047cc108a8919060d1fad9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012744"
---
# <a name="using-internal-consistency-evaluators"></a>Usando avaliadores de consistência interna

Para validar um banco de dados, use uma ferramenta [](internal-consistency-evaluators-ices.md) de validação especial para mesclar um arquivo .file que contém os ICEs (Avaliadores de Consistência Interna) em seu banco de dados, executar os ICEs e relatar os resultados. Várias dessas ferramentas são fornecidas no Microsoft Windows Software Development Kit (SDK). Ambientes de autor de fornecedores de terceiros também podem incorporar o sistema de validação ICE em seu ambiente de autor. Também é possível escrever sua própria ferramenta para executar a validação de ICE. A maioria das ferramentas de validação ICE mescla o arquivo .file e seu banco de dados em um terceiro banco de dados temporário. Windows O instalador exibe avisos, erros, informações de depuração e erros de API à medida que executa cada ICE no arquivo .file. Quando o instalador concluir a execução dos ICEs, ele fechará o arquivo .msi, o arquivo .file e o banco de dados temporário sem salvar nenhuma alteração. O .msi arquivo e o arquivo .file permanecem inalterados pelo teste de validação.

As ações personalizadas ice se comunicam com o usuário [**chamando MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) e postando uma mensagem INSTALLMESSAGE \_ USER. Uma mensagem ICE normalmente retorna informações como as seguintes:

-   Nome do ICE que encontrou um erro
-   Data em que o ICE foi criado
-   Autor do ICE
-   Data em que o ICE foi modificado pela última vez.
-   Descrição do erro de API fazendo com que o ICE falhe
-   Descrição do erro
-   Um aviso para o usuário
-   Nome da tabela de banco de dados que contém o erro ou aviso
-   Nome da coluna de tabela que contém o erro ou aviso
-   Chaves primárias da tabela que contém o erro ou aviso
-   Uma URL para um arquivo HTML dando sugestões de depuração
-   Uma cadeia de caracteres que pode conter outras informações

Os autores de pacotes de instalação podem escrever ações personalizadas ice ou usar o conjunto padrão de ICEs incluídos nos arquivos .set fornecidos com o SDK. Para obter mais informações sobre como escrever um ICE, consulte [Criando um ICE.](building-an-ice.md)

Depois de escrever os ICEs apropriados para validação, um desenvolvedor deve coletar as ações personalizadas em um banco de dados .msi, chamado de arquivo .oracle, que contém apenas os ICEs e suas tabelas necessárias. Um arquivo .file não pode ser instalado e é usado apenas para armazenar e fornecer acesso a ações personalizadas ice. Para obter mais informações sobre como criar arquivos .cú, consulte [Criando um banco de dados ICE.](building-an-ice-database.md) Como alternativa, os desenvolvedores podem validar seu pacote de instalação usando os ICEs existentes descritos em [Referência de ICE.](ice-reference.md) Esses ICEs podem ser obtidos de arquivos .cú padrão fornecidos com o SDK.

A instalação do editor de tabela de banco de dados Orca ou da ferramenta de validação msival2 fornece os arquivos Logo.oracle, Darice.oracle e Mergemod.oracle. O conjunto de ICEs no arquivo Logo.file é um subconjunto daqueles no arquivo Darice.file. Se o pacote passar na validação usando Darice.plus, ele passará com Logo.plus. Mergemod.ltd contém um conjunto de ICEs usados para validar módulos de mesclagem. Para obter mais informações, consulte [Referência ice do módulo de mesclagem](merge-module-ice-reference.md).

**Para validar um pacote de instalação**

1.  Obtenha ou autor das ações personalizadas de ICE apropriadas. Você pode usar um ou mais dos ICEs existentes descritos na [Referência ICE.](ice-reference.md) Se sua validação exigir um ICE ainda não nesta lista, você poderá criar um novo ICE, conforme descrito em [Criando um ICE.](building-an-ice.md)
2.  Prepare um Banco de Dados ICE que contém todas as ações personalizadas do ICE. Consulte a seção [Criando um banco de dados ICE](building-an-ice-database.md) para obter informações sobre como preparar um arquivo .file.
3.  Forneça o arquivo .file e o arquivo .msi para uma ferramenta de validação de [ pacote, como ](orca-exe.md)Orca.exeou [Msival2.exe](msival2-exe.md).

Observe que os módulos de mesclagem devem ser validados conforme descrito em [Validando módulos de mesclagem.](validating-merge-modules.md)

 

 



