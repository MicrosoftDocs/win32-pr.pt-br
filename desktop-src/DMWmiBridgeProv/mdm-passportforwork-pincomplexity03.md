---
title: Classe MDM_PassportForWork_PINComplexity03
description: A \_ classe MDM PassportForWork \_ PINComplexity03 define a complexidade do PIN para as credenciais de logon do Windows Hello para empresas.
ms.assetid: 83dcf859-03da-4508-b809-bafd24dc8bd4
keywords:
- Classe MDM_PassportForWork_PINComplexity03
- Classe MDM_PassportForWork_PINComplexity03, descrita
topic_type:
- apiref
api_name:
- MDM_PassportForWork_PINComplexity03
- MDM_PassportForWork_PINComplexity03.InstanceID
- MDM_PassportForWork_PINComplexity03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a9d01cd152935a1daa0a9b0721ea27129e21934
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918256"
---
# <a name="mdm_passportforwork_pincomplexity03-class"></a><span data-ttu-id="da9ec-105">\_ \_ Classe PINCOMPLEXITY03 do MDM PassportForWork</span><span class="sxs-lookup"><span data-stu-id="da9ec-105">MDM\_PassportForWork\_PINComplexity03 class</span></span>

<span data-ttu-id="da9ec-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="da9ec-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="da9ec-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="da9ec-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="da9ec-108">A classe **MDM \_ PassportForWork \_ PINComplexity03** define a complexidade do PIN para as credenciais de logon do Windows Hello para empresas.</span><span class="sxs-lookup"><span data-stu-id="da9ec-108">The **MDM\_PassportForWork\_PINComplexity03** class defines the PIN complexity for the logon credentials for Windows Hello for Business.</span></span>

