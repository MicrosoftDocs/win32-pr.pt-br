---
description: Método Shell. CanStartStopService – determina se o usuário atual pode iniciar e parar o serviço nomeado.
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
ms.openlocfilehash: 29561519b95329093ef1f7bfc64023fd1ac4533d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083684"
---
# <a name="shellcanstartstopservice-method"></a><span data-ttu-id="0808a-103">Método Shell. CanStartStopService</span><span class="sxs-lookup"><span data-stu-id="0808a-103">Shell.CanStartStopService method</span></span>

<span data-ttu-id="0808a-104">Determina se o usuário atual pode iniciar e parar o serviço nomeado.</span><span class="sxs-lookup"><span data-stu-id="0808a-104">Determines if the current user can start and stop the named service.</span></span>

## <a name="syntax"></a><span data-ttu-id="0808a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0808a-105">Syntax</span></span>


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





## <a name="parameters"></a><span data-ttu-id="0808a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0808a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0808a-107">*sServiceName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0808a-107">*sServiceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0808a-108">Tipo: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0808a-108">Type: **String**</span></span>

<span data-ttu-id="0808a-109">Uma **cadeia de caracteres** que contém o nome do serviço.</span><span class="sxs-lookup"><span data-stu-id="0808a-109">A **String** that contains the name of the service.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0808a-110">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="0808a-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="0808a-111">JScript</span><span class="sxs-lookup"><span data-stu-id="0808a-111">JScript</span></span>

<span data-ttu-id="0808a-112">Tipo: **variante \***</span><span class="sxs-lookup"><span data-stu-id="0808a-112">Type: **Variant\***</span></span>

<span data-ttu-id="0808a-113">Retornará **true** se o usuário puder iniciar e parar o serviço; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="0808a-113">Returns **true** if the user can start and stop the service; otherwise, **false**.</span></span>

### <a name="vb"></a><span data-ttu-id="0808a-114">VB</span><span class="sxs-lookup"><span data-stu-id="0808a-114">VB</span></span>

<span data-ttu-id="0808a-115">Tipo: **variante \***</span><span class="sxs-lookup"><span data-stu-id="0808a-115">Type: **Variant\***</span></span>

<span data-ttu-id="0808a-116">Retornará **true** se o usuário puder iniciar e parar o serviço; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="0808a-116">Returns **true** if the user can start and stop the service; otherwise, **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="0808a-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="0808a-117">Remarks</span></span>

<span data-ttu-id="0808a-118">Este método não está disponível atualmente no Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="0808a-118">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="0808a-119">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0808a-119">Examples</span></span>

<span data-ttu-id="0808a-120">Os exemplos a seguir mostram o uso de **CanStartStopService** para JScript e VBScript.</span><span class="sxs-lookup"><span data-stu-id="0808a-120">The following examples show the usage of **CanStartStopService** for JScript and VBScript.</span></span>

<span data-ttu-id="0808a-121">JScript</span><span class="sxs-lookup"><span data-stu-id="0808a-121">JScript:</span></span>


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



<span data-ttu-id="0808a-122">VBScript</span><span class="sxs-lookup"><span data-stu-id="0808a-122">VBScript:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="0808a-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0808a-123">Requirements</span></span>



| <span data-ttu-id="0808a-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="0808a-124">Requirement</span></span> | <span data-ttu-id="0808a-125">Valor</span><span class="sxs-lookup"><span data-stu-id="0808a-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0808a-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0808a-126">Minimum supported client</span></span><br/> | <span data-ttu-id="0808a-127">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="0808a-127">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0808a-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0808a-128">Minimum supported server</span></span><br/> | <span data-ttu-id="0808a-129">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0808a-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="0808a-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0808a-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="0808a-131"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="0808a-131"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="0808a-132">INSERI</span><span class="sxs-lookup"><span data-stu-id="0808a-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0808a-133"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0808a-133"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="0808a-134">DLL</span><span class="sxs-lookup"><span data-stu-id="0808a-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0808a-135"><dt>Shell32.dll (versão 5,0 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="0808a-135"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 




