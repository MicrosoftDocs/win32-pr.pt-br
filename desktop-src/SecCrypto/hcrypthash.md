---
description: O tipo de dados HCRYPTHASH é usado para representar identificadores para objetos de hash.
ms.assetid: 3b872bf0-cf1b-465b-82a2-c6fd154e1125
title: HCRYPTHASH (Wincrypt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a009350ed910627c1e6ec9ae33997ed20c7fec2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829536"
---
# <a name="hcrypthash"></a><span data-ttu-id="85315-103">HCRYPTHASH</span><span class="sxs-lookup"><span data-stu-id="85315-103">HCRYPTHASH</span></span>

<span data-ttu-id="85315-104">O tipo de dados **HCRYPTHASH** é usado para representar identificadores para [*objetos de hash*](../secgloss/h-gly.md).</span><span class="sxs-lookup"><span data-stu-id="85315-104">The **HCRYPTHASH** data type is used to represent handles to [*hash objects*](../secgloss/h-gly.md).</span></span> <span data-ttu-id="85315-105">Esses identificadores indicam ao módulo CSP qual hash está sendo usado em uma operação específica.</span><span class="sxs-lookup"><span data-stu-id="85315-105">These handles indicate to the CSP module which hash is being used in a particular operation.</span></span> <span data-ttu-id="85315-106">O módulo CSP não habilita a manipulação direta dos valores de hash.</span><span class="sxs-lookup"><span data-stu-id="85315-106">The CSP module does not enable direct manipulation of the hash values.</span></span> <span data-ttu-id="85315-107">Em vez disso, o usuário manipula os valores de hash por meio do identificador de hash.</span><span class="sxs-lookup"><span data-stu-id="85315-107">Instead, the user manipulates the hash values through the hash handle.</span></span>


```C++
typedef ULONG_PTR HCRYPTHASH;
```



## <a name="requirements"></a><span data-ttu-id="85315-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="85315-108">Requirements</span></span>



| <span data-ttu-id="85315-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="85315-109">Requirement</span></span> | <span data-ttu-id="85315-110">Valor</span><span class="sxs-lookup"><span data-stu-id="85315-110">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="85315-111">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="85315-111">Minimum supported client</span></span><br/> | <span data-ttu-id="85315-112">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="85315-112">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="85315-113">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="85315-113">Minimum supported server</span></span><br/> | <span data-ttu-id="85315-114">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="85315-114">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="85315-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="85315-115">Header</span></span><br/>                   | <dl> <span data-ttu-id="85315-116"><dt>Wincrypt. h</dt></span><span class="sxs-lookup"><span data-stu-id="85315-116"><dt>Wincrypt.h</dt></span></span> </dl> |



 

 
