---
description: Método IShellDispatch2. FindPrinter – exibe a caixa de diálogo Localizar impressora.
ms.assetid: a3d1e810-f0cf-48ec-93da-5cc01117c5d4
title: Método IShellDispatch2. FindPrinter (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch2.FindPrinter
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 64a3975039255de76b3e59432b0848cc2cb1795b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117114"
---
# <a name="ishelldispatch2findprinter-method"></a><span data-ttu-id="72319-103">Método IShellDispatch2. FindPrinter</span><span class="sxs-lookup"><span data-stu-id="72319-103">IShellDispatch2.FindPrinter method</span></span>

<span data-ttu-id="72319-104">Exibe a caixa de diálogo **Localizar impressora** .</span><span class="sxs-lookup"><span data-stu-id="72319-104">Displays the **Find Printer** dialog box.</span></span>

## <a name="syntax"></a><span data-ttu-id="72319-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="72319-105">Syntax</span></span>


```JScript
iRetVal = IShellDispatch2.FindPrinter(
  [ sName ],
  [ sLocation ],
  [ sModel ]
)
```


```VB

IShellDispatch2.FindPrinter( _
  [ ByVal sName As BSTR ], _
  [ ByVal sLocation As BSTR ], _
  [ ByVal sModel As BSTR ] _
) As Integer
```





## <a name="parameters"></a><span data-ttu-id="72319-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="72319-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="72319-107">*sname* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="72319-107">*sName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="72319-108">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="72319-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="72319-109">Uma **cadeia de caracteres** que contém o nome da impressora.</span><span class="sxs-lookup"><span data-stu-id="72319-109">A **String** that contains the printer name.</span></span>

</dd> <dt>

<span data-ttu-id="72319-110">*sLocation* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="72319-110">*sLocation* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="72319-111">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="72319-111">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="72319-112">Uma **cadeia de caracteres** que contém o local da impressora.</span><span class="sxs-lookup"><span data-stu-id="72319-112">A **String** that contains the printer location.</span></span>

</dd> <dt>

<span data-ttu-id="72319-113">*sModel* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="72319-113">*sModel* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="72319-114">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="72319-114">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="72319-115">Uma **cadeia de caracteres** que contém o modelo de impressora.</span><span class="sxs-lookup"><span data-stu-id="72319-115">A **String** that contains the printer model.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="72319-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="72319-116">Remarks</span></span>

<span data-ttu-id="72319-117">Esse método é implementado e acessado por meio do método [**shell. FindPrinter**](./shell-findprinter.md) .</span><span class="sxs-lookup"><span data-stu-id="72319-117">This method is implemented and accessed through the [**Shell.FindPrinter**](./shell-findprinter.md) method.</span></span>

<span data-ttu-id="72319-118">Se você atribuir cadeias de caracteres a um ou mais dos parâmetros opcionais, eles serão exibidos como valores padrão no controle de edição associado quando a caixa de diálogo **Localizar impressora** for exibida.</span><span class="sxs-lookup"><span data-stu-id="72319-118">If you assign strings to one or more of the optional parameters, they are displayed as default values in the associated edit control when the **Find Printer** dialog box is displayed.</span></span> <span data-ttu-id="72319-119">O usuário pode aceitar ou substituir esses valores.</span><span class="sxs-lookup"><span data-stu-id="72319-119">The user can either accept or override these values.</span></span> <span data-ttu-id="72319-120">Se nenhum valor for atribuído a um parâmetro, a caixa de edição associada estará vazia e o usuário deverá inserir um valor.</span><span class="sxs-lookup"><span data-stu-id="72319-120">If no value is assigned to a parameter, the associated edit box is empty and the user must enter a value.</span></span>

<span data-ttu-id="72319-121">Este método não está disponível atualmente no Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="72319-121">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="72319-122">Exemplos</span><span class="sxs-lookup"><span data-stu-id="72319-122">Examples</span></span>

<span data-ttu-id="72319-123">Os exemplos a seguir mostram o uso de **FindPrinter** para exibir a caixa de diálogo **Localizar impressora** para um aplicativo específico.</span><span class="sxs-lookup"><span data-stu-id="72319-123">The following examples show the use of **FindPrinter** to display the **Find Printer** dialog box for a particular application.</span></span> <span data-ttu-id="72319-124">O uso é mostrado para JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="72319-124">Usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="72319-125">JScript</span><span class="sxs-lookup"><span data-stu-id="72319-125">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFindPrinterJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.FindPrinter();
    }
</script>
```



<span data-ttu-id="72319-126">VBScript</span><span class="sxs-lookup"><span data-stu-id="72319-126">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnFindPrinterVB()
        dim objShell
        dim bReturn

        set objShell = CreateObject("shell.application")
        objShell.FindPrinter()

        set objShell = nothing
    end function
</script>
```



## <a name="requirements"></a><span data-ttu-id="72319-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="72319-127">Requirements</span></span>



| <span data-ttu-id="72319-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="72319-128">Requirement</span></span> | <span data-ttu-id="72319-129">Valor</span><span class="sxs-lookup"><span data-stu-id="72319-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72319-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="72319-130">Minimum supported client</span></span><br/> | <span data-ttu-id="72319-131">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="72319-131">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="72319-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="72319-132">Minimum supported server</span></span><br/> | <span data-ttu-id="72319-133">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="72319-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="72319-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="72319-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="72319-135"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="72319-135"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="72319-136">INSERI</span><span class="sxs-lookup"><span data-stu-id="72319-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="72319-137"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="72319-137"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="72319-138">DLL</span><span class="sxs-lookup"><span data-stu-id="72319-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="72319-139"><dt>Shell32.dll (versão 5,0 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="72319-139"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
