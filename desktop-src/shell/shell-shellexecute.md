---
description: Executa uma operação especificada em um arquivo especificado.
ms.assetid: 62E59A1C-51BD-4864-AF09-35FFD49FAB9D
title: Método Shell.ShellExecute (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.ShellExecute
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 83ab9741199bff675245f15dc2ad1ffb20592a35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104967984"
---
# <a name="shellshellexecute-method"></a><span data-ttu-id="9e8b8-103">Método Shell. ShellExecute</span><span class="sxs-lookup"><span data-stu-id="9e8b8-103">Shell.ShellExecute method</span></span>

<span data-ttu-id="9e8b8-104">Executa uma operação especificada em um arquivo especificado.</span><span class="sxs-lookup"><span data-stu-id="9e8b8-104">Performs a specified operation on a specified file.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e8b8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9e8b8-105">Syntax</span></span>

<span data-ttu-id="9e8b8-106">JScript</span><span class="sxs-lookup"><span data-stu-id="9e8b8-106">JScript:</span></span>

```js
iRetVal = Shell.ShellExecute(
  sFile,
  [ vArguments ],
  [ vDirectory ],
  [ vOperation ],
  [ vShow ]
);
```

<span data-ttu-id="9e8b8-107">VBScript</span><span class="sxs-lookup"><span data-stu-id="9e8b8-107">VBScript:</span></span>

```vb
iRetVal = Shell.ShellExecute( _
  sFile, _
  [ ByVal vArguments ], _
  [ ByVal vDirectory ], _
  [ ByVal vOperation ], _
  [ ByVal vShow ] _
)
```

<span data-ttu-id="9e8b8-108">VB:</span><span class="sxs-lookup"><span data-stu-id="9e8b8-108">VB:</span></span>

```vb
Shell.ShellExecute( _
  ByVal sFile As BSTR, _
  [ ByVal vArguments As Variant ], _
  [ ByVal vDirectory As Variant ], _
  [ ByVal vOperation As Variant ], _
  [ ByVal vShow As Variant ] _
) As Integer
```

## <a name="parameters"></a><span data-ttu-id="9e8b8-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9e8b8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e8b8-110">*sfile* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9e8b8-110">*sFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e8b8-111">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="9e8b8-111">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="9e8b8-112">Uma **cadeia de caracteres** que contém o nome do arquivo no qual **ShellExecute** executará a ação especificada por *vOperation*.</span><span class="sxs-lookup"><span data-stu-id="9e8b8-112">A **String** that contains the name of the file on which **ShellExecute** will perform the action specified by *vOperation*.</span></span>

</dd> <dt>

<span data-ttu-id="9e8b8-113">*vArguments* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="9e8b8-113">*vArguments* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9e8b8-114">Tipo: **variante**</span><span class="sxs-lookup"><span data-stu-id="9e8b8-114">Type: **Variant**</span></span>

<span data-ttu-id="9e8b8-115">Uma cadeia de caracteres que contém valores de parâmetro para a operação.</span><span class="sxs-lookup"><span data-stu-id="9e8b8-115">A string that contains parameter values for the operation.</span></span>

</dd> <dt>

<span data-ttu-id="9e8b8-116">*vDirectory* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="9e8b8-116">*vDirectory* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9e8b8-117">Tipo: **variante**</span><span class="sxs-lookup"><span data-stu-id="9e8b8-117">Type: **Variant**</span></span>

<span data-ttu-id="9e8b8-118">O caminho totalmente qualificado do diretório que contém o arquivo especificado por *sfile*.</span><span class="sxs-lookup"><span data-stu-id="9e8b8-118">The fully qualified path of the directory that contains the file specified by *sFile*.</span></span> <span data-ttu-id="9e8b8-119">Se esse parâmetro não for especificado, o diretório de trabalho atual será usado.</span><span class="sxs-lookup"><span data-stu-id="9e8b8-119">If this parameter is not specified, the current working directory is used.</span></span>

</dd> <dt>

<span data-ttu-id="9e8b8-120">*vOperation* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="9e8b8-120">*vOperation* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9e8b8-121">Tipo: **variante**</span><span class="sxs-lookup"><span data-stu-id="9e8b8-121">Type: **Variant**</span></span>

<span data-ttu-id="9e8b8-122">A operação a ser executada.</span><span class="sxs-lookup"><span data-stu-id="9e8b8-122">The operation to be performed.</span></span> <span data-ttu-id="9e8b8-123">Esse valor é definido como uma das cadeias de caracteres de verbo com suporte no arquivo.</span><span class="sxs-lookup"><span data-stu-id="9e8b8-123">This value is set to one of the verb strings that is supported by the file.</span></span> <span data-ttu-id="9e8b8-124">Para obter uma discussão sobre verbos, consulte a seção comentários.</span><span class="sxs-lookup"><span data-stu-id="9e8b8-124">For a discussion of verbs, see the Remarks section.</span></span> <span data-ttu-id="9e8b8-125">Se esse parâmetro não for especificado, a operação padrão será executada.</span><span class="sxs-lookup"><span data-stu-id="9e8b8-125">If this parameter is not specified, the default operation is performed.</span></span>

</dd> <dt>

<span data-ttu-id="9e8b8-126">*vShow* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="9e8b8-126">*vShow* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9e8b8-127">Tipo: **variante**</span><span class="sxs-lookup"><span data-stu-id="9e8b8-127">Type: **Variant**</span></span>

<span data-ttu-id="9e8b8-128">Uma recomendação sobre como a janela do aplicativo deve ser exibida inicialmente.</span><span class="sxs-lookup"><span data-stu-id="9e8b8-128">A recommendation as to how the application window should be displayed initially.</span></span> <span data-ttu-id="9e8b8-129">O aplicativo pode ignorar essa recomendação.</span><span class="sxs-lookup"><span data-stu-id="9e8b8-129">The application can ignore this recommendation.</span></span> <span data-ttu-id="9e8b8-130">Esse parâmetro pode usar um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="9e8b8-130">This parameter can be one of the following values.</span></span> <span data-ttu-id="9e8b8-131">Se esse parâmetro não for especificado, o aplicativo usará seu valor padrão.</span><span class="sxs-lookup"><span data-stu-id="9e8b8-131">If this parameter is not specified, the application uses its default value.</span></span>



| <span data-ttu-id="9e8b8-132">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8b8-132">Value</span></span>                                                                                                                               | <span data-ttu-id="9e8b8-133">Significado</span><span class="sxs-lookup"><span data-stu-id="9e8b8-133">Meaning</span></span>                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9e8b8-134"><dt></dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="9e8b8-134"><dt></dt> <dt>0</dt></span></span> </dl>  | <span data-ttu-id="9e8b8-135">Abra o aplicativo com uma janela oculta.</span><span class="sxs-lookup"><span data-stu-id="9e8b8-135">Open the application with a hidden window.</span></span><br/>                                                                                                    |
| <dl> <span data-ttu-id="9e8b8-136"><dt></dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="9e8b8-136"><dt></dt> <dt>1</dt></span></span> </dl>  | <span data-ttu-id="9e8b8-137">Abra o aplicativo com uma janela normal.</span><span class="sxs-lookup"><span data-stu-id="9e8b8-137">Open the application with a normal window.</span></span> <span data-ttu-id="9e8b8-138">Se a janela for minimizada ou maximizada, o sistema a restaurará para seu tamanho e posição originais.</span><span class="sxs-lookup"><span data-stu-id="9e8b8-138">If the window is minimized or maximized, the system restores it to its original size and position.</span></span><br/> |
| <dl> <span data-ttu-id="9e8b8-139"><dt></dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="9e8b8-139"><dt></dt> <dt>2</dt></span></span> </dl>  | <span data-ttu-id="9e8b8-140">Abra o aplicativo com uma janela minimizada.</span><span class="sxs-lookup"><span data-stu-id="9e8b8-140">Open the application with a minimized window.</span></span><br/>                                                                                                 |
| <dl> <span data-ttu-id="9e8b8-141"><dt></dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="9e8b8-141"><dt></dt> <dt>3</dt></span></span> </dl>  | <span data-ttu-id="9e8b8-142">Abra o aplicativo com uma janela maximizada.</span><span class="sxs-lookup"><span data-stu-id="9e8b8-142">Open the application with a maximized window.</span></span><br/>                                                                                                 |
| <dl> <span data-ttu-id="9e8b8-143"><dt></dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="9e8b8-143"><dt></dt> <dt>4</dt></span></span> </dl>  | <span data-ttu-id="9e8b8-144">Abra o aplicativo com sua janela em seu tamanho e posição mais recentes.</span><span class="sxs-lookup"><span data-stu-id="9e8b8-144">Open the application with its window at its most recent size and position.</span></span> <span data-ttu-id="9e8b8-145">A janela ativa permanece ativa.</span><span class="sxs-lookup"><span data-stu-id="9e8b8-145">The active window remains active.</span></span><br/>                                  |
| <dl> <span data-ttu-id="9e8b8-146"><dt></dt><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="9e8b8-146"><dt></dt> <dt>5</dt></span></span> </dl>  | <span data-ttu-id="9e8b8-147">Abra o aplicativo com sua janela em seu tamanho e posição atuais.</span><span class="sxs-lookup"><span data-stu-id="9e8b8-147">Open the application with its window at its current size and position.</span></span><br/>                                                                        |
| <dl> <span data-ttu-id="9e8b8-148"><dt></dt><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="9e8b8-148"><dt></dt> <dt>7</dt></span></span> </dl>  | <span data-ttu-id="9e8b8-149">Abra o aplicativo com uma janela minimizada.</span><span class="sxs-lookup"><span data-stu-id="9e8b8-149">Open the application with a minimized window.</span></span> <span data-ttu-id="9e8b8-150">A janela ativa permanece ativa.</span><span class="sxs-lookup"><span data-stu-id="9e8b8-150">The active window remains active.</span></span><br/>                                                               |
| <dl> <span data-ttu-id="9e8b8-151"><dt></dt><dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="9e8b8-151"><dt></dt> <dt>10</dt></span></span> </dl> | <span data-ttu-id="9e8b8-152">Abra o aplicativo com sua janela no estado padrão especificado pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="9e8b8-152">Open the application with its window in the default state specified by the application.</span></span><br/>                                                       |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9e8b8-153">Comentários</span><span class="sxs-lookup"><span data-stu-id="9e8b8-153">Remarks</span></span>

<span data-ttu-id="9e8b8-154">Esse método é equivalente a iniciar um dos comandos associados ao menu de atalho de um arquivo.</span><span class="sxs-lookup"><span data-stu-id="9e8b8-154">This method is equivalent to launching one of the commands associated with a file's shortcut menu.</span></span> <span data-ttu-id="9e8b8-155">Cada comando é representado por uma cadeia de caracteres de verbo.</span><span class="sxs-lookup"><span data-stu-id="9e8b8-155">Each command is represented by a verb string.</span></span> <span data-ttu-id="9e8b8-156">O conjunto de verbos com suporte varia de arquivo para arquivo.</span><span class="sxs-lookup"><span data-stu-id="9e8b8-156">The set of supported verbs varies from file to file.</span></span> <span data-ttu-id="9e8b8-157">O verbo mais comumente suportado é "Open", que também é geralmente o verbo padrão.</span><span class="sxs-lookup"><span data-stu-id="9e8b8-157">The most commonly supported verb is "open", which is also usually the default verb.</span></span> <span data-ttu-id="9e8b8-158">Outros verbos podem ter suporte apenas em determinados tipos de arquivos.</span><span class="sxs-lookup"><span data-stu-id="9e8b8-158">Other verbs might be supported by only certain types of files.</span></span> <span data-ttu-id="9e8b8-159">Para obter mais informações sobre os verbos do Shell, consulte [iniciando aplicativos](launch.md) ou [estendendo menus de atalho](context.md).</span><span class="sxs-lookup"><span data-stu-id="9e8b8-159">For further discussion of Shell verbs, see [Launching Applications](launch.md) or [Extending Shortcut Menus](context.md).</span></span>

<span data-ttu-id="9e8b8-160">Este método não está disponível atualmente no Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="9e8b8-160">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="9e8b8-161">Exemplos</span><span class="sxs-lookup"><span data-stu-id="9e8b8-161">Examples</span></span>

<span data-ttu-id="9e8b8-162">Os exemplos a seguir mostram o uso de **ShellExecute** para abrir o bloco de notas.</span><span class="sxs-lookup"><span data-stu-id="9e8b8-162">The following examples show the use of **ShellExecute** to open Notepad.</span></span> <span data-ttu-id="9e8b8-163">O uso é mostrado para JScript e VBScript.</span><span class="sxs-lookup"><span data-stu-id="9e8b8-163">Usage is shown for JScript and VBScript.</span></span>

<span data-ttu-id="9e8b8-164">JScript</span><span class="sxs-lookup"><span data-stu-id="9e8b8-164">JScript:</span></span>


```JScript
function ShellExecuteJS()
{
    var objShell = new ActiveXObject("Shell.Application");
    objShell.ShellExecute("notepad.exe", "", "", "open", 1);
}
```

<span data-ttu-id="9e8b8-165">VBScript</span><span class="sxs-lookup"><span data-stu-id="9e8b8-165">VBScript:</span></span>

```vb
Function ShellExecuteVB()
    Dim objShell
    Set objShell = CreateObject("Shell.Application")
    Call objShell.ShellExecute("notepad.exe", "", "", "open", 1)
End Function
```



## <a name="requirements"></a><span data-ttu-id="9e8b8-166">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9e8b8-166">Requirements</span></span>



| <span data-ttu-id="9e8b8-167">Requisito</span><span class="sxs-lookup"><span data-stu-id="9e8b8-167">Requirement</span></span> | <span data-ttu-id="9e8b8-168">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8b8-168">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e8b8-169">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9e8b8-169">Minimum supported client</span></span><br/> | <span data-ttu-id="9e8b8-170">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="9e8b8-170">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9e8b8-171">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9e8b8-171">Minimum supported server</span></span><br/> | <span data-ttu-id="9e8b8-172">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9e8b8-172">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="9e8b8-173">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9e8b8-173">Header</span></span><br/>                   | <dl> <span data-ttu-id="9e8b8-174"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="9e8b8-174"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="9e8b8-175">INSERI</span><span class="sxs-lookup"><span data-stu-id="9e8b8-175">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9e8b8-176"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9e8b8-176"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="9e8b8-177">DLL</span><span class="sxs-lookup"><span data-stu-id="9e8b8-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9e8b8-178"><dt>Shell32.dll (versão 5,0 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="9e8b8-178"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
