---
description: Os autores de pacote podem monitorar mensagens Windows Installer internas por meio da criação de um aplicativo executável que contém um manipulador de retorno de chamada para receber as mensagens e a funcionalidade para iniciar uma instalação.
ms.assetid: 0aa8a2d6-f519-4d87-a28f-a11cb546bff5
title: Monitorando uma instalação usando o MsiSetExternalUI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06cc461845a6db1fab4ede22581093c46c0e76e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105769315"
---
# <a name="monitoring-an-installation-using-msisetexternalui"></a><span data-ttu-id="f5e30-103">Monitorando uma instalação usando o MsiSetExternalUI</span><span class="sxs-lookup"><span data-stu-id="f5e30-103">Monitoring an Installation Using MsiSetExternalUI</span></span>

<span data-ttu-id="f5e30-104">Os autores de pacote podem monitorar mensagens Windows Installer internas por meio da criação de um aplicativo executável que contém um manipulador de retorno de chamada para receber as mensagens e a funcionalidade para iniciar uma instalação.</span><span class="sxs-lookup"><span data-stu-id="f5e30-104">Package authors can monitor internal Windows Installer messages through the creation of an executable application that contains both a callback handler to receive the messages and functionality to initiate an installation.</span></span>

<span data-ttu-id="f5e30-105">O manipulador de retorno de chamada está em conformidade com o \_ protótipo do manipulador INSTALLUI e um ponteiro para esse manipulador de retorno de chamada é passado para [**MsiSetExternalUI**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia).</span><span class="sxs-lookup"><span data-stu-id="f5e30-105">The callback handler conforms to the INSTALLUI\_HANDLER prototype, and a pointer to this callback handler is passed to [**MsiSetExternalUI**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia).</span></span> <span data-ttu-id="f5e30-106">Depois que a instalação for iniciada por uma chamada para [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta), as mensagens de instalação serão interceptadas pelo manipulador de retorno de chamada e o autor do pacote poderá exibir ou ignorar seletivamente qualquer ou todas essas mensagens.</span><span class="sxs-lookup"><span data-stu-id="f5e30-106">Once the installation has been initiated by a call to [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta), installation messages are trapped by the callback handler and the package author can selectively display or ignore any or all of these messages.</span></span>

<span data-ttu-id="f5e30-107">Para obter mais informações, consulte [manipulando mensagens de progresso usando MsiSetExternalUI](handling-progress-messages-using-msisetexternalui.md), [retornando valores de um manipulador de interface de usuário externo](returning-values-from-an-external-user-interface-handler.md)e [analisando Windows Installer mensagens](parsing-windows-installer-messages.md).</span><span class="sxs-lookup"><span data-stu-id="f5e30-107">For more information, see [Handling Progress Messages Using MsiSetExternalUI](handling-progress-messages-using-msisetexternalui.md), [Returning Values from an External User Interface Handler](returning-values-from-an-external-user-interface-handler.md), and [Parsing Windows Installer Messages](parsing-windows-installer-messages.md).</span></span>

<span data-ttu-id="f5e30-108">Para obter mais informações sobre como usar um manipulador externo baseado em registro, consulte [monitorando uma instalação usando o MsiSetExternalUIRecord](monitoring-an-installation-using-msisetexternaluirecord.md).</span><span class="sxs-lookup"><span data-stu-id="f5e30-108">For more information about using a record-based external handler, see [Monitoring an Installation Using MsiSetExternalUIRecord](monitoring-an-installation-using-msisetexternaluirecord.md).</span></span>

 

 



