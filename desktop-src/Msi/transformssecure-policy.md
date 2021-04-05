---
description: Definir a política TransformsSecure como 1 informa ao instalador que as transformações devem ser armazenadas em cache localmente no computador do usuário em um local em que o usuário não tem acesso de gravação.
ms.assetid: 4fe992ed-1e8c-4ee2-a325-138bdc039e44
title: Política de TransformsSecure
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69180c797008f34755cfa415c7a76fb5f7721f30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826781"
---
# <a name="transformssecure-policy"></a><span data-ttu-id="3b1e8-103">Política de TransformsSecure</span><span class="sxs-lookup"><span data-stu-id="3b1e8-103">TransformsSecure Policy</span></span>

<span data-ttu-id="3b1e8-104">Definir a política TransformsSecure como 1 informa ao instalador que as transformações devem ser armazenadas em cache localmente no computador do usuário em um local em que o usuário não tem acesso de gravação.</span><span class="sxs-lookup"><span data-stu-id="3b1e8-104">Setting the TransformsSecure policy to 1 informs the installer that transforms are to be cached locally on the user's computer in a location where the user does not have write access.</span></span> <span data-ttu-id="3b1e8-105">Definir essa política é o mesmo que definir a [Propriedade TRANSFORMSSECURE](transformssecure.md) , exceto que o escopo é diferente.</span><span class="sxs-lookup"><span data-stu-id="3b1e8-105">Setting this policy is the same as setting the [TRANSFORMSSECURE property](transformssecure.md) except the scope is different.</span></span> <span data-ttu-id="3b1e8-106">A configuração da política TransformsSecure se aplica a todos os pacotes instalados em um determinado computador.</span><span class="sxs-lookup"><span data-stu-id="3b1e8-106">Setting TransformsSecure policy applies to all packages installed to a given computer.</span></span> <span data-ttu-id="3b1e8-107">A definição da propriedade TRANSFORMSSECURE se aplica ao pacote, independentemente do computador.</span><span class="sxs-lookup"><span data-stu-id="3b1e8-107">Setting the TRANSFORMSSECURE property applies to the package regardless of the computer.</span></span>

<span data-ttu-id="3b1e8-108">A finalidade dessa política é fornecer armazenamento de transformação seguro com usuários viajando do Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="3b1e8-108">The purpose of this policy is to provide for secure transform storage with traveling users of Windows 2000.</span></span> <span data-ttu-id="3b1e8-109">A partir do Windows Server 2003, o valor padrão dessa política é 1.</span><span class="sxs-lookup"><span data-stu-id="3b1e8-109">Beginning with Windows Server 2003, the default value of this policy is 1.</span></span>

<span data-ttu-id="3b1e8-110">Quando essa política é definida, uma [instalação de manutenção](maintenance-installation.md) só pode usar a transformação do cache protegido.</span><span class="sxs-lookup"><span data-stu-id="3b1e8-110">When this policy is set, a [maintenance installation](maintenance-installation.md) can only use the transform from the secured cache.</span></span> <span data-ttu-id="3b1e8-111">Caso o instalador ache que a transformação está ausente no computador local, o instalador tentará restaurar a transformação.</span><span class="sxs-lookup"><span data-stu-id="3b1e8-111">In the event that the installer finds that the transform is missing on the local computer, the installer attempts to restore the transform.</span></span> <span data-ttu-id="3b1e8-112">Para que o instalador restaure a transformação, a transformação segura deve residir em uma fonte autorizada na lista de origem do pacote de instalação.</span><span class="sxs-lookup"><span data-stu-id="3b1e8-112">In order for the installer to restore the transform, the secure transform must reside at an authorized source in the installation package's source list.</span></span> <span data-ttu-id="3b1e8-113">Para obter mais informações, consulte [resiliência de origem](source-resiliency.md).</span><span class="sxs-lookup"><span data-stu-id="3b1e8-113">For more information, see [Source Resiliency](source-resiliency.md).</span></span> <span data-ttu-id="3b1e8-114">A instalação de manutenção falhará se a transformação não estiver disponível ou não puder ser carregada.</span><span class="sxs-lookup"><span data-stu-id="3b1e8-114">The maintenance installation fails if the transform is unavailable or cannot be loaded.</span></span>

<span data-ttu-id="3b1e8-115">No Windows Server 2003, se essa política não estiver definida, o comportamento padrão será armazenar as transformações em um local seguro.</span><span class="sxs-lookup"><span data-stu-id="3b1e8-115">On Windows Server 2003, if this policy is not set, the default behavior is to store the transforms in a secure location.</span></span> <span data-ttu-id="3b1e8-116">Em todas as versões anteriores ao Windows Server 2003, se a política não estiver definida, o comportamento padrão será armazenar as transformações no perfil de usuários.</span><span class="sxs-lookup"><span data-stu-id="3b1e8-116">On all versions prior to Windows Server 2003, if the policy is not set, the default behavior is to store the transforms in the users profile.</span></span>

<span data-ttu-id="3b1e8-117">Consulte também [transformações protegidas](secured-transforms.md) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="3b1e8-117">See also [Secured Transforms](secured-transforms.md) for more information.</span></span>

<span data-ttu-id="3b1e8-118">Windows Installer interpreta a [política TransformsAtSource](transformsatsource-policy.md) para ser a mesma que a política TransformsSecure.</span><span class="sxs-lookup"><span data-stu-id="3b1e8-118">Windows Installer interprets the [TransformsAtSource policy](transformsatsource-policy.md) to be the same as the TransformsSecure policy.</span></span>

## <a name="registry-key"></a><span data-ttu-id="3b1e8-119">Chave do Registro</span><span class="sxs-lookup"><span data-stu-id="3b1e8-119">Registry Key</span></span>

<span data-ttu-id="3b1e8-120">**HKEY \_ \_** Políticas de \\ **software** do computador local \\  \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="3b1e8-120">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="3b1e8-121">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="3b1e8-121">Data Type</span></span>

<span data-ttu-id="3b1e8-122">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="3b1e8-122">**REG\_DWORD**</span></span>

## <a name="related-topics"></a><span data-ttu-id="3b1e8-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3b1e8-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3b1e8-124">Sem suporte no Windows Installer 2,0 e versões anteriores</span><span class="sxs-lookup"><span data-stu-id="3b1e8-124">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 



