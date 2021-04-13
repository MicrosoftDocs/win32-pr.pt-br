---
title: SoHAttributeValue Union (NapProtocol. h)
description: Define o conteúdo do membro de tipo em uma estrutura SoHAttribute.
ms.assetid: 53b30455-33a5-4cf5-8d4e-f0fa8e4e1a12
keywords:
- NAP do SoHAttributeValue Union
topic_type:
- apiref
api_name:
- SoHAttributeValue
api_location:
- NapProtocol.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36660e4e360ff0df31bb3a76d06c50e5d366c894
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455721"
---
# <a name="sohattributevalue-union"></a><span data-ttu-id="a2951-104">SoHAttributeValue Union</span><span class="sxs-lookup"><span data-stu-id="a2951-104">SoHAttributeValue union</span></span>

> [!Note]  
> <span data-ttu-id="a2951-105">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="a2951-105">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="a2951-106">A União **SoHAttributeValue** define o conteúdo do membro de **tipo** em uma estrutura [**SoHAttribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute) .</span><span class="sxs-lookup"><span data-stu-id="a2951-106">The **SoHAttributeValue** union defines the contents of the **type** member in a [**SoHAttribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute) structure.</span></span> <span data-ttu-id="a2951-107">A estrutura da União **SoHAttributeValue** é determinada pelo [**SoHAttributeType**](sohattributetype-enum.md) especificado no membro de **tipo** da estrutura [**SoHAttribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute) .</span><span class="sxs-lookup"><span data-stu-id="a2951-107">The structure of the **SoHAttributeValue** union is determined by the [**SoHAttributeType**](sohattributetype-enum.md) specified in the **type** member of the [**SoHAttribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2951-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a2951-108">Syntax</span></span>


```C++
typedef union tagSoHAttributeValue {
  SystemHealthEntityId     idVal;
  struct tagIpv4Addresses {
    UINT16      count;
    Ipv4Address *addresses;
  } v4AddressesVal;
  struct tagIpv6Addresses {
    UINT16      count;
    Ipv6Address *addresses;
  } v6AddressesVal;
  ResultCodes              codesVal;
  FILETIME                 dateTimeVal;
  struct tagVendorSpecific {
    UINT32 vendorId;
    UINT16 size;
    BYTE   *vendorSpecificData;
  } vendorSpecificVal;
  UINT8                    uint8Val;
  struct tagOctetString {
    UINT16 size;
    BYTE   *data;
  } octetStringVal;
} SoHAttributeValue;
```



## <a name="members"></a><span data-ttu-id="a2951-109">Membros</span><span class="sxs-lookup"><span data-stu-id="a2951-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="a2951-110">**idVal**</span><span class="sxs-lookup"><span data-stu-id="a2951-110">**idVal**</span></span>
</dt> <dd>

<span data-ttu-id="a2951-111">**caso (sohAttributeTypeSystemHealthId)**</span><span class="sxs-lookup"><span data-stu-id="a2951-111">**case(sohAttributeTypeSystemHealthId)**</span></span>

<span data-ttu-id="a2951-112">Um [SystemHealthEntityId](nap-datatypes.md) exclusivo que contém a ID do Sha (agente de integridade do sistema) ou o SHV (validador da integridade do sistema) que construiu este pacote [**soh**](/windows/win32/api/naptypes/ns-naptypes-soh) .</span><span class="sxs-lookup"><span data-stu-id="a2951-112">A unique [SystemHealthEntityId](nap-datatypes.md) that contains the ID of the System Health Agent (SHA) or System Health Validator (SHV) that constructed this [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) packet.</span></span>

</dd> <dt>

<span data-ttu-id="a2951-113">**v4AddressesVal**</span><span class="sxs-lookup"><span data-stu-id="a2951-113">**v4AddressesVal**</span></span>
</dt> <dd>

<span data-ttu-id="a2951-114">**caso (sohAttributeTypeIpv4FixupServers)**</span><span class="sxs-lookup"><span data-stu-id="a2951-114">**case(sohAttributeTypeIpv4FixupServers)**</span></span>

<span data-ttu-id="a2951-115">Os endereços IPv4 dos servidores de correção em uso pelo sistema NAP.</span><span class="sxs-lookup"><span data-stu-id="a2951-115">The IPv4 addresses of the fix-up servers in use by the NAP system.</span></span>

<dl> <dt>

<span data-ttu-id="a2951-116">**contagem**</span><span class="sxs-lookup"><span data-stu-id="a2951-116">**count**</span></span>
</dt> <dd>

<span data-ttu-id="a2951-117">O número de endereços IPv4 no membro de **endereços** no intervalo de 1 a [**maxIpv4CountPerSoHAttribute**](nap-type-constants.md).</span><span class="sxs-lookup"><span data-stu-id="a2951-117">The number of IPv4 addresses in the **addresses** member in the range 1 to [**maxIpv4CountPerSoHAttribute**](nap-type-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="a2951-118">**atende**</span><span class="sxs-lookup"><span data-stu-id="a2951-118">**addresses**</span></span>
</dt> <dd>

<span data-ttu-id="a2951-119">Uma matriz de estruturas [**Ipv4Address**](/windows/win32/api/naptypes/ns-naptypes-ipv4address) que contêm os endereços IPv4.</span><span class="sxs-lookup"><span data-stu-id="a2951-119">An array of [**Ipv4Address**](/windows/win32/api/naptypes/ns-naptypes-ipv4address) structures that contain the IPv4 addresses.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="a2951-120">**v6AddressesVal**</span><span class="sxs-lookup"><span data-stu-id="a2951-120">**v6AddressesVal**</span></span>
</dt> <dd>

<span data-ttu-id="a2951-121">**caso (sohAttributeTypeIpv6FixupServers)**</span><span class="sxs-lookup"><span data-stu-id="a2951-121">**case(sohAttributeTypeIpv6FixupServers)**</span></span>

<span data-ttu-id="a2951-122">Os endereços IPv6 dos servidores de correção em uso pelo sistema NAP.</span><span class="sxs-lookup"><span data-stu-id="a2951-122">The IPv6 addresses of the fix-up servers in use by the NAP system.</span></span>

<dl> <dt>

<span data-ttu-id="a2951-123">**contagem**</span><span class="sxs-lookup"><span data-stu-id="a2951-123">**count**</span></span>
</dt> <dd>

<span data-ttu-id="a2951-124">O número de endereços IPv4 no membro de **endereços** no intervalo de 1 a [**maxIpv6CountPerSoHAttribute**](nap-type-constants.md).</span><span class="sxs-lookup"><span data-stu-id="a2951-124">The number of IPv4 addresses in the **addresses** member in the range 1 to [**maxIpv6CountPerSoHAttribute**](nap-type-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="a2951-125">**atende**</span><span class="sxs-lookup"><span data-stu-id="a2951-125">**addresses**</span></span>
</dt> <dd>

<span data-ttu-id="a2951-126">Uma matriz de estruturas [**Ipv6Address**](/windows/win32/api/naptypes/ns-naptypes-ipv6address) que contêm os endereços IPv4.</span><span class="sxs-lookup"><span data-stu-id="a2951-126">An array of [**Ipv6Address**](/windows/win32/api/naptypes/ns-naptypes-ipv6address) structures that contain the IPv4 addresses.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="a2951-127">**codesVal**</span><span class="sxs-lookup"><span data-stu-id="a2951-127">**codesVal**</span></span>
</dt> <dd>

<span data-ttu-id="a2951-128">**caso (sohAttributeTypeComplianceResultCodes, sohAttributeTypeErrorCodes)**</span><span class="sxs-lookup"><span data-stu-id="a2951-128">**case(sohAttributeTypeComplianceResultCodes, sohAttributeTypeErrorCodes)**</span></span>

<span data-ttu-id="a2951-129">Uma estrutura [**ResultCodes**](/windows/win32/api/naptypes/ns-naptypes-resultcodes) que contém os códigos de resultado de conformidade definidos pelo aplicativo das [**constantes de erro**](nap-error-constants.md)do cliente ou NAP.</span><span class="sxs-lookup"><span data-stu-id="a2951-129">A [**ResultCodes**](/windows/win32/api/naptypes/ns-naptypes-resultcodes) structure that contains either the application defined compliance result codes of the client or [**NAP error constants**](nap-error-constants.md).</span></span> <span data-ttu-id="a2951-130">Um pacote [**soh**](/windows/win32/api/naptypes/ns-naptypes-soh) deve conter esse TLV ou o TLV **sohAttributeTypeFailureCategory** .</span><span class="sxs-lookup"><span data-stu-id="a2951-130">An [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) packet must contain this TLV or the **sohAttributeTypeFailureCategory** TLV.</span></span>

</dd> <dt>

<span data-ttu-id="a2951-131">**dateTimeVal**</span><span class="sxs-lookup"><span data-stu-id="a2951-131">**dateTimeVal**</span></span>
</dt> <dd>

<span data-ttu-id="a2951-132">**caso (sohAttributeTypeTimeOfLastUpdate, sohAttributeTypeSoHGenerationTime)**</span><span class="sxs-lookup"><span data-stu-id="a2951-132">**case(sohAttributeTypeTimeOfLastUpdate, sohAttributeTypeSoHGenerationTime)**</span></span>

<span data-ttu-id="a2951-133">Uma estrutura [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime) que contém a hora da última atualização [**soh**](/windows/win32/api/naptypes/ns-naptypes-soh) ou o tempo de geração **soh** .</span><span class="sxs-lookup"><span data-stu-id="a2951-133">A [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime) structure that contains the time of the last [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) update or the **SoH** generation time.</span></span>

</dd> <dt>

<span data-ttu-id="a2951-134">**vendorSpecificVal**</span><span class="sxs-lookup"><span data-stu-id="a2951-134">**vendorSpecificVal**</span></span>
</dt> <dd>

<span data-ttu-id="a2951-135">**caso (sohAttributeTypeVendorSpecific)**</span><span class="sxs-lookup"><span data-stu-id="a2951-135">**case(sohAttributeTypeVendorSpecific)**</span></span>

<span data-ttu-id="a2951-136">Dados específicos do aplicativo que são definidos pelo fornecedor.</span><span class="sxs-lookup"><span data-stu-id="a2951-136">Application-specific data that is defined by the vendor.</span></span>

<dl> <dt>

<span data-ttu-id="a2951-137">**vendorId**</span><span class="sxs-lookup"><span data-stu-id="a2951-137">**vendorId**</span></span>
</dt> <dd>

<span data-ttu-id="a2951-138">Um identificador de 4 bytes que define a ID do par de SHA/SHV.</span><span class="sxs-lookup"><span data-stu-id="a2951-138">A 4-byte identifier that defines the SHA/SHV pair ID.</span></span> <span data-ttu-id="a2951-139">Os três primeiros bytes são o código de SMI atribuído pela IETF do fornecedor e o último byte identifica o próprio componente.</span><span class="sxs-lookup"><span data-stu-id="a2951-139">The first 3 bytes are the IETF-assigned SMI code of the vendor, and the last byte identifies the component itself.</span></span> <span data-ttu-id="a2951-140">Ao implementar um SHA ou SHV, não use os valores de ID atribuídos aos componentes internos da integridade do sistema da Microsoft nas [**constantes do fornecedor NAP**](nap-vendor-constants.md).</span><span class="sxs-lookup"><span data-stu-id="a2951-140">When implementing a SHA or SHV, do not use the ID values assigned to internal Microsoft system health components on [**NAP vendor constants**](nap-vendor-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="a2951-141">**size**</span><span class="sxs-lookup"><span data-stu-id="a2951-141">**size**</span></span>
</dt> <dd>

<span data-ttu-id="a2951-142">O tamanho, em bytes, dos dados do fornecedor no intervalo de 0 a ([**maxSoHAttributeSize**](nap-type-constants.md) -4).</span><span class="sxs-lookup"><span data-stu-id="a2951-142">The size, in bytes, of the vendor data in the range 0 to ([**maxSoHAttributeSize**](nap-type-constants.md) - 4).</span></span>

</dd> <dt>

<span data-ttu-id="a2951-143">**vendorSpecificData**</span><span class="sxs-lookup"><span data-stu-id="a2951-143">**vendorSpecificData**</span></span>
</dt> <dd>

<span data-ttu-id="a2951-144">Um ponteiro para os dados específicos do fornecedor na ordem de bytes da rede.</span><span class="sxs-lookup"><span data-stu-id="a2951-144">A pointer to the vendor specific data in network byte order.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="a2951-145">**uint8Val**</span><span class="sxs-lookup"><span data-stu-id="a2951-145">**uint8Val**</span></span>
</dt> <dd>

<span data-ttu-id="a2951-146">**Case (sohAttributeTypeHealthClass, sohAttributeTypeFailureCategory, sohAttributeTypeExtendedIsolationState)**</span><span class="sxs-lookup"><span data-stu-id="a2951-146">**case(sohAttributeTypeHealthClass, sohAttributeTypeFailureCategory,sohAttributeTypeExtendedIsolationState)**</span></span>

<span data-ttu-id="a2951-147">A classe de integridade, a categoria de falha ou o estado de isolamento estendido de um componente NAP como um valor [**HealthClassValue**](healthclassvalue-enum.md) ou [**FailureCategory**](/windows/win32/api/naptypes/ne-naptypes-failurecategory) ou uma estrutura [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) .</span><span class="sxs-lookup"><span data-stu-id="a2951-147">The health class, failure category, or extended isolation state of a NAP component as either a [**HealthClassValue**](healthclassvalue-enum.md) or [**FailureCategory**](/windows/win32/api/naptypes/ne-naptypes-failurecategory) value, or a [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) structure.</span></span>

</dd> <dt>

<span data-ttu-id="a2951-148">**octetStringVal**</span><span class="sxs-lookup"><span data-stu-id="a2951-148">**octetStringVal**</span></span>
</dt> <dd>

<span data-ttu-id="a2951-149">**default**</span><span class="sxs-lookup"><span data-stu-id="a2951-149">**default**</span></span>

<span data-ttu-id="a2951-150">Os seguintes valores de atributos são cadeias de caracteres de octeto:</span><span class="sxs-lookup"><span data-stu-id="a2951-150">The following attributes' values are octet strings:</span></span>

-   <span data-ttu-id="a2951-151">sohAttributeTypeSoftwareVersion</span><span class="sxs-lookup"><span data-stu-id="a2951-151">sohAttributeTypeSoftwareVersion</span></span>
-   <span data-ttu-id="a2951-152">sohAttributeTypeClientId</span><span class="sxs-lookup"><span data-stu-id="a2951-152">sohAttributeTypeClientId</span></span>
-   <span data-ttu-id="a2951-153">sohAttributeTypeProductName</span><span class="sxs-lookup"><span data-stu-id="a2951-153">sohAttributeTypeProductName</span></span>
-   <span data-ttu-id="a2951-154">sohAttributeTypeHealthClassStatus</span><span class="sxs-lookup"><span data-stu-id="a2951-154">sohAttributeTypeHealthClassStatus</span></span>

<span data-ttu-id="a2951-155">Para compatibilidade com o encaminhamento, todos os atributos não reconhecidos são retornados como cadeias de caracteres de octeto.</span><span class="sxs-lookup"><span data-stu-id="a2951-155">For forward compatibility, all unrecognized attributes are returned as octet strings.</span></span> <span data-ttu-id="a2951-156">**os dados** devem estar na ordem de bytes da rede.</span><span class="sxs-lookup"><span data-stu-id="a2951-156">**data** must be in network byte order.</span></span>

<dl> <dt>

<span data-ttu-id="a2951-157">**size**</span><span class="sxs-lookup"><span data-stu-id="a2951-157">**size**</span></span>
</dt> <dd>

<span data-ttu-id="a2951-158">O tamanho, em bytes, dos **dados** no intervalo de 0 a [**maxSoHAttributeSize**](nap-type-constants.md).</span><span class="sxs-lookup"><span data-stu-id="a2951-158">The size, in bytes, of **data** in the range 0 to [**maxSoHAttributeSize**](nap-type-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="a2951-159">**data**</span><span class="sxs-lookup"><span data-stu-id="a2951-159">**data**</span></span>
</dt> <dd>

<span data-ttu-id="a2951-160">Um ponteiro para o valor da cadeia de caracteres do octeto.</span><span class="sxs-lookup"><span data-stu-id="a2951-160">A pointer to the octet string value.</span></span>

</dd> </dl> </dd> </dl>

## <a name="actual-data-layout"></a><span data-ttu-id="a2951-161">Layout de dados real</span><span class="sxs-lookup"><span data-stu-id="a2951-161">Actual data layout</span></span>

<span data-ttu-id="a2951-162">Devido à natureza do ambiente de publicação do SDK, as uniões não são claramente representadas em blocos de sintaxe.</span><span class="sxs-lookup"><span data-stu-id="a2951-162">Due to the nature of the SDK publishing environment, unions are not clearly represented in syntax blocks.</span></span> <span data-ttu-id="a2951-163">Aqui está a sintaxe real do arquivo de cabeçalho NapProtocol. h.</span><span class="sxs-lookup"><span data-stu-id="a2951-163">Here is the actual syntax from the NapProtocol.h header file.</span></span>


```C++
#include <windows.h>

typedef [switch_type(SoHAttributeType)] 
   union tagSoHAttributeValue
   {
      [case(sohAttributeTypeSystemHealthId)]
         SystemHealthEntityId idVal;
   
      [case(sohAttributeTypeIpv4FixupServers)]
         struct tagIpv4Addresses
         {
            [range(1, maxIpv4CountPerSoHAttribute)] 
               UINT16 count;
            [size_is(count)] Ipv4Address* addresses;
         } v4AddressesVal;

      [case(sohAttributeTypeIpv6FixupServers)]
         struct tagIpv6Addresses
         {
            [range(1, maxIpv6CountPerSoHAttribute)]
               UINT16 count;
            [size_is(count)] Ipv6Address* addresses;
         } v6AddressesVal;

      [case(sohAttributeTypeComplianceResultCodes, 
            sohAttributeTypeErrorCodes)]
         ResultCodes codesVal;

      [case(sohAttributeTypeTimeOfLastUpdate, 
            sohAttributeTypeSoHGenerationTime)]
         FILETIME dateTimeVal;

      [case(sohAttributeTypeVendorSpecific)]
         struct tagVendorSpecific
         {
            UINT32 vendorId;
            [range(0, maxSoHAttributeSize - 4)] 
               UINT16 size;
            [size_is(size)] BYTE* vendorSpecificData;
         } vendorSpecificVal;

      [case(sohAttributeTypeHealthClass, 
            sohAttributeTypeFailureCategory,
            sohAttributeTypeExtendedIsolationState)]
         UINT8 uint8Val;

      [default]
         struct tagOctetString
         {
            [range(0, maxSoHAttributeSize)] UINT16 size;
            [size_is(size)] BYTE* data;
         } octetStringVal;

   } SoHAttributeValue;
};
```



## <a name="remarks"></a><span data-ttu-id="a2951-164">Comentários</span><span class="sxs-lookup"><span data-stu-id="a2951-164">Remarks</span></span>

<span data-ttu-id="a2951-165">Esses tipos de atributo são consumidos pelo sistema NAP:</span><span class="sxs-lookup"><span data-stu-id="a2951-165">These attribute types are consumed by the NAP system:</span></span>

-   <span data-ttu-id="a2951-166">sohAttributeTypeSystemHealthId</span><span class="sxs-lookup"><span data-stu-id="a2951-166">sohAttributeTypeSystemHealthId</span></span>
-   <span data-ttu-id="a2951-167">sohAttributeTypeIpv4FixupServers</span><span class="sxs-lookup"><span data-stu-id="a2951-167">sohAttributeTypeIpv4FixupServers</span></span>
-   <span data-ttu-id="a2951-168">sohAttributeTypeIpv6FixupServers</span><span class="sxs-lookup"><span data-stu-id="a2951-168">sohAttributeTypeIpv6FixupServers</span></span>
-   <span data-ttu-id="a2951-169">sohAttributeTypeComplianceResultCodes</span><span class="sxs-lookup"><span data-stu-id="a2951-169">sohAttributeTypeComplianceResultCodes</span></span>
-   <span data-ttu-id="a2951-170">sohAttributeTypeFailureCategory</span><span class="sxs-lookup"><span data-stu-id="a2951-170">sohAttributeTypeFailureCategory</span></span>

<span data-ttu-id="a2951-171">O restante dos [**SoHAttributeTypes**](sohattributetype-enum.md) são apenas uma orientação prescritiva para uso por SHAs e SHVs.</span><span class="sxs-lookup"><span data-stu-id="a2951-171">The rest of the [**SoHAttributeTypes**](sohattributetype-enum.md) are meant purely as prescriptive guidance for usage by SHAs and SHVs.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2951-172">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a2951-172">Requirements</span></span>



| <span data-ttu-id="a2951-173">Requisito</span><span class="sxs-lookup"><span data-stu-id="a2951-173">Requirement</span></span> | <span data-ttu-id="a2951-174">Valor</span><span class="sxs-lookup"><span data-stu-id="a2951-174">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2951-175">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a2951-175">Minimum supported client</span></span><br/> | <span data-ttu-id="a2951-176">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a2951-176">Windows Vista \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="a2951-177">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a2951-177">Minimum supported server</span></span><br/> | <span data-ttu-id="a2951-178">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a2951-178">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="a2951-179">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a2951-179">Header</span></span><br/>                   | <dl> <span data-ttu-id="a2951-180"><dt>NapProtocol. h</dt></span><span class="sxs-lookup"><span data-stu-id="a2951-180"><dt>NapProtocol.h</dt></span></span> </dl>   |
| <span data-ttu-id="a2951-181">INSERI</span><span class="sxs-lookup"><span data-stu-id="a2951-181">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a2951-182"><dt>NapProtocol. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a2951-182"><dt>NapProtocol.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2951-183">Confira também</span><span class="sxs-lookup"><span data-stu-id="a2951-183">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2951-184">Referência de NAP</span><span class="sxs-lookup"><span data-stu-id="a2951-184">NAP Reference</span></span>](nap-reference.md)
</dt> <dt>

[<span data-ttu-id="a2951-185">Estruturas de NAP</span><span class="sxs-lookup"><span data-stu-id="a2951-185">NAP Structures</span></span>](nap-structures.md)
</dt> </dl>

 

