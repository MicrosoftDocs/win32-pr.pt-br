---
description: Procura o destino de um link do Shell, mesmo que o destino tenha sido movido ou renomeado.
ms.assetid: 60e119be-8e45-4f63-a381-cad048de0765
title: Método ShellLinkObject. resolve (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellLinkObject.Resolve
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: b1cb0760f1ee19acfa10208711e73919fd084ecf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968212"
---
# <a name="shelllinkobjectresolve-method"></a><span data-ttu-id="49045-103">Método ShellLinkObject. resolve</span><span class="sxs-lookup"><span data-stu-id="49045-103">ShellLinkObject.Resolve method</span></span>

<span data-ttu-id="49045-104">Procura o destino de um link do Shell, mesmo que o destino tenha sido movido ou renomeado.</span><span class="sxs-lookup"><span data-stu-id="49045-104">Looks for the target of a Shell link, even if the target has been moved or renamed.</span></span>

## <a name="syntax"></a><span data-ttu-id="49045-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="49045-105">Syntax</span></span>


```JScript
iRetVal = ShellLinkObject.Resolve(
  fFlags
)
```



## <a name="parameters"></a><span data-ttu-id="49045-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="49045-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49045-107">*fFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="49045-107">*fFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49045-108">Tipo: **inteiro**</span><span class="sxs-lookup"><span data-stu-id="49045-108">Type: **Integer**</span></span>

<span data-ttu-id="49045-109">Sinalizadores que especificam a ação a ser executada.</span><span class="sxs-lookup"><span data-stu-id="49045-109">Flags that specify the action to be taken.</span></span> <span data-ttu-id="49045-110">Isso pode ser uma combinação dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="49045-110">This can be a combination of the following values:</span></span>

<dt>



 <span data-ttu-id="49045-111">(1)</span><span class="sxs-lookup"><span data-stu-id="49045-111">(1)</span></span>


</dt> <dd>

<span data-ttu-id="49045-112">Não exibir uma caixa de diálogo se o link não puder ser resolvido.</span><span class="sxs-lookup"><span data-stu-id="49045-112">Do not display a dialog box if the link cannot be resolved.</span></span> <span data-ttu-id="49045-113">Quando esse sinalizador é definido, a palavra de ordem superior de *fFlags* especifica uma duração de tempo limite, em milissegundos.</span><span class="sxs-lookup"><span data-stu-id="49045-113">When this flag is set, the high-order word of *fFlags* specifies a time-out duration, in milliseconds.</span></span> <span data-ttu-id="49045-114">O método retornará se o link não puder ser resolvido dentro da duração do tempo limite.</span><span class="sxs-lookup"><span data-stu-id="49045-114">The method returns if the link cannot be resolved within the time-out duration.</span></span> <span data-ttu-id="49045-115">Se a palavra de ordem superior for definida como zero, a duração do tempo limite padrão será de 3000 milissegundos (3 segundos).</span><span class="sxs-lookup"><span data-stu-id="49045-115">If the high-order word is set to zero, the time-out duration defaults to 3000 milliseconds (3 seconds).</span></span>

</dd> <dt>



 <span data-ttu-id="49045-116">(4)</span><span class="sxs-lookup"><span data-stu-id="49045-116">(4)</span></span>


</dt> <dd>

<span data-ttu-id="49045-117">Se o link tiver sido alterado, atualize seu caminho e a lista de identificadores.</span><span class="sxs-lookup"><span data-stu-id="49045-117">If the link has changed, update its path and list of identifiers.</span></span>

</dd> <dt>



 <span data-ttu-id="49045-118">(8)</span><span class="sxs-lookup"><span data-stu-id="49045-118">(8)</span></span>


</dt> <dd>

<span data-ttu-id="49045-119">Não atualize as informações do link.</span><span class="sxs-lookup"><span data-stu-id="49045-119">Do not update the link information.</span></span>

</dd> <dt>



 <span data-ttu-id="49045-120">(16)</span><span class="sxs-lookup"><span data-stu-id="49045-120">(16)</span></span>


</dt> <dd>

<span data-ttu-id="49045-121">Não execute a heurística da pesquisa.</span><span class="sxs-lookup"><span data-stu-id="49045-121">Do not execute the search heuristics.</span></span>

</dd> <dt>



 <span data-ttu-id="49045-122">(32)</span><span class="sxs-lookup"><span data-stu-id="49045-122">(32)</span></span>


</dt> <dd>

<span data-ttu-id="49045-123">Não use o rastreamento de link distribuído.</span><span class="sxs-lookup"><span data-stu-id="49045-123">Do not use distributed link tracking.</span></span>

</dd> <dt>



 <span data-ttu-id="49045-124">(64)</span><span class="sxs-lookup"><span data-stu-id="49045-124">(64)</span></span>


</dt> <dd>

<span data-ttu-id="49045-125">Desabilitar o rastreamento de link distribuído.</span><span class="sxs-lookup"><span data-stu-id="49045-125">Disable distributed link tracking.</span></span> <span data-ttu-id="49045-126">Por padrão, o rastreamento de link distribuído controla a mídia removível em vários dispositivos com base no nome do volume.</span><span class="sxs-lookup"><span data-stu-id="49045-126">By default, distributed link tracking tracks removable media across multiple devices based on the volume name.</span></span> <span data-ttu-id="49045-127">Ele também usa o caminho UNC para rastrear sistemas de arquivos remotos cuja letra da unidade foi alterada.</span><span class="sxs-lookup"><span data-stu-id="49045-127">It also uses the UNC path to track remote file systems whose drive letter has changed.</span></span> <span data-ttu-id="49045-128">A definição desse sinalizador desabilita os dois tipos de controle.</span><span class="sxs-lookup"><span data-stu-id="49045-128">Setting this flag disables both types of tracking.</span></span>

</dd> <dt>



 <span data-ttu-id="49045-129">(128)</span><span class="sxs-lookup"><span data-stu-id="49045-129">(128)</span></span>


</dt> <dd>

<span data-ttu-id="49045-130">Chame o Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="49045-130">Call the Windows Installer.</span></span>

</dd> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="49045-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="49045-131">Remarks</span></span>

<span data-ttu-id="49045-132">Esse método é essencialmente idêntico na funcionalidade a ser [**resolvida**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-resolve).</span><span class="sxs-lookup"><span data-stu-id="49045-132">This method is essentially identical in functionality to [**Resolve**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-resolve).</span></span> <span data-ttu-id="49045-133">Para obter mais informações sobre a resolução de links, consulte a seção comentários da página.</span><span class="sxs-lookup"><span data-stu-id="49045-133">For further discussion of link resolution, see the Remarks section of that page.</span></span>

## <a name="examples"></a><span data-ttu-id="49045-134">Exemplos</span><span class="sxs-lookup"><span data-stu-id="49045-134">Examples</span></span>

<span data-ttu-id="49045-135">O exemplo a seguir mostra o uso apropriado desse método para JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="49045-135">The following example shows the proper usage of this method for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="49045-136">JScript</span><span class="sxs-lookup"><span data-stu-id="49045-136">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellLinkObjectResolveJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder;
        var ssfPROGRAMS = 2;
        
        objFolder = objShell.NameSpace(ssfPROGRAMS);
        if (objFolder != null)
        {
            var objFolderItem;
            
            objFolderItem = objFolder.ParseName("Internet Explorer.lnk");
            if (objFolderItem != null)
            {
                var objShellLink;
                
                objShellLink = objFolderItem.GetLink;
                if (objShellLink != null)
                {
                    objShellLink.Resolve(1);
                }
            }
        }
    }
