---
title: Classe MDM_Policy_Config01_TextInput02
description: A \_ classe MDM Policy \_ Config01 \_ TextInput02 representa as políticas de entrada de texto disponíveis.
ms.assetid: e5a8d331-40ec-49f2-aedd-5941fe59092f
keywords:
- Classe MDM_Policy_Config01_TextInput02
- Classe MDM_Policy_Config01_TextInput02, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_TextInput02
- MDM_Policy_Config01_TextInput02.InstanceID
- MDM_Policy_Config01_TextInput02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f79d750973edf501ca292d042e04bf4dc27ef42
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455214"
---
# <a name="mdm_policy_config01_textinput02-class"></a><span data-ttu-id="792bc-105">\_Classe MDM \_ Config01 \_ TextInput02</span><span class="sxs-lookup"><span data-stu-id="792bc-105">MDM\_Policy\_Config01\_TextInput02 class</span></span>

<span data-ttu-id="792bc-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="792bc-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="792bc-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="792bc-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="792bc-108">A classe **MDM \_ Policy \_ Config01 \_ TextInput02** representa as políticas de entrada de texto disponíveis.</span><span class="sxs-lookup"><span data-stu-id="792bc-108">The **MDM\_Policy\_Config01\_TextInput02** class represents the text input policies available.</span></span>

