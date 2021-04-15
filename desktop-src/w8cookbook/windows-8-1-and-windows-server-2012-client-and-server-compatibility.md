---
title: Compatibilidade de cliente e servidor do Windows 8.1 e do Windows Server 2012 R2
description: Compatibilidade de cliente e servidor do Windows 8.1 e do Windows Server 2012 R2
ms.assetid: 45C37E2D-3513-4708-A562-1426D2B832F0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c46647dd9ad0f0baeae1ffb98905740a37f9530
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104498650"
---
# <a name="windows-81-and-windows-server-2012-r2-client-and-server-compatibility"></a><span data-ttu-id="9c4d6-103">Compatibilidade de cliente e servidor do Windows 8.1 e do Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="9c4d6-103">Windows 8.1 and Windows Server 2012 R2 client and server compatibility</span></span>

<span data-ttu-id="9c4d6-104">Esta seção descreve as alterações no sistema operacional que você deve prestar atenção especial devido aos possíveis impactos nos aplicativos existentes e como os novos aplicativos devem ser criados em clientes, em servidores ou em clientes e servidores.</span><span class="sxs-lookup"><span data-stu-id="9c4d6-104">This section describes changes in the operating system that you should pay special attention to due to the potential impacts on existing apps and how new apps should be designed on clients, on servers, or on both clients and servers.</span></span> <span data-ttu-id="9c4d6-105">A seguir está a lista de tópicos abordados nesta seção:</span><span class="sxs-lookup"><span data-stu-id="9c4d6-105">Following is the list of topics covered in this section:</span></span>

## <a name="in-this-section"></a><span data-ttu-id="9c4d6-106">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="9c4d6-106">In this section</span></span>



| <span data-ttu-id="9c4d6-107">Tópico</span><span class="sxs-lookup"><span data-stu-id="9c4d6-107">Topic</span></span>                                                                                                                                                                                                                         | <span data-ttu-id="9c4d6-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="9c4d6-108">Description</span></span> |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------|
| [<span data-ttu-id="9c4d6-109">Alterações de versão do sistema operacional no Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="9c4d6-109">Operating system version changes in Windows 8.1</span></span>](operating-system-version-changes-in-windows-8-1.md)<br/>                                                                                                             |             |
| [<span data-ttu-id="9c4d6-110">Componentes do Windows instalados sob demanda</span><span class="sxs-lookup"><span data-stu-id="9c4d6-110">Windows components installed on demand</span></span>](windows-components-installed-on-demand.md)<br/>                                                                                                                               |             |
| [<span data-ttu-id="9c4d6-111">Comportamento de fallback de fontes HTML</span><span class="sxs-lookup"><span data-stu-id="9c4d6-111">HTML font fallback behavior</span></span>](html-font-fallback-behavior.md)<br/>                                                                                                                                                     |             |
| [<span data-ttu-id="9c4d6-112">Windows 8.1 permite apenas URIs HTTPS, não URIs http</span><span class="sxs-lookup"><span data-stu-id="9c4d6-112">Windows 8.1 allows only https URIs, not http URIs</span></span>](windows-8-1-allows-only-https-uris--not-http-uris.md)<br/>                                                                                                         |             |
| [<span data-ttu-id="9c4d6-113">Entrada MouseWheel para Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="9c4d6-113">Mousewheel input for Windows 8.1</span></span>](mousewheel-input-for-windows-8-1.md)<br/>                                                                                                                                           |             |
| [<span data-ttu-id="9c4d6-114">Dispositivos Touchpad do Windows Precision</span><span class="sxs-lookup"><span data-stu-id="9c4d6-114">Windows precision touchpad devices</span></span>](windows-precision-touchpad-devices.md)<br/>                                                                                                                                       |             |
| [<span data-ttu-id="9c4d6-115">Alto DPI para aplicativos da área de trabalho no Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="9c4d6-115">High DPI for desktop apps in Windows 8.1</span></span>](high-dpi-for-desktop-apps-in-windows-8-1.md)<br/>                                                                                                                           |             |
| [<span data-ttu-id="9c4d6-116">A interface do usuário do Edge é suprimida em cenários de entrada e inércia</span><span class="sxs-lookup"><span data-stu-id="9c4d6-116">Edge UI is suppressed in  in-out-in  and  inertia  scenarios</span></span>](edge-ui-is-suppressed-in--in-out-in--and--inertia--scenarios.md)<br/>                                                                                   |             |
| [<span data-ttu-id="9c4d6-117">Não há suporte para a chamada de ImmSetConversionStatus () ou ImmGetConversionStatus () de aplicativos da Windows Store</span><span class="sxs-lookup"><span data-stu-id="9c4d6-117">Calling ImmSetConversionStatus() or ImmGetConversionStatus() from Windows Store apps is not supported</span></span>](calling-immsetconversionstatus---or-immgetconversionstatus---from-windows-store-apps-is-not-supported.md)<br/> |             |
| [<span data-ttu-id="9c4d6-118">O modelo de modo IME mudou de por usuário para por thread</span><span class="sxs-lookup"><span data-stu-id="9c4d6-118">IME mode model changed from per-user to per-thread</span></span>](ime-mode-model-changed-from-per-user-to-per-thread.md)<br/>                                                                                                       |             |
| [<span data-ttu-id="9c4d6-119">As APIs do Gerenciador de métodos de entrada não são suportadas pelo IME do chinês simplificado</span><span class="sxs-lookup"><span data-stu-id="9c4d6-119">Input Method manager APIs are not supported by Simplified Chinese IME</span></span>](input-method-manager-apis-are-not-supported-by-simplified-chinese-ime.md)<br/>                                                                 |             |
| [<span data-ttu-id="9c4d6-120">Alguns painéis de entrada de software do IME do leste asiático agora enviam vKey</span><span class="sxs-lookup"><span data-stu-id="9c4d6-120">Some East Asian IME software input panels now send vKey</span></span>](some-east-asian-ime-software-input-panels-now-send-vkey.md)<br/>                                                                                             |             |



 

 

 





