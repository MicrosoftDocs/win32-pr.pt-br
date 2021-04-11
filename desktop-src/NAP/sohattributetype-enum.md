---
title: Enumeração SoHAttributeType (NapProtocol. h)
description: Especifica o tipo de atributo armazenado no objeto TLV (tipo-tamanho-valor) do atributo.
ms.assetid: ba725bf1-1d0a-4489-b912-3e761557d772
keywords:
- SoHAttributeType de enumeração de NAP
topic_type:
- apiref
api_name:
- SoHAttributeType
api_location:
- NapProtocol.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db164bbedf2267aaa5941a21a56ccfd53e1e1646
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104295846"
---
# <a name="sohattributetype-enumeration"></a><span data-ttu-id="df648-104">Enumeração SoHAttributeType</span><span class="sxs-lookup"><span data-stu-id="df648-104">SoHAttributeType enumeration</span></span>

> [!Note]  
> <span data-ttu-id="df648-105">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="df648-105">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="df648-106">A enumeração **SoHAttributeType** especifica o tipo de atributo armazenado no objeto de tipo de valor de tamanho (TLV).</span><span class="sxs-lookup"><span data-stu-id="df648-106">The **SoHAttributeType** enumeration specifies the type of attribute stored in the attribute type-length-value (TLV) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="df648-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="df648-107">Syntax</span></span>


```C++
typedef enum tagSoHAttributeType { 
  sohAttributeTypeSystemHealthId          = 2,
  sohAttributeTypeIpv4FixupServers        = 3,
  sohAttributeTypeComplianceResultCodes   = 4,
  sohAttributeTypeTimeOfLastUpdate        = 5,
  sohAttributeTypeClientId                = 6,
  sohAttributeTypeVendorSpecific          = 7,
  sohAttributeTypeHealthClass             = 8,
  sohAttributeTypeSoftwareVersion         = 9,
  sohAttributeTypeProductName             = 10,
  sohAttributeTypeHealthClassStatus       = 11,
  sohAttributeTypeSoHGenerationTime       = 12,
  sohAttributeTypeErrorCodes              = 13,
  sohAttributeTypeFailureCategory         = 14,
  sohAttributeTypeIpv6FixupServers        = 15,
  sohAttributeTypeExtendedIsolationState  = 16
} SoHAttributeType;
```



## <a name="constants"></a><span data-ttu-id="df648-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="df648-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="df648-109"><span id="sohAttributeTypeSystemHealthId"></span><span id="sohattributetypesystemhealthid"></span><span id="SOHATTRIBUTETYPESYSTEMHEALTHID"></span>**sohAttributeTypeSystemHealthId**</span><span class="sxs-lookup"><span data-stu-id="df648-109"><span id="sohAttributeTypeSystemHealthId"></span><span id="sohattributetypesystemhealthid"></span><span id="SOHATTRIBUTETYPESYSTEMHEALTHID"></span>**sohAttributeTypeSystemHealthId**</span></span>
</dt> <dd>

<span data-ttu-id="df648-110">Especifica o tipo de atributo de ID de integridade do sistema.</span><span class="sxs-lookup"><span data-stu-id="df648-110">Specifies the system health ID attribute type.</span></span>

</dd> <dt>

<span data-ttu-id="df648-111"><span id="sohAttributeTypeIpv4FixupServers"></span><span id="sohattributetypeipv4fixupservers"></span><span id="SOHATTRIBUTETYPEIPV4FIXUPSERVERS"></span>**sohAttributeTypeIpv4FixupServers**</span><span class="sxs-lookup"><span data-stu-id="df648-111"><span id="sohAttributeTypeIpv4FixupServers"></span><span id="sohattributetypeipv4fixupservers"></span><span id="SOHATTRIBUTETYPEIPV4FIXUPSERVERS"></span>**sohAttributeTypeIpv4FixupServers**</span></span>
</dt> <dd>

