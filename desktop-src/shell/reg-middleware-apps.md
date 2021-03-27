---
description: 'Este tópico explica como registrar um programa no registro do Windows como um dos seguintes tipos de cliente: navegador, email, reprodução de mídia, mensagens instantâneas ou máquina virtual para Java.'
title: Registrando programas com tipos de cliente
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 33fcb63c-3db2-44df-acfe-8c88e2e634e4
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 71dd4e3192dc75821fd0a3e8c0d4742e1a8d571a
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "103837693"
---
# <a name="registering-programs-with-client-types"></a><span data-ttu-id="15794-103">Registrando programas com tipos de cliente</span><span class="sxs-lookup"><span data-stu-id="15794-103">Registering Programs with Client Types</span></span>

<span data-ttu-id="15794-104">Este tópico explica como registrar um programa no registro do Windows como um dos seguintes tipos de cliente: navegador, email, reprodução de mídia, mensagens instantâneas ou máquina virtual para Java.</span><span class="sxs-lookup"><span data-stu-id="15794-104">This topic explains how to register a program in the Windows registry as one of the following client types: browser, email, media playback, instant messaging, or virtual machine for Java.</span></span>

> [!Note]  
> <span data-ttu-id="15794-105">Essas informações se aplicam aos seguintes sistemas operacionais:</span><span class="sxs-lookup"><span data-stu-id="15794-105">This information applies to the following operating systems:</span></span>
> 
> -   <span data-ttu-id="15794-106">Windows 2000 Service Pack 3 (SP3)</span><span class="sxs-lookup"><span data-stu-id="15794-106">Windows 2000 Service Pack 3 (SP3)</span></span>
> -   <span data-ttu-id="15794-107">Windows 2000 Service Pack 4 (SP4)</span><span class="sxs-lookup"><span data-stu-id="15794-107">Windows 2000 Service Pack 4 (SP4)</span></span>
> -   <span data-ttu-id="15794-108">Windows XP Service Pack 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="15794-108">Windows XP Service Pack 1 (SP1)</span></span>
> -   <span data-ttu-id="15794-109">Windows XP Service Pack 2 (SP2)</span><span class="sxs-lookup"><span data-stu-id="15794-109">Windows XP Service Pack 2 (SP2)</span></span>
> -   <span data-ttu-id="15794-110">Windows XP Service Pack 3 (SP3)</span><span class="sxs-lookup"><span data-stu-id="15794-110">Windows XP Service Pack 3 (SP3)</span></span>
> -   <span data-ttu-id="15794-111">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="15794-111">Windows Server 2003</span></span>
> -   <span data-ttu-id="15794-112">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="15794-112">Windows Vista</span></span>
> -   <span data-ttu-id="15794-113">Windows Vista Service Pack 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="15794-113">Windows Vista Service Pack 1 (SP1)</span></span>
> -   <span data-ttu-id="15794-114">Windows 8</span><span class="sxs-lookup"><span data-stu-id="15794-114">Windows 8</span></span>

 

<span data-ttu-id="15794-115">Este tópico inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="15794-115">This topic includes the following sections.</span></span>

