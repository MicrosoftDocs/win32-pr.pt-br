---
description: Essa política do sistema por máquina desativa a criação de pontos de verificação por Windows Installer.
ms.assetid: 706d6c85-3876-4205-b7da-b0fd709e65dd
title: LimitSystemRestoreCheckpointing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7606d266b4e9e42f6287669df9b3ab33a3ad9f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105770193"
---
# <a name="limitsystemrestorecheckpointing"></a><span data-ttu-id="bc70b-103">LimitSystemRestoreCheckpointing</span><span class="sxs-lookup"><span data-stu-id="bc70b-103">LimitSystemRestoreCheckpointing</span></span>

<span data-ttu-id="bc70b-104">Essa [política do sistema](system-policy.md) por máquina desativa a criação de pontos de verificação por Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="bc70b-104">This per-machine [system policy](system-policy.md) turns off the creation of checkpoints by Windows Installer.</span></span>

<span data-ttu-id="bc70b-105">Definido como 0 ou ausente, o instalador faz um ponto de verificação normal para instalação ou desinstalação.</span><span class="sxs-lookup"><span data-stu-id="bc70b-105">Set to 0 or absent, the installer does normal checkpointing for install or uninstall.</span></span> <span data-ttu-id="bc70b-106">Definido como 1, o instalador não cria nenhum ponto de verificação.</span><span class="sxs-lookup"><span data-stu-id="bc70b-106">Set to 1, the installer creates no checkpoints.</span></span>

<span data-ttu-id="bc70b-107">Essa política afeta somente os pontos de verificação definidos por Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="bc70b-107">This policy affects only checkpoints set by Windows Installer.</span></span> <span data-ttu-id="bc70b-108">Em computadores com Windows XP, os administradores podem optar por desabilitar o ponto de verificação no Windows Installer para melhorar o desempenho.</span><span class="sxs-lookup"><span data-stu-id="bc70b-108">On Windows XP computers, administrators may decide to disable checkpointing from within Windows Installer to improve performance.</span></span> <span data-ttu-id="bc70b-109">A [**restauração do sistema**](../sr/system-restore-portal.md) também cria pontos de verificação adicionais.</span><span class="sxs-lookup"><span data-stu-id="bc70b-109">[**System Restore**](../sr/system-restore-portal.md) also creates additional checkpoints.</span></span> <span data-ttu-id="bc70b-110">Para obter mais informações, consulte [pontos de restauração do sistema e o Windows Installer](system-restore-points-and-the-windows-installer.md) e [definindo um ponto de restauração de uma ação personalizada](setting-a-restore-point-from-a-custom-action.md).</span><span class="sxs-lookup"><span data-stu-id="bc70b-110">For more information, see [System Restore Points and the Windows Installer](system-restore-points-and-the-windows-installer.md) and [Setting a Restore Point from a Custom Action](setting-a-restore-point-from-a-custom-action.md).</span></span>

## <a name="registry-key"></a><span data-ttu-id="bc70b-111">Chave do Registro</span><span class="sxs-lookup"><span data-stu-id="bc70b-111">Registry Key</span></span>

<span data-ttu-id="bc70b-112">Defina o valor chamado LimitSystemRestoreCheckpointing na seguinte chave do registro.</span><span class="sxs-lookup"><span data-stu-id="bc70b-112">Set the value named LimitSystemRestoreCheckpointing under the following registry key.</span></span>

<span data-ttu-id="bc70b-113">**HKEY \_ local \_ Machine \\ software \\ Policies \\ Microsoft \\ Windows \\ Installer**</span><span class="sxs-lookup"><span data-stu-id="bc70b-113">**HKEY\_LOCAL\_MACHINE\\Software\\Policies\\Microsoft\\Windows\\Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="bc70b-114">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="bc70b-114">Data Type</span></span>

<span data-ttu-id="bc70b-115">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="bc70b-115">**REG\_DWORD**</span></span>

 

 