<span data-ttu-id="df648-112">Especifica o tipo de atributo de servidor de correção IPv4.</span><span class="sxs-lookup"><span data-stu-id="df648-112">Specifies the IPv4 fix-up server attribute type.</span></span>

</dd> <dt>

<span data-ttu-id="df648-113"><span id="sohAttributeTypeComplianceResultCodes"></span><span id="sohattributetypecomplianceresultcodes"></span><span id="SOHATTRIBUTETYPECOMPLIANCERESULTCODES"></span>**sohAttributeTypeComplianceResultCodes**</span><span class="sxs-lookup"><span data-stu-id="df648-113"><span id="sohAttributeTypeComplianceResultCodes"></span><span id="sohattributetypecomplianceresultcodes"></span><span id="SOHATTRIBUTETYPECOMPLIANCERESULTCODES"></span>**sohAttributeTypeComplianceResultCodes**</span></span>
</dt> <dd>

<span data-ttu-id="df648-114">Especifica o tipo de atributo de código de resultado de conformidade.</span><span class="sxs-lookup"><span data-stu-id="df648-114">Specifies the compliance result code attribute type.</span></span>

</dd> <dt>

<span data-ttu-id="df648-115"><span id="sohAttributeTypeTimeOfLastUpdate"></span><span id="sohattributetypetimeoflastupdate"></span><span id="SOHATTRIBUTETYPETIMEOFLASTUPDATE"></span>**sohAttributeTypeTimeOfLastUpdate**</span><span class="sxs-lookup"><span data-stu-id="df648-115"><span id="sohAttributeTypeTimeOfLastUpdate"></span><span id="sohattributetypetimeoflastupdate"></span><span id="SOHATTRIBUTETYPETIMEOFLASTUPDATE"></span>**sohAttributeTypeTimeOfLastUpdate**</span></span>
</dt> <dd>

<span data-ttu-id="df648-116">Especifica a hora do último tipo de atributo de atualização.</span><span class="sxs-lookup"><span data-stu-id="df648-116">Specifies the time of the last update attribute type.</span></span>

</dd> <dt>

<span data-ttu-id="df648-117"><span id="sohAttributeTypeClientId"></span><span id="sohattributetypeclientid"></span><span id="SOHATTRIBUTETYPECLIENTID"></span>**sohAttributeTypeClientId**</span><span class="sxs-lookup"><span data-stu-id="df648-117"><span id="sohAttributeTypeClientId"></span><span id="sohattributetypeclientid"></span><span id="SOHATTRIBUTETYPECLIENTID"></span>**sohAttributeTypeClientId**</span></span>
</dt> <dd>

<span data-ttu-id="df648-118">Especifica o tipo de atributo de ID do cliente.</span><span class="sxs-lookup"><span data-stu-id="df648-118">Specifies the client ID attribute type.</span></span>

</dd> <dt>

<span data-ttu-id="df648-119"><span id="sohAttributeTypeVendorSpecific"></span><span id="sohattributetypevendorspecific"></span><span id="SOHATTRIBUTETYPEVENDORSPECIFIC"></span>**sohAttributeTypeVendorSpecific**</span><span class="sxs-lookup"><span data-stu-id="df648-119"><span id="sohAttributeTypeVendorSpecific"></span><span id="sohattributetypevendorspecific"></span><span id="SOHATTRIBUTETYPEVENDORSPECIFIC"></span>**sohAttributeTypeVendorSpecific**</span></span>
</dt> <dd>

<span data-ttu-id="df648-120">Especifica o tipo de atributo específico do fornecedor.</span><span class="sxs-lookup"><span data-stu-id="df648-120">Specifies the vendor-specific attribute type.</span></span>

</dd> <dt>

<span data-ttu-id="df648-121"><span id="sohAttributeTypeHealthClass"></span><span id="sohattributetypehealthclass"></span><span id="SOHATTRIBUTETYPEHEALTHCLASS"></span>**sohAttributeTypeHealthClass**</span><span class="sxs-lookup"><span data-stu-id="df648-121"><span id="sohAttributeTypeHealthClass"></span><span id="sohattributetypehealthclass"></span><span id="SOHATTRIBUTETYPEHEALTHCLASS"></span>**sohAttributeTypeHealthClass**</span></span>
</dt> <dd>

