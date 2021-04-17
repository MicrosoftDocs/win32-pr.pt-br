---
description: O \_ abstrato MethodParameterClass do Win32, a classe base WMI deriva qualquer classe definida como um contêiner de valores de parâmetro que serão passados para um método.
ms.assetid: 293fa378-432d-4e97-a8ab-8dc4917d5476
ms.tgt_platform: multiple
title: Classe Win32_MethodParameterClass
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_MethodParameterClass
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4e791941df681b2e46c4de6f0714b1290baecfde
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105754818"
---
# <a name="win32_methodparameterclass-class"></a><span data-ttu-id="12108-103">\_Classe Win32 MethodParameterClass</span><span class="sxs-lookup"><span data-stu-id="12108-103">Win32\_MethodParameterClass class</span></span>

<span data-ttu-id="12108-104">O **abstrato \_ MethodParameterClass do Win32** , a [classe base WMI](/windows/desktop/WmiSdk/retrieving-a-class) deriva qualquer classe definida como um contêiner de valores de parâmetro que serão passados para um método.</span><span class="sxs-lookup"><span data-stu-id="12108-104">The **Win32\_MethodParameterClass** abstract, base [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) derives any class defined as a container of parameter values that will be passed to a method.</span></span> <span data-ttu-id="12108-105">Sem Propriedades próprias, essa classe serve como um nó de classificação.</span><span class="sxs-lookup"><span data-stu-id="12108-105">Having no properties of its own, this class serves as a classification node.</span></span> <span data-ttu-id="12108-106">Um exemplo semelhante é o [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="12108-106">A similar example is [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span> <span data-ttu-id="12108-107">A derivação de **CIM \_ físicoelement** indica que a classe descreve uma entidade física em vez de lógica.</span><span class="sxs-lookup"><span data-stu-id="12108-107">Derivation from **CIM\_PhysicalElement** indicates that the class describes a physical rather than logical entity.</span></span> <span data-ttu-id="12108-108">No caso do **Win32 \_ MethodParameterClass**, as classes derivadas dele são criadas especificamente para passar parâmetros para um método.</span><span class="sxs-lookup"><span data-stu-id="12108-108">In the case of **Win32\_MethodParameterClass**, classes derived from it are created specifically to pass parameters to a method.</span></span>

## <a name="syntax"></a><span data-ttu-id="12108-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="12108-109">Syntax</span></span>

## <a name="members"></a><span data-ttu-id="12108-110">Membros</span><span class="sxs-lookup"><span data-stu-id="12108-110">Members</span></span>

<span data-ttu-id="12108-111">A classe **Win32 \_ MethodParameterClass** não define nenhum membro.</span><span class="sxs-lookup"><span data-stu-id="12108-111">The **Win32\_MethodParameterClass** class does not define any members.</span></span>

## <a name="requirements"></a><span data-ttu-id="12108-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="12108-112">Requirements</span></span>



| <span data-ttu-id="12108-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="12108-113">Requirement</span></span> | <span data-ttu-id="12108-114">Valor</span><span class="sxs-lookup"><span data-stu-id="12108-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="12108-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="12108-115">Minimum supported client</span></span><br/> | <span data-ttu-id="12108-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="12108-116">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="12108-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="12108-117">Minimum supported server</span></span><br/> | <span data-ttu-id="12108-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="12108-118">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="12108-119">Namespace</span><span class="sxs-lookup"><span data-stu-id="12108-119">Namespace</span></span><br/>                | <span data-ttu-id="12108-120">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="12108-120">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="12108-121">MOF</span><span class="sxs-lookup"><span data-stu-id="12108-121">MOF</span></span><br/>                      | <dl> <span data-ttu-id="12108-122"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="12108-122"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="12108-123">DLL</span><span class="sxs-lookup"><span data-stu-id="12108-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="12108-124"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="12108-124"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12108-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="12108-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12108-126">Classes de gerenciamento de serviço WMI</span><span class="sxs-lookup"><span data-stu-id="12108-126">WMI Service Management Classes</span></span>](/windows/desktop/CIMWin32Prov/wmi-service-management-classes)
</dt> </dl>

 

