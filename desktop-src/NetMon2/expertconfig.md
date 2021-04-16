---
description: A estrutura EXPERTCONFIG contém os dados de configuração do especialista. O especialista sobrepõe o membro RawConfigData com uma estrutura específica de especialista.
ms.assetid: 6167e846-d58c-40a8-94f7-c6d6185ae724
title: Estrutura EXPERTCONFIG (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EXPERTCONFIG
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 293bdf4c792c10232564a7ba6386df430e81ecb5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105758295"
---
# <a name="expertconfig-structure"></a><span data-ttu-id="1aa6d-104">Estrutura EXPERTCONFIG</span><span class="sxs-lookup"><span data-stu-id="1aa6d-104">EXPERTCONFIG structure</span></span>

<span data-ttu-id="1aa6d-105">A estrutura **EXPERTCONFIG** contém os dados de configuração do especialista.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-105">The **EXPERTCONFIG** structure contains the configuration data of the expert.</span></span> <span data-ttu-id="1aa6d-106">O especialista sobrepõe o membro **RawConfigData** com uma estrutura específica de especialista.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-106">The expert overlays the **RawConfigData** member with an expert-specific structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="1aa6d-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1aa6d-107">Syntax</span></span>


```C++
typedef struct {
  DWORD RawConfigLength;
  BYTE  RawConfigData[];
} EXPERTCONFIG, *PEXPERTCONFIG;
```



## <a name="members"></a><span data-ttu-id="1aa6d-108">Membros</span><span class="sxs-lookup"><span data-stu-id="1aa6d-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="1aa6d-109">**RawConfigLength**</span><span class="sxs-lookup"><span data-stu-id="1aa6d-109">**RawConfigLength**</span></span>
</dt> <dd>

<span data-ttu-id="1aa6d-110">Comprimento total da estrutura, incluindo os quatro bytes usados para o membro.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-110">Total length of the structure, including the four bytes used for the member.</span></span> <span data-ttu-id="1aa6d-111">Monitor de Rede usa o valor quando a estrutura é salva e lida a partir de uma unidade de disco.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-111">Network Monitor uses the value when the structure is saved-to and read-from a disk drive.</span></span>

</dd> <dt>

<span data-ttu-id="1aa6d-112">**RawConfigData**</span><span class="sxs-lookup"><span data-stu-id="1aa6d-112">**RawConfigData**</span></span>
</dt> <dd>

<span data-ttu-id="1aa6d-113">Dados de configuração.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-113">Configuration data.</span></span> <span data-ttu-id="1aa6d-114">O especialista deve adicionar os dados de configuração.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-114">The expert must add the configuration data.</span></span> <span data-ttu-id="1aa6d-115">Por exemplo, suponha que você tenha uma estrutura de dados parecida com esta.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-115">For example, suppose that you had a data structure that looked like this.</span></span>

``` syntax
typedef struct
{
    DWORD       RawConfigLength;   // Overlay of structure
    DWORD       PickNumEvents;
    DWORD       NumEventsSpecific;
    DWORD       PickSpeedThroughCapture;
    DWORD       PickStartup;
    DWORD       PickAttachProperties;
} TESTEXPERTCONFIG;
typedef TESTEXPERTCONFIG* LPTESTEXPERTCONFIG;
```

<span data-ttu-id="1aa6d-116">Observe que o **RawConfigLength** garante que a sobreposição funcione corretamente.</span><span class="sxs-lookup"><span data-stu-id="1aa6d-116">Note that **RawConfigLength** ensures that the overlay works correctly.</span></span> <span data-ttu-id="1aa6d-117">Quando você usa os dados, seu código pode ter a seguinte aparência:</span><span class="sxs-lookup"><span data-stu-id="1aa6d-117">When you use the data, your code might look like this:</span></span>

``` syntax
BOOL WINAPI Configure( 
    HEXPERTKEY ExpertKey,
    PEXPERTCONFIG * ppConfig,
    PEXPERTSTARTUPINFO pStartupInfo,
    DWORD StartupFlags,
    HWND hWnd
)
{
    LPTESTEXPERTCONFIG  lpConfig;

    //...
    lpConfig = (LPTESTEXPERTCONFIG)(*ppConfig);
    //...
}
```

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1aa6d-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1aa6d-118">Requirements</span></span>



| <span data-ttu-id="1aa6d-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="1aa6d-119">Requirement</span></span> | <span data-ttu-id="1aa6d-120">Valor</span><span class="sxs-lookup"><span data-stu-id="1aa6d-120">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="1aa6d-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1aa6d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="1aa6d-122">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="1aa6d-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="1aa6d-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1aa6d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="1aa6d-124">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="1aa6d-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="1aa6d-125">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="1aa6d-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="1aa6d-126"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="1aa6d-126"><dt>Netmon.h</dt></span></span> </dl> |



 

 




