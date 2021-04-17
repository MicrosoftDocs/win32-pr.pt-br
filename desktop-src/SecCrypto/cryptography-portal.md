---
description: Use tecnologias de criptografia para criptografia de chave pública, algoritmos de criptografia, criptografia RSA e certificados digitais.
ms.assetid: c53af815-ee3f-417a-8e62-3a3689715bc6
title: Criptografia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 852b7c2b38ca5b7d330a70e91a5b7a9dd5bb6557
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105811286"
---
# <a name="cryptography"></a><span data-ttu-id="9fccc-103">Criptografia</span><span class="sxs-lookup"><span data-stu-id="9fccc-103">Cryptography</span></span>

## <a name="purpose"></a><span data-ttu-id="9fccc-104">Finalidade</span><span class="sxs-lookup"><span data-stu-id="9fccc-104">Purpose</span></span>

<span data-ttu-id="9fccc-105">Criptografia é o uso de códigos para converter dados para que apenas um destinatário específico possa lê-los, usando uma chave.</span><span class="sxs-lookup"><span data-stu-id="9fccc-105">Cryptography is the use of codes to convert data so that only a specific recipient will be able to read it, using a key.</span></span>

<span data-ttu-id="9fccc-106">As tecnologias de criptografia da Microsoft incluem CryptoAPI, CSP (provedores de serviços de criptografia), ferramentas de CryptoAPI, CAPICOM, a emissão e o gerenciamento de certificados e o desenvolvimento de infraestruturas de chave pública personalizáveis.</span><span class="sxs-lookup"><span data-stu-id="9fccc-106">Microsoft cryptographic technologies include CryptoAPI, Cryptographic Service Providers (CSP), CryptoAPI Tools, CAPICOM, WinTrust, issuing and managing certificates, and developing customizable public key infrastructures.</span></span> <span data-ttu-id="9fccc-107">O registro de certificado e de cartão inteligente, o gerenciamento de certificados e o desenvolvimento de módulos personalizados também são descritos.</span><span class="sxs-lookup"><span data-stu-id="9fccc-107">Certificate and smart card enrollment, certificate management, and custom module development are also described.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="9fccc-108">Público de desenvolvedores</span><span class="sxs-lookup"><span data-stu-id="9fccc-108">Developer audience</span></span>

<span data-ttu-id="9fccc-109">O CryptoAPI destina-se a ser usado por desenvolvedores de aplicativos baseados no Windows que permitirão que os usuários criem e troquem documentos e outros dados em um ambiente seguro, especialmente em mídias não seguras, como a Internet.</span><span class="sxs-lookup"><span data-stu-id="9fccc-109">CryptoAPI is intended for use by developers of Windows-based applications that will enable users to create and exchange documents and other data in a secure environment, especially over nonsecure media such as the Internet.</span></span> <span data-ttu-id="9fccc-110">Os desenvolvedores devem estar familiarizados com as linguagens de programação C e C++ e o ambiente de programação do Windows.</span><span class="sxs-lookup"><span data-stu-id="9fccc-110">Developers should be familiar with the C and C++ programming languages and the Windows programming environment.</span></span> <span data-ttu-id="9fccc-111">Embora não seja necessário, uma compreensão de criptografia ou de assuntos relacionados à segurança é aconselhada.</span><span class="sxs-lookup"><span data-stu-id="9fccc-111">Although not required, an understanding of cryptography or security-related subjects is advised.</span></span>

<span data-ttu-id="9fccc-112">O capicor é um componente somente de 32 bits que se destina ao uso por desenvolvedores que estão criando aplicativos usando a linguagem de programação Visual Basic Scripting Edition (VBScript) ou a linguagem de programação C++.</span><span class="sxs-lookup"><span data-stu-id="9fccc-112">CAPICOM is a 32-bit only component that is intended for use by developers who are creating applications using Visual Basic Scripting Edition (VBScript) programming language or the C++ programming language.</span></span> <span data-ttu-id="9fccc-113">O CAPICOM está disponível para uso nos sistemas operacionais especificados nos requisitos de Run-Time.</span><span class="sxs-lookup"><span data-stu-id="9fccc-113">CAPICOM is available for use in the operating systems specified in Run-Time Requirements.</span></span> <span data-ttu-id="9fccc-114">Para desenvolvimento futuro, recomendamos que você use o .NET Framework para implementar recursos de segurança.</span><span class="sxs-lookup"><span data-stu-id="9fccc-114">For future development, we recommend that you use the .NET Framework to implement security features.</span></span> <span data-ttu-id="9fccc-115">Para obter mais informações, consulte [alternativas ao uso do CApicom](alternatives-to-using-capicom.md).</span><span class="sxs-lookup"><span data-stu-id="9fccc-115">For more information, see [Alternatives to Using CAPICOM](alternatives-to-using-capicom.md).</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="9fccc-116">Requisitos de tempo de execução</span><span class="sxs-lookup"><span data-stu-id="9fccc-116">Run-time requirements</span></span>

