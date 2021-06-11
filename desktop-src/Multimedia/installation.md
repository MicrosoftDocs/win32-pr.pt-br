---
title: Instalação (Multimídia do Windows)
description: Saiba mais sobre a instalação de Multimídia do Windows, incluindo o processamento DRV_INSTALL e DRV_REMOVE mensagens.
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
ms.openlocfilehash: 29f82a23a781e62553d6488331b2c832104fd770
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989031"
---
# <a name="installation-windows-multimedia"></a><span data-ttu-id="ab5b3-110">Instalação (Multimídia do Windows)</span><span class="sxs-lookup"><span data-stu-id="ab5b3-110">Installation (Windows Multimedia)</span></span>

<span data-ttu-id="ab5b3-111">Um driver instalável pode executar tarefas de instalação específicas do driver ao processar as mensagens [**DRV \_ INSTALL**](drv-install.md) e [**DRV \_ REMOVE.**](drv-remove.md)</span><span class="sxs-lookup"><span data-stu-id="ab5b3-111">An installable driver can carry out driver-specific installation tasks when processing the [**DRV\_INSTALL**](drv-install.md) and [**DRV\_REMOVE**](drv-remove.md) messages.</span></span> <span data-ttu-id="ab5b3-112">Um aplicativo de instalação, como um Painel de Controle, envia as mensagens para o driver ao instalar ou remover o driver, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="ab5b3-112">An installation application, such as a Control Panel application, sends the messages to the driver when installing or removing the driver, respectively.</span></span>

<span data-ttu-id="ab5b3-113">Ao processar a mensagem DRV INSTALL, o driver normalmente verifica se o hardware necessário está presente e exibe a caixa de diálogo de configuração para permitir que o usuário escolha as definições de configuração iniciais para o driver e o \_ hardware associado.</span><span class="sxs-lookup"><span data-stu-id="ab5b3-113">When processing the DRV\_INSTALL message, the driver typically verifies that the required hardware is present and then displays the configuration dialog box to let the user choose the initial configuration settings for the driver and associated hardware.</span></span> <span data-ttu-id="ab5b3-114">A mensagem inclui o endereço de uma estrutura [**DRVCONFIGINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-drvconfiginfo) que contém os nomes da chave do Registro e o valor associados ao driver; o driver verifica o valor do Registro para obter informações de configuração padrão.</span><span class="sxs-lookup"><span data-stu-id="ab5b3-114">The message includes the address of a [**DRVCONFIGINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-drvconfiginfo) structure that contains the names of the registry key and value associated with the driver; the driver checks the registry value for default configuration information.</span></span> <span data-ttu-id="ab5b3-115">Por fim, o driver também cria quaisquer chaves e valores adicionais do Registro necessários para uma operação bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="ab5b3-115">Finally, the driver also creates any additional registry keys and values needed for successful operation.</span></span>

<span data-ttu-id="ab5b3-116">Ao processar a mensagem DRV REMOVE, o driver remove todas as chaves do Registro e \_ os valores que ele pode ter criado.</span><span class="sxs-lookup"><span data-stu-id="ab5b3-116">When processing the DRV\_REMOVE message, the driver removes any registry keys and values it may have created.</span></span>

 

 
