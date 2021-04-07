---
description: Se essa política do sistema por máquina for definida como 1, os patches não poderão ser removidos do computador por um usuário ou um administrador.
ms.assetid: e964cb2b-ceaa-4122-bf54-cf1eeab4bc25
title: DisablePatchUninstall
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2de1bc85a249b4377024f22a7cd0451421dcd060
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827351"
---
# <a name="disablepatchuninstall"></a><span data-ttu-id="0f4ea-103">DisablePatchUninstall</span><span class="sxs-lookup"><span data-stu-id="0f4ea-103">DisablePatchUninstall</span></span>

<span data-ttu-id="0f4ea-104">Se essa [política do sistema](system-policy.md) por máquina for definida como 1, os patches não poderão ser removidos do computador por um usuário ou um administrador.</span><span class="sxs-lookup"><span data-stu-id="0f4ea-104">If this per-machine [system policy](system-policy.md) is set to 1, patches cannot be removed from the computer by a user or an administrator.</span></span> <span data-ttu-id="0f4ea-105">O Windows Installer ainda pode remover um patch que não é mais aplicável a um produto.</span><span class="sxs-lookup"><span data-stu-id="0f4ea-105">The Windows Installer can still remove a patch that is no longer applicable to a product.</span></span> <span data-ttu-id="0f4ea-106">Se essa política não estiver definida, um usuário poderá remover um patch do computador somente se o usuário tiver concedido privilégios para remover o patch.</span><span class="sxs-lookup"><span data-stu-id="0f4ea-106">If this policy is not set, a user can remove a patch from the computer only if the user has been granted privileges to remove the patch.</span></span> <span data-ttu-id="0f4ea-107">Isso pode depender se o usuário é um administrador, se as configurações de política [DisableMsi](disablemsi.md) e [AlwaysInstallElevated](alwaysinstallelevated.md) estão definidas e se o patch foi instalado em um contexto gerenciado por usuário, não gerenciado por usuário ou por computador.</span><span class="sxs-lookup"><span data-stu-id="0f4ea-107">This can depend on whether the user is an administrator, whether [DisableMsi](disablemsi.md) and [AlwaysInstallElevated](alwaysinstallelevated.md) policy settings are set, and whether the patch was installed in a per-user managed, per-user unmanaged, or per-machine context.</span></span>

## <a name="registry-key"></a><span data-ttu-id="0f4ea-108">Chave do Registro</span><span class="sxs-lookup"><span data-stu-id="0f4ea-108">Registry Key</span></span>

<span data-ttu-id="0f4ea-109">**HKEY \_ \_** Políticas de \\ **software** do computador local \\  \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="0f4ea-109">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="0f4ea-110">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="0f4ea-110">Data Type</span></span>

<span data-ttu-id="0f4ea-111">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="0f4ea-111">**REG\_DWORD**</span></span>

## <a name="related-topics"></a><span data-ttu-id="0f4ea-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0f4ea-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0f4ea-113">Sem suporte no Windows Installer 2,0 e versões anteriores</span><span class="sxs-lookup"><span data-stu-id="0f4ea-113">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 