</script>
```



<span data-ttu-id="49045-137">VBScript</span><span class="sxs-lookup"><span data-stu-id="49045-137">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellLinkObjectResolveVB()
        dim objShell
        dim objFolder
        dim ssfPROGRAMS
        
        ssfPROGRAMS = 2
        set objShell = CreateObject("shell.application")
        set objFolder = objShell.NameSpace(ssfPROGRAMS)
            if (not objFolder is nothing) then
                dim objFolderItem
                
                set objFolderItem = objFolder.ParseName("Internet Explorer.lnk")
                    if (not objFolderItem is nothing) then
                        dim objShellLink
                        
                        set objShellLink = objFolderItem.GetLink
                            if (not objShellLink is nothing) then
                                objShellLink.Resolve(1)
                            end if
                        set objShellLink = nothing
                    end if
                set objFolderItem = nothing
            end if
        set objFolder = nothing
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="49045-138">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="49045-138">Visual Basic:</span></span>


```VB
Private Sub fnShellLinkObjectResolveVB()
    Dim objShell  As Shell
    Dim objFolder As Folder
    
    Set objShell = New Shell
    Set objFolder = objShell.NameSpace(ssfPROGRAMS)
        If (Not objFolder Is Nothing) Then
            Dim objFolderItem As FolderItem
            
            Set objFolderItem = objFolder.ParseName("Internet Explorer.lnk")
                If (Not objFolderItem Is Nothing) Then
                    Dim objShellLink As ShellLinkObject
                    
                    Set objShellLink = objFolderItem.GetLink
                        If (Not objShellLink Is Nothing) Then
                            objShellLink.Resolve (1)
                        End If
                    Set objShellLink = Nothing
                End If
            Set objFolderItem = Nothing
        End If
    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="49045-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="49045-139">Requirements</span></span>



| <span data-ttu-id="49045-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="49045-140">Requirement</span></span> | <span data-ttu-id="49045-141">Valor</span><span class="sxs-lookup"><span data-stu-id="49045-141">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49045-142">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="49045-142">Minimum supported client</span></span><br/> | <span data-ttu-id="49045-143">Somente aplicativos de área de trabalho do Windows 2000 Professional com SP3 \[\]</span><span class="sxs-lookup"><span data-stu-id="49045-143">Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="49045-144">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="49045-144">Minimum supported server</span></span><br/> | <span data-ttu-id="49045-145">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="49045-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="49045-146">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="49045-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="49045-147"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="49045-147"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="49045-148">INSERI</span><span class="sxs-lookup"><span data-stu-id="49045-148">IDL</span></span><br/>                      | <dl> <span data-ttu-id="49045-149"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="49045-149"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="49045-150">DLL</span><span class="sxs-lookup"><span data-stu-id="49045-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="49045-151"><dt>Shell32.dll (versão 5,0 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="49045-151"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
