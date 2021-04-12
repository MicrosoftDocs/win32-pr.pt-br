---
title: Classe MDM_VPNv2_CryptographySuite03
description: A \_ classe MDM VPNv2 \_ CryptographySuite03 contém informações de criptografia para o perfil VPN nativo.
ms.assetid: d8d16d43-bd54-4ca8-a850-ce48390df7d6
keywords:
- Classe MDM_VPNv2_CryptographySuite03
- Classe MDM_VPNv2_CryptographySuite03, descrita
topic_type:
- apiref
api_name:
- MDM_VPNv2_CryptographySuite03
- MDM_VPNv2_CryptographySuite03.InstanceID
- MDM_VPNv2_CryptographySuite03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 553f2dcddd4d7c7e0926945a80f74f6aba2a9467
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455164"
---
# <a name="mdm_vpnv2_cryptographysuite03-class"></a><span data-ttu-id="f2693-105">\_ \_ Classe CRYPTOGRAPHYSUITE03 do MDM VPNv2</span><span class="sxs-lookup"><span data-stu-id="f2693-105">MDM\_VPNv2\_CryptographySuite03 class</span></span>

<span data-ttu-id="f2693-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="f2693-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="f2693-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="f2693-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="f2693-108">A classe **MDM \_ VPNv2 \_ CryptographySuite03** contém informações de criptografia para o perfil VPN nativo.</span><span class="sxs-lookup"><span data-stu-id="f2693-108">The **MDM\_VPNv2\_CryptographySuite03** class contains cryptography information for the native VPN profile.</span></span>

<span data-ttu-id="f2693-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="f2693-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2693-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f2693-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_CryptographySuite03
{
  string InstanceID;
  string ParentID;
  string AuthenticationTransformConstants;
  string CipherTransformConstants;
  string EncryptionMethod;
  string IntegrityCheckMethod;
  string DHGroup;
  string PfsGroup;
};
```

## <a name="members"></a><span data-ttu-id="f2693-111">Membros</span><span class="sxs-lookup"><span data-stu-id="f2693-111">Members</span></span>

<span data-ttu-id="f2693-112">A **classe \_ \_ CryptographySuite03 de MDM VPNv2** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="f2693-112">The **MDM\_VPNv2\_CryptographySuite03** class has these types of members:</span></span>

-   [<span data-ttu-id="f2693-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f2693-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f2693-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f2693-114">Properties</span></span>

<span data-ttu-id="f2693-115">A **classe \_ \_ CryptographySuite03 do MDM VPNv2** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="f2693-115">The **MDM\_VPNv2\_CryptographySuite03** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="f2693-116">AuthenticationTransformConstants</span><span class="sxs-lookup"><span data-stu-id="f2693-116">AuthenticationTransformConstants</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-nativeprofile-cryptographysuite-authenticationtransformconstants)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2693-117">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f2693-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f2693-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f2693-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f2693-119">CipherTransformConstants</span><span class="sxs-lookup"><span data-stu-id="f2693-119">CipherTransformConstants</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-nativeprofile-cryptographysuite-ciphertransformconstants)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2693-120">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f2693-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f2693-121">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f2693-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f2693-122">DHGroup</span><span class="sxs-lookup"><span data-stu-id="f2693-122">DHGroup</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-nativeprofile-cryptographysuite-dhgroup)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2693-123">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f2693-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f2693-124">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f2693-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f2693-125">EncryptionMethod</span><span class="sxs-lookup"><span data-stu-id="f2693-125">EncryptionMethod</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-nativeprofile-cryptographysuite-encryptionmethod)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2693-126">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f2693-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f2693-127">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f2693-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f2693-128">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="f2693-128">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2693-129">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f2693-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f2693-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f2693-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f2693-131">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f2693-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="f2693-132">Nó que contém as propriedades de túneis IPSec.</span><span class="sxs-lookup"><span data-stu-id="f2693-132">Node containing the properties of IPSec tunnels.</span></span>

</dd> <dt>

[<span data-ttu-id="f2693-133">IntegrityCheckMethod</span><span class="sxs-lookup"><span data-stu-id="f2693-133">IntegrityCheckMethod</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-nativeprofile-cryptographysuite-integritycheckmethod)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2693-134">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f2693-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f2693-135">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f2693-135">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f2693-136">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="f2693-136">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2693-137">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f2693-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f2693-138">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f2693-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f2693-139">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f2693-139">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="f2693-140">Descreve o caminho completo para o nó pai.</span><span class="sxs-lookup"><span data-stu-id="f2693-140">Describes the full path to the parent node.</span></span> <span data-ttu-id="f2693-141">Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/VPNv2/*ProfileName*/NativeProfile"</span><span class="sxs-lookup"><span data-stu-id="f2693-141">For this class, the string is "./Vendor/MSFT/VPNv2/*ProfileName*/NativeProfile"</span></span>

</dd> <dt>

[<span data-ttu-id="f2693-142">PfsGroup</span><span class="sxs-lookup"><span data-stu-id="f2693-142">PfsGroup</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-nativeprofile-cryptographysuite-pfsgroup)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2693-143">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f2693-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f2693-144">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f2693-144">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f2693-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f2693-145">Requirements</span></span>



| <span data-ttu-id="f2693-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="f2693-146">Requirement</span></span> | <span data-ttu-id="f2693-147">Valor</span><span class="sxs-lookup"><span data-stu-id="f2693-147">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2693-148">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f2693-148">Minimum supported client</span></span><br/> | <span data-ttu-id="f2693-149">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="f2693-149">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f2693-150">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f2693-150">Minimum supported server</span></span><br/> | <span data-ttu-id="f2693-151">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="f2693-151">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="f2693-152">Namespace</span><span class="sxs-lookup"><span data-stu-id="f2693-152">Namespace</span></span><br/>                | <span data-ttu-id="f2693-153">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="f2693-153">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="f2693-154">MOF</span><span class="sxs-lookup"><span data-stu-id="f2693-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f2693-155"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f2693-155"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="f2693-156">DLL</span><span class="sxs-lookup"><span data-stu-id="f2693-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f2693-157"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f2693-157"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

