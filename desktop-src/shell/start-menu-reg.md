---
description: O menu iniciar no Windows XP e no Windows Vista contém Slots reservados para os clientes padrão de Internet (navegador) e email (email), juntos conhecidos como aplicativos de Internet do menu iniciar.
ms.assetid: a3d7416f-0dbd-4af2-ab38-758f9cc8aec5
title: Como registrar um navegador da Internet ou cliente de email com o menu Iniciar do Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eccdd8fb8efe32522947b30ab2ce1a50b7058e97
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "104172538"
---
# <a name="how-to-register-an-internet-browser-or-email-client-with-the-windows-start-menu"></a><span data-ttu-id="f4ad5-103">Como registrar um navegador da Internet ou cliente de email com o menu Iniciar do Windows</span><span class="sxs-lookup"><span data-stu-id="f4ad5-103">How to Register an Internet Browser or Email Client With the Windows Start Menu</span></span>

> [!Note]  
> <span data-ttu-id="f4ad5-104">Este tópico aplica-se ao Windows XP, Windows Vista e Windows 7.</span><span class="sxs-lookup"><span data-stu-id="f4ad5-104">This topic applies to Windows XP, Windows Vista, and Windows 7.</span></span>

 

<span data-ttu-id="f4ad5-105">O menu iniciar no Windows XP e no Windows Vista contém Slots reservados para os clientes padrão de **Internet** (navegador) e **email** (email), juntos conhecidos como *aplicativos de Internet do menu iniciar*.</span><span class="sxs-lookup"><span data-stu-id="f4ad5-105">The Start menu in Windows XP and Windows Vista contains reserved slots for the default **Internet** (browser) and **E-mail** (mail) clients, together commonly known as *Start Menu Internet Applications*.</span></span> <span data-ttu-id="f4ad5-106">Os aplicativos que se registram como menu iniciar aplicativos de Internet fazem isso em todo o sistema (por máquina).</span><span class="sxs-lookup"><span data-stu-id="f4ad5-106">Applications which register as Start Menu Internet Applications do so across the entire system (per-machine).</span></span> <span data-ttu-id="f4ad5-107">No Windows Vista, o usuário pode usar o recurso **programas padrão** para definir um padrão por usuário.</span><span class="sxs-lookup"><span data-stu-id="f4ad5-107">In Windows Vista, the user may use the **Default Programs** feature to set a per-user default.</span></span>

<span data-ttu-id="f4ad5-108">Quando os aplicativos são registrados como menu iniciar aplicativos de Internet, o Windows XP e o Windows Vista criam ícones de **Internet** e **email** no menu iniciar.</span><span class="sxs-lookup"><span data-stu-id="f4ad5-108">When applications register as Start Menu Internet Applications, Windows XP and Windows Vista create **Internet** and **E-mail** icons on the Start menu.</span></span> <span data-ttu-id="f4ad5-109">Clicar nesses ícones faz com que o menu iniciar Verifique a subárvore do registro por usuário (**HKEY \_ Current \_ User**).</span><span class="sxs-lookup"><span data-stu-id="f4ad5-109">Clicking these icons causes the Start menu to check the per-user registry subtree (**HKEY\_CURRENT\_USER**).</span></span> <span data-ttu-id="f4ad5-110">Se nenhuma configuração padrão por usuário for encontrada, o menu iniciar procurará a subchave padrão por máquina na subárvore **do \_ \_ computador local hKey** .</span><span class="sxs-lookup"><span data-stu-id="f4ad5-110">If no per-user default setting is found, the Start menu looks for the per-machine default subkey in the **HKEY\_LOCAL\_MACHINE** subtree.</span></span>

> [!Note]  
> <span data-ttu-id="f4ad5-111">A instalação padrão do Windows não registra um programa de email ou Internet padrão por usuário, apenas um padrão em todo o sistema.</span><span class="sxs-lookup"><span data-stu-id="f4ad5-111">The default installation of Windows does not register a per-user default Internet or email program, only a system-wide default.</span></span> <span data-ttu-id="f4ad5-112">Isso fornece um caminho de atualização suave de versões anteriores do sistema operacional, em que apenas a \_ subárvore do computador local hKey tem \_ suporte para registros de cliente.</span><span class="sxs-lookup"><span data-stu-id="f4ad5-112">This provides a smooth upgrade path from previous versions of the operating system, in which only the HKEY\_LOCAL\_MACHINE subtree is supported for client registrations.</span></span>

 

<span data-ttu-id="f4ad5-113">Este tópico discute os seguintes itens:</span><span class="sxs-lookup"><span data-stu-id="f4ad5-113">This topic discusses the following items:</span></span>

