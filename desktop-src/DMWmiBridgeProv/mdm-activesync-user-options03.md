---
title: Classe MDM_ActiveSync_User_Options03
description: A \_ classe Options03 de usuário do MDM ActiveSync \_ \_ define as opções que são definidas para cada conta do ActiveSync.
ms.assetid: b325f676-9b83-4212-a228-e2d774515be6
keywords:
- Classe MDM_ActiveSync_User_Options03
- Classe MDM_ActiveSync_User_Options03, descrita
topic_type:
- apiref
api_name:
- MDM_ActiveSync_User_Options03
- MDM_ActiveSync_User_Options03.InstanceID
- MDM_ActiveSync_User_Options03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c459e20b519801c622a091060fd6a87ced2807c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085452"
---
# <a name="mdm_activesync_user_options03-class"></a><span data-ttu-id="afcb2-105">\_ \_ Classe Options03 de usuário do MDM ActiveSync \_</span><span class="sxs-lookup"><span data-stu-id="afcb2-105">MDM\_ActiveSync\_User\_Options03 class</span></span>

<span data-ttu-id="afcb2-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="afcb2-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="afcb2-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="afcb2-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="afcb2-108">A **classe \_ \_ \_ Options03 de usuário do MDM ActiveSync** define as opções que são definidas para cada conta do ActiveSync.</span><span class="sxs-lookup"><span data-stu-id="afcb2-108">The **MDM\_ActiveSync\_User\_Options03** class defines the options that are set for each ActiveSync account.</span></span>

<span data-ttu-id="afcb2-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="afcb2-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="afcb2-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="afcb2-110">Syntax</span></span>

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_ActiveSync_User_Options03
{
  string InstanceID;
  string ParentID;
  string UseSSL;
  string Schedule;
  string MailAgeFilter;
  string Logging;
};
```

## <a name="members"></a><span data-ttu-id="afcb2-111">Membros</span><span class="sxs-lookup"><span data-stu-id="afcb2-111">Members</span></span>

<span data-ttu-id="afcb2-112">A **classe \_ \_ \_ Options03 do usuário do MDM ActiveSync** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="afcb2-112">The **MDM\_ActiveSync\_User\_Options03** class has these types of members:</span></span>

-   [<span data-ttu-id="afcb2-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="afcb2-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="afcb2-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="afcb2-114">Properties</span></span>

<span data-ttu-id="afcb2-115">A **classe \_ \_ \_ Options03 de usuário do MDM ActiveSync** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="afcb2-115">The **MDM\_ActiveSync\_User\_Options03** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="afcb2-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="afcb2-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="afcb2-117">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="afcb2-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="afcb2-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="afcb2-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="afcb2-119">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="afcb2-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="afcb2-120">Identifica o nome do nó pai.</span><span class="sxs-lookup"><span data-stu-id="afcb2-120">Identifies the name of the parent node.</span></span>

</dd> <dt>

[<span data-ttu-id="afcb2-121">Logging</span><span class="sxs-lookup"><span data-stu-id="afcb2-121">Logging</span></span>](/windows/client-management/mdm/activesync-csp#options-logging)
</dt> <dd> <dl> <dt>

<span data-ttu-id="afcb2-122">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="afcb2-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="afcb2-123">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="afcb2-123">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="afcb2-124">MailAgeFilter</span><span class="sxs-lookup"><span data-stu-id="afcb2-124">MailAgeFilter</span></span>](/windows/client-management/mdm/activesync-csp#options-mailagefilter)
</dt> <dd> <dl> <dt>

<span data-ttu-id="afcb2-125">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="afcb2-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="afcb2-126">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="afcb2-126">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="afcb2-127">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="afcb2-127">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="afcb2-128">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="afcb2-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="afcb2-129">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="afcb2-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="afcb2-130">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="afcb2-130">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="afcb2-131">Descreve o caminho completo para o nó pai.</span><span class="sxs-lookup"><span data-stu-id="afcb2-131">Describes the full path to the parent node.</span></span> <span data-ttu-id="afcb2-132">Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/ActiveSync/Accounts/*GUID*/"</span><span class="sxs-lookup"><span data-stu-id="afcb2-132">For this class, the string is "./Vendor/MSFT/ActiveSync/Accounts/*GUID*/"</span></span>

</dd> <dt>

[<span data-ttu-id="afcb2-133">Agenda</span><span class="sxs-lookup"><span data-stu-id="afcb2-133">Schedule</span></span>](/windows/client-management/mdm/activesync-csp#options-schedule)
</dt> <dd> <dl> <dt>

<span data-ttu-id="afcb2-134">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="afcb2-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="afcb2-135">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="afcb2-135">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="afcb2-136">UseSSL</span><span class="sxs-lookup"><span data-stu-id="afcb2-136">UseSSL</span></span>](/windows/client-management/mdm/activesync-csp#options-usessl)
</dt> <dd> <dl> <dt>

<span data-ttu-id="afcb2-137">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="afcb2-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="afcb2-138">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="afcb2-138">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="afcb2-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="afcb2-139">Requirements</span></span>



| <span data-ttu-id="afcb2-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="afcb2-140">Requirement</span></span> | <span data-ttu-id="afcb2-141">Valor</span><span class="sxs-lookup"><span data-stu-id="afcb2-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="afcb2-142">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="afcb2-142">Minimum supported client</span></span><br/> | <span data-ttu-id="afcb2-143">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="afcb2-143">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="afcb2-144">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="afcb2-144">Minimum supported server</span></span><br/> | <span data-ttu-id="afcb2-145">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="afcb2-145">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="afcb2-146">Namespace</span><span class="sxs-lookup"><span data-stu-id="afcb2-146">Namespace</span></span><br/>                | <span data-ttu-id="afcb2-147">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="afcb2-147">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="afcb2-148">MOF</span><span class="sxs-lookup"><span data-stu-id="afcb2-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="afcb2-149"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="afcb2-149"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="afcb2-150">DLL</span><span class="sxs-lookup"><span data-stu-id="afcb2-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="afcb2-151"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="afcb2-151"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="afcb2-152">Confira também</span><span class="sxs-lookup"><span data-stu-id="afcb2-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="afcb2-153">Como usar os scripts do PowerShell com o provedor de ponte WMI</span><span class="sxs-lookup"><span data-stu-id="afcb2-153">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

