---
description: Método Shell. instart – inicia um serviço nomeado.
ms.assetid: 72214E80-38A2-4a57-B555-942902BAFC3D
title: Método Shell. OnStart (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.ServiceStart
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 9c88b1980d215ad088a4a24362f17147b5d6e432
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083744"
---
# <a name="shellservicestart-method"></a><span data-ttu-id="b3692-103">Método Shell. OnStart</span><span class="sxs-lookup"><span data-stu-id="b3692-103">Shell.ServiceStart method</span></span>

<span data-ttu-id="b3692-104">Inicia um serviço nomeado.</span><span class="sxs-lookup"><span data-stu-id="b3692-104">Starts a named service.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3692-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b3692-105">Syntax</span></span>


```JScript
retVal = Shell.ServiceStart(
  sServiceName,
  vPersistent
)
```


```VB

Shell.ServiceStart( _
  ByVal sServiceName As BSTR, _
  ByVal vPersistent As Variant _
) As Variant
```





## <a name="parameters"></a><span data-ttu-id="b3692-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b3692-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3692-107">*sServiceName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b3692-107">*sServiceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3692-108">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="b3692-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="b3692-109">Uma **cadeia de caracteres** que contém o nome do serviço.</span><span class="sxs-lookup"><span data-stu-id="b3692-109">A **String** that contains the name of the service.</span></span>

</dd> <dt>

<span data-ttu-id="b3692-110">*vPersistent* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b3692-110">*vPersistent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3692-111">Tipo: **variante**</span><span class="sxs-lookup"><span data-stu-id="b3692-111">Type: **Variant**</span></span>

<span data-ttu-id="b3692-112">Defina como **true** para que o serviço seja iniciado automaticamente pelo Gerenciador de controle de serviço durante a inicialização do sistema.</span><span class="sxs-lookup"><span data-stu-id="b3692-112">Set to **true** to have the service started automatically by the service control manager during system startup.</span></span> <span data-ttu-id="b3692-113">Defina como **false** para deixar a configuração de serviço inalterada.</span><span class="sxs-lookup"><span data-stu-id="b3692-113">Set to **false** to leave the service configuration unchanged.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3692-114">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="b3692-114">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="b3692-115">JScript</span><span class="sxs-lookup"><span data-stu-id="b3692-115">JScript</span></span>

<span data-ttu-id="b3692-116">Tipo: **variante \***</span><span class="sxs-lookup"><span data-stu-id="b3692-116">Type: **Variant\***</span></span>

<span data-ttu-id="b3692-117">Retornará **true** se for bem-sucedido; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="b3692-117">Returns **true** if successful; otherwise, **false**.</span></span>

### <a name="vb"></a><span data-ttu-id="b3692-118">VB</span><span class="sxs-lookup"><span data-stu-id="b3692-118">VB</span></span>

<span data-ttu-id="b3692-119">Tipo: **variante \***</span><span class="sxs-lookup"><span data-stu-id="b3692-119">Type: **Variant\***</span></span>

<span data-ttu-id="b3692-120">Retornará **true** se for bem-sucedido; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="b3692-120">Returns **true** if successful; otherwise, **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="b3692-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="b3692-121">Remarks</span></span>

<span data-ttu-id="b3692-122">O método retornará **false** se o serviço já tiver sido iniciado.</span><span class="sxs-lookup"><span data-stu-id="b3692-122">The method returns **false** if the service has already been started.</span></span> <span data-ttu-id="b3692-123">Antes de chamar esse método, você pode chamar [**shell. IsServiceRunning**](./shell-isservicerunning.md) para verificar o status do serviço.</span><span class="sxs-lookup"><span data-stu-id="b3692-123">Before calling this method, you can call [**Shell.IsServiceRunning**](./shell-isservicerunning.md) to ascertain the status of the service.</span></span>

<span data-ttu-id="b3692-124">Este método não está disponível atualmente no Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="b3692-124">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="b3692-125">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b3692-125">Examples</span></span>

<span data-ttu-id="b3692-126">Os exemplos a seguir mostram o uso do **Imstart** para iniciar o serviço mensageiro.</span><span class="sxs-lookup"><span data-stu-id="b3692-126">The following examples show the use of **ServiceStart** to start the Messenger service.</span></span> <span data-ttu-id="b3692-127">O uso é mostrado para JScript e VBScript.</span><span class="sxs-lookup"><span data-stu-id="b3692-127">Usage is shown for JScript and VBScript.</span></span>

<span data-ttu-id="b3692-128">JScript</span><span class="sxs-lookup"><span data-stu-id="b3692-128">JScript:</span></span>


```JScript
<script language="JScript">
    function fnServiceStartJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var bReturn;
        
        bReturn = objShell.ServiceStart("Messenger", true);
    }
```



<span data-ttu-id="b3692-129">VBScript</span><span class="sxs-lookup"><span data-stu-id="b3692-129">VBScript:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="b3692-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b3692-130">Requirements</span></span>



| <span data-ttu-id="b3692-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3692-131">Requirement</span></span> | <span data-ttu-id="b3692-132">Valor</span><span class="sxs-lookup"><span data-stu-id="b3692-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3692-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b3692-133">Minimum supported client</span></span><br/> | <span data-ttu-id="b3692-134">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="b3692-134">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b3692-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b3692-135">Minimum supported server</span></span><br/> | <span data-ttu-id="b3692-136">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b3692-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="b3692-137">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b3692-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="b3692-138"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b3692-138"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="b3692-139">INSERI</span><span class="sxs-lookup"><span data-stu-id="b3692-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b3692-140"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b3692-140"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="b3692-141">DLL</span><span class="sxs-lookup"><span data-stu-id="b3692-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b3692-142"><dt>Shell32.dll (versão 5,0 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="b3692-142"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
