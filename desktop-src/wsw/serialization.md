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
# <a name="serialization"></a>Serialização

A serialização é o processo de gravar valores em estruturas de dados C (structs, matrizes e valores primitivos) como um elemento XML. A desserialização é o processo reverso.


A serialização é o processo de gravar valores em estruturas de dados C (estruturas, matrizes e valores primitivos) como um elemento XML. A desserialização é o processo reverso.

Ambos os processos dependem de uma descrição do mapeamento entre as estruturas de dados C e o XML.

![Diagrama mostrando como a serialização e a desserialização dependem de uma descrição do mapeamento entre as estruturas de dados C e o XML.](images/xmlmapping.png)

Para serializar um valor, o aplicativo chama [**WsWriteElement**](/windows/desktop/api/WebServices/nf-webservices-wswriteelement), [**WsWriteAttribute**](/windows/desktop/api/WebServices/nf-webservices-wswriteattribute) ou [**WsWriteType**](/windows/desktop/api/WebServices/nf-webservices-wswritetype).

Para desserializar um valor, o aplicativo chama [**WsReadElement**](/windows/desktop/api/WebServices/nf-webservices-wsreadelement), [**WsReadAttribute**](/windows/desktop/api/WebServices/nf-webservices-wsreadattribute) ou [**WsReadType**](/windows/desktop/api/WebServices/nf-webservices-wsreadtype).

## <a name="security"></a>Segurança

O [leitor de XML](xml-reader.md) é usado no processo de desserialização. Consulte a seção segurança em informações de segurança relacionadas ao XML Reader for XML.

O desserializador continua desserializando os dados até que ele tenha concluído a leitura do elemento que está sendo desserializado. O processo de desserialização falha quando encontra qualquer documento XML que não esteja de acordo com a descrição dos dados que estão sendo desserializados. Nesse ponto, o leitor de XML que está sendo usado torna-se inválido e um erro é retornado.

Por padrão, a desserialização é estrita. Algumas condições que fazem com que a desserialização falhe incluem, mas não se limitando a:

