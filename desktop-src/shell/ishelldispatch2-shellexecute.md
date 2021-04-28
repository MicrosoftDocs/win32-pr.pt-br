---
description: Método IShellDispatch2. ShellExecute-executa uma operação especificada em um arquivo especificado.
ms.assetid: a55e804c-ed7c-4b22-b86f-8e5653976654
title: Método IShellDispatch2. ShellExecute (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch2.ShellExecute
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 5c058275948d5d96805ae24a76389321d7c69b8e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117014"
---
# <a name="ishelldispatch2shellexecute-method"></a><span data-ttu-id="c2f95-103">Método IShellDispatch2. ShellExecute</span><span class="sxs-lookup"><span data-stu-id="c2f95-103">IShellDispatch2.ShellExecute method</span></span>

<span data-ttu-id="c2f95-104">Executa uma operação especificada em um arquivo especificado.</span><span class="sxs-lookup"><span data-stu-id="c2f95-104">Performs a specified operation on a specified file.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2f95-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c2f95-105">Syntax</span></span>


```JScript
iRetVal = IShellDispatch2.ShellExecute(
  sFile,
  [ vArguments ],
  [ vDirectory ],
  [ vOperation ],
  [ vShow ]
)
```


```VB

IShellDispatch2.ShellExecute( _
  ByVal sFile As BSTR, _
  [ ByVal vArguments As Variant ], _
  [ ByVal vDirectory As Variant ], _
  [ ByVal vOperation As Variant ], _
  [ ByVal vShow As Variant ] _
) As Integer
```





## <a name="parameters"></a><span data-ttu-id="c2f95-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c2f95-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2f95-107">*sfile* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c2f95-107">*sFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2f95-108">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="c2f95-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="c2f95-109">Uma **cadeia de caracteres** que contém o nome do arquivo no qual **ShellExecute** executará a ação especificada por *vOperation*.</span><span class="sxs-lookup"><span data-stu-id="c2f95-109">A **String** that contains the name of the file on which **ShellExecute** will perform the action specified by *vOperation*.</span></span>

</dd> <dt>

<span data-ttu-id="c2f95-110">*vArguments* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="c2f95-110">*vArguments* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c2f95-111">Tipo: **variante**</span><span class="sxs-lookup"><span data-stu-id="c2f95-111">Type: **Variant**</span></span>

<span data-ttu-id="c2f95-112">Uma cadeia de caracteres que contém valores de parâmetro para a operação.</span><span class="sxs-lookup"><span data-stu-id="c2f95-112">A string that contains parameter values for the operation.</span></span>

</dd> <dt>

<span data-ttu-id="c2f95-113">*vDirectory* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="c2f95-113">*vDirectory* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c2f95-114">Tipo: **variante**</span><span class="sxs-lookup"><span data-stu-id="c2f95-114">Type: **Variant**</span></span>

<span data-ttu-id="c2f95-115">O caminho totalmente qualificado do diretório que contém o arquivo especificado por *sfile*.</span><span class="sxs-lookup"><span data-stu-id="c2f95-115">The fully qualified path of the directory that contains the file specified by *sFile*.</span></span> <span data-ttu-id="c2f95-116">Se esse parâmetro não for especificado, o diretório de trabalho atual será usado.</span><span class="sxs-lookup"><span data-stu-id="c2f95-116">If this parameter is not specified, the current working directory is used.</span></span>

</dd> <dt>

<span data-ttu-id="c2f95-117">*vOperation* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="c2f95-117">*vOperation* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c2f95-118">Tipo: **variante**</span><span class="sxs-lookup"><span data-stu-id="c2f95-118">Type: **Variant**</span></span>

<span data-ttu-id="c2f95-119">A operação a ser executada.</span><span class="sxs-lookup"><span data-stu-id="c2f95-119">The operation to be performed.</span></span> <span data-ttu-id="c2f95-120">Esse valor é definido como uma das cadeias de caracteres de verbo com suporte no arquivo.</span><span class="sxs-lookup"><span data-stu-id="c2f95-120">This value is set to one of the verb strings that is supported by the file.</span></span> <span data-ttu-id="c2f95-121">Para obter uma discussão sobre verbos, consulte a seção comentários.</span><span class="sxs-lookup"><span data-stu-id="c2f95-121">For a discussion of verbs, see the Remarks section.</span></span> <span data-ttu-id="c2f95-122">Se esse parâmetro não for especificado, a operação padrão será executada.</span><span class="sxs-lookup"><span data-stu-id="c2f95-122">If this parameter is not specified, the default operation is performed.</span></span>

</dd> <dt>

<span data-ttu-id="c2f95-123">*vShow* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="c2f95-123">*vShow* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c2f95-124">Tipo: **variante**</span><span class="sxs-lookup"><span data-stu-id="c2f95-124">Type: **Variant**</span></span>

<span data-ttu-id="c2f95-125">Uma recomendação sobre como a janela do aplicativo deve ser exibida inicialmente.</span><span class="sxs-lookup"><span data-stu-id="c2f95-125">A recommendation as to how the application window should be displayed initially.</span></span> <span data-ttu-id="c2f95-126">O aplicativo pode ignorar essa recomendação.</span><span class="sxs-lookup"><span data-stu-id="c2f95-126">The application can ignore this recommendation.</span></span> <span data-ttu-id="c2f95-127">Esse parâmetro pode usar um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="c2f95-127">This parameter can be one of the following values.</span></span> <span data-ttu-id="c2f95-128">Se esse parâmetro não for especificado, o aplicativo usará seu valor padrão.</span><span class="sxs-lookup"><span data-stu-id="c2f95-128">If this parameter is not specified, the application uses its default value.</span></span>



| <span data-ttu-id="c2f95-129">Valor</span><span class="sxs-lookup"><span data-stu-id="c2f95-129">Value</span></span>                                                                                                                               | <span data-ttu-id="c2f95-130">Significado</span><span class="sxs-lookup"><span data-stu-id="c2f95-130">Meaning</span></span>                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c2f95-131"><dt></dt><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="c2f95-131"><dt></dt> <dt>0</dt></span></span> </dl>  | <span data-ttu-id="c2f95-132">Abra o aplicativo com uma janela oculta.</span><span class="sxs-lookup"><span data-stu-id="c2f95-132">Open the application with a hidden window.</span></span><br/>                                                                                                    |
| <dl> <span data-ttu-id="c2f95-133"><dt></dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="c2f95-133"><dt></dt> <dt>1</dt></span></span> </dl>  | <span data-ttu-id="c2f95-134">Abra o aplicativo com uma janela normal.</span><span class="sxs-lookup"><span data-stu-id="c2f95-134">Open the application with a normal window.</span></span> <span data-ttu-id="c2f95-135">Se a janela for minimizada ou maximizada, o sistema a restaurará para seu tamanho e posição originais.</span><span class="sxs-lookup"><span data-stu-id="c2f95-135">If the window is minimized or maximized, the system restores it to its original size and position.</span></span><br/> |
| <dl> <span data-ttu-id="c2f95-136"><dt></dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="c2f95-136"><dt></dt> <dt>2</dt></span></span> </dl>  | <span data-ttu-id="c2f95-137">Abra o aplicativo com uma janela minimizada.</span><span class="sxs-lookup"><span data-stu-id="c2f95-137">Open the application with a minimized window.</span></span><br/>                                                                                                 |
| <dl> <span data-ttu-id="c2f95-138"><dt></dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="c2f95-138"><dt></dt> <dt>3</dt></span></span> </dl>  | <span data-ttu-id="c2f95-139">Abra o aplicativo com uma janela maximizada.</span><span class="sxs-lookup"><span data-stu-id="c2f95-139">Open the application with a maximized window.</span></span><br/>                                                                                                 |
| <dl> <span data-ttu-id="c2f95-140"><dt></dt><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="c2f95-140"><dt></dt> <dt>4</dt></span></span> </dl>  | <span data-ttu-id="c2f95-141">Abra o aplicativo com sua janela em seu tamanho e posição mais recentes.</span><span class="sxs-lookup"><span data-stu-id="c2f95-141">Open the application with its window at its most recent size and position.</span></span> <span data-ttu-id="c2f95-142">A janela ativa permanece ativa.</span><span class="sxs-lookup"><span data-stu-id="c2f95-142">The active window remains active.</span></span><br/>                                  |
| <dl> <span data-ttu-id="c2f95-143"><dt></dt><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="c2f95-143"><dt></dt> <dt>5</dt></span></span> </dl>  | <span data-ttu-id="c2f95-144">Abra o aplicativo com sua janela em seu tamanho e posição atuais.</span><span class="sxs-lookup"><span data-stu-id="c2f95-144">Open the application with its window at its current size and position.</span></span><br/>                                                                        |
| <dl> <span data-ttu-id="c2f95-145"><dt></dt><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="c2f95-145"><dt></dt> <dt>7</dt></span></span> </dl>  | <span data-ttu-id="c2f95-146">Abra o aplicativo com uma janela minimizada.</span><span class="sxs-lookup"><span data-stu-id="c2f95-146">Open the application with a minimized window.</span></span> <span data-ttu-id="c2f95-147">A janela ativa permanece ativa.</span><span class="sxs-lookup"><span data-stu-id="c2f95-147">The active window remains active.</span></span><br/>                                                               |
| <dl> <span data-ttu-id="c2f95-148"><dt></dt><dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="c2f95-148"><dt></dt> <dt>10</dt></span></span> </dl> | <span data-ttu-id="c2f95-149">Abra o aplicativo com sua janela no estado padrão especificado pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c2f95-149">Open the application with its window in the default state specified by the application.</span></span><br/>                                                       |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c2f95-150">Comentários</span><span class="sxs-lookup"><span data-stu-id="c2f95-150">Remarks</span></span>

<span data-ttu-id="c2f95-151">Esse método é implementado e acessado por meio do método [**shell. ShellExecute**](./shell-shellexecute.md) .</span><span class="sxs-lookup"><span data-stu-id="c2f95-151">This method is implemented and accessed through the [**Shell.ShellExecute**](./shell-shellexecute.md) method.</span></span>

<span data-ttu-id="c2f95-152">Esse método é equivalente a iniciar um dos comandos associados ao menu de atalho de um arquivo.</span><span class="sxs-lookup"><span data-stu-id="c2f95-152">This method is equivalent to launching one of the commands associated with a file's shortcut menu.</span></span> <span data-ttu-id="c2f95-153">Cada comando é representado por uma cadeia de caracteres de verbo.</span><span class="sxs-lookup"><span data-stu-id="c2f95-153">Each command is represented by a verb string.</span></span> <span data-ttu-id="c2f95-154">O conjunto de verbos com suporte varia de arquivo para arquivo.</span><span class="sxs-lookup"><span data-stu-id="c2f95-154">The set of supported verbs varies from file to file.</span></span> <span data-ttu-id="c2f95-155">O verbo mais comumente suportado é "Open", que também é geralmente o verbo padrão.</span><span class="sxs-lookup"><span data-stu-id="c2f95-155">The most commonly supported verb is "open", which is also usually the default verb.</span></span> <span data-ttu-id="c2f95-156">Outros verbos podem ter suporte apenas em determinados tipos de arquivos.</span><span class="sxs-lookup"><span data-stu-id="c2f95-156">Other verbs might be supported by only certain types of files.</span></span> <span data-ttu-id="c2f95-157">Para obter mais informações sobre os verbos do Shell, consulte [iniciando aplicativos](launch.md) ou [estendendo menus de atalho](context.md).</span><span class="sxs-lookup"><span data-stu-id="c2f95-157">For further discussion of Shell verbs, see [Launching Applications](launch.md) or [Extending Shortcut Menus](context.md).</span></span>

<span data-ttu-id="c2f95-158">Este método não está disponível atualmente no Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="c2f95-158">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="c2f95-159">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c2f95-159">Examples</span></span>

<span data-ttu-id="c2f95-160">Os exemplos a seguir mostram o uso de **ShellExecute** para abrir o bloco de notas.</span><span class="sxs-lookup"><span data-stu-id="c2f95-160">The following examples show the use of **ShellExecute** to open Notepad.</span></span> <span data-ttu-id="c2f95-161">O uso é mostrado para JScript e VBScript.</span><span class="sxs-lookup"><span data-stu-id="c2f95-161">Usage is shown for JScript and VBScript.</span></span>

<span data-ttu-id="c2f95-162">JScript</span><span class="sxs-lookup"><span data-stu-id="c2f95-162">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellExecuteJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.ShellExecute("notepad.exe", "", "", "open", 1);
    }