-   [<span data-ttu-id="f4ad5-114">Registro no link da Internet do menu iniciar</span><span class="sxs-lookup"><span data-stu-id="f4ad5-114">Registering for the Start Menu Internet Link</span></span>](#registering-for-the-start-menu-internet-link)
    -   [<span data-ttu-id="f4ad5-115">Como registrar-se como o cliente de Internet padrão</span><span class="sxs-lookup"><span data-stu-id="f4ad5-115">How to Register as the Default Internet Client</span></span>](#how-to-register-as-the-default-internet-client)
-   [<span data-ttu-id="f4ad5-116">Registro para o link de email do menu iniciar</span><span class="sxs-lookup"><span data-stu-id="f4ad5-116">Registering for the Start Menu Email Link</span></span>](#registering-for-the-start-menu-email-link)
    -   [<span data-ttu-id="f4ad5-117">Como o menu iniciar exibe o cliente de email padrão</span><span class="sxs-lookup"><span data-stu-id="f4ad5-117">How the Start Menu Displays the Default Email Client</span></span>](#how-the-start-menu-displays-the-default-email-client)
    -   [<span data-ttu-id="f4ad5-118">Como registrar-se como o cliente de EMail padrão</span><span class="sxs-lookup"><span data-stu-id="f4ad5-118">How to Register as the Default EMail Client</span></span>](#how-to-register-as-the-default-email-client)
-   [<span data-ttu-id="f4ad5-119">Personalizando o menu de contexto</span><span class="sxs-lookup"><span data-stu-id="f4ad5-119">Customizing the Context Menu</span></span>](#customizing-the-context-menu)

## <a name="registering-for-the-start-menu-internet-link"></a><span data-ttu-id="f4ad5-120">Registro no link da Internet do menu iniciar</span><span class="sxs-lookup"><span data-stu-id="f4ad5-120">Registering for the Start Menu Internet Link</span></span>

> [!Note]  
> <span data-ttu-id="f4ad5-121">Esse registro é preterido a partir do Windows 7, que não fornece mais um link de Internet do menu iniciar.</span><span class="sxs-lookup"><span data-stu-id="f4ad5-121">This registration is deprecated as of Windows 7, which no longer provides a Start menu Internet link.</span></span> <span data-ttu-id="f4ad5-122">Os registros existentes são ignorados no Windows 7 e versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="f4ad5-122">Existing registrations are ignored in Windows 7 and later.</span></span> <span data-ttu-id="f4ad5-123">Ser registrado como o aplicativo de Internet do menu Iniciar padrão não é o mesmo que está sendo registrado como o navegador da Web padrão.</span><span class="sxs-lookup"><span data-stu-id="f4ad5-123">Being registered as the default Start menu Internet application is not the same as being registered as the default web browser.</span></span> <span data-ttu-id="f4ad5-124">O navegador da Web padrão é usado para iniciar URLs arbitrárias de qualquer lugar no sistema.</span><span class="sxs-lookup"><span data-stu-id="f4ad5-124">The default web browser is used for launching arbitrary URLs from anywhere in the system.</span></span> <span data-ttu-id="f4ad5-125">O menu iniciar aplicativo de Internet simplesmente controla o programa que é iniciado quando o usuário clica no ícone Internet no menu iniciar.</span><span class="sxs-lookup"><span data-stu-id="f4ad5-125">The Start menu Internet application merely controls the program that is started when the user clicks the Internet icon on the Start menu.</span></span>

 

<span data-ttu-id="f4ad5-126">Qualquer aplicativo de navegador da Web pode se registrar para aparecer como um cliente de Internet no menu iniciar.</span><span class="sxs-lookup"><span data-stu-id="f4ad5-126">Any web browser application can register to appear as an Internet client on the Start menu.</span></span> <span data-ttu-id="f4ad5-127">Essa visibilidade, associada ao registro adequado para os tipos de [arquivo](fa-intro.md) e [protocolo](/previous-versions//aa767743(v=vs.85)) de um aplicativo, fornece um status de navegador padrão do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f4ad5-127">This visibility, coupled with proper registration for an application's [file](fa-intro.md) and [protocol](/previous-versions//aa767743(v=vs.85)) types, gives an application default browser status.</span></span>

<span data-ttu-id="f4ad5-128">Os registros feitos na subárvore do **\_ \_ usuário atual do hKey** têm maior precedência para o usuário do console do que os registros correspondentes feitos no **\_ \_ computador local hKey**.</span><span class="sxs-lookup"><span data-stu-id="f4ad5-128">Registrations made in the **HKEY\_CURRENT\_USER** subtree have higher precedence for the console user than corresponding registrations made in the **HKEY\_LOCAL\_MACHINE**.</span></span> <span data-ttu-id="f4ad5-129">Para novos usuários no sistema, as configurações armazenadas na **\_ \_ máquina local hKey** são usadas.</span><span class="sxs-lookup"><span data-stu-id="f4ad5-129">For new users on the system, the settings stored in **HKEY\_LOCAL\_MACHINE** are used.</span></span> <span data-ttu-id="f4ad5-130">A partir do Windows XP, as configurações de Internet do menu iniciar são mantidas nas entradas padrão de dois locais de registro:</span><span class="sxs-lookup"><span data-stu-id="f4ad5-130">As of Windows XP, Start menu Internet settings are kept in the default entries of two registry locations:</span></span>

-   <span data-ttu-id="f4ad5-131">**HKEY \_ \_** Clientes de \\ **software** do usuário atual \\  \\ **StartMenuInternet**</span><span class="sxs-lookup"><span data-stu-id="f4ad5-131">**HKEY\_CURRENT\_USER**\\**SOFTWARE**\\**Clients**\\**StartMenuInternet**</span></span>
-   <span data-ttu-id="f4ad5-132">**HKEY \_ \_** Clientes de \\ **software** de computador local \\  \\ **StartMenuInternet**</span><span class="sxs-lookup"><span data-stu-id="f4ad5-132">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Clients**\\**StartMenuInternet**</span></span>

<span data-ttu-id="f4ad5-133">A subchave **HKEY \_ Current \_ User** \\ **software** \\ **clients** \\ **StartMenuInternet** descreve o navegador da Internet que é iniciado quando o usuário clica no ícone **Internet** no menu iniciar.</span><span class="sxs-lookup"><span data-stu-id="f4ad5-133">The subkey **HKEY\_CURRENT\_USER**\\**SOFTWARE**\\**Clients**\\**StartMenuInternet** describes the Internet browser that is started when the user clicks the **Internet** icon on the Start menu.</span></span> <span data-ttu-id="f4ad5-134">Se essa subchave estiver em branco ou ausente, o ícone da **Internet** no menu iniciar será definido como o padrão do sistema armazenado no segundo local em **HKEY \_ local \_ Machine** \\ **software** \\ **clients** \\ **StartMenuInternet** , que descreve todos os aplicativos de navegador da Internet instalados no sistema.</span><span class="sxs-lookup"><span data-stu-id="f4ad5-134">If that subkey is blank or missing, then the **Internet** icon on the Start menu is set to the system default stored in the second location at **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Clients**\\**StartMenuInternet** , which describes all Internet browser applications that are installed on the system.</span></span>

<span data-ttu-id="f4ad5-135">Quando um novo usuário faz logon no sistema, o menu iniciar usa o valor padrão na subchave em **HKEY \_ local \_ Machine** \\ **software** \\ **clients** \\ **StartMenuInternet** para exibir o cliente de Internet padrão e inicia o aplicativo registrado quando esse ícone é clicado.</span><span class="sxs-lookup"><span data-stu-id="f4ad5-135">When a new user logs onto the system, the Start menu uses the default value in the subkey at **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Clients**\\**StartMenuInternet** to display the default Internet client and starts the registered application when that icon is clicked.</span></span>

### <a name="how-to-register-as-the-default-internet-client"></a><span data-ttu-id="f4ad5-136">Como registrar-se como o cliente de Internet padrão</span><span class="sxs-lookup"><span data-stu-id="f4ad5-136">How to Register as the Default Internet Client</span></span>

<span data-ttu-id="f4ad5-137">Abaixo da subchave **HKEY \_ \_ computador local** \\ **software** \\ **clients** \\ **StartMenuInternet** pode haver zero ou mais subchaves, uma para cada aplicativo registrado de navegador da Internet.</span><span class="sxs-lookup"><span data-stu-id="f4ad5-137">Below the subkey **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Clients**\\**StartMenuInternet** there can be zero or more subkeys, one for each registered Internet browser application.</span></span> <span data-ttu-id="f4ad5-138">Por exemplo, um sistema hipotético pode ter essa disposição:</span><span class="sxs-lookup"><span data-stu-id="f4ad5-138">For example, a hypothetical system might have this arrangement:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         StartMenuInternet
            IEXPLORE.EXE
            BROWSER2.EXE
            BROWSER3.EXE
```

<span data-ttu-id="f4ad5-139">Demonstraremos as entradas do registro com um navegador hipotético chamado "visão acesa" de uma empresa fictícia chamada Litware Inc. suponha que o nome do executável para exibição acesa seja Litview.exe.</span><span class="sxs-lookup"><span data-stu-id="f4ad5-139">We will demonstrate registry entries with a hypothetical browser called "Lit View" from a fictional company called Litware Inc. Suppose that the executable name for Lit View is Litview.exe.</span></span> <span data-ttu-id="f4ad5-140">O registro da exibição acesa ocorre conforme mostrado aqui:</span><span class="sxs-lookup"><span data-stu-id="f4ad5-140">The registration of Lit View occurs as shown here:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         StartMenuInternet
            LITVIEW.EXE
               LocalizedString = @C:\Program Files\LitwareInc\ResourceDLL.dll,-123
```

<span data-ttu-id="f4ad5-141">Os dados de localizadas são do tipo REG \_ sz ou reg \_ Expand \_ sz Se variáveis de caminho, como `%programfiles%` são usadas.</span><span class="sxs-lookup"><span data-stu-id="f4ad5-141">The LocalizedString data is of type REG\_SZ, or REG\_EXPAND\_SZ if path variables such as `%programfiles%` are used.</span></span> <span data-ttu-id="f4ad5-142">A localizadastring fornece o caminho para um arquivo executável (. exe) ou de biblioteca (. dll).</span><span class="sxs-lookup"><span data-stu-id="f4ad5-142">LocalizedString provides the path to an executable (.exe) or library (.dll) file.</span></span> <span data-ttu-id="f4ad5-143">Observe que a cadeia de caracteres do caminho começa com um sinal de "arroba" (@) e que nenhuma aspa é necessária em relação ao caminho, independentemente dos espaços dentro dela.</span><span class="sxs-lookup"><span data-stu-id="f4ad5-143">Note that the path string begins with an "at" sign (@) and that no quotation marks are required around the path regardless of spaces within it.</span></span> <span data-ttu-id="f4ad5-144">O inteiro decimal é a ID de um recurso de cadeia de caracteres, contido na DLL especificada, cujo valor deve ser exibido ao usuário.</span><span class="sxs-lookup"><span data-stu-id="f4ad5-144">The decimal integer is the ID of a string resource, contained within the specified DLL, whose value is to be displayed to the user.</span></span> <span data-ttu-id="f4ad5-145">Isso permite que o mesmo registro seja usado para vários idiomas.</span><span class="sxs-lookup"><span data-stu-id="f4ad5-145">This enables the same registration to be used for multiple languages.</span></span> <span data-ttu-id="f4ad5-146">Cada idioma fornece um ResourceDLL.dll diferente.</span><span class="sxs-lookup"><span data-stu-id="f4ad5-146">Each language provides a different ResourceDLL.dll.</span></span> <span data-ttu-id="f4ad5-147">Isso permite que o sistema exiba a cadeia de caracteres correta com base no idioma selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="f4ad5-147">This enables the system to display the correct string based on the currently selected language.</span></span>

<span data-ttu-id="f4ad5-148">O seguinte \_ valor de sz de reg-sz ou reg \_ Expand \_ informa o menu Iniciar do ícone padrão a ser exibido quando o usuário seleciona a exibição acesa como o navegador de Internet do menu iniciar.</span><span class="sxs-lookup"><span data-stu-id="f4ad5-148">The following REG\_SZ or REG\_EXPAND\_SZ value informs the Start menu of the default icon to display when the user selects Lit View as the Start menu Internet browser.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         StartMenuInternet
            LITVIEW.EXE
               DefaultIcon
                  (Default) = C:\Program Files\LitwareInc\LitView.exe,1
```

<span data-ttu-id="f4ad5-149">A subchave do registro a seguir especifica uma linha de comando a ser executada quando o usuário clica no comando de menu da Internet no menu Iniciar, supondo que a exibição acesa seja o navegador da Internet do menu iniciar selecionado.</span><span class="sxs-lookup"><span data-stu-id="f4ad5-149">The following registry subkey specifies a command line to run when the user clicks the Internet menu command on the Start menu, assuming that Lit View is the selected Start menu Internet browser.</span></span> <span data-ttu-id="f4ad5-150">Por exemplo, o comando pode abrir o navegador com o home page do usuário ou o comando pode iniciar uma interface do usuário introdutória que as funcionalidades do ISV (fornecedor independente de software) são apropriadas.</span><span class="sxs-lookup"><span data-stu-id="f4ad5-150">For example, the command might open the browser with the user's home page or the command could launch an introductory user interface that the independent software vendor (ISV) feels is appropriate.</span></span> <span data-ttu-id="f4ad5-151">Os dados são do tipo REG \_ sz ou reg \_ Expand \_ sz, mas observe que, como há um espaço no caminho da linha de comando, o caminho do executável é colocado entre aspas.</span><span class="sxs-lookup"><span data-stu-id="f4ad5-151">The data is of type REG\_SZ or REG\_EXPAND\_SZ, but notice that because there is a space in the command-line path, the executable path is enclosed in quotation marks.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         StartMenuInternet
            LITVIEW.EXE
               shell
                  open
                     (Default) = "C:\Program Files\LitwareInc\LitView.exe" -welcome
```

<span data-ttu-id="f4ad5-152">Quando o usuário especifica por meio de [Definir acesso do programa e padrões do computador (SPAD)](cpl-setprogramaccess.md) que a exibição acesa deve ser usada como o navegador da Web padrão no nível do computador, o aplicativo deve definir a entrada reg sz a seguir \_ .</span><span class="sxs-lookup"><span data-stu-id="f4ad5-152">When the user specifies through [Set Program Access and Computer Defaults (SPAD)](cpl-setprogramaccess.md) that Lit View should be used as the computer-level default web browser, the application should set the following REG\_SZ entry.</span></span> <span data-ttu-id="f4ad5-153">Observe que, como o SPAD é executado com privilégios de administrador, o acesso a essa subchave é permitido.</span><span class="sxs-lookup"><span data-stu-id="f4ad5-153">Note that because SPAD runs with Administrator privileges, access to this subkey is allowed.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         StartMenuInternet
            (Default) = LITVIEW.EXE
```

> [!Note]
> <span data-ttu-id="f4ad5-154">No Windows Vista, o navegador da Web padrão de nível de usuário deve ser definido usando a ferramenta **programas padrão** , não o [SPAD](cpl-setprogramaccess.md).</span><span class="sxs-lookup"><span data-stu-id="f4ad5-154">In Windows Vista, the user-level default web browser should be set using the **Default Programs** tool, not [SPAD](cpl-setprogramaccess.md).</span></span>
> 
> <span data-ttu-id="f4ad5-155">**As informações a seguir aplicam-se apenas ao Windows XP.**</span><span class="sxs-lookup"><span data-stu-id="f4ad5-155">**The following information applies to Windows XP only.**</span></span>
> 
> <span data-ttu-id="f4ad5-156">Se o registro do navegador da Web padrão no nível do computador em HKEY \_ local \_ Machine como mostrado acima for bem-sucedido, o aplicativo deverá excluir a entrada padrão na seguinte subchave:</span><span class="sxs-lookup"><span data-stu-id="f4ad5-156">If the registration of the computer-level default web browser under HKEY\_LOCAL\_MACHINE as shown above is successful, the application should delete the Default entry under the following subkey:</span></span>
> 
> ```
> HKEY_CURRENT_USER
>    SOFTWARE
>       Clients
>          StartMenuInternet
> ```
> 
> <span data-ttu-id="f4ad5-157">Se o registro do navegador da Web padrão no nível do computador em HKEY \_ local \_ Machine falhar, o aplicativo deverá definir os \_ dados de reg sz, conforme mostrado neste exemplo para o aplicativo de exibição iluminada:</span><span class="sxs-lookup"><span data-stu-id="f4ad5-157">If the registration of the computer-level default web browser under HKEY\_LOCAL\_MACHINE fails, the application should set the REG\_SZ data as shown in this example for the Lit View application:</span></span>
> 
> ```
> HKEY_CURRENT_USER
>    SOFTWARE
>       Clients
>          (Default) = LITVIEW.EXE
> ```

 

<span data-ttu-id="f4ad5-158">Depois de atualizar as subchaves apropriadas, o aplicativo transmite a mensagem do [**WM \_ SETTINGCHANGE**](../winmsg/wm-settingchange.md) com seu parâmetro *wParam* definido como 0 e seu parâmetro *lParam* apontando para a cadeia de caracteres terminada em nulo `"Software\Clients\StartMenuInternet"` .</span><span class="sxs-lookup"><span data-stu-id="f4ad5-158">After updating the appropriate subkeys, the application broadcasts the [**WM\_SETTINGCHANGE**](../winmsg/wm-settingchange.md) message with its *wParam* parameter set to 0 and its *lParam* parameter pointing to the null-terminated string `"Software\Clients\StartMenuInternet"`.</span></span> <span data-ttu-id="f4ad5-159">Isso notifica o sistema operacional que o cliente padrão alterou.</span><span class="sxs-lookup"><span data-stu-id="f4ad5-159">This notifies the operating system that the default client has changed.</span></span>

<span data-ttu-id="f4ad5-160">A definição dessas subchaves para o navegador da Internet do menu Iniciar padrão é necessária para preservar a compatibilidade com versões anteriores de navegadores da Web que não dão suporte a registros por usuário.</span><span class="sxs-lookup"><span data-stu-id="f4ad5-160">Setting these subkeys for the default Start menu Internet browser is necessary to preserve backward compatibility with old web browsers that do not support per-user registrations.</span></span>

## <a name="registering-for-the-start-menu-email-link"></a><span data-ttu-id="f4ad5-161">Registro para o link de email do menu iniciar</span><span class="sxs-lookup"><span data-stu-id="f4ad5-161">Registering for the Start Menu Email Link</span></span>

> [!Note]  
> <span data-ttu-id="f4ad5-162">O link email do menu iniciar foi removido do Windows 7.</span><span class="sxs-lookup"><span data-stu-id="f4ad5-162">The Start menu Email link has been removed as of Windows 7.</span></span> <span data-ttu-id="f4ad5-163">No entanto, esse registro abordado nesta seção ainda deve ser executado para seu efeito na atribuição do cliente MAPI padrão.</span><span class="sxs-lookup"><span data-stu-id="f4ad5-163">However, this registration discussed in this section should still be performed for its effect in assigning the default MAPI client.</span></span>

 

### <a name="how-the-start-menu-displays-the-default-email-client"></a><span data-ttu-id="f4ad5-164">Como o menu iniciar exibe o cliente de email padrão</span><span class="sxs-lookup"><span data-stu-id="f4ad5-164">How the Start Menu Displays the Default Email Client</span></span>

<span data-ttu-id="f4ad5-165">Qualquer aplicativo de email pode se registrar para aparecer como um cliente de email no menu iniciar.</span><span class="sxs-lookup"><span data-stu-id="f4ad5-165">Any email application can register to appear as an email client on the Start menu.</span></span> <span data-ttu-id="f4ad5-166">Essa visibilidade, associada ao registro adequado para os tipos de [arquivo](fa-intro.md) e [protocolo](/previous-versions//aa767743(v=vs.85)) de um aplicativo, fornece um status de email padrão do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f4ad5-166">This visibility, coupled with proper registration for an application's [file](fa-intro.md) and [protocol](/previous-versions//aa767743(v=vs.85)) types, gives an application default mail status.</span></span>

<span data-ttu-id="f4ad5-167">Os registros feitos na subárvore do **\_ \_ usuário atual do hKey** têm maior precedência para o usuário do console do que os registros correspondentes feitos no **\_ \_ computador local hKey**.</span><span class="sxs-lookup"><span data-stu-id="f4ad5-167">Registrations made in the **HKEY\_CURRENT\_USER** subtree have higher precedence for the console user than corresponding registrations made in the **HKEY\_LOCAL\_MACHINE**.</span></span> <span data-ttu-id="f4ad5-168">Para novos usuários no sistema, as configurações armazenadas na **\_ \_ máquina local hKey** são usadas.</span><span class="sxs-lookup"><span data-stu-id="f4ad5-168">For new users on the system, the settings stored in **HKEY\_LOCAL\_MACHINE** are used.</span></span> <span data-ttu-id="f4ad5-169">A partir do Windows XP, as configurações de email do menu iniciar são mantidas nas entradas padrão de dois locais de registro:</span><span class="sxs-lookup"><span data-stu-id="f4ad5-169">As of Windows XP, Start menu Email settings are kept in the default entries of two registry locations:</span></span>

-   <span data-ttu-id="f4ad5-170">**HKEY \_ \_** Email de \\  \\ **clientes** \\  de software do usuário atual</span><span class="sxs-lookup"><span data-stu-id="f4ad5-170">**HKEY\_CURRENT\_USER**\\**SOFTWARE**\\**Clients**\\**Mail**</span></span>
-   <span data-ttu-id="f4ad5-171">**HKEY \_ \_** Email de \\  \\ **clientes** \\  de software do computador local</span><span class="sxs-lookup"><span data-stu-id="f4ad5-171">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Clients**\\**Mail**</span></span>

<span data-ttu-id="f4ad5-172">A subchave **HKEY \_ Current \_ User** \\ **software** \\ **clients** \\ **mail** descreve o cliente de email que é iniciado quando o usuário clica no ícone de **email** no menu iniciar.</span><span class="sxs-lookup"><span data-stu-id="f4ad5-172">The subkey **HKEY\_CURRENT\_USER**\\**SOFTWARE**\\**Clients**\\**Mail** describes the email client that is started when the user clicks the **E-mail** icon on the Start menu.</span></span>

<span data-ttu-id="f4ad5-173">A subchave **HKEY do \_ \_ computador local** \\ **software** \\ **clients** \\ **mail** descreve os aplicativos de email que estão instalados no sistema, bem como o aplicativo de email padrão.</span><span class="sxs-lookup"><span data-stu-id="f4ad5-173">The subkey **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Clients**\\**Mail** describes the email applications that are installed on the system, as well as the default email application.</span></span>

<span data-ttu-id="f4ad5-174">Se o **HKEY \_ atual \_ User** \\ **software** \\ **clients** \\ **mail** estiver em branco ou ausente, o valor padrão definido em **HKEY \_ local \_ Machine** \\ **software** \\ **clients** \\ **mail** será usado para selecionar o aplicativo de email que aparece no menu iniciar.</span><span class="sxs-lookup"><span data-stu-id="f4ad5-174">If the **HKEY\_CURRENT\_USER**\\**SOFTWARE**\\**Clients**\\**Mail** is blank or missing, the default value defined in **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Clients**\\**Mail** is used to select the email application that appears on the Start menu.</span></span>

<span data-ttu-id="f4ad5-175">Quando um novo usuário faz logon no sistema, o menu iniciar usa o valor padrão na subchave em **HKEY \_ local \_ Machine** \\ **software** \\ **clients** \\ **mail** para exibir o cliente de email padrão e inicia o aplicativo registrado quando esse ícone é clicado.</span><span class="sxs-lookup"><span data-stu-id="f4ad5-175">When a new user logs onto the system, the Start menu uses the default value in the subkey at **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Clients**\\**Mail** to display the default email client and starts the registered application when that icon is clicked.</span></span>

### <a name="how-to-register-as-the-default-email-client"></a><span data-ttu-id="f4ad5-176">Como registrar-se como o cliente de EMail padrão</span><span class="sxs-lookup"><span data-stu-id="f4ad5-176">How to Register as the Default EMail Client</span></span>

<span data-ttu-id="f4ad5-177">**HKEY \_ O \_** \\  \\  \\ **email** de clientes de software de computador local pode conter zero ou mais subchaves, um para cada aplicativo de email registrado.</span><span class="sxs-lookup"><span data-stu-id="f4ad5-177">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Clients**\\**Mail** can contain zero or more subkeys, one for each registered email application.</span></span> <span data-ttu-id="f4ad5-178">Por exemplo, um sistema hipotético pode definir as seguintes subchaves:</span><span class="sxs-lookup"><span data-stu-id="f4ad5-178">For example, a hypothetical system might define the following subkeys:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            Eudora
            Windows Mail
```

<span data-ttu-id="f4ad5-179">Demonstraremos as entradas do registro com um cliente de email hipotético chamado "email aceso" da empresa fictícia chamada Litware Inc. Litware Inc. decide registrar esse cliente de email com o nome interno "LitMail".</span><span class="sxs-lookup"><span data-stu-id="f4ad5-179">We will demonstrate registry entries with a hypothetical email client called "Lit Mail" from the fictional company called Litware Inc. Litware Inc. decides to register this email client under the internal name "LitMail".</span></span> <span data-ttu-id="f4ad5-180">Assim como em um navegador, o nome interno é uma cadeia de caracteres exclusiva usada como o nome da subchave, mas nunca é mostrado ao usuário.</span><span class="sxs-lookup"><span data-stu-id="f4ad5-180">As with a browser, the internal name is a unique string used as the subkey name, but it is never shown to the user.</span></span>

<span data-ttu-id="f4ad5-181">Para instalar o cliente de email de email aceso como o padrão, eles usam a seguinte subchave e suas entradas:</span><span class="sxs-lookup"><span data-stu-id="f4ad5-181">To install the Lit Mail email client as the default, they use the following subkey and its entries:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            LitMail
               (Default) = Lit Mail
               LocalizedString = @C:\Program Files\LitwareInc\ResourceDLL.dll,-456
```

<span data-ttu-id="f4ad5-182">Os dados de localizadas são do tipo REG \_ sz ou reg \_ Expand \_ sz Se variáveis de caminho, como `%programfiles%` são usadas.</span><span class="sxs-lookup"><span data-stu-id="f4ad5-182">The LocalizedString data is of type REG\_SZ, or REG\_EXPAND\_SZ if path variables such as `%programfiles%` are used.</span></span> <span data-ttu-id="f4ad5-183">A localizadastring fornece o caminho para um arquivo executável (. exe) ou de biblioteca (. dll).</span><span class="sxs-lookup"><span data-stu-id="f4ad5-183">LocalizedString provides the path to an executable (.exe) or library (.dll) file.</span></span> <span data-ttu-id="f4ad5-184">Observe que a cadeia de caracteres do caminho começa com um sinal de "arroba" (@) e que nenhuma aspa é necessária em relação ao caminho, independentemente dos espaços dentro dela.</span><span class="sxs-lookup"><span data-stu-id="f4ad5-184">Note that the path string begins with an "at" sign (@) and that no quotation marks are required around the path regardless of spaces within it.</span></span> <span data-ttu-id="f4ad5-185">O inteiro decimal é a ID de um recurso de cadeia de caracteres, contido na DLL especificada, cujo valor deve ser exibido ao usuário.</span><span class="sxs-lookup"><span data-stu-id="f4ad5-185">The decimal integer is the ID of a string resource, contained within the specified DLL, whose value is to be displayed to the user.</span></span> <span data-ttu-id="f4ad5-186">Isso permite que o mesmo registro seja usado para vários idiomas.</span><span class="sxs-lookup"><span data-stu-id="f4ad5-186">This enables the same registration to be used for multiple languages.</span></span> <span data-ttu-id="f4ad5-187">Cada idioma fornece um ResourceDLL.dll diferente.</span><span class="sxs-lookup"><span data-stu-id="f4ad5-187">Each language provides a different ResourceDLL.dll.</span></span> <span data-ttu-id="f4ad5-188">Isso permite que o sistema exiba a cadeia de caracteres correta com base no idioma selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="f4ad5-188">This enables the system to display the correct string based on the currently selected language.</span></span>

<span data-ttu-id="f4ad5-189">Depois de atualizar as subchaves apropriadas, o aplicativo transmite a mensagem do [**WM \_ SETTINGCHANGE**](../winmsg/wm-settingchange.md) com seu parâmetro *wParam* definido como 0 e seu parâmetro *lParam* apontando para a cadeia de caracteres terminada em nulo `"Software\Clients\Mail"` .</span><span class="sxs-lookup"><span data-stu-id="f4ad5-189">After updating the appropriate subkeys, the application broadcasts the [**WM\_SETTINGCHANGE**](../winmsg/wm-settingchange.md) message with its *wParam* parameter set to 0 and its *lParam* parameter pointing to the null-terminated string `"Software\Clients\Mail"`.</span></span> <span data-ttu-id="f4ad5-190">Isso notifica o sistema operacional que o cliente padrão alterou.</span><span class="sxs-lookup"><span data-stu-id="f4ad5-190">This notifies the operating system that the default client has changed.</span></span>

<span data-ttu-id="f4ad5-191">Para compatibilidade com versões anteriores com aplicativos que não dão suporte a cadeias de caracteres localizadas, o nome do aplicativo no idioma instalado também deve ser definido como o valor padrão para a subchave.</span><span class="sxs-lookup"><span data-stu-id="f4ad5-191">For backward compatibility with applications that do not support localized strings, the name of the application in the installed language should also be set as the default value for the subkey.</span></span>

<span data-ttu-id="f4ad5-192">O seguinte valor de sz- **\_ sz reg** ou **reg \_ expande \_** informa o menu Iniciar do ícone padrão a ser exibido quando o usuário seleciona email aceso como o programa de email do menu iniciar:</span><span class="sxs-lookup"><span data-stu-id="f4ad5-192">The following **REG\_SZ** or **REG\_EXPAND\_SZ** value informs the Start menu of the default icon to display when the user selects Lit Mail as the Start menu mail program:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            LitMail
               DefaultIcon
                  (Default) = C:\Program Files\LitwareInc\LitMail.exe,1
```

<span data-ttu-id="f4ad5-193">A entrada a seguir especifica uma linha de comando a ser executada quando o usuário clica no item de menu de **email** no menu Iniciar, supondo que email aceso seja o programa de email do menu iniciar selecionado.</span><span class="sxs-lookup"><span data-stu-id="f4ad5-193">The following entry specifies a command line to run when the user clicks the **E-mail** menu item on the Start menu, assuming that Lit Mail is the selected Start menu email program.</span></span> <span data-ttu-id="f4ad5-194">Essa linha de comando também será executada se o usuário selecionar **ler email** no menu **ferramentas** do Internet Explorer do Windows.</span><span class="sxs-lookup"><span data-stu-id="f4ad5-194">This command line is also run if the user selects **Read email** from the Windows Internet Explorer **Tools** menu.</span></span> <span data-ttu-id="f4ad5-195">Os dados são do tipo **reg \_ sz** ou **reg \_ Expand \_ sz**, mas observe que, como há um espaço no caminho da linha de comando, o caminho do executável é colocado entre aspas.</span><span class="sxs-lookup"><span data-stu-id="f4ad5-195">The data is of type **REG\_SZ** or **REG\_EXPAND\_SZ**, but notice that because there is a space in the command-line path, the executable path is enclosed in quotation marks.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            shell
               open
                  command
                     (Default) = "C:\Program Files\LitwareInc\LitMail.exe" -inbox
```

<span data-ttu-id="f4ad5-196">Se (e somente se) *o usuário* especificar email aceso como o aplicativo de email do menu Iniciar padrão, o aplicativo de email aceso pode gravar seu nome interno no seguinte valor de **reg \_ sz** :</span><span class="sxs-lookup"><span data-stu-id="f4ad5-196">If (and only if) *the user* specifies Lit Mail to be the default Start menu email application, the Lit Mail application may write its internal name to the following **REG\_SZ** value:</span></span>

```
HKEY_CURRENT_USER
   SOFTWARE
      Clients
         Mail
            (Default) = LitMail
```

<span data-ttu-id="f4ad5-197">Se (e somente se) *o usuário* especificar o email aceso para ser o aplicativo de email padrão em todo o sistema, o aplicativo de email aceso poderá gravar seu nome interno no valor de **\_ sz do reg** especificado abaixo.</span><span class="sxs-lookup"><span data-stu-id="f4ad5-197">If (and only if) *the user* specifies Lit Mail to be the system-wide default email application, the Lit Mail application may write its internal name to the **REG\_SZ** value specified below.</span></span> <span data-ttu-id="f4ad5-198">Observe que o acesso a essa subchave pode ser restrito.</span><span class="sxs-lookup"><span data-stu-id="f4ad5-198">Note that access to this subkey might be restricted.</span></span> <span data-ttu-id="f4ad5-199">Os aplicativos não devem pressupor que todos os usuários tenham permissão para alterar o aplicativo de email padrão de todo o sistema.</span><span class="sxs-lookup"><span data-stu-id="f4ad5-199">Applications should not assume that all users have permission to change the system-wide default email application.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            (Default) = LitMail
```

<span data-ttu-id="f4ad5-200">O registro como o aplicativo de email do menu Iniciar padrão não é equivalente ao registro como o cliente de email padrão do sistema ou o manipulador do *mailto* registrado.</span><span class="sxs-lookup"><span data-stu-id="f4ad5-200">Registration as the default Start menu email application is not equivalent to registration as the system default email client or the registered *mailto* handler.</span></span>

-   <span data-ttu-id="f4ad5-201">O cliente de email padrão do sistema é iniciado quando o usuário clica em **ler email** no menu **ferramentas** do Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="f4ad5-201">The system default email client is started when the user clicks **Read email** from the Internet Explorer **Tools** menu.</span></span>
-   <span data-ttu-id="f4ad5-202">O manipulador *mailto* registrado é iniciado quando o usuário clica em uma URL do formulário `mailto:someone@example.com` .</span><span class="sxs-lookup"><span data-stu-id="f4ad5-202">The registered *mailto* handler is started when the user clicks a URL of the form `mailto:someone@example.com`.</span></span>
-   <span data-ttu-id="f4ad5-203">O aplicativo de email do menu iniciar é iniciado quando o usuário clica no ícone de **email** no menu iniciar.</span><span class="sxs-lookup"><span data-stu-id="f4ad5-203">The Start menu email application is started when the user clicks the **E-mail** icon on the Start menu.</span></span>

<span data-ttu-id="f4ad5-204">Se nenhum aplicativo de email do menu Iniciar padrão for especificado, o ícone de email no menu iniciar inicia o cliente de email padrão do sistema.</span><span class="sxs-lookup"><span data-stu-id="f4ad5-204">If no default Start menu email application is specified, the Email icon on the Start menu launches the system default email client.</span></span>

<span data-ttu-id="f4ad5-205">Este tópico não abrange o registro do aplicativo como o manipulador de protocolo padrão *mailto* .</span><span class="sxs-lookup"><span data-stu-id="f4ad5-205">This topic does not cover registration of the application as the default *mailto* protocol handler.</span></span> <span data-ttu-id="f4ad5-206">Os aplicativos que desejam se registrar dessa maneira devem continuar a seguir as especificações existentes sobre esse assunto.</span><span class="sxs-lookup"><span data-stu-id="f4ad5-206">Applications that want to register in such a manner should continue to follow existing specifications on this subject.</span></span>

## <a name="customizing-the-context-menu"></a><span data-ttu-id="f4ad5-207">Personalizando o menu de contexto</span><span class="sxs-lookup"><span data-stu-id="f4ad5-207">Customizing the Context Menu</span></span>

<span data-ttu-id="f4ad5-208">Um aplicativo pode personalizar as páginas de propriedades que são exibidas quando o usuário seleciona **Propriedades** no menu de atalho do ícone **email** (ou **Internet**).</span><span class="sxs-lookup"><span data-stu-id="f4ad5-208">An application can customize the property pages that are displayed when the user selects **Properties** from the **E-mail** (or **Internet**) icon's shortcut menu.</span></span> <span data-ttu-id="f4ad5-209">Por exemplo, o aplicativo de email Litware adiciona os seguintes dados **reg \_ sz** ou **reg \_ expande \_ sz** para exibir uma folha de propriedades Personalizada para o ícone de **email** em vez de sua folha de propriedades padrão.</span><span class="sxs-lookup"><span data-stu-id="f4ad5-209">For example, the Litware email application adds the following **REG\_SZ** or **REG\_EXPAND\_SZ** data to display a custom property sheet for the **E-mail** icon rather than its default property sheet.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            LitMail
               shell
                  properties
                     MUIVerb = @C:\Program Files\LitwareInc\ResourceDLL.dll,-789
                     command
                        (Default) = "C:\Program Files\LitwareInc\LitMail.exe" -properties
```

<span data-ttu-id="f4ad5-210">O item de dados MUIVerb é construído começando com um sinal "arroba" (@), seguido pelo caminho completo para a DLL de recurso, uma vírgula, um sinal de menos (-) e o identificador de recurso de cadeia de caracteres decimal a ser exibido.</span><span class="sxs-lookup"><span data-stu-id="f4ad5-210">The MUIVerb data item is constructed beginning with an "at" sign (@), followed by the full path to the resource DLL, a comma, a minus sign (-), and then the decimal string resource identifier to display.</span></span> <span data-ttu-id="f4ad5-211">Observe que o caminho para o programa de LitMail.exe contém espaços, portanto, a cadeia de caracteres do caminho é colocada entre aspas.</span><span class="sxs-lookup"><span data-stu-id="f4ad5-211">Note that the path to the LitMail.exe program contains spaces, so the path string is placed inside quotation marks.</span></span>

<span data-ttu-id="f4ad5-212">Um aplicativo também pode adicionar outros comandos ao menu de contexto.</span><span class="sxs-lookup"><span data-stu-id="f4ad5-212">An application can also add additional commands to the context menu.</span></span> <span data-ttu-id="f4ad5-213">Por exemplo, o aplicativo de email Litware adiciona um comando **Find** com os seguintes dados **reg \_ sz** :</span><span class="sxs-lookup"><span data-stu-id="f4ad5-213">For example, the Litware email application adds a **find** command with the following **REG\_SZ** data:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            LitMail
               shell
                  find
                     MUIVerb = @C:\Program File\LitwareInc\ResourceDLL.dll,-790
                     command
                        (Default) = "C:\Program Files\LitwareInc\LitMail.exe" -contacts
```

<span data-ttu-id="f4ad5-214">O nome da subchave abaixo do **shell** (nesse caso, "Find") é um nome arbitrário e não-local.</span><span class="sxs-lookup"><span data-stu-id="f4ad5-214">The subkey name below **shell** (in this case, "find") is an arbitrary, nonlocalized name.</span></span> <span data-ttu-id="f4ad5-215">Mais uma vez, os dados de MUIVerb contêm um sinal de "arroba" (@) como o primeiro elemento, seguido pelo caminho para uma DLL de recurso, um separador de vírgula e um sinal de subtração que antecede o identificador de recurso de cadeia de caracteres decimal.</span><span class="sxs-lookup"><span data-stu-id="f4ad5-215">Once again the MUIVerb data contains an "at" sign (@) as the first element, followed by the path to a resource DLL, a comma separator, and then a minus sign preceding the decimal string resource identifier.</span></span> <span data-ttu-id="f4ad5-216">Por exemplo, esse recurso de cadeia de caracteres pode ser "abrir catálogo de endereços".</span><span class="sxs-lookup"><span data-stu-id="f4ad5-216">For example, that string resource might be "Open Address Book".</span></span> <span data-ttu-id="f4ad5-217">Por fim, observe que a cadeia de caracteres de linha de comando contém espaços, portanto, ela é colocada entre aspas.</span><span class="sxs-lookup"><span data-stu-id="f4ad5-217">Finally, note that the command-line string contains spaces, so it is enclosed in quotation marks.</span></span>

 

 
