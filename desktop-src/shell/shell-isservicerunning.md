---
description: Método Shell. IsServiceRunning – retorna um valor que indica se um serviço específico está em execução.
ms.assetid: FDC41C2D-7462-458f-BBE6-D97260C26B6C
title: Método Shell. IsServiceRunning (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.IsServiceRunning
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 01af900bb7930ec7b6dde0b0700c83f211733dc3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083710"
---
# <a name="shellisservicerunning-method"></a><span data-ttu-id="6dd2b-103">Método Shell. IsServiceRunning</span><span class="sxs-lookup"><span data-stu-id="6dd2b-103">Shell.IsServiceRunning method</span></span>

<span data-ttu-id="6dd2b-104">Retorna um valor que indica se um serviço específico está em execução.</span><span class="sxs-lookup"><span data-stu-id="6dd2b-104">Returns a value that indicates whether a particular service is running.</span></span>

## <a name="syntax"></a><span data-ttu-id="6dd2b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6dd2b-105">Syntax</span></span>


```JScript
retVal = Shell.IsServiceRunning(
  sServiceName
)
```


```VB

Shell.IsServiceRunning( _
  ByVal sServiceName As BSTR _
) As Variant
```





## <a name="parameters"></a><span data-ttu-id="6dd2b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6dd2b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6dd2b-107">*sServiceName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6dd2b-107">*sServiceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6dd2b-108">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="6dd2b-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="6dd2b-109">Uma **cadeia de caracteres** que contém o nome do serviço.</span><span class="sxs-lookup"><span data-stu-id="6dd2b-109">A **String** that contains the name of the service.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6dd2b-110">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="6dd2b-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="6dd2b-111">JScript</span><span class="sxs-lookup"><span data-stu-id="6dd2b-111">JScript</span></span>

<span data-ttu-id="6dd2b-112">Tipo: **variante \***</span><span class="sxs-lookup"><span data-stu-id="6dd2b-112">Type: **Variant\***</span></span>

<span data-ttu-id="6dd2b-113">Retornará **true** se o serviço especificado por *sServiceName* estiver em execução; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="6dd2b-113">Returns **true** if the service specified by *sServiceName* is running; otherwise, **false**.</span></span>

### <a name="vb"></a><span data-ttu-id="6dd2b-114">VB</span><span class="sxs-lookup"><span data-stu-id="6dd2b-114">VB</span></span>

<span data-ttu-id="6dd2b-115">Tipo: **variante \***</span><span class="sxs-lookup"><span data-stu-id="6dd2b-115">Type: **Variant\***</span></span>

<span data-ttu-id="6dd2b-116">Retornará **true** se o serviço especificado por *sServiceName* estiver em execução; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="6dd2b-116">Returns **true** if the service specified by *sServiceName* is running; otherwise, **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="6dd2b-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="6dd2b-117">Remarks</span></span>

<span data-ttu-id="6dd2b-118">Este método não está disponível atualmente no Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="6dd2b-118">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="6dd2b-119">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6dd2b-119">Examples</span></span>

<span data-ttu-id="6dd2b-120">Os exemplos a seguir mostram o uso de **IsServiceRunning** para determinar se o serviço de temas está em execução para um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6dd2b-120">The following examples show the use of **IsServiceRunning** to determine whether the Themes service is running for an application.</span></span> <span data-ttu-id="6dd2b-121">O uso é mostrado para JScript e VBScript.</span><span class="sxs-lookup"><span data-stu-id="6dd2b-121">Usage is shown for JScript and VBScript.</span></span>

<span data-ttu-id="6dd2b-122">JScript</span><span class="sxs-lookup"><span data-stu-id="6dd2b-122">JScript:</span></span>


```JScript
function fnIsServiceRunningJ()
{
    var objShell = new ActiveXObject("shell.application");
    var bReturn;

    bReturn = objShell.IsServiceRunning("Themes");
}
```



<span data-ttu-id="6dd2b-123">VBScript</span><span class="sxs-lookup"><span data-stu-id="6dd2b-123">VBScript:</span></span>


```VB
function fnIsServiceRunningVB()
    dim objShell
    dim bReturn

    set objShell = CreateObject("shell.application")

    bReturn = objShell.IsServiceRunning("Themes")

    set objShell = nothing
end function
```



## <a name="requirements"></a><span data-ttu-id="6dd2b-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6dd2b-124">Requirements</span></span>



| <span data-ttu-id="6dd2b-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="6dd2b-125">Requirement</span></span> | <span data-ttu-id="6dd2b-126">Valor</span><span class="sxs-lookup"><span data-stu-id="6dd2b-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6dd2b-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6dd2b-127">Minimum supported client</span></span><br/> | <span data-ttu-id="6dd2b-128">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="6dd2b-128">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6dd2b-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6dd2b-129">Minimum supported server</span></span><br/> | <span data-ttu-id="6dd2b-130">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6dd2b-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="6dd2b-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6dd2b-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="6dd2b-132"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="6dd2b-132"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="6dd2b-133">INSERI</span><span class="sxs-lookup"><span data-stu-id="6dd2b-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6dd2b-134"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="6dd2b-134"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="6dd2b-135">DLL</span><span class="sxs-lookup"><span data-stu-id="6dd2b-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6dd2b-136"><dt>Shell32.dll (versão 5,0 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="6dd2b-136"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
