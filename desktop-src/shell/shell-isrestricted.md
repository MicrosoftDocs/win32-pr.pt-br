---
description: Recupera a configuração de restrição de um grupo do registro.
ms.assetid: C4B3B5C0-7445-483a-885F-5283BD4D4B39
title: Método Shell. IsRestricted (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.IsRestricted
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 2224a3ea4ea26cf39f2e15486de4f96afe5448d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170091"
---
# <a name="shellisrestricted-method"></a><span data-ttu-id="14479-103">Método de Shell. IsRestricted</span><span class="sxs-lookup"><span data-stu-id="14479-103">Shell.IsRestricted method</span></span>

<span data-ttu-id="14479-104">Recupera a configuração de restrição de um grupo do registro.</span><span class="sxs-lookup"><span data-stu-id="14479-104">Retrieves a group's restriction setting from the registry.</span></span>

## <a name="syntax"></a><span data-ttu-id="14479-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="14479-105">Syntax</span></span>


```JScript
iRetVal = Shell.IsRestricted(
  sGroup,
  sRestriction
)
```


```VB

Shell.IsRestricted( _
  ByVal sGroup As BSTR, _
  ByVal sRestriction As BSTR _
) As Integer
```





## <a name="parameters"></a><span data-ttu-id="14479-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="14479-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14479-107">*sGroup* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="14479-107">*sGroup* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14479-108">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="14479-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="14479-109">Uma **cadeia de caracteres** que contém o nome do grupo.</span><span class="sxs-lookup"><span data-stu-id="14479-109">A **String** that contains the group name.</span></span> <span data-ttu-id="14479-110">Esse valor é o nome de uma subchave do registro sob a qual verificar a restrição.</span><span class="sxs-lookup"><span data-stu-id="14479-110">This value is the name of a registry subkey under which to check for the restriction.</span></span>

</dd> <dt>

<span data-ttu-id="14479-111">*sRestriction* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="14479-111">*sRestriction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14479-112">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="14479-112">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="14479-113">Uma **cadeia de caracteres** que contém a restrição cujo valor deve ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="14479-113">A **String** that contains the restriction whose value is to be retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14479-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="14479-114">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="14479-115">JScript</span><span class="sxs-lookup"><span data-stu-id="14479-115">JScript</span></span>

<span data-ttu-id="14479-116">Tipo: \**inteiro \** _</span><span class="sxs-lookup"><span data-stu-id="14479-116">Type: \**Integer\** _</span></span>

<span data-ttu-id="14479-117">O valor da restrição.</span><span class="sxs-lookup"><span data-stu-id="14479-117">The value of the restriction.</span></span> <span data-ttu-id="14479-118">Se a restrição especificada não for encontrada, o valor de retorno será 0.</span><span class="sxs-lookup"><span data-stu-id="14479-118">If the specified restriction is not found, the return value is 0.</span></span>

### <a name="vb"></a><span data-ttu-id="14479-119">VB</span><span class="sxs-lookup"><span data-stu-id="14479-119">VB</span></span>

<span data-ttu-id="14479-120">Tipo: _*inteiro \**_</span><span class="sxs-lookup"><span data-stu-id="14479-120">Type: _*Integer\**_</span></span>

<span data-ttu-id="14479-121">O valor da restrição.</span><span class="sxs-lookup"><span data-stu-id="14479-121">The value of the restriction.</span></span> <span data-ttu-id="14479-122">Se a restrição especificada não for encontrada, o valor de retorno será 0.</span><span class="sxs-lookup"><span data-stu-id="14479-122">If the specified restriction is not found, the return value is 0.</span></span>

## <a name="remarks"></a><span data-ttu-id="14479-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="14479-123">Remarks</span></span>

<span data-ttu-id="14479-124">_ *IsRestricted*\* primeiro procura um nome de subchave que corresponda a *sGroup* sob a chave a seguir.</span><span class="sxs-lookup"><span data-stu-id="14479-124">_ *IsRestricted*\* first looks for a subkey name that matches *sGroup* under the following key.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Policies
```

<span data-ttu-id="14479-125">As restrições são declaradas como valores das subchaves de política individuais.</span><span class="sxs-lookup"><span data-stu-id="14479-125">Restrictions are declared as values of the individual policy subkeys.</span></span> <span data-ttu-id="14479-126">Se a restrição nomeada em *sRestriction* for encontrada na subchave nomeada em *SGroup*, **IsRestricted** retornará o valor atual da restrição.</span><span class="sxs-lookup"><span data-stu-id="14479-126">If the restriction named in *sRestriction* is found in the subkey named in *sGroup*, **IsRestricted** returns the restriction's current value.</span></span> <span data-ttu-id="14479-127">Se a restrição não for encontrada em **HKEY \_ local \_ Machine**, a mesma subchave será verificada em **HKEY \_ Current \_ User**.</span><span class="sxs-lookup"><span data-stu-id="14479-127">If the restriction is not found under **HKEY\_LOCAL\_MACHINE**, the same subkey is checked under **HKEY\_CURRENT\_USER**.</span></span>

<span data-ttu-id="14479-128">Este método não está disponível atualmente no Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="14479-128">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="14479-129">Exemplos</span><span class="sxs-lookup"><span data-stu-id="14479-129">Examples</span></span>

<span data-ttu-id="14479-130">Os exemplos a seguir mostram o uso de **IsRestricted** para recuperar o valor de dados da restrição **undockwithoutlogon** da subchave do **sistema** .</span><span class="sxs-lookup"><span data-stu-id="14479-130">The following examples show the use of **IsRestricted** to retrieve the data value of the **undockwithoutlogon** restriction from the **System** subkey.</span></span> <span data-ttu-id="14479-131">O uso é mostrado para JScript e VBScript.</span><span class="sxs-lookup"><span data-stu-id="14479-131">Usage is shown for JScript and VBScript.</span></span>

<span data-ttu-id="14479-132">JScript</span><span class="sxs-lookup"><span data-stu-id="14479-132">JScript:</span></span>


```JScript
<script language="JScript">
    function fnIsRestricedJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var lReturn;
        
        lReturn = objShell.IsRestricted("system", "undockwithoutlogon");
        document.write(lReturn);
    }
</script>
```



<span data-ttu-id="14479-133">VBScript</span><span class="sxs-lookup"><span data-stu-id="14479-133">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnIsRestricedVB()
        dim objShell
        dim lReturn

        set objShell = CreateObject("shell.application")

        lReturn = objShell.IsRestricted("system", "undockwithoutlogon")
        document.write(lReturn)

        set objShell = nothing
    end function
</script>
```



## <a name="requirements"></a><span data-ttu-id="14479-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="14479-134">Requirements</span></span>



| <span data-ttu-id="14479-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="14479-135">Requirement</span></span> | <span data-ttu-id="14479-136">Valor</span><span class="sxs-lookup"><span data-stu-id="14479-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="14479-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="14479-137">Minimum supported client</span></span><br/> | <span data-ttu-id="14479-138">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="14479-138">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="14479-139">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="14479-139">Minimum supported server</span></span><br/> | <span data-ttu-id="14479-140">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="14479-140">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="14479-141">parâmetro</span><span class="sxs-lookup"><span data-stu-id="14479-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="14479-142"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="14479-142"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="14479-143">INSERI</span><span class="sxs-lookup"><span data-stu-id="14479-143">IDL</span></span><br/>                      | <dl> <span data-ttu-id="14479-144"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="14479-144"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="14479-145">DLL</span><span class="sxs-lookup"><span data-stu-id="14479-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="14479-146"><dt>Shell32.dll (versão 5,0 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="14479-146"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
