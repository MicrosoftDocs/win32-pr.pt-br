---
title: Requisitos para mecanismos de conversão de texto em fala
description: Requisitos para mecanismos de conversão de texto em fala
ms.assetid: 21d19949-c9b4-4d9c-9684-6d15162f7a7d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa6d1bc9f4340327c5fbfb71b900e10f60738fdf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104453621"
---
# <a name="requirements-for-text-to-speech-engines"></a>Requisitos para mecanismos de conversão de texto em fala

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

O mecanismo deve ser totalmente compatível com SAPI 4,0. Além disso, o mecanismo também deve dar suporte às seguintes interfaces SAPI para texto marcado e notificações de indicador. Essas interfaces permitem que o Microsoft Agent comacompanhe a saída do texto para o balão de palavras de um caractere e o Lip sincronize a boca do caractere (ou equivalente) com as palavras faladas.

-   [ITTSCentralW](ittscentralw.md)
-   [ITTSNotifySinkW](ittsnotifysinkw.md)
-   [ITTSBufNotifySinkW](ittsbufnotifysinkw.md)
-   [ITTSAttributesW](ittsattributesw.md)

 

 




