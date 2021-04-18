---
description: Cria um certificado X. 509, assinado pela chave raiz de teste ou outra chave especificada, que associa seu nome à parte pública do par de chaves. O certificado é salvo em um arquivo, um repositório de certificados do sistema ou ambos.
ms.assetid: a28e77dd-72c9-42a3-a72d-1b3eaf59d9cf
title: MakeCert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 980ba379688f2dc61c44b06d66ed5255e5b2e988
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105811054"
---
# <a name="makecert"></a><span data-ttu-id="caabd-104">MakeCert</span><span class="sxs-lookup"><span data-stu-id="caabd-104">MakeCert</span></span>

> [!Note]  
> <span data-ttu-id="caabd-105">O MakeCert foi preterido.</span><span class="sxs-lookup"><span data-stu-id="caabd-105">MakeCert is deprecated.</span></span> <span data-ttu-id="caabd-106">Para criar certificados autoassinados, use o cmdlet do PowerShell [New-SelfSignedCertificate](/powershell/module/pkiclient/new-selfsignedcertificate).</span><span class="sxs-lookup"><span data-stu-id="caabd-106">To create self-signed certificates, use the Powershell Cmdlet [New-SelfSignedCertificate](/powershell/module/pkiclient/new-selfsignedcertificate).</span></span>

 

<span data-ttu-id="caabd-107">A ferramenta MakeCert cria um certificado [*X. 509*](../secgloss/x-gly.md) , assinado pela chave raiz de teste ou outra chave especificada, que associa seu nome à parte pública do par de chaves.</span><span class="sxs-lookup"><span data-stu-id="caabd-107">The MakeCert tool creates an [*X.509*](../secgloss/x-gly.md) certificate, signed by the test root key or other specified key, that binds your name to the public part of the key pair.</span></span> <span data-ttu-id="caabd-108">O certificado é salvo em um arquivo, um repositório de certificados do sistema ou ambos.</span><span class="sxs-lookup"><span data-stu-id="caabd-108">The certificate is saved to a file, a system certificate store, or both.</span></span> <span data-ttu-id="caabd-109">A ferramenta é instalada na \\ pasta bin do caminho de instalação do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="caabd-109">The tool is installed in the \\Bin folder of the Microsoft Windows Software Development Kit (SDK) installation path.</span></span>

<span data-ttu-id="caabd-110">A ferramenta MakeCert usa a seguinte sintaxe de comando:</span><span class="sxs-lookup"><span data-stu-id="caabd-110">The MakeCert tool uses the following command syntax:</span></span>

<span data-ttu-id="caabd-111">**MakeCert** \[ *Basicoptions* \| *Extended* \] *Arquivo_de_saída*</span><span class="sxs-lookup"><span data-stu-id="caabd-111">**MakeCert** \[*BasicOptions*\|*ExtendedOptions*\] *OutputFile*</span></span>

<span data-ttu-id="caabd-112">*Arquivo_de_saída* é o nome do arquivo no qual o certificado será gravado.</span><span class="sxs-lookup"><span data-stu-id="caabd-112">*OutputFile* is the name of the file where the certificate will be written.</span></span> <span data-ttu-id="caabd-113">Você pode omitir o *arquivo_de_saída* se o certificado não for gravado em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="caabd-113">You can omit *OutputFile* if the certificate is not to be written to a file.</span></span>

## <a name="options"></a><span data-ttu-id="caabd-114">Opções</span><span class="sxs-lookup"><span data-stu-id="caabd-114">Options</span></span>

<span data-ttu-id="caabd-115">O MakeCert inclui opções básicas e estendidas.</span><span class="sxs-lookup"><span data-stu-id="caabd-115">MakeCert includes basic and extended options.</span></span> <span data-ttu-id="caabd-116">As opções básicas são as mais comuns para criar um certificado.</span><span class="sxs-lookup"><span data-stu-id="caabd-116">Basic options are those most commonly used to create a certificate.</span></span> <span data-ttu-id="caabd-117">As opções estendidas dão mais flexibilidade.</span><span class="sxs-lookup"><span data-stu-id="caabd-117">Extended options provide more flexibility.</span></span>

<span data-ttu-id="caabd-118">As opções para MakeCert também são divididas em três grupos funcionais:</span><span class="sxs-lookup"><span data-stu-id="caabd-118">The options for MakeCert are also divided into three functional groups:</span></span>

-   <span data-ttu-id="caabd-119">Opções básicas específicas somente para a tecnologia de repositório de certificados.</span><span class="sxs-lookup"><span data-stu-id="caabd-119">Basic options specific to certificate store technology only.</span></span>
-   <span data-ttu-id="caabd-120">Opções estendidas específicas somente para o SPC-File e a tecnologia de chave privada.</span><span class="sxs-lookup"><span data-stu-id="caabd-120">Extended options specific to SPC-file and private key technology only.</span></span>
-   <span data-ttu-id="caabd-121">Opções estendidas aplicáveis à tecnologia de arquivo SPC, chave privada e repositório de certificados.</span><span class="sxs-lookup"><span data-stu-id="caabd-121">Extended options applicable to SPC-file, private key, and certificate store technology.</span></span>

