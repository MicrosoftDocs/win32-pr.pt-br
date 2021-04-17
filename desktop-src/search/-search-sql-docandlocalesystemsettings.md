---
description: Quando o sistema operacional, ou até mesmo um aplicativo, é definido para usar um idioma e localidade específicos, muitas configurações são afetadas.
ms.assetid: cec164d1-125f-483c-9d74-0e24b8215157
title: Configurações de localidade do sistema e do documento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9408093a8583a4b17566b5fcd118b30439c0ebda
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105791376"
---
# <a name="document-and-system-locale-settings"></a>Configurações de localidade do sistema e do documento

Quando o sistema operacional, ou até mesmo um aplicativo, é definido para usar um idioma e localidade específicos, muitas configurações são afetadas. Essas configurações incluem formato numérico, formato de data, formato de moeda, mapeamento de letras maiúsculas e minúsculas, ordenação de classificação de dicionário, geração de tokens e outros. Embora essas configurações ajudem a pesquisa do Windows a fornecer excelente suporte localizado, podem ocorrer resultados inesperados quando documentos de uma localidade são pesquisados usando um sistema definido como outra localidade.

Quando o objeto [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) processa as propriedades de texto e o conteúdo de um documento, ele relata o idioma desse documento para o indexador de conteúdo. Usando essas informações, o Windows Search pode aplicar o separador de palavras apropriado.

 

 
