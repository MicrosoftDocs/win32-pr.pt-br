---
title: Classe MDM_DevDetail_Microsoft02
description: A \_ classe MDM DevDetail \_ Microsoft02 lida com o objeto de gerenciamento que fornece parâmetros específicos do dispositivo para o servidor OMA DM.
ms.assetid: 22a8ba26-d215-4bc5-a51b-6933d5473da3
keywords:
- Classe MDM_DevDetail_Microsoft02
- Classe MDM_DevDetail_Microsoft02, descrita
topic_type:
- apiref
api_name:
- MDM_DevDetail_Microsoft02
- MDM_DevDetail_Microsoft02.InstanceID
- MDM_DevDetail_Microsoft02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b384f9a24e30ca739ff9290efc83730b6d467e4a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918851"
---
# <a name="mdm_devdetail_microsoft02-class"></a><span data-ttu-id="81392-105">\_ \_ Classe MICROSOFT02 do MDM DevDetail</span><span class="sxs-lookup"><span data-stu-id="81392-105">MDM\_DevDetail\_Microsoft02 class</span></span>

<span data-ttu-id="81392-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="81392-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="81392-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="81392-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="81392-108">A classe **MDM \_ DevDetail \_ Microsoft02** lida com o objeto de gerenciamento que fornece parâmetros específicos do dispositivo para o servidor OMA DM.</span><span class="sxs-lookup"><span data-stu-id="81392-108">The **MDM\_DevDetail\_Microsoft02** class handles the management object which provides device-specific parameters to the OMA DM server.</span></span> <span data-ttu-id="81392-109">Esses parâmetros de dispositivo não são enviados do cliente para o servidor automaticamente, mas podem ser consultados por servidores usando comandos OMA DM.</span><span class="sxs-lookup"><span data-stu-id="81392-109">These device parameters are not sent from the client to the server automatically, but can be queried by servers using OMA DM commands.</span></span>

