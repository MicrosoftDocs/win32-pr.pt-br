---
description: Adiciona um item ao Microsoft Active Desktop.
title: Método ShellUIHelper.AddDesktopComponent (Exdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellUIHelper.AddDesktopComponent
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 41634a89-15b9-41c8-ba3f-4bf19b786f6f
ms.openlocfilehash: 2edaa79bd62dcee40e4f197700d2128cb0b2070d
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842457"
---
# <a name="shelluihelperadddesktopcomponent-method"></a><span data-ttu-id="2042b-103">Método ShellUIHelper.AddDesktopComponent</span><span class="sxs-lookup"><span data-stu-id="2042b-103">ShellUIHelper.AddDesktopComponent method</span></span>

<span data-ttu-id="2042b-104">Adiciona um item ao Microsoft Active Desktop.</span><span class="sxs-lookup"><span data-stu-id="2042b-104">Adds an item to the Microsoft Active Desktop.</span></span>

## <a name="syntax"></a><span data-ttu-id="2042b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2042b-105">Syntax</span></span>


```JScript
iRetVal = ShellUIHelper.AddDesktopComponent(
  sURL,
  sType,
  [ Left ],
  [ Top ],
  [ Width ],
  [ Height ]
)
```



## <a name="parameters"></a><span data-ttu-id="2042b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2042b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2042b-107">*sURL* \[ Em\]</span><span class="sxs-lookup"><span data-stu-id="2042b-107">*sURL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2042b-108">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="2042b-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="2042b-109">Um **valor string** que especifica a URL do novo item favorito.</span><span class="sxs-lookup"><span data-stu-id="2042b-109">A **String** value that specifies the URL of the new favorite item.</span></span>

</dd> <dt>

<span data-ttu-id="2042b-110">*sType* \[ Em\]</span><span class="sxs-lookup"><span data-stu-id="2042b-110">*sType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2042b-111">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="2042b-111">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="2042b-112">Um **valor string** que especifica o tipo de item que está sendo adicionado.</span><span class="sxs-lookup"><span data-stu-id="2042b-112">A **String** value that specifies the type of item being added.</span></span> <span data-ttu-id="2042b-113">Esse pode ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="2042b-113">This can be one of the following values.</span></span>

<dt>



 <span data-ttu-id="2042b-114">(imagem)</span><span class="sxs-lookup"><span data-stu-id="2042b-114">(image)</span></span>


</dt> <dd>

<span data-ttu-id="2042b-115">O componente é uma imagem.</span><span class="sxs-lookup"><span data-stu-id="2042b-115">The component is an image.</span></span>

</dd> <dt>



 <span data-ttu-id="2042b-116">(site)</span><span class="sxs-lookup"><span data-stu-id="2042b-116">(website)</span></span>


</dt> <dd>

<span data-ttu-id="2042b-117">O componente é um site.</span><span class="sxs-lookup"><span data-stu-id="2042b-117">The component is a website.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="2042b-118">*Esquerda* \[ in, opcional\]</span><span class="sxs-lookup"><span data-stu-id="2042b-118">*Left* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2042b-119">Tipo: **Variante**</span><span class="sxs-lookup"><span data-stu-id="2042b-119">Type: **Variant**</span></span>

<span data-ttu-id="2042b-120">A posição da borda esquerda do componente, em coordenadas de tela.</span><span class="sxs-lookup"><span data-stu-id="2042b-120">The position of the left edge of the component, in screen coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="2042b-121">*Superior* \[ in, opcional\]</span><span class="sxs-lookup"><span data-stu-id="2042b-121">*Top* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2042b-122">Tipo: **Variante**</span><span class="sxs-lookup"><span data-stu-id="2042b-122">Type: **Variant**</span></span>

<span data-ttu-id="2042b-123">A posição da borda superior do componente, em coordenadas da tela.</span><span class="sxs-lookup"><span data-stu-id="2042b-123">The position of the top edge of the component, in screen coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="2042b-124">*Largura* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="2042b-124">*Width* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2042b-125">Tipo: **variante**</span><span class="sxs-lookup"><span data-stu-id="2042b-125">Type: **Variant**</span></span>

<span data-ttu-id="2042b-126">A largura do componente, em unidades da tela.</span><span class="sxs-lookup"><span data-stu-id="2042b-126">The width of the component, in screen units.</span></span>

</dd> <dt>

<span data-ttu-id="2042b-127">*Altura* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="2042b-127">*Height* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2042b-128">Tipo: **variante**</span><span class="sxs-lookup"><span data-stu-id="2042b-128">Type: **Variant**</span></span>

<span data-ttu-id="2042b-129">A altura do componente, em unidades da tela.</span><span class="sxs-lookup"><span data-stu-id="2042b-129">The height of the component, in screen units.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="2042b-130">Exemplos</span><span class="sxs-lookup"><span data-stu-id="2042b-130">Examples</span></span>

<span data-ttu-id="2042b-131">O exemplo a seguir mostra o uso correto desse método para JScript Embedded em HTML e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="2042b-131">The following example shows the proper usage of this method for JScript embedded in HTML and Visual Basic.</span></span>

<span data-ttu-id="2042b-132">JScript</span><span class="sxs-lookup"><span data-stu-id="2042b-132">JScript:</span></span>


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
    function fnShellUIHelperAddDesktopComponentJ()
    {
        ShellUIHelper.AddDesktopComponent("https://www.microsoft.com/", "website");
    }
</script>

</head>
<body onload=fnShellUIHelperAddDesktopComponentJ()>
</body>
</html>
```



<span data-ttu-id="2042b-133">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="2042b-133">Visual Basic:</span></span>


```VB
Private Sub fnShellUIHelperAddDesktopComponentVB()
    Dim objShellUIHelper As ShellUIHelper
    
    Set objShellUIHelper = New ShellUIHelper
        objShellUIHelper.AddDesktopComponent "https://www.microsoft.com/", "website"
    Set objShellUIHelper = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="2042b-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2042b-134">Requirements</span></span>



| <span data-ttu-id="2042b-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="2042b-135">Requirement</span></span> | <span data-ttu-id="2042b-136">Valor</span><span class="sxs-lookup"><span data-stu-id="2042b-136">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2042b-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2042b-137">Minimum supported client</span></span><br/> | <span data-ttu-id="2042b-138">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="2042b-138">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="2042b-139">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2042b-139">Minimum supported server</span></span><br/> | <span data-ttu-id="2042b-140">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="2042b-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="2042b-141">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="2042b-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="2042b-142"><dt>O textdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="2042b-142"><dt>Exdisp.h</dt></span></span> </dl>                            |
| <span data-ttu-id="2042b-143">DLL</span><span class="sxs-lookup"><span data-stu-id="2042b-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2042b-144"><dt>Shell32.dll (versão 4,71 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="2042b-144"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
