---
description: A estrutura de dados PROPERTYINFO define uma propriedade do protocolo.
ms.assetid: 878777ab-141d-4cc5-b0c1-f2ac8f770bf0
title: Estrutura PROPERTYINFO (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PROPERTYINFO
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 435b08c5dd5e020dce2bde9be03a0d41299836c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921469"
---
# <a name="propertyinfo-structure"></a><span data-ttu-id="8c901-103">Estrutura de PROPERTYINFO</span><span class="sxs-lookup"><span data-stu-id="8c901-103">PROPERTYINFO structure</span></span>

<span data-ttu-id="8c901-104">A estrutura de dados **PROPERTYINFO** define uma propriedade do protocolo.</span><span class="sxs-lookup"><span data-stu-id="8c901-104">The **PROPERTYINFO** data structure defines one property of the protocol.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c901-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8c901-105">Syntax</span></span>


```C++
typedef struct _PROPERTYINFO {
  HPROPERTY hProperty;
  DWORD     Version;
  LPSTR     Label;
  LPSTR     Comment;
  BYTE      DataType;
  BYTE      DataQualifier;
  union {
    LPVOID  lpExtendedInfo;
    LPRANGE lpRange;
    LPSET   lpSet;
    DWORD   Bitmask;
    DWORD   Value;
  };
  WORD      FormatStringSize;
  LPVOID    InstanceData;
} PROPERTYINFO, *LPPROPERTYINFO;
```



## <a name="members"></a><span data-ttu-id="8c901-106">Membros</span><span class="sxs-lookup"><span data-stu-id="8c901-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="8c901-107">**hProperty**</span><span class="sxs-lookup"><span data-stu-id="8c901-107">**hProperty**</span></span>
</dt> <dd>

<span data-ttu-id="8c901-108">Defina esse campo como zero.</span><span class="sxs-lookup"><span data-stu-id="8c901-108">Set this field to zero.</span></span> <span data-ttu-id="8c901-109">Na saída, Monitor de Rede retorna um identificador para a propriedade depois que a propriedade é adicionada ao banco de dados de propriedades.</span><span class="sxs-lookup"><span data-stu-id="8c901-109">On output, Network Monitor returns a handle to the property after the property is added to the property database.</span></span>

</dd> <dt>

<span data-ttu-id="8c901-110">**Versão**</span><span class="sxs-lookup"><span data-stu-id="8c901-110">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="8c901-111">Reservado.</span><span class="sxs-lookup"><span data-stu-id="8c901-111">Reserved.</span></span> <span data-ttu-id="8c901-112">Deve ser definido como zero.</span><span class="sxs-lookup"><span data-stu-id="8c901-112">Must be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="8c901-113">**Rótulo**</span><span class="sxs-lookup"><span data-stu-id="8c901-113">**Label**</span></span>
</dt> <dd>

<span data-ttu-id="8c901-114">Nome da propriedade.</span><span class="sxs-lookup"><span data-stu-id="8c901-114">Name of the property.</span></span>

</dd> <dt>

<span data-ttu-id="8c901-115">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="8c901-115">**Comment**</span></span>
</dt> <dd>

<span data-ttu-id="8c901-116">Descrição da propriedade.</span><span class="sxs-lookup"><span data-stu-id="8c901-116">Description of the property.</span></span> <span data-ttu-id="8c901-117">A descrição é exibida na barra de Status Monitor de Rede.</span><span class="sxs-lookup"><span data-stu-id="8c901-117">The description appears on the Network Monitor status bar.</span></span>

</dd> <dt>

<span data-ttu-id="8c901-118">**DataType**</span><span class="sxs-lookup"><span data-stu-id="8c901-118">**DataType**</span></span>
</dt> <dd>

<span data-ttu-id="8c901-119">Tipo de dados da propriedade.</span><span class="sxs-lookup"><span data-stu-id="8c901-119">Data type of the property.</span></span> <span data-ttu-id="8c901-120">Esse membro pode ter um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="8c901-120">This member can have one of the following values.</span></span>



| <span data-ttu-id="8c901-121">Valor</span><span class="sxs-lookup"><span data-stu-id="8c901-121">Value</span></span>                                                                                                                                                                                                       | <span data-ttu-id="8c901-122">Significado</span><span class="sxs-lookup"><span data-stu-id="8c901-122">Meaning</span></span>                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PROP_TYPE_VOID"></span><span id="prop_type_void"></span><dl> <span data-ttu-id="8c901-123"><dt>**tipo de PROP \_ \_ void**</dt></span><span class="sxs-lookup"><span data-stu-id="8c901-123"><dt>**PROP\_TYPE\_VOID**</dt></span></span> </dl>                                           | <span data-ttu-id="8c901-124">O tipo de propriedade é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="8c901-124">Property type is unknown.</span></span> <span data-ttu-id="8c901-125">Não há comprimento ou formato implícito.</span><span class="sxs-lookup"><span data-stu-id="8c901-125">There is no implied length or format.</span></span><br/>                                                                                                                                                                                                                                  |
| <span id="PROP_TYPE_SUMMARY"></span><span id="prop_type_summary"></span><dl> <span data-ttu-id="8c901-126"><dt>**\_Resumo do tipo prop \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8c901-126"><dt>**PROP\_TYPE\_SUMMARY**</dt></span></span> </dl>                                  | <span data-ttu-id="8c901-127">Resumindo o tipo de propriedade.</span><span class="sxs-lookup"><span data-stu-id="8c901-127">Summarizing property type.</span></span> <span data-ttu-id="8c901-128">Indica a primeira instância de propriedade que o analisador anexa a um quadro.</span><span class="sxs-lookup"><span data-stu-id="8c901-128">Indicates the first property instance that the parser attaches to a frame.</span></span> <span data-ttu-id="8c901-129">O \_ \_ Resumo do tipo prop pode servir como um espaço reservado para grupos de propriedades.</span><span class="sxs-lookup"><span data-stu-id="8c901-129">PROP\_TYPE\_SUMMARY can serve as a placeholder for groups of properties.</span></span> <span data-ttu-id="8c901-130">Esse valor indica que a propriedade não está definida na *RFC* do protocolo.</span><span class="sxs-lookup"><span data-stu-id="8c901-130">This value indicates that the property is not defined in the protocol *RFC*.</span></span><br/> |
| <span id="PROP_TYPE_BYTE"></span><span id="prop_type_byte"></span><dl> <span data-ttu-id="8c901-131"><dt>**\_byte do tipo prop \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8c901-131"><dt>**PROP\_TYPE\_BYTE**</dt></span></span> </dl>                                           | <span data-ttu-id="8c901-132">Dados numéricos com um tamanho de um byte (entidade de 8 bits).</span><span class="sxs-lookup"><span data-stu-id="8c901-132">Numeric data with a size of one byte (8-bit entity).</span></span><br/>                                                                                                                                                                                                                                             |
| <span id="PROP_TYPE_WORD"></span><span id="prop_type_word"></span><dl> <span data-ttu-id="8c901-133"><dt>**tipo de PROP \_ \_ Word**</dt></span><span class="sxs-lookup"><span data-stu-id="8c901-133"><dt>**PROP\_TYPE\_WORD**</dt></span></span> </dl>                                           | <span data-ttu-id="8c901-134">Dados numéricos com um tamanho de dois bytes (entidade de 16 bits).</span><span class="sxs-lookup"><span data-stu-id="8c901-134">Numeric data with a size of two bytes (16-bit entity).</span></span><br/>                                                                                                                                                                                                                                           |
| <span id="PROP_TYPE_DWORD"></span><span id="prop_type_dword"></span><dl> <span data-ttu-id="8c901-135"><dt>**tipo de PROP \_ \_ DWORD**</dt></span><span class="sxs-lookup"><span data-stu-id="8c901-135"><dt>**PROP\_TYPE\_DWORD**</dt></span></span> </dl>                                        | <span data-ttu-id="8c901-136">Dados numéricos com um tamanho de quatro bytes (entidade de 32 bits).</span><span class="sxs-lookup"><span data-stu-id="8c901-136">Numeric data with a size of four bytes (32-bit entity).</span></span><br/>                                                                                                                                                                                                                                          |
| <span id="PROP_TYPE_LARGEINT"></span><span id="prop_type_largeint"></span><dl> <span data-ttu-id="8c901-137"><dt>**tipo de PROP \_ \_ LARGEINT**</dt></span><span class="sxs-lookup"><span data-stu-id="8c901-137"><dt>**PROP\_TYPE\_LARGEINT**</dt></span></span> </dl>                               | <span data-ttu-id="8c901-138">Dados numéricos com um tamanho de oito bytes (entidade de 64 bits).</span><span class="sxs-lookup"><span data-stu-id="8c901-138">Numeric data with a size of eight bytes (64-bit entity).</span></span><br/>                                                                                                                                                                                                                                         |
| <span id="PROP_TYPE_ADDR"></span><span id="prop_type_addr"></span><dl> <span data-ttu-id="8c901-139"><dt>**\_endereço do tipo prop \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8c901-139"><dt>**PROP\_TYPE\_ADDR**</dt></span></span> </dl>                                           | <span data-ttu-id="8c901-140">Endereço MAC (entidade de 6 bytes).</span><span class="sxs-lookup"><span data-stu-id="8c901-140">MAC address (6-byte entity).</span></span><br/>                                                                                                                                                                                                                                                                     |
| <span id="PROP_TYPE_TIME"></span><span id="prop_type_time"></span><dl> <span data-ttu-id="8c901-141"><dt>**\_hora do tipo de prop \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8c901-141"><dt>**PROP\_TYPE\_TIME**</dt></span></span> </dl>                                           | <span data-ttu-id="8c901-142">Estrutura **SYSTEMTIME** .</span><span class="sxs-lookup"><span data-stu-id="8c901-142">**SYSTEMTIME** structure.</span></span><br/>                                                                                                                                                                                                                                                                        |
| <span id="PROP_TYPE_STRING"></span><span id="prop_type_string"></span><dl> <span data-ttu-id="8c901-143"><dt>**Cadeia de caracteres do \_ tipo prop \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8c901-143"><dt>**PROP\_TYPE\_STRING**</dt></span></span> </dl>                                     | <span data-ttu-id="8c901-144">Dados de texto ASCII.</span><span class="sxs-lookup"><span data-stu-id="8c901-144">ASCII text data.</span></span> <span data-ttu-id="8c901-145">Este tipo de dados não é encerrado em nulo.</span><span class="sxs-lookup"><span data-stu-id="8c901-145">This data type is not NULL-terminated.</span></span> <br/> <span data-ttu-id="8c901-146">Para dados Unicode, quando os dados de texto ASCII são especificados, o \_ sinalizador Unicode IFLAG também deve ser definido quando a função de instância da propriedade Attach é chamada.</span><span class="sxs-lookup"><span data-stu-id="8c901-146">For Unicode data, when ASCII text data is specified, the IFLAG\_UNICODE flag must also be set when the attach property instance function is called.</span></span><br/>                                                                          |
| <span id="PROP_TYPE_IP_ADDRESS"></span><span id="prop_type_ip_address"></span><dl> <span data-ttu-id="8c901-147"><dt>**\_ \_ endereço IP do tipo prop \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8c901-147"><dt>**PROP\_TYPE\_IP\_ADDRESS**</dt></span></span> </dl>                        | <span data-ttu-id="8c901-148">Endereço IP.</span><span class="sxs-lookup"><span data-stu-id="8c901-148">IP Address.</span></span> <span data-ttu-id="8c901-149">(entidade de 4 bytes).</span><span class="sxs-lookup"><span data-stu-id="8c901-149">(4-byte entity).</span></span><br/>                                                                                                                                                                                                                                                                     |
| <span id="PROP_TYPE_IPX_ADDRESS"></span><span id="prop_type_ipx_address"></span><dl> <span data-ttu-id="8c901-150"><dt>**\_ \_ Endereço IPX do tipo prop \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8c901-150"><dt>**PROP\_TYPE\_IPX\_ADDRESS**</dt></span></span> </dl>                     | <span data-ttu-id="8c901-151">Endereço IPX.</span><span class="sxs-lookup"><span data-stu-id="8c901-151">IPX Address.</span></span> <span data-ttu-id="8c901-152">(entidade de 10 bytes).</span><span class="sxs-lookup"><span data-stu-id="8c901-152">(10-byte entity).</span></span><br/>                                                                                                                                                                                                                                                                   |
| <span id="PROP_TYPE_BYTESWAPPED_WORD"></span><span id="prop_type_byteswapped_word"></span><dl> <span data-ttu-id="8c901-153"><dt>**PROPs \_ Type \_ BYTESWAPPED \_ Word**</dt></span><span class="sxs-lookup"><span data-stu-id="8c901-153"><dt>**PROP\_TYPE\_BYTESWAPPED\_WORD**</dt></span></span> </dl>      | <span data-ttu-id="8c901-154">Obsoleto.</span><span class="sxs-lookup"><span data-stu-id="8c901-154">Obsolete.</span></span> <span data-ttu-id="8c901-155">Para dados do WORD trocados por byte, defina **DataType** como prop \_ Type \_ Word e defina o \_ sinalizador permutated IFLAG ao chamar uma função de instância de propriedade **Attach** .</span><span class="sxs-lookup"><span data-stu-id="8c901-155">For byte-swapped WORD data, set **DataType** to PROP\_TYPE\_WORD and set the IFLAG\_SWAPPED flag when calling an **Attach** property instance function.</span></span><br/>                                                                                                                                |
| <span id="PROP_TYPE_BYTESWAPPED_DWORD"></span><span id="prop_type_byteswapped_dword"></span><dl> <span data-ttu-id="8c901-156"><dt>**tipo de PROP \_ \_ BYTESWAPPED \_ DWORD**</dt></span><span class="sxs-lookup"><span data-stu-id="8c901-156"><dt>**PROP\_TYPE\_BYTESWAPPED\_DWORD**</dt></span></span> </dl>   | <span data-ttu-id="8c901-157">Obsoleto.</span><span class="sxs-lookup"><span data-stu-id="8c901-157">Obsolete.</span></span> <span data-ttu-id="8c901-158">Para dados DWORD trocados por byte, defina **DataType** como prop \_ Type \_ DWORD e defina o \_ sinalizador permutated IFLAG ao chamar uma função de instância da propriedade **Attach** .</span><span class="sxs-lookup"><span data-stu-id="8c901-158">For byte-swapped DWORD data, set **DataType** to PROP\_TYPE\_DWORD and set the IFLAG\_SWAPPED flag when calling an **Attach** property instance function.</span></span><br/>                                                                                                                              |
| <span id="PROP_TYPE_TYPED_STRING"></span><span id="prop_type_typed_string"></span><dl> <span data-ttu-id="8c901-159"><dt>**\_cadeia de \_ caracteres tipada do tipo prop \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8c901-159"><dt>**PROP\_TYPE\_TYPED\_STRING**</dt></span></span> </dl>                  | <span data-ttu-id="8c901-160">Obsoleto.</span><span class="sxs-lookup"><span data-stu-id="8c901-160">Obsolete.</span></span> <span data-ttu-id="8c901-161">Para dados de cadeia de caracteres de tipo variável, defina **DataType** como prop \_ Type \_ String e defina o \_ sinalizador Unicode IFLAG ao chamar uma função de instância de propriedade **Attach** .</span><span class="sxs-lookup"><span data-stu-id="8c901-161">For variable-type string data, set **DataType** to PROP\_TYPE\_STRING and set the IFLAG\_UNICODE flag when calling an **Attach** property instance function.</span></span><br/>                                                                                                                           |
| <span id="PROP_TYPE_RAW_DATA"></span><span id="prop_type_raw_data"></span><dl> <span data-ttu-id="8c901-162"><dt>**\_ \_ dados brutos do tipo prop \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8c901-162"><dt>**PROP\_TYPE\_RAW\_DATA**</dt></span></span> </dl>                              | <span data-ttu-id="8c901-163">Dados brutos de comprimento e formato desconhecidos.</span><span class="sxs-lookup"><span data-stu-id="8c901-163">Raw data of unknown length and format.</span></span><br/>                                                                                                                                                                                                                                                           |
| <span id="PROP_TYPE_COMMENT"></span><span id="prop_type_comment"></span><dl> <span data-ttu-id="8c901-164"><dt>**\_Comentário do tipo prop \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8c901-164"><dt>**PROP\_TYPE\_COMMENT**</dt></span></span> </dl>                                  | <span data-ttu-id="8c901-165">O mesmo que o tipo de PROP \_ \_ void.</span><span class="sxs-lookup"><span data-stu-id="8c901-165">Same as PROP\_TYPE\_VOID.</span></span><br/>                                                                                                                                                                                                                                                                        |
| <span id="PROP_TYPE_SRCFRIENDLYNAME"></span><span id="prop_type_srcfriendlyname"></span><dl> <span data-ttu-id="8c901-166"><dt>**tipo de PROP \_ \_ SRCFRIENDLYNAME**</dt></span><span class="sxs-lookup"><span data-stu-id="8c901-166"><dt>**PROP\_TYPE\_SRCFRIENDLYNAME**</dt></span></span> </dl>          | <span data-ttu-id="8c901-167">Endereço do nome amigável da fonte.</span><span class="sxs-lookup"><span data-stu-id="8c901-167">Address of source-friendly name.</span></span> <span data-ttu-id="8c901-168">Monitor de Rede não fornece suporte de formatação interno para esse tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="8c901-168">Network Monitor does not provide built-in formatting support for this data type.</span></span><br/>                                                                                                                                                                                |
| <span id="PROP_TYPE_DSTFRIENDLYNAME"></span><span id="prop_type_dstfriendlyname"></span><dl> <span data-ttu-id="8c901-169"><dt>**tipo de PROP \_ \_ DSTFRIENDLYNAME**</dt></span><span class="sxs-lookup"><span data-stu-id="8c901-169"><dt>**PROP\_TYPE\_DSTFRIENDLYNAME**</dt></span></span> </dl>          | <span data-ttu-id="8c901-170">Endereço do nome amigável de destino.</span><span class="sxs-lookup"><span data-stu-id="8c901-170">Address of destination friendly name.</span></span> <span data-ttu-id="8c901-171">Monitor de Rede não fornece suporte de formatação interno para esse tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="8c901-171">Network Monitor does not provide built-in formatting support for this data type.</span></span><br/>                                                                                                                                                                           |
| <span id="PROP_TYPE_TOKENRING_ADDRESS"></span><span id="prop_type_tokenring_address"></span><dl> <span data-ttu-id="8c901-172"><dt>**\_ \_ endereço TOKENRING do tipo prop \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8c901-172"><dt>**PROP\_TYPE\_TOKENRING\_ADDRESS**</dt></span></span> </dl>   | <span data-ttu-id="8c901-173">Endereço de token ring.</span><span class="sxs-lookup"><span data-stu-id="8c901-173">Token-ring address.</span></span> <span data-ttu-id="8c901-174">Monitor de Rede não fornece suporte de formatação interno para esse tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="8c901-174">Network Monitor does not provide built-in formatting support for this data type.</span></span><br/>                                                                                                                                                                                             |
| <span id="PROP_TYPE_FDDI_ADDRESS"></span><span id="prop_type_fddi_address"></span><dl> <span data-ttu-id="8c901-175"><dt>**\_ \_ endereço FDDI do tipo prop \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8c901-175"><dt>**PROP\_TYPE\_FDDI\_ADDRESS**</dt></span></span> </dl>                  | <span data-ttu-id="8c901-176">Endereço FDDI.</span><span class="sxs-lookup"><span data-stu-id="8c901-176">FDDI address.</span></span> <span data-ttu-id="8c901-177">Monitor de Rede não fornece suporte de formatação interno para esse tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="8c901-177">Network Monitor does not provide built-in formatting support for this data type.</span></span><br/>                                                                                                                                                                                                   |
| <span id="PROP_TYPE_ETHERNET_ADDRESS"></span><span id="prop_type_ethernet_address"></span><dl> <span data-ttu-id="8c901-178"><dt>**\_ \_ endereço Ethernet do tipo prop \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8c901-178"><dt>**PROP\_TYPE\_ETHERNET\_ADDRESS**</dt></span></span> </dl>      | <span data-ttu-id="8c901-179">Endereço Ethernet.</span><span class="sxs-lookup"><span data-stu-id="8c901-179">Ethernet address.</span></span> <span data-ttu-id="8c901-180">Monitor de Rede não fornece suporte de formatação interno para esse tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="8c901-180">Network Monitor does not provide built-in formatting support for this data type.</span></span><br/>                                                                                                                                                                                               |
| <span id="PROP_TYPE_OBJECT_IDENTIFIER"></span><span id="prop_type_object_identifier"></span><dl> <span data-ttu-id="8c901-181"><dt>**\_identificador de \_ objeto do tipo prop \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8c901-181"><dt>**PROP\_TYPE\_OBJECT\_IDENTIFIER**</dt></span></span> </dl>   | <span data-ttu-id="8c901-182">Identificador de objeto SNMP codificado em BER.</span><span class="sxs-lookup"><span data-stu-id="8c901-182">BER-encoded SNMP object identifier.</span></span><br/>                                                                                                                                                                                                                                                              |
| <span id="PROP_TYPE_VINES_IP_ADDRESS"></span><span id="prop_type_vines_ip_address"></span><dl> <span data-ttu-id="8c901-183"><dt>**\_ \_ endereço IP de Vines do tipo prop \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8c901-183"><dt>**PROP\_TYPE\_VINES\_IP\_ADDRESS**</dt></span></span> </dl>     | <span data-ttu-id="8c901-184">Endereço IP de Vines (entidade de 6 bytes).</span><span class="sxs-lookup"><span data-stu-id="8c901-184">Vines IP address (6-byte entity).</span></span><br/>                                                                                                                                                                                                                                                                |
| <span id="PROP_TYPE_VAR_LEN_SMALL_INT"></span><span id="prop_type_var_len_small_int"></span><dl> <span data-ttu-id="8c901-185"><dt>**tipo de PROP \_ \_ var \_ Len \_ pequeno \_ int**</dt></span><span class="sxs-lookup"><span data-stu-id="8c901-185"><dt>**PROP\_TYPE\_VAR\_LEN\_SMALL\_INT**</dt></span></span> </dl> | <span data-ttu-id="8c901-186">Valor numérico sem um comprimento predeterminado, mas não mais do que 8 bytes de comprimento.</span><span class="sxs-lookup"><span data-stu-id="8c901-186">Numeric value without a pre-determined length, but no more than 8 bytes long.</span></span> <span data-ttu-id="8c901-187">O comprimento dos dados anexados determina o comprimento do valor.</span><span class="sxs-lookup"><span data-stu-id="8c901-187">The length of the attached data determines the length of the value.</span></span><br/>                                                                                                                                                |



 

</dd> <dt>

<span data-ttu-id="8c901-188">**Dataqualificador**</span><span class="sxs-lookup"><span data-stu-id="8c901-188">**DataQualifier**</span></span>
</dt> <dd>

<span data-ttu-id="8c901-189">O qualificador de dados de uma propriedade.</span><span class="sxs-lookup"><span data-stu-id="8c901-189">The data qualifier of a property.</span></span> <span data-ttu-id="8c901-190">Esse membro fornece informações precisas sobre o tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="8c901-190">This member provides precise information about the data type.</span></span>

<span data-ttu-id="8c901-191">O **Dataqualificador** pode ter um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="8c901-191">**DataQualifier** can have one of the following values.</span></span>



| <span data-ttu-id="8c901-192">Valor</span><span class="sxs-lookup"><span data-stu-id="8c901-192">Value</span></span>                                                                                                                                                                                                  | <span data-ttu-id="8c901-193">Significado</span><span class="sxs-lookup"><span data-stu-id="8c901-193">Meaning</span></span>                                                                                                                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PROP_QUAL_NONE"></span><span id="prop_qual_none"></span><dl> <span data-ttu-id="8c901-194"><dt>**PROP \_ igual \_ None**</dt></span><span class="sxs-lookup"><span data-stu-id="8c901-194"><dt>**PROP\_QUAL\_NONE**</dt></span></span> </dl>                                      | <span data-ttu-id="8c901-195">O tipo de dados Property é a única especificação da propriedade.</span><span class="sxs-lookup"><span data-stu-id="8c901-195">The property data type is the only specification of the property.</span></span> <br/> <span data-ttu-id="8c901-196">Quando esse valor é definido, o membro Union da estrutura é definido como **NULL** e, em seguida, ignorado.</span><span class="sxs-lookup"><span data-stu-id="8c901-196">When this value is set, the union member of the structure is set to **NULL**, and then ignored.</span></span><br/>                                                                                                                                        |
| <span id="PROP_QUAL_RANGE"></span><span id="prop_qual_range"></span><dl> <span data-ttu-id="8c901-197"><dt>**\_intervalo de igual prop \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8c901-197"><dt>**PROP\_QUAL\_RANGE**</dt></span></span> </dl>                                   | <span data-ttu-id="8c901-198">Espera-se que o valor numérico esteja dentro de um determinado intervalo.</span><span class="sxs-lookup"><span data-stu-id="8c901-198">The numeric value is expected to be within a given range.</span></span> <span data-ttu-id="8c901-199">Defina o intervalo no membro **lpRange** .</span><span class="sxs-lookup"><span data-stu-id="8c901-199">Define the range in the **lpRange** member.</span></span><br/>                                                                                                                                                                                                                |
| <span id="PROP_QUAL_SET"></span><span id="prop_qual_set"></span><dl> <span data-ttu-id="8c901-200"><dt>**\_conjunto de igual prop \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8c901-200"><dt>**PROP\_QUAL\_SET**</dt></span></span> </dl>                                         | <span data-ttu-id="8c901-201">O valor de uma propriedade é comparado a um conjunto de valores que são especificados no membro **lpSet** da União da estrutura.</span><span class="sxs-lookup"><span data-stu-id="8c901-201">The value of a property is compared to a set of values that are specified in the **lpSet** member of the structure's union.</span></span> <span data-ttu-id="8c901-202">O valor de uma propriedade pode ser um **byte**, **Word**, **DWORD**, **LARGEINT** ou **time**.</span><span class="sxs-lookup"><span data-stu-id="8c901-202">The value of a property can be a **BYTE**, **WORD**, **DWORD**, **LARGEINT** or **TIME**.</span></span><br/>                                                                                                |
| <span id="PROP_QUAL_BITFIELD"></span><span id="prop_qual_bitfield"></span><dl> <span data-ttu-id="8c901-203"><dt>**campo de igual de PROP \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8c901-203"><dt>**PROP\_QUAL\_BITFIELD**</dt></span></span> </dl>                          | <span data-ttu-id="8c901-204">Obsoleto.</span><span class="sxs-lookup"><span data-stu-id="8c901-204">Obsolete.</span></span><br/>                                                                                                                                                                                                                                                                                                            |
| <span id="PROP_QUAL_LABELED_SET"></span><span id="prop_qual_labeled_set"></span><dl> <span data-ttu-id="8c901-205"><dt>**PROP \_ igual \_ rotulado \_ conjunto**</dt></span><span class="sxs-lookup"><span data-stu-id="8c901-205"><dt>**PROP\_QUAL\_LABELED\_SET**</dt></span></span> </dl>                | <span data-ttu-id="8c901-206">O valor de uma propriedade é comparado a um valor em um conjunto de pares de rótulo de valor.</span><span class="sxs-lookup"><span data-stu-id="8c901-206">The value of a property is compared to a value in a set of value label pairs.</span></span> <span data-ttu-id="8c901-207">Os pares de rótulo de valor são especificados no membro **lpSet** da União da estrutura.</span><span class="sxs-lookup"><span data-stu-id="8c901-207">The value label pairs are specified in the **lpSet** member of the structure's union.</span></span> <br/> <span data-ttu-id="8c901-208">No momento da exibição, se o valor da propriedade corresponder a um valor no conjunto, então o valor e o rótulo associado serão exibidos.</span><span class="sxs-lookup"><span data-stu-id="8c901-208">At display time, if the value of the property matches a value in the set, then both a value, and the associated label are displayed.</span></span><br/> |
| <span id="PROP_QUAL_LABELED_BITFIELD"></span><span id="prop_qual_labeled_bitfield"></span><dl> <span data-ttu-id="8c901-209"><dt>**PROP \_ igual \_ rotulado como campo de bits \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8c901-209"><dt>**PROP\_QUAL\_LABELED\_BITFIELD**</dt></span></span> </dl> | <span data-ttu-id="8c901-210">Obsoleto.</span><span class="sxs-lookup"><span data-stu-id="8c901-210">Obsolete.</span></span> <span data-ttu-id="8c901-211">\_ \_ Em vez disso, use os sinalizadores prop igual.</span><span class="sxs-lookup"><span data-stu-id="8c901-211">Use PROP\_QUAL\_FLAGS instead.</span></span><br/>                                                                                                                                                                                                                                                                             |
| <span id="PROP_QUAL_CONST"></span><span id="prop_qual_const"></span><dl> <span data-ttu-id="8c901-212"><dt>**\_igual \_ const de prop**</dt></span><span class="sxs-lookup"><span data-stu-id="8c901-212"><dt>**PROP\_QUAL\_CONST**</dt></span></span> </dl>                                   | <span data-ttu-id="8c901-213">O valor de uma propriedade é comparado a uma constante que é especificada no membro de **valor** da União.</span><span class="sxs-lookup"><span data-stu-id="8c901-213">The value of a property is compared to a constant that is specified in the **Value** member of the union.</span></span> <br/> <span data-ttu-id="8c901-214">No momento da exibição, se os valores de propriedade e a constante não corresponderem, uma mensagem de erro formatada será exibida com o valor definido como normal.</span><span class="sxs-lookup"><span data-stu-id="8c901-214">At display time, if the property values and constant do not match, a formatted error message appears with the value set as Normal.</span></span><br/>                                                             |
| <span id="PROP_QUAL_FLAGS"></span><span id="prop_qual_flags"></span><dl> <span data-ttu-id="8c901-215"><dt>**\_sinalizadores de igual de prop \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8c901-215"><dt>**PROP\_QUAL\_FLAGS**</dt></span></span> </dl>                                   | <span data-ttu-id="8c901-216">O valor da propriedade é comparado a BITs específicos identificados no membro **lpSet** da União.</span><span class="sxs-lookup"><span data-stu-id="8c901-216">The value of the property is compared to specific BITs identified in the **lpSet** member of the union.</span></span><br/>                                                                                                                                                                                                              |
| <span id="PROP_QUAL_ARRAY"></span><span id="prop_qual_array"></span><dl> <span data-ttu-id="8c901-217"><dt>**\_matriz igual \_ prop**</dt></span><span class="sxs-lookup"><span data-stu-id="8c901-217"><dt>**PROP\_QUAL\_ARRAY**</dt></span></span> </dl>                                   | <span data-ttu-id="8c901-218">O valor de uma propriedade especifica uma matriz de valores.</span><span class="sxs-lookup"><span data-stu-id="8c901-218">The value of a property specifies an array of values.</span></span> <span data-ttu-id="8c901-219">O comprimento dos dados anexados determina o comprimento de uma matriz.</span><span class="sxs-lookup"><span data-stu-id="8c901-219">The length of attached data determines the length of an array.</span></span> <br/> <span data-ttu-id="8c901-220">Quando o \_ valor da matriz prop igual \_ é definido, o membro Union da estrutura de dados **PROPERTYINFO** é definido como **NULL** e ignorado.</span><span class="sxs-lookup"><span data-stu-id="8c901-220">When the PROP\_QUAL\_ARRAY value is set, the union member of the **PROPERTYINFO** data structure is set to **NULL** and ignored.</span></span><br/>                                                    |



 

</dd> <dt>

<span data-ttu-id="8c901-221">**lpExtendedInfo**</span><span class="sxs-lookup"><span data-stu-id="8c901-221">**lpExtendedInfo**</span></span>
</dt> <dd>

<span data-ttu-id="8c901-222">Reservado (membro de União).</span><span class="sxs-lookup"><span data-stu-id="8c901-222">Reserved (member of union).</span></span>

</dd> <dt>

<span data-ttu-id="8c901-223">**lpRange**</span><span class="sxs-lookup"><span data-stu-id="8c901-223">**lpRange**</span></span>
</dt> <dd>

<span data-ttu-id="8c901-224">Ponteiro para uma estrutura de [intervalo](range.md) que define um intervalo de valores.</span><span class="sxs-lookup"><span data-stu-id="8c901-224">Pointer to a [RANGE](range.md) structure that defines a range of values.</span></span> <span data-ttu-id="8c901-225">Esse membro deve ser definido se o membro **Dataqualificador** dessa estrutura estiver definido como prop \_ igual \_ Range (membro of Union).</span><span class="sxs-lookup"><span data-stu-id="8c901-225">This member must be set if the **DataQualifier** member of this structure is set to PROP\_QUAL\_RANGE (member of union).</span></span>

</dd> <dt>

<span data-ttu-id="8c901-226">**lpSet**</span><span class="sxs-lookup"><span data-stu-id="8c901-226">**lpSet**</span></span>
</dt> <dd>

<span data-ttu-id="8c901-227">Ponteiro para uma estrutura de [conjunto](set.md) que especifica um conjunto de valores ou rótulos.</span><span class="sxs-lookup"><span data-stu-id="8c901-227">Pointer to a [SET](set.md) structure that specifies a set of values or labels.</span></span> <span data-ttu-id="8c901-228">Esse membro deve ser definido se o membro **Dataqualificador** da estrutura estiver definido como prop \_ igual \_ set, prop \_ igual \_ labeld \_ set ou os \_ sinalizadores igual prop \_ (member of Union).</span><span class="sxs-lookup"><span data-stu-id="8c901-228">This member must be set if the **DataQualifier** member of the structure is set to PROP\_QUAL\_SET, PROP\_QUAL\_LABELED\_SET, or PROP\_QUAL\_FLAGS (member of union).</span></span>

</dd> <dt>

<span data-ttu-id="8c901-229">**Bitmask**</span><span class="sxs-lookup"><span data-stu-id="8c901-229">**Bitmask**</span></span>
</dt> <dd>

<span data-ttu-id="8c901-230">Obsoleto (membro de União).</span><span class="sxs-lookup"><span data-stu-id="8c901-230">Obsolete (member of union).</span></span>

</dd> <dt>

<span data-ttu-id="8c901-231">**Valor**</span><span class="sxs-lookup"><span data-stu-id="8c901-231">**Value**</span></span>
</dt> <dd>

<span data-ttu-id="8c901-232">Valor constante usado quando **Dataqualificador** é definido como prop \_ igual \_ const (membro de Union).</span><span class="sxs-lookup"><span data-stu-id="8c901-232">Constant value used when the **DataQualifier** is set to PROP\_QUAL\_CONST (member of union).</span></span>

</dd> <dt>

<span data-ttu-id="8c901-233">**FormatStringSize**</span><span class="sxs-lookup"><span data-stu-id="8c901-233">**FormatStringSize**</span></span>
</dt> <dd>

<span data-ttu-id="8c901-234">Tamanho máximo usado somente para a descrição da propriedade.</span><span class="sxs-lookup"><span data-stu-id="8c901-234">Maximum size used only for the property description.</span></span>

</dd> <dt>

<span data-ttu-id="8c901-235">**InstanceData**</span><span class="sxs-lookup"><span data-stu-id="8c901-235">**InstanceData**</span></span>
</dt> <dd>

<span data-ttu-id="8c901-236">Especifique a função de formato que é chamada para formatar os dados exibidos para a propriedade.</span><span class="sxs-lookup"><span data-stu-id="8c901-236">Specify the format function that is called to format the displayed data for the property.</span></span> <span data-ttu-id="8c901-237">Para usar o formatador genérico, especifique a função **FormatPropertyInstance** .</span><span class="sxs-lookup"><span data-stu-id="8c901-237">To use the generic formatter, specify the **FormatPropertyInstance** function.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8c901-238">Comentários</span><span class="sxs-lookup"><span data-stu-id="8c901-238">Remarks</span></span>

<span data-ttu-id="8c901-239">A estrutura **PROPERTYINFO** é usada em chamadas para a função [AddProperty](/previous-versions/bb251873(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="8c901-239">The **PROPERTYINFO** structure is used in calls to the [AddProperty](/previous-versions/bb251873(v=msdn.10)) function.</span></span> <span data-ttu-id="8c901-240">A função **AddProperty** adiciona uma única definição de propriedade ao banco de [*dados de propriedades*](p.md)do analisador.</span><span class="sxs-lookup"><span data-stu-id="8c901-240">The **AddProperty** function adds a single property definition to the parser [*property database*](p.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8c901-241">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8c901-241">Requirements</span></span>



| <span data-ttu-id="8c901-242">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c901-242">Requirement</span></span> | <span data-ttu-id="8c901-243">Valor</span><span class="sxs-lookup"><span data-stu-id="8c901-243">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="8c901-244">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8c901-244">Minimum supported client</span></span><br/> | <span data-ttu-id="8c901-245">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="8c901-245">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="8c901-246">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8c901-246">Minimum supported server</span></span><br/> | <span data-ttu-id="8c901-247">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="8c901-247">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="8c901-248">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="8c901-248">Header</span></span><br/>                   | <dl> <span data-ttu-id="8c901-249"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="8c901-249"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c901-250">Confira também</span><span class="sxs-lookup"><span data-stu-id="8c901-250">See also</span></span>

<dl> <dt>

<span data-ttu-id="8c901-251">[AddProperty](/previous-versions/bb251873(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="8c901-251">[AddProperty](/previous-versions/bb251873(v=msdn.10))</span></span>
</dt> <dt>

[<span data-ttu-id="8c901-252">AMPLITUDE</span><span class="sxs-lookup"><span data-stu-id="8c901-252">RANGE</span></span>](range.md)
</dt> <dt>

[<span data-ttu-id="8c901-253">SET</span><span class="sxs-lookup"><span data-stu-id="8c901-253">SET</span></span>](set.md)
</dt> </dl>

 

