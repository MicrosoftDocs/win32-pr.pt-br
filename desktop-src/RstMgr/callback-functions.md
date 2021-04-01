---
title: Iniciar funções de retorno de chamada do Gerenciador
description: A API do Gerenciador de reinicialização usa as funções de retorno de chamada na tabela a seguir.
ms.assetid: abb78aa5-0487-4e99-85b6-adc38b600c09
keywords:
- Restart Manager Restart Mgr, referência, funções de retorno de chamada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44c850dd805aeff664e3e09292825e342a6c5603
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641667"
---
# <a name="restart-manager-callback-functions"></a><span data-ttu-id="e5d2a-104">Iniciar funções de retorno de chamada do Gerenciador</span><span class="sxs-lookup"><span data-stu-id="e5d2a-104">Restart Manager Callback Functions</span></span>

<span data-ttu-id="e5d2a-105">A API do Gerenciador de reinicialização usa as funções de retorno de chamada na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="e5d2a-105">The Restart Manager API uses the callback functions in the following table.</span></span>



| <span data-ttu-id="e5d2a-106">Função de retorno da chamada</span><span class="sxs-lookup"><span data-stu-id="e5d2a-106">Callback Function</span></span>                                               | <span data-ttu-id="e5d2a-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="e5d2a-107">Description</span></span>                                                                                                                                                            |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e5d2a-108">**\_retorno de \_ chamada de status de gravação do RM \_**</span><span class="sxs-lookup"><span data-stu-id="e5d2a-108">**RM\_WRITE\_STATUS\_CALLBACK**</span></span>](/windows/win32/api/restartmanager/nc-restartmanager-rm_write_status_callback) | <span data-ttu-id="e5d2a-109">O aplicativo que iniciou a sessão do Gerenciador de reinicialização pode passar um ponteiro para essa função para as funções do Gerenciador de reinicialização para receber uma porcentagem de integridade.</span><span class="sxs-lookup"><span data-stu-id="e5d2a-109">The application that started the Restart Manager session can pass a pointer to this function to the Restart Manager functions to receive a percentage of completeness.</span></span> |



 

 

 