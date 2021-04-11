---
title: Tipos de dados DNS (windns. h)
ms.assetid: 652012a5-e45d-4ea6-896a-17e8b1ed4a05
description: 'Saiba mais sobre: tipos de dados DNS'
keywords:
- IP4_ADDRESS
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2caa113670a749029b70df9772d6e2707684b7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169527"
---
# <a name="dns-data-types"></a><span data-ttu-id="b606c-104">Tipos de dados DNS</span><span class="sxs-lookup"><span data-stu-id="b606c-104">DNS Data Types</span></span>

<span data-ttu-id="b606c-105">Os seguintes tipos de dados são definidos para o DNS:</span><span class="sxs-lookup"><span data-stu-id="b606c-105">The following data types are defined for DNS:</span></span>


```C++
typedef DWORD IP4_ADDRESS;
```



<dl> <dt>

<span data-ttu-id="b606c-106">**\_Endereço ip4**</span><span class="sxs-lookup"><span data-stu-id="b606c-106">**IP4\_ADDRESS**</span></span>
</dt> <dd>

<span data-ttu-id="b606c-107">Um valor que representa um endereço IPv4 (protocolo IP versão 4).</span><span class="sxs-lookup"><span data-stu-id="b606c-107">A value that represents an Internet Protocol version 4 (IPv4) address.</span></span> <span data-ttu-id="b606c-108">Por exemplo, o endereço IPv4 de decimal pontilhado, **127.0.0.1**, é representado na ordem de bytes do host como **0x7F000001**.</span><span class="sxs-lookup"><span data-stu-id="b606c-108">For example, the dotted decimal IPv4 address, **127.0.0.1**, is represented in host byte order as **0x7F000001**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b606c-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b606c-109">Requirements</span></span>



| <span data-ttu-id="b606c-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="b606c-110">Requirement</span></span> | <span data-ttu-id="b606c-111">Valor</span><span class="sxs-lookup"><span data-stu-id="b606c-111">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b606c-112">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b606c-112">Minimum supported client</span></span><br/> | <span data-ttu-id="b606c-113">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="b606c-113">Windows 8 \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="b606c-114">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b606c-114">Minimum supported server</span></span><br/> | <span data-ttu-id="b606c-115">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="b606c-115">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="b606c-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b606c-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="b606c-117"><dt>Windns. h</dt></span><span class="sxs-lookup"><span data-stu-id="b606c-117"><dt>Windns.h</dt></span></span> </dl> |



 

 





