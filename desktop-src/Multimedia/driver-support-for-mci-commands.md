---
title: Suporte de driver para comandos MCI
description: Suporte de driver para comandos MCI
ms.assetid: 1adea076-c04e-4613-a793-60de41b2e9db
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64b57e28feaa3fd1e0b4d7f3edc7c95df3f00e83
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635597"
---
# <a name="driver-support-for-mci-commands"></a><span data-ttu-id="9a505-103">Suporte de driver para comandos MCI</span><span class="sxs-lookup"><span data-stu-id="9a505-103">Driver Support for MCI Commands</span></span>

<span data-ttu-id="9a505-104">Os drivers MCI fornecem a funcionalidade para comandos MCI.</span><span class="sxs-lookup"><span data-stu-id="9a505-104">MCI drivers provide the functionality for MCI commands.</span></span> <span data-ttu-id="9a505-105">O software do sistema executa algumas tarefas básicas de gerenciamento de dados, mas toda a reprodução, apresentação e gravação de multimídia é tratada pelos drivers MCI individuais.</span><span class="sxs-lookup"><span data-stu-id="9a505-105">The system software performs some basic data-management tasks, but all the multimedia playback, presentation, and recording is handled by the individual MCI drivers.</span></span>

<span data-ttu-id="9a505-106">Os drivers variam em seu suporte para comandos MCI e sinalizadores de comando.</span><span class="sxs-lookup"><span data-stu-id="9a505-106">Drivers vary in their support for MCI commands and command flags.</span></span> <span data-ttu-id="9a505-107">Como os dispositivos de multimídia podem ter recursos amplamente diferentes, o MCI foi projetado para permitir que drivers individuais estendam ou reduzam os conjuntos de comandos para corresponder aos recursos do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9a505-107">Because multimedia devices can have widely different capabilities, MCI is designed to let individual drivers extend or reduce the command sets to match the capabilities of the device.</span></span> <span data-ttu-id="9a505-108">Por exemplo, o comando [**Record**](record.md) ([**\_ registro MCI**](mci-record.md)) faz parte do conjunto de comandos para sequenciadores MIDI, mas o driver MCISEQ incluído com o Windows não oferece suporte a esse comando.</span><span class="sxs-lookup"><span data-stu-id="9a505-108">For example, the [**record**](record.md) ([**MCI\_RECORD**](mci-record.md)) command is part of the command set for MIDI sequencers, but the MCISEQ driver included with Windows does not support this command.</span></span> <span data-ttu-id="9a505-109">O tópico de referência para o comando de registro explica que os dispositivos do tipo de dispositivo **Sequencer** reconhecem o comando; Isso não significa que todos os dispositivos desse tipo dão suporte ao comando.</span><span class="sxs-lookup"><span data-stu-id="9a505-109">The reference topic for the record command explains that devices of the **sequencer** device type recognize the command; this does not mean that all devices of this type support the command.</span></span> <span data-ttu-id="9a505-110">Os aplicativos devem usar o comando de [**capacidade**](capability.md) ([**MCI \_ GETDEVCAPS**](mci-getdevcaps.md)) para determinar os recursos de um dispositivo específico.</span><span class="sxs-lookup"><span data-stu-id="9a505-110">Applications should use the [**capability**](capability.md) ([**MCI\_GETDEVCAPS**](mci-getdevcaps.md)) command to determine the capabilities of a particular device.</span></span>

 

 




