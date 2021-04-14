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
# <a name="requirements-for-text-to-speech-engines"></a><span data-ttu-id="b8de3-103">Requisitos para mecanismos de conversão de texto em fala</span><span class="sxs-lookup"><span data-stu-id="b8de3-103">Requirements for Text-To-Speech Engines</span></span>

<span data-ttu-id="b8de3-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="b8de3-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="b8de3-105">O mecanismo deve ser totalmente compatível com SAPI 4,0.</span><span class="sxs-lookup"><span data-stu-id="b8de3-105">The engine must be fully SAPI 4.0-compliant.</span></span> <span data-ttu-id="b8de3-106">Além disso, o mecanismo também deve dar suporte às seguintes interfaces SAPI para texto marcado e notificações de indicador.</span><span class="sxs-lookup"><span data-stu-id="b8de3-106">In addition, the engine must also support the following SAPI interfaces for tagged text and bookmark notifications.</span></span> <span data-ttu-id="b8de3-107">Essas interfaces permitem que o Microsoft Agent comacompanhe a saída do texto para o balão de palavras de um caractere e o Lip sincronize a boca do caractere (ou equivalente) com as palavras faladas.</span><span class="sxs-lookup"><span data-stu-id="b8de3-107">These interfaces enable Microsoft Agent to pace the output of text to a character's word balloon and lip-sync the character's mouth (or equivalent) with the spoken words.</span></span>

-   [<span data-ttu-id="b8de3-108">ITTSCentralW</span><span class="sxs-lookup"><span data-stu-id="b8de3-108">ITTSCentralW</span></span>](ittscentralw.md)
-   [<span data-ttu-id="b8de3-109">ITTSNotifySinkW</span><span class="sxs-lookup"><span data-stu-id="b8de3-109">ITTSNotifySinkW</span></span>](ittsnotifysinkw.md)
-   [<span data-ttu-id="b8de3-110">ITTSBufNotifySinkW</span><span class="sxs-lookup"><span data-stu-id="b8de3-110">ITTSBufNotifySinkW</span></span>](ittsbufnotifysinkw.md)
-   [<span data-ttu-id="b8de3-111">ITTSAttributesW</span><span class="sxs-lookup"><span data-stu-id="b8de3-111">ITTSAttributesW</span></span>](ittsattributesw.md)

 

 




