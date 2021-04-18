---
description: Instrumentação de Gerenciamento do Windows (WMI) tem uma nova chave do registro para habilitar ou desabilitar o recurso repositório de autorestore.
ms.assetid: 6c93fc40-b5d8-42da-9d02-7fa04fce3f65
ms.tgt_platform: multiple
title: Chave do registro para configuração do repositório
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed981da7c0540378746c78fecceefab8fc62559b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105789263"
---
# <a name="registry-key-for-repository-configuration"></a><span data-ttu-id="7bf1d-103">Chave do registro para configuração do repositório</span><span class="sxs-lookup"><span data-stu-id="7bf1d-103">Registry Key for Repository Configuration</span></span>

<span data-ttu-id="7bf1d-104">Instrumentação de Gerenciamento do Windows (WMI) tem uma nova chave do registro para habilitar ou desabilitar o recurso repositório de autorestore.</span><span class="sxs-lookup"><span data-stu-id="7bf1d-104">Windows Management Instrumentation (WMI) has a new registry key to enable or disable the AutoRestore repository feature..</span></span> <span data-ttu-id="7bf1d-105">Para obter mais informações sobre como restaurar o repositório WMI, consulte [backup ou restaurar repositório WMI](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731460(v=ws.11)).</span><span class="sxs-lookup"><span data-stu-id="7bf1d-105">For more information on restoring the WMI repository, see [Backup or Restore WMI Repository](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731460(v=ws.11)).</span></span>

<span data-ttu-id="7bf1d-106">No Windows 7, o comportamento padrão é restaurar automaticamente um repositório de uma versão de backup se for detectada uma corrupção de repositório.</span><span class="sxs-lookup"><span data-stu-id="7bf1d-106">In Windows 7, the default behavior is to auto-restore a repository from a backed-up version if a repository corruption is detected.</span></span> <span data-ttu-id="7bf1d-107">O WMI fornece o valor do registro **AutoRestoreEnabled** para desabilitar esse recurso.</span><span class="sxs-lookup"><span data-stu-id="7bf1d-107">WMI provides the **AutoRestoreEnabled** registry value to disable this feature.</span></span>

<span data-ttu-id="7bf1d-108">As chaves do registro para WMI estão localizadas no registro em **HKEY \_ local \_ Machine** \\ **software** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ .</span><span class="sxs-lookup"><span data-stu-id="7bf1d-108">The registry keys for WMI are located in the registry at **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**CIMOM**\\.</span></span>

<dl> <dt>

<span data-ttu-id="7bf1d-109"><span id="AutoRestoreEnabled"></span><span id="autorestoreenabled"></span><span id="AUTORESTOREENABLED"></span>**AutoRestoreEnabled**</span><span class="sxs-lookup"><span data-stu-id="7bf1d-109"><span id="AutoRestoreEnabled"></span><span id="autorestoreenabled"></span><span id="AUTORESTOREENABLED"></span>**AutoRestoreEnabled**</span></span>
</dt> <dd>

<span data-ttu-id="7bf1d-110">Permite que o usuário determine se deseja ou não usar o recurso de repositório de restauração autorestore.</span><span class="sxs-lookup"><span data-stu-id="7bf1d-110">Enables the user to determine whether or not to use the AutoRestore repository feature.</span></span> <span data-ttu-id="7bf1d-111">Por padrão, essa chave é definida como 1 e o recurso repositório de autorestore é habilitado.</span><span class="sxs-lookup"><span data-stu-id="7bf1d-111">By default this key is set to 1 and the AutoRestore Repository feature is enabled.</span></span>

<span data-ttu-id="7bf1d-112">As seguintes configurações são possíveis:</span><span class="sxs-lookup"><span data-stu-id="7bf1d-112">The following settings are possible:</span></span>

<dl> <dt>

<span data-ttu-id="7bf1d-113"><span id="0"></span>0</span><span class="sxs-lookup"><span data-stu-id="7bf1d-113"><span id="0"></span>0</span></span>
</dt> <dd>

<span data-ttu-id="7bf1d-114">Desabilitado</span><span class="sxs-lookup"><span data-stu-id="7bf1d-114">Disabled</span></span>

</dd> <dt>

<span data-ttu-id="7bf1d-115"><span id="1"></span>1</span><span class="sxs-lookup"><span data-stu-id="7bf1d-115"><span id="1"></span>1</span></span>
</dt> <dd>

