---
title: Classe MDM_Policy_Result01_TextInput02
description: A \_ classe MDM Policy \_ Result01 \_ TextInput02 representa as políticas de entrada de texto disponíveis.
ms.assetid: d0ab2d69-6d43-410e-936a-cb87a521d5f3
keywords:
- Classe MDM_Policy_Result01_TextInput02
- Classe MDM_Policy_Result01_TextInput02, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_TextInput02
- MDM_Policy_Result01_TextInput02.InstanceID
- MDM_Policy_Result01_TextInput02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a0c02c2afe70f3e7122de0c3d888c42ac179317
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454995"
---
# <a name="mdm_policy_result01_textinput02-class"></a><span data-ttu-id="a7405-105">\_Classe MDM \_ Result01 \_ TextInput02</span><span class="sxs-lookup"><span data-stu-id="a7405-105">MDM\_Policy\_Result01\_TextInput02 class</span></span>

<span data-ttu-id="a7405-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="a7405-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="a7405-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="a7405-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="a7405-108">A classe **MDM \_ Policy \_ Result01 \_ TextInput02** representa as políticas de entrada de texto disponíveis.</span><span class="sxs-lookup"><span data-stu-id="a7405-108">The **MDM\_Policy\_Result01\_TextInput02** class represents the text input policies available.</span></span>

<span data-ttu-id="a7405-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="a7405-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7405-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a7405-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_TextInput02
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

## <a name="members"></a><span data-ttu-id="a7405-111">Membros</span><span class="sxs-lookup"><span data-stu-id="a7405-111">Members</span></span>

<span data-ttu-id="a7405-112">A **classe \_ \_ Result01 \_ TextInput02 da política MDM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="a7405-112">The **MDM\_Policy\_Result01\_TextInput02** class has these types of members:</span></span>

-   [<span data-ttu-id="a7405-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="a7405-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a7405-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="a7405-114">Properties</span></span>

<span data-ttu-id="a7405-115">A **classe \_ \_ Result01 \_ TextInput02 da política MDM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="a7405-115">The **MDM\_Policy\_Result01\_TextInput02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="a7405-116">AllowIMELogging</span><span class="sxs-lookup"><span data-stu-id="a7405-116">AllowIMELogging</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-allowimelogging)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7405-117">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="a7405-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a7405-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="a7405-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a7405-119">AllowIMENetworkAccess</span><span class="sxs-lookup"><span data-stu-id="a7405-119">AllowIMENetworkAccess</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-allowimenetworkaccess)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7405-120">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="a7405-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a7405-121">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="a7405-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a7405-122">AllowInputPanel</span><span class="sxs-lookup"><span data-stu-id="a7405-122">AllowInputPanel</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-allowinputpanel)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7405-123">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="a7405-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a7405-124">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="a7405-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a7405-125">AllowJapaneseIMESurrogatePairCharacters</span><span class="sxs-lookup"><span data-stu-id="a7405-125">AllowJapaneseIMESurrogatePairCharacters</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-allowjapaneseimesurrogatepaircharacters)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7405-126">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="a7405-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a7405-127">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="a7405-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a7405-128">AllowJapaneseIVSCharacters</span><span class="sxs-lookup"><span data-stu-id="a7405-128">AllowJapaneseIVSCharacters</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-allowjapaneseivscharacters)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7405-129">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="a7405-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a7405-130">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="a7405-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a7405-131">Configuração allowjapanesenonpublishingstandardglyph ativada</span><span class="sxs-lookup"><span data-stu-id="a7405-131">AllowJapaneseNonPublishingStandardGlyph</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-allowjapanesenonpublishingstandardglyph)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7405-132">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="a7405-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a7405-133">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="a7405-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a7405-134">AllowJapaneseUserDictionary</span><span class="sxs-lookup"><span data-stu-id="a7405-134">AllowJapaneseUserDictionary</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-allowjapaneseuserdictionary)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7405-135">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="a7405-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a7405-136">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="a7405-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a7405-137">AllowKeyboardTextSuggestions</span><span class="sxs-lookup"><span data-stu-id="a7405-137">AllowKeyboardTextSuggestions</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-allowkeyboardtextsuggestions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7405-138">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="a7405-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a7405-139">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="a7405-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a7405-140">AllowLanguageFeaturesUninstall</span><span class="sxs-lookup"><span data-stu-id="a7405-140">AllowLanguageFeaturesUninstall</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-allowlanguagefeaturesuninstall)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7405-141">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="a7405-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a7405-142">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="a7405-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a7405-143">Configuração excludejapaneseimeexceptjis0208 ativada</span><span class="sxs-lookup"><span data-stu-id="a7405-143">ExcludeJapaneseIMEExceptJIS0208</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-excludejapaneseimeexceptjis0208)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7405-144">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="a7405-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a7405-145">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="a7405-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a7405-146">Configuração excludejapaneseimeexceptjis0208andeudc ativada</span><span class="sxs-lookup"><span data-stu-id="a7405-146">ExcludeJapaneseIMEExceptJIS0208andEUDC</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-excludejapaneseimeexceptjis0208andeudc)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7405-147">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="a7405-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a7405-148">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="a7405-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a7405-149">ExcludeJapaneseIMEExceptShiftJIS</span><span class="sxs-lookup"><span data-stu-id="a7405-149">ExcludeJapaneseIMEExceptShiftJIS</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-excludejapaneseimeexceptshiftjis)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7405-150">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="a7405-150">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a7405-151">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="a7405-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a7405-152">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="a7405-152">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7405-153">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a7405-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a7405-154">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a7405-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7405-155">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a7405-155">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="a7405-156">Identifica o nome do nó pai.</span><span class="sxs-lookup"><span data-stu-id="a7405-156">Identifies the name of the parent node.</span></span> <span data-ttu-id="a7405-157">Para essa classe, a cadeia de caracteres é "TextInput"</span><span class="sxs-lookup"><span data-stu-id="a7405-157">For this class, the string is "TextInput"</span></span>

