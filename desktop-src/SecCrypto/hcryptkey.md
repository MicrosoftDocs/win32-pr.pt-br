---
description: O tipo de dados HCRYPTKEY é usado para representar identificadores para chaves de criptografia.
ms.assetid: d62f1d40-4f42-4684-96d7-de88db67dceb
title: HCRYPTKEY (Wincrypt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56bda14169aa2f4d7c6e502d3444473ea0f00408
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105770340"
---
# <a name="hcryptkey"></a><span data-ttu-id="d56e5-103">HCRYPTKEY</span><span class="sxs-lookup"><span data-stu-id="d56e5-103">HCRYPTKEY</span></span>

<span data-ttu-id="d56e5-104">O tipo de dados **HCRYPTKEY** é usado para representar identificadores para [*chaves de criptografia*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="d56e5-104">The **HCRYPTKEY** data type is used to represent handles to [*cryptographic keys*](../secgloss/c-gly.md).</span></span> <span data-ttu-id="d56e5-105">Esses identificadores são usados para indicar ao módulo CSP qual chave está sendo usada em uma operação específica.</span><span class="sxs-lookup"><span data-stu-id="d56e5-105">These handles are used to indicate to the CSP module which key is being used in a specific operation.</span></span> <span data-ttu-id="d56e5-106">O módulo CSP não habilita o acesso direto aos valores de chave.</span><span class="sxs-lookup"><span data-stu-id="d56e5-106">The CSP module does not enable direct access to the key values.</span></span> <span data-ttu-id="d56e5-107">Em vez disso, o usuário executa funções usando o valor de chave por meio do identificador de chave.</span><span class="sxs-lookup"><span data-stu-id="d56e5-107">Instead, the user performs functions by using the key value through the key handle.</span></span>


```C++
typedef ULONG_PTR HCRYPTKEY;
```



## <a name="requirements"></a><span data-ttu-id="d56e5-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d56e5-108">Requirements</span></span>



| <span data-ttu-id="d56e5-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="d56e5-109">Requirement</span></span> | <span data-ttu-id="d56e5-110">Valor</span><span class="sxs-lookup"><span data-stu-id="d56e5-110">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d56e5-111">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d56e5-111">Minimum supported client</span></span><br/> | <span data-ttu-id="d56e5-112">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="d56e5-112">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="d56e5-113">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d56e5-113">Minimum supported server</span></span><br/> | <span data-ttu-id="d56e5-114">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d56e5-114">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d56e5-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d56e5-115">Header</span></span><br/>                   | <dl> <span data-ttu-id="d56e5-116"><dt>Wincrypt. h</dt></span><span class="sxs-lookup"><span data-stu-id="d56e5-116"><dt>Wincrypt.h</dt></span></span> </dl> |



 

 
