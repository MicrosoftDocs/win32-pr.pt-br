---
title: Enumeração de WMDM_SESSION_TYPE
description: O \_ tipo de enumeração do tipo de sessão WMDM \_ define o tipo de sessão.
ms.assetid: e4ed41c0-521f-4da0-8361-287b64d74d77
keywords:
- WMDM_SESSION_TYPE de enumeração do Windows Media Gerenciador de Dispositivos
topic_type:
- apiref
api_name:
- WMDM_SESSION_TYPE
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84322986266143e5ff4ecc469c56504f29de9e3a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760479"
---
# <a name="wmdm_session_type-enumeration"></a><span data-ttu-id="f9753-104">Enumeração de tipo de \_ sessão WMDM \_</span><span class="sxs-lookup"><span data-stu-id="f9753-104">WMDM\_SESSION\_TYPE enumeration</span></span>

<span data-ttu-id="f9753-105">O tipo de enumeração do **\_ \_ tipo de sessão WMDM** define o tipo de sessão.</span><span class="sxs-lookup"><span data-stu-id="f9753-105">The **WMDM\_SESSION\_TYPE** enumeration type defines the session type.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9753-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="f9753-106">Syntax</span></span>


```C++
typedef enum tagWMDM_SESSION_TYPE { 
  WMDM_SESSION_NONE,
  WMDM_SESSION_TRANSFER_TO_DEVICE,
  WMDM_SESSION_TRANSFER_FROM_DEVICE,
  WMDM_SESSION_DELETE,
  WMDM_SESSION_CUSTOM
} WMDM_SESSION_TYPE;
```



## <a name="constants"></a><span data-ttu-id="f9753-107">Constantes</span><span class="sxs-lookup"><span data-stu-id="f9753-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="f9753-108"><span id="WMDM_SESSION_NONE"></span><span id="wmdm_session_none"></span>**\_sessão WMDM \_ nenhum**</span><span class="sxs-lookup"><span data-stu-id="f9753-108"><span id="WMDM_SESSION_NONE"></span><span id="wmdm_session_none"></span>**WMDM\_SESSION\_NONE**</span></span>
</dt> <dd>

<span data-ttu-id="f9753-109">A sessão não está definida.</span><span class="sxs-lookup"><span data-stu-id="f9753-109">The session is not defined.</span></span>

</dd> <dt>

<span data-ttu-id="f9753-110"><span id="WMDM_SESSION_TRANSFER_TO_DEVICE"></span><span id="wmdm_session_transfer_to_device"></span>**\_transferência de sessão do WMDM \_ para o \_ \_ dispositivo**</span><span class="sxs-lookup"><span data-stu-id="f9753-110"><span id="WMDM_SESSION_TRANSFER_TO_DEVICE"></span><span id="wmdm_session_transfer_to_device"></span>**WMDM\_SESSION\_TRANSFER\_TO\_DEVICE**</span></span>
</dt> <dd>

<span data-ttu-id="f9753-111">A sessão é definida como transferindo dados para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f9753-111">The session is defined as transferring data to the device.</span></span>

</dd> <dt>

<span data-ttu-id="f9753-112"><span id="WMDM_SESSION_TRANSFER_FROM_DEVICE"></span><span id="wmdm_session_transfer_from_device"></span>**\_ \_ transferência de sessão \_ do WMDM do \_ dispositivo**</span><span class="sxs-lookup"><span data-stu-id="f9753-112"><span id="WMDM_SESSION_TRANSFER_FROM_DEVICE"></span><span id="wmdm_session_transfer_from_device"></span>**WMDM\_SESSION\_TRANSFER\_FROM\_DEVICE**</span></span>
</dt> <dd>

<span data-ttu-id="f9753-113">A sessão é definida como transferência de dados do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f9753-113">The session is defined as transferring data from the device.</span></span>

</dd> <dt>

<span data-ttu-id="f9753-114"><span id="WMDM_SESSION_DELETE"></span><span id="wmdm_session_delete"></span>**\_exclusão da sessão do WMDM \_**</span><span class="sxs-lookup"><span data-stu-id="f9753-114"><span id="WMDM_SESSION_DELETE"></span><span id="wmdm_session_delete"></span>**WMDM\_SESSION\_DELETE**</span></span>
</dt> <dd>

<span data-ttu-id="f9753-115">A sessão é definida como excluindo dados.</span><span class="sxs-lookup"><span data-stu-id="f9753-115">The session is defined as deleting data.</span></span>

</dd> <dt>

<span data-ttu-id="f9753-116"><span id="WMDM_SESSION_CUSTOM"></span><span id="wmdm_session_custom"></span>**\_sessão \_ personalizada do WMDM**</span><span class="sxs-lookup"><span data-stu-id="f9753-116"><span id="WMDM_SESSION_CUSTOM"></span><span id="wmdm_session_custom"></span>**WMDM\_SESSION\_CUSTOM**</span></span>
</dt> <dd>

<span data-ttu-id="f9753-117">A sessão é definida como uma sessão Personalizada.</span><span class="sxs-lookup"><span data-stu-id="f9753-117">The session is defined as a custom session.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f9753-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f9753-118">Requirements</span></span>



| <span data-ttu-id="f9753-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="f9753-119">Requirement</span></span> | <span data-ttu-id="f9753-120">Valor</span><span class="sxs-lookup"><span data-stu-id="f9753-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="f9753-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f9753-121">Header</span></span><br/> | <dl> <span data-ttu-id="f9753-122"><dt>WMDM. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f9753-122"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9753-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="f9753-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9753-124">**Tipos de enumeração**</span><span class="sxs-lookup"><span data-stu-id="f9753-124">**Enumeration Types**</span></span>](enumeration-types.md)
</dt> </dl>

 

 





