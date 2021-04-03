---
title: Arquivo de Module-Definition de unidade instalável
description: Arquivo de Module-Definition de unidade instalável
ms.assetid: d8d8d32e-18ac-47a5-a923-48b94b75e11d
keywords:
- drivers instaláveis, arquivos de definição de módulo
- drivers instaláveis, arquivos DEF
- drivers nstallable, função DriverProc
- Função DriverProc
- arquivos de definição de módulo
- arquivos DEF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 700931c91bfb3c17a36a1e3a1bbc4833097b4b38
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104007437"
---
# <a name="installable-drive-module-definition-file"></a><span data-ttu-id="223d6-109">Arquivo de Module-Definition de unidade instalável</span><span class="sxs-lookup"><span data-stu-id="223d6-109">Installable Drive Module-Definition File</span></span>

<span data-ttu-id="223d6-110">A definição de módulo (. DEF) de um driver instalável nomeia o driver, exporta a função [DriverProc](/windows/win32/api/mmiscapi/nc-mmiscapi-driverproc) e define uma descrição do driver.</span><span class="sxs-lookup"><span data-stu-id="223d6-110">The module-definition (.DEF) file of an installable driver names the driver, exports the [DriverProc](/windows/win32/api/mmiscapi/nc-mmiscapi-driverproc) function, and defines a driver description.</span></span> <span data-ttu-id="223d6-111">O exemplo a seguir mostra um arquivo de definição de módulo típico para um driver instalável:</span><span class="sxs-lookup"><span data-stu-id="223d6-111">The following example shows a typical module-definition file for an installable driver:</span></span>


```C++
LIBRARY OSCI 
DESCRIPTION 'FREQ,AMPL:Oscilloscope frequency and amplitude drivers.'
EXPORTS
    DriverProc
 
```



<span data-ttu-id="223d6-112">Alguns aplicativos de instalação podem abrir o driver e recuperar a linha de descrição a ser usada ao instalar o driver.</span><span class="sxs-lookup"><span data-stu-id="223d6-112">Some installation applications may open the driver and retrieve the description line to use when installing the driver.</span></span> <span data-ttu-id="223d6-113">Para permanecer compatível com esses aplicativos de instalação, a linha de descrição deve ter este formulário:</span><span class="sxs-lookup"><span data-stu-id="223d6-113">To remain compatible with these installation applications, the description line should have this form:</span></span>

<span data-ttu-id="223d6-114">  *Alias* \[ de descrição,*alias* \] ... **:\* \* * texto*</span><span class="sxs-lookup"><span data-stu-id="223d6-114">**DESCRIPTION**  *alias*\[,*alias*\]...\**:\*\*\*text*</span></span>

<span data-ttu-id="223d6-115">O *alias* especifica um nome exclusivo para o driver que os aplicativos podem usar para abrir o driver.</span><span class="sxs-lookup"><span data-stu-id="223d6-115">The *alias* specifies a unique name for the driver that applications can use to open the driver.</span></span> <span data-ttu-id="223d6-116">O alias também serve como o nome do valor associado ao driver no registro.</span><span class="sxs-lookup"><span data-stu-id="223d6-116">The alias also serves as the value name associated with the driver in the registry.</span></span> <span data-ttu-id="223d6-117">Vários aliases são separados por vírgulas.</span><span class="sxs-lookup"><span data-stu-id="223d6-117">Multiple aliases are separated by commas.</span></span> <span data-ttu-id="223d6-118">O *texto* descreve a finalidade do driver.</span><span class="sxs-lookup"><span data-stu-id="223d6-118">The *text* describes the purpose of the driver.</span></span>

 

 