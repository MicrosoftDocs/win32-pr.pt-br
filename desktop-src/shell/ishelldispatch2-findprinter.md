---
description: Exibe a caixa de diálogo Localizar impressora.
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
ms.openlocfilehash: 81124e3f0d04244b9b81e812e090bde25971c17c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164749"
---
# <a name="ishelldispatch2findprinter-method"></a><span data-ttu-id="4b1cb-103">Método IShellDispatch2. FindPrinter</span><span class="sxs-lookup"><span data-stu-id="4b1cb-103">IShellDispatch2.FindPrinter method</span></span>

<span data-ttu-id="4b1cb-104">Exibe a caixa de diálogo **Localizar impressora** .</span><span class="sxs-lookup"><span data-stu-id="4b1cb-104">Displays the **Find Printer** dialog box.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b1cb-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4b1cb-105">Syntax</span></span>


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





## <a name="parameters"></a><span data-ttu-id="4b1cb-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4b1cb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4b1cb-107">*sname* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="4b1cb-107">*sName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4b1cb-108">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="4b1cb-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="4b1cb-109">Uma **cadeia de caracteres** que contém o nome da impressora.</span><span class="sxs-lookup"><span data-stu-id="4b1cb-109">A **String** that contains the printer name.</span></span>

</dd> <dt>

<span data-ttu-id="4b1cb-110">*sLocation* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="4b1cb-110">*sLocation* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4b1cb-111">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="4b1cb-111">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="4b1cb-112">Uma **cadeia de caracteres** que contém o local da impressora.</span><span class="sxs-lookup"><span data-stu-id="4b1cb-112">A **String** that contains the printer location.</span></span>

</dd> <dt>

<span data-ttu-id="4b1cb-113">*sModel* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="4b1cb-113">*sModel* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4b1cb-114">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="4b1cb-114">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="4b1cb-115">Uma **cadeia de caracteres** que contém o modelo de impressora.</span><span class="sxs-lookup"><span data-stu-id="4b1cb-115">A **String** that contains the printer model.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4b1cb-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="4b1cb-116">Remarks</span></span>

<span data-ttu-id="4b1cb-117">Esse método é implementado e acessado por meio do método [**shell. FindPrinter**](./shell-findprinter.md) .</span><span class="sxs-lookup"><span data-stu-id="4b1cb-117">This method is implemented and accessed through the [**Shell.FindPrinter**](./shell-findprinter.md) method.</span></span>

<span data-ttu-id="4b1cb-118">Se você atribuir cadeias de caracteres a um ou mais dos parâmetros opcionais, eles serão exibidos como valores padrão no controle de edição associado quando a caixa de diálogo **Localizar impressora** for exibida.</span><span class="sxs-lookup"><span data-stu-id="4b1cb-118">If you assign strings to one or more of the optional parameters, they are displayed as default values in the associated edit control when the **Find Printer** dialog box is displayed.</span></span> <span data-ttu-id="4b1cb-119">O usuário pode aceitar ou substituir esses valores.</span><span class="sxs-lookup"><span data-stu-id="4b1cb-119">The user can either accept or override these values.</span></span> <span data-ttu-id="4b1cb-120">Se nenhum valor for atribuído a um parâmetro, a caixa de edição associada estará vazia e o usuário deverá inserir um valor.</span><span class="sxs-lookup"><span data-stu-id="4b1cb-120">If no value is assigned to a parameter, the associated edit box is empty and the user must enter a value.</span></span>

<span data-ttu-id="4b1cb-121">Este método não está disponível atualmente no Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="4b1cb-121">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="4b1cb-122">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4b1cb-122">Examples</span></span>

<span data-ttu-id="4b1cb-123">Os exemplos a seguir mostram o uso de **FindPrinter** para exibir a caixa de diálogo **Localizar impressora** para um aplicativo específico.</span><span class="sxs-lookup"><span data-stu-id="4b1cb-123">The following examples show the use of **FindPrinter** to display the **Find Printer** dialog box for a particular application.</span></span> <span data-ttu-id="4b1cb-124">O uso é mostrado para JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="4b1cb-124">Usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="4b1cb-125">JScript</span><span class="sxs-lookup"><span data-stu-id="4b1cb-125">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFindPrinterJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.FindPrinter();
    }
</script>
```



<span data-ttu-id="4b1cb-126">VBScript</span><span class="sxs-lookup"><span data-stu-id="4b1cb-126">VBScript:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="4b1cb-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4b1cb-127">Requirements</span></span>



| <span data-ttu-id="4b1cb-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="4b1cb-128">Requirement</span></span> | <span data-ttu-id="4b1cb-129">Valor</span><span class="sxs-lookup"><span data-stu-id="4b1cb-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b1cb-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4b1cb-130">Minimum supported client</span></span><br/> | <span data-ttu-id="4b1cb-131">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="4b1cb-131">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4b1cb-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4b1cb-132">Minimum supported server</span></span><br/> | <span data-ttu-id="4b1cb-133">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4b1cb-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="4b1cb-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4b1cb-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="4b1cb-135"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="4b1cb-135"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="4b1cb-136">INSERI</span><span class="sxs-lookup"><span data-stu-id="4b1cb-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4b1cb-137"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4b1cb-137"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="4b1cb-138">DLL</span><span class="sxs-lookup"><span data-stu-id="4b1cb-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4b1cb-139"><dt>Shell32.dll (versão 5,0 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="4b1cb-139"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
