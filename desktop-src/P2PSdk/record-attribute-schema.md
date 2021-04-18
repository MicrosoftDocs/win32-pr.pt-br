---
description: Os registros podem ter atributos específicos do aplicativo que são uma sequência de pares de nome ou valor representados como uma cadeia de caracteres XML no membro pszAttributes da estrutura de registro de mesmo nível \_ .
ms.assetid: 2991af9b-da32-4915-b4d6-575e3faac04e
title: Esquema de atributo de registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eefa8c4c8b00b09e9c8cb988088af645e9f9c967
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105780489"
---
# <a name="record-attribute-schema"></a><span data-ttu-id="de8a3-103">Esquema de atributo de registro</span><span class="sxs-lookup"><span data-stu-id="de8a3-103">Record Attribute Schema</span></span>

<span data-ttu-id="de8a3-104">Os registros podem ter atributos específicos do aplicativo que são uma sequência de pares de nome ou valor representados como uma cadeia de caracteres XML no membro **pszAttributes** da estrutura de [**\_ registro de mesmo nível**](/windows/desktop/api/P2P/ns-p2p-peer_record) .</span><span class="sxs-lookup"><span data-stu-id="de8a3-104">Records can have application-specific attributes that are a sequence of name or value pairs represented as an XML string in the **pszAttributes** member of the [**PEER\_RECORD**](/windows/desktop/api/P2P/ns-p2p-peer_record) structure.</span></span> <span data-ttu-id="de8a3-105">Os atributos são usados para filtrar uma pesquisa de registro iniciada por chamadas para [**PeerGroupSearchRecords**](/windows/desktop/api/P2P/nf-p2p-peergroupsearchrecords), que usa um filtro de pesquisa XML especificado no [formato de consulta de pesquisa de registro](record-search-query-format.md) como um parâmetro.</span><span class="sxs-lookup"><span data-stu-id="de8a3-105">The attributes are used to filter a record search initiated by calls to [**PeerGroupSearchRecords**](/windows/desktop/api/P2P/nf-p2p-peergroupsearchrecords), which takes an XML search filter specified in [Record Search Query Format](record-search-query-format.md) as a parameter.</span></span>

<span data-ttu-id="de8a3-106">Um atributo de registro pode ser um dos três tipos a seguir:</span><span class="sxs-lookup"><span data-stu-id="de8a3-106">A record attribute can be one of the following three types:</span></span>

