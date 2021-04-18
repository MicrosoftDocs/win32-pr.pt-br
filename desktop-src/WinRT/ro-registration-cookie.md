---
description: Representa as fábricas de ativação registradas chamando a função RoRegisterActivationFactories.
ms.assetid: D74E5886-45DB-40DE-9740-D14341E78713
title: RO_REGISTRATION_COOKIE (Roapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe9b5242901c1beff4152bc16108976d6f7de275
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105814058"
---
# <a name="ro_registration_cookie"></a><span data-ttu-id="00914-103">\_cookie de registro ro \_</span><span class="sxs-lookup"><span data-stu-id="00914-103">RO\_REGISTRATION\_COOKIE</span></span>

<span data-ttu-id="00914-104">Representa as fábricas de ativação registradas chamando a função [**RoRegisterActivationFactories**](/windows/win32/api/roapi/nf-roapi-roregisteractivationfactories) .</span><span class="sxs-lookup"><span data-stu-id="00914-104">Represents activation factories that are registered by calling the [**RoRegisterActivationFactories**](/windows/win32/api/roapi/nf-roapi-roregisteractivationfactories) function.</span></span>


```C++
typedef struct {}* RO_REGISTRATION_COOKIE;
```



## <a name="remarks"></a><span data-ttu-id="00914-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="00914-105">Remarks</span></span>

<span data-ttu-id="00914-106">A função [**RoRegisterActivationFactories**](/windows/win32/api/roapi/nf-roapi-roregisteractivationfactories) retorna um **\_ \_ Cookie ro de registro** quando uma fábricas de classe ativável é registrada com o Windows Runtime.</span><span class="sxs-lookup"><span data-stu-id="00914-106">The [**RoRegisterActivationFactories**](/windows/win32/api/roapi/nf-roapi-roregisteractivationfactories) function returns a **RO\_REGISTRATION\_COOKIE** when a activatable class factories are registered with the Windows Runtime.</span></span> <span data-ttu-id="00914-107">A função [**RoRevokeActivationFactories**](/windows/win32/api/roapi/nf-roapi-rorevokeactivationfactories) usa o cookie para remover as fábricas de classes.</span><span class="sxs-lookup"><span data-stu-id="00914-107">The [**RoRevokeActivationFactories**](/windows/win32/api/roapi/nf-roapi-rorevokeactivationfactories) function uses the cookie to remove the class factories.</span></span>

## <a name="requirements"></a><span data-ttu-id="00914-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="00914-108">Requirements</span></span>



| <span data-ttu-id="00914-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="00914-109">Requirement</span></span> | <span data-ttu-id="00914-110">Valor</span><span class="sxs-lookup"><span data-stu-id="00914-110">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="00914-111">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="00914-111">Minimum supported client</span></span><br/> | <span data-ttu-id="00914-112">Windows 8</span><span class="sxs-lookup"><span data-stu-id="00914-112">Windows 8</span></span><br/>                                                               |
| <span data-ttu-id="00914-113">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="00914-113">Minimum supported server</span></span><br/> | <span data-ttu-id="00914-114">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="00914-114">Windows Server 2012</span></span><br/>                                                     |
| <span data-ttu-id="00914-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="00914-115">Header</span></span><br/>                   | <dl> <span data-ttu-id="00914-116"><dt>Roapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="00914-116"><dt>Roapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="00914-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="00914-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00914-118">**RoRegisterActivationFactories**</span><span class="sxs-lookup"><span data-stu-id="00914-118">**RoRegisterActivationFactories**</span></span>](/windows/win32/api/roapi/nf-roapi-roregisteractivationfactories)
</dt> <dt>

[<span data-ttu-id="00914-119">**RoRevokeActivationFactories**</span><span class="sxs-lookup"><span data-stu-id="00914-119">**RoRevokeActivationFactories**</span></span>](/windows/win32/api/roapi/nf-roapi-rorevokeactivationfactories)
</dt> </dl>

 

 
