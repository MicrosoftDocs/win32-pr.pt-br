---
title: Serialização
description: A serialização é o processo de gravar valores em estruturas de dados C (structs, matrizes e valores primitivos) como um elemento XML. A desserialização é o processo reverso.
ms.assetid: aa092156-30ae-4f8a-baa2-450f38a78153
keywords:
- Serviços Web de serialização para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63f986c6cec9a035424aaafe1c51f4dc0d3ee014
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/12/2021
ms.locfileid: "104172438"
---
# <a name="serialization"></a><span data-ttu-id="8495a-107">Serialização</span><span class="sxs-lookup"><span data-stu-id="8495a-107">Serialization</span></span>

<span data-ttu-id="8495a-108">A serialização é o processo de gravar valores em estruturas de dados C (structs, matrizes e valores primitivos) como um elemento XML.</span><span class="sxs-lookup"><span data-stu-id="8495a-108">Serialization is the process of writing values in C data structures (structs, arrays, and primitive values) as an XML element.</span></span> <span data-ttu-id="8495a-109">A desserialização é o processo reverso.</span><span class="sxs-lookup"><span data-stu-id="8495a-109">Deserialization is the reverse process.</span></span>


<span data-ttu-id="8495a-110">A serialização é o processo de gravar valores em estruturas de dados C (estruturas, matrizes e valores primitivos) como um elemento XML.</span><span class="sxs-lookup"><span data-stu-id="8495a-110">Serialization is the process of writing values in C data structures (structures, arrays, and primitive values) as an XML element.</span></span> <span data-ttu-id="8495a-111">A desserialização é o processo reverso.</span><span class="sxs-lookup"><span data-stu-id="8495a-111">Deserialization is the reverse process.</span></span>

<span data-ttu-id="8495a-112">Ambos os processos dependem de uma descrição do mapeamento entre as estruturas de dados C e o XML.</span><span class="sxs-lookup"><span data-stu-id="8495a-112">Both processes rely on a description of the mapping between the C data structures and the XML.</span></span>

![Diagrama mostrando como a serialização e a desserialização dependem de uma descrição do mapeamento entre as estruturas de dados C e o XML.](images/xmlmapping.png)

<span data-ttu-id="8495a-114">Para serializar um valor, o aplicativo chama [**WsWriteElement**](/windows/desktop/api/WebServices/nf-webservices-wswriteelement), [**WsWriteAttribute**](/windows/desktop/api/WebServices/nf-webservices-wswriteattribute) ou [**WsWriteType**](/windows/desktop/api/WebServices/nf-webservices-wswritetype).</span><span class="sxs-lookup"><span data-stu-id="8495a-114">To serialize a value, the application calls [**WsWriteElement**](/windows/desktop/api/WebServices/nf-webservices-wswriteelement), [**WsWriteAttribute**](/windows/desktop/api/WebServices/nf-webservices-wswriteattribute) or [**WsWriteType**](/windows/desktop/api/WebServices/nf-webservices-wswritetype).</span></span>

<span data-ttu-id="8495a-115">Para desserializar um valor, o aplicativo chama [**WsReadElement**](/windows/desktop/api/WebServices/nf-webservices-wsreadelement), [**WsReadAttribute**](/windows/desktop/api/WebServices/nf-webservices-wsreadattribute) ou [**WsReadType**](/windows/desktop/api/WebServices/nf-webservices-wsreadtype).</span><span class="sxs-lookup"><span data-stu-id="8495a-115">To deserialize a value, the application calls [**WsReadElement**](/windows/desktop/api/WebServices/nf-webservices-wsreadelement), [**WsReadAttribute**](/windows/desktop/api/WebServices/nf-webservices-wsreadattribute) or [**WsReadType**](/windows/desktop/api/WebServices/nf-webservices-wsreadtype).</span></span>

