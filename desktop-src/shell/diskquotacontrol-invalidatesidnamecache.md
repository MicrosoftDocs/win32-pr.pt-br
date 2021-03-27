---
description: Invalida o cache de nome de usuário da ID de segurança.
ms.assetid: 52f4a051-0caf-43c1-b190-c83c20e9fcf8
title: Método DiskQuotaControl. InvalidateSidNameCache (Dskquota. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.InvalidateSidNameCache
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 4e7202c1293d32d55e12e88671ed9960d376f63e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920750"
---
# <a name="diskquotacontrolinvalidatesidnamecache-method"></a><span data-ttu-id="dea43-103">Método DiskQuotaControl. InvalidateSidNameCache</span><span class="sxs-lookup"><span data-stu-id="dea43-103">DiskQuotaControl.InvalidateSidNameCache method</span></span>

<span data-ttu-id="dea43-104">Invalida o cache de nome de usuário da ID de segurança.</span><span class="sxs-lookup"><span data-stu-id="dea43-104">Invalidates the security ID user name cache.</span></span>

## <a name="syntax"></a><span data-ttu-id="dea43-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dea43-105">Syntax</span></span>


```JScript
DiskQuotaControl.InvalidateSidNameCache()
```



## <a name="parameters"></a><span data-ttu-id="dea43-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dea43-106">Parameters</span></span>

<span data-ttu-id="dea43-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="dea43-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="dea43-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="dea43-108">Return value</span></span>

<span data-ttu-id="dea43-109">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="dea43-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="dea43-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="dea43-110">Remarks</span></span>

<span data-ttu-id="dea43-111">Os nomes de usuário e as IDs de segurança associadas são armazenados em um cache.</span><span class="sxs-lookup"><span data-stu-id="dea43-111">User names and associated security IDs are stored in a cache.</span></span> <span data-ttu-id="dea43-112">Você pode limpar esse cache chamando **InvalidateSidNameCache**.</span><span class="sxs-lookup"><span data-stu-id="dea43-112">You can clear this cache by calling **InvalidateSidNameCache**.</span></span> <span data-ttu-id="dea43-113">Se você criar subseqüentemente um novo objeto de usuário, as informações precisarão ser obtidas no controlador de domínio e o cache precisará ser restabelecido.</span><span class="sxs-lookup"><span data-stu-id="dea43-113">If you subsequently create a new user object, the information will have to be obtained from the domain controller, and the cache will have to be reestablished.</span></span>

## <a name="requirements"></a><span data-ttu-id="dea43-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dea43-114">Requirements</span></span>



| <span data-ttu-id="dea43-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="dea43-115">Requirement</span></span> | <span data-ttu-id="dea43-116">Valor</span><span class="sxs-lookup"><span data-stu-id="dea43-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dea43-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dea43-117">Minimum supported client</span></span><br/> | <span data-ttu-id="dea43-118">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="dea43-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="dea43-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dea43-119">Minimum supported server</span></span><br/> | <span data-ttu-id="dea43-120">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="dea43-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="dea43-121">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="dea43-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="dea43-122"><dt>Dskquota. h</dt></span><span class="sxs-lookup"><span data-stu-id="dea43-122"><dt>Dskquota.h</dt></span></span> </dl>                         |
| <span data-ttu-id="dea43-123">DLL</span><span class="sxs-lookup"><span data-stu-id="dea43-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dea43-124"><dt>Shell32.dll (versão 5,0 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="dea43-124"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dea43-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="dea43-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dea43-126">**Objeto DiskQuotaControl**</span><span class="sxs-lookup"><span data-stu-id="dea43-126">**DiskQuotaControl Object**</span></span>](diskquotacontrol-object.md)
</dt> </dl>

 

 




