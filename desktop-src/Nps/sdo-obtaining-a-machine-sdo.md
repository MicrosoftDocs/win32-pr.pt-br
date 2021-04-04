---
title: Obtendo um SDO de máquina
description: A primeira etapa ao usar a API de SDO é criar um objeto de computador SDO.
ms.assetid: bdb01437-08d0-4279-94f2-840cb786cc44
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bf85f9712e76bbdadcffa3914a86cc56576aecd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007799"
---
# <a name="obtaining-a-machine-sdo"></a><span data-ttu-id="6ba31-103">Obtendo um SDO de máquina</span><span class="sxs-lookup"><span data-stu-id="6ba31-103">Obtaining a Machine SDO</span></span>

<span data-ttu-id="6ba31-104">A primeira etapa ao usar a API de SDO é criar um objeto de computador SDO.</span><span class="sxs-lookup"><span data-stu-id="6ba31-104">The first step in using the SDO API is to create an SDO machine object.</span></span>

<span data-ttu-id="6ba31-105">Use a função [**CLSIDFromProgID**](/windows/win32/api/combaseapi/nf-combaseapi-clsidfromprogid) para obter o identificador de classe (CLSID) para o objeto de computador SDO.</span><span class="sxs-lookup"><span data-stu-id="6ba31-105">Use the [**CLSIDFromProgID**](/windows/win32/api/combaseapi/nf-combaseapi-clsidfromprogid) function to obtain the class identifier (CLSID) for the SDO machine object.</span></span> <span data-ttu-id="6ba31-106">O identificador programático (ProgID) a ser usado para o objeto é "IAS. SdoMachine".</span><span class="sxs-lookup"><span data-stu-id="6ba31-106">The programmatic identifier (ProgID) to use for the object is "IAS.SdoMachine".</span></span>

<span data-ttu-id="6ba31-107">Quando você tiver o CLSID, chame [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) com esse CLSID.</span><span class="sxs-lookup"><span data-stu-id="6ba31-107">Once you have the CLSID, call [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) with this CLSID.</span></span> <span data-ttu-id="6ba31-108">Especifique [**ISdoMachine**](/windows/desktop/api/sdoias/nn-sdoias-isdomachine) como a interface para a qual retornar um ponteiro.</span><span class="sxs-lookup"><span data-stu-id="6ba31-108">Specify [**ISdoMachine**](/windows/desktop/api/sdoias/nn-sdoias-isdomachine) as the interface for which to return a pointer.</span></span>

<span data-ttu-id="6ba31-109">Consulte [anexando a um computador SDO-Enabled](/windows/desktop/Nps/sdo-attaching-to-an-sdo-enabled-computer) para ver o código de exemplo que demonstra como obter um SDO de máquina.</span><span class="sxs-lookup"><span data-stu-id="6ba31-109">See [Attaching to an SDO-Enabled Computer](/windows/desktop/Nps/sdo-attaching-to-an-sdo-enabled-computer) for sample code that demonstrates how to obtain a machine SDO.</span></span>

 

 