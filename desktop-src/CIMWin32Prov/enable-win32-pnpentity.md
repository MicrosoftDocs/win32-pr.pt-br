---
description: Habilita este dispositivo Plug and Play.
ms.assetid: 8f2096c4-03b4-4005-9b97-0086f2b41080
ms.tgt_platform: multiple
title: Método Enable da classe Win32_PnPEntity
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PnPEntity.Enable
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8f64c833a29f4df3b353a7e9782ffea39396cece
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105753810"
---
# <a name="enable-method-of-the-win32_pnpentity-class"></a><span data-ttu-id="dc919-103">Habilitar o método da \_ classe Win32 PnPEntity</span><span class="sxs-lookup"><span data-stu-id="dc919-103">Enable method of the Win32\_PnPEntity class</span></span>

<span data-ttu-id="dc919-104">Habilita este dispositivo Plug and Play.</span><span class="sxs-lookup"><span data-stu-id="dc919-104">Enables this Plug and Play device.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc919-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dc919-105">Syntax</span></span>


```mof
Uint32 Enable(
  [out] boolean rebootNeeded
);
```



## <a name="parameters"></a><span data-ttu-id="dc919-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dc919-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc919-107">*rebootNeeded* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="dc919-107">*rebootNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dc919-108">Se uma reinicialização é necessária.</span><span class="sxs-lookup"><span data-stu-id="dc919-108">Whether a reboot is needed.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dc919-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dc919-109">Requirements</span></span>



| <span data-ttu-id="dc919-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="dc919-110">Requirement</span></span> | <span data-ttu-id="dc919-111">Valor</span><span class="sxs-lookup"><span data-stu-id="dc919-111">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dc919-112">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dc919-112">Minimum supported client</span></span><br/> | <span data-ttu-id="dc919-113">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="dc919-113">Windows 10 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="dc919-114">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dc919-114">Minimum supported server</span></span><br/> | <span data-ttu-id="dc919-115">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="dc919-115">Windows Server 2016</span></span><br/>                                                          |
| <span data-ttu-id="dc919-116">Namespace</span><span class="sxs-lookup"><span data-stu-id="dc919-116">Namespace</span></span><br/>                | <span data-ttu-id="dc919-117">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="dc919-117">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="dc919-118">MOF</span><span class="sxs-lookup"><span data-stu-id="dc919-118">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dc919-119"><dt>Cimwin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dc919-119"><dt>Cimwin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="dc919-120">DLL</span><span class="sxs-lookup"><span data-stu-id="dc919-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dc919-121"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dc919-121"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc919-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="dc919-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc919-123">**\_PnPEntity Win32**</span><span class="sxs-lookup"><span data-stu-id="dc919-123">**Win32\_PnPEntity**</span></span>](win32-pnpentity.md)
</dt> </dl>

 

 




