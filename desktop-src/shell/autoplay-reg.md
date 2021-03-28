---
description: Há muitas situações em que a execução automática pode precisar ser temporariamente desabilitada ou persistente.
ms.assetid: 5e65a3d8-04b9-46ba-b4e5-a976e1923bfd
title: Habilitando e desabilitando o AutoRun
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a567f50db75cd129346e193e66ba0ae5f74fa955
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370618"
---
# <a name="enabling-and-disabling-autorun"></a><span data-ttu-id="3142f-103">Habilitando e desabilitando o AutoRun</span><span class="sxs-lookup"><span data-stu-id="3142f-103">Enabling and Disabling AutoRun</span></span>

<span data-ttu-id="3142f-104">Há muitas situações em que a execução automática pode precisar ser temporariamente desabilitada ou persistente.</span><span class="sxs-lookup"><span data-stu-id="3142f-104">There are many situations where AutoRun may need to be temporarily or persistently disabled.</span></span> <span data-ttu-id="3142f-105">Por exemplo, o AutoRun pode interferir na operação de um aplicativo em execução e precisa ser desabilitado durante a duração.</span><span class="sxs-lookup"><span data-stu-id="3142f-105">For example, AutoRun might interfere with the operation of a running application and need to be disabled for the duration.</span></span> <span data-ttu-id="3142f-106">O sistema fornece várias maneiras de desabilitar o AutoRun.</span><span class="sxs-lookup"><span data-stu-id="3142f-106">The system provides several ways to disable AutoRun.</span></span>

