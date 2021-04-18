---
title: Estrutura de WMDRM_LICENSE_FILTER (wmdrmsdk. h)
description: A estrutura do filtro de licença do WMDRM \_ define os \_ parâmetros de filtragem para uso ao criar uma enumeração de licenças.
ms.assetid: 43bbbfdc-1ec4-44a6-8245-96853bbeea86
keywords:
- Formato de mídia do Windows de estrutura de WMDRM_LICENSE_FILTER
- estruturar formato de mídia do Windows
topic_type:
- apiref
api_name:
- WMDRM_LICENSE_FILTER
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9200bea0d74b7c9a84c5731072e2e65bca81b6cf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105763891"
---
# <a name="wmdrm_license_filter-structure"></a><span data-ttu-id="c9d39-105">Estrutura de filtro de \_ licença WMDRM \_</span><span class="sxs-lookup"><span data-stu-id="c9d39-105">WMDRM\_LICENSE\_FILTER structure</span></span>

<span data-ttu-id="c9d39-106">A estrutura do **\_ \_ filtro de licença do WMDRM** define os parâmetros de filtragem para uso ao criar uma enumeração de licenças.</span><span class="sxs-lookup"><span data-stu-id="c9d39-106">The **WMDRM\_LICENSE\_FILTER** structure defines filtering parameters for use when creating a license enumeration.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9d39-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c9d39-107">Syntax</span></span>


```C++
typedef struct WMDRM_LICENSE_FILTER {
  DWORD dwVersion;
  BSTR  bstrKID;
  BSTR  bstrRights;
  BSTR  bstrAllowedSourceIDs;
} ;
```



## <a name="members"></a><span data-ttu-id="c9d39-108">Membros</span><span class="sxs-lookup"><span data-stu-id="c9d39-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="c9d39-109">**DW**</span><span class="sxs-lookup"><span data-stu-id="c9d39-109">**dwVersion**</span></span>
</dt> <dd>

<span data-ttu-id="c9d39-110">Especifica um número de versão mínimo para as licenças retornadas.</span><span class="sxs-lookup"><span data-stu-id="c9d39-110">Specifies a minimum version number for the returned licenses.</span></span>

</dd> <dt>

<span data-ttu-id="c9d39-111">**bstrKID**</span><span class="sxs-lookup"><span data-stu-id="c9d39-111">**bstrKID**</span></span>
</dt> <dd>

<span data-ttu-id="c9d39-112">Especifica uma ID de chave para filtrar licenças.</span><span class="sxs-lookup"><span data-stu-id="c9d39-112">Specifies a key ID to filter licenses for.</span></span> <span data-ttu-id="c9d39-113">Somente as licenças com a ID de chave especificada serão incluídas na enumeração.</span><span class="sxs-lookup"><span data-stu-id="c9d39-113">Only licenses with the specified key ID will be included in the enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="c9d39-114">**bstrRights**</span><span class="sxs-lookup"><span data-stu-id="c9d39-114">**bstrRights**</span></span>
</dt> <dd>

<span data-ttu-id="c9d39-115">Especifica um conjunto de direitos para filtrar licenças para.</span><span class="sxs-lookup"><span data-stu-id="c9d39-115">Specifies a set of rights to filter licenses for.</span></span> <span data-ttu-id="c9d39-116">Somente as licenças que fornecem todos os direitos especificados serão incluídas na enumeração.</span><span class="sxs-lookup"><span data-stu-id="c9d39-116">Only licenses that provide all of the specified rights will be included in the enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="c9d39-117">**bstrAllowedSourceIDs**</span><span class="sxs-lookup"><span data-stu-id="c9d39-117">**bstrAllowedSourceIDs**</span></span>
</dt> <dd>

<span data-ttu-id="c9d39-118">Especifica as fontes de conteúdo protegido a serem incluídas na pesquisa de licença.</span><span class="sxs-lookup"><span data-stu-id="c9d39-118">Specifies the sources of protected content to include in the license search.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c9d39-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="c9d39-119">Remarks</span></span>

<span data-ttu-id="c9d39-120">Essa estrutura é usada pelo método [**IWMDRMLicenseManagement:: CreateLicenseEnumeration**](iwmdrmlicensemanagement-createlicenseenumeration.md) .</span><span class="sxs-lookup"><span data-stu-id="c9d39-120">This structure is used by the [**IWMDRMLicenseManagement::CreateLicenseEnumeration**](iwmdrmlicensemanagement-createlicenseenumeration.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9d39-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c9d39-121">Requirements</span></span>



| <span data-ttu-id="c9d39-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="c9d39-122">Requirement</span></span> | <span data-ttu-id="c9d39-123">Valor</span><span class="sxs-lookup"><span data-stu-id="c9d39-123">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c9d39-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c9d39-124">Header</span></span><br/> | <dl> <span data-ttu-id="c9d39-125"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="c9d39-125"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9d39-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="c9d39-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9d39-127">**Estruturas**</span><span class="sxs-lookup"><span data-stu-id="c9d39-127">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





