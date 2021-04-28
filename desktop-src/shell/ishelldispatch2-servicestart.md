---
description: Método IShellDispatch2. FileStart – inicia um serviço nomeado.
ms.assetid: 3af57cdc-f449-433d-a9e1-119038045e4c
title: Método IShellDispatch2. OnStart (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch2.ServiceStart
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: c0f4fa218c4def993025ff18bffd0cc54def9818
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117044"
---
# <a name="ishelldispatch2servicestart-method"></a><span data-ttu-id="9219c-103">Método IShellDispatch2. OnStart</span><span class="sxs-lookup"><span data-stu-id="9219c-103">IShellDispatch2.ServiceStart method</span></span>

<span data-ttu-id="9219c-104">Inicia um serviço nomeado.</span><span class="sxs-lookup"><span data-stu-id="9219c-104">Starts a named service.</span></span>

## <a name="syntax"></a><span data-ttu-id="9219c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9219c-105">Syntax</span></span>


```JScript
retVal = IShellDispatch2.ServiceStart(
  sServiceName,
  vPersistent
)
```


```VB

IShellDispatch2.ServiceStart( _
  ByVal sServiceName As BSTR, _
  ByVal vPersistent As Variant _
) As Variant
```





## <a name="parameters"></a><span data-ttu-id="9219c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9219c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9219c-107">*sServiceName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9219c-107">*sServiceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9219c-108">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="9219c-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="9219c-109">Uma **cadeia de caracteres** que contém o nome do serviço.</span><span class="sxs-lookup"><span data-stu-id="9219c-109">A **String** that contains the name of the service.</span></span>

</dd> <dt>

<span data-ttu-id="9219c-110">*vPersistent* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9219c-110">*vPersistent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9219c-111">Tipo: **variante**</span><span class="sxs-lookup"><span data-stu-id="9219c-111">Type: **Variant**</span></span>

<span data-ttu-id="9219c-112">Defina como **true** para que o serviço seja iniciado automaticamente pelo Gerenciador de controle de serviço durante a inicialização do sistema.</span><span class="sxs-lookup"><span data-stu-id="9219c-112">Set to **true** to have the service started automatically by the service control manager during system startup.</span></span> <span data-ttu-id="9219c-113">Defina como **false** para deixar a configuração de serviço inalterada.</span><span class="sxs-lookup"><span data-stu-id="9219c-113">Set to **false** to leave the service configuration unchanged.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9219c-114">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="9219c-114">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="9219c-115">JScript</span><span class="sxs-lookup"><span data-stu-id="9219c-115">JScript</span></span>

<span data-ttu-id="9219c-116">Tipo: **variante \***</span><span class="sxs-lookup"><span data-stu-id="9219c-116">Type: **Variant\***</span></span>

<span data-ttu-id="9219c-117">Retornará **true** se for bem-sucedido; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="9219c-117">Returns **true** if successful; otherwise, **false**.</span></span>

### <a name="vb"></a><span data-ttu-id="9219c-118">VB</span><span class="sxs-lookup"><span data-stu-id="9219c-118">VB</span></span>

<span data-ttu-id="9219c-119">Tipo: **variante \***</span><span class="sxs-lookup"><span data-stu-id="9219c-119">Type: **Variant\***</span></span>

<span data-ttu-id="9219c-120">Retornará **true** se for bem-sucedido; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="9219c-120">Returns **true** if successful; otherwise, **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="9219c-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="9219c-121">Remarks</span></span>

<span data-ttu-id="9219c-122">Esse método é implementado e acessado por meio do método [**shell. OnStart**](./shell-servicestart.md) .</span><span class="sxs-lookup"><span data-stu-id="9219c-122">This method is implemented and accessed through the [**Shell.ServiceStart**](./shell-servicestart.md) method.</span></span>

<span data-ttu-id="9219c-123">O método retornará **false** se o serviço já tiver sido iniciado.</span><span class="sxs-lookup"><span data-stu-id="9219c-123">The method returns **false** if the service has already been started.</span></span> <span data-ttu-id="9219c-124">Antes de chamar esse método, você pode chamar [**shell. IsServiceRunning**](./shell-isservicerunning.md) para verificar o status do serviço.</span><span class="sxs-lookup"><span data-stu-id="9219c-124">Before calling this method, you can call [**Shell.IsServiceRunning**](./shell-isservicerunning.md) to ascertain the status of the service.</span></span>

<span data-ttu-id="9219c-125">Este método não está disponível atualmente no Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="9219c-125">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="9219c-126">Exemplos</span><span class="sxs-lookup"><span data-stu-id="9219c-126">Examples</span></span>

<span data-ttu-id="9219c-127">Os exemplos a seguir mostram o uso do **Imstart** para iniciar o serviço mensageiro.</span><span class="sxs-lookup"><span data-stu-id="9219c-127">The following examples show the use of **ServiceStart** to start the Messenger service.</span></span> <span data-ttu-id="9219c-128">O uso é mostrado para JScript e VBScript.</span><span class="sxs-lookup"><span data-stu-id="9219c-128">Usage is shown for JScript and VBScript.</span></span>

<span data-ttu-id="9219c-129">JScript</span><span class="sxs-lookup"><span data-stu-id="9219c-129">JScript:</span></span>


```JScript
<script language="JScript">
    function fnServiceStartJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var bReturn;
        
        bReturn = objShell.ServiceStart("Messenger", true);
    }
</script>
```



<span data-ttu-id="9219c-130">VBScript</span><span class="sxs-lookup"><span data-stu-id="9219c-130">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnServiceStartVB()
        dim objShell
        dim bReturn

        set objShell = CreateObject("shell.application")

        bReturn = objShell.ServiceStart("Messenger", true)

        set objShell = nothing
    end function
</script>
```



## <a name="requirements"></a><span data-ttu-id="9219c-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9219c-131">Requirements</span></span>



| <span data-ttu-id="9219c-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="9219c-132">Requirement</span></span> | <span data-ttu-id="9219c-133">Valor</span><span class="sxs-lookup"><span data-stu-id="9219c-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9219c-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9219c-134">Minimum supported client</span></span><br/> | <span data-ttu-id="9219c-135">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="9219c-135">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9219c-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9219c-136">Minimum supported server</span></span><br/> | <span data-ttu-id="9219c-137">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9219c-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="9219c-138">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9219c-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="9219c-139"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="9219c-139"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="9219c-140">INSERI</span><span class="sxs-lookup"><span data-stu-id="9219c-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9219c-141"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9219c-141"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="9219c-142">DLL</span><span class="sxs-lookup"><span data-stu-id="9219c-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9219c-143"><dt>Shell32.dll (versão 5,0 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="9219c-143"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