<span data-ttu-id="df648-122">Especifica o tipo de atributo de classe de integridade.</span><span class="sxs-lookup"><span data-stu-id="df648-122">Specifies the health class attribute type.</span></span>

</dd> <dt>

<span data-ttu-id="df648-123"><span id="sohAttributeTypeSoftwareVersion"></span><span id="sohattributetypesoftwareversion"></span><span id="SOHATTRIBUTETYPESOFTWAREVERSION"></span>**sohAttributeTypeSoftwareVersion**</span><span class="sxs-lookup"><span data-stu-id="df648-123"><span id="sohAttributeTypeSoftwareVersion"></span><span id="sohattributetypesoftwareversion"></span><span id="SOHATTRIBUTETYPESOFTWAREVERSION"></span>**sohAttributeTypeSoftwareVersion**</span></span>
</dt> <dd>

<span data-ttu-id="df648-124">Especifica o tipo de atributo da versão do software.</span><span class="sxs-lookup"><span data-stu-id="df648-124">Specifies the software version attribute type.</span></span>

</dd> <dt>

<span data-ttu-id="df648-125"><span id="sohAttributeTypeProductName"></span><span id="sohattributetypeproductname"></span><span id="SOHATTRIBUTETYPEPRODUCTNAME"></span>**sohAttributeTypeProductName**</span><span class="sxs-lookup"><span data-stu-id="df648-125"><span id="sohAttributeTypeProductName"></span><span id="sohattributetypeproductname"></span><span id="SOHATTRIBUTETYPEPRODUCTNAME"></span>**sohAttributeTypeProductName**</span></span>
</dt> <dd>

<span data-ttu-id="df648-126">Especifica o tipo de atributo nome do produto.</span><span class="sxs-lookup"><span data-stu-id="df648-126">Specifies the product name attribute type.</span></span>

</dd> <dt>

<span data-ttu-id="df648-127"><span id="sohAttributeTypeHealthClassStatus"></span><span id="sohattributetypehealthclassstatus"></span><span id="SOHATTRIBUTETYPEHEALTHCLASSSTATUS"></span>**sohAttributeTypeHealthClassStatus**</span><span class="sxs-lookup"><span data-stu-id="df648-127"><span id="sohAttributeTypeHealthClassStatus"></span><span id="sohattributetypehealthclassstatus"></span><span id="SOHATTRIBUTETYPEHEALTHCLASSSTATUS"></span>**sohAttributeTypeHealthClassStatus**</span></span>
</dt> <dd>

<span data-ttu-id="df648-128">Especifica o tipo de atributo de status da classe de integridade.</span><span class="sxs-lookup"><span data-stu-id="df648-128">Specifies the health class status attribute type.</span></span>

</dd> <dt>

<span data-ttu-id="df648-129"><span id="sohAttributeTypeSoHGenerationTime"></span><span id="sohattributetypesohgenerationtime"></span><span id="SOHATTRIBUTETYPESOHGENERATIONTIME"></span>**sohAttributeTypeSoHGenerationTime**</span><span class="sxs-lookup"><span data-stu-id="df648-129"><span id="sohAttributeTypeSoHGenerationTime"></span><span id="sohattributetypesohgenerationtime"></span><span id="SOHATTRIBUTETYPESOHGENERATIONTIME"></span>**sohAttributeTypeSoHGenerationTime**</span></span>
</dt> <dd>

<span data-ttu-id="df648-130">Especifica o tempo de geração da instrução do tipo de atributo de integridade.</span><span class="sxs-lookup"><span data-stu-id="df648-130">Specifies the generation time of the Statement of Health attribute type.</span></span>

</dd> <dt>

