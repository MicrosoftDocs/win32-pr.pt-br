---
description: Desabilita este dispositivo de Plug and Play.
ms.assetid: 88d60218-7282-4d0e-9a2c-0ad1a8c96650
ms.tgt_platform: multiple
title: Método Disable da classe Win32_PnPEntity
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PnPEntity.Disable
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 59d08d14f8dbf32941554dcecc372d73c60bef60
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104500886"
---
# <a name="disable-method-of-the-win32_pnpentity-class"></a><span data-ttu-id="7e19f-103">Método Disable da classe Win32 \_ PnPEntity</span><span class="sxs-lookup"><span data-stu-id="7e19f-103">Disable method of the Win32\_PnPEntity class</span></span>

<span data-ttu-id="7e19f-104">Desabilita este dispositivo de Plug and Play.</span><span class="sxs-lookup"><span data-stu-id="7e19f-104">Disables this Plug and Play device.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e19f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7e19f-105">Syntax</span></span>


```mof
Uint32 Disable(
  [out] boolean rebootNeeded
);
```



## <a name="parameters"></a><span data-ttu-id="7e19f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7e19f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e19f-107">*rebootNeeded* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="7e19f-107">*rebootNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7e19f-108">Se uma reinicialização é necessária.</span><span class="sxs-lookup"><span data-stu-id="7e19f-108">Whether a reboot is needed.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7e19f-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7e19f-109">Requirements</span></span>



| <span data-ttu-id="7e19f-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="7e19f-110">Requirement</span></span> | <span data-ttu-id="7e19f-111">Valor</span><span class="sxs-lookup"><span data-stu-id="7e19f-111">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7e19f-112">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7e19f-112">Minimum supported client</span></span><br/> | <span data-ttu-id="7e19f-113">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="7e19f-113">Windows 10 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="7e19f-114">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7e19f-114">Minimum supported server</span></span><br/> | <span data-ttu-id="7e19f-115">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="7e19f-115">Windows Server 2016</span></span><br/>                                                          |
| <span data-ttu-id="7e19f-116">Namespace</span><span class="sxs-lookup"><span data-stu-id="7e19f-116">Namespace</span></span><br/>                | <span data-ttu-id="7e19f-117">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="7e19f-117">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7e19f-118">MOF</span><span class="sxs-lookup"><span data-stu-id="7e19f-118">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7e19f-119"><dt>Cimwin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7e19f-119"><dt>Cimwin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7e19f-120">DLL</span><span class="sxs-lookup"><span data-stu-id="7e19f-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7e19f-121"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7e19f-121"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e19f-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="7e19f-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e19f-123">**\_PnPEntity Win32**</span><span class="sxs-lookup"><span data-stu-id="7e19f-123">**Win32\_PnPEntity**</span></span>](win32-pnpentity.md)
</dt> </dl>

 

 




