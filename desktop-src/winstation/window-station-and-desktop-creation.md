---
title: Estação de janela e criação de área de trabalho
description: O sistema cria automaticamente a estação de janela interativa.
ms.assetid: 5b908cb6-3a72-4afc-aed0-8411e8d0888f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34aff24a29432e3e394a199bf881aa386bf17e71
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294062"
---
# <a name="window-station-and-desktop-creation"></a><span data-ttu-id="f870a-103">Estação de janela e criação de área de trabalho</span><span class="sxs-lookup"><span data-stu-id="f870a-103">Window Station and Desktop Creation</span></span>

<span data-ttu-id="f870a-104">O sistema cria automaticamente a estação de janela interativa.</span><span class="sxs-lookup"><span data-stu-id="f870a-104">The system automatically creates the interactive window station.</span></span> <span data-ttu-id="f870a-105">Quando um usuário interativo faz logon, o sistema associa a estação de janela interativa à sessão de logon do usuário.</span><span class="sxs-lookup"><span data-stu-id="f870a-105">When an interactive user logs on, the system associates the interactive window station with the user logon session.</span></span> <span data-ttu-id="f870a-106">O sistema também cria a área de trabalho de entrada padrão para a estação de janela interativa (Winsta0 \\ padrão).</span><span class="sxs-lookup"><span data-stu-id="f870a-106">The system also creates the default input desktop for the interactive window station (Winsta0\\default).</span></span> <span data-ttu-id="f870a-107">Os processos iniciados pelo usuário conectado são associados à \\ área de trabalho padrão do Winsta0.</span><span class="sxs-lookup"><span data-stu-id="f870a-107">Processes started by the logged-on user are associated with the Winsta0\\default desktop.</span></span>

<span data-ttu-id="f870a-108">Um processo pode usar a função [**CreateWindowStation**](/windows/win32/api/winuser/nf-winuser-createwindowstationa) para criar uma nova estação de janela e a função **createdesktop** ou [**CreateDesktopEx**](/windows/win32/api/winuser/nf-winuser-createdesktopexa) para criar uma nova área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="f870a-108">A process can use the [**CreateWindowStation**](/windows/win32/api/winuser/nf-winuser-createwindowstationa) function to create a new window station, and the **CreateDesktop** or [**CreateDesktopEx**](/windows/win32/api/winuser/nf-winuser-createdesktopexa) function to create a new desktop.</span></span> <span data-ttu-id="f870a-109">O número de áreas de trabalho que podem ser criadas é limitado pelo tamanho do heap da área de trabalho do sistema.</span><span class="sxs-lookup"><span data-stu-id="f870a-109">The number of desktops that can be created is limited by the size of the system desktop heap.</span></span> <span data-ttu-id="f870a-110">Para obter mais informações, consulte [**createdesktop**](/windows/win32/api/winuser/nf-winuser-createdesktopa).</span><span class="sxs-lookup"><span data-stu-id="f870a-110">For more information, see [**CreateDesktop**](/windows/win32/api/winuser/nf-winuser-createdesktopa).</span></span>

<span data-ttu-id="f870a-111">Quando um processo não interativo, como um aplicativo de serviço, tenta se conectar a uma estação de janela e não existe nenhuma estação de janela para a sessão de logon do processo, o sistema tenta criar uma estação de janela e uma área de trabalho para a sessão.</span><span class="sxs-lookup"><span data-stu-id="f870a-111">When a noninteractive process such as a service application attempts to connect to a window station and no window station exists for the process logon session, the system attempts to create a window station and desktop for the session.</span></span> <span data-ttu-id="f870a-112">O nome da estação de janela criada é baseado no identificador de sessão de logon, e a área de trabalho é denominada padrão, conforme descrito aqui:</span><span class="sxs-lookup"><span data-stu-id="f870a-112">The name of the created window station is based on the logon session identifier, and the desktop is named default, as described here:</span></span>

