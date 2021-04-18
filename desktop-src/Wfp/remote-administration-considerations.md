---
description: Há algumas considerações que são exclusivas para sistemas administrados remotamente.
ms.assetid: bfdf121e-9b4e-4323-82ec-9bd32531caad
title: Considerações sobre administração remota de WFP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57bb40776f6b727abb49d7e0685bb12b087ed2bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105784506"
---
# <a name="wfp-remote-administration-considerations"></a><span data-ttu-id="8940f-103">Considerações sobre administração remota de WFP</span><span class="sxs-lookup"><span data-stu-id="8940f-103">WFP Remote Administration Considerations</span></span>

<span data-ttu-id="8940f-104">Há algumas considerações que são exclusivas para sistemas administrados remotamente.</span><span class="sxs-lookup"><span data-stu-id="8940f-104">There are some considerations that are unique to remotely administered systems.</span></span> <span data-ttu-id="8940f-105">Primeiro, quando a instalação de software é implantada remotamente (usando SMS ou MSI), as caixas de diálogo de erro WFP são exibidas na tela de um administrador conectado localmente (se houver), não no serviço de instalação.</span><span class="sxs-lookup"><span data-stu-id="8940f-105">First, when software installation is remotely deployed (using SMS or MSI), WFP error dialog boxes are displayed on the screen of a locally logged on administrator (if present), not to the installation service.</span></span> <span data-ttu-id="8940f-106">Em segundo lugar, se um administrador fizer logon em um servidor de terminal remotamente e instalar um aplicativo que substitui arquivos do sistema protegidos, as caixas de diálogo de erro WFP serão exibidas somente no console principal, não na janela remota do administrador.</span><span class="sxs-lookup"><span data-stu-id="8940f-106">Second, if an administrator logs into a terminal server remotely and installs an application that replaces protected system files, the WFP error dialog boxes are displayed only in the main console, not the administrator's remote window.</span></span>

<span data-ttu-id="8940f-107">Por esses motivos, a WFP suprime suas caixas de diálogo de erro até que um administrador faça logon localmente.</span><span class="sxs-lookup"><span data-stu-id="8940f-107">For these reasons, WFP suppresses its error dialog boxes until an administrator logs on locally.</span></span> <span data-ttu-id="8940f-108">Os administradores remotos podem encontrar erros de substituição de arquivo no log de eventos do sistema.</span><span class="sxs-lookup"><span data-stu-id="8940f-108">Remote administrators can find file replacement errors in the system event log.</span></span>

<span data-ttu-id="8940f-109">**Windows Vista e Windows Server 2008:** Não há suporte para a administração remota de WFP.</span><span class="sxs-lookup"><span data-stu-id="8940f-109">**Windows Vista and Windows Server 2008:** WFP remote administration is not supported.</span></span>

 

 



