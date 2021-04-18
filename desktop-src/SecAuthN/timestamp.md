---
description: O tipo de dados TimeStamp contém informações sobre a validade do tempo de tokens de segurança. O formato do valor do tipo de dados TimeStamp é o mesmo da estrutura FILETIME.
ms.assetid: 0a609b32-dbd7-4905-8990-65ebabcd0668
title: Carimbo de data/hora (SSPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4898e85b0c11f55e5bb0dba2dbdefe2a3b6a2e4e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105752135"
---
# <a name="timestamp"></a><span data-ttu-id="71511-104">TimeStamp</span><span class="sxs-lookup"><span data-stu-id="71511-104">TimeStamp</span></span>

<span data-ttu-id="71511-105">O tipo de dados **timestamp** contém informações sobre a validade do tempo de tokens de segurança.</span><span class="sxs-lookup"><span data-stu-id="71511-105">The **TimeStamp** data type holds information about the time validity of security tokens.</span></span> <span data-ttu-id="71511-106">O formato do valor do tipo de dados **timestamp** é o mesmo da estrutura [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) .</span><span class="sxs-lookup"><span data-stu-id="71511-106">The format of the value of the **TimeStamp** data type is the same as that of the [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) structure.</span></span>


```C++
typedef SECURITY_INTEGER TimeStamp, *PTimeStamp;
```



## <a name="requirements"></a><span data-ttu-id="71511-107">Requisitos</span><span class="sxs-lookup"><span data-stu-id="71511-107">Requirements</span></span>



| <span data-ttu-id="71511-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="71511-108">Requirement</span></span> | <span data-ttu-id="71511-109">Valor</span><span class="sxs-lookup"><span data-stu-id="71511-109">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71511-110">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="71511-110">Minimum supported client</span></span><br/> | <span data-ttu-id="71511-111">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="71511-111">Windows XP \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="71511-112">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="71511-112">Minimum supported server</span></span><br/> | <span data-ttu-id="71511-113">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="71511-113">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="71511-114">parâmetro</span><span class="sxs-lookup"><span data-stu-id="71511-114">Header</span></span><br/>                   | <dl> <span data-ttu-id="71511-115"><dt>SSPI. h (incluir Security. h)</dt></span><span class="sxs-lookup"><span data-stu-id="71511-115"><dt>Sspi.h (include Security.h)</dt></span></span> </dl> |



 

 
