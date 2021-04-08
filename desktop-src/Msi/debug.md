---
description: Se essa política do sistema por máquina estiver definida como &\# 0034; 1&\# 0034;, o instalador gravará mensagens de depuração comuns no depurador usando a função OutputDebugString.
ms.assetid: 0a9416ca-0535-4595-a4f3-b3ef7c2d3a13
title: Depurar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2615b12bb76f4c4da0677bbeb459fa549f8233e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829011"
---
# <a name="debug"></a><span data-ttu-id="97816-103">Depurar</span><span class="sxs-lookup"><span data-stu-id="97816-103">Debug</span></span>

<span data-ttu-id="97816-104">Se essa [política do sistema](system-policy.md) por máquina for definida como "1", o instalador gravará mensagens de depuração comuns no depurador usando a função [**OutputDebugString**](/windows/desktop/api/debugapi/nf-debugapi-outputdebugstringw) .</span><span class="sxs-lookup"><span data-stu-id="97816-104">If this per-machine [system policy](system-policy.md) is set to "1", the installer writes common debugging messages to the debugger using the [**OutputDebugString**](/windows/desktop/api/debugapi/nf-debugapi-outputdebugstringw) function.</span></span> <span data-ttu-id="97816-105">Se esse valor for definido como "2", o instalador gravará todas as mensagens de depuração válidas no depurador usando a função [**OutputDebugString**](/windows/desktop/api/debugapi/nf-debugapi-outputdebugstringw) .</span><span class="sxs-lookup"><span data-stu-id="97816-105">If this value is set to "2", the installer writes all valid debugging messages to the debugger using the [**OutputDebugString**](/windows/desktop/api/debugapi/nf-debugapi-outputdebugstringw) function.</span></span> <span data-ttu-id="97816-106">Essa política destina-se apenas para fins de depuração e pode não ter suporte em versões futuras do Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="97816-106">This policy is for debugging purposes only and may not be supported in future versions of Windows Installer.</span></span>

<span data-ttu-id="97816-107">Windows Installer apenas grava linhas de comando no arquivo de log se o terceiro bit (0x04) estiver definido no valor da política de depuração.</span><span class="sxs-lookup"><span data-stu-id="97816-107">Windows Installer only writes command lines into the log file if the third (0x04) bit is set in the value of the Debug policy.</span></span> <span data-ttu-id="97816-108">Portanto, para exibir linhas de comando no log, defina o valor da política de depuração como 7.</span><span class="sxs-lookup"><span data-stu-id="97816-108">Therefore, to display command lines in the log, set the Debug policy value to 7.</span></span> <span data-ttu-id="97816-109">Isso não exibe as propriedades associadas a um [controle de edição](edit-control.md) com o [atributo de controle de senha](password-control-attribute.md).</span><span class="sxs-lookup"><span data-stu-id="97816-109">This does not display properties associated with an [Edit Control](edit-control.md) having the [Password Control Attribute](password-control-attribute.md).</span></span> <span data-ttu-id="97816-110">Isso fará com que as propriedades definidas na linha de comando sejam visíveis no log, mesmo que a propriedade seja incluída na propriedade [**MsiHiddenProperties**](msihiddenproperties.md) .</span><span class="sxs-lookup"><span data-stu-id="97816-110">This will make properties set on the command line visible in the log even if the property is included in the [**MsiHiddenProperties**](msihiddenproperties.md) property.</span></span> <span data-ttu-id="97816-111">Para obter mais informações, consulte [impedindo que informações confidenciais sejam gravadas no arquivo de log](preventing-confidential-information-from-being-written-into-the-log-file.md).</span><span class="sxs-lookup"><span data-stu-id="97816-111">For more information, see [Preventing Confidential Information from Being Written into the Log File](preventing-confidential-information-from-being-written-into-the-log-file.md).</span></span>

## <a name="registry-key"></a><span data-ttu-id="97816-112">Chave do Registro</span><span class="sxs-lookup"><span data-stu-id="97816-112">Registry Key</span></span>

<span data-ttu-id="97816-113">**HKEY \_ \_** Políticas de \\ **software** do computador local \\  \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="97816-113">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="97816-114">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="97816-114">Data Type</span></span>

<span data-ttu-id="97816-115">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="97816-115">**REG\_DWORD**</span></span>

 

 
