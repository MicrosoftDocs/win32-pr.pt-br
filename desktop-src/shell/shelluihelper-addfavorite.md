---
description: Exibe a interface do usuário padrão para criar um item favorito. A interface do usuário é inicializada para os parâmetros especificados.
title: Método ShellUIHelper. addfavorito (textdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellUIHelper.AddFavorite
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: b30e776e-642c-4599-b83f-ef15bc0b23d2
ms.openlocfilehash: a5c3cae52f0ad18c1f2ddf6cf91759d1c6daf6c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968193"
---
# <a name="shelluihelperaddfavorite-method"></a><span data-ttu-id="877b3-104">Método ShellUIHelper. addfavorito</span><span class="sxs-lookup"><span data-stu-id="877b3-104">ShellUIHelper.AddFavorite method</span></span>

<span data-ttu-id="877b3-105">Exibe a interface do usuário padrão para criar um item favorito.</span><span class="sxs-lookup"><span data-stu-id="877b3-105">Displays the default user interface for creating a favorite item.</span></span> <span data-ttu-id="877b3-106">A interface do usuário é inicializada para os parâmetros especificados.</span><span class="sxs-lookup"><span data-stu-id="877b3-106">The user interface is initialized to the specified parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="877b3-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="877b3-107">Syntax</span></span>


```JScript
iRetVal = ShellUIHelper.AddFavorite(
  sURL,
  [ vTitle ]
)
```



## <a name="parameters"></a><span data-ttu-id="877b3-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="877b3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="877b3-109">*sUrl* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="877b3-109">*sURL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="877b3-110">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="877b3-110">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="877b3-111">Um valor de **cadeia de caracteres** que especifica a URL do item a ser adicionado à pasta **favoritos** .</span><span class="sxs-lookup"><span data-stu-id="877b3-111">A **String** value that specifies the URL of the item to be added to the **Favorites** folder.</span></span>

</dd> <dt>

<span data-ttu-id="877b3-112">*vTitle* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="877b3-112">*vTitle* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="877b3-113">Tipo: \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="877b3-113">Type: \**Variant\** _</span></span>

<span data-ttu-id="877b3-114">Um valor _ *Variant*\* que especifica o nome do item.</span><span class="sxs-lookup"><span data-stu-id="877b3-114">A _ *Variant*\* value that specifies the name of the item.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="877b3-115">Exemplos</span><span class="sxs-lookup"><span data-stu-id="877b3-115">Examples</span></span>

<span data-ttu-id="877b3-116">O exemplo a seguir mostra o uso correto desse método para JScript Embedded em HTML e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="877b3-116">The following example shows the proper usage of this method for JScript embedded in HTML and Visual Basic.</span></span>

<span data-ttu-id="877b3-117">JScript</span><span class="sxs-lookup"><span data-stu-id="877b3-117">JScript:</span></span>


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
    function fnShellUIHelperAddFavoriteJ()
    {
        ShellUIHelper.AddFavorite("https://www.msn.com", "MSN Home Page");
    }
</script>

</head>
<body onload=fnShellUIHelperAddFavoriteJ()>
</body>
</html>
```



<span data-ttu-id="877b3-118">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="877b3-118">Visual Basic:</span></span>


```VB
Private Sub fnShellUIHelperAddFavoriteVB()
    Dim objShellUIHelper As ShellUIHelper
    
    Set objShellUIHelper = New ShellUIHelper
        objShellUIHelper.AddFavorite "https://www.msn.com", "MSN Home Page"
    Set objShellUIHelper = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="877b3-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="877b3-119">Requirements</span></span>



| <span data-ttu-id="877b3-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="877b3-120">Requirement</span></span> | <span data-ttu-id="877b3-121">Valor</span><span class="sxs-lookup"><span data-stu-id="877b3-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="877b3-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="877b3-122">Minimum supported client</span></span><br/> | <span data-ttu-id="877b3-123">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="877b3-123">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="877b3-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="877b3-124">Minimum supported server</span></span><br/> | <span data-ttu-id="877b3-125">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="877b3-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="877b3-126">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="877b3-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="877b3-127"><dt>O textdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="877b3-127"><dt>Exdisp.h</dt></span></span> </dl>                            |
| <span data-ttu-id="877b3-128">DLL</span><span class="sxs-lookup"><span data-stu-id="877b3-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="877b3-129"><dt>Shell32.dll (versão 4,71 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="877b3-129"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
