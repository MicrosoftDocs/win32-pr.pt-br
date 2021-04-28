---
description: Método Shell. ShowBrowserBar – exibe uma barra de navegador.
ms.assetid: 203636D2-54D3-4163-B9AC-39213D6F4203
title: Método Shell. ShowBrowserBar (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.ShowBrowserBar
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: d19cd5b98ce39470860cc481ab05e4bb41adc9a4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083720"
---
# <a name="shellshowbrowserbar-method"></a><span data-ttu-id="3db41-103">Método Shell. ShowBrowserBar</span><span class="sxs-lookup"><span data-stu-id="3db41-103">Shell.ShowBrowserBar method</span></span>

<span data-ttu-id="3db41-104">Exibe uma barra de navegador.</span><span class="sxs-lookup"><span data-stu-id="3db41-104">Displays a browser bar.</span></span>

## <a name="syntax"></a><span data-ttu-id="3db41-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3db41-105">Syntax</span></span>


```JScript
retVal = Shell.ShowBrowserBar(
  sCLSID,
  vShow
)
```


```VB

Shell.ShowBrowserBar( _
  ByVal sCLSID As BSTR, _
  ByVal vShow As Variant _
) As Variant
```





## <a name="parameters"></a><span data-ttu-id="3db41-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3db41-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3db41-107">*sCLSID* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3db41-107">*sCLSID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3db41-108">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="3db41-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="3db41-109">Uma **cadeia de caracteres** que contém a forma de cadeia de caracteres do CLSID da barra do navegador a ser exibida.</span><span class="sxs-lookup"><span data-stu-id="3db41-109">A **String** that contains the string form of the CLSID of the browser bar to be displayed.</span></span> <span data-ttu-id="3db41-110">O objeto deve ser registrado como um objeto de barra do Explorer com uma \_ categoria de componente InfoBand de CATID.</span><span class="sxs-lookup"><span data-stu-id="3db41-110">The object must be registered as an Explorer Bar object with a CATID\_InfoBand component category.</span></span> <span data-ttu-id="3db41-111">Para obter mais informações, consulte [Criando barras personalizadas do Explorer, faixas de ferramentas e faixas de escrivaninha](band-objects.md).</span><span class="sxs-lookup"><span data-stu-id="3db41-111">For further information, see [Creating Custom Explorer Bars, Tool Bands, and Desk Bands](band-objects.md).</span></span>

</dd> <dt>

<span data-ttu-id="3db41-112">*vShow* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3db41-112">*vShow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3db41-113">Tipo: **variante**</span><span class="sxs-lookup"><span data-stu-id="3db41-113">Type: **Variant**</span></span>

<span data-ttu-id="3db41-114">Defina como **true** para mostrar a barra de navegador ou **false** para ocultá-la.</span><span class="sxs-lookup"><span data-stu-id="3db41-114">Set to **true** to show the browser bar or **false** to hide it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3db41-115">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="3db41-115">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="3db41-116">JScript</span><span class="sxs-lookup"><span data-stu-id="3db41-116">JScript</span></span>

<span data-ttu-id="3db41-117">Tipo: **variante \***</span><span class="sxs-lookup"><span data-stu-id="3db41-117">Type: **Variant\***</span></span>

<span data-ttu-id="3db41-118">Retornará **true** se for bem-sucedido; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="3db41-118">Returns **true** if successful; otherwise, **false**.</span></span>

### <a name="vb"></a><span data-ttu-id="3db41-119">VB</span><span class="sxs-lookup"><span data-stu-id="3db41-119">VB</span></span>

<span data-ttu-id="3db41-120">Tipo: **variante \***</span><span class="sxs-lookup"><span data-stu-id="3db41-120">Type: **Variant\***</span></span>

<span data-ttu-id="3db41-121">Retornará **true** se for bem-sucedido; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="3db41-121">Returns **true** if successful; otherwise, **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="3db41-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="3db41-122">Remarks</span></span>

<span data-ttu-id="3db41-123">Você pode exibir uma das barras padrão do Explorer definindo o parâmetro *sCLSID* como o CLSID da barra do Gerenciador.</span><span class="sxs-lookup"><span data-stu-id="3db41-123">You can display one of the standard Explorer Bars by setting the *sCLSID* parameter to the CLSID of that Explorer Bar.</span></span> <span data-ttu-id="3db41-124">As barras padrão do Explorer e suas cadeias de caracteres CLSID são as seguintes:</span><span class="sxs-lookup"><span data-stu-id="3db41-124">The standard Explorer Bars and their CLSID strings are as follows:</span></span>



| <span data-ttu-id="3db41-125">Barra do Explorer</span><span class="sxs-lookup"><span data-stu-id="3db41-125">Explorer Bar</span></span> | <span data-ttu-id="3db41-126">Cadeia de caracteres CLSID</span><span class="sxs-lookup"><span data-stu-id="3db41-126">CLSID string</span></span>                           |
|--------------|----------------------------------------|
| <span data-ttu-id="3db41-127">Favoritos</span><span class="sxs-lookup"><span data-stu-id="3db41-127">Favorites</span></span>    | <span data-ttu-id="3db41-128">{EFA24E61-B078-11d0-89E4-00C04FC9E26E}</span><span class="sxs-lookup"><span data-stu-id="3db41-128">{EFA24E61-B078-11d0-89E4-00C04FC9E26E}</span></span> |
| <span data-ttu-id="3db41-129">Pastas</span><span class="sxs-lookup"><span data-stu-id="3db41-129">Folders</span></span>      | <span data-ttu-id="3db41-130">{EFA24E64-B078-11d0-89E4-00C04FC9E26E}</span><span class="sxs-lookup"><span data-stu-id="3db41-130">{EFA24E64-B078-11d0-89E4-00C04FC9E26E}</span></span> |
| <span data-ttu-id="3db41-131">Histórico</span><span class="sxs-lookup"><span data-stu-id="3db41-131">History</span></span>      | <span data-ttu-id="3db41-132">{EFA24E62-B078-11d0-89E4-00C04FC9E26E}</span><span class="sxs-lookup"><span data-stu-id="3db41-132">{EFA24E62-B078-11d0-89E4-00C04FC9E26E}</span></span> |
| <span data-ttu-id="3db41-133">Search</span><span class="sxs-lookup"><span data-stu-id="3db41-133">Search</span></span>       | <span data-ttu-id="3db41-134">{30D02401-6A81-11d0-8274-00C04FD5AE38}</span><span class="sxs-lookup"><span data-stu-id="3db41-134">{30D02401-6A81-11d0-8274-00C04FD5AE38}</span></span> |



 

<span data-ttu-id="3db41-135">Este método não está disponível atualmente no Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="3db41-135">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="3db41-136">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3db41-136">Examples</span></span>

<span data-ttu-id="3db41-137">Os exemplos a seguir mostram o uso de **shell. ShowBrowserBar** para exibir a barra de navegador de **favoritos** .</span><span class="sxs-lookup"><span data-stu-id="3db41-137">The following examples show the use of **Shell.ShowBrowserBar** to display the **Favorites** browser bar.</span></span> <span data-ttu-id="3db41-138">O uso é mostrado para JScript e VBScript.</span><span class="sxs-lookup"><span data-stu-id="3db41-138">Usage is shown for JScript and VBScript.</span></span>

<span data-ttu-id="3db41-139">JScript</span><span class="sxs-lookup"><span data-stu-id="3db41-139">JScript:</span></span>


```JScript
<script language="JavaScript">
    function fnShowBrowserBarJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var bReturn;
        
        bReturn = objShell.ShowBrowserBar("{EFA24E61-B078-11d0-89E4-00C04FC9E26E}", true);
    }
</script>
```



<span data-ttu-id="3db41-140">VBScript</span><span class="sxs-lookup"><span data-stu-id="3db41-140">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShowBrowserBarVB()
        dim objShell
        dim bReturn

        set objShell = CreateObject("shell.application")

        bReturn = objShell.ShowBrowserBar("{EFA24E61-B078-11d0-89E4-00C04FC9E26E}", true)

        set objShell = nothing
    end function
</script>
```



## <a name="requirements"></a><span data-ttu-id="3db41-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3db41-141">Requirements</span></span>



| <span data-ttu-id="3db41-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="3db41-142">Requirement</span></span> | <span data-ttu-id="3db41-143">Valor</span><span class="sxs-lookup"><span data-stu-id="3db41-143">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3db41-144">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3db41-144">Minimum supported client</span></span><br/> | <span data-ttu-id="3db41-145">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="3db41-145">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3db41-146">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3db41-146">Minimum supported server</span></span><br/> | <span data-ttu-id="3db41-147">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3db41-147">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="3db41-148">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3db41-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="3db41-149"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="3db41-149"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="3db41-150">INSERI</span><span class="sxs-lookup"><span data-stu-id="3db41-150">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3db41-151"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3db41-151"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="3db41-152">DLL</span><span class="sxs-lookup"><span data-stu-id="3db41-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3db41-153"><dt>Shell32.dll (versão 5,0 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="3db41-153"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
