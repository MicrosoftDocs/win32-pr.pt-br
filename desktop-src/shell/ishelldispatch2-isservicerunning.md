---
description: Método IShellDispatch2. IsServiceRunning – retorna um valor que indica se um serviço específico está em execução.
ms.assetid: 91f3fba1-7aa5-423a-bc37-49db230c79db
title: Método IShellDispatch2. IsServiceRunning (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch2.IsServiceRunning
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: e8ad792f1669a8ebcfa411c58b34da214ccf69a7
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117084"
---
# <a name="ishelldispatch2isservicerunning-method"></a><span data-ttu-id="10877-103">Método IShellDispatch2. IsServiceRunning</span><span class="sxs-lookup"><span data-stu-id="10877-103">IShellDispatch2.IsServiceRunning method</span></span>

<span data-ttu-id="10877-104">Retorna um valor que indica se um serviço específico está em execução.</span><span class="sxs-lookup"><span data-stu-id="10877-104">Returns a value that indicates whether a particular service is running.</span></span>

## <a name="syntax"></a><span data-ttu-id="10877-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="10877-105">Syntax</span></span>


```JScript
retVal = IShellDispatch2.IsServiceRunning(
  sServiceName
)
```


```VB

IShellDispatch2.IsServiceRunning( _
  ByVal sServiceName As BSTR _
) As Variant
```





## <a name="parameters"></a><span data-ttu-id="10877-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="10877-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10877-107">*sServiceName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="10877-107">*sServiceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="10877-108">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="10877-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="10877-109">Uma **cadeia de caracteres** que contém o nome do serviço.</span><span class="sxs-lookup"><span data-stu-id="10877-109">A **String** that contains the name of the service.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="10877-110">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="10877-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="10877-111">JScript</span><span class="sxs-lookup"><span data-stu-id="10877-111">JScript</span></span>

<span data-ttu-id="10877-112">Tipo: **variante \***</span><span class="sxs-lookup"><span data-stu-id="10877-112">Type: **Variant\***</span></span>

<span data-ttu-id="10877-113">Retornará **true** se o serviço especificado por *sServiceName* estiver em execução; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="10877-113">Returns **true** if the service specified by *sServiceName* is running; otherwise, **false**.</span></span>

### <a name="vb"></a><span data-ttu-id="10877-114">VB</span><span class="sxs-lookup"><span data-stu-id="10877-114">VB</span></span>

<span data-ttu-id="10877-115">Tipo: **variante \***</span><span class="sxs-lookup"><span data-stu-id="10877-115">Type: **Variant\***</span></span>

<span data-ttu-id="10877-116">Retornará **true** se o serviço especificado por *sServiceName* estiver em execução; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="10877-116">Returns **true** if the service specified by *sServiceName* is running; otherwise, **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="10877-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="10877-117">Remarks</span></span>

<span data-ttu-id="10877-118">Esse método é implementado e acessado por meio do método [**shell. IsServiceRunning**](./shell-isservicerunning.md) .</span><span class="sxs-lookup"><span data-stu-id="10877-118">This method is implemented and accessed through the [**Shell.IsServiceRunning**](./shell-isservicerunning.md) method.</span></span>

<span data-ttu-id="10877-119">Este método não está disponível atualmente no Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="10877-119">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="10877-120">Exemplos</span><span class="sxs-lookup"><span data-stu-id="10877-120">Examples</span></span>

<span data-ttu-id="10877-121">Os exemplos a seguir mostram o uso de **IsServiceRunning** para determinar se o serviço de temas está em execução para um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="10877-121">The following examples show the use of **IsServiceRunning** to determine whether the Themes service is running for an application.</span></span> <span data-ttu-id="10877-122">O uso é mostrado para JScript e VBScript.</span><span class="sxs-lookup"><span data-stu-id="10877-122">Usage is shown for JScript and VBScript.</span></span>

<span data-ttu-id="10877-123">JScript</span><span class="sxs-lookup"><span data-stu-id="10877-123">JScript:</span></span>


```JScript
<script language="JScript">
    function fnIsServiceRunningJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var bReturn;
    
        bReturn = objShell.IsServiceRunning("Themes");
    }
</script>
```



<span data-ttu-id="10877-124">VBScript</span><span class="sxs-lookup"><span data-stu-id="10877-124">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnIsServiceRunningVB()
        dim objShell
        dim bReturn
    
        set objShell = CreateObject("shell.application")
    
        bReturn = objShell.IsServiceRunning("Themes")
    
        set objShell = nothing
    end function
</script>
```



## <a name="requirements"></a><span data-ttu-id="10877-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="10877-125">Requirements</span></span>



| <span data-ttu-id="10877-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="10877-126">Requirement</span></span> | <span data-ttu-id="10877-127">Valor</span><span class="sxs-lookup"><span data-stu-id="10877-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10877-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="10877-128">Minimum supported client</span></span><br/> | <span data-ttu-id="10877-129">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="10877-129">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="10877-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="10877-130">Minimum supported server</span></span><br/> | <span data-ttu-id="10877-131">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="10877-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="10877-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="10877-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="10877-133"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="10877-133"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="10877-134">INSERI</span><span class="sxs-lookup"><span data-stu-id="10877-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="10877-135"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="10877-135"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="10877-136">DLL</span><span class="sxs-lookup"><span data-stu-id="10877-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="10877-137"><dt>Shell32.dll (versão 5,0 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="10877-137"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
