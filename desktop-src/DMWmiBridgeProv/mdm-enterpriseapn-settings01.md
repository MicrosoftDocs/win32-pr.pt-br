---
title: Classe MDM_EnterpriseAPN_Settings01
description: A \_ classe MDM EnterpriseAPN \_ Settings01 é usada pela empresa para alterar as configurações globais do APN.
ms.assetid: 3f2d3d38-c389-4945-b519-5f2d7dedb86c
keywords:
- Classe MDM_EnterpriseAPN_Settings01
- Classe MDM_EnterpriseAPN_Settings01, descrita
topic_type:
- apiref
api_name:
- MDM_EnterpriseAPN_Settings01
- MDM_EnterpriseAPN_Settings01.InstanceID
- MDM_EnterpriseAPN_Settings01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74704451790690df8f9cc11fec8bc1ed80d3c2dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085993"
---
# <a name="mdm_enterpriseapn_settings01-class"></a><span data-ttu-id="0b03c-105">\_ \_ Classe SETTINGS01 do MDM EnterpriseAPN</span><span class="sxs-lookup"><span data-stu-id="0b03c-105">MDM\_EnterpriseAPN\_Settings01 class</span></span>

<span data-ttu-id="0b03c-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="0b03c-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="0b03c-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="0b03c-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="0b03c-108">A classe **MDM \_ EnterpriseAPN \_ Settings01** é usada pela empresa para alterar as configurações globais do APN.</span><span class="sxs-lookup"><span data-stu-id="0b03c-108">The **MDM\_EnterpriseAPN\_Settings01** class is used by the enterprise to change APN global settings.</span></span>

<span data-ttu-id="0b03c-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="0b03c-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b03c-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0b03c-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_EnterpriseAPN_Settings01
{
  string  InstanceID;
  string  ParentID;
  boolean AllowUserControl;
  boolean HideView;
};
```

## <a name="members"></a><span data-ttu-id="0b03c-111">Membros</span><span class="sxs-lookup"><span data-stu-id="0b03c-111">Members</span></span>

<span data-ttu-id="0b03c-112">A **classe \_ \_ Settings01 de MDM EnterpriseAPN** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="0b03c-112">The **MDM\_EnterpriseAPN\_Settings01** class has these types of members:</span></span>

-   [<span data-ttu-id="0b03c-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="0b03c-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0b03c-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="0b03c-114">Properties</span></span>

<span data-ttu-id="0b03c-115">A **classe \_ \_ Settings01 do MDM EnterpriseAPN** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="0b03c-115">The **MDM\_EnterpriseAPN\_Settings01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="0b03c-116">AllowUserControl</span><span class="sxs-lookup"><span data-stu-id="0b03c-116">AllowUserControl</span></span>](/windows/client-management/mdm/enterpriseapn-csp#enterpriseapn-settings-allowusercontrol)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b03c-117">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="0b03c-117">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0b03c-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0b03c-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b03c-119">HideView</span><span class="sxs-lookup"><span data-stu-id="0b03c-119">HideView</span></span>](/windows/client-management/mdm/enterpriseapn-csp#enterpriseapn-settings-hideview)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b03c-120">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="0b03c-120">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0b03c-121">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0b03c-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0b03c-122">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="0b03c-122">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b03c-123">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0b03c-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b03c-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0b03c-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b03c-125">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="0b03c-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="0b03c-126">Nó que contém configurações globais do APN.</span><span class="sxs-lookup"><span data-stu-id="0b03c-126">Node that contains APN global settings.</span></span>

</dd> <dt>

<span data-ttu-id="0b03c-127">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="0b03c-127">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b03c-128">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0b03c-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b03c-129">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0b03c-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b03c-130">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="0b03c-130">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="0b03c-131">Descreve o caminho completo para o nó pai.</span><span class="sxs-lookup"><span data-stu-id="0b03c-131">Describes the full path to the parent node.</span></span> <span data-ttu-id="0b03c-132">Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/EnterpriseAPN/Settings"</span><span class="sxs-lookup"><span data-stu-id="0b03c-132">For this class, the string is "./Vendor/MSFT/EnterpriseAPN/Settings"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0b03c-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0b03c-133">Requirements</span></span>



| <span data-ttu-id="0b03c-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b03c-134">Requirement</span></span> | <span data-ttu-id="0b03c-135">Valor</span><span class="sxs-lookup"><span data-stu-id="0b03c-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b03c-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0b03c-136">Minimum supported client</span></span><br/> | <span data-ttu-id="0b03c-137">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="0b03c-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0b03c-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0b03c-138">Minimum supported server</span></span><br/> | <span data-ttu-id="0b03c-139">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="0b03c-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="0b03c-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="0b03c-140">Namespace</span></span><br/>                | <span data-ttu-id="0b03c-141">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="0b03c-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="0b03c-142">MOF</span><span class="sxs-lookup"><span data-stu-id="0b03c-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0b03c-143"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0b03c-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="0b03c-144">DLL</span><span class="sxs-lookup"><span data-stu-id="0b03c-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0b03c-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0b03c-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

