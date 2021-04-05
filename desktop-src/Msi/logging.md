---
description: Essa política de sistema por computador será usada somente se o log não tiver sido habilitado pela \# opção de linha de comando &0034;/l&\# 0034; ou por MsiEnableLog.
ms.assetid: d8649808-5dc3-4496-8c2f-da9b1512b5aa
title: Registro em log (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a461051022791e414fe7e211e4dde33c7e83101b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103662193"
---
# <a name="logging-windows-installer"></a><span data-ttu-id="d8147-103">Registro em log (Windows Installer)</span><span class="sxs-lookup"><span data-stu-id="d8147-103">Logging (Windows Installer)</span></span>

<span data-ttu-id="d8147-104">Essa [política do sistema](system-policy.md) por máquina será usada somente se o registro em log não tiver sido habilitado pela opção de linha de comando "/l" ou por [**MsiEnableLog**](/windows/desktop/api/Msi/nf-msi-msienableloga).</span><span class="sxs-lookup"><span data-stu-id="d8147-104">This per-machine [system policy](system-policy.md) is used only if logging has not been enabled by the "/L" command line option or by [**MsiEnableLog**](/windows/desktop/api/Msi/nf-msi-msienableloga).</span></span> <span data-ttu-id="d8147-105">Se a política for definida nesse caso, o instalador criará um arquivo de log em% temp% com o nome aleatório: MSI \* . Façam.</span><span class="sxs-lookup"><span data-stu-id="d8147-105">If the policy is set in this case, the installer creates a log file in %temp% with the random name: MSI\*.LOG.</span></span> <span data-ttu-id="d8147-106">Especifique o modo de log definindo o valor da política como uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="d8147-106">Specify the logging mode by setting the policy value to a string of characters.</span></span> <span data-ttu-id="d8147-107">Use os mesmos caracteres para especificar a política do modo de log, conforme usado pela [opção de linha de comando](command-line-options.md)"/l".</span><span class="sxs-lookup"><span data-stu-id="d8147-107">Use the same characters to specify logging mode policy as used by the "/L" [command line option](command-line-options.md).</span></span> <span data-ttu-id="d8147-108">Observe que você não pode usar "+" e " \* " para a política.</span><span class="sxs-lookup"><span data-stu-id="d8147-108">Note that you cannot use "+" and "\*" for the policy.</span></span>

<span data-ttu-id="d8147-109">O modo de log pode ser definido usando a política, uma opção de linha de comando ou programaticamente.</span><span class="sxs-lookup"><span data-stu-id="d8147-109">The logging mode can be set using policy, a command line option, or programmatically.</span></span> <span data-ttu-id="d8147-110">Para obter mais informações sobre todos os métodos que estão disponíveis para definir o modo de log, consulte [log normal](normal-logging.md) na seção [log de Windows Installer](windows-installer-logging.md) .</span><span class="sxs-lookup"><span data-stu-id="d8147-110">For more information about all the methods that are available for setting the logging mode, see [Normal Logging](normal-logging.md) in the [Windows Installer Logging](windows-installer-logging.md) section.</span></span>

<span data-ttu-id="d8147-111">Você pode impedir que informações confidenciais, por exemplo, senhas, sejam inseridas no arquivo de log e fiquem visíveis.</span><span class="sxs-lookup"><span data-stu-id="d8147-111">You can prevent confidential information, for example passwords, from being entered into the log file and made visible.</span></span> <span data-ttu-id="d8147-112">Para obter mais informações, consulte [impedindo que informações confidenciais sejam gravadas no arquivo de log](preventing-confidential-information-from-being-written-into-the-log-file.md)</span><span class="sxs-lookup"><span data-stu-id="d8147-112">For more information, see [Preventing Confidential Information from Being Written into the Log File](preventing-confidential-information-from-being-written-into-the-log-file.md)</span></span>

## <a name="registry-key"></a><span data-ttu-id="d8147-113">Chave do Registro</span><span class="sxs-lookup"><span data-stu-id="d8147-113">Registry Key</span></span>

<span data-ttu-id="d8147-114">Defina o valor chamado Logging na seguinte chave do registro.</span><span class="sxs-lookup"><span data-stu-id="d8147-114">Set the value named Logging under the following registry key.</span></span>

<span data-ttu-id="d8147-115">**HKEY \_ \_** Políticas de \\ **software** do computador local \\  \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="d8147-115">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="d8147-116">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="d8147-116">Data Type</span></span>

<span data-ttu-id="d8147-117">**REG \_ sz**</span><span class="sxs-lookup"><span data-stu-id="d8147-117">**REG\_SZ**</span></span>

 

 



