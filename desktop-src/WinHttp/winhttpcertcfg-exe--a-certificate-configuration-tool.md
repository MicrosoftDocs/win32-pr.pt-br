---
description: A ferramenta de configuração de certificado do Microsoft Windows HTTP Services (WinHTTP), &\# 0034; WinHttpCertCfg.exe&\# 0034;, permite que os administradores instalem e configurem certificados de cliente em qualquer repositório de certificados que possa ser acessado pela conta do Gerenciador de aplicativos da Web do servidor da Internet (IWAM). A ferramenta também elimina a necessidade de fazer qualquer coisa especial para contas como a conta IWAM para obter acesso aos certificados ao usar páginas de Active Server (ASP).
ms.assetid: e4c2afc2-0fd3-4bdd-812e-f112958e1576
title: WinHttpCertCfg.exe, uma ferramenta de configuração de certificado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4250cd717b9f611f4f23f17c93069760c283c97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090422"
---
# <a name="winhttpcertcfgexe-a-certificate-configuration-tool"></a><span data-ttu-id="23579-104">WinHttpCertCfg.exe, uma ferramenta de configuração de certificado</span><span class="sxs-lookup"><span data-stu-id="23579-104">WinHttpCertCfg.exe, a Certificate Configuration Tool</span></span>

<span data-ttu-id="23579-105">A ferramenta de configuração de certificado do [Microsoft Windows http Services (WinHTTP)](about-winhttp.md) , "WinHttpCertCfg.exe", permite que os administradores instalem e configurem certificados de cliente em qualquer [*repositório de certificados*](glossary.md) que possa ser acessado pela conta do Gerenciador de aplicativos da Web do servidor da Internet (IWAM).</span><span class="sxs-lookup"><span data-stu-id="23579-105">The [Microsoft Windows HTTP Services (WinHTTP)](about-winhttp.md) certificate configuration tool, "WinHttpCertCfg.exe", enables administrators to install and configure client certificates in any [*certificate store*](glossary.md) that can be accessed by the Internet Server Web Application Manager (IWAM) account.</span></span> <span data-ttu-id="23579-106">A ferramenta também elimina a necessidade de fazer qualquer coisa especial para contas como a conta IWAM para obter acesso aos certificados ao usar páginas de Active Server (ASP).</span><span class="sxs-lookup"><span data-stu-id="23579-106">The tool also eliminates the need to do anything special to accounts such as the IWAM account to gain access to certificates when using Active Server Pages (ASP).</span></span>

<span data-ttu-id="23579-107">O MMC (console de gerenciamento Microsoft) permite que os administradores importem certificados de cliente para um computador local.</span><span class="sxs-lookup"><span data-stu-id="23579-107">The Microsoft Management Console (MMC) enables administrators to import client certificates to a local computer.</span></span> <span data-ttu-id="23579-108">No entanto, a importação de um certificado não concede automaticamente acesso à chave privada para outras contas.</span><span class="sxs-lookup"><span data-stu-id="23579-108">However, importing a certificate does not automatically grant access to the private key for other accounts.</span></span> <span data-ttu-id="23579-109">Essa chave privada é necessária para a autenticação de certificado do cliente.</span><span class="sxs-lookup"><span data-stu-id="23579-109">This private key is required for client certificate authentication.</span></span> <span data-ttu-id="23579-110">A ferramenta de configuração de certificado do Microsoft Windows HTTP Services (WinHTTP) fornece a capacidade de conceder acesso a contas adicionais, como a conta IWAM, quando necessário.</span><span class="sxs-lookup"><span data-stu-id="23579-110">The Microsoft Windows HTTP Services (WinHTTP) certificate configuration tool provides the ability to grant access to additional accounts, such as the IWAM account, when required.</span></span>

