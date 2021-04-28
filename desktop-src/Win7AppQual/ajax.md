---
description: AJAX
ms.assetid: F9907D49-F9FE-406A-BF5F-17C61706ADC1
title: AJAX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 575ab08530936ab083baa4bb3fcfa2956ffe3b2d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088754"
---
# <a name="ajax"></a>AJAX

Os recursos do AJAX no Windows Internet Explorer 8 como [**XDomainRequest (XDR)**](https://msdn.microsoft.com/library/Cc288060(v=VS.85).aspx) e [xdm (mensagens entre documentos)](https://download.microsoft.com/download/7/0/D/70D193BF-F818-4539-8325-A2F321C3061E/Cross Document Messaging - Developer Series Information Page.pdf) têm propriedades nativas que podem entrar em conflito com as propriedades personalizadas existentes.

O Windows Internet Explorer expõe novas propriedades para determinados recursos do AJAX, como [xdm (mensagens entre documentos)](https://download.microsoft.com/download/7/0/D/70D193BF-F818-4539-8325-A2F321C3061E/Cross Document Messaging - Developer Series Information Page.pdf), mesmo no modo de exibição de compatibilidade. Se você adicionar propriedades personalizadas ao objeto Event, elas poderão entrar em conflito com essas novas propriedades, como **Source**.

O exemplo de código a seguir funciona em versões mais antigas do Internet Explorer, mas não nas versões mais recentes, pois os novos recursos usam a propriedade **Source** .


```JScript
event.source = myObject;
```



O exemplo de código a seguir mostra como você pode alterar esse objeto para permanecer compatível.


```JScript
event.mySource = myObject;// Read-only in IE8, use mySource instead
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Corrigindo problemas de compatibilidade em aplicativos Web usando o modo de exibição de compatibilidade](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 



