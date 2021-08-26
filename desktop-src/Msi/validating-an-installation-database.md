---
description: Os autores de pacotes de instalação sempre devem executar a validação em seus pacotes antes de tentar instalar o pacote pela primeira vez e executar a validação novamente sempre que fizerem alterações no pacote.
ms.assetid: 1f16a349-4919-46d2-9b78-2533b8679a73
title: Validando um banco de dados de instalação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d28d4d1937b5946d6c1df85a4c6c21ec8113ef6463b5aaad0e181f4bdc711e70
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119995816"
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

 

 