<span data-ttu-id="caabd-122">As opções fornecidas nas tabelas a seguir podem ser usadas somente com o Internet Explorer 4,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="caabd-122">Options given in the following tables can be used only with Internet Explorer 4.0 or later.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="caabd-123">Opção básica</span><span class="sxs-lookup"><span data-stu-id="caabd-123">Basic option</span></span></th>
<th><span data-ttu-id="caabd-124">Description</span><span class="sxs-lookup"><span data-stu-id="caabd-124">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="caabd-125"><strong>-a</strong> <strong></strong> <em>Algoritmo</em> do</span><span class="sxs-lookup"><span data-stu-id="caabd-125"><strong>-a</strong> <strong></strong> <em>Algorithm</em></span></span></td>
<td><span data-ttu-id="caabd-126">Algoritmo de <a href="/windows/desktop/SecGloss/h-gly"><em>hash</em></a> .</span><span class="sxs-lookup"><span data-stu-id="caabd-126"><a href="/windows/desktop/SecGloss/h-gly"><em>Hash</em></a> algorithm.</span></span> <span data-ttu-id="caabd-127">Deve ser definido como <strong>SHA-1</strong> ou <strong>MD5</strong> (padrão).</span><span class="sxs-lookup"><span data-stu-id="caabd-127">Must be set to either <strong>SHA-1</strong> or <strong>MD5</strong> (default).</span></span> <span data-ttu-id="caabd-128">Para obter informações sobre MD5, consulte <a href="/windows/desktop/SecGloss/m-gly"><em>MD5</em></a>.</span><span class="sxs-lookup"><span data-stu-id="caabd-128">For information about MD5, see <a href="/windows/desktop/SecGloss/m-gly"><em>MD5</em></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="caabd-129"><strong>-b</strong> <strong></strong> <em>DateStart</em></span><span class="sxs-lookup"><span data-stu-id="caabd-129"><strong>-b</strong> <strong></strong> <em>DateStart</em></span></span></td>
<td><span data-ttu-id="caabd-130">Data em que o certificado se torna válido pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="caabd-130">Date the certificate first becomes valid.</span></span> <span data-ttu-id="caabd-131">O padrão é quando o certificado é criado.</span><span class="sxs-lookup"><span data-stu-id="caabd-131">The default is when the certificate is created.</span></span> <span data-ttu-id="caabd-132">O formato de <em>DateStart</em> é mm/dd/aaaa.</span><span class="sxs-lookup"><span data-stu-id="caabd-132">The format of <em>DateStart</em> is mm/dd/yyyy.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="caabd-133"><strong>-CY</strong> <strong></strong> <em>CertificateTypes</em></span><span class="sxs-lookup"><span data-stu-id="caabd-133"><strong>-cy</strong> <strong></strong> <em>CertificateTypes</em></span></span></td>
<td><span data-ttu-id="caabd-134">Tipo de certificado.</span><span class="sxs-lookup"><span data-stu-id="caabd-134">Certificate type.</span></span> <span data-ttu-id="caabd-135"><em>CertificateTypes</em> pode ser <strong>end</strong> para a entidade end ou <strong>autoridade</strong> para <a href="/windows/desktop/SecGloss/c-gly"><em>autoridade de certificação</em></a>.</span><span class="sxs-lookup"><span data-stu-id="caabd-135"><em>CertificateTypes</em> can be <strong>end</strong> for end-entity, or <strong>authority</strong> for <a href="/windows/desktop/SecGloss/c-gly"><em>certification authority</em></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="caabd-136"><strong>-e</strong> <strong></strong> <em>DateEnd</em></span><span class="sxs-lookup"><span data-stu-id="caabd-136"><strong>-e</strong> <strong></strong> <em>DateEnd</em></span></span></td>
<td><span data-ttu-id="caabd-137">Data em que o período de validade termina.</span><span class="sxs-lookup"><span data-stu-id="caabd-137">Date when the validity period ends.</span></span> <span data-ttu-id="caabd-138">O padrão é o ano 2039.</span><span class="sxs-lookup"><span data-stu-id="caabd-138">The default is the year 2039.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="caabd-139"><strong>-EKU</strong> <strong></strong> <em>OID1</em><strong>,</strong> <em>OID2</em> ...</span><span class="sxs-lookup"><span data-stu-id="caabd-139"><strong>-eku</strong> <strong></strong> <em>OID1</em><strong>,</strong> <em>OID2</em> …</span></span></td>
<td><span data-ttu-id="caabd-140">Insere uma lista de um ou mais OIDs ( <a href="/windows/desktop/SecGloss/o-gly"><em>identificadores de objeto</em></a> ) de <a href="/windows/desktop/SecGloss/e-gly"><em>uso avançado de chave</em></a> separados por vírgula no certificado.</span><span class="sxs-lookup"><span data-stu-id="caabd-140">Inserts a list of one or more comma-separated, <a href="/windows/desktop/SecGloss/e-gly"><em>enhanced key usage</em></a> <a href="/windows/desktop/SecGloss/o-gly"><em>object identifiers</em></a> (OIDs) into the certificate.</span></span> <span data-ttu-id="caabd-141">Por exemplo, <strong>-EKU 1.3.6.1.5.5.7.3.2</strong> insere o OID de autenticação de cliente.</span><span class="sxs-lookup"><span data-stu-id="caabd-141">For example, <strong>-eku 1.3.6.1.5.5.7.3.2</strong> inserts the client authentication OID.</span></span> <span data-ttu-id="caabd-142">Para obter definições de OIDs permitidos, consulte o arquivo Wincrypt. h em CryptoAPI 2.0.</span><span class="sxs-lookup"><span data-stu-id="caabd-142">For definitions of allowable OIDs, see the Wincrypt.h file in CryptoAPI 2.0.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="caabd-143"><strong>-h</strong> <strong></strong> <em>NumChildren</em></span><span class="sxs-lookup"><span data-stu-id="caabd-143"><strong>-h</strong> <strong></strong> <em>NumChildren</em></span></span></td>
<td><span data-ttu-id="caabd-144">Altura máxima da árvore abaixo deste certificado.</span><span class="sxs-lookup"><span data-stu-id="caabd-144">Maximum height of the tree below this certificate.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="caabd-145"><strong>-l</strong> <strong></strong> <em>PolicyLink</em></span><span class="sxs-lookup"><span data-stu-id="caabd-145"><strong>-l</strong> <strong></strong> <em>PolicyLink</em></span></span></td>
<td><span data-ttu-id="caabd-146">Link para informações de política do SPC Agency (por exemplo, uma URL).</span><span class="sxs-lookup"><span data-stu-id="caabd-146">Link to SPC agency policy information (for example, a URL).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="caabd-147"><strong>-m</strong> <strong></strong> <em>nMonths</em></span><span class="sxs-lookup"><span data-stu-id="caabd-147"><strong>-m</strong> <strong></strong> <em>nMonths</em></span></span></td>
<td><span data-ttu-id="caabd-148">Duração do período de validade.</span><span class="sxs-lookup"><span data-stu-id="caabd-148">Duration of the validity period.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="caabd-149"><strong>-n</strong> <strong>&quot;</strong> <em>Nome</em> do<strong>&quot;</strong></span><span class="sxs-lookup"><span data-stu-id="caabd-149"><strong>-n</strong> <strong>&quot;</strong><em>Name</em><strong>&quot;</strong></span></span></td>
<td><span data-ttu-id="caabd-150">Nome do certificado do editor.</span><span class="sxs-lookup"><span data-stu-id="caabd-150">Name for the publisher's certificate.</span></span> <span data-ttu-id="caabd-151">Esse nome deve estar em conformidade com o padrão <a href="/windows/desktop/SecGloss/x-gly"><em>X. 500</em></a> .</span><span class="sxs-lookup"><span data-stu-id="caabd-151">This name must conform to the <a href="/windows/desktop/SecGloss/x-gly"><em>X.500</em></a> standard.</span></span> <span data-ttu-id="caabd-152">O método mais simples é usar o &quot; formato CN =<em>myname</em> &quot; .</span><span class="sxs-lookup"><span data-stu-id="caabd-152">The simplest method is to use the &quot;CN=<em>MyName</em>&quot; format.</span></span> <span data-ttu-id="caabd-153">Por exemplo: <strong>-n &quot; CN = test &quot; </strong>.</span><span class="sxs-lookup"><span data-stu-id="caabd-153">For example: <strong>-n &quot;CN=Test&quot;</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="caabd-154"><strong>-nscp</strong></span><span class="sxs-lookup"><span data-stu-id="caabd-154"><strong>-nscp</strong></span></span></td>
<td><span data-ttu-id="caabd-155">A extensão de autenticação de cliente do Netscape deve ser incluída.</span><span class="sxs-lookup"><span data-stu-id="caabd-155">The Netscape client authentication extension should be included.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="caabd-156"><strong>-PE</strong></span><span class="sxs-lookup"><span data-stu-id="caabd-156"><strong>-pe</strong></span></span></td>
<td><span data-ttu-id="caabd-157">Marca a chave privada como exportável.</span><span class="sxs-lookup"><span data-stu-id="caabd-157">Marks the private key as exportable.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="caabd-158"><strong>-r</strong></span><span class="sxs-lookup"><span data-stu-id="caabd-158"><strong>-r</strong></span></span></td>
<td><span data-ttu-id="caabd-159">Cria um certificado autoassinado.</span><span class="sxs-lookup"><span data-stu-id="caabd-159">Creates a self-signed certificate.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="caabd-160"><strong>-SC</strong> <strong></strong> <em>SubjectCertFile</em></span><span class="sxs-lookup"><span data-stu-id="caabd-160"><strong>-sc</strong> <strong></strong> <em>SubjectCertFile</em></span></span></td>
<td><span data-ttu-id="caabd-161">Nome do arquivo de certificado com a chave pública de entidade existente a ser usada.</span><span class="sxs-lookup"><span data-stu-id="caabd-161">Certificate file name with the existing subject public key to be used.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="caabd-162"><strong>-SK</strong> <strong></strong> <em>SubjectKey</em></span><span class="sxs-lookup"><span data-stu-id="caabd-162"><strong>-sk</strong> <strong></strong> <em>SubjectKey</em></span></span></td>
<td><span data-ttu-id="caabd-163">Local do contêiner de chave da entidade que contém a <a href="/windows/desktop/SecGloss/p-gly"><em>chave privada</em></a>.</span><span class="sxs-lookup"><span data-stu-id="caabd-163">Location of the subject's key container which holds the <a href="/windows/desktop/SecGloss/p-gly"><em>private key</em></a>.</span></span> <span data-ttu-id="caabd-164">Se um contêiner de chave não existir, um será criado.</span><span class="sxs-lookup"><span data-stu-id="caabd-164">If a key container does not exist, one is created.</span></span> <span data-ttu-id="caabd-165">Se nem a opção <strong>-SK</strong> ou <strong>-SV</strong> for usada, um contêiner de chave padrão será criado e usado por padrão.</span><span class="sxs-lookup"><span data-stu-id="caabd-165">If neither the <strong>-sk</strong> or <strong>-sv</strong> option is used, a default key container is created and used by default.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="caabd-166"><strong>-céu</strong> <strong></strong> <em>SubjectKeySpec</em></span><span class="sxs-lookup"><span data-stu-id="caabd-166"><strong>-sky</strong> <strong></strong> <em>SubjectKeySpec</em></span></span></td>
<td><span data-ttu-id="caabd-167">Especificação da chave da entidade.</span><span class="sxs-lookup"><span data-stu-id="caabd-167">Subject's key specification.</span></span> <span data-ttu-id="caabd-168"><em>SubjectKeySpec</em> deve ser um dos três valores possíveis:</span><span class="sxs-lookup"><span data-stu-id="caabd-168"><em>SubjectKeySpec</em> must be one of three possible values:</span></span><br/>
<ul>
<li><span data-ttu-id="caabd-169"><strong>Assinatura</strong> (AT_SIGNATURE especificação de chave)</span><span class="sxs-lookup"><span data-stu-id="caabd-169"><strong>Signature</strong> (AT_SIGNATURE key specification)</span></span></li>
<li><span data-ttu-id="caabd-170"><strong>Troca</strong> (AT_KEYEXCHANGE especificação de chave)</span><span class="sxs-lookup"><span data-stu-id="caabd-170"><strong>Exchange</strong> (AT_KEYEXCHANGE key specification)</span></span></li>
<li><span data-ttu-id="caabd-171">Um inteiro, como <strong>3</strong></span><span class="sxs-lookup"><span data-stu-id="caabd-171">An integer, such as <strong>3</strong></span></span></li>
</ul>
<span data-ttu-id="caabd-172">Para obter mais informações, consulte a observação que segue esta tabela.</span><span class="sxs-lookup"><span data-stu-id="caabd-172">For more information, see the Note that follows this table.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="caabd-173"><strong>-SP</strong> <strong></strong> <em>SubjectProviderName</em></span><span class="sxs-lookup"><span data-stu-id="caabd-173"><strong>-sp</strong> <strong></strong> <em>SubjectProviderName</em></span></span></td>
<td><span data-ttu-id="caabd-174">Provedor de CryptoAPI para o assunto.</span><span class="sxs-lookup"><span data-stu-id="caabd-174">CryptoAPI provider for subject.</span></span> <span data-ttu-id="caabd-175">O padrão é o provedor do usuário.</span><span class="sxs-lookup"><span data-stu-id="caabd-175">The default is the user's provider.</span></span> <span data-ttu-id="caabd-176">Para obter informações sobre provedores de CryptoAPI, consulte a documentação do CryptoAPI 2.0.</span><span class="sxs-lookup"><span data-stu-id="caabd-176">For information about CryptoAPI providers, see the CryptoAPI 2.0 documentation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="caabd-177"><strong>-Sr</strong> <strong></strong> <em>SubjectCertStoreLocation</em></span><span class="sxs-lookup"><span data-stu-id="caabd-177"><strong>-sr</strong> <strong></strong> <em>SubjectCertStoreLocation</em></span></span></td>
<td><span data-ttu-id="caabd-178">Local do registro do repositório de certificados da entidade.</span><span class="sxs-lookup"><span data-stu-id="caabd-178">Registry location of the subject's certificate store.</span></span> <span data-ttu-id="caabd-179"><em>SubjectCertStoreLocation</em> deve ser <strong>LocalMachine</strong> (chave do registro HKEY_LOCAL_MACHINE) ou <strong>CurrentUser</strong> (chave do registro HKEY_CURRENT_USER).</span><span class="sxs-lookup"><span data-stu-id="caabd-179"><em>SubjectCertStoreLocation</em> must be either <strong>LocalMachine</strong> (registry key HKEY_LOCAL_MACHINE) or <strong>CurrentUser</strong> (registry key HKEY_CURRENT_USER).</span></span> <span data-ttu-id="caabd-180"><strong>CurrentUser</strong> é o padrão.</span><span class="sxs-lookup"><span data-stu-id="caabd-180"><strong>CurrentUser</strong> is the default.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="caabd-181"><strong>-SS</strong> <strong></strong> <em>SubjectCertStoreName</em></span><span class="sxs-lookup"><span data-stu-id="caabd-181"><strong>-ss</strong> <strong></strong> <em>SubjectCertStoreName</em></span></span></td>
<td><span data-ttu-id="caabd-182">Nome do repositório de certificados da entidade em que o certificado gerado será armazenado.</span><span class="sxs-lookup"><span data-stu-id="caabd-182">Name of the subject's certificate store where the generated certificate will be stored.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="caabd-183"><strong>-VA</strong> <strong></strong> <em>SubjectKeyFile</em></span><span class="sxs-lookup"><span data-stu-id="caabd-183"><strong>-sv</strong> <strong></strong> <em>SubjectKeyFile</em></span></span></td>
<td><span data-ttu-id="caabd-184">Nome do arquivo. pvk da entidade.</span><span class="sxs-lookup"><span data-stu-id="caabd-184">Name of the subject's .pvk file.</span></span> <span data-ttu-id="caabd-185">Se nem a opção <strong>-SK</strong> ou <strong>-SV</strong> for usada, um contêiner de chave padrão será criado e usado por padrão.</span><span class="sxs-lookup"><span data-stu-id="caabd-185">If neither the <strong>-sk</strong> or <strong>-sv</strong> option is used, a default key container is created and used by default.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="caabd-186"><strong>-Sy</strong> <strong></strong> <em>nSubjectProviderType</em></span><span class="sxs-lookup"><span data-stu-id="caabd-186"><strong>-sy</strong> <strong></strong> <em>nSubjectProviderType</em></span></span></td>
<td><span data-ttu-id="caabd-187">Tipo de provedor de CryptoAPI para o assunto.</span><span class="sxs-lookup"><span data-stu-id="caabd-187">CryptoAPI provider type for subject.</span></span> <span data-ttu-id="caabd-188">O padrão é <a href="/windows/desktop/SecGloss/p-gly"><em>PROV_RSA_FULL</em></a>.</span><span class="sxs-lookup"><span data-stu-id="caabd-188">The default is <a href="/windows/desktop/SecGloss/p-gly"><em>PROV_RSA_FULL</em></a>.</span></span> <span data-ttu-id="caabd-189">Para obter informações sobre tipos de provedor de CryptoAPI, consulte a documentação do CryptoAPI 2.0.</span><span class="sxs-lookup"><span data-stu-id="caabd-189">For information about CryptoAPI provider types, see the CryptoAPI 2.0 documentation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="caabd-190"><strong>-#</strong><strong></strong> <em>SerialNumber</em></span><span class="sxs-lookup"><span data-stu-id="caabd-190"><strong>-#</strong> <strong></strong> <em>SerialNumber</em></span></span></td>
<td><span data-ttu-id="caabd-191">Número de série do certificado.</span><span class="sxs-lookup"><span data-stu-id="caabd-191">Serial number of the certificate.</span></span> <span data-ttu-id="caabd-192">O valor máximo é 2 ^ 31.</span><span class="sxs-lookup"><span data-stu-id="caabd-192">The maximum value is 2^31.</span></span> <span data-ttu-id="caabd-193">O padrão é um valor gerado pela ferramenta que tem a garantia de ser exclusivo.</span><span class="sxs-lookup"><span data-stu-id="caabd-193">The default is a value generated by the tool that is guaranteed to be unique.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="caabd-194"><strong>-$</strong><strong></strong> <em>CertificateAuthority</em></span><span class="sxs-lookup"><span data-stu-id="caabd-194"><strong>-$</strong> <strong></strong> <em>CertificateAuthority</em></span></span></td>
<td><span data-ttu-id="caabd-195">Tipo de <a href="/windows/desktop/SecGloss/c-gly"><em>autoridade de certificação</em></a>.</span><span class="sxs-lookup"><span data-stu-id="caabd-195">Type of <a href="/windows/desktop/SecGloss/c-gly"><em>certification authority</em></a>.</span></span> <span data-ttu-id="caabd-196">O <em>CertificateAuthority</em> deve ser definido como <strong>comercial</strong> (para certificados a serem usados por editores de software comercial) ou <strong>individual</strong> (para certificados a serem usados por editores de software individuais).</span><span class="sxs-lookup"><span data-stu-id="caabd-196"><em>CertificateAuthority</em> must be set to either <strong>commercial</strong> (for certificates to be used by commercial software publishers) or <strong>individual</strong> (for certificates to be used by individual software publishers).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="caabd-197"><strong>-?</strong></span><span class="sxs-lookup"><span data-stu-id="caabd-197"><strong>-?</strong></span></span></td>
<td><span data-ttu-id="caabd-198">Exibe as opções básicas.</span><span class="sxs-lookup"><span data-stu-id="caabd-198">Displays the basic options.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="caabd-199"><strong>-!</strong></span><span class="sxs-lookup"><span data-stu-id="caabd-199"><strong>-!</strong></span></span></td>
<td><span data-ttu-id="caabd-200">Exibe as opções estendidas.</span><span class="sxs-lookup"><span data-stu-id="caabd-200">Displays the extended options.</span></span></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> <span data-ttu-id="caabd-201">Se a opção de especificação de chave **-céu** for usada no Internet Explorer versão 4,0 ou posterior, a especificação deverá corresponder à especificação de chave indicada pelo arquivo de [*chave privada*](../secgloss/p-gly.md) ou pelo [*contêiner de chave*](../secgloss/k-gly.md)privada.</span><span class="sxs-lookup"><span data-stu-id="caabd-201">If the **-sky** key specification option is used in Internet Explorer version 4.0 or later, the specification must match the key specification indicated by the [*private key*](../secgloss/p-gly.md) file or private [*key container*](../secgloss/k-gly.md).</span></span> <span data-ttu-id="caabd-202">Se a opção de especificação de chave não for usada, a especificação de chave indicada pelo arquivo de chave privada ou pelo contêiner de chave privada será usada.</span><span class="sxs-lookup"><span data-stu-id="caabd-202">If the key specification option is not used, the key specification indicated by the private key file or private key container will be used.</span></span> <span data-ttu-id="caabd-203">Se houver mais de uma especificação de chave no contêiner de chave, o MakeCert tentará primeiro usar a \_ especificação de chave de assinatura at.</span><span class="sxs-lookup"><span data-stu-id="caabd-203">If there is more than one key specification in the key container, MakeCert will first attempt to use the AT\_SIGNATURE key specification.</span></span> <span data-ttu-id="caabd-204">Se isso falhar, o MakeCert tentará usar AT \_ Exchange.</span><span class="sxs-lookup"><span data-stu-id="caabd-204">If that fails, MakeCert will try to use AT\_KEYEXCHANGE.</span></span> <span data-ttu-id="caabd-205">Como a maioria dos usuários tem uma \_ chave de assinatura at ou uma \_ chave de troca de chaves, essa opção não precisa ser usada na maioria dos casos.</span><span class="sxs-lookup"><span data-stu-id="caabd-205">Because most users have either an AT\_SIGNATURE key or an AT\_KEYEXCHANGE key, this option does not need to be used in most cases.</span></span>

 

