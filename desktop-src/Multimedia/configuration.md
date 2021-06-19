---
title: Configuração (Multimídia do Windows)
description: Saiba como um driver multimídia do Windows pode permitir que os usuários escolham definições de configuração exibindo uma caixa de diálogo de configuração.
ms.assetid: d61d6c8b-8dba-45c2-ba99-0b2111a2d624
keywords:
- drivers instaláveis, configuração
- drivers instaláveis, DRV_CONFIGURE mensagem
- DRV_CONFIGURE mensagem
- DRV_QUERYCONFIGURE mensagem
- Mensagem DRVCONFIGINFO
- configurando drivers instaláveis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7804e4d92d30d666d4d28c253a1a44572a707daa
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112403919"
---
# <a name="configuration-windows-multimedia"></a><span data-ttu-id="f4063-109">Configuração (Multimídia do Windows)</span><span class="sxs-lookup"><span data-stu-id="f4063-109">Configuration (Windows Multimedia)</span></span>

<span data-ttu-id="f4063-110">Um driver instalável pode permitir que os usuários escolham definições de configuração para o driver e o hardware associado exibindo uma caixa de diálogo de configuração ao processar a mensagem [**DRV \_ CONFIGURE.**](drv-configure.md)</span><span class="sxs-lookup"><span data-stu-id="f4063-110">An installable driver can let users choose configuration settings for the driver and associated hardware by displaying a configuration dialog box when processing the [**DRV\_CONFIGURE**](drv-configure.md) message.</span></span> <span data-ttu-id="f4063-111">O driver é responsável por criar e gerenciar a caixa de diálogo, processar qualquer entrada do usuário na caixa de diálogo e alterar a configuração do driver ou hardware conforme solicitado pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="f4063-111">The driver is responsible for creating and managing the dialog box, processing any user input from the dialog box, and changing the configuration of the driver or hardware as requested by the user.</span></span> <span data-ttu-id="f4063-112">O driver deve fornecer um procedimento de caixa de diálogo separado para processar mensagens de janela para a caixa de diálogo e um modelo de caixa de diálogo para definir a aparência e o conteúdo da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="f4063-112">The driver must provide a separate dialog box procedure to process window messages for the dialog box and a dialog box template to define the appearance and content of the dialog box.</span></span>

<span data-ttu-id="f4063-113">Antes de receber a mensagem \_ DRV CONFIGURE, um driver recebe a [**mensagem \_ DRV QUERYCONFIGURE.**](drv-queryconfigure.md)</span><span class="sxs-lookup"><span data-stu-id="f4063-113">Before receiving the DRV\_CONFIGURE message, a driver receives the [**DRV\_QUERYCONFIGURE**](drv-queryconfigure.md) message.</span></span> <span data-ttu-id="f4063-114">O driver deve retornar um valor que não seja zero para a consulta para garantir o recebimento da mensagem DRV \_ CONFIGURE subsequente.</span><span class="sxs-lookup"><span data-stu-id="f4063-114">The driver must return a nonzero value to the query to ensure receipt of the subsequent DRV\_CONFIGURE message.</span></span>

<span data-ttu-id="f4063-115">Ao inicializar a caixa de diálogo de configuração, o driver normalmente recupera informações de configuração do Registro.</span><span class="sxs-lookup"><span data-stu-id="f4063-115">When initializing the configuration dialog box, the driver typically retrieves configuration information from the registry.</span></span> <span data-ttu-id="f4063-116">Para ajudar a localizar essas informações, a mensagem DRV CONFIGURE geralmente inclui o endereço de uma estrutura \_ [**DRVCONFIGINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-drvconfiginfo) que contém os nomes da chave do Registro e o valor associados ao driver.</span><span class="sxs-lookup"><span data-stu-id="f4063-116">To help locate this information, the DRV\_CONFIGURE message usually includes the address of a [**DRVCONFIGINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-drvconfiginfo) structure that contains the names of the registry key and value associated with the driver.</span></span> <span data-ttu-id="f4063-117">Se o usuário solicitar alterações na configuração, o driver deverá atualizar as informações de configuração no Registro.</span><span class="sxs-lookup"><span data-stu-id="f4063-117">If the user requests changes to the configuration, the driver should update the configuration information in the registry.</span></span>

 

 
