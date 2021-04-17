---
description: Contém informações básicas do módulo.
ms.assetid: 5cdb0b11-8bd3-46d2-b214-85cdb2f274a7
title: Estrutura de AUX_MODULE_BASIC_INFO (aux \_ klib. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AUX_MODULE_BASIC_INFO
api_type:
- HeaderDef
api_location:
- Aux_klib.h
ms.openlocfilehash: 1ee7300ec2c2d84e1ddadc4149135dab53d2336b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752575"
---
# <a name="aux_module_basic_info-structure"></a><span data-ttu-id="a015c-103">\_Estrutura de \_ informações básicas do módulo aux \_</span><span class="sxs-lookup"><span data-stu-id="a015c-103">AUX\_MODULE\_BASIC\_INFO structure</span></span>

<span data-ttu-id="a015c-104">Contém informações básicas do módulo.</span><span class="sxs-lookup"><span data-stu-id="a015c-104">Contains basic module information.</span></span>

## <a name="syntax"></a><span data-ttu-id="a015c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a015c-105">Syntax</span></span>


```C++
typedef struct _AUX_MODULE_BASIC_INFO {
  PVOID ImageBase;
} AUX_MODULE_BASIC_INFO, *PAUX_MODULE_BASIC_INFO;
```



## <a name="members"></a><span data-ttu-id="a015c-106">Membros</span><span class="sxs-lookup"><span data-stu-id="a015c-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="a015c-107">**ImageBase**</span><span class="sxs-lookup"><span data-stu-id="a015c-107">**ImageBase**</span></span>
</dt> <dd>

<span data-ttu-id="a015c-108">O endereço base do módulo dentro do espaço de endereço do kernel.</span><span class="sxs-lookup"><span data-stu-id="a015c-108">The base address of the module within the kernel's address space.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a015c-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="a015c-109">Remarks</span></span>

<span data-ttu-id="a015c-110">A biblioteca de objetos que implementa essa API pode ser baixada [aqui](https://www.microsoft.com/?ref=go).</span><span class="sxs-lookup"><span data-stu-id="a015c-110">The object library that implements this API can be downloaded from [here](https://www.microsoft.com/?ref=go).</span></span>

## <a name="requirements"></a><span data-ttu-id="a015c-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a015c-111">Requirements</span></span>



| <span data-ttu-id="a015c-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="a015c-112">Requirement</span></span> | <span data-ttu-id="a015c-113">Valor</span><span class="sxs-lookup"><span data-stu-id="a015c-113">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a015c-114">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="a015c-114">Redistributable</span></span><br/> | <span data-ttu-id="a015c-115">Biblioteca de API auxiliar do Windows versão 1,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="a015c-115">Windows Auxiliary API library version 1.0 or later</span></span><br/>                          |
| <span data-ttu-id="a015c-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a015c-116">Header</span></span><br/>          | <dl> <span data-ttu-id="a015c-117"><dt>\_Klib aux. h</dt></span><span class="sxs-lookup"><span data-stu-id="a015c-117"><dt>Aux\_klib.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a015c-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="a015c-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a015c-119">**AuxKlibQueryModuleInformation**</span><span class="sxs-lookup"><span data-stu-id="a015c-119">**AuxKlibQueryModuleInformation**</span></span>](auxklibquerymoduleinformation-func.md)
</dt> </dl>

 

 




