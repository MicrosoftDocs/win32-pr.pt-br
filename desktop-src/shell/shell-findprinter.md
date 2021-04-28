---
description: Método Shell. FindPrinter – exibe a caixa de diálogo Localizar impressora.
ms.assetid: 61C700CF-623B-4c99-A211-AC26A1E4AE85
title: Método Shell. FindPrinter (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.FindPrinter
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 17d04b60de2b52ca3d2f17fbdccf7de93ac095b3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104304"
---
# <a name="shellfindprinter-method"></a><span data-ttu-id="5857e-103">Método Shell. FindPrinter</span><span class="sxs-lookup"><span data-stu-id="5857e-103">Shell.FindPrinter method</span></span>

<span data-ttu-id="5857e-104">Exibe a caixa de diálogo **Localizar impressora** .</span><span class="sxs-lookup"><span data-stu-id="5857e-104">Displays the **Find Printer** dialog box.</span></span>

## <a name="syntax"></a><span data-ttu-id="5857e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5857e-105">Syntax</span></span>


```JScript
iRetVal = Shell.FindPrinter(
  [ sName ],
  [ sLocation ],
  [ sModel ]
)
```


```VB

Shell.FindPrinter( _
  [ ByVal sName As BSTR ], _
  [ ByVal sLocation As BSTR ], _
  [ ByVal sModel As BSTR ] _
) As Integer
```





## <a name="parameters"></a><span data-ttu-id="5857e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5857e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5857e-107">*sname* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="5857e-107">*sName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5857e-108">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="5857e-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="5857e-109">Uma **cadeia de caracteres** que contém o nome da impressora.</span><span class="sxs-lookup"><span data-stu-id="5857e-109">A **String** that contains the printer name.</span></span>

</dd> <dt>

<span data-ttu-id="5857e-110">*sLocation* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="5857e-110">*sLocation* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5857e-111">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="5857e-111">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="5857e-112">Uma **cadeia de caracteres** que contém o local da impressora.</span><span class="sxs-lookup"><span data-stu-id="5857e-112">A **String** that contains the printer location.</span></span>

</dd> <dt>

<span data-ttu-id="5857e-113">*sModel* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="5857e-113">*sModel* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5857e-114">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="5857e-114">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="5857e-115">Uma **cadeia de caracteres** que contém o modelo de impressora.</span><span class="sxs-lookup"><span data-stu-id="5857e-115">A **String** that contains the printer model.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5857e-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="5857e-116">Remarks</span></span>

<span data-ttu-id="5857e-117">Se você atribuir cadeias de caracteres a um ou mais dos parâmetros opcionais, eles serão exibidos como valores padrão no controle de edição associado quando a caixa de diálogo **Localizar impressora** for exibida.</span><span class="sxs-lookup"><span data-stu-id="5857e-117">If you assign strings to one or more of the optional parameters, they are displayed as default values in the associated edit control when the **Find Printer** dialog box is displayed.</span></span> <span data-ttu-id="5857e-118">O usuário pode aceitar ou substituir esses valores.</span><span class="sxs-lookup"><span data-stu-id="5857e-118">The user can either accept or override these values.</span></span> <span data-ttu-id="5857e-119">Se nenhum valor for atribuído a um parâmetro, a caixa de edição associada estará vazia e o usuário deverá inserir um valor.</span><span class="sxs-lookup"><span data-stu-id="5857e-119">If no value is assigned to a parameter, the associated edit box is empty and the user must enter a value.</span></span>

<span data-ttu-id="5857e-120">Este método não está disponível atualmente no Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="5857e-120">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="5857e-121">Exemplos</span><span class="sxs-lookup"><span data-stu-id="5857e-121">Examples</span></span>

<span data-ttu-id="5857e-122">Os exemplos a seguir mostram o uso de **FindPrinter** para exibir a caixa de diálogo **Localizar impressora** para um aplicativo específico.</span><span class="sxs-lookup"><span data-stu-id="5857e-122">The following examples show the use of **FindPrinter** to display the **Find Printer** dialog box for a particular application.</span></span> <span data-ttu-id="5857e-123">O uso é mostrado para JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="5857e-123">Usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="5857e-124">JScript</span><span class="sxs-lookup"><span data-stu-id="5857e-124">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFindPrinterJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.FindPrinter();
    }
</script>
```



<span data-ttu-id="5857e-125">VBScript</span><span class="sxs-lookup"><span data-stu-id="5857e-125">VBScript:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="5857e-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5857e-126">Requirements</span></span>



| <span data-ttu-id="5857e-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="5857e-127">Requirement</span></span> | <span data-ttu-id="5857e-128">Valor</span><span class="sxs-lookup"><span data-stu-id="5857e-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5857e-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5857e-129">Minimum supported client</span></span><br/> | <span data-ttu-id="5857e-130">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="5857e-130">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5857e-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5857e-131">Minimum supported server</span></span><br/> | <span data-ttu-id="5857e-132">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="5857e-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="5857e-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5857e-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="5857e-134"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="5857e-134"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="5857e-135">INSERI</span><span class="sxs-lookup"><span data-stu-id="5857e-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5857e-136"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5857e-136"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="5857e-137">DLL</span><span class="sxs-lookup"><span data-stu-id="5857e-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5857e-138"><dt>Shell32.dll (versão 5,0 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="5857e-138"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
