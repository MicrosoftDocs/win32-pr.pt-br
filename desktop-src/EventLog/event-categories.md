---
description: As categorias ajudam a organizar eventos para que Visualizador de Eventos possam filtrá-los. Cada fonte de evento pode definir suas próprias categorias numeradas e as cadeias de caracteres de texto para as quais elas estão mapeadas.
ms.assetid: ddba8066-b6b9-42a6-b49f-cbae8f97ef6d
title: Categorias de evento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efd84a095754bd51499edf5a21ebea0ade042d75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105789819"
---
# <a name="event-categories"></a>Categorias de evento

As categorias ajudam a organizar eventos para que Visualizador de Eventos possam filtrá-los. Cada [fonte de evento](event-sources.md) pode definir suas próprias categorias numeradas e as cadeias de caracteres de texto para as quais elas estão mapeadas.

As categorias devem ser numeradas consecutivamente, começando com o número 1. As categorias em si são definidas em um arquivo de mensagem. Por exemplo, use a sintaxe a seguir para declarar três categorias de evento. No Visualizador de Eventos, os eventos que usam essas categorias terão a categoria 1, categoria 2 ou categoria 3 exibida na coluna **categoria** .

``` syntax
MessageId=0x1
SymbolicName=CATEGORY_1
Language=English
Category 1
.

MessageId=0x2
SymbolicName=CATEGORY_2
Language=English
Category 2
.

MessageId=0x3
SymbolicName=CATEGORY_3
Language=English
Category 3
.
```

As categorias podem ser armazenadas em um arquivo de mensagem separado ou em um arquivo que contém mensagens de outros tipos. Se você criar um único arquivo de mensagem, certifique-se de que as categorias sejam as primeiras mensagens no arquivo. Para obter mais informações sobre como criar e usar arquivos de mensagens, consulte [arquivos de mensagem](message-files.md).

O número total de categorias é armazenado no valor de **CategoryCount** para a origem do evento.

 

 



