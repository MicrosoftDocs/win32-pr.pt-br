---
description: Se essa política do sistema por máquina não estiver definida, somente os administradores poderão corrigir os produtos existentes que foram instalados usando privilégios elevados.
ms.assetid: cd07dcb0-b9b5-4186-a916-604c40f88b5f
title: AllowLockdownPatch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c85507d4f24209220ffb64411b452bbe46f3c76a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921521"
---
# <a name="allowlockdownpatch"></a><span data-ttu-id="8e3ca-103">AllowLockdownPatch</span><span class="sxs-lookup"><span data-stu-id="8e3ca-103">AllowLockdownPatch</span></span>

<span data-ttu-id="8e3ca-104">Se essa [política do sistema](system-policy.md) por máquina não estiver definida, somente os administradores poderão corrigir os produtos existentes que foram instalados usando privilégios elevados.</span><span class="sxs-lookup"><span data-stu-id="8e3ca-104">If this per-machine [system policy](system-policy.md) is not set, only administrators can patch existing products that were installed using elevated privileges.</span></span> <span data-ttu-id="8e3ca-105">Se AllowLockdownPatch for definido como "1", os usuários não administrativos poderão, em alguns casos, aplicar patches aos produtos enquanto executam uma instalação usando privilégios elevados.</span><span class="sxs-lookup"><span data-stu-id="8e3ca-105">If AllowLockdownPatch is set to "1", nonadministrative users can, in some cases, apply patches to products while running an installation using elevated privileges.</span></span> <span data-ttu-id="8e3ca-106">Com a política definida, o patch pode instalar [pequenas atualizações](minor-upgrades.md) ao executar uma instalação usando privilégios elevados, o patch não pode instalar as [principais atualizações](major-upgrades.md).</span><span class="sxs-lookup"><span data-stu-id="8e3ca-106">With the policy set, the patch can install [minor upgrades](minor-upgrades.md) while running an installation using elevated privileges, the patch cannot install [major upgrades](major-upgrades.md).</span></span> <span data-ttu-id="8e3ca-107">Definir essa política também permite que usuários não administrativos executem programas em privilégios LocalSystem durante uma instalação elevada.</span><span class="sxs-lookup"><span data-stu-id="8e3ca-107">Setting this policy also enables nonadministrative users to run programs at LocalSystem privileges during an elevated installation.</span></span>

<span data-ttu-id="8e3ca-108">A configuração padrão é recomendada para garantir um ambiente seguro.</span><span class="sxs-lookup"><span data-stu-id="8e3ca-108">The default setting is recommended to ensure a secure environment.</span></span>

## <a name="registry-key"></a><span data-ttu-id="8e3ca-109">Chave do Registro</span><span class="sxs-lookup"><span data-stu-id="8e3ca-109">Registry Key</span></span>

<span data-ttu-id="8e3ca-110">**HKEY \_ \_** Políticas de \\ **software** do computador local \\  \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="8e3ca-110">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="8e3ca-111">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="8e3ca-111">Data Type</span></span>

<span data-ttu-id="8e3ca-112">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="8e3ca-112">**REG\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="8e3ca-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="8e3ca-113">Remarks</span></span>

<span data-ttu-id="8e3ca-114">Qualquer usuário pode aplicar um patch durante uma instalação não elevada.</span><span class="sxs-lookup"><span data-stu-id="8e3ca-114">Any user can apply a patch during a nonelevated installation.</span></span> <span data-ttu-id="8e3ca-115">Definir essa [política de sistema](system-policy.md) por máquina como "1" fornece aos usuários não administrativos a flexibilidade adicional de aplicar patches a qualquer produto durante uma instalação elevada.</span><span class="sxs-lookup"><span data-stu-id="8e3ca-115">Setting this per-machine [system policy](system-policy.md) to "1" gives nonadministrative users the additional flexibility of applying patches to any product during an elevated installation.</span></span> <span data-ttu-id="8e3ca-116">Se essa política não estiver definida, os usuários não administrativos não poderão aplicar um patch a aplicativos atribuídos ou publicados.</span><span class="sxs-lookup"><span data-stu-id="8e3ca-116">If this policy is not set, nonadministrative users cannot apply a patch to assigned or published applications.</span></span>

<span data-ttu-id="8e3ca-117">Definir essa política também permite que usuários não administrativos executem programas arbitrários em privilégios LocalSystem se tiverem um pacote de patches Windows Installer que instala ou inicia esses programas.</span><span class="sxs-lookup"><span data-stu-id="8e3ca-117">Setting this policy also enables nonadministrative users to run arbitrary programs at LocalSystem privileges if they have a Windows Installer patch package that installs or launches those programs.</span></span>

 

 



