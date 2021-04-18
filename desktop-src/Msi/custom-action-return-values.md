---
description: Se a opção de processamento de retorno msidbCustomActionTypeContinue não estiver definida, a ação personalizada deverá retornar um código de status inteiro, conforme mostrado na tabela a seguir.
ms.assetid: 56c2d639-eef8-47cd-9d47-9a4781b9be36
title: Valores de retorno de ação personalizada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c01ba6273aea6cf950edb56ef3c2a94ab9a272d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105753271"
---
# <a name="custom-action-return-values"></a><span data-ttu-id="12965-103">Valores de retorno de ação personalizada</span><span class="sxs-lookup"><span data-stu-id="12965-103">Custom Action Return Values</span></span>

<span data-ttu-id="12965-104">Se a opção de processamento de retorno **msidbCustomActionTypeContinue** não estiver definida, a ação personalizada deverá retornar um código de status inteiro, conforme mostrado na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="12965-104">If the **msidbCustomActionTypeContinue** return processing option is not set, the custom action must return an integer status code as shown in the following table.</span></span>



| <span data-ttu-id="12965-105">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="12965-105">Return value</span></span>                 | <span data-ttu-id="12965-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="12965-106">Description</span></span>                           |
|------------------------------|---------------------------------------|
| <span data-ttu-id="12965-107">função de erro \_ \_ não \_ chamada</span><span class="sxs-lookup"><span data-stu-id="12965-107">ERROR\_FUNCTION\_NOT\_CALLED</span></span> | <span data-ttu-id="12965-108">Ação não executada.</span><span class="sxs-lookup"><span data-stu-id="12965-108">Action not executed.</span></span>                  |
| <span data-ttu-id="12965-109">êxito do erro \_</span><span class="sxs-lookup"><span data-stu-id="12965-109">ERROR\_SUCCESS</span></span>               | <span data-ttu-id="12965-110">Ações concluídas com êxito.</span><span class="sxs-lookup"><span data-stu-id="12965-110">Completed actions successfully.</span></span>       |
| <span data-ttu-id="12965-111">ERRO ao \_ instalar o \_ UserExit</span><span class="sxs-lookup"><span data-stu-id="12965-111">ERROR\_INSTALL\_USEREXIT</span></span>     | <span data-ttu-id="12965-112">O usuário terminou prematuramente.</span><span class="sxs-lookup"><span data-stu-id="12965-112">User terminated prematurely.</span></span>          |
| <span data-ttu-id="12965-113">\_falha na instalação do erro \_</span><span class="sxs-lookup"><span data-stu-id="12965-113">ERROR\_INSTALL\_FAILURE</span></span>      | <span data-ttu-id="12965-114">Ocorreu um erro irrecuperável.</span><span class="sxs-lookup"><span data-stu-id="12965-114">Unrecoverable error occurred.</span></span>         |
| <span data-ttu-id="12965-115">ERRO \_ não há \_ mais \_ itens</span><span class="sxs-lookup"><span data-stu-id="12965-115">ERROR\_NO\_MORE\_ITEMS</span></span>       | <span data-ttu-id="12965-116">Ignore as ações restantes, não um erro.</span><span class="sxs-lookup"><span data-stu-id="12965-116">Skip remaining actions, not an error.</span></span> |



 

<span data-ttu-id="12965-117">Observe que as ações personalizadas que são [arquivos executáveis](executable-files.md) devem retornar um valor de 0 para êxito.</span><span class="sxs-lookup"><span data-stu-id="12965-117">Note that custom actions that are [executable files](executable-files.md) must return a value of 0 for success.</span></span> <span data-ttu-id="12965-118">O instalador interpreta qualquer outro valor de retorno como falha.</span><span class="sxs-lookup"><span data-stu-id="12965-118">The installer interprets any other return value as failure.</span></span> <span data-ttu-id="12965-119">Para ignorar valores de retorno, defina o sinalizador de bit **msidbCustomActionTypeContinue** no campo Type da [tabela CustomAction](customaction-table.md).</span><span class="sxs-lookup"><span data-stu-id="12965-119">To ignore return values, set the **msidbCustomActionTypeContinue** bit flag in the Type field of the [CustomAction table](customaction-table.md).</span></span>

<span data-ttu-id="12965-120">Para obter mais informações sobre a opção **msidbCustomActionTypeContinue** e outras opções de processamento de retorno, consulte [Opções de processamento de retorno de ação personalizada](custom-action-return-processing-options.md).</span><span class="sxs-lookup"><span data-stu-id="12965-120">For more information about the **msidbCustomActionTypeContinue** option and other return processing options, see [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span>

<span data-ttu-id="12965-121">Observe que Windows Installer converte os valores de retorno de todas as ações quando grava o valor de retorno no arquivo de log.</span><span class="sxs-lookup"><span data-stu-id="12965-121">Note that Windows Installer translates the return values from all actions when it writes the return value into the log file.</span></span> <span data-ttu-id="12965-122">Por exemplo, se o valor de retorno da ação aparecer como 1 no arquivo de log, isso significa que a ação retornou êxito de erro \_ .</span><span class="sxs-lookup"><span data-stu-id="12965-122">For example, if the action return value appears as 1 in the log file, this means that the action returned ERROR\_SUCCESS.</span></span> <span data-ttu-id="12965-123">Para obter mais informações sobre essa conversão, consulte [log de valores de retorno de ação](logging-of-action-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="12965-123">For more information about this translation see [Logging of Action Return Values](logging-of-action-return-values.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="12965-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="12965-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="12965-125">Códigos de Erro</span><span class="sxs-lookup"><span data-stu-id="12965-125">Error Codes</span></span>](error-codes.md)
</dt> <dt>

[<span data-ttu-id="12965-126">Registro de valores de retorno de ação</span><span class="sxs-lookup"><span data-stu-id="12965-126">Logging of Action Return Values</span></span>](logging-of-action-return-values.md)
</dt> </dl>

 

 