-   <span data-ttu-id="f870a-113">Se um serviço estiver em execução no contexto de segurança da conta LocalSystem, mas não incluir o \_ atributo processo interativo do serviço \_ , ele usará a seguinte estação de janela e área de trabalho: Service-0x0-3e7 $ \\ Default.</span><span class="sxs-lookup"><span data-stu-id="f870a-113">If a service is running in the security context of the LocalSystem account but does not include the SERVICE\_INTERACTIVE\_PROCESS attribute, it uses the following window station and desktop: Service-0x0-3e7$\\default.</span></span> <span data-ttu-id="f870a-114">Esta estação de janela não é interativa, portanto o serviço não pode exibir uma interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="f870a-114">This window station is not interactive, so the service cannot display a user interface.</span></span> <span data-ttu-id="f870a-115">Além disso, os processos criados pelo serviço não podem exibir uma interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="f870a-115">In addition, processes created by the service cannot display a user interface.</span></span>
-   <span data-ttu-id="f870a-116">Se o serviço estiver em execução no contexto de segurança de uma conta de usuário, o nome da estação de janela será baseado no serviço SID do usuário-0x *Z1* - *Z2*$, em que *Z1* é a parte superior do Sid de logon e *Z2* é a parte inferior do Sid de logon.</span><span class="sxs-lookup"><span data-stu-id="f870a-116">If the service is running in the security context of a user account, the name of the window station is based on the user SID Service-0x *Z1*-*Z2*$, where *Z1* is the high part of the logon SID and *Z2* is the low part of the logon SID.</span></span> <span data-ttu-id="f870a-117">Como um SID é exclusivo para a sessão de logon, dois serviços em execução no mesmo contexto de segurança recebem estações de janela exclusivas.</span><span class="sxs-lookup"><span data-stu-id="f870a-117">Because a SID is unique to the logon session, two services running in the same security context receive unique window stations.</span></span> <span data-ttu-id="f870a-118">Essas estações de janela não são interativas.</span><span class="sxs-lookup"><span data-stu-id="f870a-118">These window stations are not interactive.</span></span>

<span data-ttu-id="f870a-119">A DACL (lista de controle de acesso discricionário) para a estação de janela e área de trabalho inclui os seguintes direitos de acesso para a conta de usuário do serviço:</span><span class="sxs-lookup"><span data-stu-id="f870a-119">The discretionary access control list (DACL) for the window station and desktop includes the following access rights for the service's user account:</span></span>

<span data-ttu-id="f870a-120">Estação de janela:</span><span class="sxs-lookup"><span data-stu-id="f870a-120">Window Station:</span></span>

<dl> <span data-ttu-id="f870a-121">WINSTA \_ ACCESSCLIPBOARD</span><span class="sxs-lookup"><span data-stu-id="f870a-121">WINSTA\_ACCESSCLIPBOARD</span></span>  
<span data-ttu-id="f870a-122">WINSTA \_ ACCESSGLOBALATOMS</span><span class="sxs-lookup"><span data-stu-id="f870a-122">WINSTA\_ACCESSGLOBALATOMS</span></span>  
<span data-ttu-id="f870a-123">WINSTA \_ CREATEdesktop</span><span class="sxs-lookup"><span data-stu-id="f870a-123">WINSTA\_CREATEDESKTOP</span></span>  
<span data-ttu-id="f870a-124">WINSTA \_ EXITWINDOWS</span><span class="sxs-lookup"><span data-stu-id="f870a-124">WINSTA\_EXITWINDOWS</span></span>  
<span data-ttu-id="f870a-125">WINSTA \_ ReadAttributes</span><span class="sxs-lookup"><span data-stu-id="f870a-125">WINSTA\_READATTRIBUTES</span></span>  
<span data-ttu-id="f870a-126">\_direitos padrão \_ necessários</span><span class="sxs-lookup"><span data-stu-id="f870a-126">STANDARD\_RIGHTS\_REQUIRED</span></span>  
</dl>

<span data-ttu-id="f870a-127">Área de trabalho:</span><span class="sxs-lookup"><span data-stu-id="f870a-127">Desktop:</span></span>

<dl> <span data-ttu-id="f870a-128">CreateMenu da área de trabalho \_</span><span class="sxs-lookup"><span data-stu-id="f870a-128">DESKTOP\_CREATEMENU</span></span>  
<span data-ttu-id="f870a-129">CREATEWINDOW da área de trabalho \_</span><span class="sxs-lookup"><span data-stu-id="f870a-129">DESKTOP\_CREATEWINDOW</span></span>  
<span data-ttu-id="f870a-130">enumerar área de trabalho \_</span><span class="sxs-lookup"><span data-stu-id="f870a-130">DESKTOP\_ENUMERATE</span></span>  
<span data-ttu-id="f870a-131">\_HOOKCONTROL desktop</span><span class="sxs-lookup"><span data-stu-id="f870a-131">DESKTOP\_HOOKCONTROL</span></span>  
<span data-ttu-id="f870a-132">\_READOBJECTS desktop</span><span class="sxs-lookup"><span data-stu-id="f870a-132">DESKTOP\_READOBJECTS</span></span>  
<span data-ttu-id="f870a-133">\_WRITEOBJECTS desktop</span><span class="sxs-lookup"><span data-stu-id="f870a-133">DESKTOP\_WRITEOBJECTS</span></span>  
<span data-ttu-id="f870a-134">\_direitos padrão \_ necessários</span><span class="sxs-lookup"><span data-stu-id="f870a-134">STANDARD\_RIGHTS\_REQUIRED</span></span>  
</dl>

 

 