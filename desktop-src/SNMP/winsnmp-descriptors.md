---
title: Descritores de WinSNMP
description: No ambiente de programação WinSNMP, um descritor é uma das duas estruturas a seguir.
ms.assetid: a329963b-cdb9-40d2-9a82-6f0d9f4ac73a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cd7f844ab1365d6020afce0ca7bfeb3afa244a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104291890"
---
# <a name="winsnmp-descriptors"></a><span data-ttu-id="10548-103">Descritores de WinSNMP</span><span class="sxs-lookup"><span data-stu-id="10548-103">WinSNMP Descriptors</span></span>

<span data-ttu-id="10548-104">No ambiente de programação WinSNMP, um *descritor* é uma das duas estruturas a seguir:</span><span class="sxs-lookup"><span data-stu-id="10548-104">In the WinSNMP programming environment a *descriptor* is one of the following two structures:</span></span>

-   <span data-ttu-id="10548-105">Uma estrutura [**smiOCTETS**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) que descreve uma variável de cadeia de caracteres de octeto</span><span class="sxs-lookup"><span data-stu-id="10548-105">An [**smiOCTETS**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) structure which describes an octet string variable</span></span>
-   <span data-ttu-id="10548-106">Uma estrutura [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) que descreve uma variável de identificador de objeto SNMP</span><span class="sxs-lookup"><span data-stu-id="10548-106">An [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) structure which describes an SNMP object identifier variable</span></span>

<span data-ttu-id="10548-107">Um descritor de WinSNMP é uma estrutura que tem dois membros: um membro de comprimento, **Len** e um membro de ponteiro, **PTR**.</span><span class="sxs-lookup"><span data-stu-id="10548-107">A WinSNMP descriptor is a structure that has two members: a length member, **len**, and a pointer member, **ptr**.</span></span> <span data-ttu-id="10548-108">O membro **PTR** aponta para a cadeia de caracteres de octeto ou o identificador de objeto de interesse.</span><span class="sxs-lookup"><span data-stu-id="10548-108">The **ptr** member points to the octet string or object identifier of interest.</span></span> <span data-ttu-id="10548-109">O membro **PTR** pode ser o tipo de dados **smiLPBYTE** ou **smiLPUINT32** .</span><span class="sxs-lookup"><span data-stu-id="10548-109">The **ptr** member can be either the **smiLPBYTE** or **smiLPUINT32** data type.</span></span>

<span data-ttu-id="10548-110">Um descritor de [**smiOCTETS**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) ou um descritor de [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) pode ser o membro de **valor** de uma estrutura **smiVALUE** .</span><span class="sxs-lookup"><span data-stu-id="10548-110">An [**smiOCTETS**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) descriptor or an [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) descriptor can be the **value** member of an **smiVALUE** structure.</span></span> <span data-ttu-id="10548-111">A estrutura [**smiVALUE**](/windows/desktop/api/Winsnmp/ns-winsnmp-smivalue) descreve o valor associado a um nome de variável em uma entrada de associação de variável.</span><span class="sxs-lookup"><span data-stu-id="10548-111">The [**smiVALUE**](/windows/desktop/api/Winsnmp/ns-winsnmp-smivalue) structure describes the value associated with a variable name in a variable binding entry.</span></span>

<span data-ttu-id="10548-112">A implementação do Microsoft WinSNMP aloca e desaloca memória para todas as estruturas **smiOCTETS** e **smiOID** de saída.</span><span class="sxs-lookup"><span data-stu-id="10548-112">The Microsoft WinSNMP implementation allocates and deallocates memory for all output **smiOCTETS** and **smiOID** structures.</span></span> <span data-ttu-id="10548-113">Portanto, o aplicativo deve chamar a função [**SnmpFreeDescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor) para liberar a memória para o membro **PTR** dessas estruturas.</span><span class="sxs-lookup"><span data-stu-id="10548-113">Therefore, the application must call the [**SnmpFreeDescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor) function to free the memory for the **ptr** member of these structures.</span></span>

<span data-ttu-id="10548-114">Membros de cadeia de caracteres nos descritores não exigem um byte de terminação **nulo** .</span><span class="sxs-lookup"><span data-stu-id="10548-114">String members in descriptors do not require a **NULL** terminating byte.</span></span> <span data-ttu-id="10548-115">Para obter informações adicionais sobre como gerenciar a memória alocada para descritores, consulte [alocando objetos de memória WinSNMP](allocating-winsnmp-memory-objects.md).</span><span class="sxs-lookup"><span data-stu-id="10548-115">For additional information about managing the memory allocated for descriptors, see [Allocating WinSNMP Memory Objects](allocating-winsnmp-memory-objects.md).</span></span>

 

 




