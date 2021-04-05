---
title: Classe MDM_DevDetail_Ext01
description: A \_ classe MDM DevDetail \_ Ext01 lida com o objeto de gerenciamento que fornece parâmetros específicos do dispositivo para o servidor OMA DM.
ms.assetid: 8b8cb8e8-a299-4a87-8206-a846a79dd647
keywords:
- Classe MDM_DevDetail_Ext01
- Classe MDM_DevDetail_Ext01, descrita
topic_type:
- apiref
api_name:
- MDM_DevDetail_Ext01
- MDM_DevDetail_Ext01.InstanceID
- MDM_DevDetail_Ext01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed7d7b68ab192a50a4c029bf573f5de730b8e30b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644933"
---
# <a name="mdm_devdetail_ext01-class"></a><span data-ttu-id="63970-105">\_ \_ Classe EXT01 do MDM DevDetail</span><span class="sxs-lookup"><span data-stu-id="63970-105">MDM\_DevDetail\_Ext01 class</span></span>

<span data-ttu-id="63970-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="63970-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="63970-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="63970-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="63970-108">A classe **MDM \_ DevDetail \_ Ext01** lida com o objeto de gerenciamento que fornece parâmetros específicos do dispositivo para o servidor OMA DM.</span><span class="sxs-lookup"><span data-stu-id="63970-108">The **MDM\_DevDetail\_Ext01** class handles the management object which provides device-specific parameters to the OMA DM server.</span></span> <span data-ttu-id="63970-109">Esses parâmetros de dispositivo não são enviados do cliente para o servidor automaticamente, mas podem ser consultados por servidores usando comandos OMA DM.</span><span class="sxs-lookup"><span data-stu-id="63970-109">These device parameters are not sent from the client to the server automatically, but can be queried by servers using OMA DM commands.</span></span>

<span data-ttu-id="63970-110">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="63970-110">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="63970-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="63970-111">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_DevDetail_Ext01
{
  string InstanceID;
  string ParentID;
  string DeviceHardwareData;
  string WLANMACAddress;
};
```

## <a name="members"></a><span data-ttu-id="63970-112">Membros</span><span class="sxs-lookup"><span data-stu-id="63970-112">Members</span></span>

<span data-ttu-id="63970-113">A **classe \_ \_ Ext01 de MDM DevDetail** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="63970-113">The **MDM\_DevDetail\_Ext01** class has these types of members:</span></span>

-   [<span data-ttu-id="63970-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="63970-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="63970-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="63970-115">Properties</span></span>

<span data-ttu-id="63970-116">A **classe \_ \_ Ext01 do MDM DevDetail** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="63970-116">The **MDM\_DevDetail\_Ext01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="63970-117">DeviceHardwareData</span><span class="sxs-lookup"><span data-stu-id="63970-117">DeviceHardwareData</span></span>](/windows/client-management/mdm/devdetail-csp#devicehardwaredata)
</dt> <dd> <dl> <dt>

<span data-ttu-id="63970-118">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="63970-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="63970-119">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="63970-119">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="63970-120">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="63970-120">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63970-121">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="63970-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="63970-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="63970-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63970-123">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="63970-123">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="63970-124">Identifica o nome do nó pai.</span><span class="sxs-lookup"><span data-stu-id="63970-124">Identifies the name of the parent node.</span></span> <span data-ttu-id="63970-125">Para essa classe, a cadeia de caracteres é "ext"</span><span class="sxs-lookup"><span data-stu-id="63970-125">For this class, the string is "Ext"</span></span>

</dd> <dt>

<span data-ttu-id="63970-126">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="63970-126">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63970-127">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="63970-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="63970-128">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="63970-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63970-129">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="63970-129">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="63970-130">Descreve o caminho completo para o nó pai.</span><span class="sxs-lookup"><span data-stu-id="63970-130">Describes the full path to the parent node.</span></span> <span data-ttu-id="63970-131">Para essa classe, a cadeia de caracteres é "./DevDetail/"</span><span class="sxs-lookup"><span data-stu-id="63970-131">For this class, the string is "./DevDetail/"</span></span>

</dd> <dt>

[<span data-ttu-id="63970-132">WLANMACAddress</span><span class="sxs-lookup"><span data-stu-id="63970-132">WLANMACAddress</span></span>](/windows/client-management/mdm/devdetail-csp#ext-wlanmacaddress)
</dt> <dd> <dl> <dt>

<span data-ttu-id="63970-133">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="63970-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="63970-134">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="63970-134">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="63970-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="63970-135">Requirements</span></span>



| <span data-ttu-id="63970-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="63970-136">Requirement</span></span> | <span data-ttu-id="63970-137">Valor</span><span class="sxs-lookup"><span data-stu-id="63970-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63970-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="63970-138">Minimum supported client</span></span><br/> | <span data-ttu-id="63970-139">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="63970-139">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="63970-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="63970-140">Minimum supported server</span></span><br/> | <span data-ttu-id="63970-141">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="63970-141">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="63970-142">Namespace</span><span class="sxs-lookup"><span data-stu-id="63970-142">Namespace</span></span><br/>                | <span data-ttu-id="63970-143">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="63970-143">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="63970-144">MOF</span><span class="sxs-lookup"><span data-stu-id="63970-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="63970-145"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="63970-145"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="63970-146">DLL</span><span class="sxs-lookup"><span data-stu-id="63970-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="63970-147"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="63970-147"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63970-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="63970-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63970-149">Como usar os scripts do PowerShell com o provedor de ponte WMI</span><span class="sxs-lookup"><span data-stu-id="63970-149">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

