---
title: Classe MDM_Policy_Config01_ErrorReporting02
description: A \_ classe Config01 ErrorReporting02 de política de MDM \_ \_ configura as políticas de relatório de erros.
ms.assetid: 41067b5e-0db5-43b3-b1d5-2d6c54c35388
keywords:
- Classe MDM_Policy_Config01_ErrorReporting02
- Classe MDM_Policy_Config01_ErrorReporting02, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_ErrorReporting02
- MDM_Policy_Config01_ErrorReporting02.InstanceID
- MDM_Policy_Config01_ErrorReporting02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1c23cf5b0b01f05fa3712d6b1de11461c6f47da
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009171"
---
# <a name="mdm_policy_config01_errorreporting02-class"></a><span data-ttu-id="1d1e6-105">\_Classe MDM \_ Config01 \_ ErrorReporting02</span><span class="sxs-lookup"><span data-stu-id="1d1e6-105">MDM\_Policy\_Config01\_ErrorReporting02 class</span></span>

<span data-ttu-id="1d1e6-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="1d1e6-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="1d1e6-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="1d1e6-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="1d1e6-108">A \_ classe Config01 ErrorReporting02 de política de MDM \_ \_ configura as políticas de relatório de erros.</span><span class="sxs-lookup"><span data-stu-id="1d1e6-108">The MDM\_Policy\_Config01\_ErrorReporting02 class configures the error reporting policies.</span></span>

<span data-ttu-id="1d1e6-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="1d1e6-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d1e6-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1d1e6-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_ErrorReporting02
{
  string InstanceID;
  string ParentID;
  string CustomizeConsentSettings;
  string DisableWindowsErrorReporting;
  string DisplayErrorNotification;
  string DoNotSendAdditionalData;
  string PreventCriticalErrorDisplay;
};
```

## <a name="members"></a><span data-ttu-id="1d1e6-111">Membros</span><span class="sxs-lookup"><span data-stu-id="1d1e6-111">Members</span></span>

<span data-ttu-id="1d1e6-112">A **classe \_ \_ Config01 \_ ErrorReporting02 da política MDM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="1d1e6-112">The **MDM\_Policy\_Config01\_ErrorReporting02** class has these types of members:</span></span>

-   [<span data-ttu-id="1d1e6-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="1d1e6-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1d1e6-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="1d1e6-114">Properties</span></span>

<span data-ttu-id="1d1e6-115">A **classe \_ \_ Config01 \_ ErrorReporting02 da política MDM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="1d1e6-115">The **MDM\_Policy\_Config01\_ErrorReporting02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="1d1e6-116">CustomizeConsentSettings</span><span class="sxs-lookup"><span data-stu-id="1d1e6-116">CustomizeConsentSettings</span></span>](/windows/client-management/mdm/policy-csp-errorreporting#errorreporting-customizeconsentsettings)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d1e6-117">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1d1e6-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d1e6-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1d1e6-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1d1e6-119">DisableWindowsErrorReporting</span><span class="sxs-lookup"><span data-stu-id="1d1e6-119">DisableWindowsErrorReporting</span></span>](/windows/client-management/mdm/policy-csp-errorreporting#errorreporting-disablewindowserrorreporting)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d1e6-120">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1d1e6-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d1e6-121">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1d1e6-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1d1e6-122">DisplayErrorNotification</span><span class="sxs-lookup"><span data-stu-id="1d1e6-122">DisplayErrorNotification</span></span>](/windows/client-management/mdm/policy-csp-errorreporting#errorreporting-displayerrornotification)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d1e6-123">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1d1e6-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d1e6-124">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1d1e6-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1d1e6-125">DoNotSendAdditionalData</span><span class="sxs-lookup"><span data-stu-id="1d1e6-125">DoNotSendAdditionalData</span></span>](/windows/client-management/mdm/policy-csp-errorreporting#errorreporting-donotsendadditionaldata)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d1e6-126">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1d1e6-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d1e6-127">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1d1e6-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1d1e6-128">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="1d1e6-128">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d1e6-129">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1d1e6-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d1e6-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1d1e6-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d1e6-131">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1d1e6-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1d1e6-132">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="1d1e6-132">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d1e6-133">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1d1e6-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d1e6-134">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1d1e6-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d1e6-135">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1d1e6-135">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1d1e6-136">PreventCriticalErrorDisplay</span><span class="sxs-lookup"><span data-stu-id="1d1e6-136">PreventCriticalErrorDisplay</span></span>](/windows/client-management/mdm/policy-csp-errorreporting#errorreporting-preventcriticalerrordisplay)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d1e6-137">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1d1e6-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d1e6-138">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1d1e6-138">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1d1e6-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1d1e6-139">Requirements</span></span>



| <span data-ttu-id="1d1e6-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="1d1e6-140">Requirement</span></span> | <span data-ttu-id="1d1e6-141">Valor</span><span class="sxs-lookup"><span data-stu-id="1d1e6-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d1e6-142">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1d1e6-142">Minimum supported client</span></span><br/> | <span data-ttu-id="1d1e6-143">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="1d1e6-143">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1d1e6-144">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1d1e6-144">Minimum supported server</span></span><br/> | <span data-ttu-id="1d1e6-145">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="1d1e6-145">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="1d1e6-146">Namespace</span><span class="sxs-lookup"><span data-stu-id="1d1e6-146">Namespace</span></span><br/>                | <span data-ttu-id="1d1e6-147">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="1d1e6-147">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="1d1e6-148">MOF</span><span class="sxs-lookup"><span data-stu-id="1d1e6-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1d1e6-149"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1d1e6-149"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="1d1e6-150">DLL</span><span class="sxs-lookup"><span data-stu-id="1d1e6-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1d1e6-151"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1d1e6-151"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

