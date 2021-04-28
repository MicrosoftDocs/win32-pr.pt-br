---
description: Método IShellDispatch2. instop – interrompe um serviço nomeado.
ms.assetid: f4cd0e2c-4ecc-4e9f-a0b5-d2a8a739f0e2
title: Método IShellDispatch2. OnStop (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch2.ServiceStop
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 651138eb687cfd83406bc6e1a7fcf520ff001171
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117024"
---
# <a name="ishelldispatch2servicestop-method"></a><span data-ttu-id="6d0dd-103">Método IShellDispatch2. OnStop</span><span class="sxs-lookup"><span data-stu-id="6d0dd-103">IShellDispatch2.ServiceStop method</span></span>

<span data-ttu-id="6d0dd-104">Interrompe um serviço nomeado.</span><span class="sxs-lookup"><span data-stu-id="6d0dd-104">Stops a named service.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d0dd-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6d0dd-105">Syntax</span></span>


```JScript
retVal = IShellDispatch2.ServiceStop(
  sServiceName,
  vPersistent
)
```


```VB

IShellDispatch2.ServiceStop( _
  ByVal sServiceName As BSTR, _
  ByVal vPersistent As Variant _
) As Variant
```





## <a name="parameters"></a><span data-ttu-id="6d0dd-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6d0dd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d0dd-107">*sServiceName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6d0dd-107">*sServiceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d0dd-108">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="6d0dd-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="6d0dd-109">Uma **cadeia de caracteres** que contém o nome do serviço.</span><span class="sxs-lookup"><span data-stu-id="6d0dd-109">A **String** that contains the name of the service.</span></span>

</dd> <dt>

<span data-ttu-id="6d0dd-110">*vPersistent* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6d0dd-110">*vPersistent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d0dd-111">Tipo: **variante**</span><span class="sxs-lookup"><span data-stu-id="6d0dd-111">Type: **Variant**</span></span>

<span data-ttu-id="6d0dd-112">Defina como **true** para que o serviço seja iniciado pelo Gerenciador de controle de serviço quando o [**instart**](ishelldispatch2-servicestart.md) for chamado.</span><span class="sxs-lookup"><span data-stu-id="6d0dd-112">Set to **true** to have the service started by the service control manager when [**ServiceStart**](ishelldispatch2-servicestart.md) is called.</span></span> <span data-ttu-id="6d0dd-113">Para deixar a configuração de serviço inalterada, defina *vPersistent* como **false**.</span><span class="sxs-lookup"><span data-stu-id="6d0dd-113">To leave the service configuration unchanged, set *vPersistent* to **false**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6d0dd-114">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="6d0dd-114">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="6d0dd-115">JScript</span><span class="sxs-lookup"><span data-stu-id="6d0dd-115">JScript</span></span>

<span data-ttu-id="6d0dd-116">Tipo: **variante \***</span><span class="sxs-lookup"><span data-stu-id="6d0dd-116">Type: **Variant\***</span></span>

<span data-ttu-id="6d0dd-117">Retornará **true** se for bem-sucedido; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="6d0dd-117">Returns **true** if successful; otherwise, **false**.</span></span>

### <a name="vb"></a><span data-ttu-id="6d0dd-118">VB</span><span class="sxs-lookup"><span data-stu-id="6d0dd-118">VB</span></span>

<span data-ttu-id="6d0dd-119">Tipo: **variante \***</span><span class="sxs-lookup"><span data-stu-id="6d0dd-119">Type: **Variant\***</span></span>

<span data-ttu-id="6d0dd-120">Retornará **true** se for bem-sucedido; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="6d0dd-120">Returns **true** if successful; otherwise, **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="6d0dd-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="6d0dd-121">Remarks</span></span>

<span data-ttu-id="6d0dd-122">Esse método é implementado e acessado por meio do método [**shell. OnStop**](./shell-servicestop.md) .</span><span class="sxs-lookup"><span data-stu-id="6d0dd-122">This method is implemented and accessed through the [**Shell.ServiceStop**](./shell-servicestop.md) method.</span></span>

<span data-ttu-id="6d0dd-123">O método retornará **false** se o serviço já tiver sido interrompido.</span><span class="sxs-lookup"><span data-stu-id="6d0dd-123">The method returns **false** if the service has already been stopped.</span></span> <span data-ttu-id="6d0dd-124">Antes de chamar esse método, você pode chamar [**shell. IsServiceRunning**](./shell-isservicerunning.md) para verificar o status do serviço.</span><span class="sxs-lookup"><span data-stu-id="6d0dd-124">Before calling this method, you can call [**Shell.IsServiceRunning**](./shell-isservicerunning.md) to ascertain the status of the service.</span></span>

<span data-ttu-id="6d0dd-125">Este método não está disponível atualmente no Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="6d0dd-125">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="6d0dd-126">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6d0dd-126">Examples</span></span>

<span data-ttu-id="6d0dd-127">Os exemplos a seguir mostram o uso de **OnStop** para interromper o serviço de mensageiro.</span><span class="sxs-lookup"><span data-stu-id="6d0dd-127">The following examples show the use of **ServiceStop** to stop the Messenger service.</span></span> <span data-ttu-id="6d0dd-128">O uso é mostrado para JScript e VBScript.</span><span class="sxs-lookup"><span data-stu-id="6d0dd-128">Usage is shown for JScript and VBScript.</span></span>

<span data-ttu-id="6d0dd-129">JScript</span><span class="sxs-lookup"><span data-stu-id="6d0dd-129">JScript:</span></span>


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



<span data-ttu-id="6d0dd-130">VBScript</span><span class="sxs-lookup"><span data-stu-id="6d0dd-130">VBScript:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="6d0dd-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6d0dd-131">Requirements</span></span>



| <span data-ttu-id="6d0dd-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="6d0dd-132">Requirement</span></span> | <span data-ttu-id="6d0dd-133">Valor</span><span class="sxs-lookup"><span data-stu-id="6d0dd-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d0dd-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6d0dd-134">Minimum supported client</span></span><br/> | <span data-ttu-id="6d0dd-135">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="6d0dd-135">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6d0dd-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6d0dd-136">Minimum supported server</span></span><br/> | <span data-ttu-id="6d0dd-137">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6d0dd-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="6d0dd-138">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6d0dd-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="6d0dd-139"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="6d0dd-139"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="6d0dd-140">INSERI</span><span class="sxs-lookup"><span data-stu-id="6d0dd-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6d0dd-141"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="6d0dd-141"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="6d0dd-142">DLL</span><span class="sxs-lookup"><span data-stu-id="6d0dd-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6d0dd-143"><dt>Shell32.dll (versão 5,0 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="6d0dd-143"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
