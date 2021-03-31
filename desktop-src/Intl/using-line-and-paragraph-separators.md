---
description: Seus aplicativos devem usar o caractere separador de linha (0x2028) e o caractere separador de parágrafo (0x2029) para dividir o texto sem formatação. Uma nova linha é iniciada após cada separador de linha. Um novo parágrafo é iniciado após cada separador de parágrafo.
ms.assetid: 086aca6c-8d1f-4e54-9e1c-642be50b303c
title: Usando separadores de linha e parágrafo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2c9511ba2a8889b3c9139daf1d088d91ed746db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104172178"
---
# <a name="using-line-and-paragraph-separators"></a>Usando separadores de linha e parágrafo

Seus aplicativos devem usar o caractere separador de linha (0x2028) e o caractere separador de parágrafo (0x2029) para dividir o texto sem formatação. Uma nova linha é iniciada após cada separador de linha. Um novo parágrafo é iniciado após cada separador de parágrafo.

Não é necessário iniciar a primeira linha ou parágrafo em um arquivo com esses caracteres, ou para terminar a última linha ou parágrafo com eles. Isso indica que há uma linha ou parágrafo vazio nesse local.

O aplicativo pode usar o separador de linha para indicar um fim de linha incondicional. No entanto, separadores de linha não correspondem ao retorno de carro separado e caracteres de avanço de linha nem a uma combinação desses caracteres. Os separadores de linha devem ser processados separadamente de caracteres de avanço de linha e de retorno do carro.

O aplicativo pode inserir um separador de parágrafo entre parágrafos de texto. O uso desse separador permite a criação de arquivos de texto sem formatação que podem ser formatados com larguras de linha diferentes em sistemas operacionais diversos. O sistema de destino pode ignorar todos os separadores de linha e interromper parágrafos apenas nos separadores de parágrafo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando caracteres especiais em Unicode](using-special-characters-in-unicode.md)
</dt> </dl>

 

 



