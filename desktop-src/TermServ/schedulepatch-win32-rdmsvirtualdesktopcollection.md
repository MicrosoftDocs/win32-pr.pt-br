---
title: Método SchedulePatch da classe Win32_RDMSVirtualDesktopCollection
description: Agenda um trabalho de provisionamento de atualização de software que instala atualizações de software nas máquinas virtuais em uma coleção de áreas de trabalho virtuais.
ms.assetid: 780d5709-9e7d-41d9-a4d0-b5d021615655
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método SchedulePatch
- Método SchedulePatch Serviços de Área de Trabalho Remota, classe Win32_RDMSVirtualDesktopCollection
- Classe Win32_RDMSVirtualDesktopCollection Serviços de Área de Trabalho Remota, método SchedulePatch
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.SchedulePatch
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d9585e3d13ea1f02115506741c153d62c33fcc8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455048"
---
# <a name="schedulepatch-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a><span data-ttu-id="6a725-106">Método SchedulePatch da classe Win32 \_ RDMSVirtualDesktopCollection</span><span class="sxs-lookup"><span data-stu-id="6a725-106">SchedulePatch method of the Win32\_RDMSVirtualDesktopCollection class</span></span>

<span data-ttu-id="6a725-107">Agenda um trabalho de provisionamento de atualização de software que instala atualizações de software nas máquinas virtuais em uma coleção de áreas de trabalho virtuais.</span><span class="sxs-lookup"><span data-stu-id="6a725-107">Schedules a software update provisioning job that installs software updates on the virtual machines in a virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a725-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6a725-108">Syntax</span></span>


```mof
uint32 SchedulePatch(
  [in] DATETIME StartTime,
  [in] DATETIME ForceLogOffTime,
  [in] string   JobInputXml
);
```



## <a name="parameters"></a><span data-ttu-id="6a725-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6a725-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a725-110">*StartTime* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6a725-110">*StartTime* \[in\]</span></span>
</dt> <dd>

> [!Note]  
> <span data-ttu-id="6a725-111">O sistema não fará logoff dos usuários das máquinas virtuais até o tempo especificado no parâmetro *ForceLogOffTime* .</span><span class="sxs-lookup"><span data-stu-id="6a725-111">The system will not log off users of the virtual machines until the time specified in the *ForceLogOffTime* parameter.</span></span>

 

<span data-ttu-id="6a725-112">A data e a hora para instalar as atualizações.</span><span class="sxs-lookup"><span data-stu-id="6a725-112">The date and time to install the updates.</span></span>

</dd> <dt>

<span data-ttu-id="6a725-113">*ForceLogOffTime* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6a725-113">*ForceLogOffTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a725-114">A data e a hora em que o sistema fará logoff dos usuários das máquinas virtuais.</span><span class="sxs-lookup"><span data-stu-id="6a725-114">The date and time on which the system will log off users of the virtual machines.</span></span>

</dd> <dt>

<span data-ttu-id="6a725-115">*JobInputXml* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6a725-115">*JobInputXml* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a725-116">Uma cadeia de caracteres formatada em XML que contém as informações do trabalho de atualização de software.</span><span class="sxs-lookup"><span data-stu-id="6a725-116">An XML formatted string that contains the software update job information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a725-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6a725-117">Return value</span></span>

<span data-ttu-id="6a725-118">Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="6a725-118">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a725-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6a725-119">Requirements</span></span>



| <span data-ttu-id="6a725-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="6a725-120">Requirement</span></span> | <span data-ttu-id="6a725-121">Valor</span><span class="sxs-lookup"><span data-stu-id="6a725-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a725-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6a725-122">Minimum supported client</span></span><br/> | <span data-ttu-id="6a725-123">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="6a725-123">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="6a725-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6a725-124">Minimum supported server</span></span><br/> | <span data-ttu-id="6a725-125">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6a725-125">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="6a725-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="6a725-126">Namespace</span></span><br/>                | <span data-ttu-id="6a725-127">\\RDMs CIMv2 \\ raiz</span><span class="sxs-lookup"><span data-stu-id="6a725-127">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="6a725-128">MOF</span><span class="sxs-lookup"><span data-stu-id="6a725-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6a725-129"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6a725-129"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="6a725-130">DLL</span><span class="sxs-lookup"><span data-stu-id="6a725-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6a725-131"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6a725-131"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="6a725-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="6a725-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a725-133">**\_RDMSVirtualDesktopCollection Win32**</span><span class="sxs-lookup"><span data-stu-id="6a725-133">**Win32\_RDMSVirtualDesktopCollection**</span></span>](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





