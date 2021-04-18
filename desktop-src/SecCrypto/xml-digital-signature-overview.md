---
description: O XML é um padrão do setor para descrever dados estruturados. Uma assinatura digital XML é uma representação XML de uma assinatura digital que fornece a capacidade de verificar a origem e a integridade do documento XML e de dados referenciados externamente.
ms.assetid: 02ca8d9b-be08-4b15-895f-9c8c4b0ed536
title: Visão geral da assinatura digital XML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b41a1b748305ab26b686e126cd201ad9e7f34d51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105811046"
---
# <a name="xml-digital-signature-overview"></a><span data-ttu-id="5551b-104">Visão geral da assinatura digital XML</span><span class="sxs-lookup"><span data-stu-id="5551b-104">XML Digital Signature Overview</span></span>

<span data-ttu-id="5551b-105">O XML é um padrão do setor para descrever dados estruturados.</span><span class="sxs-lookup"><span data-stu-id="5551b-105">XML is an industry standard for describing structured data.</span></span> <span data-ttu-id="5551b-106">Uma assinatura digital XML é uma representação XML de uma [*assinatura digital*](../secgloss/d-gly.md) que fornece a capacidade de verificar a origem e a integridade do documento XML e de dados referenciados externamente.</span><span class="sxs-lookup"><span data-stu-id="5551b-106">An XML Digital Signature is an XML representation of a [*digital signature*](../secgloss/d-gly.md) that provides the ability to verify the origin and integrity of XML document and externally referenced data.</span></span> <span data-ttu-id="5551b-107">As assinaturas digitais XML podem ser usadas para assinar dados arbitrários, incluindo um documento ou fragmento XML, uma página HTML, texto sem formatação ou dados codificados em binários, como um arquivo JPEG.</span><span class="sxs-lookup"><span data-stu-id="5551b-107">XML digital signatures can be used to sign arbitrary data, including an XML document or fragment, an HTML page, plain text, or binary-encoded data such as a JPEG file.</span></span>

<span data-ttu-id="5551b-108">O formato de assinatura digital XML com suporte da API de assinatura digital CryptXML é especificado pela recomendação W3C de sintaxe e processamento (segunda edição) de assinatura XML.</span><span class="sxs-lookup"><span data-stu-id="5551b-108">The XML digital signature format supported by the CryptXML digital signature API is specified by the XML Signature Syntax and Processing (Second Edition) W3C recommendation.</span></span>

<span data-ttu-id="5551b-109">A assinatura digital CryptXML implementa o suporte para os tipos de assinatura necessários, algoritmos criptográficos, algoritmos de canonização e a transformação envelopada especificada.</span><span class="sxs-lookup"><span data-stu-id="5551b-109">The CryptXML digital signature implements support for the required signature types, cryptographic algorithms, canonicalization algorithms, and the specified enveloped transform.</span></span>

<span data-ttu-id="5551b-110">Os desenvolvedores podem estender o conjunto padrão de algoritmos criptográficos com suporte do CryptXML criando DLLs de extensão criptográfica.</span><span class="sxs-lookup"><span data-stu-id="5551b-110">Developers can extend the default set of cryptographic algorithms supported by CryptXML by creating cryptographic extension DLLs.</span></span> <span data-ttu-id="5551b-111">Os desenvolvedores também podem criar suas próprias transformações personalizadas e algoritmos de canonização na parte superior da API do CryptXML.</span><span class="sxs-lookup"><span data-stu-id="5551b-111">Developers can also create their own custom transforms and canonicalization algorithms on top of CryptXML API.</span></span> <span data-ttu-id="5551b-112">Os desenvolvedores podem usar as APIs do CryptXML com as APIs de certificado do Windows.</span><span class="sxs-lookup"><span data-stu-id="5551b-112">Developers can use the CryptXML APIs with the Windows certificate APIs.</span></span>

 

 