-   [<span data-ttu-id="23579-111">Usando a ferramenta de configuração de certificado</span><span class="sxs-lookup"><span data-stu-id="23579-111">Using the Certificate Configuration Tool</span></span>](#using-the-certificate-configuration-tool)
-   [<span data-ttu-id="23579-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="23579-112">Examples</span></span>](#examples)

## <a name="using-the-certificate-configuration-tool"></a><span data-ttu-id="23579-113">Usando a ferramenta de configuração de certificado</span><span class="sxs-lookup"><span data-stu-id="23579-113">Using the Certificate Configuration Tool</span></span>

<span data-ttu-id="23579-114">A ferramenta de configuração de certificado WinHTTP, WinHttpCertCfg.exe, está disponível como um download no site de [Ferramentas do Windows Server 2003 Resource Kit](https://www.microsoft.com/downloads/details.aspx?familyid=9d467a69-57ff-4ae7-96ee-b18c4790cffd) .</span><span class="sxs-lookup"><span data-stu-id="23579-114">The WinHTTP certificate configuration tool, WinHttpCertCfg.exe, is available as a download on the [Windows Server 2003 Resource Kit Tools](https://www.microsoft.com/downloads/details.aspx?familyid=9d467a69-57ff-4ae7-96ee-b18c4790cffd) website.</span></span> <span data-ttu-id="23579-115">O código de exemplo a seguir mostra os parâmetros de linha de comando válidos a serem usados com essa ferramenta.</span><span class="sxs-lookup"><span data-stu-id="23579-115">The following example code shows the valid command line parameters to use with this tool.</span></span>

``` syntax
winhttpcertcfg [-?]
 
winhttpcertcfg [-i PFXFile | -g | -r | -l]
               [-a Account] [-c CertStore] 
               [-s SubjectStr] [-p PFXPassword]
```

<span data-ttu-id="23579-116">A tabela a seguir lista os parâmetros para a ferramenta de configuração do.</span><span class="sxs-lookup"><span data-stu-id="23579-116">The following table lists parameters for the configuration tool.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="23579-117">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="23579-117">Parameter</span></span></th>
<th><span data-ttu-id="23579-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="23579-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="23579-119">-?</span><span class="sxs-lookup"><span data-stu-id="23579-119">-?</span></span></td>
<td><span data-ttu-id="23579-120">Exibe dados de sintaxe.</span><span class="sxs-lookup"><span data-stu-id="23579-120">Displays syntax data.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="23579-121">-i</span><span class="sxs-lookup"><span data-stu-id="23579-121">-i</span></span></td>
<td><span data-ttu-id="23579-122">Especifica que o certificado deve ser importado de um arquivo de troca de informações pessoais (PFX).</span><span class="sxs-lookup"><span data-stu-id="23579-122">Specifies that the certificate is to be imported from a Personal Information Exchange (PFX) file.</span></span> <span data-ttu-id="23579-123">Esse parâmetro deve ser seguido pelo nome do arquivo.</span><span class="sxs-lookup"><span data-stu-id="23579-123">This parameter must be followed by the name of the file.</span></span> <span data-ttu-id="23579-124">Quando esse parâmetro é especificado, &quot; -a &quot; e &quot; -c &quot; também devem ser especificados.</span><span class="sxs-lookup"><span data-stu-id="23579-124">When this parameter is specified, &quot;-a&quot; and &quot;-c&quot; must also be specified.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="23579-125">-g</span><span class="sxs-lookup"><span data-stu-id="23579-125">-g</span></span></td>
<td><span data-ttu-id="23579-126">Especifica que o acesso é concedido a uma chave privada.</span><span class="sxs-lookup"><span data-stu-id="23579-126">Specifies that access is granted to a private key.</span></span> <span data-ttu-id="23579-127">Quando esse parâmetro é especificado, &quot; -a &quot; , &quot; -c e &quot; &quot; -s &quot; também devem ser especificados.</span><span class="sxs-lookup"><span data-stu-id="23579-127">When this parameter is specified, &quot;-a&quot;, &quot;-c&quot;, and &quot;-s&quot; must also be specified.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="23579-128">-r</span><span class="sxs-lookup"><span data-stu-id="23579-128">-r</span></span></td>
<td><span data-ttu-id="23579-129">Especifica que o acesso é removido para uma chave privada.</span><span class="sxs-lookup"><span data-stu-id="23579-129">Specifies that access is removed for a private key.</span></span> <span data-ttu-id="23579-130">Quando esse parâmetro é especificado, &quot; -a &quot; , &quot; -c e &quot; &quot; -s &quot; também devem ser especificados.</span><span class="sxs-lookup"><span data-stu-id="23579-130">When this parameter is specified, &quot;-a&quot;, &quot;-c&quot;, and &quot;-s&quot; must also be specified.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="23579-131">-l</span><span class="sxs-lookup"><span data-stu-id="23579-131">-l</span></span></td>
<td><span data-ttu-id="23579-132">Especifica que as contas com acesso a uma chave privada estão listadas.</span><span class="sxs-lookup"><span data-stu-id="23579-132">Specifies that accounts with access to a private key are listed.</span></span> <span data-ttu-id="23579-133">Quando esse parâmetro é especificado, &quot; -c &quot; e &quot; -s &quot; também devem ser especificados.</span><span class="sxs-lookup"><span data-stu-id="23579-133">When this parameter is specified, &quot;-c&quot; and &quot;-s&quot; must also be specified.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="23579-134">-a</span><span class="sxs-lookup"><span data-stu-id="23579-134">-a</span></span></td>
<td><span data-ttu-id="23579-135">Especifica a conta de usuário no computador que está sendo configurado.</span><span class="sxs-lookup"><span data-stu-id="23579-135">Specifies the user account on the machine being configured.</span></span> <span data-ttu-id="23579-136">Pode ser um computador local ou uma conta de domínio, como &quot; IWAM_TESTMACHINE &quot; , &quot; testuser &quot; ou &quot; TESTDOMAIN\DOMAINUSER &quot; .</span><span class="sxs-lookup"><span data-stu-id="23579-136">This could be a local machine or domain account, such as &quot;IWAM_TESTMACHINE&quot;, &quot;TESTUSER&quot;, or &quot;TESTDOMAIN\DOMAINUSER&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="23579-137">-c</span><span class="sxs-lookup"><span data-stu-id="23579-137">-c</span></span></td>
<td><span data-ttu-id="23579-138">Especifica o local e o nome do <a href="glossary.md"><em>repositório de certificados</em></a>.</span><span class="sxs-lookup"><span data-stu-id="23579-138">Specifies the location and name of the <a href="glossary.md"><em>certificate store</em></a>.</span></span> <span data-ttu-id="23579-139">Use &quot; local_machine &quot; ou &quot; CURRENT_USER &quot; para designar qual ramificação do Registro usar para o local.</span><span class="sxs-lookup"><span data-stu-id="23579-139">Use &quot;LOCAL_MACHINE&quot; or &quot;CURRENT_USER&quot; to designate which registry branch to use for the location.</span></span> <span data-ttu-id="23579-140">O <em>repositório de certificados</em> pode ser qualquer instalado no computador.</span><span class="sxs-lookup"><span data-stu-id="23579-140">The <em>certificate store</em> can be any installed on the machine.</span></span> <span data-ttu-id="23579-141">Os exemplos de nome típicos são &quot; My &quot; , &quot; root &quot; e &quot; TrustedPeople &quot; .</span><span class="sxs-lookup"><span data-stu-id="23579-141">Typical name examples are &quot;MY&quot;, &quot;Root&quot;, and &quot;TrustedPeople&quot;.</span></span> <span data-ttu-id="23579-142">O local e o nome do <em>repositório de certificados</em> são separados por uma barra invertida, por exemplo, &quot; local_machine \root &quot; .</span><span class="sxs-lookup"><span data-stu-id="23579-142">The location and name of the <em>certificate store</em> are separated with a backward slash, for example, &quot;LOCAL_MACHINE\Root&quot;.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="23579-143">Embora a &quot; &quot; ramificação CURRENT_USER do registro possa ser especificada com esse parâmetro, estender o acesso às chaves privadas destina-se principalmente a certificados instalados em um <a href="glossary.md"><em>repositório de certificados</em></a> do computador local que pode ser acessado por vários usuários.</span><span class="sxs-lookup"><span data-stu-id="23579-143">Although the &quot;CURRENT_USER&quot; branch of the registry can be specified with this parameter, extending access to private keys is primarily intended for certificates installed in a local computer <a href="glossary.md"><em>certificate store</em></a> that can be accessed by multiple users.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="23579-144">-S</span><span class="sxs-lookup"><span data-stu-id="23579-144">-s</span></span></td>
<td><span data-ttu-id="23579-145">Especifica uma cadeia de caracteres de pesquisa que não diferencia maiúsculas de minúsculas para localizar o primeiro certificado enumerado com um nome de entidade que contém essa subcadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="23579-145">Specifies a case-insensitive search string for finding the first enumerated certificate with a subject name that contains this substring.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="23579-146">-p</span><span class="sxs-lookup"><span data-stu-id="23579-146">-p</span></span></td>
<td><span data-ttu-id="23579-147">Especifica uma senha que é usada para importar o certificado e a chave privada.</span><span class="sxs-lookup"><span data-stu-id="23579-147">Specifies a password that is used to import the certificate and the private key.</span></span> <span data-ttu-id="23579-148">Isso só é usado com a opção de importação.</span><span class="sxs-lookup"><span data-stu-id="23579-148">This is only used with the import option.</span></span></td>
</tr>
</tbody>
</table>



 

> [!NOTE]
> <span data-ttu-id="23579-149">O usuário deve ter privilégios suficientes para usar essa ferramenta, o que exige que o usuário seja um administrador e o mesmo usuário que instalou o certificado do cliente, se estiver instalado.</span><span class="sxs-lookup"><span data-stu-id="23579-149">The user must have sufficient privileges to use this tool, which requires the user to be an administrator and the same user who installed the client certificate, if installed.</span></span>
>
> <span data-ttu-id="23579-150">A ferramenta "WinHttpCertCfg.exe" não é útil para configurar certificados armazenados em um sistema de arquivos, como FAT32, que não oferece suporte a ACLs (listas de controle de acesso).</span><span class="sxs-lookup"><span data-stu-id="23579-150">The "WinHttpCertCfg.exe" tool is not useful to configure certificates stored in a file system such as FAT32, which does not support access control lists (ACL).</span></span>

## <a name="examples"></a><span data-ttu-id="23579-151">Exemplos</span><span class="sxs-lookup"><span data-stu-id="23579-151">Examples</span></span>

<span data-ttu-id="23579-152">Os exemplos a seguir mostram algumas das maneiras como a ferramenta de configuração pode ser usada.</span><span class="sxs-lookup"><span data-stu-id="23579-152">The following examples show some of the ways in which the configuration tool can be used.</span></span>

1.  <span data-ttu-id="23579-153">Esse comando lista as contas que têm acesso à chave privada para o certificado "myCertificate" no [*repositório de certificados*](glossary.md) "raiz" da \_ ramificação do computador local do registro.</span><span class="sxs-lookup"><span data-stu-id="23579-153">This command lists accounts that have access to the private key for the "MyCertificate" certificate in the "Root" [*certificate store*](glossary.md) of the LOCAL\_MACHINE branch of the registry.</span></span>

    <span data-ttu-id="23579-154">**Winhttpcertcfg-l-c \_ raiz do computador local \\ -s myCertificate**</span><span class="sxs-lookup"><span data-stu-id="23579-154">**winhttpcertcfg -l -c LOCAL\_MACHINE\\Root -s MyCertificate**</span></span>

2.  <span data-ttu-id="23579-155">Esse comando concede acesso à chave privada do certificado "myCertificate" no [*repositório de certificados*](glossary.md) "My" para a conta testuser.</span><span class="sxs-lookup"><span data-stu-id="23579-155">This command grants access to the private key of the "MyCertificate" certificate in the "My" [*certificate store*](glossary.md) for the TESTUSER account.</span></span>

    <span data-ttu-id="23579-156">**Winhttpcertcfg-g-c \_ computador local \\ My-s myCertificate-a testuser**</span><span class="sxs-lookup"><span data-stu-id="23579-156">**winhttpcertcfg -g -c LOCAL\_MACHINE\\My -s MyCertificate -a TESTUSER**</span></span>

3.  <span data-ttu-id="23579-157">Esse comando importa um certificado e uma chave privada de um arquivo PFX e estende o acesso à chave privada para outra conta.</span><span class="sxs-lookup"><span data-stu-id="23579-157">This command imports a certificate and private key from a PFX file and extends private key access to another account.</span></span>

    <span data-ttu-id="23579-158">**Winhttpcertcfg-i PFXFile-c \_ máquina local \\ My-a IWAM \_ TESTMACHINE-p PFXPassword**</span><span class="sxs-lookup"><span data-stu-id="23579-158">**winhttpcertcfg -i PFXFile -c LOCAL\_MACHINE\\My -a IWAM\_TESTMACHINE -p PFXPassword**</span></span>

4.  <span data-ttu-id="23579-159">Esse comando nega o acesso à chave privada para a conta IWAM \_ TESTMACHINE com o certificado especificado.</span><span class="sxs-lookup"><span data-stu-id="23579-159">This command denies access to the private key for the IWAM\_TESTMACHINE account with the specified certificate.</span></span>

    <span data-ttu-id="23579-160">**Winhttpcertcfg-r-c \_ raiz do computador local \\ -s myCertificate-a IWAM \_ TESTMACHINE**</span><span class="sxs-lookup"><span data-stu-id="23579-160">**winhttpcertcfg -r -c LOCAL\_MACHINE\\Root -s MyCertificate -a IWAM\_TESTMACHINE**</span></span>

 

 




