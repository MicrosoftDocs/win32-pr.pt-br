---
description: Se essa política do sistema por máquina for definida como 1 (uma), Windows Installer não interagirá com o Gerenciador de reinicialização, mas usará a caixa de diálogo FilesInUse. se essa política do sistema por máquina for definida como 2 (dois), Windows Installer usará a caixa de diálogo FilesInUse.
ms.assetid: a59de5bb-e0a1-459d-83e6-afaf81298123
title: DisableAutomaticApplicationShutdown
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 060c4027a1fb4026f4e1d578bd1d0c2ed8cd979c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105780515"
---
# <a name="disableautomaticapplicationshutdown"></a><span data-ttu-id="804a9-103">DisableAutomaticApplicationShutdown</span><span class="sxs-lookup"><span data-stu-id="804a9-103">DisableAutomaticApplicationShutdown</span></span>

<span data-ttu-id="804a9-104">Se essa política do sistema por máquina for definida como 1 (uma), Windows Installer não irá interagir com o [Gerenciador de reinicialização](/windows/desktop/RstMgr/restart-manager-portal), mas usará a [caixa de diálogo FilesInUse](filesinuse-dialog.md).</span><span class="sxs-lookup"><span data-stu-id="804a9-104">If this per-machine system policy is set to 1 (one), Windows Installer does not interact with [Restart Manager](/windows/desktop/RstMgr/restart-manager-portal), but it will use the [FilesInUse Dialog](filesinuse-dialog.md).</span></span>

<span data-ttu-id="804a9-105">Se essa política do sistema por máquina for definida como 2 (dois), Windows Installer usará a [caixa de diálogo FilesInUse](filesinuse-dialog.md).</span><span class="sxs-lookup"><span data-stu-id="804a9-105">If this per-machine system policy is set to 2 (two), Windows Installer uses the [FilesInUse Dialog](filesinuse-dialog.md).</span></span> <span data-ttu-id="804a9-106">Essa configuração desabilita as tentativas do Gerenciador de [reinicialização](/windows/desktop/RstMgr/restart-manager-portal) para atenuar as reinicializações ao instalar um pacote de Windows Installer que não foi criado para usar o Gerenciador de reinicialização.</span><span class="sxs-lookup"><span data-stu-id="804a9-106">This setting disables attempts by the [Restart Manager](/windows/desktop/RstMgr/restart-manager-portal) to mitigate restarts when installing a Windows Installer package that has not been authored to use the Restart Manager.</span></span> <span data-ttu-id="804a9-107">O instalador ainda usa o Gerenciador de reinicialização para detectar arquivos em uso pelos aplicativos.</span><span class="sxs-lookup"><span data-stu-id="804a9-107">The installer still uses the Restart Manager to detect files in use by applications.</span></span>

<span data-ttu-id="804a9-108">A política DisableAutomaticApplicationShutdown está disponível a partir do Windows Installer versão 4,0 no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="804a9-108">The DisableAutomaticApplicationShutdown policy is available beginning with Windows Installer version 4.0 on Windows Vista.</span></span>

## <a name="registry-key"></a><span data-ttu-id="804a9-109">Chave do Registro</span><span class="sxs-lookup"><span data-stu-id="804a9-109">Registry Key</span></span>

<span data-ttu-id="804a9-110">**HKEY \_ \_** Políticas de \\ **software** do computador local \\  \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="804a9-110">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="804a9-111">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="804a9-111">Data Type</span></span>

<span data-ttu-id="804a9-112">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="804a9-112">**REG\_DWORD**</span></span>

## <a name="related-topics"></a><span data-ttu-id="804a9-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="804a9-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="804a9-114">**MSIRESTARTMANAGERCONTROL**</span><span class="sxs-lookup"><span data-stu-id="804a9-114">**MSIRESTARTMANAGERCONTROL**</span></span>](msirestartmanagercontrol.md)
</dt> <dt>

[<span data-ttu-id="804a9-115">Sem suporte no Windows Installer 3,1 e versões anteriores</span><span class="sxs-lookup"><span data-stu-id="804a9-115">Not Supported in Windows Installer 3.1 and earlier versions</span></span>](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 
