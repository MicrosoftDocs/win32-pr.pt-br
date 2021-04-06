---
description: No Windows de 64 bits, partes das entradas do registro são armazenadas separadamente para aplicativos de 32 bits e de 64 bits e mapeadas em exibições lógicas separadas do registro usando o redirecionador do registro e a reflexão do registro, pois a versão de 64 bits de um aplicativo pode usar chaves de registro e valores diferentes da versão de 32 bits. Também há chaves de registro compartilhadas que não são redirecionadas ou refletidas.
ms.assetid: 08dc034c-15ce-41d9-8e74-a49b61ad40a6
title: Dados de aplicativo de 32 bits e 64 bits no registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bc82dfbf9b22cf90866e13109aeea2bcdb10e27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828528"
---
# <a name="32-bit-and-64-bit-application-data-in-the-registry"></a><span data-ttu-id="0aca8-104">Dados de aplicativo de 32 bits e 64 bits no registro</span><span class="sxs-lookup"><span data-stu-id="0aca8-104">32-bit and 64-bit Application Data in the Registry</span></span>

<span data-ttu-id="0aca8-105">No Windows de 64 bits, partes das entradas do registro são armazenadas separadamente para aplicativos de 32 bits e de 64 bits e mapeadas em exibições lógicas separadas do registro usando o [redirecionador do registro](/windows/desktop/WinProg64/registry-redirector) e a [reflexão do registro](/windows/desktop/WinProg64/registry-reflection), pois a versão de 64 bits de um aplicativo pode usar chaves de registro e valores diferentes da versão de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="0aca8-105">On 64-bit Windows, portions of the registry entries are stored separately for 32-bit application and 64-bit applications and mapped into separate logical registry views using the [registry redirector](/windows/desktop/WinProg64/registry-redirector) and [registry reflection](/windows/desktop/WinProg64/registry-reflection), because the 64-bit version of an application may use different registry keys and values than the 32-bit version.</span></span> <span data-ttu-id="0aca8-106">Também há [chaves de registro compartilhadas](/windows/desktop/WinProg64/shared-registry-keys) que não são redirecionadas ou refletidas.</span><span class="sxs-lookup"><span data-stu-id="0aca8-106">There are also [shared registry keys](/windows/desktop/WinProg64/shared-registry-keys) that are not redirected or reflected.</span></span>

<span data-ttu-id="0aca8-107">O pai de cada nó de registro de 64 bits é o Image-Specific nó ou não.</span><span class="sxs-lookup"><span data-stu-id="0aca8-107">The parent of each 64-bit registry node is the Image-Specific Node or ISN.</span></span> <span data-ttu-id="0aca8-108">O redirecionador de registro direciona, de forma transparente, o acesso de registro de um aplicativo ao subnó não apropriado.</span><span class="sxs-lookup"><span data-stu-id="0aca8-108">The registry redirector transparently directs an application's registry access to the appropriate ISN subnode.</span></span> <span data-ttu-id="0aca8-109">Os subnós de redirecionamento na árvore do registro são criados automaticamente pelo componente WOW64 usando o nome **Wow6432Node**.</span><span class="sxs-lookup"><span data-stu-id="0aca8-109">Redirection subnodes in the registry tree are created automatically by the WOW64 component using the name **Wow6432Node**.</span></span> <span data-ttu-id="0aca8-110">Como resultado, é essencial não nomear nenhuma chave do registro que você criar **Wow6432Node**.</span><span class="sxs-lookup"><span data-stu-id="0aca8-110">As a result, it is essential not to name any registry key you create **Wow6432Node**.</span></span>

<span data-ttu-id="0aca8-111">Os principais \_ \_ sinalizadores 64KEY de WOW64 \_ e \_ 32KEY da chave WOW64 habilitam o acesso explícito à exibição do registro de 64 bits e à exibição de 32 bits, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="0aca8-111">The KEY\_WOW64\_64KEY and KEY\_WOW64\_32KEY flags enable explicit access to the 64-bit registry view and the 32-bit view, respectively.</span></span> <span data-ttu-id="0aca8-112">Para obter mais informações, consulte [acessando uma exibição de registro alternativa](/windows/desktop/WinProg64/accessing-an-alternate-registry-view).</span><span class="sxs-lookup"><span data-stu-id="0aca8-112">For more information, see [Accessing an Alternate Registry View](/windows/desktop/WinProg64/accessing-an-alternate-registry-view).</span></span>

<span data-ttu-id="0aca8-113">Para desabilitar e habilitar a reflexão do registro para uma chave específica, use as funções [**RegDisableReflectionKey**](/windows/desktop/api/Winreg/nf-winreg-regdisablereflectionkey) e [**RegEnableReflectionKey**](/windows/desktop/api/Winreg/nf-winreg-regenablereflectionkey) .</span><span class="sxs-lookup"><span data-stu-id="0aca8-113">To disable and enable registry reflection for a particular key, use the [**RegDisableReflectionKey**](/windows/desktop/api/Winreg/nf-winreg-regdisablereflectionkey) and [**RegEnableReflectionKey**](/windows/desktop/api/Winreg/nf-winreg-regenablereflectionkey) functions.</span></span> <span data-ttu-id="0aca8-114">Os aplicativos devem desabilitar a reflexão somente para as chaves do registro que elas criam e não tentar desabilitar a reflexão para as chaves predefinidas, como **HKEY \_ local \_ Machine** ou **HKEY \_ Current \_ User**.</span><span class="sxs-lookup"><span data-stu-id="0aca8-114">Applications should disable reflection only for the registry keys that they create and not attempt to disable reflection for the predefined keys such as **HKEY\_LOCAL\_MACHINE** or **HKEY\_CURRENT\_USER**.</span></span> <span data-ttu-id="0aca8-115">Para determinar quais chaves estão na lista de reflexo, use a função [**RegQueryReflectionKey**](/windows/desktop/api/WinReg/nf-winreg-regqueryreflectionkey) .</span><span class="sxs-lookup"><span data-stu-id="0aca8-115">To determine which keys are on the reflection list, use the [**RegQueryReflectionKey**](/windows/desktop/api/WinReg/nf-winreg-regqueryreflectionkey) function.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0aca8-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0aca8-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0aca8-117">Redirecionador de registro</span><span class="sxs-lookup"><span data-stu-id="0aca8-117">registry redirector</span></span>](/windows/desktop/WinProg64/registry-redirector)
</dt> <dt>

[<span data-ttu-id="0aca8-118">reflexão do registro</span><span class="sxs-lookup"><span data-stu-id="0aca8-118">registry reflection</span></span>](/windows/desktop/WinProg64/registry-reflection)
</dt> </dl>

 

 