-   <span data-ttu-id="de8a3-107">**int** é um valor inteiro.</span><span class="sxs-lookup"><span data-stu-id="de8a3-107">**int** is an integer value.</span></span>
-   <span data-ttu-id="de8a3-108">**Date** é um valor DateTime representado como um dos formatos padrão descritos em [https://www.w3.org/TR/NOTE-datetime](https://www.w3.org/TR/NOTE-datetime) .</span><span class="sxs-lookup"><span data-stu-id="de8a3-108">**date** is a datetime value represented as one of the standard formats described at [https://www.w3.org/TR/NOTE-datetime](https://www.w3.org/TR/NOTE-datetime).</span></span>
-   <span data-ttu-id="de8a3-109">**String** é um valor de cadeia de caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="de8a3-109">**string** is a Unicode string value.</span></span>

<span data-ttu-id="de8a3-110">A lista a seguir identifica os nomes de atributo específicos que são reservados pela infraestrutura de mesmo nível:</span><span class="sxs-lookup"><span data-stu-id="de8a3-110">The following list identifies the specific attribute names that are reserved by the Peer Infrastructure:</span></span>

-   <span data-ttu-id="de8a3-111">**peerlastmodifiedby**</span><span class="sxs-lookup"><span data-stu-id="de8a3-111">**peerlastmodifiedby**</span></span>
-   <span data-ttu-id="de8a3-112">**peercreatorid**</span><span class="sxs-lookup"><span data-stu-id="de8a3-112">**peercreatorid**</span></span>
-   <span data-ttu-id="de8a3-113">**peerlastmodificationtime**</span><span class="sxs-lookup"><span data-stu-id="de8a3-113">**peerlastmodificationtime**</span></span>
-   <span data-ttu-id="de8a3-114">**peerrecordid**</span><span class="sxs-lookup"><span data-stu-id="de8a3-114">**peerrecordid**</span></span>
-   <span data-ttu-id="de8a3-115">**peerrecordtype**</span><span class="sxs-lookup"><span data-stu-id="de8a3-115">**peerrecordtype**</span></span>
-   <span data-ttu-id="de8a3-116">**peercreationtime**</span><span class="sxs-lookup"><span data-stu-id="de8a3-116">**peercreationtime**</span></span>
-   <span data-ttu-id="de8a3-117">**peerlastmodificationtime**</span><span class="sxs-lookup"><span data-stu-id="de8a3-117">**peerlastmodificationtime**</span></span>

## <a name="example-of-defining-record-attributes"></a><span data-ttu-id="de8a3-118">Exemplo de definição de atributos de registro</span><span class="sxs-lookup"><span data-stu-id="de8a3-118">Example of Defining Record Attributes</span></span>

<span data-ttu-id="de8a3-119">O exemplo de esquema a seguir mostra como definir atributos de registro:</span><span class="sxs-lookup"><span data-stu-id="de8a3-119">The following schema example shows you how to define record attributes:</span></span>

``` syntax
<?xml version="1.0" encoding="utf-8" ?>
<xs:schema xmlns:xs="https://www.w3.org/2001/XMLSchema">
   <xs:simpleType name="alphanum">
       <xs:restriction base="xs:string">
          <xs:pattern value="\c+" />
       </xs:restriction>
   </xs:simpleType>
   <xs:complexType name="attributeType">
       <xs:simpleContent>
          <xs:extension base="xs:string">
                <xs:attribute name="name" type="alphanum" />
                <xs:attribute name="type">
                    <xs:simpleType>
                        <xs:restriction base="alphanum">
                           <xs:enumeration value="string"/>
                           <xs:enumeration value="date"/>
                           <xs:enumeration value="int"/>
                        </xs:restriction>
                    </xs:simpleType>
                </xs:attribute>
           </xs:extension>
       </xs:simpleContent>
    </xs:complexType>
    <xs:element name="attributes">
       <xs:complexType>
           <xs:sequence>
                <xs:element name="attribute" type="attributeType" minOccurs="0" maxOccurs="unbounded" />
           </xs:sequence>
       </xs:complexType>
    </xs:element>
</xs:schema>  
```

> [!Note]  
> <span data-ttu-id="de8a3-120">Os nomes de atributo devem ser sequências de caracteres alfanuméricos.</span><span class="sxs-lookup"><span data-stu-id="de8a3-120">Attribute names must be sequences of alphanumeric characters.</span></span> <span data-ttu-id="de8a3-121">Caracteres especiais como hifens ("-") e sublinhados (" \_ ") não são permitidos em um nome de atributo.</span><span class="sxs-lookup"><span data-stu-id="de8a3-121">Special characters like hyphens ("-") and underscores ("\_") are not allowed in an attribute name.</span></span>

 

<span data-ttu-id="de8a3-122">O exemplo a seguir de uma sequência de atributo XML contém os atributos **AuthenticationType** e **AuthExpires** personalizados que aparecem no membro **pszAttributes** do [**\_ registro de pares**](/windows/desktop/api/P2P/ns-p2p-peer_record).</span><span class="sxs-lookup"><span data-stu-id="de8a3-122">The following example of an XML attribute sequence contains the custom **AuthenticationType** and **AuthExpires** attributes that appear in the **pszAttributes** member of [**PEER\_RECORD**](/windows/desktop/api/P2P/ns-p2p-peer_record).</span></span>

``` syntax
<attributes>
  <attribute name="AuthenticationType" type="string">Kerberos</attribute><attribute name="AuthExpires" type="date">2002-01-31</attribute>
<attributes>
```

 

 