## <a name="security"></a><span data-ttu-id="8495a-116">Segurança</span><span class="sxs-lookup"><span data-stu-id="8495a-116">Security</span></span>

<span data-ttu-id="8495a-117">O [leitor de XML](xml-reader.md) é usado no processo de desserialização.</span><span class="sxs-lookup"><span data-stu-id="8495a-117">[XML Reader](xml-reader.md) is used in deserialization process.</span></span> <span data-ttu-id="8495a-118">Consulte a seção segurança em informações de segurança relacionadas ao XML Reader for XML.</span><span class="sxs-lookup"><span data-stu-id="8495a-118">Refer to the security section in XML Reader for XML related security information.</span></span>

<span data-ttu-id="8495a-119">O desserializador continua desserializando os dados até que ele tenha concluído a leitura do elemento que está sendo desserializado.</span><span class="sxs-lookup"><span data-stu-id="8495a-119">The deserializer continues to deserialize data until it has completed reading the element being deserialized.</span></span> <span data-ttu-id="8495a-120">O processo de desserialização falha quando encontra qualquer documento XML que não esteja de acordo com a descrição dos dados que estão sendo desserializados.</span><span class="sxs-lookup"><span data-stu-id="8495a-120">Deserialization process fails when it encounter any XML document that does not conform to the description of the data being deserialized.</span></span> <span data-ttu-id="8495a-121">Nesse ponto, o leitor de XML que está sendo usado torna-se inválido e um erro é retornado.</span><span class="sxs-lookup"><span data-stu-id="8495a-121">At that point XML reader being used becomes invalid, and an error is returned.</span></span>

<span data-ttu-id="8495a-122">Por padrão, a desserialização é estrita.</span><span class="sxs-lookup"><span data-stu-id="8495a-122">By default deserialization is strict.</span></span> <span data-ttu-id="8495a-123">Algumas condições que fazem com que a desserialização falhe incluem, mas não se limitando a:</span><span class="sxs-lookup"><span data-stu-id="8495a-123">Some conditions that cause deserialization to fail include but not limited to:</span></span>

