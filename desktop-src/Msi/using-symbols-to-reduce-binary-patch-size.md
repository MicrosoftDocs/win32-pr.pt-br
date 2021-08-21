---
description: O uso de símbolos públicos para os binários de imagem de destino e atualização pode reduzir os tamanhos de patch binários em aproximadamente metade.
ms.assetid: 83351a1b-ba70-4f0b-bacf-71ad7993a5aa
title: Usando símbolos para reduzir o tamanho do patch binário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 502c11a1a6b058db8c9f4a7c9bde897034c3b4affa8c02d1b049d754013f4455
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117804078"
---
# <a name="using-symbols-to-reduce-binary-patch-size"></a>Usando símbolos para reduzir o tamanho do patch binário

O uso de símbolos públicos para os binários de imagem de destino e atualização pode reduzir os tamanhos de patch binários em aproximadamente metade. A redução real depende dos símbolos usados. Observe que o uso de símbolos pode resultar em tempos de criação de patch mais lentos porque leva mais tempo para processar os arquivos de símbolo.

Para reduzir o tamanho de um patch binário usando símbolos, você deve fornecer símbolos para os binários de imagem de destino e de atualização. Especifique os símbolos na coluna SymbolPaths da tabela [TargetImages](targetimages-table-patchwiz-dll-.md) e na coluna SymbolPaths da [tabela UpgradedImages.](upgradedimages-table-patchwiz-dll-.md) Você deve usar Visual C++ para gerar símbolos no formato de arquivo PDB (banco de dados do programa). Versões mais recentes Visual C++ fornecem todas as informações necessárias no arquivo PDB. As versões mais antigas Visual C++ também geram o formato de arquivo dbG (depuração). Nesse caso, o valor SymbolsPaths deve especificar o local dos arquivos PDB e DBG.

Por exemplo, o TargetImage para um patch pode ser o pacote de instalação fornecido com o Windows 2000 e que instala a versão 1.1.1029.0 do MSI.DLL. O UpgradedImage pode ser o pacote de instalação atualizado fornecido com o Windows 2000 com Service Pack 1 (SP1) e que instala a versão 1.11.1314.0 do MSI.DLL. Dois arquivos PCP (Propriedades de Criação de Patch) teriam que ser criados, um com a coluna SymbolPaths das tabelas [TargetImages](targetimages-table-patchwiz-dll-.md) e [UpgradedImages](upgradedimages-table-patchwiz-dll-.md) deixadas como NULL (em branco) e outro com a coluna SymbolPaths das tabelas TargetImages e UpgradedImages preenchidas com o local dos símbolos para os binários. Nesse caso, o tamanho do patch gerado sem usar símbolos pode ser aproximadamente três vezes o tamanho do patch gerado usando símbolos.

O Mpatch.exe utilitário pode ser usado para testar a geração de patches binários para um único arquivo e verificar se os símbolos são válidos ou não. O Mpatch.exe utilitário está incluído no Windows [componentes do SDK para desenvolvedores Windows instalador.](platform-sdk-components-for-windows-installer-developers.md) A saída de Mpatch.exe indicará se os símbolos não corresponderão.

Por exemplo, insira a linha de comando a seguir para verificar se os símbolos são válidos ou não.

**mpatch.exe -NEWSYMPATH:d: \\ update -OLDSYMPATH:d: \\ target d: \\ targetexample.dll \\ d: updateexample.dll \\ \\ example.pat**

Se os símbolos não estão no local correto, a saída Mpatch.exe pode incluir o aviso a seguir.

``` syntax
WARNING: no debug symbols for d:\update\example.dll
```

 

 



