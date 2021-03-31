---
title: Funções e mensagens de driver instaláveis
description: Funções e mensagens de driver instaláveis
ms.assetid: f487705a-ae8e-4ea8-bfd5-9b0f6087ddbb
keywords:
- drivers instaláveis, funções
- drivers instaláveis, mensagens
- drivers instaláveis, função OpenDriver
- Função OpenDriver
- drivers instaláveis, mensagens personalizadas
- mensagens do driver
- mensagens de driver personalizado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c66e6ebaac73bf8eb779119750cb390481152c3f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103917264"
---
# <a name="installable-driver-functions-and-messages"></a><span data-ttu-id="e8523-110">Funções e mensagens de driver instaláveis</span><span class="sxs-lookup"><span data-stu-id="e8523-110">Installable Driver Functions and Messages</span></span>

<span data-ttu-id="e8523-111">Você pode abrir um driver instalável de um aplicativo usando a função [**OpenDriver**](/windows/win32/api/mmiscapi/nf-mmiscapi-opendriver) .</span><span class="sxs-lookup"><span data-stu-id="e8523-111">You can open an installable driver from an application by using the [**OpenDriver**](/windows/win32/api/mmiscapi/nf-mmiscapi-opendriver) function.</span></span> <span data-ttu-id="e8523-112">Essa função cria uma instância do driver, carregando o driver na memória se nenhuma outra instância existir e retorna o identificador da nova instância.</span><span class="sxs-lookup"><span data-stu-id="e8523-112">This function creates an instance of the driver, loading the driver into memory if no other instance exists, and returns the handle of the new instance.</span></span> <span data-ttu-id="e8523-113">Ao abrir um driver instalável, você deve fornecer o caminho completo do driver ou os nomes da chave do registro e o valor associado ao driver.</span><span class="sxs-lookup"><span data-stu-id="e8523-113">When opening an installable driver, you must supply either the full path of the driver or the names of the registry key and value associated with the driver.</span></span>

<span data-ttu-id="e8523-114">Quando um driver estiver aberto, você poderá direcioná-lo para executar tarefas usando a função [**SendDriverMessage**](/windows/win32/api/mmiscapi/nf-mmiscapi-senddrivermessage) para enviar mensagens de driver ao driver.</span><span class="sxs-lookup"><span data-stu-id="e8523-114">Once a driver is open, you can direct it to carry out tasks by using the [**SendDriverMessage**](/windows/win32/api/mmiscapi/nf-mmiscapi-senddrivermessage) function to send driver messages to the driver.</span></span> <span data-ttu-id="e8523-115">Por exemplo, você pode direcionar o driver para exibir sua caixa de diálogo de configuração enviando a mensagem de [**\_ Configurar drv**](drv-configure.md) .</span><span class="sxs-lookup"><span data-stu-id="e8523-115">For example, you can direct the driver to display its configuration dialog box by sending the [**DRV\_CONFIGURE**](drv-configure.md) message.</span></span> <span data-ttu-id="e8523-116">Antes de enviar essa mensagem, você deve determinar se o driver tem uma caixa de diálogo de configuração enviando a mensagem [**\_ QUERYCONFIGURE drv**](drv-queryconfigure.md) e verificando um valor de retorno diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="e8523-116">Before sending this message, you must determine whether the driver has a configuration dialog box by sending the [**DRV\_QUERYCONFIGURE**](drv-queryconfigure.md) message and checking for a nonzero return value.</span></span> <span data-ttu-id="e8523-117">Muitos drivers fornecem um conjunto de mensagens personalizadas que você pode enviar para direcionar as operações do driver.</span><span class="sxs-lookup"><span data-stu-id="e8523-117">Many drivers provide a set of custom messages that you can send to direct the operations of the driver.</span></span>

<span data-ttu-id="e8523-118">Se você precisar de acesso especial a um driver instalável, como o acesso a seus recursos, poderá recuperar o identificador de módulo do driver usando a função [**GetDriverModuleHandle**](/windows/win32/api/mmiscapi/nf-mmiscapi-getdrivermodulehandle) .</span><span class="sxs-lookup"><span data-stu-id="e8523-118">If you need special access to an installable driver, such as access to its resources, you can retrieve the module handle of the driver by using the [**GetDriverModuleHandle**](/windows/win32/api/mmiscapi/nf-mmiscapi-getdrivermodulehandle) function.</span></span>

<span data-ttu-id="e8523-119">Quando você não precisar mais do driver instalável, poderá fechá-lo usando a função [**CloseDriver**](/windows/win32/api/mmiscapi/nf-mmiscapi-closedriver) .</span><span class="sxs-lookup"><span data-stu-id="e8523-119">When you no longer need the installable driver, you can close it by using the [**CloseDriver**](/windows/win32/api/mmiscapi/nf-mmiscapi-closedriver) function.</span></span>

<span data-ttu-id="e8523-120">Você pode usar as funções e mensagens de driver instaláveis para abrir e gerenciar qualquer driver instalável.</span><span class="sxs-lookup"><span data-stu-id="e8523-120">You can use the installable driver functions and messages to open and manage any installable driver.</span></span> <span data-ttu-id="e8523-121">No entanto, o curso recomendado de ação para abrir e gerenciar dispositivos multimídia é primeiro usar os serviços padrão (como [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen), [**waveOutMessage**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutmessage)e [**waveOutClose**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutclose) para dispositivos de saída de forma de onda), se existirem.</span><span class="sxs-lookup"><span data-stu-id="e8523-121">However, the recommended course of action for opening and managing multimedia devices is to first use standard services (such as [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen), [**waveOutMessage**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutmessage), and [**waveOutClose**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutclose) for waveform output devices), if they exist.</span></span> <span data-ttu-id="e8523-122">Se os serviços padrão não existirem para um driver de multimídia, abra e gerencie o driver usando as funções e mensagens de driver instaláveis.</span><span class="sxs-lookup"><span data-stu-id="e8523-122">If standard services do not exist for a multimedia driver, then open and manage the driver using the installable driver functions and messages.</span></span>

> [!Note]  
> <span data-ttu-id="e8523-123">As funções [**SendDriverMessage**](/windows/win32/api/mmiscapi/nf-mmiscapi-senddrivermessage) e [**GetDriverModuleHandle**](/windows/win32/api/mmiscapi/nf-mmiscapi-getdrivermodulehandle) são as funções preferenciais a serem usadas para enviar mensagens a um driver e para obter um identificador para uma instância de módulo.</span><span class="sxs-lookup"><span data-stu-id="e8523-123">The [**SendDriverMessage**](/windows/win32/api/mmiscapi/nf-mmiscapi-senddrivermessage) and [**GetDriverModuleHandle**](/windows/win32/api/mmiscapi/nf-mmiscapi-getdrivermodulehandle) functions are the preferred functions to use to send messages to a driver and to obtain a handle to a module instance.</span></span> <span data-ttu-id="e8523-124">No entanto, a função [**DrvGetModuleHandle**](/windows/win32/api/mmiscapi/nf-mmiscapi-drvgetmodulehandle) mais antiga foi incluída para manter a compatibilidade com as versões anteriores do sistema operacional Windows.</span><span class="sxs-lookup"><span data-stu-id="e8523-124">The older [**DrvGetModuleHandle**](/windows/win32/api/mmiscapi/nf-mmiscapi-drvgetmodulehandle) function, however, has been included to maintain compatibility with previous versions of the Windows operating system.</span></span>

 

 

 