---
description: A plataforma de sensor e localização do Windows inclui configurações de privacidade para ajudar a proteger as informações pessoais dos usuários.
ms.assetid: 24425ed2-7b94-4b05-b117-9118d2074f49
title: Privacidade e segurança na plataforma de sensor e localização do Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cb0bf50cd27de1fc7fd4f42bd7a8455a549eea3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105811282"
---
# <a name="privacy-and-security-in-the-windows-sensor-and-location-platform"></a><span data-ttu-id="0b4ca-103">Privacidade e segurança na plataforma de sensor e localização do Windows</span><span class="sxs-lookup"><span data-stu-id="0b4ca-103">Privacy and Security in the Windows Sensor and Location Platform</span></span>

<span data-ttu-id="0b4ca-104">A plataforma de sensor e localização do Windows inclui configurações de privacidade para ajudar a proteger as informações pessoais dos usuários.</span><span class="sxs-lookup"><span data-stu-id="0b4ca-104">The Windows Sensor and Location platform includes privacy settings to help protect users' personal information.</span></span>

<span data-ttu-id="0b4ca-105">A plataforma ajuda a garantir que os dados do sensor permaneçam privados, quando a privacidade é necessária, das seguintes maneiras:</span><span class="sxs-lookup"><span data-stu-id="0b4ca-105">The platform helps to ensure that sensor data remains private, when privacy is required, in the following ways:</span></span>

-   <span data-ttu-id="0b4ca-106">Por padrão, os sensores estão desativados.</span><span class="sxs-lookup"><span data-stu-id="0b4ca-106">By default, sensors are off.</span></span> <span data-ttu-id="0b4ca-107">Como o design da plataforma presume que qualquer sensor possa fornecer dados pessoais, cada sensor é desabilitado até que o usuário forneça consentimento explícito para acessar os dados do sensor.</span><span class="sxs-lookup"><span data-stu-id="0b4ca-107">Because the platform design presumes that any sensor can provide personal data, each sensor is disabled until the user provides explicit consent to access the sensor data.</span></span>
-   <span data-ttu-id="0b4ca-108">O Windows fornece mensagens de divulgação e conteúdo de ajuda para o usuário.</span><span class="sxs-lookup"><span data-stu-id="0b4ca-108">Windows provides disclosure messages and Help content for the user.</span></span> <span data-ttu-id="0b4ca-109">Esse conteúdo ajuda os usuários a entender como os sensores podem afetar a privacidade de seus dados pessoais e ajuda os usuários a tomar decisões informadas.</span><span class="sxs-lookup"><span data-stu-id="0b4ca-109">This content helps users understand how sensors can affect the privacy of their personal data and helps users make informed decisions.</span></span>
-   <span data-ttu-id="0b4ca-110">O fornecimento de permissão para um sensor requer direitos de administrador.</span><span class="sxs-lookup"><span data-stu-id="0b4ca-110">Providing permission for a sensor requires administrator rights.</span></span>
-   <span data-ttu-id="0b4ca-111">Quando habilitado, um dispositivo de sensor funciona para todos os programas em execução em uma conta de usuário específica (ou para todas as contas de usuário).</span><span class="sxs-lookup"><span data-stu-id="0b4ca-111">When it is enabled, a sensor device works for all programs running under a particular user account (or for all user accounts).</span></span> <span data-ttu-id="0b4ca-112">Isso inclui usuários e serviços não interativos, como ASPNET ou SYSTEM.</span><span class="sxs-lookup"><span data-stu-id="0b4ca-112">This includes noninteractive users and services, such as ASPNET or SYSTEM.</span></span> <span data-ttu-id="0b4ca-113">Por exemplo, se você habilitar um sensor de GPS para sua conta de usuário, somente os programas em execução na sua conta de usuário terão acesso ao GPS.</span><span class="sxs-lookup"><span data-stu-id="0b4ca-113">For example, if you enable a GPS sensor for your user account, only programs running under your user account have access to the GPS.</span></span> <span data-ttu-id="0b4ca-114">Se você habilitar o GPS para todos os usuários, qualquer programa em execução em qualquer conta de usuário terá acesso ao GPS.</span><span class="sxs-lookup"><span data-stu-id="0b4ca-114">If you enable the GPS for all users, any program running under any user account has access to the GPS.</span></span>
-   <span data-ttu-id="0b4ca-115">Os programas que usam sensores podem chamar um método para abrir uma caixa de diálogo do sistema que solicita que os usuários habilitem os dispositivos de sensor necessários.</span><span class="sxs-lookup"><span data-stu-id="0b4ca-115">Programs that use sensors can call a method to open a system dialog box that prompts users to enable needed sensor devices.</span></span> <span data-ttu-id="0b4ca-116">Esse recurso torna mais fácil para os desenvolvedores e usuários garantir que os sensores funcionem quando os programas precisarem, mantendo o controle de usuário de divulgação de dados de sensor.</span><span class="sxs-lookup"><span data-stu-id="0b4ca-116">This feature makes it easy for developers and users to make sure that sensors work when programs need them, while maintaining user control of disclosure of sensor data.</span></span>
-   <span data-ttu-id="0b4ca-117">Os drivers de sensor usam um objeto especial que processa todas as solicitações de e/s.</span><span class="sxs-lookup"><span data-stu-id="0b4ca-117">Sensor drivers use a special object that processes all I/O requests.</span></span> <span data-ttu-id="0b4ca-118">Esse objeto garante que somente os programas que têm permissão de usuário possam acessar os dados do sensor.</span><span class="sxs-lookup"><span data-stu-id="0b4ca-118">This object makes sure that only programs that have user permission can access sensor data.</span></span>

 

 



