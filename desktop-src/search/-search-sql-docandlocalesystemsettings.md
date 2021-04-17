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
# <a name="document-and-system-locale-settings"></a><span data-ttu-id="e0a18-103">Configurações de localidade do sistema e do documento</span><span class="sxs-lookup"><span data-stu-id="e0a18-103">Document and System Locale Settings</span></span>

<span data-ttu-id="e0a18-104">Quando o sistema operacional, ou até mesmo um aplicativo, é definido para usar um idioma e localidade específicos, muitas configurações são afetadas.</span><span class="sxs-lookup"><span data-stu-id="e0a18-104">When the operating system, or even an application, is set to use a particular language and locale, many settings are affected.</span></span> <span data-ttu-id="e0a18-105">Essas configurações incluem formato numérico, formato de data, formato de moeda, mapeamento de letras maiúsculas e minúsculas, ordenação de classificação de dicionário, geração de tokens e outros.</span><span class="sxs-lookup"><span data-stu-id="e0a18-105">These settings include numeric format, date format, currency format, uppercase and lowercase mapping, dictionary sort ordering, tokenization, and others.</span></span> <span data-ttu-id="e0a18-106">Embora essas configurações ajudem a pesquisa do Windows a fornecer excelente suporte localizado, podem ocorrer resultados inesperados quando documentos de uma localidade são pesquisados usando um sistema definido como outra localidade.</span><span class="sxs-lookup"><span data-stu-id="e0a18-106">Although these settings help Windows Search provide excellent localized support, unexpected results can occur when documents from one locale are searched by using a system that is set to another locale.</span></span>

<span data-ttu-id="e0a18-107">Quando o objeto [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) processa as propriedades de texto e o conteúdo de um documento, ele relata o idioma desse documento para o indexador de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="e0a18-107">When the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) object processes a document's text properties and content, it reports the language of that document to the content indexer.</span></span> <span data-ttu-id="e0a18-108">Usando essas informações, o Windows Search pode aplicar o separador de palavras apropriado.</span><span class="sxs-lookup"><span data-stu-id="e0a18-108">Using this information, Windows Search can apply the appropriate word breaker.</span></span>

 

 
