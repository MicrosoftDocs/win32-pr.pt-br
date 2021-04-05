---
description: Explica como usar SignTool para assinar um arquivo.
ms.assetid: fa8ee4d3-8927-4f7d-a09e-dbcf75a164d3
title: Usando SignTool para assinar um arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 089026cde629278e5c6ac033164c2a9d26528917
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090914"
---
# <a name="using-signtool-to-sign-a-file"></a><span data-ttu-id="c5e6c-103">Usando SignTool para assinar um arquivo</span><span class="sxs-lookup"><span data-stu-id="c5e6c-103">Using SignTool to Sign a File</span></span>

<span data-ttu-id="c5e6c-104">O comando a seguir assina o arquivo chamado MyControl.exe usando um [*certificado*](../secgloss/c-gly.md) armazenado em um arquivo de troca de informações pessoais (pfx):</span><span class="sxs-lookup"><span data-stu-id="c5e6c-104">The following command signs the file named MyControl.exe using a [*certificate*](../secgloss/c-gly.md) stored in a Personal Information Exchange (PFX) file:</span></span>

<pre>SignTool sign /f <b>MyCert</b>.pfx MyControl.exe</pre>

<span data-ttu-id="c5e6c-105">O comando a seguir assina o arquivo usando um certificado armazenado em um arquivo PFX protegido por senha:</span><span class="sxs-lookup"><span data-stu-id="c5e6c-105">The following command signs the file using a certificate stored in a password-protected PFX file:</span></span>

<pre>SignTool sign /f <b>MyCert</b>.pfx /p <b>MyPassword</b> MyControl.exe</pre>

> [!Note]  
> <span data-ttu-id="c5e6c-106">Certifique-se de proteger a senha corretamente.</span><span class="sxs-lookup"><span data-stu-id="c5e6c-106">Ensure that you properly protect the password.</span></span>

 

<span data-ttu-id="c5e6c-107">Os seguintes sinais de comando e carimbo de data/hora do arquivo:</span><span class="sxs-lookup"><span data-stu-id="c5e6c-107">The following command signs and time stamps the file:</span></span>

<pre>SignTool sign /f <b>MyCert</b>.pfx /t http://timestamp.digicert.com MyControl.exe</pre>

> [!Note]  
> <span data-ttu-id="c5e6c-108">Para obter informações sobre o carimbo de data/hora de um arquivo após ele já ter sido assinado, consulte [adicionando carimbos de data/hora aos arquivos assinados anteriormente](adding-time-stamps-to-previously-signed-files.md).</span><span class="sxs-lookup"><span data-stu-id="c5e6c-108">For information about time stamping a file after it has already been signed, see [Adding Time Stamps to Previously Signed Files](adding-time-stamps-to-previously-signed-files.md).</span></span>

 

<span data-ttu-id="c5e6c-109">O comando a seguir assina o arquivo usando um certificado localizado no meu repositório com um nome de assunto do meu fornecedor da empresa:</span><span class="sxs-lookup"><span data-stu-id="c5e6c-109">The following command signs the file using a certificate located in the My store with a subject name of My Company Publisher:</span></span>

<pre>SignTool sign /n "<b>My Company Publisher</b>" MyControl.exe</pre>

<span data-ttu-id="c5e6c-110">O comando a seguir assina um controle ActiveX e fornece informações que são exibidas pelo Internet Explorer quando o usuário é solicitado a instalar o controle:</span><span class="sxs-lookup"><span data-stu-id="c5e6c-110">The following command signs an ActiveX control and provides information that is displayed by Internet Explorer when the user is prompted to install the control:</span></span>

<pre>SignTool sign /f <b>MyCert</b>.pfx /d "<b>My Product Name</b>" /du <b>"https://www.example.com/myproductinfo.html"</b> MyControl.exe</pre>

<span data-ttu-id="c5e6c-111">O comando a seguir assina o arquivo usando um certificado cujas informações de [*chave privada*](../secgloss/p-gly.md) são protegidas por um módulo de criptografia de hardware.</span><span class="sxs-lookup"><span data-stu-id="c5e6c-111">The following command signs the file using a certificate whose [*private key*](../secgloss/p-gly.md) information is protected by a hardware cryptography module.</span></span> <span data-ttu-id="c5e6c-112">Por exemplo, suponha que o certificado chamado "meu certificado de High-Value" tenha uma chave privada instalada em um módulo de criptografia de hardware e o certificado seja instalado corretamente.</span><span class="sxs-lookup"><span data-stu-id="c5e6c-112">For example purposes, assume that the certificate called "My High-Value Certificate," has a private key installed in a hardware cryptography module, and the certificate is properly installed.</span></span>

