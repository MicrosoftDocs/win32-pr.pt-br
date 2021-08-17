---
title: Desenvolvendo um provedor
description: Para gravar os eventos que você define em seu manifesto, use as funções incluídas na API de rastreamento de eventos (ETW). Para obter detalhes sobre como escrever um provedor, consulte fornecendo eventos.
ms.assetid: 23de19c4-5f8d-4faa-acd9-fe6208ca17a9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bdcbf17113eb926aba245f270b84e7ab50bf3072e15a9a7752b8828296a00a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117937181"
---
# <a name="developing-a-provider"></a>Desenvolvendo um provedor

Para gravar os eventos que você define em seu manifesto, use as funções incluídas na API de [rastreamento de eventos](/windows/desktop/ETW/event-tracing-portal) (ETW). Para obter detalhes sobre como escrever um provedor, consulte [fornecendo eventos](/windows/desktop/ETW/providing-events).

Depois de gravar o provedor, use a ferramenta WevtUtil.exe para registrar o provedor e o esquema. para obter detalhes sobre como usar WevtUtil, consulte [Windows ferramentas de Log de eventos](windows-event-log-tools.md). O seguinte mostra como usar WevtUtil para registrar um provedor e remover o registro.


```cmd
wevtutil im provider.man

wevtutil um provider.man
```