<span data-ttu-id="81392-110">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="81392-110">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="81392-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="81392-111">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_DevDetail_Microsoft02
{
  string InstanceID;
  string ParentID;
  string MobileID;
  string RadioSwV;
  string Resolution;
  string CommercializationOperator;
  sint32 ProcessorArchitecture;
  sint32 ProcessorType;
  string OSPlatform;
  string LocalTime;
  string DeviceName;
};
```

## <a name="members"></a><span data-ttu-id="81392-112">Membros</span><span class="sxs-lookup"><span data-stu-id="81392-112">Members</span></span>

<span data-ttu-id="81392-113">A **classe \_ \_ Microsoft02 de MDM DevDetail** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="81392-113">The **MDM\_DevDetail\_Microsoft02** class has these types of members:</span></span>

-   [<span data-ttu-id="81392-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="81392-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="81392-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="81392-115">Properties</span></span>

<span data-ttu-id="81392-116">A **classe \_ \_ Microsoft02 do MDM DevDetail** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="81392-116">The **MDM\_DevDetail\_Microsoft02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="81392-117">CommercializationOperator</span><span class="sxs-lookup"><span data-stu-id="81392-117">CommercializationOperator</span></span>](/windows/client-management/mdm/devdetail-csp#ext-microsoft-commercializationoperator)
</dt> <dd> <dl> <dt>

<span data-ttu-id="81392-118">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="81392-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81392-119">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="81392-119">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="81392-120">DeviceName</span><span class="sxs-lookup"><span data-stu-id="81392-120">DeviceName</span></span>](/windows/client-management/mdm/devdetail-csp#ext-microsoft-devicename)
</dt> <dd> <dl> <dt>

<span data-ttu-id="81392-121">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="81392-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81392-122">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="81392-122">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="81392-123">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="81392-123">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81392-124">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="81392-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81392-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="81392-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81392-126">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="81392-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="81392-127">Identifica o nome do nó pai.</span><span class="sxs-lookup"><span data-stu-id="81392-127">Identifies the name of the parent node.</span></span> <span data-ttu-id="81392-128">Para essa classe, a cadeia de caracteres é "Microsoft"</span><span class="sxs-lookup"><span data-stu-id="81392-128">For this class, the string is "Microsoft"</span></span>

</dd> <dt>

[<span data-ttu-id="81392-129">LocalTime</span><span class="sxs-lookup"><span data-stu-id="81392-129">LocalTime</span></span>](/windows/client-management/mdm/devdetail-csp#ext-microsoft-localtime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="81392-130">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="81392-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81392-131">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="81392-131">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="81392-132">Celular</span><span class="sxs-lookup"><span data-stu-id="81392-132">MobileID</span></span>](/windows/client-management/mdm/devdetail-csp#ext-microsoft-mobileid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="81392-133">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="81392-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81392-134">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="81392-134">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="81392-135">OSPlatform</span><span class="sxs-lookup"><span data-stu-id="81392-135">OSPlatform</span></span>](/windows/client-management/mdm/devdetail-csp#ext-microsoft-osplatform)
</dt> <dd> <dl> <dt>

<span data-ttu-id="81392-136">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="81392-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81392-137">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="81392-137">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="81392-138">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="81392-138">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81392-139">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="81392-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81392-140">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="81392-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81392-141">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="81392-141">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="81392-142">Descreve o caminho completo para o nó pai.</span><span class="sxs-lookup"><span data-stu-id="81392-142">Describes the full path to the parent node.</span></span> <span data-ttu-id="81392-143">Para essa classe, a cadeia de caracteres é "./DevDetail/Ext"</span><span class="sxs-lookup"><span data-stu-id="81392-143">For this class, the string is "./DevDetail/Ext"</span></span>

</dd> <dt>

[<span data-ttu-id="81392-144">ProcessorArchitecture</span><span class="sxs-lookup"><span data-stu-id="81392-144">ProcessorArchitecture</span></span>](/windows/client-management/mdm/devdetail-csp#ext-microsoft-processorarchitecture)
</dt> <dd> <dl> <dt>

<span data-ttu-id="81392-145">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="81392-145">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="81392-146">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="81392-146">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="81392-147">ProcessorType</span><span class="sxs-lookup"><span data-stu-id="81392-147">ProcessorType</span></span>](/windows/client-management/mdm/devdetail-csp#ext-microsoft-processortype)
</dt> <dd> <dl> <dt>

<span data-ttu-id="81392-148">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="81392-148">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="81392-149">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="81392-149">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="81392-150">RadioSwV</span><span class="sxs-lookup"><span data-stu-id="81392-150">RadioSwV</span></span>](/windows/client-management/mdm/devdetail-csp#ext-microsoft-radioswv)
</dt> <dd> <dl> <dt>

<span data-ttu-id="81392-151">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="81392-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81392-152">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="81392-152">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="81392-153">Retorna o número de versão do software da pilha de rádio.</span><span class="sxs-lookup"><span data-stu-id="81392-153">Returns the radio stack software version number.</span></span>

</dd> <dt>

[<span data-ttu-id="81392-154">Resolução</span><span class="sxs-lookup"><span data-stu-id="81392-154">Resolution</span></span>](/windows/client-management/mdm/devdetail-csp#ext-microsoft-resolution)
</dt> <dd> <dl> <dt>

<span data-ttu-id="81392-155">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="81392-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81392-156">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="81392-156">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="81392-157">Requisitos</span><span class="sxs-lookup"><span data-stu-id="81392-157">Requirements</span></span>



| <span data-ttu-id="81392-158">Requisito</span><span class="sxs-lookup"><span data-stu-id="81392-158">Requirement</span></span> | <span data-ttu-id="81392-159">Valor</span><span class="sxs-lookup"><span data-stu-id="81392-159">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81392-160">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="81392-160">Minimum supported client</span></span><br/> | <span data-ttu-id="81392-161">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="81392-161">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="81392-162">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="81392-162">Minimum supported server</span></span><br/> | <span data-ttu-id="81392-163">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="81392-163">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="81392-164">Namespace</span><span class="sxs-lookup"><span data-stu-id="81392-164">Namespace</span></span><br/>                | <span data-ttu-id="81392-165">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="81392-165">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="81392-166">MOF</span><span class="sxs-lookup"><span data-stu-id="81392-166">MOF</span></span><br/>                      | <dl> <span data-ttu-id="81392-167"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="81392-167"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="81392-168">DLL</span><span class="sxs-lookup"><span data-stu-id="81392-168">DLL</span></span><br/>                      | <dl> <span data-ttu-id="81392-169"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="81392-169"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81392-170">Confira também</span><span class="sxs-lookup"><span data-stu-id="81392-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81392-171">Como usar os scripts do PowerShell com o provedor de ponte WMI</span><span class="sxs-lookup"><span data-stu-id="81392-171">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

