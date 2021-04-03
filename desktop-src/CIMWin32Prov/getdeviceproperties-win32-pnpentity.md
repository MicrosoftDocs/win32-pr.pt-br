---
description: Obtém as propriedades especificadas deste Plug and Play dispositivo.
ms.assetid: 63327a4f-7d4a-4041-b58d-7a852ba08d5b
ms.tgt_platform: multiple
title: Método deviceproperties da classe Win32_PnPEntity
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PnPEntity.GetDeviceProperties
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6aa9f6cad17fe48617b5bf7d28ba19d6f5370834
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010157"
---
# <a name="getdeviceproperties-method-of-the-win32_pnpentity-class"></a><span data-ttu-id="1119d-103">Método deviceproperties da \_ classe Win32 PnPEntity</span><span class="sxs-lookup"><span data-stu-id="1119d-103">GetDeviceProperties method of the Win32\_PnPEntity class</span></span>

<span data-ttu-id="1119d-104">Obtém as propriedades especificadas deste Plug and Play dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1119d-104">Gets the specified properties of this Plug and Play device.</span></span>

## <a name="syntax"></a><span data-ttu-id="1119d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1119d-105">Syntax</span></span>


```mof
Uint32 GetDeviceProperties(
  [in, optional] string                  devicePropertyKeys[],
  [out]          Win32_PnPDeviceProperty deviceProperties[]
);
```



## <a name="parameters"></a><span data-ttu-id="1119d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1119d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1119d-107">*devicePropertyKeys* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="1119d-107">*devicePropertyKeys* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1119d-108">As propriedades a serem retornadas.</span><span class="sxs-lookup"><span data-stu-id="1119d-108">The properties to return.</span></span>

</dd> <dt>

<span data-ttu-id="1119d-109">*dispositivos* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="1119d-109">*deviceProperties* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1119d-110">As propriedades solicitadas nos subtipos apropriados da classe abstrata [**Win32 \_ PnPDeviceProperty**](win32-pnpdeviceproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="1119d-110">The requested properties in appropriate subtypes of the [**Win32\_PnPDeviceProperty**](win32-pnpdeviceproperty.md) abstract class.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1119d-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1119d-111">Requirements</span></span>



| <span data-ttu-id="1119d-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="1119d-112">Requirement</span></span> | <span data-ttu-id="1119d-113">Valor</span><span class="sxs-lookup"><span data-stu-id="1119d-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1119d-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1119d-114">Minimum supported client</span></span><br/> | <span data-ttu-id="1119d-115">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="1119d-115">Windows 10 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="1119d-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1119d-116">Minimum supported server</span></span><br/> | <span data-ttu-id="1119d-117">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="1119d-117">Windows Server 2016</span></span><br/>                                                          |
| <span data-ttu-id="1119d-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="1119d-118">Namespace</span></span><br/>                | <span data-ttu-id="1119d-119">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="1119d-119">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1119d-120">MOF</span><span class="sxs-lookup"><span data-stu-id="1119d-120">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1119d-121"><dt>Cimwin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1119d-121"><dt>Cimwin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1119d-122">DLL</span><span class="sxs-lookup"><span data-stu-id="1119d-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1119d-123"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1119d-123"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1119d-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="1119d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1119d-125">**\_PnPEntity Win32**</span><span class="sxs-lookup"><span data-stu-id="1119d-125">**Win32\_PnPEntity**</span></span>](win32-pnpentity.md)
</dt> </dl>

 

 




