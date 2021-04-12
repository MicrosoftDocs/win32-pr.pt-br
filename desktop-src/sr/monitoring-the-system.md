---
title: Monitorando o sistema
description: Monitorando o sistema
ms.assetid: e0318aca-4e3e-4272-ba31-c770d6b05272
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da7d18f42ac091b9c73c4d9a9ac3929bed235310
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104363619"
---
# <a name="monitoring-the-system"></a><span data-ttu-id="44fbe-103">Monitorando o sistema</span><span class="sxs-lookup"><span data-stu-id="44fbe-103">Monitoring the System</span></span>

<span data-ttu-id="44fbe-104">A restauração do sistema no Windows Vista e posterior salva uma cópia do volume ao gerar um ponto de restauração.</span><span class="sxs-lookup"><span data-stu-id="44fbe-104">System Restore in Windows Vista and later saves a copy of the volume when generating a restore point.</span></span> <span data-ttu-id="44fbe-105">A restauração do sistema requer um mínimo de 300 MB de espaço livre em disco na unidade do sistema na instalação.</span><span class="sxs-lookup"><span data-stu-id="44fbe-105">System Restore requires a minimum of 300 MB of free disk space on the system drive at installation.</span></span>

<span data-ttu-id="44fbe-106">A restauração do sistema no Windows XP monitora um conjunto principal de arquivos do sistema e do aplicativo, arquivando os Estados desses arquivos antes que as alterações do sistema sejam feitas.</span><span class="sxs-lookup"><span data-stu-id="44fbe-106">System Restore in Windows XP monitors a core set of system and application files, archiving the states of these files before system changes are made.</span></span> <span data-ttu-id="44fbe-107">A restauração do sistema também salva um instantâneo completo do registro e alguns arquivos de sistema dinâmicos.</span><span class="sxs-lookup"><span data-stu-id="44fbe-107">System Restore also saves a full snapshot of the registry and some dynamic system files.</span></span> <span data-ttu-id="44fbe-108">A restauração do sistema requer um mínimo de 200 MB de espaço livre em disco na unidade do sistema na instalação.</span><span class="sxs-lookup"><span data-stu-id="44fbe-108">System Restore requires a minimum of 200 MB of free disk space on the system drive at installation.</span></span> <span data-ttu-id="44fbe-109">Quando a quantidade de espaço livre em disco cai abaixo de 50 MB em qualquer unidade, a restauração do sistema muda para o modo de espera e para a criação de pontos de restauração.</span><span class="sxs-lookup"><span data-stu-id="44fbe-109">When the amount of free disk space falls below 50 MB on any drive, System Restore switches to standby mode and stops creating restore points.</span></span> <span data-ttu-id="44fbe-110">Todos os pontos de restauração são excluídos nesse momento.</span><span class="sxs-lookup"><span data-stu-id="44fbe-110">All restore points are deleted at that time.</span></span> <span data-ttu-id="44fbe-111">A restauração do sistema reativa e retoma a criação de pontos de restauração assim que 200 MB de espaço em disco estão livres na unidade do sistema.</span><span class="sxs-lookup"><span data-stu-id="44fbe-111">System Restore reactivates and resumes creating restore points as soon as 200 MB of disk space is free on the system drive.</span></span> <span data-ttu-id="44fbe-112">Os arquivos monitorados ou excluídos do monitoramento são especificados no arquivo% windir% \\ System32 \\ restore \\Filelist.xml.</span><span class="sxs-lookup"><span data-stu-id="44fbe-112">The files that are monitored or excluded from monitoring are specified in the file %windir%\\system32\\restore\\Filelist.xml.</span></span> <span data-ttu-id="44fbe-113">Para obter mais informações, consulte [extensões de nome de arquivo monitorado](monitored-file-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="44fbe-113">For more information, see [Monitored File Name Extensions](monitored-file-extensions.md).</span></span>

 

 




