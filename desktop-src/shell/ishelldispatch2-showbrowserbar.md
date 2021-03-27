---
description: Exibe uma barra de navegador.
ms.assetid: 5776370c-3bbf-449b-a8fe-2dbc7d89dd25
title: Método IShellDispatch2. ShowBrowserBar (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch2.ShowBrowserBar
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: e1df729401dd12b8221ba98a3b81ea65569113e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967516"
---
# <a name="ishelldispatch2showbrowserbar-method"></a><span data-ttu-id="fee81-103">Método IShellDispatch2. ShowBrowserBar</span><span class="sxs-lookup"><span data-stu-id="fee81-103">IShellDispatch2.ShowBrowserBar method</span></span>

<span data-ttu-id="fee81-104">Exibe uma barra de navegador.</span><span class="sxs-lookup"><span data-stu-id="fee81-104">Displays a browser bar.</span></span>

## <a name="syntax"></a><span data-ttu-id="fee81-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fee81-105">Syntax</span></span>


```JScript
retVal = IShellDispatch2.ShowBrowserBar(
  sCLSID,
  vShow
)
```


```VB

IShellDispatch2.ShowBrowserBar( _
  ByVal sCLSID As BSTR, _
  ByVal vShow As Variant _
) As Variant
```





## <a name="parameters"></a><span data-ttu-id="fee81-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fee81-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fee81-107">*sCLSID* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fee81-107">*sCLSID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fee81-108">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="fee81-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="fee81-109">Uma **cadeia de caracteres** que contém a forma de cadeia de caracteres do CLSID da barra do navegador a ser exibida.</span><span class="sxs-lookup"><span data-stu-id="fee81-109">A **String** that contains the string form of the CLSID of the browser bar to be displayed.</span></span> <span data-ttu-id="fee81-110">O objeto deve ser registrado como um objeto de barra do Explorer com uma \_ categoria de componente InfoBand de CATID.</span><span class="sxs-lookup"><span data-stu-id="fee81-110">The object must be registered as an Explorer Bar object with a CATID\_InfoBand component category.</span></span> <span data-ttu-id="fee81-111">Para obter mais informações, consulte [Criando barras personalizadas do Explorer, faixas de ferramentas e faixas de escrivaninha](band-objects.md).</span><span class="sxs-lookup"><span data-stu-id="fee81-111">For further information, see [Creating Custom Explorer Bars, Tool Bands, and Desk Bands](band-objects.md).</span></span>

</dd> <dt>

<span data-ttu-id="fee81-112">*vShow* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fee81-112">*vShow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fee81-113">Tipo: **variante**</span><span class="sxs-lookup"><span data-stu-id="fee81-113">Type: **Variant**</span></span>

<span data-ttu-id="fee81-114">Defina como **true** para mostrar a barra de navegador ou **false** para ocultá-la.</span><span class="sxs-lookup"><span data-stu-id="fee81-114">Set to **true** to show the browser bar or **false** to hide it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fee81-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fee81-115">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="fee81-116">JScript</span><span class="sxs-lookup"><span data-stu-id="fee81-116">JScript</span></span>

<span data-ttu-id="fee81-117">Tipo: \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="fee81-117">Type: \**Variant\** _</span></span>

<span data-ttu-id="fee81-118">Retorna _ *true*\* se for bem-sucedido; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="fee81-118">Returns _ *true*\* if successful; otherwise, **false**.</span></span>

### <a name="vb"></a><span data-ttu-id="fee81-119">VB</span><span class="sxs-lookup"><span data-stu-id="fee81-119">VB</span></span>

<span data-ttu-id="fee81-120">Tipo: \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="fee81-120">Type: \**Variant\** _</span></span>

<span data-ttu-id="fee81-121">Retorna _ *true*\* se for bem-sucedido; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="fee81-121">Returns _ *true*\* if successful; otherwise, **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="fee81-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="fee81-122">Remarks</span></span>

<span data-ttu-id="fee81-123">Esse método é implementado e acessado por meio do método [**shell. ShowBrowserBar**](./shell-showbrowserbar.md) .</span><span class="sxs-lookup"><span data-stu-id="fee81-123">This method is implemented and accessed through the [**Shell.ShowBrowserBar**](./shell-showbrowserbar.md) method.</span></span>

<span data-ttu-id="fee81-124">Você pode exibir uma das barras padrão do Explorer definindo o parâmetro *sCLSID* como o CLSID da barra do Gerenciador.</span><span class="sxs-lookup"><span data-stu-id="fee81-124">You can display one of the standard Explorer Bars by setting the *sCLSID* parameter to the CLSID of that Explorer Bar.</span></span> <span data-ttu-id="fee81-125">As barras padrão do Explorer e suas cadeias de caracteres CLSID são as seguintes:</span><span class="sxs-lookup"><span data-stu-id="fee81-125">The standard Explorer Bars and their CLSID strings are as follows:</span></span>



| <span data-ttu-id="fee81-126">Barra do Explorer</span><span class="sxs-lookup"><span data-stu-id="fee81-126">Explorer Bar</span></span> | <span data-ttu-id="fee81-127">Cadeia de caracteres CLSID</span><span class="sxs-lookup"><span data-stu-id="fee81-127">CLSID string</span></span>                           |
|--------------|----------------------------------------|
| <span data-ttu-id="fee81-128">Favoritos</span><span class="sxs-lookup"><span data-stu-id="fee81-128">Favorites</span></span>    | <span data-ttu-id="fee81-129">{EFA24E61-B078-11d0-89E4-00C04FC9E26E}</span><span class="sxs-lookup"><span data-stu-id="fee81-129">{EFA24E61-B078-11d0-89E4-00C04FC9E26E}</span></span> |
| <span data-ttu-id="fee81-130">Pastas</span><span class="sxs-lookup"><span data-stu-id="fee81-130">Folders</span></span>      | <span data-ttu-id="fee81-131">{EFA24E64-B078-11d0-89E4-00C04FC9E26E}</span><span class="sxs-lookup"><span data-stu-id="fee81-131">{EFA24E64-B078-11d0-89E4-00C04FC9E26E}</span></span> |
| <span data-ttu-id="fee81-132">Histórico</span><span class="sxs-lookup"><span data-stu-id="fee81-132">History</span></span>      | <span data-ttu-id="fee81-133">{EFA24E62-B078-11d0-89E4-00C04FC9E26E}</span><span class="sxs-lookup"><span data-stu-id="fee81-133">{EFA24E62-B078-11d0-89E4-00C04FC9E26E}</span></span> |
| <span data-ttu-id="fee81-134">Pesquisar</span><span class="sxs-lookup"><span data-stu-id="fee81-134">Search</span></span>       | <span data-ttu-id="fee81-135">{30D02401-6A81-11d0-8274-00C04FD5AE38}</span><span class="sxs-lookup"><span data-stu-id="fee81-135">{30D02401-6A81-11d0-8274-00C04FD5AE38}</span></span> |



 

<span data-ttu-id="fee81-136">Este método não está disponível atualmente no Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="fee81-136">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="fee81-137">Exemplos</span><span class="sxs-lookup"><span data-stu-id="fee81-137">Examples</span></span>

<span data-ttu-id="fee81-138">Os exemplos a seguir mostram o uso de **ShowBrowserBar** para exibir a barra de navegador de **favoritos** .</span><span class="sxs-lookup"><span data-stu-id="fee81-138">The following examples show the use of **ShowBrowserBar** to display the **Favorites** browser bar.</span></span> <span data-ttu-id="fee81-139">O uso é mostrado para JScript e VBScript.</span><span class="sxs-lookup"><span data-stu-id="fee81-139">Usage is shown for JScript and VBScript.</span></span>

<span data-ttu-id="fee81-140">JScript</span><span class="sxs-lookup"><span data-stu-id="fee81-140">JScript:</span></span>


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



<span data-ttu-id="fee81-141">VBScript</span><span class="sxs-lookup"><span data-stu-id="fee81-141">VBScript:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="fee81-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fee81-142">Requirements</span></span>



| <span data-ttu-id="fee81-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="fee81-143">Requirement</span></span> | <span data-ttu-id="fee81-144">Valor</span><span class="sxs-lookup"><span data-stu-id="fee81-144">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fee81-145">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fee81-145">Minimum supported client</span></span><br/> | <span data-ttu-id="fee81-146">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="fee81-146">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fee81-147">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fee81-147">Minimum supported server</span></span><br/> | <span data-ttu-id="fee81-148">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="fee81-148">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="fee81-149">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fee81-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="fee81-150"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="fee81-150"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="fee81-151">INSERI</span><span class="sxs-lookup"><span data-stu-id="fee81-151">IDL</span></span><br/>                      | <dl> <span data-ttu-id="fee81-152"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="fee81-152"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="fee81-153">DLL</span><span class="sxs-lookup"><span data-stu-id="fee81-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fee81-154"><dt>Shell32.dll (versão 5,0 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="fee81-154"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