<span data-ttu-id="caabd-206">As opções a seguir são apenas para arquivos SPC ( [*certificado do fornecedor de software*](../secgloss/s-gly.md) ) e tecnologia de chave privada.</span><span class="sxs-lookup"><span data-stu-id="caabd-206">The following options are only for [*Software Publisher Certificate*](../secgloss/s-gly.md) (SPC) files and private key technology.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="caabd-207">Opção SPC e chave privada</span><span class="sxs-lookup"><span data-stu-id="caabd-207">SPC and private key option</span></span></th>
<th><span data-ttu-id="caabd-208">Description</span><span class="sxs-lookup"><span data-stu-id="caabd-208">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="caabd-209"><strong>-IC</strong> <strong></strong> <em>IssuerCertFile</em></span><span class="sxs-lookup"><span data-stu-id="caabd-209"><strong>-ic</strong> <strong></strong> <em>IssuerCertFile</em></span></span></td>
<td><span data-ttu-id="caabd-210">Local do certificado do emissor.</span><span class="sxs-lookup"><span data-stu-id="caabd-210">Location of the issuer's certificate.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="caabd-211"><strong>-IK</strong> <strong></strong> <em>IssuerKey</em></span><span class="sxs-lookup"><span data-stu-id="caabd-211"><strong>-ik</strong> <strong></strong> <em>IssuerKey</em></span></span></td>
<td><span data-ttu-id="caabd-212">Local do contêiner de chave do emissor.</span><span class="sxs-lookup"><span data-stu-id="caabd-212">Location of the issuer's key container.</span></span> <span data-ttu-id="caabd-213">O padrão é a chave raiz de teste.</span><span class="sxs-lookup"><span data-stu-id="caabd-213">The default is the test root key.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="caabd-214"><strong>-iKy</strong> <strong></strong> <em>IssuerKeySpec</em></span><span class="sxs-lookup"><span data-stu-id="caabd-214"><strong>-iky</strong> <strong></strong> <em>IssuerKeySpec</em></span></span></td>
<td><span data-ttu-id="caabd-215">A especificação de chave do emissor, que deve ser um dos três valores possíveis:</span><span class="sxs-lookup"><span data-stu-id="caabd-215">Issuer's key specification, which must be one of three possible values:</span></span><br/>
<ul>
<li><span data-ttu-id="caabd-216"><strong>Assinatura</strong> (AT_SIGNATURE especificação de chave)</span><span class="sxs-lookup"><span data-stu-id="caabd-216"><strong>Signature</strong> (AT_SIGNATURE key specification)</span></span></li>
<li><span data-ttu-id="caabd-217"><strong>Troca</strong> (AT_KEYEXCHANGE especificação de chave)</span><span class="sxs-lookup"><span data-stu-id="caabd-217"><strong>Exchange</strong> (AT_KEYEXCHANGE key specification)</span></span></li>
<li><span data-ttu-id="caabd-218">Um inteiro, como <strong>3</strong></span><span class="sxs-lookup"><span data-stu-id="caabd-218">An integer, such as <strong>3</strong></span></span></li>
</ul>
<span data-ttu-id="caabd-219">Para obter mais informações, consulte a observação que segue esta tabela.</span><span class="sxs-lookup"><span data-stu-id="caabd-219">For more information, see the Note that follows this table.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="caabd-220"><strong>-IP</strong> <strong></strong> <em>IssuerProviderName</em></span><span class="sxs-lookup"><span data-stu-id="caabd-220"><strong>-ip</strong> <strong></strong> <em>IssuerProviderName</em></span></span></td>
<td><span data-ttu-id="caabd-221">Provedor de CryptoAPI para emissor.</span><span class="sxs-lookup"><span data-stu-id="caabd-221">CryptoAPI provider for issuer.</span></span> <span data-ttu-id="caabd-222">O padrão é o provedor do usuário.</span><span class="sxs-lookup"><span data-stu-id="caabd-222">The default is the user's provider.</span></span> <span data-ttu-id="caabd-223">Para obter informações sobre provedores de CryptoAPI, consulte a documentação do CryptoAPI 2.0.</span><span class="sxs-lookup"><span data-stu-id="caabd-223">For information about CryptoAPI providers, see the CryptoAPI 2.0 documentation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="caabd-224"><strong>-IV</strong> <strong></strong> <em>IssuerKeyFile</em></span><span class="sxs-lookup"><span data-stu-id="caabd-224"><strong>-iv</strong> <strong></strong> <em>IssuerKeyFile</em></span></span></td>
<td><span data-ttu-id="caabd-225">Arquivo de chave privada do emissor.</span><span class="sxs-lookup"><span data-stu-id="caabd-225">Issuer's private key file.</span></span> <span data-ttu-id="caabd-226">O padrão é a raiz do teste.</span><span class="sxs-lookup"><span data-stu-id="caabd-226">The default is the test root.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="caabd-227"><strong>-iy</strong> <strong></strong> <em>nIssuerProviderType</em></span><span class="sxs-lookup"><span data-stu-id="caabd-227"><strong>-iy</strong> <strong></strong> <em>nIssuerProviderType</em></span></span></td>
<td><span data-ttu-id="caabd-228">Tipo de provedor de CryptoAPI para emissor.</span><span class="sxs-lookup"><span data-stu-id="caabd-228">CryptoAPI provider type for issuer.</span></span> <span data-ttu-id="caabd-229">O padrão é <a href="/windows/desktop/SecGloss/p-gly"><em>PROV_RSA_FULL</em></a>.</span><span class="sxs-lookup"><span data-stu-id="caabd-229">The default is <a href="/windows/desktop/SecGloss/p-gly"><em>PROV_RSA_FULL</em></a>.</span></span> <span data-ttu-id="caabd-230">Para obter informações sobre tipos de provedor de CryptoAPI, consulte a documentação do CryptoAPI 2.0.</span><span class="sxs-lookup"><span data-stu-id="caabd-230">For information about CryptoAPI provider types, see the CryptoAPI 2.0 documentation.</span></span></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> <span data-ttu-id="caabd-231">Se a opção de especificação de chave **-iKy** for usada no Internet Explorer 4,0 ou posterior, a especificação deverá corresponder à especificação de chave indicada pelo arquivo de [*chave privada*](../secgloss/p-gly.md) ou pelo [*contêiner de chave*](../secgloss/k-gly.md)privada.</span><span class="sxs-lookup"><span data-stu-id="caabd-231">If the **-iky** key specification option is used in Internet Explorer 4.0 or later, the specification must match the key specification indicated by the [*private key*](../secgloss/p-gly.md) file or private [*key container*](../secgloss/k-gly.md).</span></span> <span data-ttu-id="caabd-232">Se a opção de especificação de chave não for usada, a especificação de chave indicada pelo arquivo de chave privada ou pelo contêiner de chave privada será usada.</span><span class="sxs-lookup"><span data-stu-id="caabd-232">If the key specification option is not used, the key specification indicated by the private key file or private key container will be used.</span></span> <span data-ttu-id="caabd-233">Se houver mais de uma especificação de chave no contêiner de chave, o MakeCert tentará primeiro usar a \_ especificação de chave de assinatura at.</span><span class="sxs-lookup"><span data-stu-id="caabd-233">If there is more than one key specification in the key container, MakeCert will first attempt to use the AT\_SIGNATURE key specification.</span></span> <span data-ttu-id="caabd-234">Se isso falhar, o MakeCert tentará usar AT \_ Exchange.</span><span class="sxs-lookup"><span data-stu-id="caabd-234">If that fails, MakeCert will try to use AT\_KEYEXCHANGE.</span></span> <span data-ttu-id="caabd-235">Como a maioria dos usuários tem uma \_ chave de assinatura at ou uma \_ chave de troca de chaves, essa opção não precisa ser usada na maioria dos casos.</span><span class="sxs-lookup"><span data-stu-id="caabd-235">Because most users have either an AT\_SIGNATURE key or an AT\_KEYEXCHANGE key, this option does not need to be used in most cases.</span></span>

 

