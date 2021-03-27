---
description: Retorna um valor que indica se um serviço específico está em execução.
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
ms.openlocfilehash: c3a65be4955c6f49e8e6baa49cd9dedb82fc5cc8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828461"
---
# <a name="shellisservicerunning-method"></a><span data-ttu-id="a5700-103">Método Shell. IsServiceRunning</span><span class="sxs-lookup"><span data-stu-id="a5700-103">Shell.IsServiceRunning method</span></span>

<span data-ttu-id="a5700-104">Retorna um valor que indica se um serviço específico está em execução.</span><span class="sxs-lookup"><span data-stu-id="a5700-104">Returns a value that indicates whether a particular service is running.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5700-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a5700-105">Syntax</span></span>


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





## <a name="parameters"></a><span data-ttu-id="a5700-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a5700-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5700-107">*sServiceName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a5700-107">*sServiceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5700-108">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="a5700-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="a5700-109">Uma **cadeia de caracteres** que contém o nome do serviço.</span><span class="sxs-lookup"><span data-stu-id="a5700-109">A **String** that contains the name of the service.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a5700-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a5700-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="a5700-111">JScript</span><span class="sxs-lookup"><span data-stu-id="a5700-111">JScript</span></span>

<span data-ttu-id="a5700-112">Tipo: \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="a5700-112">Type: \**Variant\** _</span></span>

<span data-ttu-id="a5700-113">Retorna _ *true*\* se o serviço especificado por *sServiceName* estiver em execução; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="a5700-113">Returns _ *true*\* if the service specified by *sServiceName* is running; otherwise, **false**.</span></span>

### <a name="vb"></a><span data-ttu-id="a5700-114">VB</span><span class="sxs-lookup"><span data-stu-id="a5700-114">VB</span></span>

<span data-ttu-id="a5700-115">Tipo: \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="a5700-115">Type: \**Variant\** _</span></span>

<span data-ttu-id="a5700-116">Retorna _ *true*\* se o serviço especificado por *sServiceName* estiver em execução; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="a5700-116">Returns _ *true*\* if the service specified by *sServiceName* is running; otherwise, **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="a5700-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="a5700-117">Remarks</span></span>

<span data-ttu-id="a5700-118">Este método não está disponível atualmente no Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="a5700-118">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="a5700-119">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a5700-119">Examples</span></span>

<span data-ttu-id="a5700-120">Os exemplos a seguir mostram o uso de **IsServiceRunning** para determinar se o serviço de temas está em execução para um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a5700-120">The following examples show the use of **IsServiceRunning** to determine whether the Themes service is running for an application.</span></span> <span data-ttu-id="a5700-121">O uso é mostrado para JScript e VBScript.</span><span class="sxs-lookup"><span data-stu-id="a5700-121">Usage is shown for JScript and VBScript.</span></span>

<span data-ttu-id="a5700-122">JScript</span><span class="sxs-lookup"><span data-stu-id="a5700-122">JScript:</span></span>


```JScript
function fnIsServiceRunningJ()
{
    var objShell = new ActiveXObject("shell.application");
    var bReturn;

    bReturn = objShell.IsServiceRunning("Themes");
}
```



<span data-ttu-id="a5700-123">VBScript</span><span class="sxs-lookup"><span data-stu-id="a5700-123">VBScript:</span></span>


```VB
function fnIsServiceRunningVB()
    dim objShell
    dim bReturn

    set objShell = CreateObject("shell.application")

    bReturn = objShell.IsServiceRunning("Themes")

    set objShell = nothing
end function
```



## <a name="requirements"></a><span data-ttu-id="a5700-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a5700-124">Requirements</span></span>



| <span data-ttu-id="a5700-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="a5700-125">Requirement</span></span> | <span data-ttu-id="a5700-126">Valor</span><span class="sxs-lookup"><span data-stu-id="a5700-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5700-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a5700-127">Minimum supported client</span></span><br/> | <span data-ttu-id="a5700-128">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="a5700-128">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a5700-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a5700-129">Minimum supported server</span></span><br/> | <span data-ttu-id="a5700-130">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a5700-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="a5700-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a5700-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="a5700-132"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="a5700-132"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="a5700-133">INSERI</span><span class="sxs-lookup"><span data-stu-id="a5700-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a5700-134"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a5700-134"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="a5700-135">DLL</span><span class="sxs-lookup"><span data-stu-id="a5700-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a5700-136"><dt>Shell32.dll (versão 5,0 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="a5700-136"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
