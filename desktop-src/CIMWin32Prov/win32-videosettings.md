---
description: A \_ classe WMI de associação do Win32 VideoSettings relaciona um controlador de vídeo e configurações de vídeo que podem ser aplicadas a ele.
ms.assetid: 0cc42352-0a89-434d-a8b6-230c677de49c
ms.tgt_platform: multiple
title: Classe Win32_VideoSettings
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_VideoSettings
- Win32_VideoSettings.Setting
- Win32_VideoSettings.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 38e949b6b6501dc51b39448d72e6bf61f37fbecb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105754383"
---
# <a name="win32_videosettings-class"></a><span data-ttu-id="82d14-103">\_Classe Win32 VideoSettings</span><span class="sxs-lookup"><span data-stu-id="82d14-103">Win32\_VideoSettings class</span></span>

<span data-ttu-id="82d14-104">A [classe WMI](../wmisdk/retrieving-a-class.md) de associação do **Win32 \_ VideoSettings** relaciona um controlador de vídeo e configurações de vídeo que podem ser aplicadas a ele.</span><span class="sxs-lookup"><span data-stu-id="82d14-104">The **Win32\_VideoSettings** association [WMI class](../wmisdk/retrieving-a-class.md) relates a video controller and video settings that can be applied to it.</span></span>

<span data-ttu-id="82d14-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="82d14-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="82d14-106">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="82d14-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="82d14-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="82d14-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{1008CCEE-7BFF-11D2-AAD2-006008C78BC7}"), AMENDMENT]
class Win32_VideoSettings : CIM_VideoSetting
{
  CIM_VideoControllerResolution REF Setting;
  Win32_VideoController         REF Element;
};
```

## <a name="members"></a><span data-ttu-id="82d14-108">Membros</span><span class="sxs-lookup"><span data-stu-id="82d14-108">Members</span></span>

<span data-ttu-id="82d14-109">A classe **Win32 \_ VideoSettings** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="82d14-109">The **Win32\_VideoSettings** class has these types of members:</span></span>

-   [<span data-ttu-id="82d14-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="82d14-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="82d14-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="82d14-111">Properties</span></span>

<span data-ttu-id="82d14-112">A classe **Win32 \_ VideoSettings** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="82d14-112">The **Win32\_VideoSettings** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="82d14-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="82d14-113">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82d14-114">Tipo de dados: **Win32 \_ VideoController**</span><span class="sxs-lookup"><span data-stu-id="82d14-114">Data type: **Win32\_VideoController**</span></span>
</dt> <dt>

<span data-ttu-id="82d14-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="82d14-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="82d14-116">Qualificadores: [**chave**](../wmisdk/key-qualifier.md), [**substituição**](../wmisdk/standard-qualifiers.md) ("elemento"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ VideoController")</span><span class="sxs-lookup"><span data-stu-id="82d14-116">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_VideoController")</span></span>
</dt> </dl>

<span data-ttu-id="82d14-117">Um [**\_ VideoController Win32**](win32-videocontroller.md) que contém as propriedades do controlador de vídeo em que uma configuração de vídeo pode ser usada.</span><span class="sxs-lookup"><span data-stu-id="82d14-117">A [**Win32\_VideoController**](win32-videocontroller.md) containing the properties of the video controller that a video setting can be used on.</span></span>

</dd> <dt>

<span data-ttu-id="82d14-118">**Configuração**</span><span class="sxs-lookup"><span data-stu-id="82d14-118">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82d14-119">Tipo de dados: **CIM \_ VideoControllerResolution**</span><span class="sxs-lookup"><span data-stu-id="82d14-119">Data type: **CIM\_VideoControllerResolution**</span></span>
</dt> <dt>

<span data-ttu-id="82d14-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="82d14-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="82d14-121">Qualificadores: [**chave**](../wmisdk/key-qualifier.md), [**substituição**](../wmisdk/standard-qualifiers.md) ("configuração"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM \| CIM \_ VideoControllerResolution")</span><span class="sxs-lookup"><span data-stu-id="82d14-121">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM\|CIM\_VideoControllerResolution")</span></span>
</dt> </dl>

<span data-ttu-id="82d14-122">Um [**\_ VideoControllerResolution CIM**](cim-videocontrollerresolution.md) que contém configurações que podem ser aplicadas ao controlador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="82d14-122">A [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md) containing settings that can be applied to the video controller.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="82d14-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="82d14-123">Remarks</span></span>

<span data-ttu-id="82d14-124">A classe **Win32 \_ VideoSettings** é derivada de [**CIM \_ VideoSetting**](cim-videosetting.md).</span><span class="sxs-lookup"><span data-stu-id="82d14-124">The **Win32\_VideoSettings** class is derived from [**CIM\_VideoSetting**](cim-videosetting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="82d14-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="82d14-125">Requirements</span></span>



| <span data-ttu-id="82d14-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="82d14-126">Requirement</span></span> | <span data-ttu-id="82d14-127">Valor</span><span class="sxs-lookup"><span data-stu-id="82d14-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="82d14-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="82d14-128">Minimum supported client</span></span><br/> | <span data-ttu-id="82d14-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="82d14-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="82d14-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="82d14-130">Minimum supported server</span></span><br/> | <span data-ttu-id="82d14-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="82d14-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="82d14-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="82d14-132">Namespace</span></span><br/>                | <span data-ttu-id="82d14-133">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="82d14-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="82d14-134">MOF</span><span class="sxs-lookup"><span data-stu-id="82d14-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="82d14-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="82d14-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="82d14-136">DLL</span><span class="sxs-lookup"><span data-stu-id="82d14-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="82d14-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="82d14-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82d14-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="82d14-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82d14-139">**\_VIDEOSETTING CIM**</span><span class="sxs-lookup"><span data-stu-id="82d14-139">**CIM\_VideoSetting**</span></span>](cim-videosetting.md)
</dt> <dt>

[<span data-ttu-id="82d14-140">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="82d14-140">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
