---
description: Para validar um banco de dados, use uma ferramenta de validação especial para mesclar um arquivo. Cub contendo avaliadores de consistência internos (ICEs) em seu banco de dados, executar a ICEs e relatar os resultados.
ms.assetid: bdf38673-ee3d-47d8-ad6e-562cd5626918
title: Usando avaliadores de consistência internos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 423e6dab453ae495dc6029b54eb039c8acc60f33
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105770169"
---
# <a name="using-internal-consistency-evaluators"></a>Usando avaliadores de consistência internos

Para validar um banco de dados, use uma ferramenta de validação especial para mesclar um arquivo. Cub contendo [avaliadores de consistência internos](internal-consistency-evaluators-ices.md) (ICES) em seu banco de dados, executar a ICES e relatar os resultados. Várias ferramentas desse tipo são fornecidas no SDK (Software Development Kit) do Microsoft Windows. A criação de ambientes de fornecedores terceirizados também pode incorporar o sistema de validação de gelo ao seu ambiente de criação. Também é possível escrever sua própria ferramenta para executar a validação de gelo. A maioria das ferramentas de validação de ICE mescla o arquivo. Cub e o banco de dados em um terceiro banco de dados temporário. Windows Installer exibe avisos, erros, informações de depuração e erros de API à medida que ele executa cada ICE no arquivo. cub. Quando o instalador conclui a execução do ICEs, ele fecha o arquivo. msi, o arquivo. Cub e o banco de dados temporário sem salvar nenhuma alteração. O arquivo. msi e o arquivo. Cub permanecem inalterados pelo teste de validação.

As ações personalizadas do ICE se comunicam ao usuário chamando [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) e postando uma mensagem de usuário do INSTALLMESSAGE \_ . Uma mensagem ICE normalmente retorna informações como as seguintes:

-   Nome do ICE que encontrou um erro
-   Data em que o ICE foi criado
-   Autor da ICE
-   Data em que a ICE foi modificada pela última vez.
-   Descrição do erro de API que causa a falha do ICE
-   Descrição do erro
-   Um aviso para o usuário
-   Nome da tabela de banco de dados que contém o erro ou aviso
-   Nome da coluna da tabela que contém o erro ou aviso
-   Chaves primárias da tabela que contém o erro ou aviso
-   Uma URL para um arquivo HTML fornecendo sugestões de depuração
-   Uma cadeia de caracteres que pode conter outras informações

Os autores de pacotes de instalação podem escrever ações personalizadas de gelo ou usar o conjunto padrão de ICEs incluído nos arquivos. Cub fornecidos com o SDK. Para obter mais informações sobre como escrever um ICE, consulte [criando um Ice](building-an-ice.md).

Depois de escrever o ICEs apropriado para validação, um desenvolvedor deve coletar as ações personalizadas em um banco de dados. msi, chamado um arquivo. Cub, que contém apenas as mesmas e as tabelas necessárias. Um arquivo. Cub não pode ser instalado e usado somente para armazenar e fornecer acesso a ações personalizadas do ICE. Para obter mais informações sobre como criar arquivos. Cub, consulte [criando um banco de dados Ice](building-an-ice-database.md). Como alternativa, os desenvolvedores podem validar seu pacote de instalação usando as ICEs existentes descritas na [referência do Ice](ice-reference.md). Essas ICEs podem ser obtidas a partir de arquivos. Cub padrão fornecidos com o SDK.

A instalação do Orca Editor de tabela de banco de dados ou da ferramenta de validação msival2 fornece os arquivos logo. Cub, Darice. Cub e Mergemod. cub. O conjunto de ICEs no arquivo logo. Cub é um subconjunto daqueles no arquivo Darice. cub. Se o pacote passar na validação usando Darice. Cub, ele passará com logo. cub. Mergemod. Cub contém um conjunto de ICEs usado para validar módulos de mesclagem. Para obter mais informações, consulte [referência de Ice do módulo de mesclagem](merge-module-ice-reference.md).

**Para validar um pacote de instalação**

1.  Obtenha ou crie as ações personalizadas de ICE apropriadas. Você poderá usar uma ou mais das ICEs existentes descritas na [referência do Ice](ice-reference.md). Se sua validação exigir uma ICE ainda não nesta lista, você poderá criar uma nova ICE, conforme descrito em [criando um Ice](building-an-ice.md).
2.  Prepare um banco de dados ICE contendo todas as ações personalizadas do ICE. Consulte a seção [criando um banco de dados Ice](building-an-ice-database.md) para obter informações sobre como preparar um arquivo. cub.
3.  Forneça o arquivo. Cub e o arquivo. msi para uma ferramenta de validação de pacote, como [Orca.exe](orca-exe.md) ou [Msival2.exe](msival2-exe.md).

Observe que os módulos de mesclagem devem ser validados conforme descrito em [Validando módulos de mesclagem](validating-merge-modules.md).

 

 



