---
title: Desenvolvendo um provedor
description: Para gravar os eventos que você define em seu manifesto, use as funções incluídas na API de rastreamento de eventos (ETW). Para obter detalhes sobre como escrever um provedor, consulte fornecendo eventos.
ms.assetid: 23de19c4-5f8d-4faa-acd9-fe6208ca17a9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83939429f1dc4d499e7c2d0e0c2bfa7a47522ffe
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084826"
---
# <a name="developing-a-provider"></a>Desenvolvendo um provedor

Para gravar os eventos que você define em seu manifesto, use as funções incluídas na API de [rastreamento de eventos](/windows/desktop/ETW/event-tracing-portal) (ETW). Para obter detalhes sobre como escrever um provedor, consulte [fornecendo eventos](/windows/desktop/ETW/providing-events).

Depois de gravar o provedor, use a ferramenta WevtUtil.exe para registrar o provedor e o esquema. Para obter detalhes sobre como usar WevtUtil, consulte [ferramentas de log de eventos do Windows](windows-event-log-tools.md). O seguinte mostra como usar WevtUtil para registrar um provedor e remover o registro.


```cmd
wevtutil im provider.man

wevtutil um provider.man
```