-   [<span data-ttu-id="15794-116">Elementos de registro comuns para todos os tipos de cliente</span><span class="sxs-lookup"><span data-stu-id="15794-116">Common Registration Elements for All Client Types</span></span>](#common-registration-elements-for-all-client-types)
    -   [<span data-ttu-id="15794-117">Selecionando um nome canônico</span><span class="sxs-lookup"><span data-stu-id="15794-117">Selecting a Canonical Name</span></span>](#selecting-a-canonical-name)
    -   [<span data-ttu-id="15794-118">Registrando o nome de exibição de um programa</span><span class="sxs-lookup"><span data-stu-id="15794-118">Registering a Program's Display Name</span></span>](#registering-a-programs-display-name)
    -   [<span data-ttu-id="15794-119">Registrando o ícone de um programa</span><span class="sxs-lookup"><span data-stu-id="15794-119">Registering a Program's Icon</span></span>](#registering-a-programs-icon)
    -   [<span data-ttu-id="15794-120">Registrando um verbo aberto</span><span class="sxs-lookup"><span data-stu-id="15794-120">Registering an Open Verb</span></span>](#registering-an-open-verb)
    -   [<span data-ttu-id="15794-121">Registrando informações de instalação</span><span class="sxs-lookup"><span data-stu-id="15794-121">Registering Installation Information</span></span>](#registering-installation-information)
-   [<span data-ttu-id="15794-122">Elementos de registro para tipos de cliente específicos</span><span class="sxs-lookup"><span data-stu-id="15794-122">Registration Elements for Specific Client Types</span></span>](#registration-elements-for-specific-client-types)
    -   [<span data-ttu-id="15794-123">Registro do menu iniciar</span><span class="sxs-lookup"><span data-stu-id="15794-123">Start Menu Registration</span></span>](#start-menu-registration)
    -   [<span data-ttu-id="15794-124">Registro de cliente de email</span><span class="sxs-lookup"><span data-stu-id="15794-124">Mail Client Registration</span></span>](#mail-client-registration)
-   [<span data-ttu-id="15794-125">Concluir os registros de exemplo</span><span class="sxs-lookup"><span data-stu-id="15794-125">Complete Sample Registrations</span></span>](#complete-sample-registrations)
    -   [<span data-ttu-id="15794-126">Um navegador de exemplo</span><span class="sxs-lookup"><span data-stu-id="15794-126">A Sample Browser</span></span>](#a-sample-browser)
    -   [<span data-ttu-id="15794-127">Um navegador de email de exemplo</span><span class="sxs-lookup"><span data-stu-id="15794-127">A Sample Mail Browser</span></span>](#a-sample-mail-browser)
    -   [<span data-ttu-id="15794-128">Um player de mídia de exemplo</span><span class="sxs-lookup"><span data-stu-id="15794-128">A Sample Media Player</span></span>](#a-sample-media-player)
    -   [<span data-ttu-id="15794-129">Um programa de Instant Messenger de exemplo</span><span class="sxs-lookup"><span data-stu-id="15794-129">A Sample Instant Messenger Program</span></span>](#a-sample-instant-messenger-program)
    -   [<span data-ttu-id="15794-130">Uma máquina virtual de exemplo para Java</span><span class="sxs-lookup"><span data-stu-id="15794-130">A Sample Virtual Machine for Java</span></span>](#a-sample-virtual-machine-for-java)
-   [<span data-ttu-id="15794-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="15794-131">Related topics</span></span>](#related-topics)

<span data-ttu-id="15794-132">Este tópico estende a documentação existente sobre o registro de um programa como um determinado tipo de cliente.</span><span class="sxs-lookup"><span data-stu-id="15794-132">This topic extends existing documentation about registering a program as a particular client type.</span></span> <span data-ttu-id="15794-133">Para obter links para essa documentação, consulte a seção Tópicos relacionados.</span><span class="sxs-lookup"><span data-stu-id="15794-133">For links to that documentation, see the Related Topics section.</span></span>

## <a name="common-registration-elements-for-all-client-types"></a><span data-ttu-id="15794-134">Elementos de registro comuns para todos os tipos de cliente</span><span class="sxs-lookup"><span data-stu-id="15794-134">Common Registration Elements for All Client Types</span></span>

<span data-ttu-id="15794-135">Ao registrar um programa como um tipo de cliente, a maioria das entradas de registro é a mesma, independentemente do tipo de cliente.</span><span class="sxs-lookup"><span data-stu-id="15794-135">When registering a program as a client type, most of the registry entries are the same regardless of the client type.</span></span> <span data-ttu-id="15794-136">Algumas entradas do registro, no entanto, são específicas para o tipo de cliente e elas são indicadas na seção [elementos de registro para tipos de cliente específicos](#registration-elements-for-specific-client-types) .</span><span class="sxs-lookup"><span data-stu-id="15794-136">Some registry entries, however, are specific to the client type and these are noted in the [Registration Elements for Specific Client Types](#registration-elements-for-specific-client-types) section.</span></span>

<span data-ttu-id="15794-137">Esta seção aborda os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="15794-137">This section discusses the following topics:</span></span>

-   [<span data-ttu-id="15794-138">Selecionando um nome canônico</span><span class="sxs-lookup"><span data-stu-id="15794-138">Selecting a Canonical Name</span></span>](#selecting-a-canonical-name)
-   [<span data-ttu-id="15794-139">Registrando o nome de exibição de um programa</span><span class="sxs-lookup"><span data-stu-id="15794-139">Registering a Program's Display Name</span></span>](#registering-a-programs-display-name)
-   [<span data-ttu-id="15794-140">Registrando o ícone de um programa</span><span class="sxs-lookup"><span data-stu-id="15794-140">Registering a Program's Icon</span></span>](#registering-a-programs-icon)
-   [<span data-ttu-id="15794-141">Registrando um verbo aberto</span><span class="sxs-lookup"><span data-stu-id="15794-141">Registering an Open Verb</span></span>](#registering-an-open-verb)
-   [<span data-ttu-id="15794-142">Registrando informações de instalação</span><span class="sxs-lookup"><span data-stu-id="15794-142">Registering Installation Information</span></span>](#registering-installation-information)

> [!Note]  
> <span data-ttu-id="15794-143">Nomes de subchaves fornecidos em itálico ao longo deste tópico são espaços reservados para nomes de subchave definidos pelo usuário ou um conjunto de valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="15794-143">Subkey names given in italics throughout this topic are placeholders for user-defined subkey names or a set of possible values.</span></span> <span data-ttu-id="15794-144">Exemplos completos com nomes de exemplo no local são fornecidos na seção de [registros de exemplo completo](#complete-sample-registrations) .</span><span class="sxs-lookup"><span data-stu-id="15794-144">Full examples with example names in place are provided in the [Complete Sample Registrations](#complete-sample-registrations) section.</span></span>

 

<span data-ttu-id="15794-145">Todas as informações de registro de tipo de cliente são armazenadas na seguinte subchave:</span><span class="sxs-lookup"><span data-stu-id="15794-145">All client type registration information is stored under the following subkey:</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
```

<span data-ttu-id="15794-146">*ClientTypeName* é um dos seguintes nomes de subchave:</span><span class="sxs-lookup"><span data-stu-id="15794-146">*ClientTypeName* is one of the following subkey names:</span></span>

-   <span data-ttu-id="15794-147">StartMenuInternet (para navegadores)</span><span class="sxs-lookup"><span data-stu-id="15794-147">StartMenuInternet (for browsers)</span></span>
-   <span data-ttu-id="15794-148">Email (para email)</span><span class="sxs-lookup"><span data-stu-id="15794-148">Mail (for email)</span></span>
-   <span data-ttu-id="15794-149">Mídia (para reprodução de mídia)</span><span class="sxs-lookup"><span data-stu-id="15794-149">Media (for media playback)</span></span>
-   <span data-ttu-id="15794-150">MENSAGENS instantâneas (para mensagens instantâneas)</span><span class="sxs-lookup"><span data-stu-id="15794-150">IM (for instant messaging)</span></span>
-   <span data-ttu-id="15794-151">JavaVM (para máquina virtual para Java)</span><span class="sxs-lookup"><span data-stu-id="15794-151">JavaVM (for virtual machine for Java)</span></span>

<span data-ttu-id="15794-152">Ao longo deste tópico, você notará referências a um programa de computador fictício chamado "visão acesa" da Litware Inc., com um arquivo executável chamado Litview.exe.</span><span class="sxs-lookup"><span data-stu-id="15794-152">Throughout this topic, you will note references to a fictional computer program named "Lit View" by Litware Inc., with an executable file named Litview.exe.</span></span> <span data-ttu-id="15794-153">Esse programa hipotético é usado de maneira intercambiável como um Messenger imediato, um navegador ou outro tipo de programa cliente, conforme necessário, para fins ilustrativos.</span><span class="sxs-lookup"><span data-stu-id="15794-153">This hypothetical program is used interchangeably as an instant messenger, a browser, or another type of client program as needed for illustrative purposes.</span></span>

### <a name="selecting-a-canonical-name"></a><span data-ttu-id="15794-154">Selecionando um nome canônico</span><span class="sxs-lookup"><span data-stu-id="15794-154">Selecting a Canonical Name</span></span>

<span data-ttu-id="15794-155">O fornecedor deve escolher um *nome canônico* para o programa.</span><span class="sxs-lookup"><span data-stu-id="15794-155">The vendor must choose a *canonical name* for the program.</span></span> <span data-ttu-id="15794-156">O nome canônico nunca é mostrado ao usuário, portanto, ele não precisa ser localizado.</span><span class="sxs-lookup"><span data-stu-id="15794-156">The canonical name is never shown to the user, so it does not need to be localized.</span></span> <span data-ttu-id="15794-157">Sua única finalidade é fornecer uma cadeia de caracteres exclusiva que possa ser usada para identificar o programa.</span><span class="sxs-lookup"><span data-stu-id="15794-157">Its only purpose is to provide a unique string that can be used to identify the program.</span></span> <span data-ttu-id="15794-158">Normalmente, é o mesmo que o nome em inglês do programa, mas essa é meramente uma convenção.</span><span class="sxs-lookup"><span data-stu-id="15794-158">It is typically the same as the English name of the program, but this is merely a convention.</span></span>

<span data-ttu-id="15794-159">Para tipos de cliente diferentes de navegadores, o nome canônico pode ser qualquer cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="15794-159">For client types other than browsers, the canonical name can be any string.</span></span> <span data-ttu-id="15794-160">Escolha um nome exclusivo, que provavelmente não será usado por outro fornecedor.</span><span class="sxs-lookup"><span data-stu-id="15794-160">Choose a unique name, one that is not likely to be used by another vendor.</span></span>

<span data-ttu-id="15794-161">Para clientes de navegador, o nome canônico deve ser o nome — incluindo a extensão — do executável associado; por exemplo, "Litview.exe".</span><span class="sxs-lookup"><span data-stu-id="15794-161">For browser clients, the canonical name must be the name—including the extension—of the associated executable; for instance, "Litview.exe".</span></span>

<span data-ttu-id="15794-162">Aqui estão alguns exemplos de nomes canônicos.</span><span class="sxs-lookup"><span data-stu-id="15794-162">Here are some examples of canonical names.</span></span>

-   <span data-ttu-id="15794-163">Iexplore.exe (navegador)</span><span class="sxs-lookup"><span data-stu-id="15794-163">Iexplore.exe (browser)</span></span>
-   <span data-ttu-id="15794-164">Windows Mail (email)</span><span class="sxs-lookup"><span data-stu-id="15794-164">Windows Mail (email)</span></span>
-   <span data-ttu-id="15794-165">Windows Media Player (mídia)</span><span class="sxs-lookup"><span data-stu-id="15794-165">Windows Media Player (media)</span></span>
-   <span data-ttu-id="15794-166">Windows Messenger (mensagens instantâneas)</span><span class="sxs-lookup"><span data-stu-id="15794-166">Windows Messenger (instant messaging)</span></span>

<span data-ttu-id="15794-167">Registre o nome canônico criando uma subchave, como mostrado aqui.</span><span class="sxs-lookup"><span data-stu-id="15794-167">Register the canonical name by creating a subkey as shown here.</span></span> <span data-ttu-id="15794-168">O nome da subchave é o nome canônico.</span><span class="sxs-lookup"><span data-stu-id="15794-168">The name of the subkey is the canonical name.</span></span> <span data-ttu-id="15794-169">Todas as informações relacionadas ao registro desse programa existirão nessa subchave.</span><span class="sxs-lookup"><span data-stu-id="15794-169">All information relating to that program's registration will exist under this subkey.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            CanonicalName
```

### <a name="registering-a-programs-display-name"></a><span data-ttu-id="15794-170">Registrando o nome de exibição de um programa</span><span class="sxs-lookup"><span data-stu-id="15794-170">Registering a Program's Display Name</span></span>

<span data-ttu-id="15794-171">A próxima etapa no registro é especificar o nome de exibição do programa.</span><span class="sxs-lookup"><span data-stu-id="15794-171">The next step in registration is to specify the program's display name.</span></span> <span data-ttu-id="15794-172">Ele é fornecido como um valor sob a chave de nome canônica, como mostrado aqui.</span><span class="sxs-lookup"><span data-stu-id="15794-172">It is given as a value under the canonical name key as shown here.</span></span> <span data-ttu-id="15794-173">Observe novamente que *canônicaname* e *ClientTypeName* não são os nomes reais das chaves, mas somente espaços reservados para os nomes verdadeiros, como a *exibição acesa*.</span><span class="sxs-lookup"><span data-stu-id="15794-173">Note again that *CanonicalName* and *ClientTypeName* are not the actual names of the keys, but only placeholders for the true names, such as *Lit View*.</span></span>

> [!Note]  
> <span data-ttu-id="15794-174">A partir do Windows 8, o nome usado para se registrar para [Definir acesso do programa e padrões do computador (SPAD)](cpl-setprogramaccess.md) e para [programas padrão](default-programs.md) deve corresponder para que as alterações SPAD disparem os registros de programas padrão.</span><span class="sxs-lookup"><span data-stu-id="15794-174">As of Windows 8, the name used to register for [Set Program Access and Computer Defaults (SPAD)](cpl-setprogramaccess.md) and for [Default Programs](default-programs.md) should match in order for SPAD changes to trigger Default Programs registrations.</span></span>

 

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            CanonicalName
               LocalizedString = @FilePath,-StringID
```

<span data-ttu-id="15794-175">O valor de **localizadastring** é uma \_ cadeia de caracteres reg sz e consiste em um sinal "arroba" (@), o caminho completo de um arquivo. dll ou. exe, uma vírgula, um sinal de menos e um inteiro decimal.</span><span class="sxs-lookup"><span data-stu-id="15794-175">The **LocalizedString** value is a REG\_SZ string and consists of an "at" sign (@), the full path to a .dll or .exe file, a comma, a minus sign, and a decimal integer.</span></span> <span data-ttu-id="15794-176">O inteiro decimal é a ID de um recurso de cadeia de caracteres — contida no arquivo. dll ou. exe — cujo valor deve ser exibido para o usuário como o nome desse cliente.</span><span class="sxs-lookup"><span data-stu-id="15794-176">The decimal integer is the ID of a string resource—contained within the .dll or .exe file—whose value is to be displayed to the user as the name of this client.</span></span> <span data-ttu-id="15794-177">Observe que o caminho do arquivo não requer aspas, mesmo que contenha espaços.</span><span class="sxs-lookup"><span data-stu-id="15794-177">Note that the file path does not require quotation marks, even if it contains spaces.</span></span>

<span data-ttu-id="15794-178">Registrar a cadeia de caracteres do nome de exibição dessa maneira permite que o mesmo registro seja usado para vários idiomas.</span><span class="sxs-lookup"><span data-stu-id="15794-178">Registering the display name string in this manner allows the same registration to be used for multiple languages.</span></span> <span data-ttu-id="15794-179">Cada instalação de idioma fornece um arquivo de recurso diferente com o nome de exibição armazenado na mesma ID de recurso.</span><span class="sxs-lookup"><span data-stu-id="15794-179">Each language installation provides a different resource file with the display name stored at the same resource ID.</span></span>

<span data-ttu-id="15794-180">O exemplo a seguir mostra o registro de um programa de mensagens instantâneas de exibição iluminada fictícia.</span><span class="sxs-lookup"><span data-stu-id="15794-180">The following example shows the registration for a fictional Lit View instant messaging program.</span></span> <span data-ttu-id="15794-181">Como é um programa de mensagens instantâneas, a subchave *canônicaname* (nesse caso, *exibição iluminada*) é armazenada na subchave **im** .</span><span class="sxs-lookup"><span data-stu-id="15794-181">Because it is an instant messaging program, the *CanonicalName* subkey (in this case *Lit View*) is stored under the **IM** subkey.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         IM
            Lit View
               (Default) = Lit View
               LocalizedString = @C:\Program Files\LitwareInc\ResourceDLL.dll,-123
```

<span data-ttu-id="15794-182">Observe o uso da entrada (padrão) como uma declaração secundária do nome de exibição do cliente.</span><span class="sxs-lookup"><span data-stu-id="15794-182">Note the use of the (Default) entry as a secondary declaration of the client's display name.</span></span> <span data-ttu-id="15794-183">Se a **localizadastring** não estiver presente, o valor (padrão) será usado em seu lugar.</span><span class="sxs-lookup"><span data-stu-id="15794-183">If the **LocalizedString** is not present, the (Default) value is used instead.</span></span> <span data-ttu-id="15794-184">Isso funciona com todos os tipos de cliente (navegadores da Internet, navegadores de email, mensageiros instantâneos e players de mídia).</span><span class="sxs-lookup"><span data-stu-id="15794-184">This works with all client types (Internet browsers, email browsers, instant messengers, and media players).</span></span> <span data-ttu-id="15794-185">Para compatibilidade com versões anteriores com o [layout do registro do cliente do Internet Explorer](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa753633(v=vs.85)), os programas de email devem definir o valor (padrão) da subchave *canônicaname* para o nome de exibição do cliente no idioma atualmente instalado.</span><span class="sxs-lookup"><span data-stu-id="15794-185">For backward compatibility with the [Internet Explorer Client Registry Layout](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa753633(v=vs.85)), email programs should set the (Default) value of the *CanonicalName* subkey to the client's display name in the currently installed language.</span></span>

### <a name="registering-a-programs-icon"></a><span data-ttu-id="15794-186">Registrando o ícone de um programa</span><span class="sxs-lookup"><span data-stu-id="15794-186">Registering a Program's Icon</span></span>

> [!Note]  
> <span data-ttu-id="15794-187">Esta seção não se aplica ao Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="15794-187">This section does not apply to Windows 2000.</span></span>

 

<span data-ttu-id="15794-188">Por padrão, a seção superior do menu **Iniciar** do Windows XP e do Windows Vista contém ícones de **Internet** e **email** .</span><span class="sxs-lookup"><span data-stu-id="15794-188">By default, the upper section of the Windows XP and Windows Vista **Start** menu contains **Internet** and **E-mail** icons.</span></span> <span data-ttu-id="15794-189">Esses ícones não estão presentes no Windows 7 e versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="15794-189">These icons are not present in Windows 7 and later.</span></span> <span data-ttu-id="15794-190">Para clientes de navegador e email, quando um programa é atribuído como o padrão para seu tipo de cliente, o ícone registrado desse programa é exibido para essas entradas do menu **Iniciar** .</span><span class="sxs-lookup"><span data-stu-id="15794-190">For browser and email clients, when a program is assigned as the default for their client type, that program's registered icon is displayed for those **Start** menu entries.</span></span>

<span data-ttu-id="15794-191">O registro do ícone de um programa é obrigatório para clientes de navegador e email.</span><span class="sxs-lookup"><span data-stu-id="15794-191">Registering a program's icon is mandatory for browser and email clients.</span></span> <span data-ttu-id="15794-192">O registro de um ícone para a reprodução de mídia, mensagens instantâneas ou máquina virtual para tipos de cliente Java é opcional, e os ícones registrados para esses tipos de cliente não são usados no momento pelo Windows e não são exibidos na seção superior dos menus **Iniciar** do Windows XP ou do Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="15794-192">Registering an icon for the media playback, instant messaging, or virtual machine for Java client types is optional, and registered icons for those client types are not currently used by Windows and are not displayed in the upper section of the Windows XP or Windows Vista **Start** menus.</span></span>

<span data-ttu-id="15794-193">Para registrar um ícone para um programa cliente, adicione uma subchave **DefaultIcon** com um valor padrão, conforme mostrado aqui.</span><span class="sxs-lookup"><span data-stu-id="15794-193">To register an icon for a client program, add a **DefaultIcon** subkey with a default value as shown here.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            CanonicalName
               DefaultIcon
                  (Default) = FilePath,IconIndex
```

<span data-ttu-id="15794-194">O valor de **FilePath** é o caminho completo para o arquivo que contém o ícone.</span><span class="sxs-lookup"><span data-stu-id="15794-194">The **FilePath** value is the full path to the file that contains the icon.</span></span> <span data-ttu-id="15794-195">Esse caminho não requer aspas, mesmo que contenha espaços.</span><span class="sxs-lookup"><span data-stu-id="15794-195">This path does not require quotation marks, even if it contains spaces.</span></span>

<span data-ttu-id="15794-196">O valor de **IconIndex** é interpretado da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="15794-196">The **IconIndex** value is interpreted as follows:</span></span>

-   <span data-ttu-id="15794-197">Se **IconIndex** for um número positivo, o número será usado como o índice da matriz *com base em zero* dos ícones armazenados no arquivo.</span><span class="sxs-lookup"><span data-stu-id="15794-197">If **IconIndex** is a positive number, the number is used as the index of the *zero-based* array of icons stored in the file.</span></span> <span data-ttu-id="15794-198">Por exemplo, se **IconIndex** for 1, o segundo ícone será carregado a partir do arquivo.</span><span class="sxs-lookup"><span data-stu-id="15794-198">For example, if **IconIndex** is 1, the second icon is loaded from the file.</span></span>
-   <span data-ttu-id="15794-199">Se **IconIndex** for um número negativo, o valor absoluto de **IconIndex** será usado como o identificador de recurso (em vez do índice) para o ícone.</span><span class="sxs-lookup"><span data-stu-id="15794-199">If **IconIndex** is a negative number, the absolute value of **IconIndex** is used as the resource identifier (rather than the index) for the icon.</span></span> <span data-ttu-id="15794-200">Por exemplo, se **IconIndex** for-3, o ícone cujo identificador de recurso é 3 será carregado a partir do arquivo.</span><span class="sxs-lookup"><span data-stu-id="15794-200">For example, if **IconIndex** is -3, the icon whose resource identifier is 3 is loaded from the file.</span></span>

<span data-ttu-id="15794-201">O exemplo a seguir mostra o registro de um navegador de exibição iluminada hipotética.</span><span class="sxs-lookup"><span data-stu-id="15794-201">The following example shows the registration of a hypothetical Lit View browser.</span></span> <span data-ttu-id="15794-202">O segundo ícone armazenado no arquivo de Litview.exe é usado como o padrão.</span><span class="sxs-lookup"><span data-stu-id="15794-202">The second icon stored in the Litview.exe file is used as the default.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         StartMenuInternet
            LITVIEW.EXE
               DefaultIcon
                  (Default) = C:\Program Files\LitwareInc\Litview.exe,1
```

### <a name="registering-an-open-verb"></a><span data-ttu-id="15794-203">Registrando um verbo aberto</span><span class="sxs-lookup"><span data-stu-id="15794-203">Registering an Open Verb</span></span>

> [!Note]  
> <span data-ttu-id="15794-204">Esta seção não se aplica ao Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="15794-204">This section does not apply to Windows 2000.</span></span> <span data-ttu-id="15794-205">A etapa a seguir é necessária apenas para clientes de navegador e de email.</span><span class="sxs-lookup"><span data-stu-id="15794-205">The following step is necessary only for browser and email clients.</span></span>

 

<span data-ttu-id="15794-206">Suponha que um usuário tenha selecionado seu programa como a Internet ou o programa de email padrão.</span><span class="sxs-lookup"><span data-stu-id="15794-206">Assume that a user has selected your program as the default Internet or email program.</span></span> <span data-ttu-id="15794-207">Esse usuário clica no ícone **Internet** ou **email** no menu **Iniciar** do Windows XP ou do Windows Vista para abrir o programa.</span><span class="sxs-lookup"><span data-stu-id="15794-207">That user clicks the **Internet** or **E-mail** icon in the Windows XP or Windows Vista **Start** menu to open the program.</span></span> <span data-ttu-id="15794-208">Nesse ponto, a linha de comando registrada conforme mostrado aqui é executada.</span><span class="sxs-lookup"><span data-stu-id="15794-208">At that point, the command line registered as shown here is executed.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            CanonicalName
               shell
                  open
                     command
                        (Default) = command line
```

<span data-ttu-id="15794-209">A linha de comando deve especificar um caminho absoluto totalmente qualificado para o arquivo, seguido por opções de linha de comando opcionais.</span><span class="sxs-lookup"><span data-stu-id="15794-209">The command line must specify a fully qualified absolute path to the file, followed by optional command-line options.</span></span> <span data-ttu-id="15794-210">Se o tipo de entrada for REG \_ Expand \_ sz, as variáveis de ambiente poderão ser usadas no caminho.</span><span class="sxs-lookup"><span data-stu-id="15794-210">If the entry type is REG\_EXPAND\_SZ, environment variables can be used in the path.</span></span> <span data-ttu-id="15794-211">Use aspas adequadamente para garantir que os espaços na linha de comando não sejam interpretados erroneamente.</span><span class="sxs-lookup"><span data-stu-id="15794-211">Use quotation marks appropriately to ensure that spaces in the command line are not misinterpreted.</span></span> <span data-ttu-id="15794-212">A linha de comando deve executar o programa com os padrões apropriados.</span><span class="sxs-lookup"><span data-stu-id="15794-212">The command line should execute the program with appropriate defaults.</span></span> <span data-ttu-id="15794-213">Os navegadores geralmente assumem como padrão o home page do usuário.</span><span class="sxs-lookup"><span data-stu-id="15794-213">Browsers generally default to the user's home page.</span></span> <span data-ttu-id="15794-214">Os programas de email geralmente abrem a **caixa de entrada** do usuário.</span><span class="sxs-lookup"><span data-stu-id="15794-214">Email programs generally open the user's **Inbox**.</span></span>

<span data-ttu-id="15794-215">O exemplo a seguir mostra o registro de um `open` verbo para um navegador de exibição iluminada hipotética.</span><span class="sxs-lookup"><span data-stu-id="15794-215">The following example shows the registration of an `open` verb for a hypothetical Lit View browser.</span></span> <span data-ttu-id="15794-216">Ele não especifica opções de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="15794-216">It specifies no command-line options.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         StartMenuInternet
            LITVIEW.EXE
               shell
                  open
                     command
                        (Default) = "C:\Program Files\LitwareInc\Litview.exe"
```

<span data-ttu-id="15794-217">Observe que, nesse valor, as aspas são colocadas em volta do caminho porque contêm espaços inseridos.</span><span class="sxs-lookup"><span data-stu-id="15794-217">Note that in this value, quotation marks are placed around the path because it contains embedded spaces.</span></span> <span data-ttu-id="15794-218">Omitir essas aspas pode fazer com que a linha de comando seja interpretada erroneamente.</span><span class="sxs-lookup"><span data-stu-id="15794-218">Omitting these quotation marks could cause the command line to be misinterpreted.</span></span>

### <a name="registering-installation-information"></a><span data-ttu-id="15794-219">Registrando informações de instalação</span><span class="sxs-lookup"><span data-stu-id="15794-219">Registering Installation Information</span></span>

> [!Note]  
> <span data-ttu-id="15794-220">Esta seção não se aplica ao Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="15794-220">This section does not apply to Windows Server 2003.</span></span>

 

-   [<span data-ttu-id="15794-221">O comando reinstalar</span><span class="sxs-lookup"><span data-stu-id="15794-221">The Reinstall Command</span></span>](#the-reinstall-command)
-   [<span data-ttu-id="15794-222">O comando Ocultar ícones</span><span class="sxs-lookup"><span data-stu-id="15794-222">The Hide Icons Command</span></span>](#the-hide-icons-command)
-   [<span data-ttu-id="15794-223">O comando mostrar ícones</span><span class="sxs-lookup"><span data-stu-id="15794-223">The Show Icons Command</span></span>](#the-show-icons-command)
-   [<span data-ttu-id="15794-224">Configuração do programa de grupo</span><span class="sxs-lookup"><span data-stu-id="15794-224">Group Program Configuration</span></span>](#group-program-configuration)
-   [<span data-ttu-id="15794-225">Exemplo de registro do navegador</span><span class="sxs-lookup"><span data-stu-id="15794-225">Browser Registration Example</span></span>](#browser-registration-example)

<span data-ttu-id="15794-226">O recurso pelo qual o usuário seleciona programas padrão por máquina é nomeado e acessado conforme mostrado na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="15794-226">The feature by which the user selects per-machine default programs is named and accessed as shown in the following table.</span></span> <span data-ttu-id="15794-227">(O Windows Vista introduziu um novo recurso, **definiu os programas padrão**, pelos quais um usuário pode definir padrões por usuário.)</span><span class="sxs-lookup"><span data-stu-id="15794-227">(Windows Vista introduced a new feature, **Set your default programs**, by which a user can set per-user defaults.)</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="15794-228">Sistema Operacional</span><span class="sxs-lookup"><span data-stu-id="15794-228">Operating System</span></span></th>
<th><span data-ttu-id="15794-229">Título</span><span class="sxs-lookup"><span data-stu-id="15794-229">Title</span></span></th>
<th><span data-ttu-id="15794-230">Local de acesso</span><span class="sxs-lookup"><span data-stu-id="15794-230">Access Location</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="15794-231">Windows 7</span><span class="sxs-lookup"><span data-stu-id="15794-231">Windows 7</span></span></td>
<td><span data-ttu-id="15794-232">Definir o acesso do programa e padrões do computador</span><span class="sxs-lookup"><span data-stu-id="15794-232">Set Program Access and Computer Defaults</span></span></td>
<td><ul>
<li><span data-ttu-id="15794-233">Opção de <strong>programas padrão</strong> do menu <strong>Iniciar</strong></span><span class="sxs-lookup"><span data-stu-id="15794-233"><strong>Start</strong> menu <strong>Default Programs</strong> option</span></span></li>
<li><span data-ttu-id="15794-234"><strong>Programas padrão</strong> Item do painel de controle</span><span class="sxs-lookup"><span data-stu-id="15794-234"><strong>Default Programs</strong> Control Panel item</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="15794-235">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="15794-235">Windows Vista</span></span></td>
<td><span data-ttu-id="15794-236">Definir o acesso do programa e padrões do computador</span><span class="sxs-lookup"><span data-stu-id="15794-236">Set Program Access and Computer Defaults</span></span></td>
<td><ul>
<li><span data-ttu-id="15794-237">Opção de <strong>programas padrão</strong> do menu <strong>Iniciar</strong></span><span class="sxs-lookup"><span data-stu-id="15794-237"><strong>Start</strong> menu <strong>Default Programs</strong> option</span></span></li>
<li><span data-ttu-id="15794-238"><strong>Programas padrão</strong> Item do painel de controle</span><span class="sxs-lookup"><span data-stu-id="15794-238"><strong>Default Programs</strong> Control Panel item</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="15794-239">Windows XP SP2</span><span class="sxs-lookup"><span data-stu-id="15794-239">Windows XP SP2</span></span></td>
<td><span data-ttu-id="15794-240">Definir acesso e padrões do programa</span><span class="sxs-lookup"><span data-stu-id="15794-240">Set Program Access and Defaults</span></span></td>
<td><ul>
<li><span data-ttu-id="15794-241">Menu <strong>Iniciar</strong></span><span class="sxs-lookup"><span data-stu-id="15794-241"><strong>Start</strong> menu</span></span></li>
<li><span data-ttu-id="15794-242"><strong>Adicionar ou remover programas</strong> Item do painel de controle</span><span class="sxs-lookup"><span data-stu-id="15794-242"><strong>Add or Remove Programs</strong> Control Panel item</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="15794-243">Windows XP SP1</span><span class="sxs-lookup"><span data-stu-id="15794-243">Windows XP SP1</span></span></td>
<td><span data-ttu-id="15794-244">Configurar programas</span><span class="sxs-lookup"><span data-stu-id="15794-244">Configure Programs</span></span></td>
<td><ul>
<li><span data-ttu-id="15794-245"><strong>Adicionar ou remover programas</strong> Item do painel de controle</span><span class="sxs-lookup"><span data-stu-id="15794-245"><strong>Add or Remove Programs</strong> Control Panel item</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="15794-246">Para simplificar, este tópico usa o título do Windows 7 do recurso.</span><span class="sxs-lookup"><span data-stu-id="15794-246">For simplicity, this topic uses the Windows 7 title of the feature.</span></span> <span data-ttu-id="15794-247">Todas as versões do recurso são conhecidas como SPAD.</span><span class="sxs-lookup"><span data-stu-id="15794-247">All versions of the feature are popularly referred to as SPAD.</span></span>

> [!Note]  
> <span data-ttu-id="15794-248">Se você estiver executando o Windows 2000 ou o Windows XP, deverá ter pelo menos o Windows 2000 SP3 ou o Windows XP SP1 instalado para ver a página **Definir acesso e padrões do programa** .</span><span class="sxs-lookup"><span data-stu-id="15794-248">If you are running Windows 2000 or Windows XP, you must have at least Windows 2000 SP3 or Windows XP SP1 installed to see the **Set Program Access and Defaults** page.</span></span> <span data-ttu-id="15794-249">No Windows Vista e posterior, o acesso à página **definir padrões de acesso a programas e computadores** requer privilégios de administrador.</span><span class="sxs-lookup"><span data-stu-id="15794-249">In Windows Vista and later, access to the **Set Program Access and Computer Defaults** page requires Administrator privileges.</span></span> <span data-ttu-id="15794-250">Por esse motivo, os desenvolvedores são incentivados a se registrarem no item definir o painel de controle de [programas padrão](default-programs.md) para que qualquer usuário possa gerenciar os padrões do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="15794-250">For this reason, developers are encouraged to register for the [Set your default programs](default-programs.md) Control Panel item so that any user can manage application defaults.</span></span>

 

<span data-ttu-id="15794-251">A árvore de registro a seguir mostra a variedade de informações que devem ser registradas na chave **InstallInfo** do programa para que o programa apareça na página **Definir acesso do programa e padrões do computador** como uma opção para seu tipo de cliente.</span><span class="sxs-lookup"><span data-stu-id="15794-251">The following registry tree shows the variety of information that must be registered in the program's **InstallInfo** key in order for the program to appear on the **Set Program Access and Computer Defaults** page as an option for its client type.</span></span> <span data-ttu-id="15794-252">Cada um desses valores é discutido em detalhes nas seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="15794-252">Each of these values is discussed in detail in the following sections.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            CanonicalName
               InstallInfo
                  HideIconsCommand = command line
                  ReinstallCommand = command line
                  ShowIconsCommand = command line
                  IconsVisible = 1
```

<span data-ttu-id="15794-253">A linha de comando deve especificar um caminho absoluto totalmente qualificado para o arquivo, seguido por opções de linha de comando opcionais.</span><span class="sxs-lookup"><span data-stu-id="15794-253">The command line must specify a fully qualified absolute path to the file, followed by optional command-line options.</span></span> <span data-ttu-id="15794-254">Use aspas adequadamente para garantir que os espaços na linha de comando não sejam interpretados erroneamente.</span><span class="sxs-lookup"><span data-stu-id="15794-254">Use quotation marks appropriately to ensure that spaces in the command line are not misinterpreted.</span></span>

### <a name="the-reinstall-command"></a><span data-ttu-id="15794-255">O comando reinstalar</span><span class="sxs-lookup"><span data-stu-id="15794-255">The Reinstall Command</span></span>

<span data-ttu-id="15794-256">A linha de comando REINSTALL declarada no valor ReinstallCommand é executada quando o usuário usa a página **Definir acesso do programa e padrões do computador** para selecionar seu programa como o padrão para seu tipo de cliente.</span><span class="sxs-lookup"><span data-stu-id="15794-256">The reinstall command line declared in the ReinstallCommand value is executed when the user uses the **Set Program Access and Computer Defaults** page to select your program as the default for its client type.</span></span> <span data-ttu-id="15794-257">No Windows Vista e posterior, o acesso a esta página requer um nível de privilégio de administrador.</span><span class="sxs-lookup"><span data-stu-id="15794-257">In Windows Vista and later, access to this page requires an Administrator privilege level.</span></span> <span data-ttu-id="15794-258">No Windows 8, se você registrou seu aplicativo usando o mesmo nome para **definir o acesso do programa e os padrões do computador** e os **programas padrão**, os padrões especificados em **programas padrão** para esse aplicativo serão aplicados ao usuário atual, bem como à execução do comando reinstalar.</span><span class="sxs-lookup"><span data-stu-id="15794-258">In Windows 8, if you have registered your application using the same name for both **Set Program Access and Computer Defaults** and **Default Programs**, the defaults specified in **Default Programs** for that application will be applied for the current user as well as running the reinstall command.</span></span>

<span data-ttu-id="15794-259">O programa iniciado pela linha de comando de reinstalação deve associar o aplicativo ao conjunto completo de tipos de [arquivo](fa-intro.md) e [protocolo](/previous-versions//aa767743(v=vs.85)) que o aplicativo pode manipular.</span><span class="sxs-lookup"><span data-stu-id="15794-259">The program launched by the reinstall command line must associate the application with the complete set of [file](fa-intro.md) and [protocol](/previous-versions//aa767743(v=vs.85)) types the application can handle.</span></span> <span data-ttu-id="15794-260">Todos os aplicativos devem estabelecer a capacidade do manipulador no comando reinstalar.</span><span class="sxs-lookup"><span data-stu-id="15794-260">All applications must establish handler capability in the reinstall command.</span></span> <span data-ttu-id="15794-261">Os aplicativos podem usar o comando reinstalar para registrar o recurso, bem como, opcionalmente, estabelecer o status padrão.</span><span class="sxs-lookup"><span data-stu-id="15794-261">Applications can use the reinstall command to register capability as well as optionally establish default status.</span></span> <span data-ttu-id="15794-262">Quando um aplicativo opta por implementar o status do manipulador de capacidade e padrão no comando reinstalar, ele também deve restabelecer os links ou atalhos visíveis desejados.</span><span class="sxs-lookup"><span data-stu-id="15794-262">When an application chooses to implement both capability and default handler status in the reinstall command, it should also reinstate any visible links or shortcuts desired.</span></span> <span data-ttu-id="15794-263">Os pontos de entrada visíveis a maioria dos aplicativos escolhem são listados no [comando Ocultar ícones](#the-hide-icons-command).</span><span class="sxs-lookup"><span data-stu-id="15794-263">The visible entry points most applications choose are listed in [The Hide Icons Command](#the-hide-icons-command).</span></span>

> [!Note]  
> <span data-ttu-id="15794-264">É altamente recomendável que os aplicativos implementem o recurso de manipulação no comando REINSTALL.</span><span class="sxs-lookup"><span data-stu-id="15794-264">It is highly recommended that applications implement handling capability in the reinstall command.</span></span>

 

<span data-ttu-id="15794-265">Depois que o processo de reinstalação for concluído, o programa iniciado pela linha de comando de reinstalação deverá sair.</span><span class="sxs-lookup"><span data-stu-id="15794-265">Once the reinstall process is complete, the program launched by the reinstall command line should exit.</span></span> <span data-ttu-id="15794-266">Ele não deve iniciar o programa correspondente; Ele deve meramente registrar os padrões.</span><span class="sxs-lookup"><span data-stu-id="15794-266">It should not launch the corresponding program; it should merely register defaults.</span></span> <span data-ttu-id="15794-267">Por exemplo, o comando reinstalar de um navegador não deve abrir o home page do usuário.</span><span class="sxs-lookup"><span data-stu-id="15794-267">For example, the reinstall command for a browser should not open the user's home page.</span></span>

> [!Note]  
> <span data-ttu-id="15794-268">Para clientes de navegador e de email no Windows XP e no Windows Vista, os aplicativos que optam por estabelecer o recurso de manipulação e o status padrão no comando reinstalar devem se registrar no ícone correspondente na parte superior do menu iniciar.</span><span class="sxs-lookup"><span data-stu-id="15794-268">For browser and email clients in Windows XP and Windows Vista, applications that choose to establish both handling capability and default status in the reinstall command should register for the corresponding icon at the top of the Start menu.</span></span> <span data-ttu-id="15794-269">Consulte o [registro do menu iniciar](#start-menu-registration) para obter informações adicionais.</span><span class="sxs-lookup"><span data-stu-id="15794-269">See [Start Menu Registration](#start-menu-registration) for additional information.</span></span>

 

### <a name="the-hide-icons-command"></a><span data-ttu-id="15794-270">O comando Ocultar ícones</span><span class="sxs-lookup"><span data-stu-id="15794-270">The Hide Icons Command</span></span>

<span data-ttu-id="15794-271">A linha de comando declarada no valor HideIconsCommand é executada quando o usuário limpa a caixa **habilitar acesso a este programa** na página **Definir acesso do programa e padrões do computador** .</span><span class="sxs-lookup"><span data-stu-id="15794-271">The command line declared in the HideIconsCommand value is executed when the user clears the **Enable access to this program** box in the **Set Program Access and Computer Defaults** page.</span></span> <span data-ttu-id="15794-272">Essa linha de comando deve ocultar todos os pontos de acesso do programa visíveis na interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="15794-272">This command line must hide all of your program's access points that are visible in the user interface.</span></span> <span data-ttu-id="15794-273">As diretrizes específicas são remover atalhos e ícones dos seguintes locais:</span><span class="sxs-lookup"><span data-stu-id="15794-273">The specific guidelines are to remove shortcuts and icons from the following locations:</span></span>

-   <span data-ttu-id="15794-274">Ícones da área de trabalho</span><span class="sxs-lookup"><span data-stu-id="15794-274">Desktop icons</span></span>
-   <span data-ttu-id="15794-275">Links do menu Iniciar, incluindo o grupo de **inicialização**</span><span class="sxs-lookup"><span data-stu-id="15794-275">Start menu links, including the **Startup** group</span></span>
-   <span data-ttu-id="15794-276">Links da barra de início rápido</span><span class="sxs-lookup"><span data-stu-id="15794-276">Quick Launch bar links</span></span>
-   <span data-ttu-id="15794-277">Área de notificação</span><span class="sxs-lookup"><span data-stu-id="15794-277">Notification area</span></span>
-   <span data-ttu-id="15794-278">Menus de atalho</span><span class="sxs-lookup"><span data-stu-id="15794-278">Shortcut menus</span></span>
-   <span data-ttu-id="15794-279">Faixa de tarefas da pasta</span><span class="sxs-lookup"><span data-stu-id="15794-279">Folder task band</span></span>

<span data-ttu-id="15794-280">Essa linha de comando também deve impedir invocações automáticas do programa, como as especificadas na chave do registro de **execução** .</span><span class="sxs-lookup"><span data-stu-id="15794-280">This command line must also prevent automatic invocations of the program, such as those specified in the **Run** registry key.</span></span> <span data-ttu-id="15794-281">Os fornecedores são incentivados a implementar essas diretrizes no retorno de chamada ocultar acesso do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="15794-281">Vendors are encouraged to implement these guidelines in the application's Hide Access callback.</span></span>

<span data-ttu-id="15794-282">Você não precisa ceder o registro (funcionalidade do aplicativo) dos tipos de arquivo quando os ícones estão ocultos.</span><span class="sxs-lookup"><span data-stu-id="15794-282">You do not need to relinquish registration (application capability) of file types when icons are hidden.</span></span> <span data-ttu-id="15794-283">Você também não precisa ceder o status padrão do aplicativo para tipos de arquivo e protocolo.</span><span class="sxs-lookup"><span data-stu-id="15794-283">You also do not need to relinquish the application's default status for file and protocol types.</span></span> <span data-ttu-id="15794-284">Isso pode levar a uma experiência de usuário inadequada quando esses tipos são encontrados na interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="15794-284">Doing so can lead to a bad user experience when these types are encountered in the UI.</span></span>

<span data-ttu-id="15794-285">Depois de ocultar os ícones com êxito, você deve atualizar o valor do registro IconsVisible para 0, conforme mostrado:</span><span class="sxs-lookup"><span data-stu-id="15794-285">After successfully hiding icons, you must update the IconsVisible registry value to 0 as shown:</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            CanonicalName
               InstallInfo
                  IconsVisible = 0
```

<span data-ttu-id="15794-286">A entrada IconsVisible é do tipo **reg \_ DWORD**.</span><span class="sxs-lookup"><span data-stu-id="15794-286">The IconsVisible entry is of type **REG\_DWORD**.</span></span>

### <a name="an-alternate-hide-icons-method-in-spad"></a><span data-ttu-id="15794-287">Um método alternativo para ocultar ícones em SPAD</span><span class="sxs-lookup"><span data-stu-id="15794-287">An Alternate Hide Icons Method in SPAD</span></span>

<span data-ttu-id="15794-288">Para alguns aplicativos herdados, uma implementação completa do acesso de ocultar pode não ser prática.</span><span class="sxs-lookup"><span data-stu-id="15794-288">For some legacy applications, a full implementation of Hide Access may not be practical.</span></span> <span data-ttu-id="15794-289">Um método alternativo que alcança o mesmo efeito é desinstalar o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="15794-289">An alternative method that achieves the same effect is to uninstall the application.</span></span> <span data-ttu-id="15794-290">A seção a seguir mostra o comportamento de exemplo e o código de exemplo para implementar essa alternativa.</span><span class="sxs-lookup"><span data-stu-id="15794-290">The section below shows example behavior and sample code to implement this alternative.</span></span> <span data-ttu-id="15794-291">Em geral, os ISVs (fornecedores independentes de software) devem evitar essa alternativa, pois ela irá:</span><span class="sxs-lookup"><span data-stu-id="15794-291">In general, independent software vendors (ISVs) should avoid this alternative since it will:</span></span>

-   <span data-ttu-id="15794-292">Desinstale completamente o aplicativo do sistema.</span><span class="sxs-lookup"><span data-stu-id="15794-292">Uninstall the application completely from the system.</span></span>
-   <span data-ttu-id="15794-293">Remova os padrões selecionados anteriormente.</span><span class="sxs-lookup"><span data-stu-id="15794-293">Remove previously selected defaults.</span></span>
-   <span data-ttu-id="15794-294">Não deixe a opção de interface do usuário para reinstalar o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="15794-294">Leave no UI option to reinstall the application.</span></span>
-   <span data-ttu-id="15794-295">Tornar o recurso habilitar acesso não mais disponível, pois uma desinstalação remove o aplicativo completamente do SPAD.</span><span class="sxs-lookup"><span data-stu-id="15794-295">Make the enable access feature no longer available, since an uninstallation removes the application completely from SPAD.</span></span>

<span data-ttu-id="15794-296">A experiência do usuário recomendada é a seguinte:</span><span class="sxs-lookup"><span data-stu-id="15794-296">The recommended user experience is as follows:</span></span>

-   <span data-ttu-id="15794-297">Quando o usuário desmarca a caixa de seleção **habilitar o acesso a este programa** no SPAD, a interface do usuário a seguir é apresentada.</span><span class="sxs-lookup"><span data-stu-id="15794-297">When the user unchecks the **Enable access to this program** box in SPAD, the following UI is presented.</span></span>

    ![caixa de diálogo sobre como ocultar o acesso ao programa](images/hideaccessvista.png)

-   <span data-ttu-id="15794-299">Quando o usuário seleciona **OK**, o item do painel de controle **programas e recursos** é iniciado para permitir que o usuário desinstale o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="15794-299">When the user selects **OK**, the **Programs and Features** Control Panel item launches to allow the user to uninstall the application.</span></span>
-   <span data-ttu-id="15794-300">Os usuários do Windows XP devem ser apresentados com essa caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="15794-300">Windows XP users should be presented with this dialog box.</span></span>

    ![caixa de diálogo equivalente do Windows XP](images/hideaccessxp.png)

-   <span data-ttu-id="15794-302">Quando o usuário do Windows XP seleciona **OK**, o item **Adicionar ou remover programas** do painel de controle é iniciado para permitir que o usuário desinstale o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="15794-302">When the Windows XP user selects **OK**, the **Add or Remove Programs** Control Panel item launches to allow the user to uninstall the application.</span></span>

<span data-ttu-id="15794-303">O código a seguir fornece uma implementação reutilizável para o recurso ocultar acesso, conforme descrito acima.</span><span class="sxs-lookup"><span data-stu-id="15794-303">The following code provides a reusable implementation for the Hide Access feature as outlined above.</span></span> <span data-ttu-id="15794-304">Ele pode ser usado no Windows XP, no Windows Vista e no Windows 7.</span><span class="sxs-lookup"><span data-stu-id="15794-304">It can be used on Windows XP, Windows Vista, and Windows 7.</span></span>


```
#include <windows.h>
#include <shlwapi.h>
#include <strsafe.h>

PCWSTR c_pszMessage1 = L"To hide access to this program, you need to uninstall it by ";
PCWSTR c_pszMessage2 = L"using\n%s in Control Panel.\n\nWould you like to start %s?";
PCWSTR c_pszApplicationName  = L"Sample App";

int _tmain(int argc, WCHAR* argv[])
{
    OSVERSIONINFO version;
    version.dwOSVersionInfoSize = sizeof(version);

    if (GetVersionEx(&version))
    {
        PCWSTR pszCPLName = NULL;

        if (version.dwMajorVersion >= 6)
        {
            // Windows Vista and later
            pszCPLName = L"Programs and Features";
        }
        else if (version.dwMajorVersion == 5 &&
                 version.dwMinorVersion == 1)
        {
            // Windows XP
            pszCPLName = L"Add/Remove Programs";
        }

        if (pszCPLName != NULL)
        {
            WCHAR szMessage[256], szScratch[256];
            if (SUCCEEDED(StringCchPrintf(szScratch, 
                                          ARRAYSIZE(szScratch), 
                                          c_pszMessage2, 
                                          pszCPLName, 
                                          pszCPLName)))
            {
                if (SUCCEEDED(StringCchCopy(szMessage, 
                                            ARRAYSIZE(szMessage), 
                                            c_pszMessage1)))
                {
                    if (SUCCEEDED(StringCchCat(szMessage, 
                                               ARRAYSIZE(szMessage), 
                                               szScratch)))
                    {
                        if (IDOK == MessageBox(NULL, 
                                               szMessage, 
                                               c_pszApplicationName, 
                                               MB_OKCANCEL))
                        {
                            ShellExecute(NULL, 
                                         NULL, 
                                         L"appwiz.cpl", 
                                         NULL, 
                                         NULL, 
                                         SW_SHOWNORMAL);
                        }
                    }
                }
            }
        }
    }
    return 0;
}
```



### <a name="the-show-icons-command"></a><span data-ttu-id="15794-305">O comando mostrar ícones</span><span class="sxs-lookup"><span data-stu-id="15794-305">The Show Icons Command</span></span>

<span data-ttu-id="15794-306">A linha de comando declarada na entrada ShowIconsCommand é executada quando o usuário marca a caixa **habilitar acesso a este programa** na página **Definir acesso do programa e padrões do computador** .</span><span class="sxs-lookup"><span data-stu-id="15794-306">The command line declared in the ShowIconsCommand entry is executed when the user checks the **Enable access to this program** box in the **Set Program Access and Computer Defaults** page.</span></span> <span data-ttu-id="15794-307">Essa linha de comando pode restaurar os pontos de acesso do programa, incluindo aqueles no menu **Iniciar** , na área de trabalho e no grupo de **inicialização** , bem como invocações automáticas normais, como as especificadas na chave do registro de **execução** .</span><span class="sxs-lookup"><span data-stu-id="15794-307">This command line may restore your program's access points, including those in the **Start** menu, on the desktop, and in the **Startup** group, as well as normal automatic invocations, such as those specified in the **Run** registry key.</span></span> <span data-ttu-id="15794-308">Os pontos de acesso visíveis de interesse para a maioria dos aplicativos são listados no [comando Ocultar ícones](#the-hide-icons-command).</span><span class="sxs-lookup"><span data-stu-id="15794-308">The visible access points of interest to most applications are listed in [The Hide Icons Command](#the-hide-icons-command).</span></span> <span data-ttu-id="15794-309">O aplicativo não deve alterar os padrões por usuário; Essa alteração deve ser feita pelo usuário por meio de **programas padrão**.</span><span class="sxs-lookup"><span data-stu-id="15794-309">The application should not change per-user defaults; that change should be done by the user through **Default Programs**.</span></span>

<span data-ttu-id="15794-310">Depois de mostrar os ícones com êxito, você deve atualizar o valor do registro IconsVisible para 1, conforme mostrado:</span><span class="sxs-lookup"><span data-stu-id="15794-310">After successfully showing your icons, you must update the IconsVisible registry value to 1 as shown:</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            CanonicalName
               InstallInfo
                  IconsVisible = 1
```

<span data-ttu-id="15794-311">Observe que, se você tiver usado a entrada HideIconsCommand para solicitar uma desinstalação do aplicativo, a entrada ShowIconsCommand não será usada.</span><span class="sxs-lookup"><span data-stu-id="15794-311">Note that if you have used the HideIconsCommand entry to prompt an uninstall of the application, the ShowIconsCommand entry is of no use.</span></span> <span data-ttu-id="15794-312">Ele deve ser removido do registro com o restante das informações do aplicativo durante o processo de desinstalação.</span><span class="sxs-lookup"><span data-stu-id="15794-312">It should be removed from the registry with the rest of the application's information during the uninstall process.</span></span>

### <a name="group-program-configuration"></a><span data-ttu-id="15794-313">Configuração do programa de grupo</span><span class="sxs-lookup"><span data-stu-id="15794-313">Group Program Configuration</span></span>

> [!Note]  
> <span data-ttu-id="15794-314">Esta seção não se aplica ao Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="15794-314">This section does not apply to Windows 2000.</span></span>

 

<span data-ttu-id="15794-315">Como parte da preparação do sistema, um OEM pode estabelecer uma configuração que oculta os pontos de acesso do navegador da Microsoft, email, reprodução de mídia, mensagens instantâneas ou máquina virtual para programas cliente Java e especifica seus próprios programas padrão.</span><span class="sxs-lookup"><span data-stu-id="15794-315">As part of system preparation, an OEM can establish a configuration that hides access points for the Microsoft browser, email, media playback, instant messaging, or virtual machine for Java client programs and specifies their own default programs.</span></span> <span data-ttu-id="15794-316">Os OEMs podem permitir que os usuários redefinam seus computadores a qualquer momento nessa configuração padrão definindo os seguintes valores de registro.</span><span class="sxs-lookup"><span data-stu-id="15794-316">OEMs can enable users to reset their computers at any time to this default configuration by setting the following registry values.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            CanonicalName
               InstallInfo
                  OEMShowIcons = 1
                  OEMDefault = 1
```

<span data-ttu-id="15794-317">Se essas chaves estiverem definidas, os usuários poderão restaurar a configuração do OEM selecionando a opção **fabricante do computador** na página **definir padrões de acesso e computador do programa** .</span><span class="sxs-lookup"><span data-stu-id="15794-317">If these keys are set, users can restore the OEM configuration by selecting the **Computer Manufacturer** option on the **Set Program Access and Computer Defaults** page.</span></span> <span data-ttu-id="15794-318">Se essas chaves não estiverem definidas, a opção **fabricante do computador** não será mostrada.</span><span class="sxs-lookup"><span data-stu-id="15794-318">If these keys are not set, the **Computer Manufacturer** option is not shown.</span></span>

<span data-ttu-id="15794-319">A entrada **OEMShowIcons** , se presente, define o estado de exibição do ícone para o cliente especificado que será aplicado se o usuário selecionar **fabricante do computador**.</span><span class="sxs-lookup"><span data-stu-id="15794-319">The **OEMShowIcons** entry, if present, sets the icon show state for the specified client that is applied if the user selects **Computer Manufacturer**.</span></span> <span data-ttu-id="15794-320">Um valor de 1 faz com que os ícones sejam mostrados e um valor de 0 faz com que os ícones não sejam mostrados.</span><span class="sxs-lookup"><span data-stu-id="15794-320">A value of 1 causes icons to be shown, and a value of 0 causes icons to not be shown.</span></span> <span data-ttu-id="15794-321">Se **OEMShowIcons** estiver ausente, selecionar **fabricante do computador** não terá nenhum efeito na configuração mostrar ícone.</span><span class="sxs-lookup"><span data-stu-id="15794-321">If **OEMShowIcons** is absent, selecting **Computer Manufacturer** has no effect on the icon show setting.</span></span> <span data-ttu-id="15794-322">**OEMShowIcons** é do tipo **reg \_ DWORD**.</span><span class="sxs-lookup"><span data-stu-id="15794-322">**OEMShowIcons** is of type **REG\_DWORD**.</span></span>

<span data-ttu-id="15794-323">A entrada **OEMDefault** , se presente e definida como 1, estabelece a preferência de OEM para o cliente padrão do tipo indicado.</span><span class="sxs-lookup"><span data-stu-id="15794-323">The **OEMDefault** entry, if present and set to 1, establishes the OEM preference for the default client of the indicated type.</span></span> <span data-ttu-id="15794-324">Somente um cliente de um tipo específico pode ser marcado como o padrão OEM.</span><span class="sxs-lookup"><span data-stu-id="15794-324">Only one client of a particular type can be marked as the OEM default.</span></span> <span data-ttu-id="15794-325">Se mais de um registro de cliente contiver a entrada **OEMDefault** , todos serão ignorados e o cliente atual continuará sendo usado como cliente padrão.</span><span class="sxs-lookup"><span data-stu-id="15794-325">If more then one client's registration contains the **OEMDefault** entry, then all are ignored and the current client continues to be used as default client.</span></span> <span data-ttu-id="15794-326">Se a entrada **OEMDefault** não estiver presente ou estiver presente e definida como 0, esse cliente específico não será usado como o cliente padrão se o usuário selecionar o **fabricante do computador**.</span><span class="sxs-lookup"><span data-stu-id="15794-326">If the **OEMDefault** entry is not present or is present and set to 0, then that particular client is not used as the default client if the user selects **Computer Manufacturer**.</span></span> <span data-ttu-id="15794-327">**OEMDefault** é do tipo **reg \_ DWORD**.</span><span class="sxs-lookup"><span data-stu-id="15794-327">**OEMDefault** is of type **REG\_DWORD**.</span></span>

<span data-ttu-id="15794-328">Além da opção de redefinir seus computadores para a configuração padrão estabelecida pelo OEM, os usuários têm três outras opções de configuração:</span><span class="sxs-lookup"><span data-stu-id="15794-328">In addition to the option to reset their computers to the default configuration established by the OEM, users have three other configuration options:</span></span>

-   <span data-ttu-id="15794-329">Defina seu computador para uma configuração do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="15794-329">Set their computer to a Microsoft Windows configuration.</span></span> <span data-ttu-id="15794-330">Nesse caso, a página **definir padrões de acesso do programa e do computador** permite o acesso a todos os softwares da Microsoft e não Microsoft no computador registrado nas categorias de produto relevantes.</span><span class="sxs-lookup"><span data-stu-id="15794-330">In this case, the **Set Program Access and Computer Defaults** page enables access to all Microsoft and non-Microsoft software on the computer registered in the relevant product categories.</span></span> <span data-ttu-id="15794-331">Os programas do Microsoft Windows são selecionados como a opção padrão para cada categoria.</span><span class="sxs-lookup"><span data-stu-id="15794-331">Microsoft Windows programs are selected as the default option for each category.</span></span>
-   <span data-ttu-id="15794-332">Defina seu computador para uma configuração que não seja da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="15794-332">Set their computer to a non-Microsoft configuration.</span></span> <span data-ttu-id="15794-333">Essa configuração oculta os pontos de acesso (como o menu **Iniciar** ) para o Windows Internet Explorer, Windows Media Player, Windows Messenger e Microsoft Outlook Express.</span><span class="sxs-lookup"><span data-stu-id="15794-333">This configuration hides access points (such as the **Start** menu) to Windows Internet Explorer, Windows Media Player, Windows Messenger, and Microsoft Outlook Express.</span></span> <span data-ttu-id="15794-334">Ele permite o acesso ao software que não é da Microsoft no computador nessas categorias.</span><span class="sxs-lookup"><span data-stu-id="15794-334">It enables access to the non-Microsoft software on the computer in these categories.</span></span> <span data-ttu-id="15794-335">Além disso, se um programa que não é da Microsoft estiver disponível em uma categoria, ele será definido como o padrão para essa categoria.</span><span class="sxs-lookup"><span data-stu-id="15794-335">Furthermore, if a non-Microsoft program is available in a category, it is set as the default for that category.</span></span> <span data-ttu-id="15794-336">Se mais de um programa que não seja da Microsoft estiver disponível em uma categoria, será solicitado que o usuário escolha qual programa que não seja da Microsoft deve ser usado como padrão.</span><span class="sxs-lookup"><span data-stu-id="15794-336">If more than one non-Microsoft program is available in a category, the user is asked to choose which non-Microsoft program should be used as the default.</span></span>
-   <span data-ttu-id="15794-337">Estabeleça uma configuração personalizada.</span><span class="sxs-lookup"><span data-stu-id="15794-337">Establish a custom configuration.</span></span> <span data-ttu-id="15794-338">Os usuários fazem suas próprias seleções para habilitar ou remover o acesso, combinando programas da Microsoft e que não são da Microsoft como se comportam.</span><span class="sxs-lookup"><span data-stu-id="15794-338">Users make their own selections for enabling or removing access, mixing Microsoft and non-Microsoft programs as they see fit.</span></span> <span data-ttu-id="15794-339">Os usuários estabelecem opções padrão em uma base categoria a categoria.</span><span class="sxs-lookup"><span data-stu-id="15794-339">Users establish default options on a category-by-category basis.</span></span>

<span data-ttu-id="15794-340">Os usuários são livres para alterar qualquer uma dessas opções a qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="15794-340">Users are free to change any of these options at any time.</span></span>

### <a name="browser-registration-example"></a><span data-ttu-id="15794-341">Exemplo de registro do navegador</span><span class="sxs-lookup"><span data-stu-id="15794-341">Browser Registration Example</span></span>

<span data-ttu-id="15794-342">O exemplo a seguir mostra o registro de **InstallInfo** completo de um navegador de exibição iluminada fictícia.</span><span class="sxs-lookup"><span data-stu-id="15794-342">The following example shows the full **InstallInfo** registration for a fictional Lit View browser.</span></span> <span data-ttu-id="15794-343">Nesse caso, as opções de linha de comando permitem que o arquivo de Litview.exe execute quaisquer ações necessárias para cada valor.</span><span class="sxs-lookup"><span data-stu-id="15794-343">In this case the command line switches allow the Litview.exe file to perform whatever actions are necessary for each value.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         StartMenuInternet
            LITVIEW.EXE
               InstallInfo
                  ReinstallCommand = "C:\Program Files\LitwareInc\Litview.exe" /reinstall
                  HideIconsCommand = "C:\Program Files\LitwareInc\Litview.exe" /hideicons
                  ShowIconsCommand = "C:\Program Files\LitwareInc\Litview.exe" /showicons
                  IconsVisible = 1
```

<span data-ttu-id="15794-344">Observe que as aspas são colocadas em volta dos caminhos porque contêm espaços inseridos.</span><span class="sxs-lookup"><span data-stu-id="15794-344">Note that quotation marks are placed around the paths because they contain embedded spaces.</span></span>

## <a name="registration-elements-for-specific-client-types"></a><span data-ttu-id="15794-345">Elementos de registro para tipos de cliente específicos</span><span class="sxs-lookup"><span data-stu-id="15794-345">Registration Elements for Specific Client Types</span></span>

<span data-ttu-id="15794-346">As informações a seguir também podem ser encontradas nos recursos listados na seção Tópicos relacionados no final deste tópico.</span><span class="sxs-lookup"><span data-stu-id="15794-346">The following information also can be found in the resources listed in the Related Topics section at the end of this topic.</span></span>

-   [<span data-ttu-id="15794-347">Registro do menu iniciar</span><span class="sxs-lookup"><span data-stu-id="15794-347">Start Menu Registration</span></span>](#start-menu-registration)
-   [<span data-ttu-id="15794-348">Registro de cliente de email</span><span class="sxs-lookup"><span data-stu-id="15794-348">Mail Client Registration</span></span>](#mail-client-registration)

### <a name="start-menu-registration"></a><span data-ttu-id="15794-349">Registro do menu iniciar</span><span class="sxs-lookup"><span data-stu-id="15794-349">Start Menu Registration</span></span>

<span data-ttu-id="15794-350">No Windows XP, os aplicativos normalmente são registrados como padrões em todo o computador (**HKEY \_ local \_ Machine**) em vez de um usuário (**HKEY \_ Current \_ User**) Scope.</span><span class="sxs-lookup"><span data-stu-id="15794-350">Under Windows XP, applications typically registered defaults on a machine-wide (**HKEY\_LOCAL\_MACHINE**) rather than a user (**HKEY\_CURRENT\_USER**) scope.</span></span> <span data-ttu-id="15794-351">Com a introdução do Windows Vista do UAC (controle de conta de usuário), os aplicativos que solicitam os slots de **Internet** e de **email** no menu **Iniciar** devem implementar o comando reinstalar dentro do contexto de execução correto.</span><span class="sxs-lookup"><span data-stu-id="15794-351">With the Windows Vista introduction of the User Account Control (UAC), applications that claim the **Internet** and **E-mail** slots in the **Start** menu must implement the reinstall command within the correct execution context.</span></span>

> [!Note]  
> <span data-ttu-id="15794-352">O link de **email** do menu iniciar foi removido do Windows 7.</span><span class="sxs-lookup"><span data-stu-id="15794-352">The Start menu **E-mail** link has been removed as of Windows 7.</span></span> <span data-ttu-id="15794-353">No entanto, o registro discutido nesta seção ainda deve ser executado porque atribui o cliente MAPI padrão.</span><span class="sxs-lookup"><span data-stu-id="15794-353">However, the registration discussed in this section should still be performed because it assigns the default MAPI client.</span></span>

 

<span data-ttu-id="15794-354">Um usuário limitado no Windows XP, no Windows Vista ou no Windows 7 não pode acessar o SPAD.</span><span class="sxs-lookup"><span data-stu-id="15794-354">A limited user on Windows XP, Windows Vista, or Windows 7 cannot access SPAD.</span></span> <span data-ttu-id="15794-355">Por esse motivo, os desenvolvedores são incentivados a se registrarem no item definir o painel de controle de **programas padrão** para que qualquer usuário possa gerenciar padrões de aplicativos por usuário.</span><span class="sxs-lookup"><span data-stu-id="15794-355">For this reason, developers are encouraged to register for the **Set your default programs** Control Panel item so that any user can manage per-user application defaults.</span></span>

<span data-ttu-id="15794-356">As seleções feitas em SPAD só devem afetar as configurações por máquina.</span><span class="sxs-lookup"><span data-stu-id="15794-356">Selections made in SPAD should only affect per-machine settings.</span></span>

<span data-ttu-id="15794-357">Defina o valor do registro da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="15794-357">Set the registry value as follows.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            (Default) = CanonicalName
```

> [!Note]
> 
> <span data-ttu-id="15794-358">**As informações a seguir aplicam-se apenas ao Windows XP.**</span><span class="sxs-lookup"><span data-stu-id="15794-358">**The following information applies to Windows XP only.**</span></span>
> 
> <span data-ttu-id="15794-359">Se o registro do padrão no nível do computador em HKEY \_ local \_ Machine como mostrado acima for bem-sucedido, o aplicativo deverá excluir o valor atribuído à entrada padrão na seguinte subchave:</span><span class="sxs-lookup"><span data-stu-id="15794-359">If the registration of the computer-level default under HKEY\_LOCAL\_MACHINE as shown above is successful, the application should delete the value assigned to the Default entry under the following subkey:</span></span>
> 
> ```
> HKEY_CURRENT_USER
>    SOFTWARE
>       Clients
>          ClientTypeName
> ```
> 
> <span data-ttu-id="15794-360">Se o registro do padrão no nível do computador em HKEY \_ local \_ Machine, conforme mostrado acima falhar, geralmente porque o usuário não tem permissão de gravação para a subchave, o aplicativo deve definir o seguinte valor:</span><span class="sxs-lookup"><span data-stu-id="15794-360">If the registration of the computer-level default under HKEY\_LOCAL\_MACHINE as shown above fails, usually because the user does not have write permission to the subkey, the application should set the following value:</span></span>
> 
> ```
> HKEY_CURRENT_USER
>    SOFTWARE
>       Clients
>          ClientTypeName
>             (Default) = CanonicalName
> ```
> 
> <span data-ttu-id="15794-361">Isso registra o nome canônico somente para o usuário atual, não para todos os usuários.</span><span class="sxs-lookup"><span data-stu-id="15794-361">This registers the canonical name only for the current user, not for all users.</span></span>

 

<span data-ttu-id="15794-362">Depois de atualizar as chaves do registro, o programa deve difundir a mensagem do [**WM \_ SETTINGCHANGE**](../winmsg/wm-settingchange.md) com **wParam** = 0 e **lParam** apontando para a cadeia de caracteres terminada em nulo "clientes de software \\ \\ **ClientTypeName**" para notificar o sistema operacional que o cliente padrão alterou.</span><span class="sxs-lookup"><span data-stu-id="15794-362">After updating the registry keys, the program should broadcast the [**WM\_SETTINGCHANGE**](../winmsg/wm-settingchange.md) message with **wParam** = 0 and **lParam** pointing to the null-terminated string "Software\\Clients\\**ClientTypeName**" to notify the operating system that the default client has changed.</span></span>

### <a name="mail-client-registration"></a><span data-ttu-id="15794-363">Registro de cliente de email</span><span class="sxs-lookup"><span data-stu-id="15794-363">Mail Client Registration</span></span>

<span data-ttu-id="15794-364">Para um cliente de email, o programa precisa ter configurações registradas na chave **HKEY \_ classes \_ raiz** \\ **mailto** para atender a URLs que usam o `mailto` protocolo.</span><span class="sxs-lookup"><span data-stu-id="15794-364">For a mail client, the program needs to have registered settings under the **HKEY\_CLASSES\_ROOT**\\**mailto** key in order to service URLs that use the `mailto` protocol.</span></span> <span data-ttu-id="15794-365">Defina valores e chaves que espelham essas configurações na chave a seguir.</span><span class="sxs-lookup"><span data-stu-id="15794-365">Set values and keys that mirror those settings under the following key.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         Mail
            CanonicalName
               Protocols
                  mailto
```

<span data-ttu-id="15794-366">Essa hierarquia de Registro substitui a `mailto` hierarquia de registro existente encontrada em **HKEY \_ classes \_ root** \\ **mailto**.</span><span class="sxs-lookup"><span data-stu-id="15794-366">This registry hierarchy replaces the existing `mailto` registry hierarchy found at **HKEY\_CLASSES\_ROOT**\\**mailto**.</span></span> <span data-ttu-id="15794-367">A hierarquia permanece a mesma, apenas o local foi alterado.</span><span class="sxs-lookup"><span data-stu-id="15794-367">The hierarchy remains the same, only the location has changed.</span></span> <span data-ttu-id="15794-368">O formato dessa hierarquia está documentado no MSDN em [visões gerais e tutoriais do protocolo conectável conectáveis](/previous-versions//aa767913(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="15794-368">The format of this hierarchy is documented on MSDN under [Asynchronous Pluggable Protocol Overviews and Tutorials](/previous-versions//aa767913(v=vs.85)).</span></span> <span data-ttu-id="15794-369">Normalmente, o `mailto` protocolo é registrado em um programa em vez de um protocolo assíncrono; nesse caso, a documentação sobre o [registro de um aplicativo em um esquema de URI](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767914(v=vs.85)) se aplica.</span><span class="sxs-lookup"><span data-stu-id="15794-369">Typically, the `mailto` protocol is registered to a program rather than an asynchronous protocol, in which case the documentation on [Registering an Application to a URI Scheme](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767914(v=vs.85)) applies.</span></span>

<span data-ttu-id="15794-370">O exemplo a seguir mostra a `mailto` seção do registro de um `mailto` manipulador registrado para um programa.</span><span class="sxs-lookup"><span data-stu-id="15794-370">The following example shows the `mailto` section of the registration for a `mailto` handler registered to a program.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         Mail
            CanonicalName
               Protocols
                  mailto
                     (Default) = URL:MailTo Protocol
                     EditFlags = 02 00 00 00
                     URL Protocol
                     DefaultIcon
                        (Default) = %FilePath%,IconIndex
                     shell
                        open
                           command
                              (Default) = command line
```

<span data-ttu-id="15794-371">O valor do registro EditFlags é documentado em [tipos de arquivo](fa-file-types.md) na seção intitulada "definindo atributos de tipo de arquivo".</span><span class="sxs-lookup"><span data-stu-id="15794-371">The EditFlags registry value is documented in [File Types](fa-file-types.md) in the section titled "Defining File Type Attributes."</span></span>

## <a name="complete-sample-registrations"></a><span data-ttu-id="15794-372">Concluir os registros de exemplo</span><span class="sxs-lookup"><span data-stu-id="15794-372">Complete Sample Registrations</span></span>

<span data-ttu-id="15794-373">Os exemplos a seguir são fornecidos para mostrar os requisitos de registro completos para os vários tipos de cliente.</span><span class="sxs-lookup"><span data-stu-id="15794-373">The following examples are provided to show the complete registration requirements for the various client types.</span></span>

-   [<span data-ttu-id="15794-374">Um navegador de exemplo</span><span class="sxs-lookup"><span data-stu-id="15794-374">A Sample Browser</span></span>](#a-sample-browser)
-   [<span data-ttu-id="15794-375">Um navegador de email de exemplo</span><span class="sxs-lookup"><span data-stu-id="15794-375">A Sample Mail Browser</span></span>](#a-sample-mail-browser)
-   [<span data-ttu-id="15794-376">Um player de mídia de exemplo</span><span class="sxs-lookup"><span data-stu-id="15794-376">A Sample Media Player</span></span>](#a-sample-media-player)
-   [<span data-ttu-id="15794-377">Um programa de Instant Messenger de exemplo</span><span class="sxs-lookup"><span data-stu-id="15794-377">A Sample Instant Messenger Program</span></span>](#a-sample-instant-messenger-program)
-   [<span data-ttu-id="15794-378">Uma máquina virtual de exemplo para Java</span><span class="sxs-lookup"><span data-stu-id="15794-378">A Sample Virtual Machine for Java</span></span>](#a-sample-virtual-machine-for-java)

### <a name="a-sample-browser"></a><span data-ttu-id="15794-379">Um navegador de exemplo</span><span class="sxs-lookup"><span data-stu-id="15794-379">A Sample Browser</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         StartMenuInternet
            LITVIEW.EXE
               (Default) = Lit View
               LocalizedString = @C:\Program Files\LitwareInc\ResourceDLL.dll,-123
               DefaultIcon
                  (Default) = C:\Program Files\LitwareInc\LITVIEW.EXE,1
               InstallInfo
                  ReinstallCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /reinstall
                  HideIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /hideicons
                  ShowIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /showicons
                  IconsVisible = 1
                  shell
                     open
                        command
                           (Default) = "C:\Program Files\LitwareInc\LITVIEW.EXE" /homepage
```

### <a name="a-sample-mail-browser"></a><span data-ttu-id="15794-380">Um navegador de email de exemplo</span><span class="sxs-lookup"><span data-stu-id="15794-380">A Sample Mail Browser</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         Mail
            Lit View
               (Default) = Lit View
               DLLPath = @C:\Program Files\LItwareInc\LitwareMAPI.dll
               LocalizedString = @C:\Program Files\LitwareInc\ResourceDLL.dll,-123
               DefaultIcon
                  (Default) = C:\Program Files\LitwareInc\LITVIEW.EXE,1
               InstallInfo
                  ReinstallCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /reinstall
                  HideIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /hideicons
                  ShowIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /showicons
                  IconsVisible = 1
               shell
                  open
                     command
                        (Default) = "C:\Program Files\LitwareInc\LITVIEW.EXE" /inbox
               protocols
                  mailto
                     (Default) = URL:MailTo Protocol
                     EditFlags = 02 00 00 00
                     URL Protocol
                     DefaultIcon
                        (Default) = C:\Program Files\LitwareInc\LITVIEW.EXE,1
                     shell
                        open
                           command
                              (Default) = "C:\Program Files\LitwareInc\LITVIEW.EXE" /mailto:%1
```

### <a name="a-sample-media-player"></a><span data-ttu-id="15794-381">Um player de mídia de exemplo</span><span class="sxs-lookup"><span data-stu-id="15794-381">A Sample Media Player</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         Media
            Lit View
               (Default) = Lit View
               LocalizedString = @C:\Program Files\LitwareInc\ResourceDLL.dll,-123
               DefaultIcon
                  (Default) = C:\Program Files\LitwareInc\LITVIEW.EXE,1
               InstallInfo
                  ReinstallCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /reinstall
                  HideIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /hideicons
                  ShowIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /showicons
                  IconsVisible = 1
```

### <a name="a-sample-instant-messenger-program"></a><span data-ttu-id="15794-382">Um programa de Instant Messenger de exemplo</span><span class="sxs-lookup"><span data-stu-id="15794-382">A Sample Instant Messenger Program</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         IM
            Lit View
               (Default) = Lit View
               LocalizedString = @C:\Program Files\LitwareInc\ResourceDLL.dll,-123
               DefaultIcon
                  (Default) = C:\Program Files\LitwareInc\LITVIEW.EXE,1
               InstallInfo
                  ReinstallCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /reinstall
                  HideIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /hideicons
                  ShowIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /showicons
                  IconsVisible = 1
```

### <a name="a-sample-virtual-machine-for-java"></a><span data-ttu-id="15794-383">Uma máquina virtual de exemplo para Java</span><span class="sxs-lookup"><span data-stu-id="15794-383">A Sample Virtual Machine for Java</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         JavaVM
            Lit View
               (Default) = Lit View
               LocalizedString = @C:\Program Files\LitwareInc\ResourceDLL.dll,-123
               DefaultIcon
                  (Default) = C:\Program Files\LitwareInc\LITVIEW.EXE,1
               InstallInfo
                  ReinstallCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /reinstall
                  HideIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /hideicons
                  ShowIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /showicons
                  IconsVisible = 1
```

<span data-ttu-id="15794-384">*As empresas de exemplo, as organizações, os produtos, os nomes de domínio, os endereços de email, os logotipos, as pessoas, os lugares e os eventos aqui descritos são fictícios. Nenhuma associação com qualquer empresa, organização, produto, nome de domínio, endereço de email, logotipo, pessoa, lugar ou evento real é intencional ou deve ser inferida.*</span><span class="sxs-lookup"><span data-stu-id="15794-384">*The example companies, organizations, products, domain names, email addresses, logos, people, places, and events depicted herein are fictitious. No association with any real company, organization, product, domain name, email address, logo, person, place, or event is intended or should be inferred.*</span></span>

## <a name="related-topics"></a><span data-ttu-id="15794-385">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="15794-385">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="15794-386">Programas padrão</span><span class="sxs-lookup"><span data-stu-id="15794-386">Default Programs</span></span>](default-programs.md)
</dt> <dt>

[<span data-ttu-id="15794-387">Como registrar um navegador da Internet ou cliente de email com o menu Iniciar do Windows</span><span class="sxs-lookup"><span data-stu-id="15794-387">How to Register an Internet Browser or Email Client With the Windows Start Menu</span></span>](start-menu-reg.md)
</dt> <dt>

<span data-ttu-id="15794-388">[Layout do registro do cliente do Internet Explorer (consulte a seção "definições da chave do registro do cliente")](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa753633(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="15794-388">[Internet Explorer Client Registry Layout (see the "Client Registry Key Definitions" section)](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa753633(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="15794-389">[Visões gerais e tutoriais de protocolos conectáveis assíncronos](/previous-versions//aa767913(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="15794-389">[Asynchronous Pluggable Protocol Overviews and Tutorials](/previous-versions//aa767913(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="15794-390">[Registrando um aplicativo em um esquema de URI](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767914(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="15794-390">[Registering an Application to a URI Scheme](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767914(v=vs.85))</span></span>
</dt> </dl>

 

 
