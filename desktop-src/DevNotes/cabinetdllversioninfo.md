---
description: O CABINETDLLVERSIONINFO contém as informações de versão para Cabinet.dll.
ms.assetid: 1dc6962c-3087-4f56-8b65-fbf55e17eeb6
title: Estrutura CABINETDLLVERSIONINFO
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CABINETDLLVERSIONINFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: b6dfcd68f1bc684554d45feb13b9976465b70efa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826334"
---
# <a name="cabinetdllversioninfo-structure"></a><span data-ttu-id="8759f-103">Estrutura CABINETDLLVERSIONINFO</span><span class="sxs-lookup"><span data-stu-id="8759f-103">CABINETDLLVERSIONINFO structure</span></span>

<span data-ttu-id="8759f-104">\[Esta estrutura contém informações necessárias apenas ao usar a função **DllGetVersion** , que não tem suporte.</span><span class="sxs-lookup"><span data-stu-id="8759f-104">\[This structure contains information required only when using the **DllGetVersion** function, which is not supported.</span></span> <span data-ttu-id="8759f-105">Esta documentação é fornecida apenas para fins informativos.\]</span><span class="sxs-lookup"><span data-stu-id="8759f-105">This documentation is provided for informational purposes only.\]</span></span>

<span data-ttu-id="8759f-106">O **CABINETDLLVERSIONINFO** contém as informações de versão para Cabinet.dll.</span><span class="sxs-lookup"><span data-stu-id="8759f-106">The **CABINETDLLVERSIONINFO** contains the version information for Cabinet.dll.</span></span>

## <a name="syntax"></a><span data-ttu-id="8759f-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8759f-107">Syntax</span></span>


```C++
typedef struct {
  DWORD cbStruct;
  DWORD dwReserved1;
  DWORD dwReserved2;
  DWORD dwFileVersionMS;
  DWORD dwFileVersionLS;
} CABINETDLLVERSIONINFO, *PCABINETDLLVERSIONINFO;
```



## <a name="members"></a><span data-ttu-id="8759f-108">Membros</span><span class="sxs-lookup"><span data-stu-id="8759f-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="8759f-109">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="8759f-109">**cbStruct**</span></span>
</dt> <dd>

<span data-ttu-id="8759f-110">O tamanho dessa estrutura, em bytes.</span><span class="sxs-lookup"><span data-stu-id="8759f-110">The size of this structure, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="8759f-111">**dwReserved1**</span><span class="sxs-lookup"><span data-stu-id="8759f-111">**dwReserved1**</span></span>
</dt> <dd>

<span data-ttu-id="8759f-112">Reservado.</span><span class="sxs-lookup"><span data-stu-id="8759f-112">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="8759f-113">**dwReserved2**</span><span class="sxs-lookup"><span data-stu-id="8759f-113">**dwReserved2**</span></span>
</dt> <dd>

<span data-ttu-id="8759f-114">Reservado.</span><span class="sxs-lookup"><span data-stu-id="8759f-114">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="8759f-115">**dwFileVersionMS**</span><span class="sxs-lookup"><span data-stu-id="8759f-115">**dwFileVersionMS**</span></span>
</dt> <dd>

<span data-ttu-id="8759f-116">Contém os bits mais significativos das informações de versão.</span><span class="sxs-lookup"><span data-stu-id="8759f-116">Contains the most significant bits of the version information.</span></span> <span data-ttu-id="8759f-117">O bits 0-15 contém a versão secundária e o bits 16-31 contém a versão principal.</span><span class="sxs-lookup"><span data-stu-id="8759f-117">Bits 0-15 contain the minor version, and bits 16-31 contain the major version.</span></span>

</dd> <dt>

<span data-ttu-id="8759f-118">**dwFileVersionLS**</span><span class="sxs-lookup"><span data-stu-id="8759f-118">**dwFileVersionLS**</span></span>
</dt> <dd>

<span data-ttu-id="8759f-119">Contém os bits menos significativos das informações de versão.</span><span class="sxs-lookup"><span data-stu-id="8759f-119">Contains the least significant bits of the version information.</span></span> <span data-ttu-id="8759f-120">O bits 0-15 contém o número de revisão e o bits 16-31 contém o número de Build.</span><span class="sxs-lookup"><span data-stu-id="8759f-120">Bits 0-15 contain the revision number, and bits 16-31 contain the build number.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="8759f-121">Consulte também</span><span class="sxs-lookup"><span data-stu-id="8759f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8759f-122">**DllGetVersion**</span><span class="sxs-lookup"><span data-stu-id="8759f-122">**DllGetVersion**</span></span>](dllgetversion.md)
</dt> </dl>

 

 



