---
description: O AutoRun é um recurso do sistema operacional Windows.
title: Criando um aplicativo de CD-ROM habilitado para AutoRun
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 5c583c1d-a4eb-4291-a839-c1ca7c51342c
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 33f3ccc0a253690cd377cad908f87b43ac1ea304
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164321"
---
# <a name="creating-an-autorun-enabled-cd-rom-application"></a><span data-ttu-id="bb152-103">Criando um aplicativo de CD-ROM habilitado para AutoRun</span><span class="sxs-lookup"><span data-stu-id="bb152-103">Creating an AutoRun-enabled CD-ROM Application</span></span>

<span data-ttu-id="bb152-104">O AutoRun é um recurso do sistema operacional Windows.</span><span class="sxs-lookup"><span data-stu-id="bb152-104">AutoRun is a feature of the Windows operating system.</span></span> <span data-ttu-id="bb152-105">Ele automatiza os procedimentos para instalar e configurar produtos projetados para plataformas baseadas no Windows que são distribuídas em CD-ROMs.</span><span class="sxs-lookup"><span data-stu-id="bb152-105">It automates the procedures for installing and configuring products designed for Windows-based platforms that are distributed on CD-ROMs.</span></span> <span data-ttu-id="bb152-106">Quando os usuários inserem um CD habilitado para AutoRun em sua unidade de CD-ROM, o AutoRun executa automaticamente um aplicativo no CD-ROM que instala, configura ou executa o produto selecionado.</span><span class="sxs-lookup"><span data-stu-id="bb152-106">When users insert an AutoRun-enabled compact disc into their CD-ROM drive, AutoRun automatically runs an application on the CD-ROM that installs, configures, or runs the selected product.</span></span>

<span data-ttu-id="bb152-107">O AutoRun pode ser usado para instalar e executar aplicativos de CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="bb152-107">AutoRun can be used to install and run CD-ROM applications.</span></span> <span data-ttu-id="bb152-108">Embora o AutoRun seja mais comumente usado para aplicativos do Windows, ele também pode ser usado para instalar, configurar ou executar aplicativos baseados em MS-dos em uma sessão do Windows Microsoft MS-DOS.</span><span class="sxs-lookup"><span data-stu-id="bb152-108">Although AutoRun is most commonly used for Windows applications, it can also be used to install, configure, or run MS-DOS-based applications in a Windows Microsoft MS-DOS session.</span></span> <span data-ttu-id="bb152-109">Você pode configurar cada aplicativo baseado em MS-dos com seu próprio ícone exclusivo, Config.sys arquivo e Autoexec.bat arquivo.</span><span class="sxs-lookup"><span data-stu-id="bb152-109">You can configure each MS-DOS-based application with its own unique icon, Config.sys file, and Autoexec.bat file.</span></span> <span data-ttu-id="bb152-110">O Windows cria os arquivos de configuração corretos para o aplicativo baseado em MS-dos.</span><span class="sxs-lookup"><span data-stu-id="bb152-110">Windows creates the correct configuration files for the MS-DOS-based application.</span></span> <span data-ttu-id="bb152-111">O aplicativo de inicialização inicia o aplicativo baseado em MS-dos em uma janela.</span><span class="sxs-lookup"><span data-stu-id="bb152-111">The startup application then starts the MS-DOS-based application in a window.</span></span>

> [!Note]  
> <span data-ttu-id="bb152-112">Para que o AutoRun funcione, a unidade de CD-ROM deve ter drivers de dispositivo 32 ou 64 bits que detectam quando um usuário insere um CD e notifica o sistema.</span><span class="sxs-lookup"><span data-stu-id="bb152-112">For AutoRun to work, the CD-ROM drive must have 32 or 64-bit device drivers that detect when a user inserts a compact disc and notify the system.</span></span>

 

<span data-ttu-id="bb152-113">As seções a seguir discutem como implementar um aplicativo de CD-ROM habilitado para AutoRun.</span><span class="sxs-lookup"><span data-stu-id="bb152-113">The following sections discuss how to implement an AutoRun-enabled CD-ROM application.</span></span>

-   [<span data-ttu-id="bb152-114">Criando um aplicativo AutoRun-Enabled</span><span class="sxs-lookup"><span data-stu-id="bb152-114">Creating an AutoRun-Enabled Application</span></span>](autoplay-works.md)
-   [<span data-ttu-id="bb152-115">Entradas autorun. inf</span><span class="sxs-lookup"><span data-stu-id="bb152-115">Autorun.inf Entries</span></span>](autorun-cmds.md)
-   [<span data-ttu-id="bb152-116">Habilitando e desabilitando o AutoRun</span><span class="sxs-lookup"><span data-stu-id="bb152-116">Enabling and Disabling AutoRun</span></span>](autoplay-reg.md)

 

 