<span data-ttu-id="7bf1d-116">habilitado</span><span class="sxs-lookup"><span data-stu-id="7bf1d-116">Enabled</span></span>

</dd> </dl> </dd> </dl>

<span data-ttu-id="7bf1d-117">O valor do registro **AutoRestoreEnabled** pode ser modificado usando o console de gerenciamento de política de grupo (GPMC).</span><span class="sxs-lookup"><span data-stu-id="7bf1d-117">The **AutoRestoreEnabled** registry value can be modified by using the Group Policy Management Console (GPMC).</span></span> <span data-ttu-id="7bf1d-118">Para obter mais informações, consulte [console de gerenciamento de política de grupo](/previous-versions/windows/desktop/gpmc/group-policy-management-console-portal).</span><span class="sxs-lookup"><span data-stu-id="7bf1d-118">For more information, see [Group Policy Management Console](/previous-versions/windows/desktop/gpmc/group-policy-management-console-portal).</span></span>

<span data-ttu-id="7bf1d-119">Este procedimento fornece detalhes sobre como habilitar ou desabilitar o recurso repositório de autorestore:</span><span class="sxs-lookup"><span data-stu-id="7bf1d-119">This procedure provides details about how to enable or disable the AutoRestore repository feature:</span></span>

<span data-ttu-id="7bf1d-120">**Para alterar o valor padrão da chave **AutoRestoreEnabled** usando política de grupo**</span><span class="sxs-lookup"><span data-stu-id="7bf1d-120">**To change the default value of the **AutoRestoreEnabled** key by using Group Policy**</span></span>

1.  <span data-ttu-id="7bf1d-121">Abra o GPMC.</span><span class="sxs-lookup"><span data-stu-id="7bf1d-121">Open the GPMC.</span></span>
2.  <span data-ttu-id="7bf1d-122">Crie um objeto de Política de Grupo (GPO).</span><span class="sxs-lookup"><span data-stu-id="7bf1d-122">Create a Group Policy object (GPO).</span></span>
3.  <span data-ttu-id="7bf1d-123">Edite o GPO.</span><span class="sxs-lookup"><span data-stu-id="7bf1d-123">Edit the GPO.</span></span>
4.  <span data-ttu-id="7bf1d-124">Navegue até preferências/configurações do Windows/registro.</span><span class="sxs-lookup"><span data-stu-id="7bf1d-124">Browse to Preferences/Windows Settings/Registry.</span></span>
5.  <span data-ttu-id="7bf1d-125">Clique com o botão direito do mouse e selecione **novo... Registro**.</span><span class="sxs-lookup"><span data-stu-id="7bf1d-125">Right-click and select **New... Registry**.</span></span> <span data-ttu-id="7bf1d-126">Essa ação apresenta uma interface do usuário na qual você pode inserir informações do registro.</span><span class="sxs-lookup"><span data-stu-id="7bf1d-126">This action presents a user interface where you can enter registry information.</span></span>
6.  <span data-ttu-id="7bf1d-127">Selecione o comando **Atualizar** .</span><span class="sxs-lookup"><span data-stu-id="7bf1d-127">Select the **Update** command.</span></span>
7.  <span data-ttu-id="7bf1d-128">Selecione o seguinte caminho de chave do registro: **HKEY \_ local \_ Machine \\ software \\ Microsoft \\ WBEM \\ CIMOM**.</span><span class="sxs-lookup"><span data-stu-id="7bf1d-128">Select the following registry key path: **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\WBEM\\CIMOM**.</span></span>
8.  <span data-ttu-id="7bf1d-129">No campo **nome** , insira **AutoRestoreEnabled**.</span><span class="sxs-lookup"><span data-stu-id="7bf1d-129">In the **name** field, enter **AutoRestoreEnabled**.</span></span>
9.  <span data-ttu-id="7bf1d-130">No campo de **dados** , digite 0 para desabilitar ou 1 para habilitar o recurso repositório de autorestore.</span><span class="sxs-lookup"><span data-stu-id="7bf1d-130">In the **data** field, enter 0 to disable or 1 to enable the AutoRestore repository feature.</span></span>
10. <span data-ttu-id="7bf1d-131">Clique em OK.</span><span class="sxs-lookup"><span data-stu-id="7bf1d-131">Click OK.</span></span>

 

 
