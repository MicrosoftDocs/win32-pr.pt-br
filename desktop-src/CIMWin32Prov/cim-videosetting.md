---
description: A \_ classe CIM VideoSetting associa o \_ objeto de configuração CIM VideoControllerResolution ao controlador ao qual ele se aplica.
ms.assetid: 1f6742ad-ab92-4723-b691-0c3e6c0d82fa
ms.tgt_platform: multiple
title: Classe CIM_VideoSetting
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VideoSetting
- CIM_VideoSetting.Setting
- CIM_VideoSetting.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a37fe8dd03738ae93f391a754caca84564dc6f6c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105755844"
---
# <a name="cim_videosetting-class"></a><span data-ttu-id="4442f-103">\_Classe CIM VideoSetting</span><span class="sxs-lookup"><span data-stu-id="4442f-103">CIM\_VideoSetting class</span></span>

<span data-ttu-id="4442f-104">A classe **CIM \_ VideoSetting** associa o objeto de configuração [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md) ao controlador ao qual ele se aplica.</span><span class="sxs-lookup"><span data-stu-id="4442f-104">The **CIM\_VideoSetting** class associates the [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md) setting object with the controller to which it applies.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4442f-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="4442f-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="4442f-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="4442f-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="4442f-107">A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="4442f-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="4442f-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="4442f-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="4442f-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4442f-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{1008CCEB-7BFF-11D2-AAD2-006008C78BC7}"), AMENDMENT]
class CIM_VideoSetting : CIM_ElementSetting
{
  CIM_VideoControllerResolution REF Setting;
  CIM_VideoController           REF Element;
};
```

## <a name="members"></a><span data-ttu-id="4442f-110">Membros</span><span class="sxs-lookup"><span data-stu-id="4442f-110">Members</span></span>

<span data-ttu-id="4442f-111">A classe **CIM \_ VideoSetting** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="4442f-111">The **CIM\_VideoSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="4442f-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="4442f-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4442f-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="4442f-113">Properties</span></span>

<span data-ttu-id="4442f-114">A classe **CIM \_ VideoSetting** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="4442f-114">The **CIM\_VideoSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4442f-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="4442f-115">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4442f-116">Tipo de dados: **CIM \_ VideoController**</span><span class="sxs-lookup"><span data-stu-id="4442f-116">Data type: **CIM\_VideoController**</span></span>
</dt> <dt>

<span data-ttu-id="4442f-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4442f-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4442f-118">Qualificadores: [**substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("element")</span><span class="sxs-lookup"><span data-stu-id="4442f-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Element")</span></span>
</dt> </dl>

<span data-ttu-id="4442f-119">Um [**\_ VideoController CIM**](cim-videocontroller.md) que descreve o controlador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="4442f-119">A [**CIM\_VideoController**](cim-videocontroller.md) that describes the video controller.</span></span>

</dd> <dt>

<span data-ttu-id="4442f-120">**Configuração**</span><span class="sxs-lookup"><span data-stu-id="4442f-120">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4442f-121">Tipo de dados: **CIM \_ VideoControllerResolution**</span><span class="sxs-lookup"><span data-stu-id="4442f-121">Data type: **CIM\_VideoControllerResolution**</span></span>
</dt> <dt>

<span data-ttu-id="4442f-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4442f-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4442f-123">Qualificadores: [**substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("Setting")</span><span class="sxs-lookup"><span data-stu-id="4442f-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Setting")</span></span>
</dt> </dl>

<span data-ttu-id="4442f-124">Um [**\_ VideoControllerResolution CIM**](cim-videocontrollerresolution.md) que descreve as resoluções, as taxas de atualização, o modo de verificação e o número de cores que podem ser definidas para o controlador.</span><span class="sxs-lookup"><span data-stu-id="4442f-124">A [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md) that describes the resolutions, refresh rates, scan mode and number of colors that can be set for the Controller.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4442f-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="4442f-125">Remarks</span></span>

<span data-ttu-id="4442f-126">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="4442f-126">WMI does not implement this class.</span></span> <span data-ttu-id="4442f-127">Para classes WMI derivadas do **CIM \_ VideoSetting**, consulte [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="4442f-127">For WMI classes derived from **CIM\_VideoSetting**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="4442f-128">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="4442f-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="4442f-129">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="4442f-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="4442f-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4442f-130">Requirements</span></span>



| <span data-ttu-id="4442f-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="4442f-131">Requirement</span></span> | <span data-ttu-id="4442f-132">Valor</span><span class="sxs-lookup"><span data-stu-id="4442f-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4442f-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4442f-133">Minimum supported client</span></span><br/> | <span data-ttu-id="4442f-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4442f-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4442f-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4442f-135">Minimum supported server</span></span><br/> | <span data-ttu-id="4442f-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4442f-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4442f-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="4442f-137">Namespace</span></span><br/>                | <span data-ttu-id="4442f-138">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="4442f-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4442f-139">MOF</span><span class="sxs-lookup"><span data-stu-id="4442f-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4442f-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4442f-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4442f-141">DLL</span><span class="sxs-lookup"><span data-stu-id="4442f-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4442f-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4442f-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4442f-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="4442f-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4442f-144">**\_ELEMENTSETTING CIM**</span><span class="sxs-lookup"><span data-stu-id="4442f-144">**CIM\_ElementSetting**</span></span>](cim-elementsetting.md)
</dt> </dl>

 

