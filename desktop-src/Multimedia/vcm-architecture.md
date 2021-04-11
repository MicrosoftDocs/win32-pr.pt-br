---
title: Arquitetura do VCM
description: Arquitetura do VCM
ms.assetid: cb0b036d-b8b1-4611-965f-08f932dbddb7
keywords:
- Vídeo para Windows (VFW), arquitetura VCM
- VFW (vídeo para Windows), arquitetura de VCM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89b672c86053086f63127aae586517fac4906326
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292453"
---
# <a name="vcm-architecture"></a><span data-ttu-id="6f7e7-105">Arquitetura do VCM</span><span class="sxs-lookup"><span data-stu-id="6f7e7-105">VCM Architecture</span></span>

<span data-ttu-id="6f7e7-106">VCM é um intermediário entre um aplicativo e a compactação e os drivers de descompactação.</span><span class="sxs-lookup"><span data-stu-id="6f7e7-106">VCM is an intermediary between an application and compression and decompression drivers.</span></span> <span data-ttu-id="6f7e7-107">Os drivers de compactação e descompactação compactam e descompactam quadros de dados individuais.</span><span class="sxs-lookup"><span data-stu-id="6f7e7-107">The compression and decompression drivers compress and decompress individual frames of data.</span></span>

<span data-ttu-id="6f7e7-108">Quando um aplicativo faz uma chamada para VCM, o VCM converte a chamada em uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="6f7e7-108">When an application makes a call to VCM, VCM translates the call into a message.</span></span> <span data-ttu-id="6f7e7-109">A mensagem é enviada usando a função [**ICSendMessage**](/windows/desktop/api/Vfw/nf-vfw-icsendmessage) para o compactador ou o descompactador apropriado, que compacta ou descompacta os dados.</span><span class="sxs-lookup"><span data-stu-id="6f7e7-109">The message is sent by using the [**ICSendMessage**](/windows/desktop/api/Vfw/nf-vfw-icsendmessage) function to the appropriate compressor or decompressor, which compresses or decompresses the data.</span></span> <span data-ttu-id="6f7e7-110">O VCM recebe o valor de retorno do driver de compactação ou descompactação e, em seguida, retorna o controle para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6f7e7-110">VCM receives the return value from the compression or decompression driver and then returns control to the application.</span></span>

<span data-ttu-id="6f7e7-111">Se uma macro for definida para uma mensagem, a macro se expandirá para uma chamada de função **ICSendMessage** fornecendo os parâmetros apropriados para essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="6f7e7-111">If a macro is defined for a message, the macro expands to an **ICSendMessage** function call supplying appropriate parameters for that message.</span></span> <span data-ttu-id="6f7e7-112">Se uma macro for definida para uma mensagem, seu aplicativo deverá usá-la em vez da mensagem.</span><span class="sxs-lookup"><span data-stu-id="6f7e7-112">If a macro is defined for a message, your application should use it rather than the message.</span></span> <span data-ttu-id="6f7e7-113">Nesta visão geral, essas macros seguem mensagens entre parênteses.</span><span class="sxs-lookup"><span data-stu-id="6f7e7-113">In this overview, these macros follow messages in parentheses.</span></span>

 

 




