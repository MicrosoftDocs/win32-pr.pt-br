---
description: Página de Glossário
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 08951f9f-d03d-4720-8f18-1413ba72e93d
title: Glossário (WinHTTP)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f74d707c828a9eeb5f07ebf3ec3c1ca92a9d2b58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828944"
---
# <a name="glossary-winhttp"></a><span data-ttu-id="f1c55-103">Glossário (WinHTTP)</span><span class="sxs-lookup"><span data-stu-id="f1c55-103">Glossary (WinHTTP)</span></span>

<dl> <dt>

<span data-ttu-id="f1c55-104"><span id="term_authentication_data"></span><span id="TERM_AUTHENTICATION_DATA"></span>**dados de autenticação**</span><span class="sxs-lookup"><span data-stu-id="f1c55-104"><span id="term_authentication_data"></span><span id="TERM_AUTHENTICATION_DATA"></span>**authentication data**</span></span>
</dt> <dd>

<span data-ttu-id="f1c55-105">Bloco de dados específico do esquema que é trocado entre o servidor e o cliente durante a autenticação.</span><span class="sxs-lookup"><span data-stu-id="f1c55-105">Scheme-specific block of data that is exchanged between the server and client during authentication.</span></span> <span data-ttu-id="f1c55-106">Para provar sua identidade, o cliente criptografa alguns ou todos esses dados com um nome de usuário e senha.</span><span class="sxs-lookup"><span data-stu-id="f1c55-106">To prove its identity, the client encrypts some or all of this data with a user name and password.</span></span> <span data-ttu-id="f1c55-107">O cliente envia os dados criptografados para o servidor, o que descriptografa os dados e os compara com o original.</span><span class="sxs-lookup"><span data-stu-id="f1c55-107">The client sends the encrypted data to the server, which decrypts the data and compares it to the original.</span></span> <span data-ttu-id="f1c55-108">Se os dados descriptografados corresponderem aos dados originais, o cliente será autenticado.</span><span class="sxs-lookup"><span data-stu-id="f1c55-108">If the decrypted data matches the original data, the client is authenticated.</span></span>

</dd> <dt>

<span data-ttu-id="f1c55-109"><span id="term_base64_encoding"></span><span id="TERM_BASE64_ENCODING"></span>**codificação Base64**</span><span class="sxs-lookup"><span data-stu-id="f1c55-109"><span id="term_base64_encoding"></span><span id="TERM_BASE64_ENCODING"></span>**base64 encoding**</span></span>
</dt> <dd>

<span data-ttu-id="f1c55-110">Esquema usado para transmitir dados binários.</span><span class="sxs-lookup"><span data-stu-id="f1c55-110">Scheme used to transmit binary data.</span></span> <span data-ttu-id="f1c55-111">A base64 processa dados como grupos de 24 bits, mapeando esses dados para quatro caracteres codificados.</span><span class="sxs-lookup"><span data-stu-id="f1c55-111">Base64 processes data as 24-bit groups, mapping this data to four encoded characters.</span></span> <span data-ttu-id="f1c55-112">Às vezes, ele é chamado de codificação de 3 a 4.</span><span class="sxs-lookup"><span data-stu-id="f1c55-112">It is sometimes referred to as 3-to-4 encoding.</span></span> <span data-ttu-id="f1c55-113">Cada 6 bits do grupo de 24 bits é usado como um índice em uma tabela de mapeamento (o alfabeto Base64) para obter um caractere para os dados codificados.</span><span class="sxs-lookup"><span data-stu-id="f1c55-113">Each 6 bits of the 24-bit group is used as an index into a mapping table (the base64 alphabet) to obtain a character for the encoded data.</span></span> <span data-ttu-id="f1c55-114">Os dados codificados têm comprimentos de linha limitados a 76 caracteres.</span><span class="sxs-lookup"><span data-stu-id="f1c55-114">The encoded data has line lengths limited to 76 characters.</span></span>

</dd> <dt>

<span data-ttu-id="f1c55-115"><span id="term_certificate_store"></span><span id="TERM_CERTIFICATE_STORE"></span>**repositório de certificados**</span><span class="sxs-lookup"><span data-stu-id="f1c55-115"><span id="term_certificate_store"></span><span id="TERM_CERTIFICATE_STORE"></span>**certificate store**</span></span>
</dt> <dd>

<span data-ttu-id="f1c55-116">Normalmente, o armazenamento permanente em que certificados, CRL (listas de certificados revogados) e listas de certificados confiáveis (CTL) são armazenados.</span><span class="sxs-lookup"><span data-stu-id="f1c55-116">Typically, permanent storage where certificates, certificate revocation lists (CRL), and certificate trust lists (CTL) are stored.</span></span> <span data-ttu-id="f1c55-117">Um repositório de certificados também pode ser temporário ao trabalhar com certificados baseados em sessão.</span><span class="sxs-lookup"><span data-stu-id="f1c55-117">A certificate store can also be temporary when working with session-based certificates.</span></span>

</dd> <dt>

<span data-ttu-id="f1c55-118"><span id="term_cobranding"></span><span id="TERM_COBRANDING"></span>**co-branding**</span><span class="sxs-lookup"><span data-stu-id="f1c55-118"><span id="term_cobranding"></span><span id="TERM_COBRANDING"></span>**cobranding**</span></span>
</dt> <dd>

<span data-ttu-id="f1c55-119">Capacidade de um site Microsoft Passport participante fornecer seus próprios elementos de identidade visual e explicações sobre as páginas de serviço de rede do Passport.</span><span class="sxs-lookup"><span data-stu-id="f1c55-119">Ability for a Microsoft Passport participant site to provide its own branding elements and explanations on the Passport network service pages.</span></span> <span data-ttu-id="f1c55-120">A comarcação inclui personalizar a aparência, o texto específico e o comportamento específico nas páginas da rede do Passport.</span><span class="sxs-lookup"><span data-stu-id="f1c55-120">Cobranding includes customizing the look and feel, specific text, and specific behavior on Passport network pages.</span></span>

