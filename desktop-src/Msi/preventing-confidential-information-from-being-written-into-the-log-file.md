---
description: Os desenvolvedores podem impedir que informações confidenciais, como senhas, sejam inseridas no arquivo de log durante uma instalação de Windows Installer.
ms.assetid: 950c3c56-3f16-4e1a-875f-d31f45065076
title: Impedir que informações confidenciais sejam gravadas no arquivo de log
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f17880f18ca08745ab1f4f764397e17b7af8827e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010900"
---
# <a name="preventing-confidential-information-from-being-written-into-the-log-file"></a><span data-ttu-id="13eb7-103">Impedir que informações confidenciais sejam gravadas no arquivo de log</span><span class="sxs-lookup"><span data-stu-id="13eb7-103">Preventing Confidential Information from Being Written into the Log File</span></span>

<span data-ttu-id="13eb7-104">Ao usar o Windows Installer, você pode impedir que informações confidenciais, por exemplo, senhas sejam inseridas no arquivo de log e fiquem visíveis.</span><span class="sxs-lookup"><span data-stu-id="13eb7-104">When using the Windows Installer, you can prevent confidential information, for example passwords, from being entered into the log file and made visible.</span></span>

-   <span data-ttu-id="13eb7-105">O instalador nunca grava as informações na coluna senha da tabela de [instalação](serviceinstall-table.md) no log.</span><span class="sxs-lookup"><span data-stu-id="13eb7-105">The Installer never writes the information in the Password column of the [ServiceInstall table](serviceinstall-table.md) into the log.</span></span>
-   <span data-ttu-id="13eb7-106">Você pode impedir que o instalador grave a propriedade associada a um controle de [edição](edit-control.md) no log definindo o [atributo de controle de senha](password-control-attribute.md).</span><span class="sxs-lookup"><span data-stu-id="13eb7-106">You can prevent the Installer from writing the property that is associated with an [Edit Control](edit-control.md) into the log by setting the [Password Control Attribute](password-control-attribute.md).</span></span> <span data-ttu-id="13eb7-107">A propriedade associada a um controle de edição que tem o atributo de controle de senha ficará oculta, mesmo que a política de [depuração](debug.md) esteja definida com um valor de 7.</span><span class="sxs-lookup"><span data-stu-id="13eb7-107">The property associated with an Edit Control that has the Password Control Attribute is hidden even if the [Debug](debug.md) policy is set to a value of 7.</span></span>
-   <span data-ttu-id="13eb7-108">Você pode impedir que o instalador grave uma propriedade privada no log, incluindo a propriedade na propriedade [**MsiHiddenProperties**](msihiddenproperties.md) .</span><span class="sxs-lookup"><span data-stu-id="13eb7-108">You can prevent the Installer from writing a private property into the log by including the property in the [**MsiHiddenProperties**](msihiddenproperties.md) property.</span></span>
    > [!Note]  
    > <span data-ttu-id="13eb7-109">Esse método pode tornar as informações confidenciais inseridas em uma linha de comando visíveis no log.</span><span class="sxs-lookup"><span data-stu-id="13eb7-109">This method can make confidential information entered on a command line visible in the log.</span></span> <span data-ttu-id="13eb7-110">Quando a política de [depuração](debug.md) for definida com um valor de 7, o instalador gravará as informações inseridas em uma linha de comando no log.</span><span class="sxs-lookup"><span data-stu-id="13eb7-110">When the [Debug](debug.md) policy is set to a value of 7, the installer will write information entered on a command line into the log.</span></span> <span data-ttu-id="13eb7-111">Isso torna a propriedade inserida em uma linha de comando visível mesmo que a propriedade seja incluída na propriedade [**MsiHiddenProperties**](msihiddenproperties.md) .</span><span class="sxs-lookup"><span data-stu-id="13eb7-111">This makes the property entered on a command line visible even if the property is included in the [**MsiHiddenProperties**](msihiddenproperties.md) property.</span></span>

     

-   <span data-ttu-id="13eb7-112">Você pode impedir que as informações na coluna de destino da tabela [CustomAction](customaction-table.md) sejam gravadas no log, incluindo o sinalizador de bit HideTarget no campo Type da tabela CustomAction.</span><span class="sxs-lookup"><span data-stu-id="13eb7-112">You can prevent the information in the Target column of the [CustomAction](customaction-table.md) Table from being written into the log by including the HideTarget bit flag in the Type field of the CustomAction table.</span></span> <span data-ttu-id="13eb7-113">O valor desse sinalizador é 8192 (0x2000).</span><span class="sxs-lookup"><span data-stu-id="13eb7-113">The value of this flag is 8192 (0x2000).</span></span> <span data-ttu-id="13eb7-114">Para obter mais informações, consulte [opção personalizada de destino oculto](custom-action-hidden-target-option.md).</span><span class="sxs-lookup"><span data-stu-id="13eb7-114">For more information, see [Custom Action Hidden Target Option](custom-action-hidden-target-option.md).</span></span>

 

 



