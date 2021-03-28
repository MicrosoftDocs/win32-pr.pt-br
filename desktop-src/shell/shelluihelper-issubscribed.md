---
description: Indica se uma URL especificada é assinada.
title: Método ShellUIHelper. issubscribeed (exdisp. h)
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
ms.openlocfilehash: 2085f38e5f91f13a2f67ff4f22b003b533249386
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011179"
---
# <a name="shelluihelperissubscribed-method"></a><span data-ttu-id="a09d0-103">Método ShellUIHelper. issubscribeed</span><span class="sxs-lookup"><span data-stu-id="a09d0-103">ShellUIHelper.IsSubscribed method</span></span>

<span data-ttu-id="a09d0-104">Indica se uma URL especificada é assinada.</span><span class="sxs-lookup"><span data-stu-id="a09d0-104">Indicates whether a specified URL is subscribed to.</span></span>

## <a name="syntax"></a><span data-ttu-id="a09d0-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a09d0-105">Syntax</span></span>


```JScript
bRetVal = ShellUIHelper.IsSubscribed(
  sURL
)
```



## <a name="parameters"></a><span data-ttu-id="a09d0-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a09d0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a09d0-107">*sUrl* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a09d0-107">*sURL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a09d0-108">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="a09d0-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="a09d0-109">Um valor de **cadeia de caracteres** que especifica a URL.</span><span class="sxs-lookup"><span data-stu-id="a09d0-109">A **String** value that specifies the URL.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a09d0-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a09d0-110">Return value</span></span>

<span data-ttu-id="a09d0-111">Tipo: \**booliano \**</span><span class="sxs-lookup"><span data-stu-id="a09d0-111">Type: \**Boolean\** _</span></span>

<span data-ttu-id="a09d0-112">_ *true*\* se a URL for assinada; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="a09d0-112">_ *true*\* if the URL is subscribed to; otherwise, **false**.</span></span>

## <a name="examples"></a><span data-ttu-id="a09d0-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a09d0-113">Examples</span></span>

<span data-ttu-id="a09d0-114">O exemplo a seguir mostra o uso correto desse método para JScript Embedded em HTML e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="a09d0-114">The following example shows the proper usage of this method for JScript embedded in HTML and Visual Basic.</span></span>

<span data-ttu-id="a09d0-115">JScript</span><span class="sxs-lookup"><span data-stu-id="a09d0-115">JScript:</span></span>


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



<span data-ttu-id="a09d0-116">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="a09d0-116">Visual Basic:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="a09d0-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a09d0-117">Requirements</span></span>



| <span data-ttu-id="a09d0-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="a09d0-118">Requirement</span></span> | <span data-ttu-id="a09d0-119">Valor</span><span class="sxs-lookup"><span data-stu-id="a09d0-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a09d0-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a09d0-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a09d0-121">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="a09d0-121">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="a09d0-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a09d0-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a09d0-123">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a09d0-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="a09d0-124">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="a09d0-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="a09d0-125"><dt>O textdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="a09d0-125"><dt>Exdisp.h</dt></span></span> </dl>                            |
| <span data-ttu-id="a09d0-126">DLL</span><span class="sxs-lookup"><span data-stu-id="a09d0-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a09d0-127"><dt>Shell32.dll (versão 4,71 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="a09d0-127"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
