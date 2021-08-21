---
description: A geração de um novo patch pode exigir um tempo significativo.
ms.assetid: 8be9a83a-8c36-43f5-8dda-05fc2f3ce0d2
title: Caching de informações de Patch (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71513ea1a9418506bbf9025f66a1689c12e9a53f8e6f2e713ddeb3b3d55de580
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118942617"
---
# <a name="patch-information-caching-patchwizdll"></a>Caching de informações de Patch (Patchwiz.dll)

A geração de um novo patch pode exigir um tempo significativo. Depois de gerar um patch usando [Patchwiz.dll](patchwiz-dll.md), talvez seja necessário alterar a imagem de atualização novamente e gerar outro patch. O cache de informações de patch pode reduzir o tempo necessário para gerar patches subsequentes reutilizando patches existentes. Por exemplo, o tempo necessário para criar Service Packs pode ser reduzido usando os patches binários gerados de patches anteriores. Patchwiz.dll pode usar \_ \_ o dir do cache de patch para encontrar um patch binário existente e adicioná-lo ao gabinete do Service Pack sem precisar recriar o patch binário.

O cache de informações de patch requer o uso de [Patchwiz.dll](patchwiz-dll.md). Para ativar o cache de patch, defina as propriedades de cache de patch \_ \_ habilitado e caminho \_ de cache de patch \_ na [tabela de Propriedades (Patchwiz.dll)](properties-table-patchwiz-dll-.md) do arquivo de propriedades de criação de patch (arquivo. PCP). O Patchwiz armazena todas as informações de criação de patch na pasta identificada pela \_ Propriedade dir do cache de patch \_ e cria essa pasta, se necessário. Na próxima vez que você tentar criar um patch, o Patchwiz verificará essa pasta para ver se os arquivos a serem comparados correspondem aos arquivos no cache. Se os arquivos corresponderem, o Patchwiz usará as informações em cache em vez de regenerar o patch binário para o arquivo. Se os arquivos não corresponderem ou se as informações estiverem ausentes do cache, o Patchwiz gerará o patch para o arquivo.

Para usar o cache de informações de patch, a pasta especificada pelo dir de cache de PATCH \_ \_ deve ser preservada após a criação de um arquivo. msp. Se a pasta for excluída, o PatchWiz precisará gerar novamente patches binários para arquivos. msp subsequentes. Para obter mais informações sobre como preservar informações em regiões selecionadas de um arquivo de destino, consulte [aplicando patch nas regiões selecionadas de um arquivo](patching-selected-regions-of-a-file.md).

 

 