-   [<span data-ttu-id="3142f-107">Suprimindo o AutoRun programaticamente</span><span class="sxs-lookup"><span data-stu-id="3142f-107">Suppressing AutoRun Programmatically</span></span>](#suppressing-autorun-programmatically)
-   [<span data-ttu-id="3142f-108">Usando o registro para desabilitar o AutoRun</span><span class="sxs-lookup"><span data-stu-id="3142f-108">Using the Registry to Disable AutoRun</span></span>](#using-the-registry-to-disable-autorun)
-   [<span data-ttu-id="3142f-109">AutoRun para outros tipos de mídia de armazenamento</span><span class="sxs-lookup"><span data-stu-id="3142f-109">AutoRun for Other Types of Storage Media</span></span>](#autorun-for-other-types-of-storage-media)

## <a name="suppressing-autorun-programmatically"></a><span data-ttu-id="3142f-110">Suprimindo o AutoRun programaticamente</span><span class="sxs-lookup"><span data-stu-id="3142f-110">Suppressing AutoRun Programmatically</span></span>

<span data-ttu-id="3142f-111">Há uma variedade de situações em que a execução de AutoRun pode precisar ser suprimida programaticamente.</span><span class="sxs-lookup"><span data-stu-id="3142f-111">There are a variety of situations where AutoRun may need to be suppressed programmatically.</span></span> <span data-ttu-id="3142f-112">Dois exemplos são:</span><span class="sxs-lookup"><span data-stu-id="3142f-112">Two examples are:</span></span>

-   <span data-ttu-id="3142f-113">Seu aplicativo tem um programa de instalação que exige que o usuário insira outro disco que possa conter um arquivo autorun. inf.</span><span class="sxs-lookup"><span data-stu-id="3142f-113">Your application has a setup program that requires the user to insert another disc that may contain an Autorun.inf file.</span></span>
-   <span data-ttu-id="3142f-114">Durante a operação do seu aplicativo, o usuário pode precisar inserir outro disco que possa conter um arquivo autorun. inf.</span><span class="sxs-lookup"><span data-stu-id="3142f-114">During the operation of your application, the user may need to insert another disc that may contain an Autorun.inf file.</span></span>

<span data-ttu-id="3142f-115">Em ambos os casos, normalmente você não vai querer iniciar outro aplicativo enquanto o original está em andamento.</span><span class="sxs-lookup"><span data-stu-id="3142f-115">In either case, you will normally not want to launch another application while the original is in progress.</span></span>

<span data-ttu-id="3142f-116">Os usuários podem suprimir manualmente o AutoRun mantendo a tecla SHIFT pressionada ao inserir o CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="3142f-116">Users can manually suppress AutoRun by holding down the SHIFT key when they insert the CD-ROM.</span></span> <span data-ttu-id="3142f-117">No entanto, geralmente é preferível lidar com essa operação programaticamente, em vez de depender do usuário.</span><span class="sxs-lookup"><span data-stu-id="3142f-117">However, it is usually preferable to handle this operation programmatically rather than depending on the user.</span></span>

<span data-ttu-id="3142f-118">Com sistemas que têm o Shell [versão 4,70](versions.md) e posterior, o Windows envia uma mensagem "QueryCancelAutoPlay" para a janela em primeiro plano.</span><span class="sxs-lookup"><span data-stu-id="3142f-118">With systems that have Shell [version 4.70](versions.md) and later, Windows sends a "QueryCancelAutoPlay" message to the foreground window.</span></span> <span data-ttu-id="3142f-119">Seu aplicativo pode responder a esta mensagem para suprimir o AutoRun.</span><span class="sxs-lookup"><span data-stu-id="3142f-119">Your application can respond to this message to suppress AutoRun.</span></span> <span data-ttu-id="3142f-120">Essa abordagem é usada por utilitários do sistema, como a caixa de diálogo [abrir](../dlgbox/open-and-save-as-dialog-boxes.md) comum para desabilitar o autorun.</span><span class="sxs-lookup"><span data-stu-id="3142f-120">This approach is used by system utilities such as the [Open](../dlgbox/open-and-save-as-dialog-boxes.md) common dialog box to disable AutoRun.</span></span>

<span data-ttu-id="3142f-121">Os fragmentos de código a seguir ilustram como configurar e tratar essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="3142f-121">The following code fragments illustrate how to set up and handle this message.</span></span> <span data-ttu-id="3142f-122">Seu aplicativo deve estar em execução na janela em primeiro plano.</span><span class="sxs-lookup"><span data-stu-id="3142f-122">Your application must be running in the foreground window.</span></span> <span data-ttu-id="3142f-123">Primeiro, registre "QueryCancelAutoPlay" como uma mensagem do Windows:</span><span class="sxs-lookup"><span data-stu-id="3142f-123">First, register "QueryCancelAutoPlay" as a Windows message:</span></span>


```C++
uMessage = RegisterWindowMessage(TEXT("QueryCancelAutoPlay"));
```



<span data-ttu-id="3142f-124">A janela do seu aplicativo deve estar no primeiro plano para receber esta mensagem.</span><span class="sxs-lookup"><span data-stu-id="3142f-124">Your application's window must be in the foreground to receive this message.</span></span> <span data-ttu-id="3142f-125">O manipulador de mensagens deve retornar **true** para cancelar autorun e **false** para habilitá-lo.</span><span class="sxs-lookup"><span data-stu-id="3142f-125">The message handler should return **TRUE** to cancel AutoRun and **FALSE** to enable it.</span></span> <span data-ttu-id="3142f-126">O fragmento de código a seguir ilustra como usar essa mensagem para desabilitar o AutoRun.</span><span class="sxs-lookup"><span data-stu-id="3142f-126">The following code fragment illustrates how to use this message to disable AutoRun.</span></span>


```C++
UINT g_uQueryCancelAutoPlay = 0;

LRESULT WndProc(HWND hwnd, UINT uMsg,  WPARAM wParam, LPARAM lParam) 
{ 
    switch (uMsg) 
    { 
    ... 
    default: 
        if (!g_uQueryCancelAutoPlay)
        { 
            g_uQueryCancelAutoPlay = RegisterWindowMessage(TEXT("QueryCancelAutoPlay"));
        } 
        if (uMsg && uMsg == g_uQueryCancelAutoPlay)
        { 
            return TRUE;       // Cancel AutoRun
        }
    }
}
```



<span data-ttu-id="3142f-127">Se seu aplicativo estiver usando uma caixa de diálogo e precisar responder a uma mensagem "QueryCancelAutoPlay", ele não poderá simplesmente retornar **true** ou **false**.</span><span class="sxs-lookup"><span data-stu-id="3142f-127">If your application is using a dialog box and needs to respond to a "QueryCancelAutoPlay" message, it cannot simply return **TRUE** or **FALSE**.</span></span> <span data-ttu-id="3142f-128">Em vez disso, chame [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) com *NIndex* definido como **DWL \_ MSGRESULT**.</span><span class="sxs-lookup"><span data-stu-id="3142f-128">Instead, call [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) with *nIndex* set to **DWL\_MSGRESULT**.</span></span> <span data-ttu-id="3142f-129">Defina o parâmetro *dwNewLong* como **true** para cancelar o autorun e **false** para habilitá-lo.</span><span class="sxs-lookup"><span data-stu-id="3142f-129">Set the *dwNewLong* parameter to **TRUE** to cancel AutoRun, and **FALSE** to enable it.</span></span> <span data-ttu-id="3142f-130">Por exemplo, o procedimento de caixa de diálogo de exemplo a seguir cancela o AutoRun quando recebe uma mensagem "QueryCancelAutoPlay".</span><span class="sxs-lookup"><span data-stu-id="3142f-130">For example, the following sample dialog box procedure cancels AutoRun when it receives a "QueryCancelAutoPlay" message.</span></span>


```C++
UINT g_uQueryCancelAutoPlay = 0;

BOOL DialogProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
    switch (uMsg) 
    { 
    ...
    default: 
        if (!g_uQueryCancelAutoPlay)
        {
            g_uQueryCancelAutoPlay = RegisterWindowMessage(TEXT("QueryCancelAutoPlay"));
        } 
        if (uMsg == g_uQueryCancelAutoPlay) 
        {
            SetWindowLong(hDlg, DWL_MSGRESULT, TRUE);          
            return 1;               
        }
    } 
```



## <a name="using-the-registry-to-disable-autorun"></a><span data-ttu-id="3142f-131">Usando o registro para desabilitar o AutoRun</span><span class="sxs-lookup"><span data-stu-id="3142f-131">Using the Registry to Disable AutoRun</span></span>

<span data-ttu-id="3142f-132">Há dois valores de registro que podem ser usados para desabilitar o AutoRun de forma persistente: NoDriveAutoRun e NoDriveTypeAutoRun.</span><span class="sxs-lookup"><span data-stu-id="3142f-132">There are two registry values that can be used to persistently disable AutoRun: NoDriveAutoRun and NoDriveTypeAutoRun.</span></span> <span data-ttu-id="3142f-133">O primeiro valor desabilita o AutoRun para as letras de unidade especificadas e a segunda desabilita o AutoRun para uma classe de unidades.</span><span class="sxs-lookup"><span data-stu-id="3142f-133">The first value disables AutoRun for specified drive letters and the second disables AutoRun for a class of drives.</span></span> <span data-ttu-id="3142f-134">Se um desses valores for definido para desabilitar o AutoRun para um dispositivo específico, ele será desabilitado.</span><span class="sxs-lookup"><span data-stu-id="3142f-134">If either of these values is set to disable AutoRun for a particular device, it will be disabled.</span></span> <span data-ttu-id="3142f-135">Consulte o artigo da base de dados de conhecimento [como desabilitar a funcionalidade de Autorun no Windows](https://support.microsoft.com/kb/967715) para obter mais informações sobre como desabilitar a funcionalidade de Autorun.</span><span class="sxs-lookup"><span data-stu-id="3142f-135">See the Knowledge Base article [How to disable the Autorun functionality in Windows](https://support.microsoft.com/kb/967715) for more information on disabling AutoRun functionality.</span></span> <span data-ttu-id="3142f-136">Este artigo lista as diferentes atualizações que você deve ter instaladas para desabilitar corretamente a funcionalidade de Autorun.</span><span class="sxs-lookup"><span data-stu-id="3142f-136">This article lists the different updates that you must have installed to correctly disable the Autorun functionality.</span></span>

> [!Note]  
> <span data-ttu-id="3142f-137">Os valores NoDriveAutoRun e NoDriveTypeAutoRun só devem ser modificados pelos administradores do sistema para alterar o valor de todo o sistema para fins de teste ou administrativos.</span><span class="sxs-lookup"><span data-stu-id="3142f-137">The NoDriveAutoRun and NoDriveTypeAutoRun values should only be modified by system administrators to change the value for the entire system for testing or administrative purposes.</span></span> <span data-ttu-id="3142f-138">Os aplicativos não devem modificar esses valores, pois não há como restaurá-los de forma confiável para seus valores originais.</span><span class="sxs-lookup"><span data-stu-id="3142f-138">Applications should not modify these values, as there is no way to reliably restore them to their original values.</span></span>

 

<span data-ttu-id="3142f-139">O valor NoDriveAutoRun desabilita o AutoRun para as letras de unidade especificadas.</span><span class="sxs-lookup"><span data-stu-id="3142f-139">The NoDriveAutoRun value disables AutoRun for specified drive letters.</span></span> <span data-ttu-id="3142f-140">É um valor de \_ dados reg DWORD, encontrado na seguinte chave:</span><span class="sxs-lookup"><span data-stu-id="3142f-140">It is a REG\_DWORD data value, found under the following key:</span></span>

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Policies
                  Explorer
```

<span data-ttu-id="3142f-141">O primeiro bit do valor corresponde à unidade A:, a segunda a B: e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="3142f-141">The first bit of the value corresponds to drive A:, the second to B:, and so on.</span></span> <span data-ttu-id="3142f-142">Para desabilitar o AutoRun para uma ou mais letras de unidade, defina os bits correspondentes.</span><span class="sxs-lookup"><span data-stu-id="3142f-142">To disable AutoRun for one or more drive letters, set the corresponding bits.</span></span> <span data-ttu-id="3142f-143">Por exemplo, para desabilitar as unidades a: e C:, defina NoDriveAutoRun como `0x00000005` .</span><span class="sxs-lookup"><span data-stu-id="3142f-143">For example, to disable the A: and C: drives, set NoDriveAutoRun to `0x00000005`.</span></span>

<span data-ttu-id="3142f-144">O valor de NoDriveTypeAutoRun desabilita a execução automática para uma classe de unidades.</span><span class="sxs-lookup"><span data-stu-id="3142f-144">The NoDriveTypeAutoRun value disables AutoRun for a class of drives.</span></span> <span data-ttu-id="3142f-145">É um valor de \_ dados binário reg de 4 bytes ou reg DWORD \_ , encontrado na mesma chave.</span><span class="sxs-lookup"><span data-stu-id="3142f-145">It is a REG\_DWORD or 4-byte REG\_BINARY data value, found under the same key.</span></span>

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Policies
                  Explorer
```

<span data-ttu-id="3142f-146">Ao definir os bits do primeiro byte deste valor, unidades diferentes podem ser excluídas do trabalho com AutoRun.</span><span class="sxs-lookup"><span data-stu-id="3142f-146">By setting the bits of this value's first byte, different drives can be excluded from working with AutoRun.</span></span>

<span data-ttu-id="3142f-147">A tabela a seguir fornece as constantes bits e bitmask, que podem ser definidas no primeiro byte de NoDriveTypeAutoRun para desabilitar o AutoRun para um determinado tipo de unidade.</span><span class="sxs-lookup"><span data-stu-id="3142f-147">The following table gives the bits and bitmask constants, that can be set in the first byte of NoDriveTypeAutoRun to disable AutoRun for a particular drive type.</span></span> <span data-ttu-id="3142f-148">Você deve reiniciar o Windows Explorer antes que as alterações entrem em vigor.</span><span class="sxs-lookup"><span data-stu-id="3142f-148">You must restart Windows Explorer before the changes take effect.</span></span>



| <span data-ttu-id="3142f-149">Número de bits</span><span class="sxs-lookup"><span data-stu-id="3142f-149">Bit Number</span></span> | <span data-ttu-id="3142f-150">Constante de bitmask</span><span class="sxs-lookup"><span data-stu-id="3142f-150">Bitmask Constant</span></span>      | <span data-ttu-id="3142f-151">Description</span><span class="sxs-lookup"><span data-stu-id="3142f-151">Description</span></span>                                             |
|------------|-----------------------|---------------------------------------------------------|
| <span data-ttu-id="3142f-152">0x04</span><span class="sxs-lookup"><span data-stu-id="3142f-152">0x04</span></span>       | <span data-ttu-id="3142f-153">**UNIDADE \_ REmovida**</span><span class="sxs-lookup"><span data-stu-id="3142f-153">**DRIVE\_REMOVEABLE**</span></span> | <span data-ttu-id="3142f-154">O disco pode ser removido da unidade (como um disquete).</span><span class="sxs-lookup"><span data-stu-id="3142f-154">Disk can be removed from drive (such as a floppy disk).</span></span> |
| <span data-ttu-id="3142f-155">0x08</span><span class="sxs-lookup"><span data-stu-id="3142f-155">0x08</span></span>       | <span data-ttu-id="3142f-156">**UNIDADE \_ fixa**</span><span class="sxs-lookup"><span data-stu-id="3142f-156">**DRIVE\_FIXED**</span></span>      | <span data-ttu-id="3142f-157">O disco não pode ser removido da unidade (um disco rígido).</span><span class="sxs-lookup"><span data-stu-id="3142f-157">Disk cannot be removed from drive (a hard disk).</span></span>        |
| <span data-ttu-id="3142f-158">0x10</span><span class="sxs-lookup"><span data-stu-id="3142f-158">0x10</span></span>       | <span data-ttu-id="3142f-159">**UNIDADE \_ remota**</span><span class="sxs-lookup"><span data-stu-id="3142f-159">**DRIVE\_REMOTE**</span></span>     | <span data-ttu-id="3142f-160">Unidade de rede.</span><span class="sxs-lookup"><span data-stu-id="3142f-160">Network drive.</span></span>                                          |
| <span data-ttu-id="3142f-161">0x20</span><span class="sxs-lookup"><span data-stu-id="3142f-161">0x20</span></span>       | <span data-ttu-id="3142f-162">**UNIDADE de \_ cdrom**</span><span class="sxs-lookup"><span data-stu-id="3142f-162">**DRIVE\_CDROM**</span></span>      | <span data-ttu-id="3142f-163">Unidade de CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="3142f-163">CD-ROM drive.</span></span>                                           |
| <span data-ttu-id="3142f-164">0x40</span><span class="sxs-lookup"><span data-stu-id="3142f-164">0x40</span></span>       | <span data-ttu-id="3142f-165">**UNIDADE de \_ ramdisk**</span><span class="sxs-lookup"><span data-stu-id="3142f-165">**DRIVE\_RAMDISK**</span></span>    | <span data-ttu-id="3142f-166">Disco RAM.</span><span class="sxs-lookup"><span data-stu-id="3142f-166">RAM disk.</span></span>                                               |



 

## <a name="autorun-for-other-types-of-storage-media"></a><span data-ttu-id="3142f-167">AutoRun para outros tipos de mídia de armazenamento</span><span class="sxs-lookup"><span data-stu-id="3142f-167">AutoRun for Other Types of Storage Media</span></span>

<span data-ttu-id="3142f-168">A execução automática destina-se principalmente à distribuição pública de aplicativos em CD-ROM e DVD-ROM, e seu uso não é recomendado para outras mídias de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="3142f-168">AutoRun is primarily intended for public distribution of applications on CD-ROM and DVD-ROM, and its use is discouraged for other storage media.</span></span> <span data-ttu-id="3142f-169">No entanto, geralmente é útil habilitar o AutoRun em outros tipos de mídia de armazenamento removível.</span><span class="sxs-lookup"><span data-stu-id="3142f-169">However, it is often useful to enable AutoRun on other types of removable storage media.</span></span> <span data-ttu-id="3142f-170">Normalmente, esse recurso é usado para simplificar a depuração de arquivos AutoRun. inf.</span><span class="sxs-lookup"><span data-stu-id="3142f-170">This feature is typically used simplify the debugging of AutoRun.inf files.</span></span> <span data-ttu-id="3142f-171">O AutoRun só funciona em dispositivos de armazenamento removíveis quando os critérios a seguir são atendidos:</span><span class="sxs-lookup"><span data-stu-id="3142f-171">AutoRun only works on removable storage devices when the following criteria are met:</span></span>

-   <span data-ttu-id="3142f-172">O dispositivo deve ter drivers compatíveis com AutoRun.</span><span class="sxs-lookup"><span data-stu-id="3142f-172">The device must have AutoRun-compatible drivers.</span></span> <span data-ttu-id="3142f-173">Para ser compatível com AutoRun, um driver deve notificar o sistema de que um disco foi inserido enviando uma mensagem do [**WM \_ DEVICECHANGE**](../devio/wm-devicechange.md) .</span><span class="sxs-lookup"><span data-stu-id="3142f-173">To be AutoRun-compatible, a driver must notify the system that a disk has been inserted by sending a [**WM\_DEVICECHANGE**](../devio/wm-devicechange.md) message.</span></span>
-   <span data-ttu-id="3142f-174">O diretório raiz da mídia inserida deve conter um arquivo autorun. inf.</span><span class="sxs-lookup"><span data-stu-id="3142f-174">The root directory of the inserted media must contain an Autorun.inf file.</span></span>
-   <span data-ttu-id="3142f-175">O dispositivo não deve ter o AutoRun desabilitado por meio do [registro](#using-the-registry-to-disable-autorun).</span><span class="sxs-lookup"><span data-stu-id="3142f-175">The device must not have AutoRun disabled through the [registry](#using-the-registry-to-disable-autorun).</span></span>
-   <span data-ttu-id="3142f-176">O aplicativo em primeiro plano não [eliminou](#suppressing-autorun-programmatically) o autorun.</span><span class="sxs-lookup"><span data-stu-id="3142f-176">The foreground application has not [suppressed](#suppressing-autorun-programmatically) AutoRun.</span></span>

> [!Note]  
> <span data-ttu-id="3142f-177">Esse recurso não deve ser usado para distribuir aplicativos em mídias removíveis.</span><span class="sxs-lookup"><span data-stu-id="3142f-177">This feature should not be used to distribute applications on removable media.</span></span> <span data-ttu-id="3142f-178">Como a implementação do AutoRun em mídia removível fornece uma maneira fácil de espalhar vírus de computador, os usuários devem ser suspeitos de qualquer disquete distribuído publicamente que contenha um arquivo autorun. inf.</span><span class="sxs-lookup"><span data-stu-id="3142f-178">Because implementing AutoRun on removable media provides an easy way to spread computer viruses, users should be suspicious of any publicly distributed floppy disk that contains an Autorun.inf file.</span></span>

 

<span data-ttu-id="3142f-179">Normalmente, o AutoRun é iniciado automaticamente, mas também pode ser iniciado manualmente.</span><span class="sxs-lookup"><span data-stu-id="3142f-179">Normally, AutoRun starts automatically, but it can also be started manually.</span></span> <span data-ttu-id="3142f-180">Se o dispositivo atender aos critérios listados acima, o menu de atalho da letra da unidade incluirá um comando de **reprodução automática** .</span><span class="sxs-lookup"><span data-stu-id="3142f-180">If the device meets the criteria listed above, the drive letter's shortcut menu will include an **AutoPlay** command.</span></span> <span data-ttu-id="3142f-181">Para executar o AutoRun manualmente, clique com o botão direito do mouse no ícone da unidade e selecione **reprodução automática** no menu de atalho ou clique duas vezes no ícone da unidade.</span><span class="sxs-lookup"><span data-stu-id="3142f-181">To run AutoRun manually, either right-click the drive icon and select **AutoPlay** from the shortcut menu or double-click the drive icon.</span></span> <span data-ttu-id="3142f-182">Se os drivers não forem compatíveis com AutoRun, o menu de atalho não terá um item de **reprodução automática** e o autorun não poderá ser iniciado.</span><span class="sxs-lookup"><span data-stu-id="3142f-182">If the drivers are not AutoRun-compatible, the shortcut menu will not have an **AutoPlay** item and AutoRun cannot be started.</span></span>

<span data-ttu-id="3142f-183">Os drivers compatíveis com AutoRun são fornecidos com algumas unidades de disco removíveis, bem como alguns outros tipos de mídia removível, como placas CompactFlash.</span><span class="sxs-lookup"><span data-stu-id="3142f-183">AutoRun-compatible drivers are provided with some removable disk drives, as well as some other types of removable media such as CompactFlash cards.</span></span> <span data-ttu-id="3142f-184">O AutoRun também funciona com unidades de rede que são mapeadas para uma letra de unidade com o Windows Explorer ou montados com o [MMC (console de gerenciamento Microsoft)](/previous-versions/windows/desktop/mmc/microsoft-management-console-start-page).</span><span class="sxs-lookup"><span data-stu-id="3142f-184">AutoRun also works with network drives that are mapped to a drive letter with Windows Explorer or mounted with the [Microsoft Management Console (MMC)](/previous-versions/windows/desktop/mmc/microsoft-management-console-start-page).</span></span> <span data-ttu-id="3142f-185">Assim como ocorre com o hardware montado, uma unidade de rede montada deve ter um arquivo autorun. inf em seu diretório raiz e não deve ser desabilitada por meio do [registro](#using-the-registry-to-disable-autorun).</span><span class="sxs-lookup"><span data-stu-id="3142f-185">As with mounted hardware, a mounted network drive must have an Autorun.inf file in its root directory, and must not be disabled through the [registry](#using-the-registry-to-disable-autorun).</span></span>

 

 
