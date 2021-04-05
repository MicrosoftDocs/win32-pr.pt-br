---
description: A \_ classe WMI de associação do Userdesktop do Win32 relaciona uma conta de usuário e configurações de área de trabalho que são específicas a ela.
ms.assetid: 5ea83ad6-bd0a-4c16-85b2-e3e61ef05903
ms.tgt_platform: multiple
title: Classe Win32_UserDesktop
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_UserDesktop
- Win32_UserDesktop.Element
- Win32_UserDesktop.Setting
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 39b45ee7859fea9f1068123041a87309cf40c2d2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826241"
---
# <a name="win32_userdesktop-class"></a><span data-ttu-id="9db6b-103">\_Classe Win32 Userdesktop</span><span class="sxs-lookup"><span data-stu-id="9db6b-103">Win32\_UserDesktop class</span></span>

<span data-ttu-id="9db6b-104">A [classe WMI](../wmisdk/retrieving-a-class.md) de associação do **\_ userdesktop do Win32** relaciona uma conta de usuário e configurações de área de trabalho que são específicas a ela.</span><span class="sxs-lookup"><span data-stu-id="9db6b-104">The **Win32\_UserDesktop** association [WMI class](../wmisdk/retrieving-a-class.md) relates a user account and desktop settings that are specific to it.</span></span>

<span data-ttu-id="9db6b-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="9db6b-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="9db6b-106">As propriedades e os métodos estão em ordem alfabética, não em ordem de MOF.</span><span class="sxs-lookup"><span data-stu-id="9db6b-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="9db6b-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9db6b-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4FF-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_UserDesktop : CIM_ElementSetting
{
  Win32_UserAccount REF Element;
  Win32_Desktop     REF Setting;
};
```

## <a name="members"></a><span data-ttu-id="9db6b-108">Membros</span><span class="sxs-lookup"><span data-stu-id="9db6b-108">Members</span></span>

<span data-ttu-id="9db6b-109">A classe **Win32 \_ userdesktop** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="9db6b-109">The **Win32\_UserDesktop** class has these types of members:</span></span>

-   [<span data-ttu-id="9db6b-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="9db6b-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9db6b-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="9db6b-111">Properties</span></span>

<span data-ttu-id="9db6b-112">A classe **Win32 \_ userdesktop** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="9db6b-112">The **Win32\_UserDesktop** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9db6b-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="9db6b-113">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9db6b-114">Tipo de dados **: \_ conta de userwin32**</span><span class="sxs-lookup"><span data-stu-id="9db6b-114">Data type: **Win32\_UserAccount**</span></span>
</dt> <dt>

<span data-ttu-id="9db6b-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9db6b-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9db6b-116">Qualificadores: [**chave**](../wmisdk/key-qualifier.md), [**substituição**](../wmisdk/standard-qualifiers.md) ("elemento"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("conta de userwmi \| Win32 \_ ")</span><span class="sxs-lookup"><span data-stu-id="9db6b-116">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_UserAccount")</span></span>
</dt> </dl>

<span data-ttu-id="9db6b-117">Referência à instância que representa a conta de usuário cuja área de trabalho pode ser personalizada pela propriedade **Settings** dessa classe.</span><span class="sxs-lookup"><span data-stu-id="9db6b-117">Reference to the instance representing the user account whose desktop can be customized by the **Settings** property of this class.</span></span>

</dd> <dt>

<span data-ttu-id="9db6b-118">**Configuração**</span><span class="sxs-lookup"><span data-stu-id="9db6b-118">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9db6b-119">Tipo de dados **: \_ Desktop Win32**</span><span class="sxs-lookup"><span data-stu-id="9db6b-119">Data type: **Win32\_Desktop**</span></span>
</dt> <dt>

<span data-ttu-id="9db6b-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9db6b-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9db6b-121">Qualificadores: [**chave**](../wmisdk/key-qualifier.md), [**substituição**](../wmisdk/standard-qualifiers.md) ("configuração"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("área de trabalho do WMI \| Win32 \_ ")</span><span class="sxs-lookup"><span data-stu-id="9db6b-121">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_Desktop")</span></span>
</dt> </dl>

<span data-ttu-id="9db6b-122">Referência à instância que representa as configurações da área de trabalho que servem para personalizar uma área de trabalho de conta de usuário específica.</span><span class="sxs-lookup"><span data-stu-id="9db6b-122">Reference to the instance representing the desktop settings that serve to customize a specific user account desktop.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9db6b-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="9db6b-123">Remarks</span></span>

<span data-ttu-id="9db6b-124">A classe **Win32 \_ userdesktop** é derivada do [**CIM \_ ElementSetting**](cim-elementsetting.md).</span><span class="sxs-lookup"><span data-stu-id="9db6b-124">The **Win32\_UserDesktop** class is derived from [**CIM\_ElementSetting**](cim-elementsetting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9db6b-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9db6b-125">Requirements</span></span>



| <span data-ttu-id="9db6b-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="9db6b-126">Requirement</span></span> | <span data-ttu-id="9db6b-127">Valor</span><span class="sxs-lookup"><span data-stu-id="9db6b-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9db6b-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9db6b-128">Minimum supported client</span></span><br/> | <span data-ttu-id="9db6b-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9db6b-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9db6b-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9db6b-130">Minimum supported server</span></span><br/> | <span data-ttu-id="9db6b-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9db6b-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9db6b-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="9db6b-132">Namespace</span></span><br/>                | <span data-ttu-id="9db6b-133">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="9db6b-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9db6b-134">MOF</span><span class="sxs-lookup"><span data-stu-id="9db6b-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9db6b-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9db6b-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9db6b-136">DLL</span><span class="sxs-lookup"><span data-stu-id="9db6b-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9db6b-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9db6b-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9db6b-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="9db6b-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9db6b-139">**\_ELEMENTSETTING CIM**</span><span class="sxs-lookup"><span data-stu-id="9db6b-139">**CIM\_ElementSetting**</span></span>](cim-elementsetting.md)
</dt> <dt>

[<span data-ttu-id="9db6b-140">Classes do sistema operacional</span><span class="sxs-lookup"><span data-stu-id="9db6b-140">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
