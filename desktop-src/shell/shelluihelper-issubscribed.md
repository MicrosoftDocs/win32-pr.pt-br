---
description: Indica se uma URL especificada está inscreveda.
title: Método ShellUIHelper.IsSubscribed (Exdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellUIHelper.IsSubscribed
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: fcf23352-6603-4b17-9c3b-b353cca1c003
ms.openlocfilehash: ca68d2e46ce74593b66aac6f995b88ddcb79796b
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842487"
---
# <a name="shelluihelperissubscribed-method"></a><span data-ttu-id="db049-103">Método ShellUIHelper.IsSubscribed</span><span class="sxs-lookup"><span data-stu-id="db049-103">ShellUIHelper.IsSubscribed method</span></span>

<span data-ttu-id="db049-104">Indica se uma URL especificada está inscreveda.</span><span class="sxs-lookup"><span data-stu-id="db049-104">Indicates whether a specified URL is subscribed to.</span></span>

## <a name="syntax"></a><span data-ttu-id="db049-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="db049-105">Syntax</span></span>


```JScript
bRetVal = ShellUIHelper.IsSubscribed(
  sURL
)
```



## <a name="parameters"></a><span data-ttu-id="db049-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="db049-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db049-107">*sURL* \[ Em\]</span><span class="sxs-lookup"><span data-stu-id="db049-107">*sURL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db049-108">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="db049-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="db049-109">Um **valor string** que especifica a URL.</span><span class="sxs-lookup"><span data-stu-id="db049-109">A **String** value that specifies the URL.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db049-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="db049-110">Return value</span></span>

<span data-ttu-id="db049-111">Tipo: **booliana \***</span><span class="sxs-lookup"><span data-stu-id="db049-111">Type: **Boolean\***</span></span>

<span data-ttu-id="db049-112">**true** se a URL for inscreveda; caso contrário, **false.**</span><span class="sxs-lookup"><span data-stu-id="db049-112">**true** if the URL is subscribed to; otherwise, **false**.</span></span>

## <a name="examples"></a><span data-ttu-id="db049-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="db049-113">Examples</span></span>

<span data-ttu-id="db049-114">O exemplo a seguir mostra o uso adequado desse método para JScript inserido em HTML e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="db049-114">The following example shows the proper usage of this method for JScript embedded in HTML and Visual Basic.</span></span>

<span data-ttu-id="db049-115">Jscript:</span><span class="sxs-lookup"><span data-stu-id="db049-115">JScript:</span></span>


```JScript
<html>
<head>
<title></title>

<object id="ShellUIHelper"
        classid="CLSID:64AB4BB7-111E-11d1-8F79-00C04FC2FBE1"
        width=0
        height=0
        VIEWASTEXT>
</object>

<script language="JavaScript">
    function fnShellUIHelperIsSubscribedJ()
    {
        var bReturn;
        
        bReturn = ShellUIHelper.IsSubscribed("https://www.microsoft.com/");
        alert(bReturn);
    }
</script>

</head>
<body onload=fnShellUIHelperIsSubscribedJ()>
</body>
</html>
```



<span data-ttu-id="db049-116">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="db049-116">Visual Basic:</span></span>


```VB
Private Sub fnShellUIHelperIsSubscribedVB()
    Dim objShellUIHelper As ShellUIHelper
    Dim bReturn          As Boolean
    
    Set objShellUIHelper = New ShellUIHelper
        bReturn = objShellUIHelper.IsSubscribed("https://www.microsoft.com/")
        Debug.Print bReturn
    Set objShellUIHelper = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="db049-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="db049-117">Requirements</span></span>



| <span data-ttu-id="db049-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="db049-118">Requirement</span></span> | <span data-ttu-id="db049-119">Valor</span><span class="sxs-lookup"><span data-stu-id="db049-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="db049-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="db049-120">Minimum supported client</span></span><br/> | <span data-ttu-id="db049-121">Windows 2000 Professional, somente aplicativos da área de trabalho do Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="db049-121">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="db049-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="db049-122">Minimum supported server</span></span><br/> | <span data-ttu-id="db049-123">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="db049-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="db049-124">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="db049-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="db049-125"><dt>Exdisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="db049-125"><dt>Exdisp.h</dt></span></span> </dl>                            |
| <span data-ttu-id="db049-126">DLL</span><span class="sxs-lookup"><span data-stu-id="db049-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="db049-127"><dt>Shell32.dll (versão 4.71 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="db049-127"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
