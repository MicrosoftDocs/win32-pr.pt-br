---
description: Personalize o comportamento do Winlogon implementando um provedor de credenciais.
ms.assetid: 70b47e29-c755-4c59-a493-d7fcbbc94b83
title: Personalizando o Winlogon
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b64da4baae9b52dd53e288c631f35d33ea5a3085
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105750506"
---
# <a name="customizing-winlogon"></a><span data-ttu-id="56cc0-103">Personalizando o Winlogon</span><span class="sxs-lookup"><span data-stu-id="56cc0-103">Customizing Winlogon</span></span>

<span data-ttu-id="56cc0-104">Personalize o comportamento do [*Winlogon*](/windows/desktop/SecGloss/w-gly) implementando um provedor de credenciais.</span><span class="sxs-lookup"><span data-stu-id="56cc0-104">Customize [*Winlogon*](/windows/desktop/SecGloss/w-gly) behavior by implementing a Credential Provider.</span></span> <span data-ttu-id="56cc0-105">Para obter informações sobre provedores de credenciais, consulte [**interface ICredentialProvider**](/windows/win32/api/credentialprovider/nn-credentialprovider-icredentialprovider).</span><span class="sxs-lookup"><span data-stu-id="56cc0-105">For information about Credential Providers, see [**ICredentialProvider Interface**](/windows/win32/api/credentialprovider/nn-credentialprovider-icredentialprovider).</span></span>

<span data-ttu-id="56cc0-106">**Windows Server 2003 e Windows XP:** Não há suporte para provedores de credenciais.</span><span class="sxs-lookup"><span data-stu-id="56cc0-106">**Windows Server 2003 and Windows XP:** Credential Providers are not supported.</span></span>

<span data-ttu-id="56cc0-107">As seções a seguir descrevem maneiras de personalizar o Winlogon em versões do Windows anteriores ao Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="56cc0-107">The following sections describe ways to customize Winlogon in Windows versions prior to Windows Vista.</span></span>

> [!Note]  
> <span data-ttu-id="56cc0-108">As DLLs GINAs e os pacotes de notificação Winlogon são ignorados no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="56cc0-108">GINA DLLs and Winlogon notification packages are ignored in Windows Vista.</span></span>

 

