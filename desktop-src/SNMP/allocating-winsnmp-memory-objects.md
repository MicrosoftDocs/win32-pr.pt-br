---
title: Alocando objetos de memória WinSNMP
description: Os descritores, os identificadores de recursos e as cadeias de caracteres em estilo C são os três tipos de objetos de memória no ambiente de programação WinSNMP.
ms.assetid: 7f51f02b-7c9f-4aa0-b0cf-83551a312e83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d70ed4d9d52452b5067a6d1e51392b84f95ccce8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104004844"
---
# <a name="allocating-winsnmp-memory-objects"></a><span data-ttu-id="9c789-103">Alocando objetos de memória WinSNMP</span><span class="sxs-lookup"><span data-stu-id="9c789-103">Allocating WinSNMP Memory Objects</span></span>

<span data-ttu-id="9c789-104">Os descritores, os identificadores de recursos e as cadeias de caracteres em estilo C são os três tipos de objetos de memória no ambiente de programação WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="9c789-104">Descriptors, resource handles and C-style strings are the three types of memory objects in the WinSNMP programming environment.</span></span>

<span data-ttu-id="9c789-105">O tipo de objeto determina se a implementação de WinSNMP da Microsoft ou o aplicativo WinSNMP aloca e anula a memória para o objeto.</span><span class="sxs-lookup"><span data-stu-id="9c789-105">The type of object determines whether the Microsoft WinSNMP implementation or the WinSNMP application allocates and deallocates the memory for the object.</span></span> <span data-ttu-id="9c789-106">Isso reduz a alocação desnecessária do espaço de buffer temporário e a cópia desnecessária de buffers.</span><span class="sxs-lookup"><span data-stu-id="9c789-106">This reduces unnecessary allocation of temporary buffer space and unnecessary copying of buffers.</span></span>

<span data-ttu-id="9c789-107">A tabela a seguir resume a alocação e a desalocação de recursos para objetos de memória WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="9c789-107">The following table summarizes the allocation and deallocation of resources for WinSNMP memory objects.</span></span>



| <span data-ttu-id="9c789-108">Tipo de Objeto</span><span class="sxs-lookup"><span data-stu-id="9c789-108">Object type</span></span>                                                                   | <span data-ttu-id="9c789-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="9c789-109">Description</span></span>                                                                                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9c789-110">descritor [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) ou [**smiOCTETS**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets)</span><span class="sxs-lookup"><span data-stu-id="9c789-110">[**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) or [**smiOCTETS**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) descriptor</span></span> | <span data-ttu-id="9c789-111">Se o aplicativo WinSNMP alocar a memória, ele deverá desalocar a memória com uma chamada para uma função apropriada.</span><span class="sxs-lookup"><span data-stu-id="9c789-111">If the WinSNMP application allocates the memory, it must deallocate the memory with a call to an appropriate function.</span></span> <span data-ttu-id="9c789-112">Se a implementação alocar a memória, o aplicativo deverá chamar a função [**SnmpFreeDescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor) para desalocar a memória.</span><span class="sxs-lookup"><span data-stu-id="9c789-112">If the implementation allocates the memory, the application must call the [**SnmpFreeDescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor) function to deallocate the memory.</span></span> |
| <span data-ttu-id="9c789-113">estrutura [**smiVALUE**](/windows/desktop/api/Winsnmp/ns-winsnmp-smivalue)</span><span class="sxs-lookup"><span data-stu-id="9c789-113">[**smiVALUE**](/windows/desktop/api/Winsnmp/ns-winsnmp-smivalue) structure</span></span>                                    | <span data-ttu-id="9c789-114">Se o membro de **valor** for um descritor [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) ou [**smiOCTETS**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) , o aplicativo deverá continuar conforme indicado acima para os descritores.</span><span class="sxs-lookup"><span data-stu-id="9c789-114">If the **value** member is an [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) or an [**smiOCTETS**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) descriptor, the application must proceed as indicated above for descriptors.</span></span>                                                                                                     |
| <span data-ttu-id="9c789-115">Identificador de recursos</span><span class="sxs-lookup"><span data-stu-id="9c789-115">Resource handle</span></span>                                                               | <span data-ttu-id="9c789-116">A implementação aloca, gerencia e libera a memória.</span><span class="sxs-lookup"><span data-stu-id="9c789-116">The implementation allocates, manages, and frees the memory.</span></span>                                                                                                                                                                                                                         |
| <span data-ttu-id="9c789-117">Cadeia de caracteres C-Style</span><span class="sxs-lookup"><span data-stu-id="9c789-117">C-style string</span></span>                                                                | <span data-ttu-id="9c789-118">O aplicativo WinSNMP deve gerenciar e liberar a memória alocada.</span><span class="sxs-lookup"><span data-stu-id="9c789-118">The WinSNMP application must manage and free the memory it allocates.</span></span>                                                                                                                                                                                                                |



 

<span data-ttu-id="9c789-119">Para obter mais informações, consulte [liberando descritores de WinSNMP](freeing-winsnmp-descriptors.md).</span><span class="sxs-lookup"><span data-stu-id="9c789-119">For more information, see [Freeing WinSNMP Descriptors](freeing-winsnmp-descriptors.md).</span></span>

 

 