</dd> <dt>

<span data-ttu-id="a7405-158">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="a7405-158">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7405-159">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a7405-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a7405-160">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a7405-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7405-161">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a7405-161">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="a7405-162">Descreve o caminho completo para o nó pai.</span><span class="sxs-lookup"><span data-stu-id="a7405-162">Describes the full path to the parent node.</span></span> <span data-ttu-id="a7405-163">Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/Policy/Result"</span><span class="sxs-lookup"><span data-stu-id="a7405-163">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a7405-164">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a7405-164">Requirements</span></span>



| <span data-ttu-id="a7405-165">Requisito</span><span class="sxs-lookup"><span data-stu-id="a7405-165">Requirement</span></span> | <span data-ttu-id="a7405-166">Valor</span><span class="sxs-lookup"><span data-stu-id="a7405-166">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7405-167">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a7405-167">Minimum supported client</span></span><br/> | <span data-ttu-id="a7405-168">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="a7405-168">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a7405-169">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a7405-169">Minimum supported server</span></span><br/> | <span data-ttu-id="a7405-170">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="a7405-170">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="a7405-171">Namespace</span><span class="sxs-lookup"><span data-stu-id="a7405-171">Namespace</span></span><br/>                | <span data-ttu-id="a7405-172">\\DMMap de \\ MDM \\ CIMv2 raiz</span><span class="sxs-lookup"><span data-stu-id="a7405-172">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="a7405-173">MOF</span><span class="sxs-lookup"><span data-stu-id="a7405-173">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a7405-174"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a7405-174"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="a7405-175">DLL</span><span class="sxs-lookup"><span data-stu-id="a7405-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a7405-176"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a7405-176"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a7405-177">Confira também</span><span class="sxs-lookup"><span data-stu-id="a7405-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7405-178">Como usar os scripts do PowerShell com o provedor de ponte WMI</span><span class="sxs-lookup"><span data-stu-id="a7405-178">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

