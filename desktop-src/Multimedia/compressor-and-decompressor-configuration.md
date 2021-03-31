---
title: Configuração de compactador e descompactador
description: Configuração de compactador e descompactador
ms.assetid: 677241d2-3ddd-423a-a1e7-b5fa3ce0a4eb
keywords:
- VCM (Gerenciador de compactação de vídeo), configurando os compactadores
- VCM (Gerenciador de compactação de vídeo), configurando os compactadores
- ICM_CONFIGURE mensagem
- Macro ICQueryConfigure
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a38fbbeb852d09296e5be7929738c9d4d71f118e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916198"
---
# <a name="compressor-and-decompressor-configuration"></a><span data-ttu-id="bb58f-107">Configuração de compactador e descompactador</span><span class="sxs-lookup"><span data-stu-id="bb58f-107">Compressor and Decompressor Configuration</span></span>

<span data-ttu-id="bb58f-108">Seu aplicativo pode configurar o compactador ou o descompactador automaticamente, ou pode permitir que o usuário os configure.</span><span class="sxs-lookup"><span data-stu-id="bb58f-108">Your application can configure the compressor or decompressor automatically, or it can allow the user to configure them.</span></span> <span data-ttu-id="bb58f-109">Se for prático, permita que o usuário configure o compressor ou o descompactador; Isso lhe libera de considerar todas as opções para o compressor ou o descompactador.</span><span class="sxs-lookup"><span data-stu-id="bb58f-109">If it is practical, allow the user to configure the compressor or decompressor; this frees you from considering all the options for the compressor or decompressor.</span></span>

<span data-ttu-id="bb58f-110">O usuário pode configurar o compressor ou o descompactador usando uma caixa de diálogo de configuração.</span><span class="sxs-lookup"><span data-stu-id="bb58f-110">The user can configure the compressor or decompressor by using a configuration dialog box.</span></span> <span data-ttu-id="bb58f-111">Você pode enviar a mensagem de [**\_ configuração de ICM**](icm-configure.md) para VCM (ou usar a macro [**ICQueryConfigure**](/windows/desktop/api/Vfw/nf-vfw-icqueryconfigure) ) para determinar se um compactador ou descompactador pode exibir uma caixa de diálogo de configuração.</span><span class="sxs-lookup"><span data-stu-id="bb58f-111">You can send the [**ICM\_CONFIGURE**](icm-configure.md) message to VCM (or use the [**ICQueryConfigure**](/windows/desktop/api/Vfw/nf-vfw-icqueryconfigure) macro) to determine if a compressor or decompressor can display a configuration dialog box.</span></span> <span data-ttu-id="bb58f-112">Nesse caso, envie a \_ mensagem ICM configure (ou use a macro [**ICConfigure**](/windows/desktop/api/Vfw/nf-vfw-icconfigure) ) para exibi-la.</span><span class="sxs-lookup"><span data-stu-id="bb58f-112">If so, send the ICM\_CONFIGURE message (or use the [**ICConfigure**](/windows/desktop/api/Vfw/nf-vfw-icconfigure) macro) to display it.</span></span>

<span data-ttu-id="bb58f-113">Seu aplicativo pode enviar as mensagens de [**ICM \_ GetState**](icm-getstate.md) e [**ICM \_ SetState**](icm-setstate.md) (ou usar as macros [**ICGetStateSize**](/windows/desktop/api/Vfw/nf-vfw-icgetstatesize), [**ICGetState**](/windows/desktop/api/Vfw/nf-vfw-icgetstate)e [**ICSetState**](/windows/desktop/api/Vfw/nf-vfw-icsetstate) ) para obter e definir o status de um compressor ou descompactador.</span><span class="sxs-lookup"><span data-stu-id="bb58f-113">Your application can send the [**ICM\_GETSTATE**](icm-getstate.md) and [**ICM\_SETSTATE**](icm-setstate.md) messages (or use the [**ICGetStateSize**](/windows/desktop/api/Vfw/nf-vfw-icgetstatesize), [**ICGetState**](/windows/desktop/api/Vfw/nf-vfw-icgetstate), and [**ICSetState**](/windows/desktop/api/Vfw/nf-vfw-icsetstate) macros) to get and set the status for a compressor or decompressor.</span></span> <span data-ttu-id="bb58f-114">Se o seu aplicativo criar ou modificar o status, ele deverá obter o layout dos dados do compressor ou do descompactador antes de restaurar seu status.</span><span class="sxs-lookup"><span data-stu-id="bb58f-114">If your application creates or modifies the status, it must obtain the layout of the compressor or decompressor data before restoring its status.</span></span> <span data-ttu-id="bb58f-115">Como alternativa, se seu aplicativo obtiver o status de um compressor ou descompactador e usá-lo para restaurar o status em uma sessão subsequente, ele deverá garantir que ele restaura apenas as informações de status obtidas do compressor ou descompactador que está usando no momento.</span><span class="sxs-lookup"><span data-stu-id="bb58f-115">Alternatively, if your application obtains the status from a compressor or decompressor and uses it to restore the status in a subsequent session, it must ensure that it restores only status information obtained from the compressor or decompressor it is currently using.</span></span>

 

 




