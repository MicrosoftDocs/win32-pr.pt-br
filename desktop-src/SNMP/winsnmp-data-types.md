---
title: Tipos de dados de WinSNMP
description: Os tipos de dados padrão de WinSNMP são definidos no WINSNMP. Arquivo H.
ms.assetid: 20f1bbc3-5a08-4206-980d-22a794cda402
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d7061ade6f9b69c63ba4718d9d79bbd4d39c67b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104008043"
---
# <a name="winsnmp-data-types"></a><span data-ttu-id="281d4-103">Tipos de dados de WinSNMP</span><span class="sxs-lookup"><span data-stu-id="281d4-103">WinSNMP Data Types</span></span>

<span data-ttu-id="281d4-104">\[O SNMP está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="281d4-104">\[SNMP is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="281d4-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="281d4-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="281d4-106">Em vez disso, use [gerenciamento remoto do Windows](/windows/desktop/WinRM/portal), que é a implementação da Microsoft do WS-Man.\]</span><span class="sxs-lookup"><span data-stu-id="281d4-106">Instead, use [Windows Remote Management](/windows/desktop/WinRM/portal), which is the Microsoft implementation of WS-Man.\]</span></span>

<span data-ttu-id="281d4-107">Os tipos de dados padrão de WinSNMP são definidos no WINSNMP. Arquivo H.</span><span class="sxs-lookup"><span data-stu-id="281d4-107">The standard WinSNMP data types are defined in the WINSNMP.H file.</span></span>

<span data-ttu-id="281d4-108">Observe que o WinSNMP especifica alguns parâmetros com o tipo de inteiro longo assinado, **smiINT**.</span><span class="sxs-lookup"><span data-stu-id="281d4-108">Note that WinSNMP specifies some parameters with the signed long integer type, **smiINT**.</span></span> <span data-ttu-id="281d4-109">Isso permite que o WinSNMP esteja em conformidade com os elementos de dados, especialmente os componentes de PDU, definidos nas RFCs relevantes.</span><span class="sxs-lookup"><span data-stu-id="281d4-109">This enables WinSNMP to comply with the data elements, especially the PDU components, defined in the relevant RFCs.</span></span>

 

 