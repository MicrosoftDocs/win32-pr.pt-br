---
description: No exemplo a seguir, uma empresa de desenvolvimento de software hipotética chamada Litware, Inc.
ms.assetid: e4392907-a84f-40ea-aa88-2ad0510bca3c
title: Exemplo de associação de arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f4104c9bc241fed4bc698bd150b03d32a70e054
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089730"
---
# <a name="file-association-example"></a><span data-ttu-id="23a8a-103">Exemplo de associação de arquivo</span><span class="sxs-lookup"><span data-stu-id="23a8a-103">File Association Example</span></span>

<span data-ttu-id="23a8a-104">No exemplo a seguir, uma empresa de desenvolvimento de software hipotética chamada Litware, Inc. cria um novo player de áudio chamado LitwarePlayer.</span><span class="sxs-lookup"><span data-stu-id="23a8a-104">In the following example, a hypothetical software development company called Litware, Inc. creates a new audio player called LitwarePlayer.</span></span> <span data-ttu-id="23a8a-105">O Litware quer criar uma associação de arquivo entre LitwarePlayer e seu tipo de arquivo primário, que usa um formato de áudio desenvolvido recentemente que permite que um CD de áudio inteiro seja armazenado em menos de 10 kilobytes de memória sem perda de qualidade.</span><span class="sxs-lookup"><span data-stu-id="23a8a-105">Litware wants to design a file association between LitwarePlayer and its primary file type, which uses a newly developed audio format that enables an entire audio CD to be stored in less than 10 kilobytes of memory with no loss of quality.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="23a8a-106">Este tópico não se aplica ao Windows 10.</span><span class="sxs-lookup"><span data-stu-id="23a8a-106">This topic does not apply for Windows 10.</span></span> <span data-ttu-id="23a8a-107">A maneira como as associações de arquivo padrão funcionam alteradas no Windows 10.</span><span class="sxs-lookup"><span data-stu-id="23a8a-107">The way that default file associations work changed in Windows 10.</span></span> <span data-ttu-id="23a8a-108">Para obter mais informações, consulte a seção sobre **alterações de como o Windows 10 trata os aplicativos padrão** nesta [postagem](https://blogs.windows.com/bloggingwindows/2015/05/20/announcing-windows-10-insider-preview-build-10122-for-pcs/).</span><span class="sxs-lookup"><span data-stu-id="23a8a-108">For more information, see the section on **Changes to how Windows 10 handles default apps** in [this post](https://blogs.windows.com/bloggingwindows/2015/05/20/announcing-windows-10-insider-preview-build-10122-for-pcs/).</span></span>

 

## <a name="designing-a-new-file-association"></a><span data-ttu-id="23a8a-109">Criando uma nova associação de arquivo</span><span class="sxs-lookup"><span data-stu-id="23a8a-109">Designing a New File Association</span></span>

<span data-ttu-id="23a8a-110">A empresa deve executar as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="23a8a-110">The company should take the following steps.</span></span>

1.  <span data-ttu-id="23a8a-111">**Decida se o novo tipo de arquivo deve ser tratado como público ou privado.**</span><span class="sxs-lookup"><span data-stu-id="23a8a-111">**Decide if the new file type should be treated as public or private.**</span></span> <span data-ttu-id="23a8a-112">Esse novo tipo de arquivo é um tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="23a8a-112">This new file type is a media type.</span></span> <span data-ttu-id="23a8a-113">Como os usuários trocam arquivos de mídia em várias plataformas e pode haver outros aplicativos que precisam ler o formato LitwarePlayer, um tipo de arquivo [público](fa-file-types.md) é o mais apropriado.</span><span class="sxs-lookup"><span data-stu-id="23a8a-113">Because users exchange media files across various platforms and there might be other applications that need to read the LitwarePlayer format, a [public](fa-file-types.md) file type is the most appropriate.</span></span>
2.  <span data-ttu-id="23a8a-114">**Determine se esse tipo de arquivo já está definido.**</span><span class="sxs-lookup"><span data-stu-id="23a8a-114">**Determine whether this file type is already defined.**</span></span> <span data-ttu-id="23a8a-115">Verifique o banco de dados MIME da IANA (Internet Assigned Numbers Authority) e outros tipos de dados públicos de tipo de arquivo na Internet para determinar que nenhum tipo de arquivo comparável foi definido.</span><span class="sxs-lookup"><span data-stu-id="23a8a-115">Check the Internet Assigned Numbers Authority (IANA) MIME database, and other public file type databases on the Internet to determine that no comparable file type has been defined.</span></span> <span data-ttu-id="23a8a-116">Como esse é um novo formato de arquivo, você precisa definir um novo tipo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="23a8a-116">Because this is a new file format, you need to define a new file type.</span></span>
3.  <span data-ttu-id="23a8a-117">**Defina uma extensão de nome de arquivo para o novo tipo de arquivo.**</span><span class="sxs-lookup"><span data-stu-id="23a8a-117">**Define a file name extension for the new file type.**</span></span> <span data-ttu-id="23a8a-118">Os desenvolvedores escolhem o `.opa-ltw-audio` , que incorpora a abreviação de seu fornecedor e uma dica sobre o que o arquivo contém.</span><span class="sxs-lookup"><span data-stu-id="23a8a-118">The developers choose the `.opa-ltw-audio`, which incorporates their vendor abbreviation and a hint about the what the file contains.</span></span> <span data-ttu-id="23a8a-119">A pesquisa determina que a extensão não está sendo usada por mais ninguém.</span><span class="sxs-lookup"><span data-stu-id="23a8a-119">Research determines that the extension is not being used by anyone else.</span></span> <span data-ttu-id="23a8a-120">Seguindo as recomendações atuais, nenhuma extensão curta é definida.</span><span class="sxs-lookup"><span data-stu-id="23a8a-120">Following current recommendations, no short extension is defined.</span></span>
4.  <span data-ttu-id="23a8a-121">**Defina um tipo MIME para o tipo de arquivo e registre-o com o IANA.**</span><span class="sxs-lookup"><span data-stu-id="23a8a-121">**Define a MIME type for the file type and register it with the IANA.**</span></span> <span data-ttu-id="23a8a-122">A Litware define o novo tipo MIME como *Audio/LitwarePlayer. 1* e prepara um aplicativo de tipo MIME, seguindo as diretrizes dispostas nos números RFC (Request for Comments) 2045, 2046, 2047 e 2048.</span><span class="sxs-lookup"><span data-stu-id="23a8a-122">Litware defines the new MIME type as *audio/LitwarePlayer.1* and prepares a MIME type application, following the guidelines laid out in Request for Comments (RFC) numbers 2045, 2046, 2047, and 2048.</span></span> <span data-ttu-id="23a8a-123">Em seguida, eles enviam o aplicativo para o IANA, que adiciona o novo tipo de arquivo ao banco de dados de tipos MIME registrados.</span><span class="sxs-lookup"><span data-stu-id="23a8a-123">They then submit the application to the IANA, which adds the new file type to the database of registered MIME types.</span></span>
5.  <span data-ttu-id="23a8a-124">**Determine se existe um ProgID para o tipo de arquivo.**</span><span class="sxs-lookup"><span data-stu-id="23a8a-124">**Determine whether a ProgID exists for the file type.**</span></span> <span data-ttu-id="23a8a-125">Como esse é um novo tipo de arquivo, não existe nenhum [ProgID](fa-progids.md) para ele.</span><span class="sxs-lookup"><span data-stu-id="23a8a-125">Because this is a new file type, no [ProgID](fa-progids.md) exists for it.</span></span> <span data-ttu-id="23a8a-126">Litware sets sobre a criação de um novo ProgID para LitwarePlayer.</span><span class="sxs-lookup"><span data-stu-id="23a8a-126">Litware sets about designing a new ProgID for LitwarePlayer.</span></span> <span data-ttu-id="23a8a-127">Eles decidem o nome amigável "Player de áudio LitwarePlayer" (que é armazenado como um recurso no arquivo LitwarePlayer.exe) e criam um ícone padrão a ser usado para os arquivos associados ao LitwarePlayer (também armazenados em LitwarePlayer.exe).</span><span class="sxs-lookup"><span data-stu-id="23a8a-127">They decide on the friendly name "LitwarePlayer Audio Player" (which is stored as a resource in the LitwarePlayer.exe file), and they design a default icon to use for files associated with LitwarePlayer (also stored in LitwarePlayer.exe).</span></span> <span data-ttu-id="23a8a-128">Como LitwarePlayer é um novo aplicativo, este é um ProgID da versão 1.</span><span class="sxs-lookup"><span data-stu-id="23a8a-128">Because LitwarePlayer is a new application, this is a version 1 ProgID.</span></span>
6.  <span data-ttu-id="23a8a-129">**Registre o ProgID.**</span><span class="sxs-lookup"><span data-stu-id="23a8a-129">**Register the ProgID.**</span></span> <span data-ttu-id="23a8a-130">Quando o LitwarePlayer é instalado, o programa de instalação cria a seguinte entrada de [ProgID](fa-progids.md) no registro.</span><span class="sxs-lookup"><span data-stu-id="23a8a-130">When LitwarePlayer is installed, the installation program creates the following [ProgID](fa-progids.md) entry in the registry.</span></span>

    ```
    HKEY_CLASSES_ROOT
       Litware.LitwarePlayer.1
          (Default) = LitwarePlayer Audio Player
          FriendlyTypeName = @LitwarePlayer, -120
          CurVer
             (Default) = Litware.LitwarePlayer.1
          DefaultIcon
             (Default) = LitwarePlayer, -142
          shell
             play
                command
                   (Default) = "%ProgramFiles%\LitwarePlayer\LitwarePlayer.exe" "%1"
    ```

    <span data-ttu-id="23a8a-131">Na chave de comando, %1 é passado como o caminho para o arquivo a ser reproduzido.</span><span class="sxs-lookup"><span data-stu-id="23a8a-131">In the command key, %1 is passed as the path to the file to play.</span></span>

7.  <span data-ttu-id="23a8a-132">**Registre a extensão de nome de arquivo para o tipo de arquivo.**</span><span class="sxs-lookup"><span data-stu-id="23a8a-132">**Register the file name extension for the file type.**</span></span> <span data-ttu-id="23a8a-133">Quando o LitwarePlayer é instalado, o programa de instalação cria as seguintes entradas no registro para sua extensão de tipo de arquivo personalizado.</span><span class="sxs-lookup"><span data-stu-id="23a8a-133">When LitwarePlayer is installed, the installation program creates the following entries in the registry for its custom file type extension.</span></span>

    ```
    HKEY_CLASSES_ROOT
       .opa-vwi-audio
          (Default) = Litware.LitwarePlayer.1
          PerceivedType = Audio
          Content Type = audio/LitwarePlayer
    ```

> [!Note]  
> <span data-ttu-id="23a8a-134">Sempre que uma associação de arquivo é criada ou alterada, notifique o sistema de que uma alteração foi feita chamando [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify), especificando o \_ evento SHCNE assocchanged.</span><span class="sxs-lookup"><span data-stu-id="23a8a-134">Whenever a file association is created or changed, notify the system that a change has been made by calling [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify), specifying the SHCNE\_ASSOCCHANGED event.</span></span> <span data-ttu-id="23a8a-135">Se isso não for feito, o Shell poderá não reconhecer nenhuma alteração feita até que o sistema seja reiniciado.</span><span class="sxs-lookup"><span data-stu-id="23a8a-135">If this is not done, the Shell might not recognize any changes made until the system restarts.</span></span>

 

## <a name="additional-resources"></a><span data-ttu-id="23a8a-136">Recursos adicionais</span><span class="sxs-lookup"><span data-stu-id="23a8a-136">Additional Resources</span></span>

-   [<span data-ttu-id="23a8a-137">Introdução às associações de arquivo</span><span class="sxs-lookup"><span data-stu-id="23a8a-137">Introduction to File Associations</span></span>](fa-intro.md)
-   [<span data-ttu-id="23a8a-138">Como registrar um navegador da Internet ou cliente de email com o menu Iniciar do Windows</span><span class="sxs-lookup"><span data-stu-id="23a8a-138">How to Register an Internet Browser or Email Client With the Windows Start Menu</span></span>](start-menu-reg.md)
-   <span data-ttu-id="23a8a-139">[Registrando um aplicativo em um esquema de URI](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767914(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="23a8a-139">[Registering an Application to a URI Scheme](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767914(v=vs.85))</span></span>

## <a name="related-topics"></a><span data-ttu-id="23a8a-140">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="23a8a-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="23a8a-141">Práticas recomendadas para associações de arquivo</span><span class="sxs-lookup"><span data-stu-id="23a8a-141">Best Practices for File Associations</span></span>](fa-best-practices.md)
</dt> <dt>

[<span data-ttu-id="23a8a-142">Diretrizes para o gerenciamento de aplicativos padrão no Windows Vista e posterior</span><span class="sxs-lookup"><span data-stu-id="23a8a-142">Guidelines for Managing Default Applications in Windows Vista and Later</span></span>](vista-managing-defaults.md)
</dt> <dt>

[<span data-ttu-id="23a8a-143">Programas padrão</span><span class="sxs-lookup"><span data-stu-id="23a8a-143">Default Programs</span></span>](default-programs.md)
</dt> <dt>

[<span data-ttu-id="23a8a-144">Definir o acesso do programa e padrões do computador (SPAD)</span><span class="sxs-lookup"><span data-stu-id="23a8a-144">Set Program Access and Computer Defaults (SPAD)</span></span>](cpl-setprogramaccess.md)
</dt> </dl>

 

 
