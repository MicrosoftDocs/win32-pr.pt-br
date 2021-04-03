---
description: O padrão Unicode não prescreve significativos específicos para os códigos de controle 0x000D (retorno de carro) e 0x000A (avanço de alimentação).
ms.assetid: fb8b1a5c-79a4-45a0-b7a1-8217c370d13e
title: Usando códigos de controle ASCII 0x000D e 0x000A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d509c83bfd6349dcceb05ab4a8946aae51feacdc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922908"
---
# <a name="using-ascii-control-codes-0x000d-and-0x000a"></a><span data-ttu-id="c33a6-103">Usando códigos de controle ASCII 0x000D e 0x000A</span><span class="sxs-lookup"><span data-stu-id="c33a6-103">Using ASCII Control Codes 0x000D and 0x000A</span></span>

<span data-ttu-id="c33a6-104">O padrão Unicode não prescreve significativos específicos para os códigos de controle 0x000D (retorno de carro) e 0x000A (avanço de alimentação).</span><span class="sxs-lookup"><span data-stu-id="c33a6-104">The Unicode standard does not prescribe specific meanings for the control codes 0x000D (carriage return) and 0x000A (linefeed).</span></span> <span data-ttu-id="c33a6-105">Esses códigos não precisam ser usados em combinação.</span><span class="sxs-lookup"><span data-stu-id="c33a6-105">These codes are not required to be used in combination.</span></span> <span data-ttu-id="c33a6-106">Se usado individualmente, qualquer código pode representar apenas ou ambos os códigos juntos.</span><span class="sxs-lookup"><span data-stu-id="c33a6-106">If used individually, either code can represent itself only or both codes together.</span></span> <span data-ttu-id="c33a6-107">O aplicativo sempre deve determinar o que esses códigos representam.</span><span class="sxs-lookup"><span data-stu-id="c33a6-107">The application must always determine what these codes represent.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c33a6-108">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c33a6-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c33a6-109">Usando caracteres especiais em Unicode</span><span class="sxs-lookup"><span data-stu-id="c33a6-109">Using Special Characters in Unicode</span></span>](using-special-characters-in-unicode.md)
</dt> </dl>

 

 



