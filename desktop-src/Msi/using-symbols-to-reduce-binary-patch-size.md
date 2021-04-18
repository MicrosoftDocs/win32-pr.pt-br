---
description: Usar símbolos públicos para seus binários de imagem de destino e de atualização pode reduzir tamanhos de patch binários por aproximadamente uma metade.
ms.assetid: 83351a1b-ba70-4f0b-bacf-71ad7993a5aa
title: Usando símbolos para reduzir o tamanho do patch binário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d5ccf33dbf3ffefbee909d99bd0204ea2f49aba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105785419"
---
# <a name="using-symbols-to-reduce-binary-patch-size"></a>Usando símbolos para reduzir o tamanho do patch binário

Usar símbolos públicos para seus binários de imagem de destino e de atualização pode reduzir tamanhos de patch binários por aproximadamente uma metade. A redução real depende dos símbolos usados. Observe que o uso de símbolos pode resultar em tempos de criação de patch mais lentos porque leva mais tempo para processar os arquivos de símbolo.

Para reduzir o tamanho de um patch binário usando símbolos, você deve fornecer símbolos para os binários de imagem de destino e de atualização. Especifique os símbolos na coluna SymbolPaths da tabela [TargetImages](targetimages-table-patchwiz-dll-.md) e a coluna SymbolPaths da tabela [UpgradedImages](upgradedimages-table-patchwiz-dll-.md) . Você deve usar Visual C++ para gerar símbolos no formato de arquivo do banco de dados do programa (PDB). As versões mais recentes do Visual C++ fornecem todas as informações necessárias no arquivo PDB. As versões mais antigas do Visual C++ também geram o formato de arquivo de depuração (DBG). Nesse caso, o valor de SymbolsPaths deve especificar o local dos arquivos PDB e DBG.

Por exemplo, o TargetImage para um patch pode ser o pacote de instalação fornecido com o Windows 2000 e que instala a versão 1.1.1029.0 do MSI.DLL. O UpgradedImage pode ser o pacote de instalação atualizado fornecido com o Windows 2000 com Service Pack 1 (SP1) e que instala a versão 1.11.1314.0 do MSI.DLL. Dois arquivos PCP (Propriedades de criação de patch) teriam de ser criados, um com a coluna SymbolPaths das tabelas [TargetImages](targetimages-table-patchwiz-dll-.md) e [UpgradedImages](upgradedimages-table-patchwiz-dll-.md) deixados como nulo (em branco) e o outro com a coluna SymbolPaths das tabelas TargetImages e UpgradedImages preenchidas com o local dos símbolos para os binários. Nesse caso, o tamanho do patch gerado sem usar símbolos pode ser aproximadamente três vezes o tamanho do patch gerado usando símbolos.

O utilitário Mpatch.exe pode ser usado para testar a geração de patches binários para um único arquivo e verificar se os símbolos são válidos ou não. O utilitário Mpatch.exe está incluído nos [componentes SDK do Windows para os desenvolvedores de Windows Installer](platform-sdk-components-for-windows-installer-developers.md). A saída de Mpatch.exe indicará se os símbolos não coincidem.

Por exemplo, digite a linha de comando a seguir para verificar se os símbolos são válidos ou não.

**mpatch.exe-NEWSYMPATH: d: \\ Update-OLDSYMPATH: d: \\ destino d: \\ destino \\example.dll d: \\ Atualizar \\example.dll exemplo. Pat**

Se os símbolos não estiverem no local correto, a saída de Mpatch.exe poderá incluir o aviso a seguir.

``` syntax
WARNING: no debug symbols for d:\update\example.dll
```

 

 



