---
title: Instalação (multimídia do Windows)
description: Instalação
ms.assetid: 1f0e23ad-4db7-4f32-98d9-e672370db559
keywords:
- drivers instaláveis, instalando
- drivers instaláveis, DRV_INSTALL mensagem
- drivers instaláveis, DRV_REMOVE mensagem
- DRV_INSTALL mensagem
- DRV_REMOVE mensagem
- Mensagem DRVCONFIGINFO
- instalando drivers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4ebebd090c7499698c59c325d1ac0d487902454
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104369103"
---
# <a name="installation-windows-multimedia"></a><span data-ttu-id="5e3b6-110">Instalação (multimídia do Windows)</span><span class="sxs-lookup"><span data-stu-id="5e3b6-110">Installation (Windows Multimedia)</span></span>

<span data-ttu-id="5e3b6-111">Um driver instalável pode executar tarefas de instalação específicas do driver ao processar a [**\_ instalação do drv**](drv-install.md) e [**\_ remover**](drv-remove.md) as mensagens.</span><span class="sxs-lookup"><span data-stu-id="5e3b6-111">An installable driver can carry out driver-specific installation tasks when processing the [**DRV\_INSTALL**](drv-install.md) and [**DRV\_REMOVE**](drv-remove.md) messages.</span></span> <span data-ttu-id="5e3b6-112">Um aplicativo de instalação, como um aplicativo do painel de controle, envia as mensagens ao driver ao instalar ou remover o driver, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="5e3b6-112">An installation application, such as a Control Panel application, sends the messages to the driver when installing or removing the driver, respectively.</span></span>

<span data-ttu-id="5e3b6-113">Ao processar a mensagem de instalação do DRV \_ , o driver normalmente verifica se o hardware necessário está presente e, em seguida, exibe a caixa de diálogo configuração para permitir que o usuário escolha as definições de configuração inicial para o driver e o hardware associado.</span><span class="sxs-lookup"><span data-stu-id="5e3b6-113">When processing the DRV\_INSTALL message, the driver typically verifies that the required hardware is present and then displays the configuration dialog box to let the user choose the initial configuration settings for the driver and associated hardware.</span></span> <span data-ttu-id="5e3b6-114">A mensagem inclui o endereço de uma estrutura [**DRVCONFIGINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-drvconfiginfo) que contém os nomes da chave do registro e o valor associado ao driver; o driver verifica o valor do registro para obter informações de configuração padrão.</span><span class="sxs-lookup"><span data-stu-id="5e3b6-114">The message includes the address of a [**DRVCONFIGINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-drvconfiginfo) structure that contains the names of the registry key and value associated with the driver; the driver checks the registry value for default configuration information.</span></span> <span data-ttu-id="5e3b6-115">Por fim, o driver também cria quaisquer chaves de registro e valores adicionais necessários para uma operação bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="5e3b6-115">Finally, the driver also creates any additional registry keys and values needed for successful operation.</span></span>

<span data-ttu-id="5e3b6-116">Ao processar a mensagem de remoção de DRV \_ , o driver remove as chaves e os valores do registro que ele pode ter criado.</span><span class="sxs-lookup"><span data-stu-id="5e3b6-116">When processing the DRV\_REMOVE message, the driver removes any registry keys and values it may have created.</span></span>

 

 