<span data-ttu-id="df648-131"><span id="sohAttributeTypeErrorCodes"></span><span id="sohattributetypeerrorcodes"></span><span id="SOHATTRIBUTETYPEERRORCODES"></span>**sohAttributeTypeErrorCodes**</span><span class="sxs-lookup"><span data-stu-id="df648-131"><span id="sohAttributeTypeErrorCodes"></span><span id="sohattributetypeerrorcodes"></span><span id="SOHATTRIBUTETYPEERRORCODES"></span>**sohAttributeTypeErrorCodes**</span></span>
</dt> <dd>

<span data-ttu-id="df648-132">Especifica o tipo de atributo de código de erro.</span><span class="sxs-lookup"><span data-stu-id="df648-132">Specifies the error code attribute type.</span></span>

</dd> <dt>

<span data-ttu-id="df648-133"><span id="sohAttributeTypeFailureCategory"></span><span id="sohattributetypefailurecategory"></span><span id="SOHATTRIBUTETYPEFAILURECATEGORY"></span>**sohAttributeTypeFailureCategory**</span><span class="sxs-lookup"><span data-stu-id="df648-133"><span id="sohAttributeTypeFailureCategory"></span><span id="sohattributetypefailurecategory"></span><span id="SOHATTRIBUTETYPEFAILURECATEGORY"></span>**sohAttributeTypeFailureCategory**</span></span>
</dt> <dd>

<span data-ttu-id="df648-134">Especifica o tipo de atributo de categoria de falha.</span><span class="sxs-lookup"><span data-stu-id="df648-134">Specifies the failure category attribute type.</span></span>

</dd> <dt>

<span data-ttu-id="df648-135"><span id="sohAttributeTypeIpv6FixupServers"></span><span id="sohattributetypeipv6fixupservers"></span><span id="SOHATTRIBUTETYPEIPV6FIXUPSERVERS"></span>**sohAttributeTypeIpv6FixupServers**</span><span class="sxs-lookup"><span data-stu-id="df648-135"><span id="sohAttributeTypeIpv6FixupServers"></span><span id="sohattributetypeipv6fixupservers"></span><span id="SOHATTRIBUTETYPEIPV6FIXUPSERVERS"></span>**sohAttributeTypeIpv6FixupServers**</span></span>
</dt> <dd>

<span data-ttu-id="df648-136">Especifica o tipo de atributo de servidor de correção IPv6.</span><span class="sxs-lookup"><span data-stu-id="df648-136">Specifies the IPv6 fix-up server attribute type.</span></span>

</dd> <dt>

<span data-ttu-id="df648-137"><span id="sohAttributeTypeExtendedIsolationState"></span><span id="sohattributetypeextendedisolationstate"></span><span id="SOHATTRIBUTETYPEEXTENDEDISOLATIONSTATE"></span>**sohAttributeTypeExtendedIsolationState**</span><span class="sxs-lookup"><span data-stu-id="df648-137"><span id="sohAttributeTypeExtendedIsolationState"></span><span id="sohattributetypeextendedisolationstate"></span><span id="SOHATTRIBUTETYPEEXTENDEDISOLATIONSTATE"></span>**sohAttributeTypeExtendedIsolationState**</span></span>
</dt> <dd>

<span data-ttu-id="df648-138">Especifica o tipo de atributo de estado de isolamento estendido.</span><span class="sxs-lookup"><span data-stu-id="df648-138">Specifies the extended isolation state attribute type.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="df648-139">Comentários</span><span class="sxs-lookup"><span data-stu-id="df648-139">Remarks</span></span>

<span data-ttu-id="df648-140">A estrutura [**SoHAttributeValue**](sohattributevalue-union.md) define os valores de atributo que correspondem a cada tipo de atributo.</span><span class="sxs-lookup"><span data-stu-id="df648-140">The [**SoHAttributeValue**](sohattributevalue-union.md) structure defines the attribute values that correspond to each attribute type.</span></span>

