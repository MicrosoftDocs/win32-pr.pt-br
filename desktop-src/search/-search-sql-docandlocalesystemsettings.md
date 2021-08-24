---
description: Quando o sistema operacional, ou até mesmo um aplicativo, é definido para usar um idioma e localidade específicos, muitas configurações são afetadas.
ms.assetid: cec164d1-125f-483c-9d74-0e24b8215157
title: documento e localidade do sistema Configurações
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed43ae52d7626b759563069b05fe4ae03649feb63fd1af8dab1b80cfd4d558a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119594776"
---
# <a name="document-and-system-locale-settings"></a>documento e localidade do sistema Configurações

Quando o sistema operacional, ou até mesmo um aplicativo, é definido para usar um idioma e localidade específicos, muitas configurações são afetadas. Essas configurações incluem formato numérico, formato de data, formato de moeda, mapeamento de letras maiúsculas e minúsculas, ordenação de classificação de dicionário, geração de tokens e outros. embora essas configurações ajudem a Windows a pesquisa fornece excelente suporte localizado, podem ocorrer resultados inesperados quando documentos de uma localidade são pesquisados usando um sistema definido como outra localidade.

Quando o objeto [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) processa as propriedades de texto e o conteúdo de um documento, ele relata o idioma desse documento para o indexador de conteúdo. usando essas informações, Windows pesquisa pode aplicar o separador de palavras apropriado.

 

 
