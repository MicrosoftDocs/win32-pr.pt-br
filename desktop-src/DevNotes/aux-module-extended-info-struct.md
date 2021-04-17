---
description: Contém informações estendidas do módulo.
ms.assetid: 705769de-0aeb-4a28-b174-8620efa74baf
title: Estrutura de AUX_MODULE_EXTENDED_INFO (aux \_ klib. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AUX_MODULE_EXTENDED_INFO
api_type:
- HeaderDef
api_location:
- Aux_klib.h
ms.openlocfilehash: 9faa706ca3603a1796d70e2f208e9b3b2e518c45
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748098"
---
# <a name="aux_module_extended_info-structure"></a><span data-ttu-id="7a72e-103">\_Estrutura de \_ informações estendidas do módulo aux \_</span><span class="sxs-lookup"><span data-stu-id="7a72e-103">AUX\_MODULE\_EXTENDED\_INFO structure</span></span>

<span data-ttu-id="7a72e-104">Contém informações estendidas do módulo.</span><span class="sxs-lookup"><span data-stu-id="7a72e-104">Contains extended module information.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a72e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7a72e-105">Syntax</span></span>


```C++
typedef struct _AUX_MODULE_EXTENDED_INFO {
  AUX_MODULE_BASIC_INFO BasicInfo;
  ULONG                 ImageSize;
  USHORT                FileNameOffset;
  UCHAR                 FullPathName[AUX_KLIB_MODULE_PATH_LEN];
} AUX_MODULE_EXTENDED_INFO, *PAUX_MODULE_EXTENDED_INFO;
```



## <a name="members"></a><span data-ttu-id="7a72e-106">Membros</span><span class="sxs-lookup"><span data-stu-id="7a72e-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="7a72e-107">**BasicInfo**</span><span class="sxs-lookup"><span data-stu-id="7a72e-107">**BasicInfo**</span></span>
</dt> <dd>

<span data-ttu-id="7a72e-108">Uma estrutura de [**\_ \_ \_ informações básicas do módulo aux**](aux-module-basic-info-struct.md) .</span><span class="sxs-lookup"><span data-stu-id="7a72e-108">An [**AUX\_MODULE\_BASIC\_INFO**](aux-module-basic-info-struct.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="7a72e-109">**ImageSize**</span><span class="sxs-lookup"><span data-stu-id="7a72e-109">**ImageSize**</span></span>
</dt> <dd>

<span data-ttu-id="7a72e-110">O tamanho, em bytes, do módulo carregado.</span><span class="sxs-lookup"><span data-stu-id="7a72e-110">The size, in bytes, of the loaded module.</span></span>

</dd> <dt>

<span data-ttu-id="7a72e-111">**FileNameOffset**</span><span class="sxs-lookup"><span data-stu-id="7a72e-111">**FileNameOffset**</span></span>
</dt> <dd>

<span data-ttu-id="7a72e-112">O deslocamento do nome do arquivo dentro do buffer de **fullpathname** .</span><span class="sxs-lookup"><span data-stu-id="7a72e-112">The offset of the file name within the **FullPathName** buffer.</span></span>

</dd> <dt>

<span data-ttu-id="7a72e-113">**FullPathname**</span><span class="sxs-lookup"><span data-stu-id="7a72e-113">**FullPathName**</span></span>
</dt> <dd>

<span data-ttu-id="7a72e-114">O caminho completo do módulo.</span><span class="sxs-lookup"><span data-stu-id="7a72e-114">The full path of the module.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7a72e-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="7a72e-115">Remarks</span></span>

<span data-ttu-id="7a72e-116">A biblioteca de objetos que implementa essa API pode ser baixada [aqui](https://www.microsoft.com/?ref=go).</span><span class="sxs-lookup"><span data-stu-id="7a72e-116">The object library that implements this API can be downloaded from [here](https://www.microsoft.com/?ref=go).</span></span>

## <a name="requirements"></a><span data-ttu-id="7a72e-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7a72e-117">Requirements</span></span>



| <span data-ttu-id="7a72e-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="7a72e-118">Requirement</span></span> | <span data-ttu-id="7a72e-119">Valor</span><span class="sxs-lookup"><span data-stu-id="7a72e-119">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7a72e-120">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="7a72e-120">Redistributable</span></span><br/> | <span data-ttu-id="7a72e-121">Biblioteca de API auxiliar do Windows versão 1,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="7a72e-121">Windows Auxiliary API library version 1.0 or later</span></span><br/>                          |
| <span data-ttu-id="7a72e-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7a72e-122">Header</span></span><br/>          | <dl> <span data-ttu-id="7a72e-123"><dt>\_Klib aux. h</dt></span><span class="sxs-lookup"><span data-stu-id="7a72e-123"><dt>Aux\_klib.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a72e-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="7a72e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a72e-125">**AuxKlibQueryModuleInformation**</span><span class="sxs-lookup"><span data-stu-id="7a72e-125">**AuxKlibQueryModuleInformation**</span></span>](auxklibquerymoduleinformation-func.md)
</dt> <dt>

[<span data-ttu-id="7a72e-126">**\_ \_ informações básicas do módulo aux \_**</span><span class="sxs-lookup"><span data-stu-id="7a72e-126">**AUX\_MODULE\_BASIC\_INFO**</span></span>](aux-module-basic-info-struct.md)
</dt> </dl>

 

 




