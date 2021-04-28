---
description: Método IShellDispatch2. CanStartStopService – determina se o usuário atual pode iniciar e parar o serviço nomeado.
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
ms.openlocfilehash: 600cf7fafd556a9192c4b0de4089516bc6cca2a0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117124"
---
# <a name="ishelldispatch2canstartstopservice-method"></a><span data-ttu-id="9b7b8-103">Método IShellDispatch2. CanStartStopService</span><span class="sxs-lookup"><span data-stu-id="9b7b8-103">IShellDispatch2.CanStartStopService method</span></span>

<span data-ttu-id="9b7b8-104">Determina se o usuário atual pode iniciar e parar o serviço nomeado.</span><span class="sxs-lookup"><span data-stu-id="9b7b8-104">Determines if the current user can start and stop the named service.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b7b8-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9b7b8-105">Syntax</span></span>


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





## <a name="parameters"></a><span data-ttu-id="9b7b8-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9b7b8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b7b8-107">*sServiceName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9b7b8-107">*sServiceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b7b8-108">Tipo: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9b7b8-108">Type: **String**</span></span>

<span data-ttu-id="9b7b8-109">Uma **cadeia de caracteres** que contém o nome do serviço.</span><span class="sxs-lookup"><span data-stu-id="9b7b8-109">A **String** that contains the name of the service.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9b7b8-110">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="9b7b8-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="9b7b8-111">JScript</span><span class="sxs-lookup"><span data-stu-id="9b7b8-111">JScript</span></span>

<span data-ttu-id="9b7b8-112">Tipo: **variante \***</span><span class="sxs-lookup"><span data-stu-id="9b7b8-112">Type: **Variant\***</span></span>

<span data-ttu-id="9b7b8-113">Retornará **true** se o usuário puder iniciar e parar o serviço; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="9b7b8-113">Returns **true** if the user can start and stop the service; otherwise, **false**.</span></span>

### <a name="vb"></a><span data-ttu-id="9b7b8-114">VB</span><span class="sxs-lookup"><span data-stu-id="9b7b8-114">VB</span></span>

<span data-ttu-id="9b7b8-115">Tipo: **variante \***</span><span class="sxs-lookup"><span data-stu-id="9b7b8-115">Type: **Variant\***</span></span>

<span data-ttu-id="9b7b8-116">Retornará **true** se o usuário puder iniciar e parar o serviço; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="9b7b8-116">Returns **true** if the user can start and stop the service; otherwise, **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="9b7b8-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="9b7b8-117">Remarks</span></span>

<span data-ttu-id="9b7b8-118">Esse método é implementado e acessado por meio do método [**shell. CanStartStopService**](./shell-canstartstopservice.md) .</span><span class="sxs-lookup"><span data-stu-id="9b7b8-118">This method is implemented and accessed through the [**Shell.CanStartStopService**](./shell-canstartstopservice.md) method.</span></span>

<span data-ttu-id="9b7b8-119">Este método não está disponível atualmente no Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="9b7b8-119">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="9b7b8-120">Exemplos</span><span class="sxs-lookup"><span data-stu-id="9b7b8-120">Examples</span></span>

<span data-ttu-id="9b7b8-121">Os exemplos a seguir mostram o uso de **CanStartStopService** para JScript e VBScript.</span><span class="sxs-lookup"><span data-stu-id="9b7b8-121">The following examples show the usage of **CanStartStopService** for JScript and VBScript.</span></span>

<span data-ttu-id="9b7b8-122">JScript</span><span class="sxs-lookup"><span data-stu-id="9b7b8-122">JScript:</span></span>


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



<span data-ttu-id="9b7b8-123">VBScript</span><span class="sxs-lookup"><span data-stu-id="9b7b8-123">VBScript:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="9b7b8-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9b7b8-124">Requirements</span></span>



| <span data-ttu-id="9b7b8-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="9b7b8-125">Requirement</span></span> | <span data-ttu-id="9b7b8-126">Valor</span><span class="sxs-lookup"><span data-stu-id="9b7b8-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b7b8-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9b7b8-127">Minimum supported client</span></span><br/> | <span data-ttu-id="9b7b8-128">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="9b7b8-128">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9b7b8-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9b7b8-129">Minimum supported server</span></span><br/> | <span data-ttu-id="9b7b8-130">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9b7b8-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="9b7b8-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9b7b8-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="9b7b8-132"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="9b7b8-132"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="9b7b8-133">INSERI</span><span class="sxs-lookup"><span data-stu-id="9b7b8-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9b7b8-134"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9b7b8-134"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="9b7b8-135">DLL</span><span class="sxs-lookup"><span data-stu-id="9b7b8-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9b7b8-136"><dt>Shell32.dll (versão 5,0 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="9b7b8-136"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
