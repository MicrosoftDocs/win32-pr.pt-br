---
description: Interrompe um serviço nomeado.
ms.assetid: AC22C91E-BBC6-4a2e-8D39-F9D7C0AC0947
title: Método Shell. OnStop (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.ServiceStop
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 31388078fe1c0e15c2e54efc86f0ff76bcfb7ed2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170088"
---
# <a name="shellservicestop-method"></a><span data-ttu-id="545b4-103">Método Shell. OnStop</span><span class="sxs-lookup"><span data-stu-id="545b4-103">Shell.ServiceStop method</span></span>

<span data-ttu-id="545b4-104">Interrompe um serviço nomeado.</span><span class="sxs-lookup"><span data-stu-id="545b4-104">Stops a named service.</span></span>

## <a name="syntax"></a><span data-ttu-id="545b4-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="545b4-105">Syntax</span></span>


```JScript
retVal = Shell.ServiceStop(
  sServiceName,
  vPersistent
)
```


```VB

Shell.ServiceStop( _
  ByVal sServiceName As BSTR, _
  ByVal vPersistent As Variant _
) As Variant
```





## <a name="parameters"></a><span data-ttu-id="545b4-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="545b4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="545b4-107">*sServiceName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="545b4-107">*sServiceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="545b4-108">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="545b4-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="545b4-109">Uma **cadeia de caracteres** que contém o nome do serviço.</span><span class="sxs-lookup"><span data-stu-id="545b4-109">A **String** that contains the name of the service.</span></span>

</dd> <dt>

<span data-ttu-id="545b4-110">*vPersistent* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="545b4-110">*vPersistent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="545b4-111">Tipo: **variante**</span><span class="sxs-lookup"><span data-stu-id="545b4-111">Type: **Variant**</span></span>

<span data-ttu-id="545b4-112">Defina como **true** para que o serviço seja iniciado pelo Gerenciador de controle de serviço quando o [**instart**](./shell-servicestart.md) for chamado.</span><span class="sxs-lookup"><span data-stu-id="545b4-112">Set to **true** to have the service started by the service control manager when [**ServiceStart**](./shell-servicestart.md) is called.</span></span> <span data-ttu-id="545b4-113">Para deixar a configuração de serviço inalterada, defina *vPersistent* como **false**.</span><span class="sxs-lookup"><span data-stu-id="545b4-113">To leave the service configuration unchanged, set *vPersistent* to **false**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="545b4-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="545b4-114">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="545b4-115">JScript</span><span class="sxs-lookup"><span data-stu-id="545b4-115">JScript</span></span>

<span data-ttu-id="545b4-116">Tipo: \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="545b4-116">Type: \**Variant\** _</span></span>

<span data-ttu-id="545b4-117">Retorna _ *true*\* se for bem-sucedido; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="545b4-117">Returns _ *true*\* if successful; otherwise, **false**.</span></span>

### <a name="vb"></a><span data-ttu-id="545b4-118">VB</span><span class="sxs-lookup"><span data-stu-id="545b4-118">VB</span></span>

<span data-ttu-id="545b4-119">Tipo: \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="545b4-119">Type: \**Variant\** _</span></span>

<span data-ttu-id="545b4-120">Retorna _ *true*\* se for bem-sucedido; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="545b4-120">Returns _ *true*\* if successful; otherwise, **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="545b4-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="545b4-121">Remarks</span></span>

<span data-ttu-id="545b4-122">O método retornará **false** se o serviço já tiver sido interrompido.</span><span class="sxs-lookup"><span data-stu-id="545b4-122">The method returns **false** if the service has already been stopped.</span></span> <span data-ttu-id="545b4-123">Antes de chamar esse método, você pode chamar [**shell. IsServiceRunning**](./shell-isservicerunning.md) para verificar o status do serviço.</span><span class="sxs-lookup"><span data-stu-id="545b4-123">Before calling this method, you can call [**Shell.IsServiceRunning**](./shell-isservicerunning.md) to ascertain the status of the service.</span></span>

<span data-ttu-id="545b4-124">Este método não está disponível atualmente no Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="545b4-124">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="545b4-125">Exemplos</span><span class="sxs-lookup"><span data-stu-id="545b4-125">Examples</span></span>

<span data-ttu-id="545b4-126">Os exemplos a seguir mostram o uso de **OnStop** para interromper o serviço de mensageiro.</span><span class="sxs-lookup"><span data-stu-id="545b4-126">The following examples show the use of **ServiceStop** to stop the Messenger service.</span></span> <span data-ttu-id="545b4-127">O uso é mostrado para JScript e VBScript.</span><span class="sxs-lookup"><span data-stu-id="545b4-127">Usage is shown for JScript and VBScript.</span></span>

<span data-ttu-id="545b4-128">JScript</span><span class="sxs-lookup"><span data-stu-id="545b4-128">JScript:</span></span>


```JScript
<script language="JScript">
    function fnServiceStopJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var bReturn;
        
        bReturn = objShell.ServiceStop("Messenger", true);
    }
</script>
```



<span data-ttu-id="545b4-129">VBScript</span><span class="sxs-lookup"><span data-stu-id="545b4-129">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnServiceStopVB()
        dim objShell
        dim bReturn

        set objShell = CreateObject("shell.application")

        bReturn = objShell.ServiceStop("Messenger", true)

        set objShell = nothing
    end function
</script>
```



## <a name="requirements"></a><span data-ttu-id="545b4-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="545b4-130">Requirements</span></span>



| <span data-ttu-id="545b4-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="545b4-131">Requirement</span></span> | <span data-ttu-id="545b4-132">Valor</span><span class="sxs-lookup"><span data-stu-id="545b4-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="545b4-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="545b4-133">Minimum supported client</span></span><br/> | <span data-ttu-id="545b4-134">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="545b4-134">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="545b4-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="545b4-135">Minimum supported server</span></span><br/> | <span data-ttu-id="545b4-136">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="545b4-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="545b4-137">parâmetro</span><span class="sxs-lookup"><span data-stu-id="545b4-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="545b4-138"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="545b4-138"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="545b4-139">INSERI</span><span class="sxs-lookup"><span data-stu-id="545b4-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="545b4-140"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="545b4-140"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="545b4-141">DLL</span><span class="sxs-lookup"><span data-stu-id="545b4-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="545b4-142"><dt>Shell32.dll (versão 5,0 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="545b4-142"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