-   [<span data-ttu-id="56cc0-109">Pacotes de notificação do Winlogon</span><span class="sxs-lookup"><span data-stu-id="56cc0-109">Winlogon Notification Packages</span></span>](#winlogon-notification-packages)
-   [<span data-ttu-id="56cc0-110">Stubs GINA</span><span class="sxs-lookup"><span data-stu-id="56cc0-110">GINA Stubs</span></span>](#gina-stubs)
-   [<span data-ttu-id="56cc0-111">Ganchos GINA</span><span class="sxs-lookup"><span data-stu-id="56cc0-111">GINA Hooks</span></span>](#gina-hooks)

## <a name="winlogon-notification-packages"></a><span data-ttu-id="56cc0-112">Pacotes de notificação do Winlogon</span><span class="sxs-lookup"><span data-stu-id="56cc0-112">Winlogon Notification Packages</span></span>

<span data-ttu-id="56cc0-113">Um pacote de notificação do Winlogon é uma DLL que exporta funções que manipulam eventos do Winlogon.</span><span class="sxs-lookup"><span data-stu-id="56cc0-113">A Winlogon notification package is a DLL that exports functions that handle Winlogon events.</span></span> <span data-ttu-id="56cc0-114">Por exemplo, quando um usuário faz logon no sistema, o Winlogon chama cada pacote de notificação para fornecer informações sobre o evento.</span><span class="sxs-lookup"><span data-stu-id="56cc0-114">For example, when a user logs onto the system, Winlogon calls each notification package to provide information about the event.</span></span> <span data-ttu-id="56cc0-115">Para obter mais informações, consulte [pacotes de notificação do Winlogon](winlogon-notification-packages.md).</span><span class="sxs-lookup"><span data-stu-id="56cc0-115">For more information, see [Winlogon Notification Packages](winlogon-notification-packages.md).</span></span>

## <a name="gina-stubs"></a><span data-ttu-id="56cc0-116">Stubs GINA</span><span class="sxs-lookup"><span data-stu-id="56cc0-116">GINA Stubs</span></span>

<span data-ttu-id="56cc0-117">Um stub [*Gina*](/windows/desktop/SecGloss/g-gly) é uma DLL Gina personalizada que usa as implementações de função de exportação de uma DLL Gina instalada anteriormente (normalmente MsGina.dll).</span><span class="sxs-lookup"><span data-stu-id="56cc0-117">A [*GINA*](/windows/desktop/SecGloss/g-gly) stub is a custom GINA DLL that uses the export function implementations of a previously installed GINA DLL (typically MsGina.dll).</span></span> <span data-ttu-id="56cc0-118">Um stub GINA Obtém ponteiros para cada função exportada pela DLL GINA instalada anteriormente.</span><span class="sxs-lookup"><span data-stu-id="56cc0-118">A GINA stub gets pointers to each function exported by the previously installed GINA DLL.</span></span> <span data-ttu-id="56cc0-119">Cada função de stub da GINA usa o ponteiro de função apropriado para chamar a função correspondente na DLL GINA instalada anteriormente.</span><span class="sxs-lookup"><span data-stu-id="56cc0-119">Each GINA stub function then uses the appropriate function pointer to call the corresponding function in the previously installed GINA DLL.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="56cc0-120">Cada função de stub GINA deve chamar a função correspondente na GINA instalada anteriormente.</span><span class="sxs-lookup"><span data-stu-id="56cc0-120">Each GINA stub function must call the corresponding function in the previously installed GINA.</span></span>

 

<span data-ttu-id="56cc0-121">Uma função de stub GINA pode implementar funcionalidade adicional em uma ou mais de suas funções de exportação.</span><span class="sxs-lookup"><span data-stu-id="56cc0-121">A GINA stub function can implement additional functionality in one or more of its export functions.</span></span> <span data-ttu-id="56cc0-122">Por exemplo, a função [**WlxLoggedOutSAS**](/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedoutsas) de um stub Gina pode verificar a hora atual antes de chamar a função **WlxLoggedOutSAS** do MsGina.dll.</span><span class="sxs-lookup"><span data-stu-id="56cc0-122">For example, the [**WlxLoggedOutSAS**](/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedoutsas) function of a GINA stub might check the current time before calling the **WlxLoggedOutSAS** function of the MsGina.dll.</span></span> <span data-ttu-id="56cc0-123">Se a hora atual estiver dentro de um intervalo específico, a função de stub poderá exibir uma mensagem indicando que o logon não é permitido durante esse período de tempo e retornará a **\_ ação de SAS WLX \_ \_ None** para o Winlogon.</span><span class="sxs-lookup"><span data-stu-id="56cc0-123">If the current time was within a specific range, the stub function could display a message that indicates logon is disallowed during that time period and return **WLX\_SAS\_ACTION\_NONE** to Winlogon.</span></span> <span data-ttu-id="56cc0-124">A função **WlxLoggedOutSAS** da MsGina.dll seria então chamada somente durante o período de tempo permitido.</span><span class="sxs-lookup"><span data-stu-id="56cc0-124">The **WlxLoggedOutSAS** function of the MsGina.dll would then be called only during the allowed time period.</span></span>

<span data-ttu-id="56cc0-125">O aplicativo stub GINA Obtém uma tabela de expedição para funções de suporte do Winlogon por meio do parâmetro *pWinlogonFunctions* da função [**WlxInitialize**](/windows/desktop/api/Winwlx/nf-winwlx-wlxinitialize) .</span><span class="sxs-lookup"><span data-stu-id="56cc0-125">The GINA stub application gets a dispatch table to Winlogon support functions through the *pWinlogonFunctions* parameter of the [**WlxInitialize**](/windows/desktop/api/Winwlx/nf-winwlx-wlxinitialize) function.</span></span> <span data-ttu-id="56cc0-126">O aplicativo stub GINA pode usar essa tabela de expedição para chamar funções de suporte do Winlogon.</span><span class="sxs-lookup"><span data-stu-id="56cc0-126">The GINA stub application can use this dispatch table to call Winlogon support functions.</span></span> <span data-ttu-id="56cc0-127">Por exemplo, um aplicativo stub GINA pode chamar a função [**WlxSasNotify**](/windows/win32/api/winwlx/nc-winwlx-pwlx_sas_notify) para causar um evento de [*sequência de atenção segura*](/windows/desktop/SecGloss/s-gly) (SAS) quando um [*cartão inteligente*](/windows/desktop/SecGloss/s-gly) é inserido em um [*leitor*](/windows/desktop/SecGloss/r-gly).</span><span class="sxs-lookup"><span data-stu-id="56cc0-127">For example, A GINA stub application can call the [**WlxSasNotify**](/windows/win32/api/winwlx/nc-winwlx-pwlx_sas_notify) function to cause a [*secure attention sequence*](/windows/desktop/SecGloss/s-gly) (SAS) event when a [*smart card*](/windows/desktop/SecGloss/s-gly) is inserted into a [*reader*](/windows/desktop/SecGloss/r-gly).</span></span>

<span data-ttu-id="56cc0-128">Para obter mais informações sobre como criar um stub GINA, consulte o exemplo stubs da Gina no \\ diretório Samples \\ Security \\ Gina \\ GinaStub de uma instalação do SDK (Software Development Kit) da plataforma.</span><span class="sxs-lookup"><span data-stu-id="56cc0-128">For more information about creating a GINA stub, see the Gina Stubs sample in the \\Samples\\Security\\Gina\\GinaStub directory of a Platform Software Development Kit (SDK) installation.</span></span>

> [!Note]  
> <span data-ttu-id="56cc0-129">Todas as chamadas entre uma GINA e Winlogon devem estar dentro de um único thread.</span><span class="sxs-lookup"><span data-stu-id="56cc0-129">All calls between a GINA and Winlogon must be within a single thread.</span></span>

 

## <a name="gina-hooks"></a><span data-ttu-id="56cc0-130">Ganchos GINA</span><span class="sxs-lookup"><span data-stu-id="56cc0-130">GINA Hooks</span></span>

<span data-ttu-id="56cc0-131">Um gancho GINA é um stub GINA que, em sua implementação da função [**WlxInitialize**](/windows/desktop/api/Winwlx/nf-winwlx-wlxinitialize) , substitui o ponteiro para a função de suporte [**WlxDialogBoxParam**](/windows/win32/api/winwlx/nc-winwlx-pwlx_dialog_box_param) na tabela de expedição com um ponteiro para sua própria implementação da função **WlxDialogBoxParam** .</span><span class="sxs-lookup"><span data-stu-id="56cc0-131">A GINA hook is a GINA stub that, in its implementation of the [**WlxInitialize**](/windows/desktop/api/Winwlx/nf-winwlx-wlxinitialize) function, replaces the pointer to the [**WlxDialogBoxParam**](/windows/win32/api/winwlx/nc-winwlx-pwlx_dialog_box_param) support function in the dispatch table with a pointer to its own implementation of the **WlxDialogBoxParam** function.</span></span> <span data-ttu-id="56cc0-132">Como resultado, cada vez que a GINA (normalmente MsGina.dll) instalada anteriormente chama a função **WlxDialogBoxParam** , a função implementada pelo gancho Gina é chamada.</span><span class="sxs-lookup"><span data-stu-id="56cc0-132">As a result, each time the previously installed GINA (typically MsGina.dll) calls the **WlxDialogBoxParam** function, the function implemented by the GINA hook is called.</span></span>

<span data-ttu-id="56cc0-133">A função [**WlxDialogBoxParam**](/windows/win32/api/winwlx/nc-winwlx-pwlx_dialog_box_param) implementada pelo gancho Gina pode substituir o procedimento de retorno de chamada [**DialogProc**](/windows/win32/api/winuser/nc-winuser-dlgproc) que responde a um evento de caixa de diálogo específico.</span><span class="sxs-lookup"><span data-stu-id="56cc0-133">The [**WlxDialogBoxParam**](/windows/win32/api/winwlx/nc-winwlx-pwlx_dialog_box_param) function implemented by the GINA hook can replace the [**DialogProc**](/windows/win32/api/winuser/nc-winuser-dlgproc) callback procedure that responds to a specific dialog box event.</span></span>

<span data-ttu-id="56cc0-134">Isso dá ao gancho GINA controle total sobre a aparência e o comportamento de todas as caixas de diálogo que MsGina.dll cria.</span><span class="sxs-lookup"><span data-stu-id="56cc0-134">This gives the GINA hook full control over the appearance and behavior of all of the dialog boxes that MsGina.dll creates.</span></span>

<span data-ttu-id="56cc0-135">Para obter mais informações sobre como criar um gancho GINA, consulte o exemplo de ganchos Gina no \\ diretório Samples \\ Security \\ Gina \\ GinaHook de uma instalação do Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="56cc0-135">For more information about creating a GINA hook, see the Gina Hooks sample in the \\Samples\\Security\\Gina\\GinaHook directory of a Platform SDK installation.</span></span>

> [!Note]  
> <span data-ttu-id="56cc0-136">Todas as chamadas entre uma GINA e Winlogon devem estar dentro de um único thread.</span><span class="sxs-lookup"><span data-stu-id="56cc0-136">All calls between a GINA and Winlogon must be within a single thread.</span></span>

 

 

 