<span data-ttu-id="792bc-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="792bc-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="792bc-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="792bc-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_TextInput02
{
  string InstanceID;
  string ParentID;
  sint32 AllowIMENetworkAccess;
  sint32 AllowIMELogging;
  sint32 AllowJapaneseNonPublishingStandardGlyph;
  sint32 AllowJapaneseIVSCharacters;
  sint32 AllowJapaneseUserDictionary;
  sint32 AllowKeyboardTextSuggestions;
  sint32 AllowJapaneseIMESurrogatePairCharacters;
  sint32 ExcludeJapaneseIMEExceptShiftJIS;
  sint32 ExcludeJapaneseIMEExceptJIS0208;
  sint32 ExcludeJapaneseIMEExceptJIS0208andEUDC;
  sint32 AllowLanguageFeaturesUninstall;
  sint32 AllowInputPanel;
};
```

## <a name="members"></a><span data-ttu-id="792bc-111">Membros</span><span class="sxs-lookup"><span data-stu-id="792bc-111">Members</span></span>

<span data-ttu-id="792bc-112">A **classe \_ \_ Config01 \_ TextInput02 da política MDM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="792bc-112">The **MDM\_Policy\_Config01\_TextInput02** class has these types of members:</span></span>

-   [<span data-ttu-id="792bc-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="792bc-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="792bc-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="792bc-114">Properties</span></span>

<span data-ttu-id="792bc-115">A **classe \_ \_ Config01 \_ TextInput02 da política MDM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="792bc-115">The **MDM\_Policy\_Config01\_TextInput02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="792bc-116">AllowIMELogging</span><span class="sxs-lookup"><span data-stu-id="792bc-116">AllowIMELogging</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-allowimelogging)
</dt> <dd> <dl> <dt>

<span data-ttu-id="792bc-117">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="792bc-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="792bc-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="792bc-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="792bc-119">AllowIMENetworkAccess</span><span class="sxs-lookup"><span data-stu-id="792bc-119">AllowIMENetworkAccess</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-allowimenetworkaccess)
</dt> <dd> <dl> <dt>

<span data-ttu-id="792bc-120">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="792bc-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="792bc-121">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="792bc-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="792bc-122">AllowInputPanel</span><span class="sxs-lookup"><span data-stu-id="792bc-122">AllowInputPanel</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-allowinputpanel)
</dt> <dd> <dl> <dt>

<span data-ttu-id="792bc-123">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="792bc-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="792bc-124">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="792bc-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="792bc-125">AllowJapaneseIMESurrogatePairCharacters</span><span class="sxs-lookup"><span data-stu-id="792bc-125">AllowJapaneseIMESurrogatePairCharacters</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-allowjapaneseimesurrogatepaircharacters)
</dt> <dd> <dl> <dt>

<span data-ttu-id="792bc-126">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="792bc-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="792bc-127">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="792bc-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="792bc-128">AllowJapaneseIVSCharacters</span><span class="sxs-lookup"><span data-stu-id="792bc-128">AllowJapaneseIVSCharacters</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-allowjapaneseivscharacters)
</dt> <dd> <dl> <dt>

<span data-ttu-id="792bc-129">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="792bc-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="792bc-130">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="792bc-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="792bc-131">Configuração allowjapanesenonpublishingstandardglyph ativada</span><span class="sxs-lookup"><span data-stu-id="792bc-131">AllowJapaneseNonPublishingStandardGlyph</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-allowjapanesenonpublishingstandardglyph)
</dt> <dd> <dl> <dt>

<span data-ttu-id="792bc-132">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="792bc-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="792bc-133">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="792bc-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="792bc-134">AllowJapaneseUserDictionary</span><span class="sxs-lookup"><span data-stu-id="792bc-134">AllowJapaneseUserDictionary</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-allowjapaneseuserdictionary)
</dt> <dd> <dl> <dt>

<span data-ttu-id="792bc-135">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="792bc-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="792bc-136">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="792bc-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="792bc-137">AllowKeyboardTextSuggestions</span><span class="sxs-lookup"><span data-stu-id="792bc-137">AllowKeyboardTextSuggestions</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-allowkeyboardtextsuggestions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="792bc-138">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="792bc-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="792bc-139">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="792bc-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="792bc-140">AllowLanguageFeaturesUninstall</span><span class="sxs-lookup"><span data-stu-id="792bc-140">AllowLanguageFeaturesUninstall</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-allowlanguagefeaturesuninstall)
</dt> <dd> <dl> <dt>

<span data-ttu-id="792bc-141">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="792bc-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="792bc-142">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="792bc-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="792bc-143">Configuração excludejapaneseimeexceptjis0208 ativada</span><span class="sxs-lookup"><span data-stu-id="792bc-143">ExcludeJapaneseIMEExceptJIS0208</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-excludejapaneseimeexceptjis0208)
</dt> <dd> <dl> <dt>

<span data-ttu-id="792bc-144">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="792bc-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="792bc-145">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="792bc-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="792bc-146">Configuração excludejapaneseimeexceptjis0208andeudc ativada</span><span class="sxs-lookup"><span data-stu-id="792bc-146">ExcludeJapaneseIMEExceptJIS0208andEUDC</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-excludejapaneseimeexceptjis0208andeudc)
</dt> <dd> <dl> <dt>

<span data-ttu-id="792bc-147">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="792bc-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="792bc-148">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="792bc-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="792bc-149">ExcludeJapaneseIMEExceptShiftJIS</span><span class="sxs-lookup"><span data-stu-id="792bc-149">ExcludeJapaneseIMEExceptShiftJIS</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-excludejapaneseimeexceptshiftjis)
</dt> <dd> <dl> <dt>

<span data-ttu-id="792bc-150">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="792bc-150">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="792bc-151">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="792bc-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="792bc-152">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="792bc-152">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="792bc-153">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="792bc-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="792bc-154">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="792bc-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="792bc-155">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="792bc-155">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="792bc-156">Identifica o nome do nó pai.</span><span class="sxs-lookup"><span data-stu-id="792bc-156">Identifies the name of the parent node.</span></span> <span data-ttu-id="792bc-157">Para essa classe, a cadeia de caracteres é "TextInput"</span><span class="sxs-lookup"><span data-stu-id="792bc-157">For this class, the string is "TextInput"</span></span>

</dd> <dt>

<span data-ttu-id="792bc-158">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="792bc-158">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="792bc-159">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="792bc-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="792bc-160">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="792bc-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="792bc-161">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="792bc-161">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="792bc-162">Descreve o caminho completo para o nó pai.</span><span class="sxs-lookup"><span data-stu-id="792bc-162">Describes the full path to the parent node.</span></span> <span data-ttu-id="792bc-163">Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/Policy/Config"</span><span class="sxs-lookup"><span data-stu-id="792bc-163">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="792bc-164">Requisitos</span><span class="sxs-lookup"><span data-stu-id="792bc-164">Requirements</span></span>



| <span data-ttu-id="792bc-165">Requisito</span><span class="sxs-lookup"><span data-stu-id="792bc-165">Requirement</span></span> | <span data-ttu-id="792bc-166">Valor</span><span class="sxs-lookup"><span data-stu-id="792bc-166">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="792bc-167">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="792bc-167">Minimum supported client</span></span><br/> | <span data-ttu-id="792bc-168">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="792bc-168">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="792bc-169">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="792bc-169">Minimum supported server</span></span><br/> | <span data-ttu-id="792bc-170">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="792bc-170">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="792bc-171">Namespace</span><span class="sxs-lookup"><span data-stu-id="792bc-171">Namespace</span></span><br/>                | <span data-ttu-id="792bc-172">\\DMMap de \\ MDM \\ CIMv2 raiz</span><span class="sxs-lookup"><span data-stu-id="792bc-172">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="792bc-173">MOF</span><span class="sxs-lookup"><span data-stu-id="792bc-173">MOF</span></span><br/>                      | <dl> <span data-ttu-id="792bc-174"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="792bc-174"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="792bc-175">DLL</span><span class="sxs-lookup"><span data-stu-id="792bc-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="792bc-176"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="792bc-176"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="792bc-177">Confira também</span><span class="sxs-lookup"><span data-stu-id="792bc-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="792bc-178">Como usar os scripts do PowerShell com o provedor de ponte WMI</span><span class="sxs-lookup"><span data-stu-id="792bc-178">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

