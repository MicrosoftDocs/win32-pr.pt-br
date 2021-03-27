---
description: Retorna um valor que indica se um serviço específico está em execução.
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
ms.openlocfilehash: f39cd7da3d9959830208ab971b636e146e549775
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967524"
---
# <a name="ishelldispatch2isservicerunning-method"></a><span data-ttu-id="2d684-103">Método IShellDispatch2. IsServiceRunning</span><span class="sxs-lookup"><span data-stu-id="2d684-103">IShellDispatch2.IsServiceRunning method</span></span>

<span data-ttu-id="2d684-104">Retorna um valor que indica se um serviço específico está em execução.</span><span class="sxs-lookup"><span data-stu-id="2d684-104">Returns a value that indicates whether a particular service is running.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d684-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2d684-105">Syntax</span></span>


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





## <a name="parameters"></a><span data-ttu-id="2d684-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2d684-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d684-107">*sServiceName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2d684-107">*sServiceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d684-108">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="2d684-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="2d684-109">Uma **cadeia de caracteres** que contém o nome do serviço.</span><span class="sxs-lookup"><span data-stu-id="2d684-109">A **String** that contains the name of the service.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d684-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2d684-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="2d684-111">JScript</span><span class="sxs-lookup"><span data-stu-id="2d684-111">JScript</span></span>

<span data-ttu-id="2d684-112">Tipo: \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="2d684-112">Type: \**Variant\** _</span></span>

<span data-ttu-id="2d684-113">Retorna _ *true*\* se o serviço especificado por *sServiceName* estiver em execução; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="2d684-113">Returns _ *true*\* if the service specified by *sServiceName* is running; otherwise, **false**.</span></span>

### <a name="vb"></a><span data-ttu-id="2d684-114">VB</span><span class="sxs-lookup"><span data-stu-id="2d684-114">VB</span></span>

<span data-ttu-id="2d684-115">Tipo: \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="2d684-115">Type: \**Variant\** _</span></span>

<span data-ttu-id="2d684-116">Retorna _ *true*\* se o serviço especificado por *sServiceName* estiver em execução; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="2d684-116">Returns _ *true*\* if the service specified by *sServiceName* is running; otherwise, **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="2d684-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="2d684-117">Remarks</span></span>

<span data-ttu-id="2d684-118">Esse método é implementado e acessado por meio do método [**shell. IsServiceRunning**](./shell-isservicerunning.md) .</span><span class="sxs-lookup"><span data-stu-id="2d684-118">This method is implemented and accessed through the [**Shell.IsServiceRunning**](./shell-isservicerunning.md) method.</span></span>

<span data-ttu-id="2d684-119">Este método não está disponível atualmente no Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="2d684-119">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="2d684-120">Exemplos</span><span class="sxs-lookup"><span data-stu-id="2d684-120">Examples</span></span>

<span data-ttu-id="2d684-121">Os exemplos a seguir mostram o uso de **IsServiceRunning** para determinar se o serviço de temas está em execução para um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="2d684-121">The following examples show the use of **IsServiceRunning** to determine whether the Themes service is running for an application.</span></span> <span data-ttu-id="2d684-122">O uso é mostrado para JScript e VBScript.</span><span class="sxs-lookup"><span data-stu-id="2d684-122">Usage is shown for JScript and VBScript.</span></span>

<span data-ttu-id="2d684-123">JScript</span><span class="sxs-lookup"><span data-stu-id="2d684-123">JScript:</span></span>


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



<span data-ttu-id="2d684-124">VBScript</span><span class="sxs-lookup"><span data-stu-id="2d684-124">VBScript:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="2d684-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2d684-125">Requirements</span></span>



| <span data-ttu-id="2d684-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="2d684-126">Requirement</span></span> | <span data-ttu-id="2d684-127">Valor</span><span class="sxs-lookup"><span data-stu-id="2d684-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d684-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2d684-128">Minimum supported client</span></span><br/> | <span data-ttu-id="2d684-129">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="2d684-129">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2d684-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2d684-130">Minimum supported server</span></span><br/> | <span data-ttu-id="2d684-131">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2d684-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="2d684-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2d684-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="2d684-133"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="2d684-133"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="2d684-134">INSERI</span><span class="sxs-lookup"><span data-stu-id="2d684-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2d684-135"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2d684-135"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="2d684-136">DLL</span><span class="sxs-lookup"><span data-stu-id="2d684-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2d684-137"><dt>Shell32.dll (versão 5,0 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="2d684-137"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