<span data-ttu-id="caabd-236">As opções a seguir são apenas para a tecnologia de [*repositório de certificados*](../secgloss/c-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="caabd-236">The following options are for [*certificate store*](../secgloss/c-gly.md) technology only.</span></span>



| <span data-ttu-id="caabd-237">Opção de repositório de certificados</span><span class="sxs-lookup"><span data-stu-id="caabd-237">Certificate store option</span></span>          | <span data-ttu-id="caabd-238">Description</span><span class="sxs-lookup"><span data-stu-id="caabd-238">Description</span></span>                                                                                                                                                                                                                                                                                                                              |
|-----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="caabd-239">**-IC** *IssuerCertFile*</span><span class="sxs-lookup"><span data-stu-id="caabd-239">**-ic** *IssuerCertFile*</span></span>          | <span data-ttu-id="caabd-240">Arquivo que contém o certificado do emissor.</span><span class="sxs-lookup"><span data-stu-id="caabd-240">File that contains the issuer's certificate.</span></span> <span data-ttu-id="caabd-241">O MakeCert pesquisará no repositório de certificados para um certificado com uma correspondência exata.</span><span class="sxs-lookup"><span data-stu-id="caabd-241">MakeCert will search in the certificate store for a certificate with an exact match.</span></span>                                                                                                                                                                                                        |
| <span data-ttu-id="caabd-242">**-em** *IssuerNameString*</span><span class="sxs-lookup"><span data-stu-id="caabd-242">**-in** *IssuerNameString*</span></span>        | <span data-ttu-id="caabd-243">Nome comum do certificado do emissor.</span><span class="sxs-lookup"><span data-stu-id="caabd-243">Common name of the issuer's certificate.</span></span> <span data-ttu-id="caabd-244">O MakeCert pesquisará no repositório de certificados para um certificado cujo nome comum inclua *IssuerNameString*.</span><span class="sxs-lookup"><span data-stu-id="caabd-244">MakeCert will search in the certificate store for a certificate whose common name includes *IssuerNameString*.</span></span>                                                                                                                                                                                  |
| <span data-ttu-id="caabd-245">**-ir** *IssuerCertStoreLocation*</span><span class="sxs-lookup"><span data-stu-id="caabd-245">**-ir** *IssuerCertStoreLocation*</span></span> | <span data-ttu-id="caabd-246">Local do registro do repositório de certificados do emissor.</span><span class="sxs-lookup"><span data-stu-id="caabd-246">Registry location of the issuer's certificate store.</span></span> <span data-ttu-id="caabd-247">*IssuerCertStoreLocation* deve ser **LocalMachine** (chave do registro hKey \_ local \_ Machine) ou **CurrentUser** (chave do registro hKey \_ Current \_ User).</span><span class="sxs-lookup"><span data-stu-id="caabd-247">*IssuerCertStoreLocation* must be either **LocalMachine** (registry key HKEY\_LOCAL\_MACHINE) or **CurrentUser** (registry key HKEY\_CURRENT\_USER).</span></span> <span data-ttu-id="caabd-248">**CurrentUser** é o padrão.</span><span class="sxs-lookup"><span data-stu-id="caabd-248">**CurrentUser** is the default.</span></span>                                                                                                |
| <span data-ttu-id="caabd-249">**-é** *IssuerCertStoreName*</span><span class="sxs-lookup"><span data-stu-id="caabd-249">**-is** *IssuerCertStoreName*</span></span>     | <span data-ttu-id="caabd-250">Repositório de certificados do emissor que inclui o certificado do emissor e suas informações de chave privada associadas.</span><span class="sxs-lookup"><span data-stu-id="caabd-250">Issuer's certificate store that includes the issuer's certificate and its associated private key information.</span></span> <span data-ttu-id="caabd-251">Se houver mais de um certificado no repositório, o usuário deverá identificá-lo exclusivamente usando a opção **-IC** ou **-in** .</span><span class="sxs-lookup"><span data-stu-id="caabd-251">If there is more than one certificate in the store, the user must uniquely identify it by using the **-ic** or **-in** option.</span></span> <span data-ttu-id="caabd-252">Se o certificado no repositório de certificados não for identificado de forma exclusiva, o MakeCert falhará.</span><span class="sxs-lookup"><span data-stu-id="caabd-252">If the certificate in the certificate store is not uniquely identified, MakeCert will fail.</span></span> |



 

 

 
