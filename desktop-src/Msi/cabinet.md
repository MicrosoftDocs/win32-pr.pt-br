---
description: O tipo de dados de gabinete deve ser usado na coluna de gabinete da tabela de mídia.
ms.assetid: 149c74ea-4342-45dd-8da4-4dfa7f4317a0
title: Gabinete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4814473ef4d21d5445b5b5319278a5e25a7f5540
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828041"
---
# <a name="cabinet"></a>Gabinete

O tipo de dados de gabinete deve ser usado na coluna de gabinete da [tabela de mídia](media-table.md).

Se o nome do gabinete for precedido pelo sinal de número, o gabinete será armazenado como um fluxo de dados dentro do pacote. A cadeia de caracteres que segue o \# é um [identificador](identifier.md) para este fluxo de dados. Observe que, se o gabinete for armazenado como um fluxo de dados, o nome de um gabinete diferenciará maiúsculas de minúsculas.

Se o nome do gabinete não for precedido pelo sinal numérico \# , o gabinete será armazenado em um arquivo separado localizado na raiz da árvore de origem especificada pela tabela de [diretórios](directory-table.md). O arquivo de gabinete deve usar a sintaxe de nome de arquivo curto que consiste em um nome de oito caracteres, um ponto e uma extensão de três caracteres. O tipo de dados Cabinet não pode usar a \| sintaxe curta longa para nomes de arquivo. Se o arquivo de gabinete for armazenado como um arquivo separado, o nome do arquivo de gabinete não diferenciará maiúsculas de minúsculas.

Para conservar o espaço em disco, o instalador remove todos os gabinetes inseridos no arquivo. msi antes de armazenar em cache o pacote de instalação no computador do usuário.

Consulte [incluindo um arquivo de gabinete em uma instalação](including-a-cabinet-file-in-an-installation.md).

 

 



