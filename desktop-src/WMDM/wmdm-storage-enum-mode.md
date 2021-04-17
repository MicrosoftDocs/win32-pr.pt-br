---
title: Enumeração de WMDM_STORAGE_ENUM_MODE
description: O \_ tipo de enumeração do modo enum de armazenamento do WMDM \_ \_ define como o conteúdo no armazenamento deve ser enumerado. Essa enumeração é usada por IWMDMStorage3 SetEnumPreference.
ms.assetid: 38293e54-92e4-4f0a-bdea-5dc684a9548b
keywords:
- WMDM_STORAGE_ENUM_MODE de enumeração do Windows Media Gerenciador de Dispositivos
topic_type:
- apiref
api_name:
- WMDM_STORAGE_ENUM_MODE
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d886ade00289e655ae3323a70d01be96a09852b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105789589"
---
# <a name="wmdm_storage_enum_mode-enumeration"></a><span data-ttu-id="26f53-105">\_Enumeração do \_ modo de enumeração de armazenamento WMDM \_</span><span class="sxs-lookup"><span data-stu-id="26f53-105">WMDM\_STORAGE\_ENUM\_MODE enumeration</span></span>

<span data-ttu-id="26f53-106">O tipo de enumeração do **\_ \_ \_ modo enum de armazenamento do WMDM** define como o conteúdo no armazenamento deve ser enumerado.</span><span class="sxs-lookup"><span data-stu-id="26f53-106">The **WMDM\_STORAGE\_ENUM\_MODE** enumeration type defines how the content on the storage is to be enumerated.</span></span> <span data-ttu-id="26f53-107">Essa enumeração é usada por [**IWMDMStorage3:: SetEnumPreference**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-setenumpreference).</span><span class="sxs-lookup"><span data-stu-id="26f53-107">This enumeration is used by [**IWMDMStorage3::SetEnumPreference**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-setenumpreference).</span></span>

## <a name="syntax"></a><span data-ttu-id="26f53-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="26f53-108">Syntax</span></span>


```C++
typedef enum tagWMDM_STORAGE_ENUM_MODE { 
  ENUM_MODE_RAW,
  ENUM_MODE_USE_DEVICE_PREF,
  ENUM_MODE_METADATA_VIEWS
} WMDM_STORAGE_ENUM_MODE;
```



## <a name="constants"></a><span data-ttu-id="26f53-109">Constantes</span><span class="sxs-lookup"><span data-stu-id="26f53-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="26f53-110"><span id="ENUM_MODE_RAW"></span><span id="enum_mode_raw"></span>**modo de enumeração \_ \_ bruto**</span><span class="sxs-lookup"><span data-stu-id="26f53-110"><span id="ENUM_MODE_RAW"></span><span id="enum_mode_raw"></span>**ENUM\_MODE\_RAW**</span></span>
</dt> <dd>

<span data-ttu-id="26f53-111">Enumera o conteúdo no armazenamento da mesma forma que ele é organizado no sistema de arquivos do armazenamento.</span><span class="sxs-lookup"><span data-stu-id="26f53-111">Enumerates content on the storage just as it is organized in the file system of the storage.</span></span>

<span data-ttu-id="26f53-112">**o \_ modo de enumeração \_ usa o \_ dispositivo \_ pref**</span><span class="sxs-lookup"><span data-stu-id="26f53-112">**ENUM\_MODE\_USE\_DEVICE\_PREF**</span></span>

<span data-ttu-id="26f53-113">Enumera o conteúdo no armazenamento com base na preferência do dispositivo, conforme indicado pelo parâmetro do dispositivo *UseMetadataViews* .</span><span class="sxs-lookup"><span data-stu-id="26f53-113">Enumerates content on the storage based on the device preference as indicated by the *UseMetadataViews* device parameter.</span></span>

<span data-ttu-id="26f53-114">**\_modos de \_ exibição de metadados do modo de enumeração \_**</span><span class="sxs-lookup"><span data-stu-id="26f53-114">**ENUM\_MODE\_METADATA\_VIEWS**</span></span>

<span data-ttu-id="26f53-115">Enumera o conteúdo no armazenamento organizando o conteúdo com base em uma exibição de metadados.</span><span class="sxs-lookup"><span data-stu-id="26f53-115">Enumerates content on the storage by organizing the content based on a metadata view.</span></span>

</dd> <dt>

<span data-ttu-id="26f53-116"><span id="ENUM_MODE_USE_DEVICE_PREF"></span><span id="enum_mode_use_device_pref"></span>**o \_ modo de enumeração \_ usa o \_ dispositivo \_ pref**</span><span class="sxs-lookup"><span data-stu-id="26f53-116"><span id="ENUM_MODE_USE_DEVICE_PREF"></span><span id="enum_mode_use_device_pref"></span>**ENUM\_MODE\_USE\_DEVICE\_PREF**</span></span>
</dt> <dd>

<span data-ttu-id="26f53-117">Enumera o conteúdo no armazenamento com base na preferência do dispositivo, conforme indicado pelo parâmetro do dispositivo *UseMetadataViews* .</span><span class="sxs-lookup"><span data-stu-id="26f53-117">Enumerates content on the storage based on the device preference as indicated by the *UseMetadataViews* device parameter.</span></span>

<span data-ttu-id="26f53-118">**\_modos de \_ exibição de metadados do modo de enumeração \_**</span><span class="sxs-lookup"><span data-stu-id="26f53-118">**ENUM\_MODE\_METADATA\_VIEWS**</span></span>

<span data-ttu-id="26f53-119">Enumera o conteúdo no armazenamento organizando o conteúdo com base em uma exibição de metadados.</span><span class="sxs-lookup"><span data-stu-id="26f53-119">Enumerates content on the storage by organizing the content based on a metadata view.</span></span>

</dd> <dt>

<span data-ttu-id="26f53-120"><span id="ENUM_MODE_METADATA_VIEWS"></span><span id="enum_mode_metadata_views"></span>**\_modos de \_ exibição de metadados do modo de enumeração \_**</span><span class="sxs-lookup"><span data-stu-id="26f53-120"><span id="ENUM_MODE_METADATA_VIEWS"></span><span id="enum_mode_metadata_views"></span>**ENUM\_MODE\_METADATA\_VIEWS**</span></span>
</dt> <dd>

<span data-ttu-id="26f53-121">Enumera o conteúdo no armazenamento organizando o conteúdo com base em uma exibição de metadados.</span><span class="sxs-lookup"><span data-stu-id="26f53-121">Enumerates content on the storage by organizing the content based on a metadata view.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="26f53-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="26f53-122">Requirements</span></span>



| <span data-ttu-id="26f53-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="26f53-123">Requirement</span></span> | <span data-ttu-id="26f53-124">Valor</span><span class="sxs-lookup"><span data-stu-id="26f53-124">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="26f53-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="26f53-125">Header</span></span><br/> | <dl> <span data-ttu-id="26f53-126"><dt>WMDM. idl</dt></span><span class="sxs-lookup"><span data-stu-id="26f53-126"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26f53-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="26f53-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26f53-128">**Tipos de enumeração**</span><span class="sxs-lookup"><span data-stu-id="26f53-128">**Enumeration Types**</span></span>](enumeration-types.md)
</dt> </dl>

 

 





