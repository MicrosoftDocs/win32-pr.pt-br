---
title: Configuração (multimídia do Windows)
description: Configuração
ms.assetid: d61d6c8b-8dba-45c2-ba99-0b2111a2d624
keywords:
- drivers instaláveis, configuração
- drivers instaláveis, DRV_CONFIGURE mensagem
- DRV_CONFIGURE mensagem
- DRV_QUERYCONFIGURE mensagem
- Mensagem DRVCONFIGINFO
- Configurando drivers instaláveis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20a248f992a857b88b723bd54c771f1af5709d97
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104008722"
---
# <a name="configuration-windows-multimedia"></a><span data-ttu-id="72a48-109">Configuração (multimídia do Windows)</span><span class="sxs-lookup"><span data-stu-id="72a48-109">Configuration (Windows Multimedia)</span></span>

<span data-ttu-id="72a48-110">Um driver instalável pode permitir que os usuários escolham as definições de configuração para o driver e o hardware associado exibindo uma caixa de diálogo de configuração ao processar a mensagem do [**drv \_ Configure**](drv-configure.md) .</span><span class="sxs-lookup"><span data-stu-id="72a48-110">An installable driver can let users choose configuration settings for the driver and associated hardware by displaying a configuration dialog box when processing the [**DRV\_CONFIGURE**](drv-configure.md) message.</span></span> <span data-ttu-id="72a48-111">O driver é responsável por criar e gerenciar a caixa de diálogo, processar qualquer entrada do usuário na caixa de diálogo e alterar a configuração do driver ou do hardware conforme solicitado pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="72a48-111">The driver is responsible for creating and managing the dialog box, processing any user input from the dialog box, and changing the configuration of the driver or hardware as requested by the user.</span></span> <span data-ttu-id="72a48-112">O driver deve fornecer um procedimento de caixa de diálogo separado para processar mensagens de janela para a caixa de diálogo e um modelo de caixa de diálogo para definir a aparência e o conteúdo da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="72a48-112">The driver must provide a separate dialog box procedure to process window messages for the dialog box and a dialog box template to define the appearance and content of the dialog box.</span></span>

<span data-ttu-id="72a48-113">Antes de receber a \_ mensagem de configuração de DRV, um driver recebe a mensagem [**\_ QUERYCONFIGURE drv**](drv-queryconfigure.md) .</span><span class="sxs-lookup"><span data-stu-id="72a48-113">Before receiving the DRV\_CONFIGURE message, a driver receives the [**DRV\_QUERYCONFIGURE**](drv-queryconfigure.md) message.</span></span> <span data-ttu-id="72a48-114">O driver deve retornar um valor diferente de zero para a consulta para garantir o recebimento da mensagem de configuração de DRV subsequente \_ .</span><span class="sxs-lookup"><span data-stu-id="72a48-114">The driver must return a nonzero value to the query to ensure receipt of the subsequent DRV\_CONFIGURE message.</span></span>

<span data-ttu-id="72a48-115">Ao inicializar a caixa de diálogo de configuração, o driver normalmente recupera as informações de configuração do registro.</span><span class="sxs-lookup"><span data-stu-id="72a48-115">When initializing the configuration dialog box, the driver typically retrieves configuration information from the registry.</span></span> <span data-ttu-id="72a48-116">Para ajudar a localizar essas informações, a \_ mensagem de configuração de drv normalmente inclui o endereço de uma estrutura [**DRVCONFIGINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-drvconfiginfo) que contém os nomes da chave do registro e o valor associado ao driver.</span><span class="sxs-lookup"><span data-stu-id="72a48-116">To help locate this information, the DRV\_CONFIGURE message usually includes the address of a [**DRVCONFIGINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-drvconfiginfo) structure that contains the names of the registry key and value associated with the driver.</span></span> <span data-ttu-id="72a48-117">Se o usuário solicitar alterações na configuração, o driver deverá atualizar as informações de configuração no registro.</span><span class="sxs-lookup"><span data-stu-id="72a48-117">If the user requests changes to the configuration, the driver should update the configuration information in the registry.</span></span>

 

 