<span data-ttu-id="df648-141">Esses tipos de atributo são consumidos pelo sistema NAP:</span><span class="sxs-lookup"><span data-stu-id="df648-141">These attribute types are consumed by the NAP system:</span></span>

-   <span data-ttu-id="df648-142">sohAttributeTypeSystemHealthId</span><span class="sxs-lookup"><span data-stu-id="df648-142">sohAttributeTypeSystemHealthId</span></span>
-   <span data-ttu-id="df648-143">sohAttributeTypeIpv4FixupServers</span><span class="sxs-lookup"><span data-stu-id="df648-143">sohAttributeTypeIpv4FixupServers</span></span>
-   <span data-ttu-id="df648-144">sohAttributeTypeIpv6FixupServers</span><span class="sxs-lookup"><span data-stu-id="df648-144">sohAttributeTypeIpv6FixupServers</span></span>
-   <span data-ttu-id="df648-145">sohAttributeTypeComplianceResultCodes</span><span class="sxs-lookup"><span data-stu-id="df648-145">sohAttributeTypeComplianceResultCodes</span></span>
-   <span data-ttu-id="df648-146">sohAttributeTypeFailureCategory</span><span class="sxs-lookup"><span data-stu-id="df648-146">sohAttributeTypeFailureCategory</span></span>

<span data-ttu-id="df648-147">O restante dos tipos destina-se apenas a guiar o uso por SHAs e SHVs.</span><span class="sxs-lookup"><span data-stu-id="df648-147">The rest of the types are only intended to guide the usage by SHAs and SHVs.</span></span>

## <a name="requirements"></a><span data-ttu-id="df648-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="df648-148">Requirements</span></span>



| <span data-ttu-id="df648-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="df648-149">Requirement</span></span> | <span data-ttu-id="df648-150">Valor</span><span class="sxs-lookup"><span data-stu-id="df648-150">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="df648-151">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="df648-151">Minimum supported client</span></span><br/> | <span data-ttu-id="df648-152">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="df648-152">Windows Vista \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="df648-153">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="df648-153">Minimum supported server</span></span><br/> | <span data-ttu-id="df648-154">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="df648-154">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="df648-155">parâmetro</span><span class="sxs-lookup"><span data-stu-id="df648-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="df648-156"><dt>NapProtocol. h</dt></span><span class="sxs-lookup"><span data-stu-id="df648-156"><dt>NapProtocol.h</dt></span></span> </dl>   |
| <span data-ttu-id="df648-157">INSERI</span><span class="sxs-lookup"><span data-stu-id="df648-157">IDL</span></span><br/>                      | <dl> <span data-ttu-id="df648-158"><dt>NapProtocol. idl</dt></span><span class="sxs-lookup"><span data-stu-id="df648-158"><dt>NapProtocol.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df648-159">Confira também</span><span class="sxs-lookup"><span data-stu-id="df648-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df648-160">**SoHAttributeValue**</span><span class="sxs-lookup"><span data-stu-id="df648-160">**SoHAttributeValue**</span></span>](sohattributevalue-union.md)
</dt> <dt>

[<span data-ttu-id="df648-161">**SoHAttribute**</span><span class="sxs-lookup"><span data-stu-id="df648-161">**SoHAttribute**</span></span>](/windows/win32/api/naptypes/ns-naptypes-sohattribute)
</dt> <dt>

[<span data-ttu-id="df648-162">**SoH**</span><span class="sxs-lookup"><span data-stu-id="df648-162">**SoH**</span></span>](/windows/win32/api/naptypes/ns-naptypes-soh)
</dt> <dt>

[<span data-ttu-id="df648-163">**INapSoHConstructor**</span><span class="sxs-lookup"><span data-stu-id="df648-163">**INapSoHConstructor**</span></span>](inapsohconstructor.md)
</dt> <dt>

[<span data-ttu-id="df648-164">**INapSoHProcessor**</span><span class="sxs-lookup"><span data-stu-id="df648-164">**INapSoHProcessor**</span></span>](inapsohprocessor.md)
</dt> </dl>

 

 





