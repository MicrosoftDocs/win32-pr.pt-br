---
description: Quando privilégios elevados não são necessários para instalar um pacote de Windows Installer, o autor do pacote pode suprimir a caixa de diálogo que o UAC (controle de conta de usuário) exibe para solicitar aos usuários a autorização do administrador.
ms.assetid: cab30f95-cc93-46db-aba5-741b44adb6de
title: Criando pacotes sem a caixa de diálogo UAC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58dcd44bf7d2250e12e7cafde46b57978b48cceb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103662065"
---
# <a name="authoring-packages-without-the-uac-dialog-box"></a><span data-ttu-id="14842-103">Criando pacotes sem a caixa de diálogo UAC</span><span class="sxs-lookup"><span data-stu-id="14842-103">Authoring Packages without the UAC Dialog Box</span></span>

<span data-ttu-id="14842-104">Quando privilégios elevados não são necessários para instalar um pacote de Windows Installer, o autor do pacote pode suprimir a caixa de diálogo que o UAC ( [*controle de conta de usuário*](u-gly.md) ) exibe para solicitar aos usuários a autorização do administrador.</span><span class="sxs-lookup"><span data-stu-id="14842-104">When elevated privileges are not required to install a Windows Installer package, the author of the package can suppress the dialog box that [*User Account Control*](u-gly.md) (UAC) displays to prompt users for administrator authorization.</span></span>

<span data-ttu-id="14842-105">Para suprimir a exibição da caixa de diálogo do UAC ao instalar o aplicativo, o autor do pacote deve fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="14842-105">To suppress the display of the UAC dialog box when installing the application, the author of the package should do the following:</span></span>

-   <span data-ttu-id="14842-106">Instale o aplicativo usando o Window Installer 4,0 ou posterior no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="14842-106">Install the application using Window Installer 4.0 or later on Windows Vista.</span></span>
-   <span data-ttu-id="14842-107">Não dependa do uso de privilégios de sistema elevados para instalar o aplicativo no computador.</span><span class="sxs-lookup"><span data-stu-id="14842-107">Do not depend on using elevated system privileges to install the application on the computer.</span></span>
-   <span data-ttu-id="14842-108">Instale o aplicativo no contexto por usuário e torne esse o contexto de instalação padrão do pacote.</span><span class="sxs-lookup"><span data-stu-id="14842-108">Install the application in the per-user context and make this the default installation context of the package.</span></span> <span data-ttu-id="14842-109">Se a propriedade [**AllUsers**](allusers.md) não estiver definida, o instalador instalará o pacote no contexto por usuário.</span><span class="sxs-lookup"><span data-stu-id="14842-109">If the [**ALLUSERS**](allusers.md) property is not set, the installer installs the package in the per-user context.</span></span> <span data-ttu-id="14842-110">Se você não incluir a propriedade **AllUsers** na tabela de [Propriedades](property-table.md), o instalador não definirá essa propriedade e, portanto, a instalação por usuário se tornará o contexto de instalação padrão.</span><span class="sxs-lookup"><span data-stu-id="14842-110">If you do not include the **ALLUSERS** property in the [Property table](property-table.md), the installer does not set this property and so per-user installation becomes the default installation context.</span></span> <span data-ttu-id="14842-111">Você pode substituir esse padrão definindo a propriedade **AllUsers** na linha de comando.</span><span class="sxs-lookup"><span data-stu-id="14842-111">You can override this default by setting the **ALLUSERS** property on the command line.</span></span>
-   <span data-ttu-id="14842-112">Defina o bit 3 na propriedade de [**Resumo contagem de palavras**](word-count-summary.md) para indicar que privilégios elevados não são necessários para instalar o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="14842-112">Set Bit 3 in the [**Word Count Summary**](word-count-summary.md) property to indicate that elevated privileges are not required to install the application.</span></span>

 

 



