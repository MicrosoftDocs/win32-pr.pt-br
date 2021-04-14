---
title: Nomes de dispositivo
description: Nomes de dispositivo
ms.assetid: 0ba06439-cc33-43e1-a094-09bcc5e2f6b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e516f7f8eed338067dc373f8509f46598e198c71
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104453727"
---
# <a name="device-names"></a><span data-ttu-id="0d4bd-103">Nomes de dispositivo</span><span class="sxs-lookup"><span data-stu-id="0d4bd-103">Device Names</span></span>

<span data-ttu-id="0d4bd-104">Para cada tipo de dispositivo, pode haver vários drivers MCI que compartilham o conjunto de comandos, mas operam em formatos de dados diferentes.</span><span class="sxs-lookup"><span data-stu-id="0d4bd-104">For each device type, there might be several MCI drivers that share the command set but operate on different data formats.</span></span> <span data-ttu-id="0d4bd-105">Para identificar exclusivamente um driver MCI, o MCI usa *nomes de dispositivo*.</span><span class="sxs-lookup"><span data-stu-id="0d4bd-105">To uniquely identify an MCI driver, MCI uses *device names*.</span></span>

<span data-ttu-id="0d4bd-106">Os nomes de dispositivo são identificados na \[ \] seção MCI do arquivo SYSTEM.INI ou na parte apropriada do registro.</span><span class="sxs-lookup"><span data-stu-id="0d4bd-106">Device names are identified either in the \[mci\] section of the SYSTEM.INI file or in the appropriate part of the registry.</span></span> <span data-ttu-id="0d4bd-107">Essas informações identificam todos os drivers MCI para o Windows.</span><span class="sxs-lookup"><span data-stu-id="0d4bd-107">This information identifies all MCI drivers to Windows.</span></span> <span data-ttu-id="0d4bd-108">As entradas na \[ seção MCI \] usam o seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="0d4bd-108">The entries in the \[mci\] section use the following form:</span></span>

<span data-ttu-id="0d4bd-109">*\_ nome do dispositivo* driver nome do  =  *\_ arquivo. extensão*</span><span class="sxs-lookup"><span data-stu-id="0d4bd-109">*device\_name* = *driver\_filename.extension*</span></span>

<span data-ttu-id="0d4bd-110">O exemplo a seguir mostra uma \[ seção MCI típica \] da SYSTEM.INI:</span><span class="sxs-lookup"><span data-stu-id="0d4bd-110">The following example shows a typical \[mci\] section from SYSTEM.INI:</span></span>


```C++
[mci]
cdaudio=mcicda.drv 
sequencer=mciseq.drv 
waveaudio=mciwave.drv 
avivideo=mciavi.drv
```



<span data-ttu-id="0d4bd-111">Se um driver MCI for instalado usando um nome de dispositivo que já existe no SYSTEM.INI ou no registro, o sistema acrescentará um inteiro ao nome do dispositivo do novo driver, criando um nome de dispositivo exclusivo.</span><span class="sxs-lookup"><span data-stu-id="0d4bd-111">If an MCI driver is installed using a device name that already exists in SYSTEM.INI or the registry, the system appends an integer to the device name of the new driver, creating a unique device name.</span></span> <span data-ttu-id="0d4bd-112">No exemplo anterior, um driver adicional instalado usando o nome do dispositivo "cdaudio" seria atribuído ao nome do dispositivo "cdaudio1".</span><span class="sxs-lookup"><span data-stu-id="0d4bd-112">In the preceding example, an additional driver installed using the "cdaudio" device name would be assigned the device name "cdaudio1".</span></span>

 

 