</dd> <dt>

<span data-ttu-id="f1c55-121"><span id="term_code_page"></span><span id="TERM_CODE_PAGE"></span>**página de código**</span><span class="sxs-lookup"><span data-stu-id="f1c55-121"><span id="term_code_page"></span><span id="TERM_CODE_PAGE"></span>**code page**</span></span>
</dt> <dd>

<span data-ttu-id="f1c55-122">Tabela que relaciona os códigos de caracteres binários usados por um programa a chaves no teclado ou à aparência de caracteres no monitor.</span><span class="sxs-lookup"><span data-stu-id="f1c55-122">Table that relates the binary character codes used by a program to keys on the keyboard or to the appearance of characters on the monitor.</span></span> <span data-ttu-id="f1c55-123">O uso de páginas de código é uma maneira de fornecer suporte a conjuntos de caracteres e layouts de teclado usados em diferentes países e regiões.</span><span class="sxs-lookup"><span data-stu-id="f1c55-123">Using code pages is a way to provide support for character sets and keyboard layouts used in different countries and regions.</span></span> <span data-ttu-id="f1c55-124">Você pode configurar dispositivos como o monitor e o teclado para usar uma página de código específica e alternar de uma página de código (como Estados Unidos) para outra (como, por exemplo, Portugal) na solicitação do usuário.</span><span class="sxs-lookup"><span data-stu-id="f1c55-124">You can configure devices such as the monitor and the keyboard to use a specific code page and to switch from one code page (such as United States) to another (such as Portugal) at the user's request.</span></span>

</dd> <dt>

<span data-ttu-id="f1c55-125"><span id="term_http_verb"></span><span id="TERM_HTTP_VERB"></span>**Verbo HTTP**</span><span class="sxs-lookup"><span data-stu-id="f1c55-125"><span id="term_http_verb"></span><span id="TERM_HTTP_VERB"></span>**HTTP verb**</span></span>
</dt> <dd>

<span data-ttu-id="f1c55-126">O verbo HTTP (ou o método HTTP) é uma instrução enviada em uma mensagem de solicitação que notifica um servidor HTTP sobre a ação a ser executada no recurso especificado.</span><span class="sxs-lookup"><span data-stu-id="f1c55-126">The HTTP verb (or HTTP method) is an instruction sent in a request message that notifies an HTTP server of the action to perform on the specified resource.</span></span> <span data-ttu-id="f1c55-127">Por exemplo, "GET" especifica que um recurso está sendo recuperado do servidor.</span><span class="sxs-lookup"><span data-stu-id="f1c55-127">For example, "GET" specifies that a resource is being retrieved from the server.</span></span> <span data-ttu-id="f1c55-128">Os verbos comuns incluem "GET", "POST" e "HEAD".</span><span class="sxs-lookup"><span data-stu-id="f1c55-128">Common verbs include "GET", "POST", and "HEAD".</span></span> <span data-ttu-id="f1c55-129">Para obter mais informações e uma lista completa de verbos HTTP padrão, consulte a especificação HTTP/1.1.</span><span class="sxs-lookup"><span data-stu-id="f1c55-129">For more information and a complete list of standard HTTP verbs, see the HTTP/1.1 specification.</span></span>

</dd> <dt>

<span data-ttu-id="f1c55-130"><span id="term_ticket"></span><span id="TERM_TICKET"></span>**concessão**</span><span class="sxs-lookup"><span data-stu-id="f1c55-130"><span id="term_ticket"></span><span id="TERM_TICKET"></span>**ticket**</span></span>
</dt> <dd>

<span data-ttu-id="f1c55-131">Cookie que contém um perfil de usuário para autenticação do Passport.</span><span class="sxs-lookup"><span data-stu-id="f1c55-131">Cookie that contains a user profile for Passport authentication.</span></span> <span data-ttu-id="f1c55-132">Cada tíquete corresponde a uma URL.</span><span class="sxs-lookup"><span data-stu-id="f1c55-132">Each ticket corresponds to one URL.</span></span> <span data-ttu-id="f1c55-133">O servidor de logon de uma autoridade de domínio do Passport fornece tíquetes que o cliente envia a um membro do Passport para autenticação.</span><span class="sxs-lookup"><span data-stu-id="f1c55-133">The logon server of a Passport Domain Authority provides tickets that the client sends to a Passport member for authentication.</span></span>

</dd> <dt>

<span data-ttu-id="f1c55-134"><span id="term_user_agent"></span><span id="TERM_USER_AGENT"></span>**agente do usuário**</span><span class="sxs-lookup"><span data-stu-id="f1c55-134"><span id="term_user_agent"></span><span id="TERM_USER_AGENT"></span>**user agent**</span></span>
</dt> <dd>

<span data-ttu-id="f1c55-135">O agente do usuário é o aplicativo cliente que solicita um documento de um servidor HTTP.</span><span class="sxs-lookup"><span data-stu-id="f1c55-135">The user agent is the client application that requests a document from an HTTP server.</span></span> <span data-ttu-id="f1c55-136">Quando o cliente envia uma solicitação para um servidor HTTP, normalmente ele envia o nome do agente do usuário com o cabeçalho da solicitação para que o servidor possa determinar os recursos do software cliente.</span><span class="sxs-lookup"><span data-stu-id="f1c55-136">When the client sends a request to an HTTP server, typically it sends the name of the user agent with the request header so that the server can determine the capabilities of the client software.</span></span>

</dd> </dl>

 

 



