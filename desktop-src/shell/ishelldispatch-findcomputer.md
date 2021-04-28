---
<span data-ttu-id="b6b6d-101">Descrição: método IShellDispatch. FindComputer-' exibe a caixa de diálogo resultados da pesquisa: computadores.</span><span class="sxs-lookup"><span data-stu-id="b6b6d-101">description: IShellDispatch.FindComputer method - 'Displays the Search Results: Computers dialog box.</span></span> <span data-ttu-id="b6b6d-102">A caixa de diálogo mostra o resultado da pesquisa de um computador especificado.</span><span class="sxs-lookup"><span data-stu-id="b6b6d-102">The dialog box shows the result of the search for a specified computer.'</span></span>
<span data-ttu-id="b6b6d-103">MS. AssetID: 9B687A8A-BB29-49a0-8AE3-11A75FAF3257 título: IShellDispatch. FindComputer método (shldisp. h) MS. Topic: referência MS. Date: 05/31/2018 topic_type:</span><span class="sxs-lookup"><span data-stu-id="b6b6d-103">ms.assetid: 9B687A8A-BB29-49a0-8AE3-11A75FAF3257 title: IShellDispatch.FindComputer method (Shldisp.h) ms.topic: reference ms.date: 05/31/2018 topic_type:</span></span> 
- <span data-ttu-id="b6b6d-104">APIRef</span><span class="sxs-lookup"><span data-stu-id="b6b6d-104">APIRef</span></span>
- <span data-ttu-id="b6b6d-105">api_name kbSyntax:</span><span class="sxs-lookup"><span data-stu-id="b6b6d-105">kbSyntax api_name:</span></span> 
- <span data-ttu-id="b6b6d-106">IShellDispatch. FindComputer api_type:</span><span class="sxs-lookup"><span data-stu-id="b6b6d-106">IShellDispatch.FindComputer api_type:</span></span> 
- <span data-ttu-id="b6b6d-107">Api_location COM:</span><span class="sxs-lookup"><span data-stu-id="b6b6d-107">COM api_location:</span></span> 
- <span data-ttu-id="b6b6d-108">Shell32.dll</span><span class="sxs-lookup"><span data-stu-id="b6b6d-108">Shell32.dll</span></span>
---

# <a name="ishelldispatchfindcomputer-method"></a><span data-ttu-id="b6b6d-109">Método IShellDispatch. FindComputer</span><span class="sxs-lookup"><span data-stu-id="b6b6d-109">IShellDispatch.FindComputer method</span></span>

<span data-ttu-id="b6b6d-110">Exibe a caixa de diálogo **resultados da pesquisa: computadores** .</span><span class="sxs-lookup"><span data-stu-id="b6b6d-110">Displays the **Search Results: Computers** dialog box.</span></span> <span data-ttu-id="b6b6d-111">A caixa de diálogo mostra o resultado da pesquisa de um computador especificado.</span><span class="sxs-lookup"><span data-stu-id="b6b6d-111">The dialog box shows the result of the search for a specified computer.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6b6d-112">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b6b6d-112">Syntax</span></span>


```JScript
IShellDispatch.FindComputer()
```


```VB

IShellDispatch.FindComputer()
```





## <a name="parameters"></a><span data-ttu-id="b6b6d-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b6b6d-113">Parameters</span></span>

<span data-ttu-id="b6b6d-114">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="b6b6d-114">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b6b6d-115">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="b6b6d-115">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="b6b6d-116">JScript</span><span class="sxs-lookup"><span data-stu-id="b6b6d-116">JScript</span></span>

<span data-ttu-id="b6b6d-117">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="b6b6d-117">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="b6b6d-118">VB</span><span class="sxs-lookup"><span data-stu-id="b6b6d-118">VB</span></span>

<span data-ttu-id="b6b6d-119">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="b6b6d-119">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b6b6d-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="b6b6d-120">Remarks</span></span>

<span data-ttu-id="b6b6d-121">Esse método é implementado e acessado por meio do método [**shell. FindComputer**](shell-findcomputer.md) .</span><span class="sxs-lookup"><span data-stu-id="b6b6d-121">This method is implemented and accessed through the [**Shell.FindComputer**](shell-findcomputer.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="b6b6d-122">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b6b6d-122">Examples</span></span>

<span data-ttu-id="b6b6d-123">Os exemplos a seguir mostram o uso de **FindComputer** em JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="b6b6d-123">The following examples show the use of **FindComputer** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="b6b6d-124">JScript</span><span class="sxs-lookup"><span data-stu-id="b6b6d-124">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellFindComputerJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.FindComputer();
    }
</script>
```



<span data-ttu-id="b6b6d-125">VBScript</span><span class="sxs-lookup"><span data-stu-id="b6b6d-125">VBScript:</span></span>


```VB
 <script language="VBScript">
    function fnShellFindComputerVB()
        dim objShell
        dim ssfWINDOWS
        ssfWINDOWS = 36

        set objShell = CreateObject("shell.application")
        objshell.FindComputer

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="b6b6d-126">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="b6b6d-126">Visual Basic:</span></span>


```VB
Private Sub fnShellFindComputerVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objshell.FindComputer

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="b6b6d-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b6b6d-127">Requirements</span></span>



| <span data-ttu-id="b6b6d-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="b6b6d-128">Requirement</span></span> | <span data-ttu-id="b6b6d-129">Valor</span><span class="sxs-lookup"><span data-stu-id="b6b6d-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6b6d-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b6b6d-130">Minimum supported client</span></span><br/> | <span data-ttu-id="b6b6d-131">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="b6b6d-131">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="b6b6d-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b6b6d-132">Minimum supported server</span></span><br/> | <span data-ttu-id="b6b6d-133">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b6b6d-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="b6b6d-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b6b6d-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="b6b6d-135"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b6b6d-135"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="b6b6d-136">INSERI</span><span class="sxs-lookup"><span data-stu-id="b6b6d-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b6b6d-137"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b6b6d-137"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="b6b6d-138">DLL</span><span class="sxs-lookup"><span data-stu-id="b6b6d-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b6b6d-139"><dt>Shell32.dll (versão 4,71 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="b6b6d-139"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




