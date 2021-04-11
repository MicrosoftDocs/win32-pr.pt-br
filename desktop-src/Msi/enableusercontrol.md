---
description: Essa política do sistema por máquina pode ser usada para especificar que o Windows Installer passar todas as propriedades públicas para o lado do servidor durante uma instalação gerenciada usando privilégios elevados.
ms.assetid: 437ceef2-730f-47ae-9b1f-dfc7c6d2d132
title: EnableUserControl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 257496be3815a20bbc855b456bb74e4cc8f61684
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091139"
---
# <a name="enableusercontrol"></a><span data-ttu-id="bb134-103">EnableUserControl</span><span class="sxs-lookup"><span data-stu-id="bb134-103">EnableUserControl</span></span>

<span data-ttu-id="bb134-104">No caso de uma instalação gerenciada, o autor do pacote pode precisar limitar quais propriedades públicas são passadas para o lado do servidor e podem ser alteradas por um usuário que não seja um administrador do sistema.</span><span class="sxs-lookup"><span data-stu-id="bb134-104">In the case of a managed installation, the package author may need to limit which public properties are passed to the server side and can be changed by a user that is not a system administrator.</span></span> <span data-ttu-id="bb134-105">Algumas restrições são comumente necessárias para manter um ambiente seguro quando a instalação requer que o instalador use privilégios elevados.</span><span class="sxs-lookup"><span data-stu-id="bb134-105">Some restrictions are commonly necessary to maintain a secure environment when the installation requires the installer to use elevated privileges.</span></span>

<span data-ttu-id="bb134-106">Se essa [política do sistema](system-policy.md) por máquina for definida como "1", o instalador poderá passar todas as [Propriedades públicas](public-properties.md) para o lado do servidor durante uma instalação gerenciada usando privilégios elevados.</span><span class="sxs-lookup"><span data-stu-id="bb134-106">If this per-machine [system policy](system-policy.md) is set to "1", then the installer can pass all [public properties](public-properties.md) to the server side during a managed installation using elevated privileges.</span></span> <span data-ttu-id="bb134-107">Definir essa política tem o mesmo efeito que definir a propriedade **EnableUserControl** .</span><span class="sxs-lookup"><span data-stu-id="bb134-107">Setting this policy has the same effect as setting the **EnableUserControl** property.</span></span> <span data-ttu-id="bb134-108">Definir essa política permite que todas as propriedades públicas sejam passadas para o serviço e sejam alteradas por usuários não administrativos.</span><span class="sxs-lookup"><span data-stu-id="bb134-108">Setting this policy allows all public properties to be passed to the service and to be changeable by nonadministrative users.</span></span> <span data-ttu-id="bb134-109">Por padrão, essa política não está habilitada; somente as propriedades públicas restritas são passadas para o lado do servidor e podem ser alteradas por um usuário não administrativo.</span><span class="sxs-lookup"><span data-stu-id="bb134-109">By default, this policy is not enabled; only restricted public properties are passed to the server side and changeable by a nonadministrative user.</span></span> <span data-ttu-id="bb134-110">Todas as outras propriedades públicas são ignoradas.</span><span class="sxs-lookup"><span data-stu-id="bb134-110">All other public properties are ignored.</span></span>

<span data-ttu-id="bb134-111">Se o sistema operacional for o Windows 2000, o usuário não é um administrador do sistema e o aplicativo ou produto está sendo instalado com privilégios elevados, e um usuário que não é um administrador do sistema só pode substituir uma lista aprovada de propriedades públicas restritas.</span><span class="sxs-lookup"><span data-stu-id="bb134-111">If the operating system is Windows 2000, the user is not a system administrator, and the application or product is being installed with elevated privileges, then a user that is not a system administrator can only override an approved list of restricted public properties.</span></span> <span data-ttu-id="bb134-112">Para obter mais informações, consulte [Propriedades públicas restritas](restricted-public-properties.md).</span><span class="sxs-lookup"><span data-stu-id="bb134-112">For more information see [Restricted Public Properties](restricted-public-properties.md).</span></span>

## <a name="registry-key"></a><span data-ttu-id="bb134-113">Chave do Registro</span><span class="sxs-lookup"><span data-stu-id="bb134-113">Registry Key</span></span>

<span data-ttu-id="bb134-114">**HKEY \_ \_** Políticas de \\ **software** do computador local \\  \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="bb134-114">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="bb134-115">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="bb134-115">Data Type</span></span>

<span data-ttu-id="bb134-116">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="bb134-116">**REG\_DWORD**</span></span>

 

 



