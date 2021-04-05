---
description: Os autores de pacotes de instalação sempre devem executar a validação em seus pacotes antes de tentar instalar o pacote pela primeira vez e executar a validação novamente sempre que fizerem alterações no pacote.
ms.assetid: 1f16a349-4919-46d2-9b78-2533b8679a73
title: Validando um banco de dados de instalação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6db262a280afa1d9222696d40a6f5949d69ece0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826776"
---
# <a name="validating-an-installation-database"></a>Validando um banco de dados de instalação

Os autores de pacotes de instalação sempre devem executar a validação em seus pacotes antes de tentar instalar o pacote pela primeira vez e executar a validação novamente sempre que fizerem alterações no pacote. A validação examina o banco de dados em busca de erros que podem parecer válidos individualmente, mas que causam comportamento incorreto no contexto do banco de dados inteiro. A tentativa de instalar um pacote que falha na validação pode danificar o sistema do usuário. Consulte as seções [validação de pacote](package-validation.md) e [avaliadores de consistência internos-ICES](internal-consistency-evaluators-ices.md).

Você pode validar o pacote de exemplo usando [Orca.exe](orca-exe.md) ou [Msival2.exe](msival2-exe.md). Para exibir a ajuda para Msival2.exe alterar os diretórios e inserir na linha de comando.

Msival2 -?

O arquivo. Cub Darice. Cub contém as ações personalizadas de ICE necessárias para Msival2.exe executar a validação. Para validar o MNP2000.msi Enter

msival2 MNP2000.msi Darice. Cub

Para obter uma descrição das mensagens de erro e de aviso retornadas pela validação, consulte a [referência de Ice](ice-reference.md). Corrija todos os erros no pacote e execute a validação novamente conforme necessário até que o pacote passe na validação sem erros.

Depois que o pacote passar na validação, você poderá instalar o pacote de exemplo clicando no ícone de MNP2000.msi ou na linha de comando usando as [Opções de linha de comando](command-line-options.md).

Isso conclui a instalação de exemplo.

## <a name="next-example"></a>Próximo exemplo

[Um exemplo de atualização](an-upgrade-example.md)

 

 



