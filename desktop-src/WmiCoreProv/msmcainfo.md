---
description: Uma classe base abstrata da qual todas as classes de dados do provedor de arquitetura de verificação de máquina (MCA), como MSMCAInfo \_ RawMCAData, são derivadas. Essa classe está disponível somente em sistemas Windows de 64 bits.
ms.assetid: 22ec8343-fc4f-4b14-9354-26b5d6a6fe09
title: Classe MSMCAInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAInfo
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: 31fc35b1d680d900af929ea8a828bcb23d222f66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010478"
---
# <a name="msmcainfo-class"></a><span data-ttu-id="bd1ee-104">Classe MSMCAInfo</span><span class="sxs-lookup"><span data-stu-id="bd1ee-104">MSMCAInfo class</span></span>

<span data-ttu-id="bd1ee-105">A classe **MSMCAInfo** é uma classe base abstrata da qual todas as classes de dados do provedor de arquitetura de verificação de máquina (MCA), como [**MSMCAInfo \_ RawMCAData**](msmcainfo-rawmcadata.md), são derivadas.</span><span class="sxs-lookup"><span data-stu-id="bd1ee-105">The **MSMCAInfo** class is an abstract base class from which all Machine Check Architecture (MCA) provider data classes, such as [**MSMCAInfo\_RawMCAData**](msmcainfo-rawmcadata.md), are derived.</span></span> <span data-ttu-id="bd1ee-106">O provedor MCA também tem classes de evento, derivadas de [**WmiEvent**](wmievent.md).</span><span class="sxs-lookup"><span data-stu-id="bd1ee-106">The MCA provider also has event classes, derived from [**WMIEvent**](wmievent.md).</span></span> <span data-ttu-id="bd1ee-107">Essa classe está disponível somente em sistemas Windows de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="bd1ee-107">This class is available only in 64-bit Windows systems.</span></span>

<span data-ttu-id="bd1ee-108">A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="bd1ee-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="bd1ee-109">As propriedades e os métodos estão em ordem alfabética, não em ordem de MOF.</span><span class="sxs-lookup"><span data-stu-id="bd1ee-109">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd1ee-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bd1ee-110">Syntax</span></span>

``` syntax
class MSMCAInfo
{
};
```

## <a name="members"></a><span data-ttu-id="bd1ee-111">Membros</span><span class="sxs-lookup"><span data-stu-id="bd1ee-111">Members</span></span>

<span data-ttu-id="bd1ee-112">A classe **MSMCAInfo** não define nenhum membro.</span><span class="sxs-lookup"><span data-stu-id="bd1ee-112">The **MSMCAInfo** class does not define any members.</span></span>

## <a name="requirements"></a><span data-ttu-id="bd1ee-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bd1ee-113">Requirements</span></span>



| <span data-ttu-id="bd1ee-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="bd1ee-114">Requirement</span></span> | <span data-ttu-id="bd1ee-115">Valor</span><span class="sxs-lookup"><span data-stu-id="bd1ee-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bd1ee-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bd1ee-116">Minimum supported client</span></span><br/> | <span data-ttu-id="bd1ee-117">Windows XP</span><span class="sxs-lookup"><span data-stu-id="bd1ee-117">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="bd1ee-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bd1ee-118">Minimum supported server</span></span><br/> | <span data-ttu-id="bd1ee-119">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="bd1ee-119">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="bd1ee-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="bd1ee-120">Namespace</span></span><br/>                | <span data-ttu-id="bd1ee-121">\\WMI raiz</span><span class="sxs-lookup"><span data-stu-id="bd1ee-121">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="bd1ee-122">MOF</span><span class="sxs-lookup"><span data-stu-id="bd1ee-122">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bd1ee-123"><dt>Wmicore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bd1ee-123"><dt>Wmicore.mof</dt></span></span> </dl> |
| <span data-ttu-id="bd1ee-124">DLL</span><span class="sxs-lookup"><span data-stu-id="bd1ee-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bd1ee-125"><dt>Wmiprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bd1ee-125"><dt>Wmiprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd1ee-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="bd1ee-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd1ee-127">Classes MSMCA</span><span class="sxs-lookup"><span data-stu-id="bd1ee-127">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="bd1ee-128">**\_Cabeçalho MSMCAEvent**</span><span class="sxs-lookup"><span data-stu-id="bd1ee-128">**MSMCAEvent\_Header**</span></span>](msmcaevent-header.md)
</dt> <dt>

[<span data-ttu-id="bd1ee-129">**WMIEvent**</span><span class="sxs-lookup"><span data-stu-id="bd1ee-129">**WMIEvent**</span></span>](wmievent.md)
</dt> </dl>

 

 




