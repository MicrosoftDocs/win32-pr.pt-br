---
description: A lista a seguir é recomendada práticas recomendadas que você deve usar ao trabalhar com associações de arquivos.
title: Práticas recomendadas para associações de arquivo
ms.topic: article
ms.date: 05/31/2018
ms.assetid: d4d0edf9-3475-4164-b0fa-15006e05e242
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: f49c1df6d145c32b8fcbdf70462b30f14f51b3d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501570"
---
# <a name="best-practices-for-file-associations"></a><span data-ttu-id="64ef2-103">Práticas recomendadas para associações de arquivo</span><span class="sxs-lookup"><span data-stu-id="64ef2-103">Best Practices for File Associations</span></span>

<span data-ttu-id="64ef2-104">A lista a seguir é recomendada práticas recomendadas que você deve usar ao trabalhar com associações de arquivos.</span><span class="sxs-lookup"><span data-stu-id="64ef2-104">The following list are recommended best practices you should use when working with file associations.</span></span>

-   [<span data-ttu-id="64ef2-105">Não copie associações de arquivo do registro</span><span class="sxs-lookup"><span data-stu-id="64ef2-105">Do Not Copy File Associations from the Registry</span></span>](#do-not-copy-file-associations-from-the-registry)
-   [<span data-ttu-id="64ef2-106">Evite caminhos de Hard-Coding no registro sempre que possível</span><span class="sxs-lookup"><span data-stu-id="64ef2-106">Avoid Hard-Coding Paths into the Registry Where Possible</span></span>](#avoid-hard-coding-paths-into-the-registry-where-possible)
-   [<span data-ttu-id="64ef2-107">Sempre encapsular cadeias de caracteres em expansão entre aspas</span><span class="sxs-lookup"><span data-stu-id="64ef2-107">Always Wrap Expanding Strings in Quotation Marks</span></span>](#always-wrap-expanding-strings-in-quotation-marks)
-   [<span data-ttu-id="64ef2-108">Não confunda reprodução automática/autorun com associações de arquivo</span><span class="sxs-lookup"><span data-stu-id="64ef2-108">Do Not Confuse Autoplay/Autorun with File Associations</span></span>](#do-not-confuse-autoplayautorun-with-file-associations)
-   [<span data-ttu-id="64ef2-109">Não confunda o banco de dados MIME do Internet Explorer com associações de arquivo</span><span class="sxs-lookup"><span data-stu-id="64ef2-109">Do Not Confuse the Internet Explorer MIME Database with File Associations</span></span>](#do-not-confuse-the-internet-explorer-mime-database-with-file-associations)
-   [<span data-ttu-id="64ef2-110">Usar ProgIDs corretamente formados e com controle de versão</span><span class="sxs-lookup"><span data-stu-id="64ef2-110">Use Properly Formed and Versioned ProgIDs</span></span>](#use-properly-formed-and-versioned-progids)
-   [<span data-ttu-id="64ef2-111">Não usar extensões de nome de arquivo curto</span><span class="sxs-lookup"><span data-stu-id="64ef2-111">Do Not Use Short File Name Extensions</span></span>](#do-not-use-short-file-name-extensions)
-   [<span data-ttu-id="64ef2-112">Registrar novos tipos de arquivo no banco de dados MIME do IANA</span><span class="sxs-lookup"><span data-stu-id="64ef2-112">Register New File Types in the IANA MIME Database</span></span>](#register-new-file-types-in-the-iana-mime-database)
-   [<span data-ttu-id="64ef2-113">Inscreva-se com o serviço Web do Windows para associações de arquivos</span><span class="sxs-lookup"><span data-stu-id="64ef2-113">Sign Up with the Windows Web Service for File Associations</span></span>](#sign-up-with-the-windows-web-service-for-file-associations)
-   [<span data-ttu-id="64ef2-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="64ef2-114">Related topics</span></span>](#related-topics)

## <a name="do-not-copy-file-associations-from-the-registry"></a><span data-ttu-id="64ef2-115">Não copie associações de arquivo do registro</span><span class="sxs-lookup"><span data-stu-id="64ef2-115">Do Not Copy File Associations from the Registry</span></span>

<span data-ttu-id="64ef2-116">Recomendamos que você não copie as associações de arquivo existentes do registro.</span><span class="sxs-lookup"><span data-stu-id="64ef2-116">We recommended that you do not copy existing file associations from the registry.</span></span> <span data-ttu-id="64ef2-117">Isso geralmente leva à propagação de associações de arquivo formadas inadequadamente.</span><span class="sxs-lookup"><span data-stu-id="64ef2-117">This often leads to the propagation of poorly formed file associations.</span></span> <span data-ttu-id="64ef2-118">Em vez disso, você deve seguir as etapas descritas no [cenário de exemplo Associação de arquivo](fa-sample-scenarios.md).</span><span class="sxs-lookup"><span data-stu-id="64ef2-118">Instead, you should follow the steps outlined in [File Association Sample Scenario](fa-sample-scenarios.md).</span></span>

## <a name="avoid-hard-coding-paths-into-the-registry-where-possible"></a><span data-ttu-id="64ef2-119">Evite caminhos de Hard-Coding no registro sempre que possível</span><span class="sxs-lookup"><span data-stu-id="64ef2-119">Avoid Hard-Coding Paths into the Registry Where Possible</span></span>

<span data-ttu-id="64ef2-120">Assim como os caminhos de código fixo em programas podem causar problemas, os caminhos de código fixo no registro também podem causar problemas.</span><span class="sxs-lookup"><span data-stu-id="64ef2-120">Just as hard-coding paths into programs can cause problems, hard-coding paths into the registry can also lead to problems.</span></span> <span data-ttu-id="64ef2-121">Em vez disso, você deve usar cadeias de caracteres de expansão do registro (REG \_ Expand \_ SZ) para fornecer independência de caminho quando aplicável.</span><span class="sxs-lookup"><span data-stu-id="64ef2-121">Instead, you should use registry expansion strings (REG\_EXPAND\_SZ) to provide path independence where applicable.</span></span> <span data-ttu-id="64ef2-122">Por exemplo, em vez de usar este método:</span><span class="sxs-lookup"><span data-stu-id="64ef2-122">For example, instead of using this method:</span></span>

```
HKEY_CLASSES_ROOT
   MyVendor.MyProgram.1
      DefaultIcon
         (Default) = C:\WINNT\hta.exe,1
```

<span data-ttu-id="64ef2-123">Você deve usar este método:</span><span class="sxs-lookup"><span data-stu-id="64ef2-123">You should use this method:</span></span>

```
HKEY_CLASSES_ROOT
   MyVendor.MyProgram.1
      DefaultIcon
         (Default) = "%SYSTEMROOT%\hta.exe,1"
```

## <a name="always-wrap-expanding-strings-in-quotation-marks"></a><span data-ttu-id="64ef2-124">Sempre encapsular cadeias de caracteres em expansão entre aspas</span><span class="sxs-lookup"><span data-stu-id="64ef2-124">Always Wrap Expanding Strings in Quotation Marks</span></span>

<span data-ttu-id="64ef2-125">A expansão de cadeias de caracteres pode conter espaços quando eles são expandidos.</span><span class="sxs-lookup"><span data-stu-id="64ef2-125">Expanding strings can contain spaces when they expand.</span></span> <span data-ttu-id="64ef2-126">Como os espaços são frequentemente interpretados como delimitadores de argumento, eles causam problemas em determinadas circunstâncias.</span><span class="sxs-lookup"><span data-stu-id="64ef2-126">Because spaces are often interpreted as argument delimiters, they cause problems under certain circumstances.</span></span> <span data-ttu-id="64ef2-127">Por exemplo, um comando para invocar myprogram pode ser armazenado no registro como:</span><span class="sxs-lookup"><span data-stu-id="64ef2-127">For example, a command to invoke MyProgram can be stored in the registry as:</span></span>

`%SYSTEMROOT%\MyProgram %1 %2`

<span data-ttu-id="64ef2-128">Myprogram espera que %1 seja o caminho completo para um nome de arquivo e %2 é uma opção para indicar alguma ação.</span><span class="sxs-lookup"><span data-stu-id="64ef2-128">MyProgram expects that %1 is the full path to a file name, and %2 is a switch to indicate some action.</span></span> <span data-ttu-id="64ef2-129">Se esse comando for executado com **os argumentos C: \\ arquivos de programas \\ meus documentos \\document.txt** e **/Print** e supondo uma raiz_do_sistema de C: \\ WinNT, ele se expandirá para:</span><span class="sxs-lookup"><span data-stu-id="64ef2-129">If this command is executed with arguments **C:\\Program Files\\My Documents\\document.txt** and **/print**, and assuming a SYSTEMROOT of C:\\WINNT, it expands to:</span></span>

`C:\WINNT\MyProgram C:\Program Files\My Documents\document.txt /print`

<span data-ttu-id="64ef2-130">Nesse caso, myprogram interpreta que o primeiro argumento é C: \\ Program, e o segundo argumento é files \\ My, que não é o comportamento pretendido.</span><span class="sxs-lookup"><span data-stu-id="64ef2-130">In this case, MyProgram interprets that the first argument is C:\\Program, and the second argument is Files\\My, which is not the intended behavior.</span></span> <span data-ttu-id="64ef2-131">Os argumentos são interpretados corretamente, no entanto, independentemente de conterem espaços, se as cadeias de caracteres em expansão forem encapsuladas entre aspas da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="64ef2-131">The arguments are interpreted correctly, however, regardless of whether they contain spaces, if the expanding strings are wrapped in quotation marks as follows:</span></span>

`"%SYSTEMROOT%\MyProgram" "%1" "%2"`

## <a name="do-not-confuse-autoplayautorun-with-file-associations"></a><span data-ttu-id="64ef2-132">Não confunda reprodução automática/autorun com associações de arquivo</span><span class="sxs-lookup"><span data-stu-id="64ef2-132">Do Not Confuse Autoplay/Autorun with File Associations</span></span>

<span data-ttu-id="64ef2-133">As associações de arquivo são semelhantes à reprodução automática/autorun de algumas maneiras.</span><span class="sxs-lookup"><span data-stu-id="64ef2-133">File Associations are similar to Autoplay/Autorun in some ways.</span></span> <span data-ttu-id="64ef2-134">No entanto, a reprodução automática/autorun oferece instalações separadas e distintas das fornecidas pelas associações de arquivo.</span><span class="sxs-lookup"><span data-stu-id="64ef2-134">However, Autoplay/Autorun offers separate and distinct facilities from those provided by file associations.</span></span> <span data-ttu-id="64ef2-135">Para obter mais informações, consulte [criando um aplicativo de CD-ROM habilitado para autorun](autoplay.md).</span><span class="sxs-lookup"><span data-stu-id="64ef2-135">For more information see [Creating an AutoRun-enabled CD-ROM Application](autoplay.md).</span></span>

## <a name="do-not-confuse-the-internet-explorer-mime-database-with-file-associations"></a><span data-ttu-id="64ef2-136">Não confunda o banco de dados MIME do Internet Explorer com associações de arquivo</span><span class="sxs-lookup"><span data-stu-id="64ef2-136">Do Not Confuse the Internet Explorer MIME Database with File Associations</span></span>

<span data-ttu-id="64ef2-137">As associações de arquivo são semelhantes ao banco de dados MIME do Windows Internet Explorer, em que os tipos de arquivo podem (e devem) incluir uma definição de tipo MIME.</span><span class="sxs-lookup"><span data-stu-id="64ef2-137">File Associations are similar to the Windows Internet Explorer MIME database, in that file types can (and should) include a MIME type definition.</span></span> <span data-ttu-id="64ef2-138">No entanto, o banco de dados MIME do Internet Explorer é separado e distinto das associações de arquivo.</span><span class="sxs-lookup"><span data-stu-id="64ef2-138">However, the Internet Explorer MIME database is separate and distinct from file associations.</span></span>

## <a name="use-properly-formed-and-versioned-progids"></a><span data-ttu-id="64ef2-139">Usar ProgIDs corretamente formados e com controle de versão</span><span class="sxs-lookup"><span data-stu-id="64ef2-139">Use Properly Formed and Versioned ProgIDs</span></span>

<span data-ttu-id="64ef2-140">Sempre use [ProgIDs com versão](fa-progids.md), mesmo se houver apenas uma versão do ProgID.</span><span class="sxs-lookup"><span data-stu-id="64ef2-140">Always use [versioned ProgIDs](fa-progids.md), even if there is only one version of the ProgID.</span></span> <span data-ttu-id="64ef2-141">ProgIDs com versão ajudam a evitar conflitos e substituições de ProgID.</span><span class="sxs-lookup"><span data-stu-id="64ef2-141">Versioned ProgIDs help to avoid ProgID conflicts and overwrites.</span></span> <span data-ttu-id="64ef2-142">Eles também permitem que versões diferentes de um aplicativo coexistam.</span><span class="sxs-lookup"><span data-stu-id="64ef2-142">They also enable different versions of an application to co-exist.</span></span>

## <a name="do-not-use-short-file-name-extensions"></a><span data-ttu-id="64ef2-143">Não usar extensões de nome de arquivo curto</span><span class="sxs-lookup"><span data-stu-id="64ef2-143">Do Not Use Short File Name Extensions</span></span>

<span data-ttu-id="64ef2-144">Extensões de nome de arquivo longo oferecem as seguintes vantagens:</span><span class="sxs-lookup"><span data-stu-id="64ef2-144">Long file name extensions offer the following advantages:</span></span>

-   <span data-ttu-id="64ef2-145">O comprimento limitado de extensões curtas as torna propensos a *colisões de extensão.*</span><span class="sxs-lookup"><span data-stu-id="64ef2-145">The limited length of short extensions make them prone to *extension collisions.*</span></span> <span data-ttu-id="64ef2-146">Uma colisão de extensão ocorre quando a mesma extensão é usada para classificar vários tipos de arquivo.</span><span class="sxs-lookup"><span data-stu-id="64ef2-146">An extension collision occurs when the same extension is used to classify multiple file types.</span></span> <span data-ttu-id="64ef2-147">O uso de extensões longas diminui significativamente as chances de uma colisão.</span><span class="sxs-lookup"><span data-stu-id="64ef2-147">Using long extensions significantly decreases the chances of a collision.</span></span>
-   <span data-ttu-id="64ef2-148">Nomes de arquivo curtos tendem a ser um pouco confusos.</span><span class="sxs-lookup"><span data-stu-id="64ef2-148">Short file names tend to be somewhat cryptic.</span></span> <span data-ttu-id="64ef2-149">As extensões longas tendem a ser mais significativas porque informações adicionais podem ser inseridas na extensão.</span><span class="sxs-lookup"><span data-stu-id="64ef2-149">Long extensions tend to be more meaningful because additional information can be embedded in the extension.</span></span>

<span data-ttu-id="64ef2-150">Para obter mais informações, consulte [extensões de nome de arquivo](fa-file-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="64ef2-150">For more information, see [file name extensions](fa-file-extensions.md).</span></span>

## <a name="register-new-file-types-in-the-iana-mime-database"></a><span data-ttu-id="64ef2-151">Registrar novos tipos de arquivo no banco de dados MIME do IANA</span><span class="sxs-lookup"><span data-stu-id="64ef2-151">Register New File Types in the IANA MIME Database</span></span>

<span data-ttu-id="64ef2-152">A IANA (Internet Assigned Numbers Authority) mantém um banco de dados público de tipos MIME registrados.</span><span class="sxs-lookup"><span data-stu-id="64ef2-152">The Internet Assigned Numbers Authority (IANA) keeps a public database of registered MIME types.</span></span> <span data-ttu-id="64ef2-153">Ao definir um novo tipo de arquivo público, recomendamos que você também defina um tipo MIME para o tipo de arquivo e registre esse tipo com o IANA.</span><span class="sxs-lookup"><span data-stu-id="64ef2-153">When defining a new public file type, we recommended that you also define a MIME type for the file type and register this type with the IANA.</span></span> <span data-ttu-id="64ef2-154">Não há nenhum custo para o registro.</span><span class="sxs-lookup"><span data-stu-id="64ef2-154">There is no cost for registration.</span></span>

## <a name="sign-up-with-the-windows-web-service-for-file-associations"></a><span data-ttu-id="64ef2-155">Inscreva-se com o serviço Web do Windows para associações de arquivos</span><span class="sxs-lookup"><span data-stu-id="64ef2-155">Sign Up with the Windows Web Service for File Associations</span></span>

<span data-ttu-id="64ef2-156">Os desenvolvedores de aplicativos podem se inscrever no serviço Web do Windows que os usuários usam para localizar aplicativos que podem operar em tipos de arquivo específicos.</span><span class="sxs-lookup"><span data-stu-id="64ef2-156">Application developers can sign up with the Windows Web Service that users use to find applications that can operate on specific file types.</span></span> <span data-ttu-id="64ef2-157">O processo de inscrição com o serviço Web é detalhado no [processo de integração do sistema de associação de arquivos do Windows](https://support.microsoft.com/kb/929149).</span><span class="sxs-lookup"><span data-stu-id="64ef2-157">The process for signing up with the web service is detailed in [Windows File Association System on-boarding process](https://support.microsoft.com/kb/929149).</span></span>

## <a name="related-topics"></a><span data-ttu-id="64ef2-158">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="64ef2-158">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="64ef2-159">Cenário de exemplo de associação de arquivo</span><span class="sxs-lookup"><span data-stu-id="64ef2-159">File Association Sample Scenario</span></span>](fa-sample-scenarios.md)
</dt> <dt>

[<span data-ttu-id="64ef2-160">Diretrizes para o gerenciamento de aplicativos padrão no Windows Vista e posterior</span><span class="sxs-lookup"><span data-stu-id="64ef2-160">Guidelines for Managing Default Applications in Windows Vista and Later</span></span>](vista-managing-defaults.md)
</dt> <dt>

[<span data-ttu-id="64ef2-161">Programas padrão</span><span class="sxs-lookup"><span data-stu-id="64ef2-161">Default Programs</span></span>](default-programs.md)
</dt> <dt>

[<span data-ttu-id="64ef2-162">Definir o acesso do programa e padrões do computador (SPAD)</span><span class="sxs-lookup"><span data-stu-id="64ef2-162">Set Program Access and Computer Defaults (SPAD)</span></span>](cpl-setprogramaccess.md)
</dt> </dl>

 

 



