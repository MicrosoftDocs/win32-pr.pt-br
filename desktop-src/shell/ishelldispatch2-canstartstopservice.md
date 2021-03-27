---
description: Determina se o usuário atual pode iniciar e parar o serviço nomeado.
ms.assetid: cbb54ae9-02e6-4243-a782-e9f125c21c0d
title: Método IShellDispatch2. CanStartStopService (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch2.CanStartStopService
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 92655c2c561284f00204826e1848a75f00f4a04d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502081"
---
# <a name="ishelldispatch2canstartstopservice-method"></a><span data-ttu-id="d2bd7-103">Método IShellDispatch2. CanStartStopService</span><span class="sxs-lookup"><span data-stu-id="d2bd7-103">IShellDispatch2.CanStartStopService method</span></span>

<span data-ttu-id="d2bd7-104">Determina se o usuário atual pode iniciar e parar o serviço nomeado.</span><span class="sxs-lookup"><span data-stu-id="d2bd7-104">Determines if the current user can start and stop the named service.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2bd7-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d2bd7-105">Syntax</span></span>


```JScript
retVal = IShellDispatch2.CanStartStopService(
  sServiceName
)
```


```VB

IShellDispatch2.CanStartStopService( _
  ByVal sServiceName As String _
) As Variant
```





## <a name="parameters"></a><span data-ttu-id="d2bd7-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d2bd7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2bd7-107">*sServiceName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d2bd7-107">*sServiceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2bd7-108">Tipo: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d2bd7-108">Type: **String**</span></span>

<span data-ttu-id="d2bd7-109">Uma **cadeia de caracteres** que contém o nome do serviço.</span><span class="sxs-lookup"><span data-stu-id="d2bd7-109">A **String** that contains the name of the service.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2bd7-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d2bd7-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="d2bd7-111">JScript</span><span class="sxs-lookup"><span data-stu-id="d2bd7-111">JScript</span></span>

<span data-ttu-id="d2bd7-112">Tipo: \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="d2bd7-112">Type: \**Variant\** _</span></span>

<span data-ttu-id="d2bd7-113">Retorna _ *true*\* se o usuário puder iniciar e parar o serviço; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="d2bd7-113">Returns _ *true*\* if the user can start and stop the service; otherwise, **false**.</span></span>

### <a name="vb"></a><span data-ttu-id="d2bd7-114">VB</span><span class="sxs-lookup"><span data-stu-id="d2bd7-114">VB</span></span>

<span data-ttu-id="d2bd7-115">Tipo: \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="d2bd7-115">Type: \**Variant\** _</span></span>

<span data-ttu-id="d2bd7-116">Retorna _ *true*\* se o usuário puder iniciar e parar o serviço; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="d2bd7-116">Returns _ *true*\* if the user can start and stop the service; otherwise, **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="d2bd7-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="d2bd7-117">Remarks</span></span>

<span data-ttu-id="d2bd7-118">Esse método é implementado e acessado por meio do método [**shell. CanStartStopService**](./shell-canstartstopservice.md) .</span><span class="sxs-lookup"><span data-stu-id="d2bd7-118">This method is implemented and accessed through the [**Shell.CanStartStopService**](./shell-canstartstopservice.md) method.</span></span>

<span data-ttu-id="d2bd7-119">Este método não está disponível atualmente no Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="d2bd7-119">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="d2bd7-120">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d2bd7-120">Examples</span></span>

<span data-ttu-id="d2bd7-121">Os exemplos a seguir mostram o uso de **CanStartStopService** para JScript e VBScript.</span><span class="sxs-lookup"><span data-stu-id="d2bd7-121">The following examples show the usage of **CanStartStopService** for JScript and VBScript.</span></span>

<span data-ttu-id="d2bd7-122">JScript</span><span class="sxs-lookup"><span data-stu-id="d2bd7-122">JScript:</span></span>


```JScript
<script language="JScript">
    function fnCanStartStopServiceJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var bReturn;

        bReturn = objShell.CanStartStopService("service name");
    }
</script>
```



<span data-ttu-id="d2bd7-123">VBScript</span><span class="sxs-lookup"><span data-stu-id="d2bd7-123">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnCanStartStopServiceVB()
        dim objShell
        dim bReturn

        set objShell = CreateObject("shell.application")

        bReturn = objShell.CanStartStopService("service name")

        set objShell = nothing
    end function
</script>
```



## <a name="requirements"></a><span data-ttu-id="d2bd7-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d2bd7-124">Requirements</span></span>



| <span data-ttu-id="d2bd7-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2bd7-125">Requirement</span></span> | <span data-ttu-id="d2bd7-126">Valor</span><span class="sxs-lookup"><span data-stu-id="d2bd7-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2bd7-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d2bd7-127">Minimum supported client</span></span><br/> | <span data-ttu-id="d2bd7-128">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="d2bd7-128">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d2bd7-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d2bd7-129">Minimum supported server</span></span><br/> | <span data-ttu-id="d2bd7-130">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d2bd7-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="d2bd7-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d2bd7-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="d2bd7-132"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="d2bd7-132"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="d2bd7-133">INSERI</span><span class="sxs-lookup"><span data-stu-id="d2bd7-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d2bd7-134"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d2bd7-134"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="d2bd7-135">DLL</span><span class="sxs-lookup"><span data-stu-id="d2bd7-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d2bd7-136"><dt>Shell32.dll (versão 5,0 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="d2bd7-136"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
