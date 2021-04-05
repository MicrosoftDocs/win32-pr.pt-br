---
description: Você pode optar por um computador no serviço de Microsoft Update e, em seguida, registrar esse serviço com Atualizações Automáticas.
ms.assetid: d6f3d8ca-3b7e-409c-87b6-db247b7b68e4
title: Opt-In Microsoft Update
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b149eb28024d77f66a08371827187adf05d4b78
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089932"
---
# <a name="opt-in-to-microsoft-update"></a><span data-ttu-id="f3559-103">Opt-In Microsoft Update</span><span class="sxs-lookup"><span data-stu-id="f3559-103">Opt-In to Microsoft Update</span></span>

<span data-ttu-id="f3559-104">Você pode optar por um computador no serviço de Microsoft Update e, em seguida, registrar esse serviço com Atualizações Automáticas.</span><span class="sxs-lookup"><span data-stu-id="f3559-104">You can opt a computer in to the Microsoft Update service and then register that service with Automatic Updates.</span></span>

<span data-ttu-id="f3559-105">O exemplo de script neste tópico mostra como usar o WUA (Windows Update Agent) para registrar o serviço de Microsoft Update com o Atualizações Automáticas.</span><span class="sxs-lookup"><span data-stu-id="f3559-105">The scripting sample in this topic shows you how to use Windows Update Agent (WUA) to register the Microsoft Update service with Automatic Updates.</span></span> <span data-ttu-id="f3559-106">Como alternativa, para registrar o serviço, o usuário pode visitar Microsoft Update.</span><span class="sxs-lookup"><span data-stu-id="f3559-106">Alternatively, to register the service, the user can visit Microsoft Update.</span></span>

<span data-ttu-id="f3559-107">Antes de tentar executar este exemplo, verifique se a versão do WUA que está instalada no computador é a versão 7.0.6000 ou uma versão posterior.</span><span class="sxs-lookup"><span data-stu-id="f3559-107">Before you attempt to run this sample, verify that the version of WUA that is installed on the computer is version 7.0.6000 or a later version.</span></span> <span data-ttu-id="f3559-108">Para obter mais informações sobre como determinar a versão do WUA que está instalada, consulte [determinando a versão atual do WUA](determining-the-current-version-of-wua.md).</span><span class="sxs-lookup"><span data-stu-id="f3559-108">For more information about how to determine the version of WUA that is installed, see [Determining the Current Version of WUA](determining-the-current-version-of-wua.md).</span></span>

## <a name="example"></a><span data-ttu-id="f3559-109">Exemplo</span><span class="sxs-lookup"><span data-stu-id="f3559-109">Example</span></span>

<span data-ttu-id="f3559-110">O exemplo de script a seguir mostra como usar o WUA (agente de Windows Update) para registrar o serviço de Microsoft Update com o Atualizações Automáticas.</span><span class="sxs-lookup"><span data-stu-id="f3559-110">The following scripting sample shows you how to use the Windows Update Agent (WUA) to register the Microsoft Update service with Automatic Updates.</span></span> <span data-ttu-id="f3559-111">O exemplo permite processamento adiado ou offline, se necessário.</span><span class="sxs-lookup"><span data-stu-id="f3559-111">The sample allows deferred or offline processing if needed.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f3559-112">Esse script destina-se a demonstrar o uso das APIs do agente de Windows Update e fornece um exemplo de como os desenvolvedores podem usar essas APIs para resolver problemas.</span><span class="sxs-lookup"><span data-stu-id="f3559-112">This script is intended to demonstrate the use of the Windows Update Agent APIs, and provide an example of how developers can use these APIs to solve problems.</span></span> <span data-ttu-id="f3559-113">Esse script não se destina como código de produção e o próprio script não tem suporte da Microsoft (embora haja suporte para as APIs de agente de Windows Update subjacentes).</span><span class="sxs-lookup"><span data-stu-id="f3559-113">This script is not intended as production code, and the script itself is not supported by Microsoft (though the underlying Windows Update Agent APIs are supported).</span></span>

 