</script>
```



<span data-ttu-id="c2f95-163">VBScript</span><span class="sxs-lookup"><span data-stu-id="c2f95-163">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellExecuteVB()
        dim objShell

        set objShell = CreateObject("shell.application")

        objShell.ShellExecute "notepad.exe", "", "", "open", 1

        set objShell = nothing
    end function
</script>
```



## <a name="requirements"></a><span data-ttu-id="c2f95-164">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c2f95-164">Requirements</span></span>



| <span data-ttu-id="c2f95-165">Requisito</span><span class="sxs-lookup"><span data-stu-id="c2f95-165">Requirement</span></span> | <span data-ttu-id="c2f95-166">Valor</span><span class="sxs-lookup"><span data-stu-id="c2f95-166">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2f95-167">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c2f95-167">Minimum supported client</span></span><br/> | <span data-ttu-id="c2f95-168">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="c2f95-168">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c2f95-169">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c2f95-169">Minimum supported server</span></span><br/> | <span data-ttu-id="c2f95-170">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c2f95-170">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="c2f95-171">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c2f95-171">Header</span></span><br/>                   | <dl> <span data-ttu-id="c2f95-172"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="c2f95-172"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="c2f95-173">INSERI</span><span class="sxs-lookup"><span data-stu-id="c2f95-173">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c2f95-174"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c2f95-174"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="c2f95-175">DLL</span><span class="sxs-lookup"><span data-stu-id="c2f95-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c2f95-176"><dt>Shell32.dll (versão 5,0 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="c2f95-176"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
