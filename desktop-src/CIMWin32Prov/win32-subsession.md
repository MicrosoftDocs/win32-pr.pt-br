---
description: A \_ Associação de Subsessão do Win32 define as relações entre as sessões em que uma sessão faz parte ou utiliza outra sessão, por exemplo, em que uma sessão de terminal usa uma sessão de logon.
ms.assetid: 2269de22-b086-4f71-8b19-bc53e1c88dc7
ms.tgt_platform: multiple
title: Classe Win32_SubSession
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SubSession
- Win32_SubSession.Antecedent
- Win32_SubSession.Dependent
api_type:
- DllExport
api_location:
- cimwin32.dll
ms.openlocfilehash: 540cfb4c00b5df64e4ff11a1cc462eaed03be434
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501059"
---
# <a name="win32_subsession-class"></a><span data-ttu-id="2641b-103">\_Classe de Subsessão Win32</span><span class="sxs-lookup"><span data-stu-id="2641b-103">Win32\_SubSession class</span></span>

<span data-ttu-id="2641b-104">A \_ Associação de Subsessão do Win32 define as relações entre as sessões em que uma sessão faz parte ou utiliza outra sessão, por exemplo, em que uma sessão de terminal usa uma sessão de logon.</span><span class="sxs-lookup"><span data-stu-id="2641b-104">The Win32\_SubSession association defines relationships between sessions where one session is a part of or utilizes another session for example where a Terminal session uses a Logon Session.</span></span>

<span data-ttu-id="2641b-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="2641b-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2641b-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2641b-106">Syntax</span></span>

``` syntax
[Abstract, AMENDMENT]
class Win32_SubSession : CIM_Dependency
{
  Win32_Session REF Antecedent;
  Win32_Session REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="2641b-107">Membros</span><span class="sxs-lookup"><span data-stu-id="2641b-107">Members</span></span>

<span data-ttu-id="2641b-108">A classe de **\_ subsessão Win32** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="2641b-108">The **Win32\_SubSession** class has these types of members:</span></span>

-   [<span data-ttu-id="2641b-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="2641b-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2641b-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="2641b-110">Properties</span></span>

<span data-ttu-id="2641b-111">A classe de **\_ subsessão Win32** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="2641b-111">The **Win32\_SubSession** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2641b-112">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="2641b-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2641b-113">Tipo de dados **: \_ sessão Win32**</span><span class="sxs-lookup"><span data-stu-id="2641b-113">Data type: **Win32\_Session**</span></span>
</dt> <dt>

<span data-ttu-id="2641b-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2641b-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2641b-115">Qualificadores: [**override**](../wmisdk/standard-qualifiers.md) (Antecedent)</span><span class="sxs-lookup"><span data-stu-id="2641b-115">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) (Antecedent)</span></span>
</dt> </dl>

<span data-ttu-id="2641b-116">Uma [**\_ sessão Win32**](win32-session.md) que descreve a sessão que tem uma subsessão.</span><span class="sxs-lookup"><span data-stu-id="2641b-116">A [**Win32\_Session**](win32-session.md) that describes the session that has a subsession.</span></span>

</dd> <dt>

<span data-ttu-id="2641b-117">**Depende**</span><span class="sxs-lookup"><span data-stu-id="2641b-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2641b-118">Tipo de dados **: \_ sessão Win32**</span><span class="sxs-lookup"><span data-stu-id="2641b-118">Data type: **Win32\_Session**</span></span>
</dt> <dt>

<span data-ttu-id="2641b-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2641b-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2641b-120">Qualificadores: [**substituir**](../wmisdk/standard-qualifiers.md) (dependente)</span><span class="sxs-lookup"><span data-stu-id="2641b-120">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) (Dependent)</span></span>
</dt> </dl>

<span data-ttu-id="2641b-121">Uma [**\_ sessão Win32**](win32-session.md) que descreve a sessão que é a subsessão.</span><span class="sxs-lookup"><span data-stu-id="2641b-121">A [**Win32\_Session**](win32-session.md) that describes the session that is the subsession.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2641b-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2641b-122">Requirements</span></span>



| <span data-ttu-id="2641b-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="2641b-123">Requirement</span></span> | <span data-ttu-id="2641b-124">Valor</span><span class="sxs-lookup"><span data-stu-id="2641b-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2641b-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2641b-125">Minimum supported client</span></span><br/> | <span data-ttu-id="2641b-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2641b-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2641b-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2641b-127">Minimum supported server</span></span><br/> | <span data-ttu-id="2641b-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2641b-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2641b-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="2641b-129">Namespace</span></span><br/>                | <span data-ttu-id="2641b-130">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="2641b-130">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2641b-131">MOF</span><span class="sxs-lookup"><span data-stu-id="2641b-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2641b-132"><dt>CimWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2641b-132"><dt>CimWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2641b-133">DLL</span><span class="sxs-lookup"><span data-stu-id="2641b-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2641b-134"><dt>Cimwin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2641b-134"><dt>Cimwin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2641b-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="2641b-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2641b-136">**\_Dependência CIM**</span><span class="sxs-lookup"><span data-stu-id="2641b-136">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

 
