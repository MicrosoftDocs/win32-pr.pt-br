---
title: Estrutura de WMDRM_ENCRYPT_SCATTER_INFO (wmdrmsdk. h)
description: A \_ estrutura de informações de dispersão do WMDRM Encrypt \_ \_ contém as informações necessárias para configurar a interface IWMDRMEncryptScatter para uso.
ms.assetid: 25e19511-56ac-441b-b521-5097dd792ead
keywords:
- Formato de mídia do Windows de estrutura de WMDRM_ENCRYPT_SCATTER_INFO
- estruturar formato de mídia do Windows
topic_type:
- apiref
api_name:
- WMDRM_ENCRYPT_SCATTER_INFO
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 500012231f6860fd94038b240355eda9aa2aee44
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105793998"
---
# <a name="wmdrm_encrypt_scatter_info-structure"></a><span data-ttu-id="1af20-105">\_Estrutura de \_ informações de dispersão do WMDRM Encrypt \_</span><span class="sxs-lookup"><span data-stu-id="1af20-105">WMDRM\_ENCRYPT\_SCATTER\_INFO structure</span></span>

<span data-ttu-id="1af20-106">A estrutura de **\_ \_ \_ informações de dispersão do WMDRM Encrypt** contém as informações necessárias para configurar a interface [**IWMDRMEncryptScatter**](iwmdrmencryptscatter.md) para uso.</span><span class="sxs-lookup"><span data-stu-id="1af20-106">The **WMDRM\_ENCRYPT\_SCATTER\_INFO** structure contains information needed to configure the [**IWMDRMEncryptScatter**](iwmdrmencryptscatter.md) interface for use.</span></span>

## <a name="syntax"></a><span data-ttu-id="1af20-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1af20-107">Syntax</span></span>


```C++
typedef struct WMDRM_ENCRYPT_SCATTER_INFO {
  DWORD dwStreamID;
  DWORD dwSampleProtectionVersion;
  DWORD cbProtectionInfo;
  BYTE  *pbProtectionInfo;
} ;
```



## <a name="members"></a><span data-ttu-id="1af20-108">Membros</span><span class="sxs-lookup"><span data-stu-id="1af20-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="1af20-109">**dwStreamID**</span><span class="sxs-lookup"><span data-stu-id="1af20-109">**dwStreamID**</span></span>
</dt> <dd>

<span data-ttu-id="1af20-110">Identificador do fluxo a ser criptografado.</span><span class="sxs-lookup"><span data-stu-id="1af20-110">Identifier of the stream to be encrypted.</span></span>

</dd> <dt>

<span data-ttu-id="1af20-111">**dwSampleProtectionVersion**</span><span class="sxs-lookup"><span data-stu-id="1af20-111">**dwSampleProtectionVersion**</span></span>
</dt> <dd>

<span data-ttu-id="1af20-112">Versão de proteção de exemplo a ser usada para codificar dados do fluxo especificado.</span><span class="sxs-lookup"><span data-stu-id="1af20-112">Sample protection version to be used to encode data from the specified stream.</span></span>

</dd> <dt>

<span data-ttu-id="1af20-113">**cbProtectionInfo**</span><span class="sxs-lookup"><span data-stu-id="1af20-113">**cbProtectionInfo**</span></span>
</dt> <dd>

<span data-ttu-id="1af20-114">Tamanho do buffer **pbProtectionInfo** em bytes.</span><span class="sxs-lookup"><span data-stu-id="1af20-114">Size of the **pbProtectionInfo** buffer in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="1af20-115">**pbProtectionInfo**</span><span class="sxs-lookup"><span data-stu-id="1af20-115">**pbProtectionInfo**</span></span>
</dt> <dd>

<span data-ttu-id="1af20-116">Buffer que contém informações adicionais de proteção.</span><span class="sxs-lookup"><span data-stu-id="1af20-116">Buffer containing additional protection information.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1af20-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="1af20-117">Remarks</span></span>

<span data-ttu-id="1af20-118">Essa estrutura é usada pelo método [**IWMDRMEncryptScatter:: InitEncryptScatter**](iwmdrmencryptscatter-initencryptscatter.md) .</span><span class="sxs-lookup"><span data-stu-id="1af20-118">This structure is used by the [**IWMDRMEncryptScatter::InitEncryptScatter**](iwmdrmencryptscatter-initencryptscatter.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="1af20-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1af20-119">Requirements</span></span>



| <span data-ttu-id="1af20-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="1af20-120">Requirement</span></span> | <span data-ttu-id="1af20-121">Valor</span><span class="sxs-lookup"><span data-stu-id="1af20-121">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1af20-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1af20-122">Header</span></span><br/> | <dl> <span data-ttu-id="1af20-123"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="1af20-123"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1af20-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="1af20-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1af20-125">**Estruturas**</span><span class="sxs-lookup"><span data-stu-id="1af20-125">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





