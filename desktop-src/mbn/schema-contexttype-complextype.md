---
description: Especifica o contexto de connenction de um dispositivo de banda larga móvel.
ms.assetid: 513e744d-bd62-43e9-a636-6690867d8b9b
title: Tipo complexo contextType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- contextType
api_type:
- Schema
ms.openlocfilehash: 63d221c6bd388196abfb73a8ac38a26de516d0df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105749390"
---
# <a name="contexttype-complex-type"></a><span data-ttu-id="94dd5-103">Tipo complexo contextType</span><span class="sxs-lookup"><span data-stu-id="94dd5-103">contextType Complex Type</span></span>

<span data-ttu-id="94dd5-104">O tipo complexo **ContextType** especifica o contexto de connenction de um dispositivo de banda larga móvel.</span><span class="sxs-lookup"><span data-stu-id="94dd5-104">The **contextType** complex type specifies the connenction context of a Mobile Broadband device.</span></span>

``` syntax
<xs:complexType name="contextType">
    <xs:sequence>
        <xs:element name="AccessString"
            minOccurs="0"
        >
            <xs:simpleType>
                <xs:restriction
                    base="token"
                >
                    <xs:minLength
                        value="1"
                     />
                    <xs:maxLength
                        value="100"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
        <xs:element name="UserLogonCred"
            minOccurs="0"
        >
            <xs:complexType>
                <xs:sequence>
                    <xs:element name="UserName"
                        type="nameType"
                     />
                    <xs:element name="IgnorePassword"
                        type="boolean"
                        minOccurs="0"
                     />
                    <xs:element name="Password"
                        type="string"
                        minOccurs="0"
                     />
                </xs:sequence>
            </xs:complexType>
        </xs:element>
        <xs:element name="Compression"
            minOccurs="0"
        >
            <xs:simpleType>
                <xs:restriction
                    base="token"
                >
                    <xs:enumeration
                        value="DISABLE"
                     />
                    <xs:enumeration
                        value="ENABLE"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
        <xs:element name="AuthProtocol"
            minOccurs="0"
        >
            <xs:simpleType>
                <xs:restriction
                    base="token"
                >
                    <xs:enumeration
                        value="NONE"
                     />
                    <xs:enumeration
                        value="PAP"
                     />
                    <xs:enumeration
                        value="CHAP"
                     />
                    <xs:enumeration
                        value="MsCHAPv2"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="94dd5-105">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="94dd5-105">Child elements</span></span>



| <span data-ttu-id="94dd5-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="94dd5-106">Element</span></span>                                                               | <span data-ttu-id="94dd5-107">Type</span><span class="sxs-lookup"><span data-stu-id="94dd5-107">Type</span></span>                                           | <span data-ttu-id="94dd5-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="94dd5-108">Description</span></span>                                                                                    |
|-----------------------------------------------------------------------|------------------------------------------------|------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="94dd5-109">**AccessString**</span><span class="sxs-lookup"><span data-stu-id="94dd5-109">**AccessString**</span></span>](schema-accessstring-contexttype-element.md)       |                                                | <span data-ttu-id="94dd5-110">A cadeia de caracteres de APN ou de discagem a ser usada para estabelecer uma conexão de dados</span><span class="sxs-lookup"><span data-stu-id="94dd5-110">APN or dial string to be used to establish a data connection</span></span><br/>                        |
| [<span data-ttu-id="94dd5-111">**AuthProtocol**</span><span class="sxs-lookup"><span data-stu-id="94dd5-111">**AuthProtocol**</span></span>](schema-authprotocol-contexttype-element.md)       |                                                | <span data-ttu-id="94dd5-112">Protocolo de autenticação a ser usado para ativar um contexto PDP.</span><span class="sxs-lookup"><span data-stu-id="94dd5-112">Authentication protocol to be used for activating a PDP context.</span></span><br/>                    |
| [<span data-ttu-id="94dd5-113">**Compactação**</span><span class="sxs-lookup"><span data-stu-id="94dd5-113">**Compression**</span></span>](schema-compression-contexttype-element.md)         |                                                | <span data-ttu-id="94dd5-114">Especifica se a compactação será usada no link de dados para a transferência de dados e de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="94dd5-114">Specifies if compression will be used at the data link for header and data transfer</span></span><br/> |
| [<span data-ttu-id="94dd5-115">**IgnorePassword**</span><span class="sxs-lookup"><span data-stu-id="94dd5-115">**IgnorePassword**</span></span>](schema-ignorepassword-userlogoncred-element.md) | <span data-ttu-id="94dd5-116">booleano</span><span class="sxs-lookup"><span data-stu-id="94dd5-116">boolean</span></span>                                        | <span data-ttu-id="94dd5-117">Como lidar com senhas ao atualizar perfis.</span><span class="sxs-lookup"><span data-stu-id="94dd5-117">How to handle passwords when upgrading profiles.</span></span><br/>                                    |
| [<span data-ttu-id="94dd5-118">**Senha**</span><span class="sxs-lookup"><span data-stu-id="94dd5-118">**Password**</span></span>](schema-password-userlogoncred-element.md)             | <span data-ttu-id="94dd5-119">string</span><span class="sxs-lookup"><span data-stu-id="94dd5-119">string</span></span>                                         | <span data-ttu-id="94dd5-120">Senha usada para autenticar um usuário</span><span class="sxs-lookup"><span data-stu-id="94dd5-120">Password used to authenticate a user</span></span><br/>                                                |
| [<span data-ttu-id="94dd5-121">**UserLogonCred**</span><span class="sxs-lookup"><span data-stu-id="94dd5-121">**UserLogonCred**</span></span>](schema-userlogoncred-contexttype-element.md)     |                                                | <span data-ttu-id="94dd5-122">Faça logon em credenciais para uma conexão.</span><span class="sxs-lookup"><span data-stu-id="94dd5-122">Log on credentials for a connection.</span></span><br/>                                                |
| [<span data-ttu-id="94dd5-123">**Usu**</span><span class="sxs-lookup"><span data-stu-id="94dd5-123">**UserName**</span></span>](schema-username-userlogoncred-element.md)             | [<span data-ttu-id="94dd5-124">**nometype**</span><span class="sxs-lookup"><span data-stu-id="94dd5-124">**nameType**</span></span>](schema-nametype-simpletype.md) | <span data-ttu-id="94dd5-125">Nome de usuário para logon</span><span class="sxs-lookup"><span data-stu-id="94dd5-125">User name for logon</span></span><br/>                                                                 |



## <a name="requirements"></a><span data-ttu-id="94dd5-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="94dd5-126">Requirements</span></span>



| <span data-ttu-id="94dd5-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="94dd5-127">Requirement</span></span> | <span data-ttu-id="94dd5-128">Valor</span><span class="sxs-lookup"><span data-stu-id="94dd5-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="94dd5-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="94dd5-129">Minimum supported client</span></span><br/> | <span data-ttu-id="94dd5-130">Aplicativos de \[ aplicativos da área de trabalho do Windows 7 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="94dd5-130">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="94dd5-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="94dd5-131">Minimum supported server</span></span><br/> | <span data-ttu-id="94dd5-132">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="94dd5-132">None supported</span></span><br/>                         |



 

 