<span data-ttu-id="da9ec-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="da9ec-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="da9ec-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="da9ec-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_PassportForWork_PINComplexity03
{
  string InstanceID;
  string ParentID;
  sint32 MinimumPINLength;
  sint32 MaximumPINLength;
  sint32 UppercaseLetters;
  sint32 LowercaseLetters;
  sint32 SpecialCharacters;
  sint32 Digits;
  sint32 History;
  sint32 Expiration;
};
```

## <a name="members"></a><span data-ttu-id="da9ec-111">Membros</span><span class="sxs-lookup"><span data-stu-id="da9ec-111">Members</span></span>

<span data-ttu-id="da9ec-112">A **classe \_ \_ PINComplexity03 de MDM PassportForWork** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="da9ec-112">The **MDM\_PassportForWork\_PINComplexity03** class has these types of members:</span></span>

-   [<span data-ttu-id="da9ec-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="da9ec-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="da9ec-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="da9ec-114">Properties</span></span>

<span data-ttu-id="da9ec-115">A **classe \_ \_ PINComplexity03 do MDM PassportForWork** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="da9ec-115">The **MDM\_PassportForWork\_PINComplexity03** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="da9ec-116">Números</span><span class="sxs-lookup"><span data-stu-id="da9ec-116">Digits</span></span>](/windows/client-management/mdm/passportforwork-csp#tenantid-policies-pincomplexity-digits)
</dt> <dd> <dl> <dt>

<span data-ttu-id="da9ec-117">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="da9ec-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="da9ec-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="da9ec-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="da9ec-119">Validade</span><span class="sxs-lookup"><span data-stu-id="da9ec-119">Expiration</span></span>](/windows/client-management/mdm/passportforwork-csp#tenantid-policies-pincomplexity-expiration)
</dt> <dd> <dl> <dt>

<span data-ttu-id="da9ec-120">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="da9ec-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="da9ec-121">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="da9ec-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="da9ec-122">Histórico</span><span class="sxs-lookup"><span data-stu-id="da9ec-122">History</span></span>](/windows/client-management/mdm/passportforwork-csp#tenantid-policies-pincomplexity-history)
</dt> <dd> <dl> <dt>

<span data-ttu-id="da9ec-123">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="da9ec-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="da9ec-124">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="da9ec-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="da9ec-125">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="da9ec-125">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da9ec-126">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="da9ec-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="da9ec-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="da9ec-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="da9ec-128">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="da9ec-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="da9ec-129">Nó raiz para políticas de PIN.</span><span class="sxs-lookup"><span data-stu-id="da9ec-129">Root node for PIN policies.</span></span>

</dd> <dt>

[<span data-ttu-id="da9ec-130">LowercaseLetters</span><span class="sxs-lookup"><span data-stu-id="da9ec-130">LowercaseLetters</span></span>](/windows/client-management/mdm/passportforwork-csp#tenantid-policies-pincomplexity-lowercaseletters)
</dt> <dd> <dl> <dt>

<span data-ttu-id="da9ec-131">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="da9ec-131">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="da9ec-132">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="da9ec-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="da9ec-133">MaximumPINLength</span><span class="sxs-lookup"><span data-stu-id="da9ec-133">MaximumPINLength</span></span>](/windows/client-management/mdm/passportforwork-csp#tenantid-policies-pincomplexity-maximumpinlength)
</dt> <dd> <dl> <dt>

<span data-ttu-id="da9ec-134">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="da9ec-134">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="da9ec-135">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="da9ec-135">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="da9ec-136">MinimumPINLength</span><span class="sxs-lookup"><span data-stu-id="da9ec-136">MinimumPINLength</span></span>](/windows/client-management/mdm/passportforwork-csp#tenantid-policies-pincomplexity-minimumpinlength)
</dt> <dd> <dl> <dt>

<span data-ttu-id="da9ec-137">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="da9ec-137">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="da9ec-138">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="da9ec-138">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="da9ec-139">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="da9ec-139">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da9ec-140">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="da9ec-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="da9ec-141">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="da9ec-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="da9ec-142">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="da9ec-142">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="da9ec-143">Descreve o caminho completo para o nó pai.</span><span class="sxs-lookup"><span data-stu-id="da9ec-143">Describes the full path to the parent node.</span></span> <span data-ttu-id="da9ec-144">Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/PassPortForWork/*tenantid*/Policies"</span><span class="sxs-lookup"><span data-stu-id="da9ec-144">For this class, the string is "./Vendor/MSFT/PassPortForWork/*TenantID*/Policies"</span></span>

</dd> <dt>

[<span data-ttu-id="da9ec-145">SpecialCharacters</span><span class="sxs-lookup"><span data-stu-id="da9ec-145">SpecialCharacters</span></span>](/windows/client-management/mdm/passportforwork-csp#tenantid-policies-pincomplexity-specialcharacters)
</dt> <dd> <dl> <dt>

<span data-ttu-id="da9ec-146">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="da9ec-146">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="da9ec-147">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="da9ec-147">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="da9ec-148">UppercaseLetters</span><span class="sxs-lookup"><span data-stu-id="da9ec-148">UppercaseLetters</span></span>](/windows/client-management/mdm/passportforwork-csp#tenantid-policies-pincomplexity-uppercaseletters)
</dt> <dd> <dl> <dt>

<span data-ttu-id="da9ec-149">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="da9ec-149">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="da9ec-150">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="da9ec-150">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="da9ec-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="da9ec-151">Requirements</span></span>



| <span data-ttu-id="da9ec-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="da9ec-152">Requirement</span></span> | <span data-ttu-id="da9ec-153">Valor</span><span class="sxs-lookup"><span data-stu-id="da9ec-153">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da9ec-154">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="da9ec-154">Minimum supported client</span></span><br/> | <span data-ttu-id="da9ec-155">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="da9ec-155">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="da9ec-156">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="da9ec-156">Minimum supported server</span></span><br/> | <span data-ttu-id="da9ec-157">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="da9ec-157">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="da9ec-158">Namespace</span><span class="sxs-lookup"><span data-stu-id="da9ec-158">Namespace</span></span><br/>                | <span data-ttu-id="da9ec-159">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="da9ec-159">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="da9ec-160">MOF</span><span class="sxs-lookup"><span data-stu-id="da9ec-160">MOF</span></span><br/>                      | <dl> <span data-ttu-id="da9ec-161"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="da9ec-161"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="da9ec-162">DLL</span><span class="sxs-lookup"><span data-stu-id="da9ec-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="da9ec-163"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="da9ec-163"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da9ec-164">Confira também</span><span class="sxs-lookup"><span data-stu-id="da9ec-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da9ec-165">Como usar os scripts do PowerShell com o provedor de ponte WMI</span><span class="sxs-lookup"><span data-stu-id="da9ec-165">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

