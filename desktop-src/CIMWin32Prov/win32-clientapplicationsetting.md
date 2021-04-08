---
description: A \_ classe WMI de associação ClientApplicationSetting do Win32 relaciona um arquivo executável e um aplicativo de Component Object Model (com) que contém as opções de configuração com do arquivo executável.
ms.assetid: c43d80ee-0f29-4452-b51f-f18543bc1d35
ms.tgt_platform: multiple
title: Classe Win32_ClientApplicationSetting
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ClientApplicationSetting
- Win32_ClientApplicationSetting.Application
- Win32_ClientApplicationSetting.Client
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: fda1f1305904fa919bb2080fe5de02f0e5850a8a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920500"
---
# <a name="win32_clientapplicationsetting-class"></a><span data-ttu-id="8afe7-103">\_Classe Win32 ClientApplicationSetting</span><span class="sxs-lookup"><span data-stu-id="8afe7-103">Win32\_ClientApplicationSetting class</span></span>

<span data-ttu-id="8afe7-104">A [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) de associação **\_ ClientApplicationSetting do Win32** relaciona um arquivo executável e um aplicativo de Component Object Model (com) que contém as opções de configuração com do arquivo executável.</span><span class="sxs-lookup"><span data-stu-id="8afe7-104">The **Win32\_ClientApplicationSetting** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates an executable file and a Component Object Model (COM) application that contains the COM configuration options for the executable file.</span></span>

<span data-ttu-id="8afe7-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="8afe7-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="8afe7-106">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="8afe7-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="8afe7-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8afe7-107">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("CIMWin32"), UUID("{0F73ED5E-8ED9-11d2-B340-00105A1F8569}"), AMENDMENT]
class Win32_ClientApplicationSetting
{
  Win32_DCOMApplication REF Application;
  CIM_DataFile          REF Client;
};
```

## <a name="members"></a><span data-ttu-id="8afe7-108">Membros</span><span class="sxs-lookup"><span data-stu-id="8afe7-108">Members</span></span>

<span data-ttu-id="8afe7-109">A classe **Win32 \_ ClientApplicationSetting** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="8afe7-109">The **Win32\_ClientApplicationSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="8afe7-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="8afe7-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8afe7-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="8afe7-111">Properties</span></span>

<span data-ttu-id="8afe7-112">A classe **Win32 \_ ClientApplicationSetting** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="8afe7-112">The **Win32\_ClientApplicationSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8afe7-113">**Aplicativo**</span><span class="sxs-lookup"><span data-stu-id="8afe7-113">**Application**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8afe7-114">Tipo de dados: **Win32 \_ DCOMApplication**</span><span class="sxs-lookup"><span data-stu-id="8afe7-114">Data type: **Win32\_DCOMApplication**</span></span>
</dt> <dt>

<span data-ttu-id="8afe7-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8afe7-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8afe7-116">Qualificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ DCOMApplication")</span><span class="sxs-lookup"><span data-stu-id="8afe7-116">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_DCOMApplication")</span></span>
</dt> </dl>

<span data-ttu-id="8afe7-117">Referência à instância que representa o aplicativo COM que contém as opções de configuração do arquivo executável.</span><span class="sxs-lookup"><span data-stu-id="8afe7-117">Reference to the instance that represents the COM application that contains configuration options of the executable file.</span></span>

</dd> <dt>

<span data-ttu-id="8afe7-118">**Cliente**</span><span class="sxs-lookup"><span data-stu-id="8afe7-118">**Client**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8afe7-119">Tipo de dados **: \_ DataFile do CIM**</span><span class="sxs-lookup"><span data-stu-id="8afe7-119">Data type: **CIM\_DataFile**</span></span>
</dt> <dt>

<span data-ttu-id="8afe7-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8afe7-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8afe7-121">Qualificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \| CIM \_ DataFile")</span><span class="sxs-lookup"><span data-stu-id="8afe7-121">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\|CIM\_DataFile")</span></span>
</dt> </dl>

<span data-ttu-id="8afe7-122">Referência à instância que representa o arquivo executável que usa as configurações de COM.</span><span class="sxs-lookup"><span data-stu-id="8afe7-122">Reference to the instance that represents the executable file that uses COM settings.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8afe7-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="8afe7-123">Remarks</span></span>

<span data-ttu-id="8afe7-124">**Win32 \_ ClientApplicationSetting** não dá suporte à enumeração.</span><span class="sxs-lookup"><span data-stu-id="8afe7-124">**Win32\_ClientApplicationSetting** does not support enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="8afe7-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8afe7-125">Requirements</span></span>



| <span data-ttu-id="8afe7-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="8afe7-126">Requirement</span></span> | <span data-ttu-id="8afe7-127">Valor</span><span class="sxs-lookup"><span data-stu-id="8afe7-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8afe7-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8afe7-128">Minimum supported client</span></span><br/> | <span data-ttu-id="8afe7-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8afe7-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8afe7-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8afe7-130">Minimum supported server</span></span><br/> | <span data-ttu-id="8afe7-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8afe7-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8afe7-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="8afe7-132">Namespace</span></span><br/>                | <span data-ttu-id="8afe7-133">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="8afe7-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8afe7-134">MOF</span><span class="sxs-lookup"><span data-stu-id="8afe7-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8afe7-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8afe7-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8afe7-136">DLL</span><span class="sxs-lookup"><span data-stu-id="8afe7-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8afe7-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8afe7-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8afe7-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="8afe7-138">See also</span></span>

<dl> <dt>

<span data-ttu-id="8afe7-139">[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8afe7-139">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

