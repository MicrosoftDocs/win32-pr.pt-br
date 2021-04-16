---
description: A \_ classe WMI de associação do Win32 SessionProcess representa uma associação entre uma sessão de logon e os processos associados a essa sessão.
ms.assetid: 19d4ecf9-27b5-4a0b-9c76-7d10679aaf5e
ms.tgt_platform: multiple
title: Classe Win32_SessionProcess
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SessionProcess
- Win32_SessionProcess.Antecedent
- Win32_SessionProcess.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: f4090da88e8f5d31b0940b0c7d217a930a364b63
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105754385"
---
# <a name="win32_sessionprocess-class"></a><span data-ttu-id="d145d-103">\_Classe Win32 SessionProcess</span><span class="sxs-lookup"><span data-stu-id="d145d-103">Win32\_SessionProcess class</span></span>

<span data-ttu-id="d145d-104">A [classe WMI](../wmisdk/retrieving-a-class.md) de associação do **Win32 \_ SessionProcess** representa uma associação entre uma sessão de logon e os processos associados a essa sessão.</span><span class="sxs-lookup"><span data-stu-id="d145d-104">The **Win32\_SessionProcess** association [WMI class](../wmisdk/retrieving-a-class.md) represents an association between a logon session and the processes associated with that session.</span></span>

<span data-ttu-id="d145d-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="d145d-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="d145d-106">As propriedades e os métodos estão em ordem alfabética, não em ordem de MOF.</span><span class="sxs-lookup"><span data-stu-id="d145d-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d145d-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d145d-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("9CD8E1CE-0D27-4a41-AADE-F8D200230FF4"), AMENDMENT]
class Win32_SessionProcess : Win32_SessionResource
{
  Win32_LogonSession REF Antecedent;
  Win32_Process      REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="d145d-108">Membros</span><span class="sxs-lookup"><span data-stu-id="d145d-108">Members</span></span>

<span data-ttu-id="d145d-109">A classe **Win32 \_ SessionProcess** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="d145d-109">The **Win32\_SessionProcess** class has these types of members:</span></span>

-   [<span data-ttu-id="d145d-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d145d-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d145d-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d145d-111">Properties</span></span>

<span data-ttu-id="d145d-112">A classe **Win32 \_ SessionProcess** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="d145d-112">The **Win32\_SessionProcess** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d145d-113">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="d145d-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d145d-114">Tipo de dados: **Win32 \_ LogonSession**</span><span class="sxs-lookup"><span data-stu-id="d145d-114">Data type: **Win32\_LogonSession**</span></span>
</dt> <dt>

<span data-ttu-id="d145d-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d145d-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d145d-116">Qualificadores: [**override**](../wmisdk/standard-qualifiers.md) ("Antecedent"), [**Key**](../wmisdk/key-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="d145d-116">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Antecedent"), [**Key**](../wmisdk/key-qualifier.md)</span></span>
</dt> </dl>

<span data-ttu-id="d145d-117">Um [**\_ LogonSession Win32**](win32-logonsessionmappeddisk.md) que representa a sessão que está relacionada ao processo.</span><span class="sxs-lookup"><span data-stu-id="d145d-117">A [**Win32\_LogonSession**](win32-logonsessionmappeddisk.md) that represents the session which is related to the process.</span></span>

</dd> <dt>

<span data-ttu-id="d145d-118">**Depende**</span><span class="sxs-lookup"><span data-stu-id="d145d-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d145d-119">Tipo de dados **: \_ processo Win32**</span><span class="sxs-lookup"><span data-stu-id="d145d-119">Data type: **Win32\_Process**</span></span>
</dt> <dt>

<span data-ttu-id="d145d-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d145d-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d145d-121">Qualificadores: [**substituir**](../wmisdk/standard-qualifiers.md) ("dependente"), [**chave**](../wmisdk/key-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="d145d-121">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Dependent"), [**Key**](../wmisdk/key-qualifier.md)</span></span>
</dt> </dl>

<span data-ttu-id="d145d-122">Um [**\_ processo Win32**](win32-processor.md) que representa o processo associado à sessão.</span><span class="sxs-lookup"><span data-stu-id="d145d-122">A [**Win32\_Process**](win32-processor.md) that represents the process associated with the session.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d145d-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="d145d-123">Remarks</span></span>

<span data-ttu-id="d145d-124">**Win32 \_ SessionProcess** retorna todas as sessões para o administrador quando conectado com privilégios elevados ou quando executado remotamente.</span><span class="sxs-lookup"><span data-stu-id="d145d-124">**Win32\_SessionProcess** returns all session for the administrator when logged in elevated or when run remotely.</span></span> <span data-ttu-id="d145d-125">Essa é uma extensão para o comportamento da classe.</span><span class="sxs-lookup"><span data-stu-id="d145d-125">This is an extension to the behavior of the class.</span></span>

## <a name="requirements"></a><span data-ttu-id="d145d-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d145d-126">Requirements</span></span>



| <span data-ttu-id="d145d-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="d145d-127">Requirement</span></span> | <span data-ttu-id="d145d-128">Valor</span><span class="sxs-lookup"><span data-stu-id="d145d-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d145d-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d145d-129">Minimum supported client</span></span><br/> | <span data-ttu-id="d145d-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d145d-130">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d145d-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d145d-131">Minimum supported server</span></span><br/> | <span data-ttu-id="d145d-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d145d-132">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d145d-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="d145d-133">Namespace</span></span><br/>                | <span data-ttu-id="d145d-134">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="d145d-134">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d145d-135">MOF</span><span class="sxs-lookup"><span data-stu-id="d145d-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d145d-136"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d145d-136"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d145d-137">DLL</span><span class="sxs-lookup"><span data-stu-id="d145d-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d145d-138"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d145d-138"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d145d-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="d145d-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d145d-140">**\_SessionResource Win32**</span><span class="sxs-lookup"><span data-stu-id="d145d-140">**Win32\_SessionResource**</span></span>](win32-sessionresource.md)
</dt> <dt>

[<span data-ttu-id="d145d-141">Classes do sistema operacional</span><span class="sxs-lookup"><span data-stu-id="d145d-141">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
