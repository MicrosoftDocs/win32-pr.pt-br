---
<span data-ttu-id="ca1f1-101">Descrição: método Shell. FindComputer-' exibe a caixa de diálogo resultados da pesquisa: computadores.</span><span class="sxs-lookup"><span data-stu-id="ca1f1-101">description: Shell.FindComputer method - 'Displays the Search Results: Computers dialog box.</span></span> <span data-ttu-id="ca1f1-102">A caixa de diálogo mostra o resultado da pesquisa de um computador especificado.</span><span class="sxs-lookup"><span data-stu-id="ca1f1-102">The dialog box shows the result of the search for a specified computer.'</span></span>
<span data-ttu-id="ca1f1-103">MS. AssetID: 0304b955-AFde-4de4-824a-9ec9c9530360 título: Shell. FindComputer método (shldisp. h) MS. Topic: referência MS. Date: 05/31/2018 topic_type:</span><span class="sxs-lookup"><span data-stu-id="ca1f1-103">ms.assetid: 0304b955-afde-4de4-824a-9ec9c9530360 title: Shell.FindComputer method (Shldisp.h) ms.topic: reference ms.date: 05/31/2018 topic_type:</span></span> 
- <span data-ttu-id="ca1f1-104">APIRef</span><span class="sxs-lookup"><span data-stu-id="ca1f1-104">APIRef</span></span>
- <span data-ttu-id="ca1f1-105">api_name kbSyntax:</span><span class="sxs-lookup"><span data-stu-id="ca1f1-105">kbSyntax api_name:</span></span> 
- <span data-ttu-id="ca1f1-106">Api_type do Shell. FindComputer:</span><span class="sxs-lookup"><span data-stu-id="ca1f1-106">Shell.FindComputer api_type:</span></span> 
- <span data-ttu-id="ca1f1-107">Api_location COM:</span><span class="sxs-lookup"><span data-stu-id="ca1f1-107">COM api_location:</span></span> 
- <span data-ttu-id="ca1f1-108">Shell32.dll</span><span class="sxs-lookup"><span data-stu-id="ca1f1-108">Shell32.dll</span></span>
---

# <a name="shellfindcomputer-method"></a><span data-ttu-id="ca1f1-109">Método Shell. FindComputer</span><span class="sxs-lookup"><span data-stu-id="ca1f1-109">Shell.FindComputer method</span></span>

<span data-ttu-id="ca1f1-110">Exibe a caixa de diálogo **resultados da pesquisa: computadores** .</span><span class="sxs-lookup"><span data-stu-id="ca1f1-110">Displays the **Search Results: Computers** dialog box.</span></span> <span data-ttu-id="ca1f1-111">A caixa de diálogo mostra o resultado da pesquisa de um computador especificado.</span><span class="sxs-lookup"><span data-stu-id="ca1f1-111">The dialog box shows the result of the search for a specified computer.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca1f1-112">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ca1f1-112">Syntax</span></span>


```JScript
Shell.FindComputer()
```


```VB

Shell.FindComputer()
```





## <a name="parameters"></a><span data-ttu-id="ca1f1-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ca1f1-113">Parameters</span></span>

<span data-ttu-id="ca1f1-114">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="ca1f1-114">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ca1f1-115">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="ca1f1-115">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="ca1f1-116">JScript</span><span class="sxs-lookup"><span data-stu-id="ca1f1-116">JScript</span></span>

<span data-ttu-id="ca1f1-117">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="ca1f1-117">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="ca1f1-118">VB</span><span class="sxs-lookup"><span data-stu-id="ca1f1-118">VB</span></span>

<span data-ttu-id="ca1f1-119">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="ca1f1-119">This method does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="ca1f1-120">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ca1f1-120">Examples</span></span>

<span data-ttu-id="ca1f1-121">O exemplo a seguir mostra **FindComputer** em uso.</span><span class="sxs-lookup"><span data-stu-id="ca1f1-121">The following example shows **FindComputer** in use.</span></span> <span data-ttu-id="ca1f1-122">O resultado desse código é o mesmo que pressionar o botão **Iniciar** , clicar em **Pesquisar**, clicar na opção **impressoras, computadores ou pessoas** e clicar em **um computador na rede**.</span><span class="sxs-lookup"><span data-stu-id="ca1f1-122">The result of this code is the same as pressing the **Start** button, clicking **Search**, clicking the **Printers, computers, or people** option, then clicking **A computer on the network**.</span></span> <span data-ttu-id="ca1f1-123">O uso adequado é mostrado para JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="ca1f1-123">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="ca1f1-124">JScript</span><span class="sxs-lookup"><span data-stu-id="ca1f1-124">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellFindComputerJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.FindComputer();
    }
</script>
```



<span data-ttu-id="ca1f1-125">VBScript</span><span class="sxs-lookup"><span data-stu-id="ca1f1-125">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellFindComputerVB()
        dim objShell
        dim ssfWINDOWS
        ssfWINDOWS = 36

        set objShell = CreateObject("shell.application")
        objShell.FindComputer

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="ca1f1-126">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="ca1f1-126">Visual Basic:</span></span>


```VB
Private Sub fnShellFindComputerVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objShell.FindComputer

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="ca1f1-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ca1f1-127">Requirements</span></span>



| <span data-ttu-id="ca1f1-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="ca1f1-128">Requirement</span></span> | <span data-ttu-id="ca1f1-129">Valor</span><span class="sxs-lookup"><span data-stu-id="ca1f1-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca1f1-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ca1f1-130">Minimum supported client</span></span><br/> | <span data-ttu-id="ca1f1-131">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="ca1f1-131">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="ca1f1-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ca1f1-132">Minimum supported server</span></span><br/> | <span data-ttu-id="ca1f1-133">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ca1f1-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="ca1f1-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ca1f1-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="ca1f1-135"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="ca1f1-135"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="ca1f1-136">INSERI</span><span class="sxs-lookup"><span data-stu-id="ca1f1-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ca1f1-137"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ca1f1-137"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="ca1f1-138">DLL</span><span class="sxs-lookup"><span data-stu-id="ca1f1-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ca1f1-139"><dt>Shell32.dll (versão 4,71 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="ca1f1-139"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