-   <span data-ttu-id="8495a-124">Os elementos esperados estão ausentes</span><span class="sxs-lookup"><span data-stu-id="8495a-124">Expected elements is missing</span></span>
-   <span data-ttu-id="8495a-125">Campos de elemento inesperados aparecem entre os elementos necessários</span><span class="sxs-lookup"><span data-stu-id="8495a-125">Unexpected element fields appear between required elements</span></span>
-   <span data-ttu-id="8495a-126">Conteúdo do elemento extra após os campos obrigatórios, a menos que o **WS_STRUCT_IGNORE_TRAILING_ELEMENT_CONTENT**</span><span class="sxs-lookup"><span data-stu-id="8495a-126">Extra element content after required fields, unless the **WS_STRUCT_IGNORE_TRAILING_ELEMENT_CONTENT**</span></span>
-   <span data-ttu-id="8495a-127">Atributos inesperados, a menos que [**WS struct ignore o sinalizador de \_ \_ \_ \_ atributos sem tratamento**](https://msdn.microsoft.com/library/Dd323454(v=VS.85).aspx) seja especificado</span><span class="sxs-lookup"><span data-stu-id="8495a-127">Unexpected attributes, unless [**WS\_STRUCT\_IGNORE\_UNHANDLED\_ATTRIBUTES**](https://msdn.microsoft.com/library/Dd323454(v=VS.85).aspx) flag is specified</span></span>
-   <span data-ttu-id="8495a-128">Valor de tipo de dados inesperado que está fora do intervalo especificado</span><span class="sxs-lookup"><span data-stu-id="8495a-128">Unexpected data type value that is out of specified range</span></span>
-   <span data-ttu-id="8495a-129">A contagem do elemento repetitivo está fora do intervalo especificado</span><span class="sxs-lookup"><span data-stu-id="8495a-129">Count of repeating element is out of the specified range</span></span>

<span data-ttu-id="8495a-130">A serialização de uma grande quantidade de dados pode causar uma alocação de memória excessiva e pode causar um ataque de negação de serviço.</span><span class="sxs-lookup"><span data-stu-id="8495a-130">Serializing large amount of data might cause excessive memory allocation and can cause denial of service attack.</span></span> <span data-ttu-id="8495a-131">O usuário que está desserializando os dados deve especificar um objeto de heap para alocar os dados, e o usuário pode usar o limite de alocação de heap para evitar ataques de alocação de memória.</span><span class="sxs-lookup"><span data-stu-id="8495a-131">The user that is deserializing data must specify a Heap object to allocate the data, and the user can use the heap allocation limit to prevent memory allocation attack.</span></span>

<span data-ttu-id="8495a-132">Suporte de intervalo para tipos de dados, incluindo comprimento máximo para cadeia de caracteres, contagem máxima de elementos na matriz, etc. permite que o usuário controle o tamanho máximo para diferentes tipos de dados.</span><span class="sxs-lookup"><span data-stu-id="8495a-132">Range support for data types, including max length for string, max element count in array, etc. allows the user to control the maximum size for different data types.</span></span> <span data-ttu-id="8495a-133">O usuário pode especificar o intervalo na descrição ou no esquema de dados para limitar o tamanho máximo de dados diferentes.</span><span class="sxs-lookup"><span data-stu-id="8495a-133">User can specify range in data description or schema to limit the maximum size of different data.</span></span>

<span data-ttu-id="8495a-134">Um valor de cadeia de caracteres contendo um zero inserido tem suporte nos formatos de conexão (text, binary, MTOM).</span><span class="sxs-lookup"><span data-stu-id="8495a-134">A string value containing an embedded zero is supported in the wire formats (text, binary, MTOM).</span></span> <span data-ttu-id="8495a-135">Ao desserializar uma cadeia de caracteres com um zero inserido, o usuário deve usar uma cadeia de caracteres contada (WS \_ String) para que o zero não confunda o cálculo do comprimento da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="8495a-135">When deserializing a string with an embedded zero, the user should use a counted string (WS\_STRING) so the zero will not confuse the calculation of the length of the string.</span></span> <span data-ttu-id="8495a-136">Se um valor de cadeia de caracteres contendo um zero inserido for desserializado em um campo que esteja esperando uma cadeia de caracteres terminada em zero, um erro será retornado e a desserialização falhará.</span><span class="sxs-lookup"><span data-stu-id="8495a-136">If a string value containing an embedded zero is deserialized into a field that is expecting a zero-terminated string, an error is returned, and deserialization fails.</span></span> <span data-ttu-id="8495a-137">Se Wsutil for usado para gerar descrições de dados,/String: \_ opção de cadeia de caracteres WS deve ser usada se for esperada uma cadeia de caracteres com zero inserido.</span><span class="sxs-lookup"><span data-stu-id="8495a-137">If wsutil is used to generate data descriptions, /string:WS\_STRING option should be used if string with embedded zero is expected.</span></span>

<span data-ttu-id="8495a-138">Os seguintes retornos de chamada são usados com serialização:</span><span class="sxs-lookup"><span data-stu-id="8495a-138">The following callbacks are used with serialization:</span></span>

-   [<span data-ttu-id="8495a-139">**\_retorno de \_ chamada de comparação de duração WS \_**</span><span class="sxs-lookup"><span data-stu-id="8495a-139">**WS\_DURATION\_COMPARISON\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_duration_comparison_callback)
-   [<span data-ttu-id="8495a-140">**\_retorno de \_ chamada do tipo leitura WS \_**</span><span class="sxs-lookup"><span data-stu-id="8495a-140">**WS\_READ\_TYPE\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_read_type_callback)
-   [<span data-ttu-id="8495a-141">**\_retorno de \_ chamada de tipo de gravação WS \_**</span><span class="sxs-lookup"><span data-stu-id="8495a-141">**WS\_WRITE\_TYPE\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_write_type_callback)

<span data-ttu-id="8495a-142">As seguintes enumerações são usadas com a serialização:</span><span class="sxs-lookup"><span data-stu-id="8495a-142">The following enumerations are used with serialization:</span></span>

-   [<span data-ttu-id="8495a-143">**\_mapeamento de campo WS \_**</span><span class="sxs-lookup"><span data-stu-id="8495a-143">**WS\_FIELD\_MAPPING**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_field_mapping)
-   [<span data-ttu-id="8495a-144">**\_Opções de campo WS \_**</span><span class="sxs-lookup"><span data-stu-id="8495a-144">**WS\_FIELD\_OPTIONS**</span></span>](/windows/win32/api/webservices/ne-webservices-ws_xml_reader_encoding_type)
-   [<span data-ttu-id="8495a-145">**\_opção WS Read \_**</span><span class="sxs-lookup"><span data-stu-id="8495a-145">**WS\_READ\_OPTION**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_read_option)
-   [<span data-ttu-id="8495a-146">**\_tipo WS**</span><span class="sxs-lookup"><span data-stu-id="8495a-146">**WS\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_type)
-   [<span data-ttu-id="8495a-147">**\_mapeamento de tipo WS \_**</span><span class="sxs-lookup"><span data-stu-id="8495a-147">**WS\_TYPE\_MAPPING**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_type_mapping)
-   [<span data-ttu-id="8495a-148">**\_opção WS Write \_**</span><span class="sxs-lookup"><span data-stu-id="8495a-148">**WS\_WRITE\_OPTION**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_write_option)

<span data-ttu-id="8495a-149">As funções a seguir são usadas com a serialização:</span><span class="sxs-lookup"><span data-stu-id="8495a-149">The following functions are used with serialization:</span></span>

-   [<span data-ttu-id="8495a-150">**WsReadAttribute**</span><span class="sxs-lookup"><span data-stu-id="8495a-150">**WsReadAttribute**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsreadattribute)
-   [<span data-ttu-id="8495a-151">**WsReadElement**</span><span class="sxs-lookup"><span data-stu-id="8495a-151">**WsReadElement**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsreadelement)
-   [<span data-ttu-id="8495a-152">**WsReadType**</span><span class="sxs-lookup"><span data-stu-id="8495a-152">**WsReadType**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsreadtype)
-   [<span data-ttu-id="8495a-153">**WsWriteAttribute**</span><span class="sxs-lookup"><span data-stu-id="8495a-153">**WsWriteAttribute**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswriteattribute)
-   [<span data-ttu-id="8495a-154">**WsWriteElement**</span><span class="sxs-lookup"><span data-stu-id="8495a-154">**WsWriteElement**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswriteelement)
-   [<span data-ttu-id="8495a-155">**WsWriteType**</span><span class="sxs-lookup"><span data-stu-id="8495a-155">**WsWriteType**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswritetype)

<span data-ttu-id="8495a-156">As seguintes estruturas são usadas com a serialização:</span><span class="sxs-lookup"><span data-stu-id="8495a-156">The following structures are used with serialization:</span></span>

-   [<span data-ttu-id="8495a-157">**\_Descrição do atributo WS \_**</span><span class="sxs-lookup"><span data-stu-id="8495a-157">**WS\_ATTRIBUTE\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_attribute_description)
-   [<span data-ttu-id="8495a-158">**\_Descrição de bool do WS \_**</span><span class="sxs-lookup"><span data-stu-id="8495a-158">**WS\_BOOL\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_bool_description)
-   [<span data-ttu-id="8495a-159">**Descrição de WS \_ bytes \_**</span><span class="sxs-lookup"><span data-stu-id="8495a-159">**WS\_BYTES\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_bytes_description)
-   [<span data-ttu-id="8495a-160">**Descrição da matriz de WS- \_ byte \_ \_**</span><span class="sxs-lookup"><span data-stu-id="8495a-160">**WS\_BYTE\_ARRAY\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_byte_array_description)
-   [<span data-ttu-id="8495a-161">**\_Descrição da \_ matriz de caracteres WS \_**</span><span class="sxs-lookup"><span data-stu-id="8495a-161">**WS\_CHAR\_ARRAY\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_char_array_description)
-   [<span data-ttu-id="8495a-162">**\_Descrição do \_ tipo \_ personalizado WS**</span><span class="sxs-lookup"><span data-stu-id="8495a-162">**WS\_CUSTOM\_TYPE\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_custom_type_description)
-   [<span data-ttu-id="8495a-163">**Descrição do WS \_ DateTime \_**</span><span class="sxs-lookup"><span data-stu-id="8495a-163">**WS\_DATETIME\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_datetime_description)
-   [<span data-ttu-id="8495a-164">**Descrição do WS \_ decimal \_**</span><span class="sxs-lookup"><span data-stu-id="8495a-164">**WS\_DECIMAL\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_decimal_description)
-   [<span data-ttu-id="8495a-165">**\_valor padrão do WS \_**</span><span class="sxs-lookup"><span data-stu-id="8495a-165">**WS\_DEFAULT\_VALUE**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_default_value)
-   [<span data-ttu-id="8495a-166">**\_Descrição dupla do WS \_**</span><span class="sxs-lookup"><span data-stu-id="8495a-166">**WS\_DOUBLE\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_double_description)
-   [<span data-ttu-id="8495a-167">**\_Descrição da duração de WS \_**</span><span class="sxs-lookup"><span data-stu-id="8495a-167">**WS\_DURATION\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_duration_description)
-   [<span data-ttu-id="8495a-168">**\_Descrição do elemento WS \_**</span><span class="sxs-lookup"><span data-stu-id="8495a-168">**WS\_ELEMENT\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_element_description)
-   [<span data-ttu-id="8495a-169">**Descrição do endereço do ponto de \_ extremidade WS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="8495a-169">**WS\_ENDPOINT\_ADDRESS\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address_description)
-   [<span data-ttu-id="8495a-170">**Descrição de WS \_ enum \_**</span><span class="sxs-lookup"><span data-stu-id="8495a-170">**WS\_ENUM\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_enum_description)
-   [<span data-ttu-id="8495a-171">**\_valor de enumeração WS \_**</span><span class="sxs-lookup"><span data-stu-id="8495a-171">**WS\_ENUM\_VALUE**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_enum_value)
-   [<span data-ttu-id="8495a-172">**\_Descrição de falha do WS \_**</span><span class="sxs-lookup"><span data-stu-id="8495a-172">**WS\_FAULT\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_fault_description)
-   [<span data-ttu-id="8495a-173">**\_Descrição do campo WS \_**</span><span class="sxs-lookup"><span data-stu-id="8495a-173">**WS\_FIELD\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_field_description)
-   [<span data-ttu-id="8495a-174">**Descrição de WS \_ float \_**</span><span class="sxs-lookup"><span data-stu-id="8495a-174">**WS\_FLOAT\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_float_description)
-   [<span data-ttu-id="8495a-175">**Descrição do WS \_ GUID \_**</span><span class="sxs-lookup"><span data-stu-id="8495a-175">**WS\_GUID\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_guid_description)
-   [<span data-ttu-id="8495a-176">**Descrição do WS \_ Int16 \_**</span><span class="sxs-lookup"><span data-stu-id="8495a-176">**WS\_INT16\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_int16_description)
-   [<span data-ttu-id="8495a-177">**Descrição do WS \_ INT32 \_**</span><span class="sxs-lookup"><span data-stu-id="8495a-177">**WS\_INT32\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_int32_description)
-   [<span data-ttu-id="8495a-178">**Descrição de WS \_ Int64 \_**</span><span class="sxs-lookup"><span data-stu-id="8495a-178">**WS\_INT64\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_int64_description)
-   [<span data-ttu-id="8495a-179">**Descrição do WS \_ INT8 \_**</span><span class="sxs-lookup"><span data-stu-id="8495a-179">**WS\_INT8\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_int8_description)
-   [<span data-ttu-id="8495a-180">**\_intervalo de itens WS \_**</span><span class="sxs-lookup"><span data-stu-id="8495a-180">**WS\_ITEM\_RANGE**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_item_range)
-   [<span data-ttu-id="8495a-181">**\_Descrição da cadeia de caracteres WS \_**</span><span class="sxs-lookup"><span data-stu-id="8495a-181">**WS\_STRING\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_string_description)
-   [<span data-ttu-id="8495a-182">**Descrição do WS \_ struct \_**</span><span class="sxs-lookup"><span data-stu-id="8495a-182">**WS\_STRUCT\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_struct_description)
-   [<span data-ttu-id="8495a-183">**Descrição do WS \_ TIMESPAN \_**</span><span class="sxs-lookup"><span data-stu-id="8495a-183">**WS\_TIMESPAN\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_timespan_description)
-   [<span data-ttu-id="8495a-184">**Descrição de WS \_ UINT16 \_**</span><span class="sxs-lookup"><span data-stu-id="8495a-184">**WS\_UINT16\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_uint16_description)
-   [<span data-ttu-id="8495a-185">**Descrição de WS \_ UINT32 \_**</span><span class="sxs-lookup"><span data-stu-id="8495a-185">**WS\_UINT32\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_uint32_description)
-   [<span data-ttu-id="8495a-186">**Descrição do WS \_ UINT64 \_**</span><span class="sxs-lookup"><span data-stu-id="8495a-186">**WS\_UINT64\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_uint64_description)
-   [<span data-ttu-id="8495a-187">**Descrição do WS \_ UINT8 \_**</span><span class="sxs-lookup"><span data-stu-id="8495a-187">**WS\_UINT8\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_uint8_description)
-   [<span data-ttu-id="8495a-188">**\_Descrição da União WS \_**</span><span class="sxs-lookup"><span data-stu-id="8495a-188">**WS\_UNION\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_union_description)
-   [<span data-ttu-id="8495a-189">**\_Descrição do \_ campo de União WS \_**</span><span class="sxs-lookup"><span data-stu-id="8495a-189">**WS\_UNION\_FIELD\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_union_field_description)
-   [<span data-ttu-id="8495a-190">**\_Descrição da \_ ID \_ exclusiva do WS**</span><span class="sxs-lookup"><span data-stu-id="8495a-190">**WS\_UNIQUE\_ID\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_unique_id_description)
-   [<span data-ttu-id="8495a-191">**\_Descrição da \_ matriz WS UTF8 \_**</span><span class="sxs-lookup"><span data-stu-id="8495a-191">**WS\_UTF8\_ARRAY\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_utf8_array_description)
-   [<span data-ttu-id="8495a-192">**Descrição do WS \_ void \_**</span><span class="sxs-lookup"><span data-stu-id="8495a-192">**WS\_VOID\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_void_description)
-   [<span data-ttu-id="8495a-193">**Descrição do WS \_ WSZ \_**</span><span class="sxs-lookup"><span data-stu-id="8495a-193">**WS\_WSZ\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_wsz_description)
-   [<span data-ttu-id="8495a-194">**Descrição de QName de WS \_ XML \_ \_**</span><span class="sxs-lookup"><span data-stu-id="8495a-194">**WS\_XML\_QNAME\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_qname_description)
-   [<span data-ttu-id="8495a-195">**\_Descrição da \_ cadeia de caracteres XML do WS \_**</span><span class="sxs-lookup"><span data-stu-id="8495a-195">**WS\_XML\_STRING\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_string_description)

 

 