<span data-ttu-id="9fccc-117">Para obter informações sobre os requisitos de tempo de execução para um determinado elemento de programação, consulte a seção requisitos da página de referência para esse elemento.</span><span class="sxs-lookup"><span data-stu-id="9fccc-117">For information about run-time requirements for a particular programming element, see the Requirements section of the reference page for that element.</span></span>

<span data-ttu-id="9fccc-118">CAPICOM 2.1.0.2 tem suporte nos seguintes sistemas operacionais e versões:</span><span class="sxs-lookup"><span data-stu-id="9fccc-118">CAPICOM 2.1.0.2 is supported on the following operating systems and versions:</span></span>

-   <span data-ttu-id="9fccc-119">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9fccc-119">Windows Server 2003</span></span>
-   <span data-ttu-id="9fccc-120">Windows XP</span><span class="sxs-lookup"><span data-stu-id="9fccc-120">Windows XP</span></span>

<span data-ttu-id="9fccc-121">O CAPICOM está disponível como um arquivo redistribuível que pode ser baixado de [Platform SDK Redistributable: CApicom](https://www.microsoft.com/download/details.aspx?id=25281).</span><span class="sxs-lookup"><span data-stu-id="9fccc-121">CAPICOM is available as a redistributable file that can be downloaded from [Platform SDK Redistributable: CAPICOM](https://www.microsoft.com/download/details.aspx?id=25281).</span></span>

<span data-ttu-id="9fccc-122">Os serviços de certificados requerem as seguintes versões desses sistemas operacionais:</span><span class="sxs-lookup"><span data-stu-id="9fccc-122">Certificate Services requires the following versions of these operating systems:</span></span>

-   <span data-ttu-id="9fccc-123">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9fccc-123">Windows Server 2008 R2</span></span>
-   <span data-ttu-id="9fccc-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9fccc-124">Windows Server 2008</span></span>
-   <span data-ttu-id="9fccc-125">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9fccc-125">Windows Server 2003</span></span>

## <a name="in-this-section"></a><span data-ttu-id="9fccc-126">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="9fccc-126">In this section</span></span>



| <span data-ttu-id="9fccc-127">Tópico</span><span class="sxs-lookup"><span data-stu-id="9fccc-127">Topic</span></span>                                                           | <span data-ttu-id="9fccc-128">Descrição</span><span class="sxs-lookup"><span data-stu-id="9fccc-128">Description</span></span>                                                                                                                                                                                                                  |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9fccc-129">Sobre criptografia</span><span class="sxs-lookup"><span data-stu-id="9fccc-129">About Cryptography</span></span>](about-cryptography.md)<br/>         | <span data-ttu-id="9fccc-130">Conceitos de criptografia de chave e uma exibição de alto nível das tecnologias de criptografia da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="9fccc-130">Key cryptography concepts and a high-level view of Microsoft cryptography technologies.</span></span><br/>                                                                                                                           |
| [<span data-ttu-id="9fccc-131">Usando criptografia</span><span class="sxs-lookup"><span data-stu-id="9fccc-131">Using Cryptography</span></span>](using-cryptography.md)<br/>         | <span data-ttu-id="9fccc-132">Processos de criptografia, procedimentos e amostras estendidas de programas C e Visual Basic usando funções CryptoAPI e objetos CAPICOM.</span><span class="sxs-lookup"><span data-stu-id="9fccc-132">Cryptography processes, procedures, and extended samples of C and Visual Basic programs using CryptoAPI functions and CAPICOM objects.</span></span><br/>                                                                            |
| [<span data-ttu-id="9fccc-133">Referência de criptografia</span><span class="sxs-lookup"><span data-stu-id="9fccc-133">Cryptography Reference</span></span>](cryptography-reference.md)<br/> | <span data-ttu-id="9fccc-134">Descrições detalhadas das funções de criptografia, interfaces, objetos, estruturas e outros elementos de programação da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="9fccc-134">Detailed descriptions of the Microsoft cryptography functions, interfaces, objects, structures, and other programming elements.</span></span> <span data-ttu-id="9fccc-135">Inclui descrições de referência da API para trabalhar com certificados digitais.</span><span class="sxs-lookup"><span data-stu-id="9fccc-135">Includes reference descriptions of the API for working with digital certificates.</span></span><br/> |



 

 

 




