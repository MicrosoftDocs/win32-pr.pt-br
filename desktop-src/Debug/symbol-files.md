---
description: Normalmente, as informações de depuração são armazenadas em um arquivo de símbolo separado do executável.
ms.assetid: 610e5cd3-9dc3-462c-98f8-6a63874464f8
title: Arquivos de Símbolo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 610e289a64ed807a26086f12780b45bc35ea65464946ec81a07e4169515d1132
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119642176"
---
# <a name="symbol-files"></a>Arquivos de Símbolo

Normalmente, as informações de depuração são armazenadas em um arquivo de símbolo separado do executável. A implementação dessas informações de depuração mudou ao longo dos anos, e a documentação a seguir fornecerá orientações sobre essas várias implementações.

## <a name="pdb-files"></a>arquivos PDB

Todas as versões modernas dos compiladores da Microsoft armazenam informações de depuração sobre um executável compilado em um arquivo de *banco de dados de programa* separado (. pdb). Esse arquivo é comumente chamado de *PDB*. Os dados são armazenados em um arquivo separado do executável para ajudar a limitar o tamanho do executável, economizando espaço de armazenamento em disco e reduzindo o tempo necessário para carregar os dados. Essa metodologia também permite que o executável seja distribuído sem revelar essas informações significativas, o que pode facilitar a engenharia reversa do programa.

Para criar um PDB, compile o arquivo executável com informações de depuração de acordo com as instruções para suas ferramentas de Build.

A API DbgHelp é capaz de usar PDBs para obter as informações a seguir.

-   públicos e exportações
-   símbolos globais
-   símbolos locais
-   dados de tipo
-   arquivos de origem
-   números de linha

## <a name="dbg-files-and-embedded-debug-information"></a>Arquivos DBG e informações de depuração inseridas

Versões anteriores do conjunto de ferramentas da Microsoft usavam para inserir as informações de depuração no executável, no entanto, normalmente seriam removidas para um arquivo separado com uma extensão. dbg. Isso normalmente é conhecido como um arquivo *DBG* . Os arquivos DBG usam o mesmo formato de arquivo PE como executáveis.

O suporte de API do DbgHelp para DBGs e informações de depuração incorporadas é limitado e inclui o seguinte.

-   públicos e exportações
-   símbolos globais

 

 



