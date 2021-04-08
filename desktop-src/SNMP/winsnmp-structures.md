---
title: Estruturas de WinSNMP
description: As funções de API WinSNMP usam as seguintes estruturas.
ms.assetid: ec74217e-8d02-4bda-b365-7b8f6c14cffb
keywords:
- Estruturas de WinSNMP SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b263f6078171c096eb7208ae4c7ef29847aead9c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103823865"
---
# <a name="winsnmp-structures"></a><span data-ttu-id="7eb58-104">Estruturas de WinSNMP</span><span class="sxs-lookup"><span data-stu-id="7eb58-104">WinSNMP Structures</span></span>

<span data-ttu-id="7eb58-105">\[O SNMP está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="7eb58-105">\[SNMP is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="7eb58-106">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="7eb58-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="7eb58-107">Em vez disso, use [gerenciamento remoto do Windows](/windows/desktop/WinRM/portal), que é a implementação da Microsoft do WS-Man.\]</span><span class="sxs-lookup"><span data-stu-id="7eb58-107">Instead, use [Windows Remote Management](/windows/desktop/WinRM/portal), which is the Microsoft implementation of WS-Man.\]</span></span>

<span data-ttu-id="7eb58-108">As funções de API WinSNMP usam as seguintes estruturas.</span><span class="sxs-lookup"><span data-stu-id="7eb58-108">The WinSNMP API functions use the following structures.</span></span>



| <span data-ttu-id="7eb58-109">Estrutura</span><span class="sxs-lookup"><span data-stu-id="7eb58-109">Structure</span></span>                                  | <span data-ttu-id="7eb58-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="7eb58-110">Description</span></span>                                                                                                            |
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7eb58-111">**smiCNTR64**</span><span class="sxs-lookup"><span data-stu-id="7eb58-111">**smiCNTR64**</span></span>](/windows/desktop/api/Winsnmp/ns-winsnmp-smicntr64)         | <span data-ttu-id="7eb58-112">Contém um valor inteiro sem sinal de 64 bits que representa um contador.</span><span class="sxs-lookup"><span data-stu-id="7eb58-112">Contains a 64-bit unsigned integer value that represents a counter.</span></span>                                                    |
| [<span data-ttu-id="7eb58-113">**smiOCTETS**</span><span class="sxs-lookup"><span data-stu-id="7eb58-113">**smiOCTETS**</span></span>](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets)         | <span data-ttu-id="7eb58-114">Contém um ponteiro para uma cadeia de caracteres de octeto SNMP de comprimento variável.</span><span class="sxs-lookup"><span data-stu-id="7eb58-114">Contains a pointer to an SNMP octet string of variable length.</span></span>                                                         |
| [<span data-ttu-id="7eb58-115">**smiOID**</span><span class="sxs-lookup"><span data-stu-id="7eb58-115">**smiOID**</span></span>](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid)               | <span data-ttu-id="7eb58-116">Contém um ponteiro para uma matriz de comprimento variável dos subidentificadores associados a um objeto nomeado especificado.</span><span class="sxs-lookup"><span data-stu-id="7eb58-116">Contains a pointer to a variable length array of the subidentifiers that are associated with a specified named object.</span></span> |
| [<span data-ttu-id="7eb58-117">**smiVALUE**</span><span class="sxs-lookup"><span data-stu-id="7eb58-117">**smiVALUE**</span></span>](/windows/desktop/api/Winsnmp/ns-winsnmp-smivalue)           | <span data-ttu-id="7eb58-118">Representa o valor associado a um nome de variável em uma entrada de associação de variável.</span><span class="sxs-lookup"><span data-stu-id="7eb58-118">Represents the value that is associated with a variable name in a variable binding entry.</span></span>                              |
| [<span data-ttu-id="7eb58-119">**smiVENDORINFO**</span><span class="sxs-lookup"><span data-stu-id="7eb58-119">**smiVENDORINFO**</span></span>](/windows/desktop/api/Winsnmp/ns-winsnmp-smivendorinfo) | <span data-ttu-id="7eb58-120">Contém informações sobre a implementação da Microsoft de WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="7eb58-120">Contains information about the Microsoft implementation of WinSNMP.</span></span>                                                    |



 

 

 