---
title: Enumeração de WMDM_FIND_SCOPE
description: O \_ tipo de \_ enumeração de escopo do WMDM Find define o escopo do objeto de armazenamento.
ms.assetid: 971f84d5-8383-4b38-a201-b21100b2f37e
keywords:
- WMDM_FIND_SCOPE de enumeração do Windows Media Gerenciador de Dispositivos
topic_type:
- apiref
api_name:
- WMDM_FIND_SCOPE
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d6b65489d14a4f1100b1da33238669310a2731f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761127"
---
# <a name="wmdm_find_scope-enumeration"></a><span data-ttu-id="076ba-104">Enumeração de escopo do WMDM \_ Find \_</span><span class="sxs-lookup"><span data-stu-id="076ba-104">WMDM\_FIND\_SCOPE enumeration</span></span>

<span data-ttu-id="076ba-105">O tipo de enumeração de **\_ \_ escopo do WMDM Find** define o escopo do objeto de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="076ba-105">The **WMDM\_FIND\_SCOPE** enumeration type defines the scope of the storage object.</span></span>

## <a name="syntax"></a><span data-ttu-id="076ba-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="076ba-106">Syntax</span></span>


```C++
typedef enum tagWMDM_FIND_SCOPE { 
  WMDM_FIND_SCOPE_GLOBAL,
  WMDM_FIND_SCOPE_IMMEDIATE_CHILDREN
} WMDM_FIND_SCOPE;
```



## <a name="constants"></a><span data-ttu-id="076ba-107">Constantes</span><span class="sxs-lookup"><span data-stu-id="076ba-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="076ba-108"><span id="WMDM_FIND_SCOPE_GLOBAL"></span><span id="wmdm_find_scope_global"></span>**WMDM \_ localizar \_ escopo \_ global**</span><span class="sxs-lookup"><span data-stu-id="076ba-108"><span id="WMDM_FIND_SCOPE_GLOBAL"></span><span id="wmdm_find_scope_global"></span>**WMDM\_FIND\_SCOPE\_GLOBAL**</span></span>
</dt> <dd>

<span data-ttu-id="076ba-109">Procurando o objeto correspondente em qualquer lugar do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="076ba-109">Looking for the matching object anywhere on the device.</span></span>

</dd> <dt>

<span data-ttu-id="076ba-110"><span id="WMDM_FIND_SCOPE_IMMEDIATE_CHILDREN"></span><span id="wmdm_find_scope_immediate_children"></span>**\_filhos de localizar \_ escopo \_ IMEDIATOs do \_ WMDM**</span><span class="sxs-lookup"><span data-stu-id="076ba-110"><span id="WMDM_FIND_SCOPE_IMMEDIATE_CHILDREN"></span><span id="wmdm_find_scope_immediate_children"></span>**WMDM\_FIND\_SCOPE\_IMMEDIATE\_CHILDREN**</span></span>
</dt> <dd>

<span data-ttu-id="076ba-111">Procurando o objeto correspondente nesse armazenamento e seus filhos.</span><span class="sxs-lookup"><span data-stu-id="076ba-111">Looking for the matching object within this storage and its children.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="076ba-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="076ba-112">Requirements</span></span>



| <span data-ttu-id="076ba-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="076ba-113">Requirement</span></span> | <span data-ttu-id="076ba-114">Valor</span><span class="sxs-lookup"><span data-stu-id="076ba-114">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="076ba-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="076ba-115">Header</span></span><br/> | <dl> <span data-ttu-id="076ba-116"><dt>WMDM. idl</dt></span><span class="sxs-lookup"><span data-stu-id="076ba-116"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="076ba-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="076ba-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="076ba-118">**Tipos de enumeração**</span><span class="sxs-lookup"><span data-stu-id="076ba-118">**Enumeration Types**</span></span>](enumeration-types.md)
</dt> </dl>

 

 





