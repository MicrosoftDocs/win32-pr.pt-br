---
description: Demonstra como usar as \_ APIs NotifyIcon e Shell NotifyIconGetRect do Shell \_ para exibir um ícone de notificação.
title: Exemplo NotificationIcon
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 9F31DB2D-4B12-4f65-AC91-25B4B5B1CB46
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 1569d162aef358130910081bee80354cb64f690d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104967971"
---
# <a name="notificationicon-sample"></a><span data-ttu-id="aa68d-103">Exemplo NotificationIcon</span><span class="sxs-lookup"><span data-stu-id="aa68d-103">NotificationIcon Sample</span></span>

<span data-ttu-id="aa68d-104">Demonstra como usar as APIs [**\_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) e [**shell \_ NotifyIconGetRect**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicongetrect) do Shell para exibir um ícone de notificação.</span><span class="sxs-lookup"><span data-stu-id="aa68d-104">Demonstrates how to use the [**Shell\_NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) and [**Shell\_NotifyIconGetRect**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicongetrect) APIs to display a notification icon.</span></span>

<span data-ttu-id="aa68d-105">Este tópico inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="aa68d-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="aa68d-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="aa68d-106">Description</span></span>](#description)
-   [<span data-ttu-id="aa68d-107">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aa68d-107">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="aa68d-108">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="aa68d-108">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="aa68d-109">Compilando o exemplo</span><span class="sxs-lookup"><span data-stu-id="aa68d-109">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="aa68d-110">Executando o exemplo</span><span class="sxs-lookup"><span data-stu-id="aa68d-110">Running the Sample</span></span>](#running-the-sample)

## <a name="description"></a><span data-ttu-id="aa68d-111">Description</span><span class="sxs-lookup"><span data-stu-id="aa68d-111">Description</span></span>

<span data-ttu-id="aa68d-112">Além do uso do [**shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) e do [**shell \_ NotifyIconGetRect**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicongetrect) para exibir um ícone de notificação, este exemplo também demonstra como exibir uma janela submenu rica, um menu de contexto e uma notificação de balão.</span><span class="sxs-lookup"><span data-stu-id="aa68d-112">In addition to the use of [**Shell\_NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) and [**Shell\_NotifyIconGetRect**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicongetrect) to display a notification icon, this sample also demonstrates how to display a rich flyout window, context menu, and balloon notification.</span></span>

> [!Note]  
> <span data-ttu-id="aa68d-113">[**Shell \_ do O NotifyIconGetRect**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicongetrect) só está disponível no Windows 7 e versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="aa68d-113">[**Shell\_NotifyIconGetRect**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicongetrect) is only available on Windows 7 and later versions.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="aa68d-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aa68d-114">Requirements</span></span>



| <span data-ttu-id="aa68d-115">Produto</span><span class="sxs-lookup"><span data-stu-id="aa68d-115">Product</span></span>                                | <span data-ttu-id="aa68d-116">Versão mínima do produto</span><span class="sxs-lookup"><span data-stu-id="aa68d-116">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="aa68d-117">Windows</span><span class="sxs-lookup"><span data-stu-id="aa68d-117">Windows</span></span>                                | <span data-ttu-id="aa68d-118">Windows 7</span><span class="sxs-lookup"><span data-stu-id="aa68d-118">Windows 7</span></span>               |
| <span data-ttu-id="aa68d-119">Windows Software Development Kit (SDK)</span><span class="sxs-lookup"><span data-stu-id="aa68d-119">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="aa68d-120">7.0</span><span class="sxs-lookup"><span data-stu-id="aa68d-120">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="aa68d-121">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="aa68d-121">Downloading the Sample</span></span>

| <span data-ttu-id="aa68d-122">Localização</span><span class="sxs-lookup"><span data-stu-id="aa68d-122">Location</span></span>      | <span data-ttu-id="aa68d-123">URL do caminho</span><span class="sxs-lookup"><span data-stu-id="aa68d-123">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa68d-124">GitHub</span><span class="sxs-lookup"><span data-stu-id="aa68d-124">GitHub</span></span>  | [<span data-ttu-id="aa68d-125">Exemplo de NotificationIcon</span><span class="sxs-lookup"><span data-stu-id="aa68d-125">NotificationIcon sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/NotificationIcon) |

## <a name="building-the-sample"></a><span data-ttu-id="aa68d-126">Compilando o exemplo</span><span class="sxs-lookup"><span data-stu-id="aa68d-126">Building the Sample</span></span>

<span data-ttu-id="aa68d-127">Para criar o exemplo do prompt de comando:</span><span class="sxs-lookup"><span data-stu-id="aa68d-127">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="aa68d-128">Abra a janela do prompt de comando e navegue até o diretório do projeto **NotificationIcon** .</span><span class="sxs-lookup"><span data-stu-id="aa68d-128">Open the command prompt window and navigate to the **NotificationIcon** project directory.</span></span>
2.  <span data-ttu-id="aa68d-129">Digite `msbuild NotificationIcon.sln`.</span><span class="sxs-lookup"><span data-stu-id="aa68d-129">Enter `msbuild NotificationIcon.sln`.</span></span>

<span data-ttu-id="aa68d-130">Para criar o exemplo usando Microsoft Visual Studio (preferencial):</span><span class="sxs-lookup"><span data-stu-id="aa68d-130">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="aa68d-131">Abra o Windows Explorer e navegue até o diretório do projeto **NotificationIcon** .</span><span class="sxs-lookup"><span data-stu-id="aa68d-131">Open Windows Explorer and navigate to the **NotificationIcon** project directory.</span></span>
2.  <span data-ttu-id="aa68d-132">Clique duas vezes no ícone do arquivo NotificationIcon. sln para abrir o projeto no Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="aa68d-132">Double-click the icon for the NotificationIcon.sln file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="aa68d-133">No menu **Compilar** , selecione **Compilar solução**.</span><span class="sxs-lookup"><span data-stu-id="aa68d-133">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="aa68d-134">Executando o exemplo</span><span class="sxs-lookup"><span data-stu-id="aa68d-134">Running the Sample</span></span>

1.  <span data-ttu-id="aa68d-135">Navegue até o diretório que contém o novo executável, usando o prompt de comando ou o Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="aa68d-135">Navigate to the directory that contains the new executable, using the command prompt or Windows Explorer.</span></span>
2.  <span data-ttu-id="aa68d-136">Na linha de comando, digite `NotificationIcon.exe` .</span><span class="sxs-lookup"><span data-stu-id="aa68d-136">At the command line, enter `NotificationIcon.exe`.</span></span> <span data-ttu-id="aa68d-137">Como alternativa, no Windows Explorer, clique duas vezes no ícone para NotificationIcon.exe.</span><span class="sxs-lookup"><span data-stu-id="aa68d-137">Alternatively, from Windows Explorer double-click the icon for NotificationIcon.exe.</span></span>

> [!Note]  
> <span data-ttu-id="aa68d-138">Os ícones de notificação especificados com um GUID são protegidos contra falsificação, Validando que apenas um único aplicativo os registra.</span><span class="sxs-lookup"><span data-stu-id="aa68d-138">Notification icons specified with a GUID are protected against spoofing by validating that only a single application registers them.</span></span> <span data-ttu-id="aa68d-139">Esse registro é executado na primeira vez que você chama o Shell \_ NotifyIcon (Nim \_ Add,...) e o nome do caminho completo do aplicativo de chamada é armazenado.</span><span class="sxs-lookup"><span data-stu-id="aa68d-139">This registration is performed the first time you call Shell\_NotifyIcon(NIM\_ADD, ...) and the full path name of the calling application is stored.</span></span> <span data-ttu-id="aa68d-140">Se posteriormente você mover o arquivo binário para um local diferente, o sistema não permitirá que o ícone seja adicionado novamente.</span><span class="sxs-lookup"><span data-stu-id="aa68d-140">If you later move your binary file to a different location, the system will not allow the icon to be added again.</span></span> <span data-ttu-id="aa68d-141">Consulte o [**shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="aa68d-141">Please see [**Shell\_NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) for more information.</span></span>

 

 

 



