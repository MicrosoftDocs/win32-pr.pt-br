---
title: Classe MDM_WindowsLicensing_Subscriptions01_01
description: A \_ classe MDM WindowsLicensing \_ Subscriptions01 \_ 01 foi projetada para cenários de gerenciamento de licenciamento relacionados à assinatura.
ms.assetid: dc3b7eae-89d3-4e66-a65f-f100e23ea9fd
keywords:
- Classe MDM_WindowsLicensing_Subscriptions01_01
- Classe MDM_WindowsLicensing_Subscriptions01_01, descrita
topic_type:
- apiref
api_name:
- MDM_WindowsLicensing_Subscriptions01_01
- MDM_WindowsLicensing_Subscriptions01_01.InstanceID
- MDM_WindowsLicensing_Subscriptions01_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 911c578bd0e3cbc56c61f2cf85438660e8f437b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085975"
---
# <a name="mdm_windowslicensing_subscriptions01_01-class"></a><span data-ttu-id="723e7-105">\_Classe MDM WindowsLicensing \_ Subscriptions01 \_ 01</span><span class="sxs-lookup"><span data-stu-id="723e7-105">MDM\_WindowsLicensing\_Subscriptions01\_01 class</span></span>

<span data-ttu-id="723e7-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="723e7-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="723e7-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="723e7-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="723e7-108">A classe **MDM \_ WindowsLicensing \_ Subscriptions01 \_ 01** foi projetada para cenários de gerenciamento de licenciamento relacionados à assinatura.</span><span class="sxs-lookup"><span data-stu-id="723e7-108">The **MDM\_WindowsLicensing\_Subscriptions01\_01** class is designed for subscription-related licensing management scenarios.</span></span>

<span data-ttu-id="723e7-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="723e7-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="723e7-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="723e7-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_WindowsLicensing_Subscriptions01_01
{
  string InstanceID;
  string ParentID;
  sint32 Status;
  string Name;
};
```

## <a name="members"></a><span data-ttu-id="723e7-111">Membros</span><span class="sxs-lookup"><span data-stu-id="723e7-111">Members</span></span>

<span data-ttu-id="723e7-112">A classe **MDM \_ WindowsLicensing \_ Subscriptions01 \_ 01** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="723e7-112">The **MDM\_WindowsLicensing\_Subscriptions01\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="723e7-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="723e7-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="723e7-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="723e7-114">Properties</span></span>

<span data-ttu-id="723e7-115">A classe **MDM \_ WindowsLicensing \_ Subscriptions01 \_ 01** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="723e7-115">The **MDM\_WindowsLicensing\_Subscriptions01\_01** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="723e7-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="723e7-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="723e7-117">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="723e7-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="723e7-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="723e7-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="723e7-119">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="723e7-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="723e7-120">Identifica o nome do nó pai.</span><span class="sxs-lookup"><span data-stu-id="723e7-120">Identifies the name of the parent node.</span></span>

</dd> <dt>

[<span data-ttu-id="723e7-121">Nome</span><span class="sxs-lookup"><span data-stu-id="723e7-121">Name</span></span>](/windows/client-management/mdm/windowslicensing-csp#subscriptions-subscriptionid-name)
</dt> <dd> <dl> <dt>

<span data-ttu-id="723e7-122">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="723e7-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="723e7-123">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="723e7-123">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="723e7-124">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="723e7-124">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="723e7-125">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="723e7-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="723e7-126">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="723e7-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="723e7-127">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="723e7-127">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="723e7-128">Descreve o caminho completo para o nó pai.</span><span class="sxs-lookup"><span data-stu-id="723e7-128">Describes the full path to the parent node.</span></span> <span data-ttu-id="723e7-129">Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/WindowsLicensing"</span><span class="sxs-lookup"><span data-stu-id="723e7-129">For this class, the string is "./Vendor/MSFT/WindowsLicensing"</span></span>

</dd> <dt>

[<span data-ttu-id="723e7-130">Status</span><span class="sxs-lookup"><span data-stu-id="723e7-130">Status</span></span>](/windows/client-management/mdm/windowslicensing-csp#subscriptions-subscriptionid-status)
</dt> <dd> <dl> <dt>

<span data-ttu-id="723e7-131">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="723e7-131">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="723e7-132">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="723e7-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="723e7-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="723e7-133">Requirements</span></span>



| <span data-ttu-id="723e7-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="723e7-134">Requirement</span></span> | <span data-ttu-id="723e7-135">Valor</span><span class="sxs-lookup"><span data-stu-id="723e7-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="723e7-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="723e7-136">Minimum supported client</span></span><br/> | <span data-ttu-id="723e7-137">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="723e7-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="723e7-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="723e7-138">Minimum supported server</span></span><br/> | <span data-ttu-id="723e7-139">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="723e7-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="723e7-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="723e7-140">Namespace</span></span><br/>                | <span data-ttu-id="723e7-141">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="723e7-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="723e7-142">MOF</span><span class="sxs-lookup"><span data-stu-id="723e7-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="723e7-143"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="723e7-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="723e7-144">DLL</span><span class="sxs-lookup"><span data-stu-id="723e7-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="723e7-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="723e7-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