```VB
Set ServiceManager = CreateObject("Microsoft.Update.ServiceManager")
ServiceManager.ClientApplicationID = "My App"

'add the Microsoft Update Service, GUID
Set NewUpdateService = ServiceManager.AddService2("7971f918-a847-4430-9279-4a52d1efe18d",7,"")

```



<span data-ttu-id="f3559-114">Em versões anteriores do WUA (uma versão mínima do WUA do 7.0.6000), você pode simplificar o processo de aceitação usando uma configuração do registro.</span><span class="sxs-lookup"><span data-stu-id="f3559-114">In earlier versions of WUA (a minimum WUA version of 7.0.6000), you can simplify the opt-in process by using a registry setting.</span></span> <span data-ttu-id="f3559-115">Depois que a chave e os valores do registro forem configurados, o Microsoft Update processo de aceitação ocorrerá na próxima vez que o WUA executar uma pesquisa.</span><span class="sxs-lookup"><span data-stu-id="f3559-115">After the registry key and values are configured, the Microsoft Update opt-in process occurs the next time WUA performs a search.</span></span> <span data-ttu-id="f3559-116">O processo de aceitação pode ser disparado por Atualizações Automáticas ou por um chamador de API.</span><span class="sxs-lookup"><span data-stu-id="f3559-116">The opt-in process may be triggered by Automatic Updates or by an API caller.</span></span>

<span data-ttu-id="f3559-117">Por exemplo, o caminho completo da chave do registro e os valores a serem definidos para o processo de aceitação são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="f3559-117">For example, the full path of the registry key and values to set for the opt-in process are as follows:</span></span>

<span data-ttu-id="f3559-118">**HKLM** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Windowsupdate** \\ **PendingServiceRegistration** \\ **7971f918-A847-4430-9279-4a52d1efe18d**</span><span class="sxs-lookup"><span data-stu-id="f3559-118">**HKLM**\\**Software**\\**Microsoft**\\**Windows**\\**CurrentVersion**\\**WindowsUpdate**\\**PendingServiceRegistration**\\**7971f918-a847-4430-9279-4a52d1efe18d**</span></span>

<span data-ttu-id="f3559-119">**ClientApplicationID** = meu aplicativo</span><span class="sxs-lookup"><span data-stu-id="f3559-119">**ClientApplicationID** = My App</span></span>

<span data-ttu-id="f3559-120">**RegisterWithAU** = 1</span><span class="sxs-lookup"><span data-stu-id="f3559-120">**RegisterWithAU** = 1</span></span>

> [!Note]
>
> <span data-ttu-id="f3559-121">A chave do registro é respeitada apenas quando o WUA é atualizado de uma versão anterior à versão 7.0.6000 para a versão 7.0.6000 ou para uma versão posterior.</span><span class="sxs-lookup"><span data-stu-id="f3559-121">The registry key is respected once only when WUA is updated from a version that is earlier than version 7.0.6000 to version 7.0.6000 or to a later version.</span></span> <span data-ttu-id="f3559-122">Recomendamos critério ao substituir valores de registro existentes, pois substituir os valores pode alterar o resultado de uma solicitação de registro de serviço anterior.</span><span class="sxs-lookup"><span data-stu-id="f3559-122">We recommend discretion when overwriting existing registry values because overwriting the values may change the result of an earlier service registration request.</span></span>
>
> <span data-ttu-id="f3559-123">A criação dessa chave do registro requer credenciais administrativas.</span><span class="sxs-lookup"><span data-stu-id="f3559-123">Creating this registry key requires administrative credentials.</span></span> <span data-ttu-id="f3559-124">Para o Windows Vista, o chamador deve criar a chave do registro em um processo elevado.</span><span class="sxs-lookup"><span data-stu-id="f3559-124">For Windows Vista, the caller must create the registry key in an elevated process.</span></span>

 

 

 



