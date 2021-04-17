---
title: Classe MDM_DevDetail
description: A \_ classe MDM DevDetail manipula o objeto de gerenciamento que fornece parâmetros específicos do dispositivo para o servidor OMA DM.
ms.assetid: 1a709051-656a-4900-b354-efbd208b46fc
keywords:
- Classe MDM_DevDetail
- Classe MDM_DevDetail, descrita
topic_type:
- apiref
api_name:
- MDM_DevDetail
- MDM_DevDetail.InstanceID
- MDM_DevDetail.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 751c4e147dd0b60398ed16eeb3eb60a8a768307f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105749067"
---
# <a name="mdm_devdetail-class"></a><span data-ttu-id="024b2-105">\_Classe DevDetail do MDM</span><span class="sxs-lookup"><span data-stu-id="024b2-105">MDM\_DevDetail class</span></span>

<span data-ttu-id="024b2-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="024b2-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="024b2-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="024b2-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="024b2-108">A classe **MDM \_ DevDetail** manipula o objeto de gerenciamento que fornece parâmetros específicos do dispositivo para o servidor OMA DM.</span><span class="sxs-lookup"><span data-stu-id="024b2-108">The **MDM\_DevDetail** class handles the management object which provides device-specific parameters to the OMA DM server.</span></span> <span data-ttu-id="024b2-109">Esses parâmetros de dispositivo não são enviados do cliente para o servidor automaticamente, mas podem ser consultados por servidores usando comandos OMA DM.</span><span class="sxs-lookup"><span data-stu-id="024b2-109">These device parameters are not sent from the client to the server automatically, but can be queried by servers using OMA DM commands.</span></span>

<span data-ttu-id="024b2-110">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="024b2-110">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="024b2-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="024b2-111">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_DevDetail
{
  string  InstanceID;
  string  ParentID;
  string  DevTyp;
  string  OEM;
  string  FwV;
  string  SwV;
  string  HwV;
  boolean LrgObj;
};
```

## <a name="members"></a><span data-ttu-id="024b2-112">Membros</span><span class="sxs-lookup"><span data-stu-id="024b2-112">Members</span></span>

<span data-ttu-id="024b2-113">A classe **MDM \_ DevDetail** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="024b2-113">The **MDM\_DevDetail** class has these types of members:</span></span>

-   [<span data-ttu-id="024b2-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="024b2-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="024b2-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="024b2-115">Properties</span></span>

<span data-ttu-id="024b2-116">A classe **MDM \_ DevDetail** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="024b2-116">The **MDM\_DevDetail** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="024b2-117">DevTyp</span><span class="sxs-lookup"><span data-stu-id="024b2-117">DevTyp</span></span>](/windows/client-management/mdm/devdetail-csp#devtyp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="024b2-118">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="024b2-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="024b2-119">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="024b2-119">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="024b2-120">FwV</span><span class="sxs-lookup"><span data-stu-id="024b2-120">FwV</span></span>](/windows/client-management/mdm/devdetail-csp#fwv)
</dt> <dd> <dl> <dt>

<span data-ttu-id="024b2-121">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="024b2-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="024b2-122">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="024b2-122">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="024b2-123">HwV</span><span class="sxs-lookup"><span data-stu-id="024b2-123">HwV</span></span>](/windows/client-management/mdm/devdetail-csp#hwv)
</dt> <dd> <dl> <dt>

<span data-ttu-id="024b2-124">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="024b2-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="024b2-125">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="024b2-125">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="024b2-126">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="024b2-126">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="024b2-127">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="024b2-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="024b2-128">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="024b2-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="024b2-129">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="024b2-129">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="024b2-130">Identifica o nome do nó pai.</span><span class="sxs-lookup"><span data-stu-id="024b2-130">Identifies the name of the parent node.</span></span> <span data-ttu-id="024b2-131">Para essa classe, a cadeia de caracteres é "DevDetail"</span><span class="sxs-lookup"><span data-stu-id="024b2-131">For this class, the string is "DevDetail"</span></span>

</dd> <dt>

[<span data-ttu-id="024b2-132">LrgObj</span><span class="sxs-lookup"><span data-stu-id="024b2-132">LrgObj</span></span>](/windows/client-management/mdm/devdetail-csp#lrgobj)
</dt> <dd> <dl> <dt>

<span data-ttu-id="024b2-133">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="024b2-133">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="024b2-134">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="024b2-134">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="024b2-135">OEM</span><span class="sxs-lookup"><span data-stu-id="024b2-135">OEM</span></span>](/windows/client-management/mdm/devdetail-csp#oem)
</dt> <dd> <dl> <dt>

<span data-ttu-id="024b2-136">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="024b2-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="024b2-137">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="024b2-137">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="024b2-138">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="024b2-138">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="024b2-139">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="024b2-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="024b2-140">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="024b2-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="024b2-141">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="024b2-141">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="024b2-142">Descreve o caminho completo para o nó pai.</span><span class="sxs-lookup"><span data-stu-id="024b2-142">Describes the full path to the parent node.</span></span>

</dd> <dt>

[<span data-ttu-id="024b2-143">SwV</span><span class="sxs-lookup"><span data-stu-id="024b2-143">SwV</span></span>](/windows/client-management/mdm/devdetail-csp#swv)
</dt> <dd> <dl> <dt>

<span data-ttu-id="024b2-144">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="024b2-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="024b2-145">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="024b2-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="024b2-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="024b2-146">Requirements</span></span>



| <span data-ttu-id="024b2-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="024b2-147">Requirement</span></span> | <span data-ttu-id="024b2-148">Valor</span><span class="sxs-lookup"><span data-stu-id="024b2-148">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="024b2-149">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="024b2-149">Minimum supported client</span></span><br/> | <span data-ttu-id="024b2-150">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="024b2-150">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="024b2-151">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="024b2-151">Minimum supported server</span></span><br/> | <span data-ttu-id="024b2-152">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="024b2-152">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="024b2-153">Namespace</span><span class="sxs-lookup"><span data-stu-id="024b2-153">Namespace</span></span><br/>                | <span data-ttu-id="024b2-154">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="024b2-154">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="024b2-155">MOF</span><span class="sxs-lookup"><span data-stu-id="024b2-155">MOF</span></span><br/>                      | <dl> <span data-ttu-id="024b2-156"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="024b2-156"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="024b2-157">DLL</span><span class="sxs-lookup"><span data-stu-id="024b2-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="024b2-158"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="024b2-158"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="024b2-159">Confira também</span><span class="sxs-lookup"><span data-stu-id="024b2-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="024b2-160">Como usar os scripts do PowerShell com o provedor de ponte WMI</span><span class="sxs-lookup"><span data-stu-id="024b2-160">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