<pre>SignTool sign /n "<b>My High-Value Certificate</b>" MyControl.exe</pre>

<span data-ttu-id="c5e6c-113">O comando a seguir assina o arquivo usando um certificado cujas informações de [*chave privada*](../secgloss/p-gly.md) são protegidas por um módulo de criptografia de hardware.</span><span class="sxs-lookup"><span data-stu-id="c5e6c-113">The following command signs the file using a certificate whose [*private key*](../secgloss/p-gly.md) information is protected by a hardware cryptography module.</span></span> <span data-ttu-id="c5e6c-114">Um repositório de computador é especificado para o repositório da AC ( [*autoridade de certificação*](../secgloss/c-gly.md) ).</span><span class="sxs-lookup"><span data-stu-id="c5e6c-114">A computer store is specified for the [*certification authority*](../secgloss/c-gly.md) (CA) store.</span></span>

<pre>SignTool sign /n "<b>My High Value Certificate</b>" /sm /s CA MyControl.exe</pre>

<span data-ttu-id="c5e6c-115">O comando a seguir assina o arquivo usando um certificado armazenado em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="c5e6c-115">The following command signs the file using a certificate stored in a file.</span></span> <span data-ttu-id="c5e6c-116">As informações de chave privada são protegidas por um módulo de criptografia de hardware e o CSP ( [*provedor de serviços de criptografia*](../secgloss/c-gly.md) ) e o contêiner de [*chave*](../secgloss/k-gly.md) são especificados pelo nome.</span><span class="sxs-lookup"><span data-stu-id="c5e6c-116">The private key information is protected by a hardware cryptography module, and the [*cryptographic service provider*](../secgloss/c-gly.md) (CSP)and [*key container*](../secgloss/k-gly.md) are specified by name.</span></span> <span data-ttu-id="c5e6c-117">Esse comando será útil se o certificado não estiver instalado corretamente.</span><span class="sxs-lookup"><span data-stu-id="c5e6c-117">This command is useful if the certificate is not properly installed.</span></span>

<pre>SignTool sign /f <b>HighValue</b>.cer /csp "<b>Hardware Cryptography Module</b>" /k <b>HighValueContainer</b> MyControl.exe</pre>

<span data-ttu-id="c5e6c-118">[SignTool](signtool.md) retorna um texto de linha de comando que declara o resultado da operação de assinatura.</span><span class="sxs-lookup"><span data-stu-id="c5e6c-118">[SignTool](signtool.md) returns command line text that states the result of the signing operation.</span></span> <span data-ttu-id="c5e6c-119">Além disso, SignTool retorna um código de saída zero para execução bem-sucedida, uma para execução com falha e duas para execução concluída com avisos.</span><span class="sxs-lookup"><span data-stu-id="c5e6c-119">Additionally, SignTool returns an exit code of zero for successful execution, one for failed execution, and two for execution that completed with warnings.</span></span>

<span data-ttu-id="c5e6c-120">Para obter informações sobre como verificar a assinatura de um arquivo, consulte [usando Signtool para verificar uma assinatura de arquivo](using-signtool-to-verify-a-file-signature.md).</span><span class="sxs-lookup"><span data-stu-id="c5e6c-120">For information about verifying a file's signature, see [Using SignTool to Verify a File Signature](using-signtool-to-verify-a-file-signature.md).</span></span> <span data-ttu-id="c5e6c-121">Para obter informações sobre como adicionar um carimbo de data/hora se o arquivo já tiver sido assinado, consulte [adicionando carimbos de data/hora aos arquivos assinados anteriormente](adding-time-stamps-to-previously-signed-files.md).</span><span class="sxs-lookup"><span data-stu-id="c5e6c-121">For information about adding a time stamp if the file has already been signed, see [Adding Time Stamps to Previously Signed Files](adding-time-stamps-to-previously-signed-files.md).</span></span> <span data-ttu-id="c5e6c-122">Para obter informações adicionais sobre [SignTool](signtool.md), consulte [SignTool](signtool.md).</span><span class="sxs-lookup"><span data-stu-id="c5e6c-122">For additional information about [SignTool](signtool.md), see [SignTool](signtool.md).</span></span>

 

 