-   Os elementos esperados estão ausentes
-   Campos de elemento inesperados aparecem entre os elementos necessários
-   Conteúdo do elemento extra após os campos obrigatórios, a menos que o **WS_STRUCT_IGNORE_TRAILING_ELEMENT_CONTENT**
-   Atributos inesperados, a menos que [**WS struct ignore o sinalizador de \_ \_ \_ \_ atributos sem tratamento**](https://msdn.microsoft.com/library/Dd323454(v=VS.85).aspx) seja especificado
-   Valor de tipo de dados inesperado que está fora do intervalo especificado
-   A contagem do elemento repetitivo está fora do intervalo especificado

A serialização de uma grande quantidade de dados pode causar uma alocação de memória excessiva e pode causar um ataque de negação de serviço. O usuário que está desserializando os dados deve especificar um objeto de heap para alocar os dados, e o usuário pode usar o limite de alocação de heap para evitar ataques de alocação de memória.

Suporte de intervalo para tipos de dados, incluindo comprimento máximo para cadeia de caracteres, contagem máxima de elementos na matriz, etc. permite que o usuário controle o tamanho máximo para diferentes tipos de dados. O usuário pode especificar o intervalo na descrição ou no esquema de dados para limitar o tamanho máximo de dados diferentes.

Um valor de cadeia de caracteres contendo um zero inserido tem suporte nos formatos de conexão (text, binary, MTOM). Ao desserializar uma cadeia de caracteres com um zero inserido, o usuário deve usar uma cadeia de caracteres contada (WS \_ String) para que o zero não confunda o cálculo do comprimento da cadeia de caracteres. Se um valor de cadeia de caracteres contendo um zero inserido for desserializado em um campo que esteja esperando uma cadeia de caracteres terminada em zero, um erro será retornado e a desserialização falhará. Se Wsutil for usado para gerar descrições de dados,/String: \_ opção de cadeia de caracteres WS deve ser usada se for esperada uma cadeia de caracteres com zero inserido.

Os seguintes retornos de chamada são usados com serialização:

-   [**\_retorno de \_ chamada de comparação de duração WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_duration_comparison_callback)
-   [**\_retorno de \_ chamada do tipo leitura WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_read_type_callback)
-   [**\_retorno de \_ chamada de tipo de gravação WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_write_type_callback)

As seguintes enumerações são usadas com a serialização:

-   [**\_mapeamento de campo WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_field_mapping)
-   [**\_Opções de campo WS \_**](/windows/win32/api/webservices/ne-webservices-ws_xml_reader_encoding_type)
-   [**\_opção WS Read \_**](/windows/desktop/api/WebServices/ne-webservices-ws_read_option)
-   [**\_tipo WS**](/windows/desktop/api/WebServices/ne-webservices-ws_type)
-   [**\_mapeamento de tipo WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_type_mapping)
-   [**\_opção WS Write \_**](/windows/desktop/api/WebServices/ne-webservices-ws_write_option)

As funções a seguir são usadas com a serialização:

-   [**WsReadAttribute**](/windows/desktop/api/WebServices/nf-webservices-wsreadattribute)
-   [**WsReadElement**](/windows/desktop/api/WebServices/nf-webservices-wsreadelement)
-   [**WsReadType**](/windows/desktop/api/WebServices/nf-webservices-wsreadtype)
-   [**WsWriteAttribute**](/windows/desktop/api/WebServices/nf-webservices-wswriteattribute)
-   [**WsWriteElement**](/windows/desktop/api/WebServices/nf-webservices-wswriteelement)
-   [**WsWriteType**](/windows/desktop/api/WebServices/nf-webservices-wswritetype)

As seguintes estruturas são usadas com a serialização:

-   [**\_Descrição do atributo WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_attribute_description)
-   [**\_Descrição de bool do WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_bool_description)
-   [**Descrição de WS \_ bytes \_**](/windows/desktop/api/WebServices/ns-webservices-ws_bytes_description)
-   [**Descrição da matriz de WS- \_ byte \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_byte_array_description)
-   [**\_Descrição da \_ matriz de caracteres WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_char_array_description)
-   [**\_Descrição do \_ tipo \_ personalizado WS**](/windows/desktop/api/WebServices/ns-webservices-ws_custom_type_description)
-   [**Descrição do WS \_ DateTime \_**](/windows/desktop/api/WebServices/ns-webservices-ws_datetime_description)
-   [**Descrição do WS \_ decimal \_**](/windows/desktop/api/WebServices/ns-webservices-ws_decimal_description)
-   [**\_valor padrão do WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_default_value)
-   [**\_Descrição dupla do WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_double_description)
-   [**\_Descrição da duração de WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_duration_description)
-   [**\_Descrição do elemento WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description)
-   [**Descrição do endereço do ponto de \_ extremidade WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address_description)
-   [**Descrição de WS \_ enum \_**](/windows/desktop/api/WebServices/ns-webservices-ws_enum_description)
-   [**\_valor de enumeração WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_enum_value)
-   [**\_Descrição de falha do WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_fault_description)
-   [**\_Descrição do campo WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_field_description)
-   [**Descrição de WS \_ float \_**](/windows/desktop/api/WebServices/ns-webservices-ws_float_description)
-   [**Descrição do WS \_ GUID \_**](/windows/desktop/api/WebServices/ns-webservices-ws_guid_description)
-   [**Descrição do WS \_ Int16 \_**](/windows/desktop/api/WebServices/ns-webservices-ws_int16_description)
-   [**Descrição do WS \_ INT32 \_**](/windows/desktop/api/WebServices/ns-webservices-ws_int32_description)
-   [**Descrição de WS \_ Int64 \_**](/windows/desktop/api/WebServices/ns-webservices-ws_int64_description)
-   [**Descrição do WS \_ INT8 \_**](/windows/desktop/api/WebServices/ns-webservices-ws_int8_description)
-   [**\_intervalo de itens WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_item_range)
-   [**\_Descrição da cadeia de caracteres WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_string_description)
-   [**Descrição do WS \_ struct \_**](/windows/desktop/api/WebServices/ns-webservices-ws_struct_description)
-   [**Descrição do WS \_ TIMESPAN \_**](/windows/desktop/api/WebServices/ns-webservices-ws_timespan_description)
-   [**Descrição de WS \_ UINT16 \_**](/windows/desktop/api/WebServices/ns-webservices-ws_uint16_description)
-   [**Descrição de WS \_ UINT32 \_**](/windows/desktop/api/WebServices/ns-webservices-ws_uint32_description)
-   [**Descrição do WS \_ UINT64 \_**](/windows/desktop/api/WebServices/ns-webservices-ws_uint64_description)
-   [**Descrição do WS \_ UINT8 \_**](/windows/desktop/api/WebServices/ns-webservices-ws_uint8_description)
-   [**\_Descrição da União WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_union_description)
-   [**\_Descrição do \_ campo de União WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_union_field_description)
-   [**\_Descrição da \_ ID \_ exclusiva do WS**](/windows/desktop/api/WebServices/ns-webservices-ws_unique_id_description)
-   [**\_Descrição da \_ matriz WS UTF8 \_**](/windows/desktop/api/WebServices/ns-webservices-ws_utf8_array_description)
-   [**Descrição do WS \_ void \_**](/windows/desktop/api/WebServices/ns-webservices-ws_void_description)
-   [**Descrição do WS \_ WSZ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_wsz_description)
-   [**Descrição de QName de WS \_ XML \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_qname_description)
-   [**\_Descrição da \_ cadeia de caracteres XML do WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_string_description)

 

 




