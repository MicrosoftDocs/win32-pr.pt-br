---
description: Determina se o usuário atual pode iniciar e parar o serviço nomeado.
ms.assetid: 1428F529-61F6-4113-A553-2C0D617FD859
title: Método Shell. CanStartStopService (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.CanStartStopService
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 1d92fa076141bdebc8a2f24059a65e842e5a3d6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103921975"
---
# <a name="shellcanstartstopservice-method"></a><span data-ttu-id="93596-103">Método Shell. CanStartStopService</span><span class="sxs-lookup"><span data-stu-id="93596-103">Shell.CanStartStopService method</span></span>

<span data-ttu-id="93596-104">Determina se o usuário atual pode iniciar e parar o serviço nomeado.</span><span class="sxs-lookup"><span data-stu-id="93596-104">Determines if the current user can start and stop the named service.</span></span>

## <a name="syntax"></a><span data-ttu-id="93596-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="93596-105">Syntax</span></span>


```JScript
retVal = Shell.CanStartStopService(
  sServiceName
)
```


```VB

Shell.CanStartStopService( _
  ByVal sServiceName As String _
) As Variant
```





## <a name="parameters"></a><span data-ttu-id="93596-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="93596-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93596-107">*sServiceName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="93596-107">*sServiceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93596-108">Tipo: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="93596-108">Type: **String**</span></span>

<span data-ttu-id="93596-109">Uma **cadeia de caracteres** que contém o nome do serviço.</span><span class="sxs-lookup"><span data-stu-id="93596-109">A **String** that contains the name of the service.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93596-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="93596-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="93596-111">JScript</span><span class="sxs-lookup"><span data-stu-id="93596-111">JScript</span></span>

<span data-ttu-id="93596-112">Tipo: \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="93596-112">Type: \**Variant\** _</span></span>

<span data-ttu-id="93596-113">Retorna _ *true*\* se o usuário puder iniciar e parar o serviço; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="93596-113">Returns _ *true*\* if the user can start and stop the service; otherwise, **false**.</span></span>

### <a name="vb"></a><span data-ttu-id="93596-114">VB</span><span class="sxs-lookup"><span data-stu-id="93596-114">VB</span></span>

<span data-ttu-id="93596-115">Tipo: \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="93596-115">Type: \**Variant\** _</span></span>

<span data-ttu-id="93596-116">Retorna _ *true*\* se o usuário puder iniciar e parar o serviço; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="93596-116">Returns _ *true*\* if the user can start and stop the service; otherwise, **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="93596-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="93596-117">Remarks</span></span>

<span data-ttu-id="93596-118">Este método não está disponível atualmente no Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="93596-118">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="93596-119">Exemplos</span><span class="sxs-lookup"><span data-stu-id="93596-119">Examples</span></span>

<span data-ttu-id="93596-120">Os exemplos a seguir mostram o uso de **CanStartStopService** para JScript e VBScript.</span><span class="sxs-lookup"><span data-stu-id="93596-120">The following examples show the usage of **CanStartStopService** for JScript and VBScript.</span></span>

<span data-ttu-id="93596-121">JScript</span><span class="sxs-lookup"><span data-stu-id="93596-121">JScript:</span></span>


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



<span data-ttu-id="93596-122">VBScript</span><span class="sxs-lookup"><span data-stu-id="93596-122">VBScript:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="93596-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="93596-123">Requirements</span></span>



| <span data-ttu-id="93596-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="93596-124">Requirement</span></span> | <span data-ttu-id="93596-125">Valor</span><span class="sxs-lookup"><span data-stu-id="93596-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93596-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="93596-126">Minimum supported client</span></span><br/> | <span data-ttu-id="93596-127">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="93596-127">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="93596-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="93596-128">Minimum supported server</span></span><br/> | <span data-ttu-id="93596-129">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="93596-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="93596-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="93596-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="93596-131"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="93596-131"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="93596-132">INSERI</span><span class="sxs-lookup"><span data-stu-id="93596-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="93596-133"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="93596-133"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="93596-134">DLL</span><span class="sxs-lookup"><span data-stu-id="93596-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="93596-135"><dt>Shell32.dll (versão 5,0 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="93596-135"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 




