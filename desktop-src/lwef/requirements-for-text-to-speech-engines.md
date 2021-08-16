---
title: Requisitos para mecanismos de conversão de texto em fala
description: Requisitos para mecanismos de conversão de texto em fala
ms.assetid: 21d19949-c9b4-4d9c-9684-6d15162f7a7d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3025be266d0aa40cd5a3bca6adb63e333310df444be7bd07e3a72b0f10b9c49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118746411"
---
# <a name="requirements-for-text-to-speech-engines"></a>Requisitos para mecanismos de conversão de texto em fala

\[o Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

O mecanismo deve ser totalmente compatível com SAPI 4,0. Além disso, o mecanismo também deve dar suporte às seguintes interfaces SAPI para texto marcado e notificações de indicador. Essas interfaces permitem que o Microsoft Agent comacompanhe a saída do texto para o balão de palavras de um caractere e o Lip sincronize a boca do caractere (ou equivalente) com as palavras faladas.

-   [ITTSCentralW](ittscentralw.md)
-   [ITTSNotifySinkW](ittsnotifysinkw.md)
-   [ITTSBufNotifySinkW](ittsbufnotifysinkw.md)
-   [ITTSAttributesW](ittsattributesw.md)

 

 




