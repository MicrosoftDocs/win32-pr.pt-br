---
description: Método IShellDispatch2. IsRestricted-recupera a configuração de restrição de um grupo do registro.
ms.assetid: 04275c5f-c3ed-4962-882f-2cce0258a9f4
title: Método IShellDispatch2. IsRestricted (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch2.IsRestricted
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: b4f482407fadd16d7ecfe9deeafd91b032a9a24f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117094"
---
# <a name="ishelldispatch2isrestricted-method"></a><span data-ttu-id="35ada-103">Método IShellDispatch2. IsRestricted</span><span class="sxs-lookup"><span data-stu-id="35ada-103">IShellDispatch2.IsRestricted method</span></span>

<span data-ttu-id="35ada-104">Recupera a configuração de restrição de um grupo do registro.</span><span class="sxs-lookup"><span data-stu-id="35ada-104">Retrieves a group's restriction setting from the registry.</span></span>

## <a name="syntax"></a><span data-ttu-id="35ada-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="35ada-105">Syntax</span></span>


```JScript
iRetVal = IShellDispatch2.IsRestricted(
  sGroup,
  sRestriction
)
```


```VB

IShellDispatch2.IsRestricted( _
  ByVal sGroup As BSTR, _
  ByVal sRestriction As BSTR _
) As Integer
```





## <a name="parameters"></a><span data-ttu-id="35ada-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="35ada-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35ada-107">*sGroup* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="35ada-107">*sGroup* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35ada-108">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="35ada-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="35ada-109">Uma **cadeia de caracteres** que contém o nome do grupo.</span><span class="sxs-lookup"><span data-stu-id="35ada-109">A **String** that contains the group name.</span></span> <span data-ttu-id="35ada-110">Esse valor é o nome de uma subchave do registro sob a qual verificar a restrição.</span><span class="sxs-lookup"><span data-stu-id="35ada-110">This value is the name of a registry subkey under which to check for the restriction.</span></span>

</dd> <dt>

<span data-ttu-id="35ada-111">*sRestriction* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="35ada-111">*sRestriction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35ada-112">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="35ada-112">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="35ada-113">Uma **cadeia de caracteres** que contém a restrição cujo valor deve ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="35ada-113">A **String** that contains the restriction whose value is to be retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35ada-114">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="35ada-114">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="35ada-115">JScript</span><span class="sxs-lookup"><span data-stu-id="35ada-115">JScript</span></span>

<span data-ttu-id="35ada-116">Tipo: **inteiro \***</span><span class="sxs-lookup"><span data-stu-id="35ada-116">Type: **Integer\***</span></span>

<span data-ttu-id="35ada-117">O valor da restrição.</span><span class="sxs-lookup"><span data-stu-id="35ada-117">The value of the restriction.</span></span> <span data-ttu-id="35ada-118">Se a restrição especificada não for encontrada, o valor de retorno será 0.</span><span class="sxs-lookup"><span data-stu-id="35ada-118">If the specified restriction is not found, the return value is 0.</span></span>

### <a name="vb"></a><span data-ttu-id="35ada-119">VB</span><span class="sxs-lookup"><span data-stu-id="35ada-119">VB</span></span>

<span data-ttu-id="35ada-120">Tipo: **inteiro \***</span><span class="sxs-lookup"><span data-stu-id="35ada-120">Type: **Integer\***</span></span>

<span data-ttu-id="35ada-121">O valor da restrição.</span><span class="sxs-lookup"><span data-stu-id="35ada-121">The value of the restriction.</span></span> <span data-ttu-id="35ada-122">Se a restrição especificada não for encontrada, o valor de retorno será 0.</span><span class="sxs-lookup"><span data-stu-id="35ada-122">If the specified restriction is not found, the return value is 0.</span></span>

## <a name="remarks"></a><span data-ttu-id="35ada-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="35ada-123">Remarks</span></span>

<span data-ttu-id="35ada-124">Esse método é implementado e acessado por meio do método [**shell. IsRestricted**](./shell-isrestricted.md) .</span><span class="sxs-lookup"><span data-stu-id="35ada-124">This method is implemented and accessed through the [**Shell.IsRestricted**](./shell-isrestricted.md) method.</span></span>

<span data-ttu-id="35ada-125">**IsRestricted** primeiro procura por um nome de subchave que corresponda a *sGroup* sob a chave a seguir.</span><span class="sxs-lookup"><span data-stu-id="35ada-125">**IsRestricted** first looks for a subkey name that matches *sGroup* under the following key.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Policies
```

<span data-ttu-id="35ada-126">As restrições são declaradas como valores das subchaves de política individuais.</span><span class="sxs-lookup"><span data-stu-id="35ada-126">Restrictions are declared as values of the individual policy subkeys.</span></span> <span data-ttu-id="35ada-127">Se a restrição nomeada em *sRestriction* for encontrada na subchave nomeada em *SGroup*, **IsRestricted** retornará o valor atual da restrição.</span><span class="sxs-lookup"><span data-stu-id="35ada-127">If the restriction named in *sRestriction* is found in the subkey named in *sGroup*, **IsRestricted** returns the restriction's current value.</span></span> <span data-ttu-id="35ada-128">Se a restrição não for encontrada em **HKEY \_ local \_ Machine**, a mesma subchave será verificada em **HKEY \_ Current \_ User**.</span><span class="sxs-lookup"><span data-stu-id="35ada-128">If the restriction is not found under **HKEY\_LOCAL\_MACHINE**, the same subkey is checked under **HKEY\_CURRENT\_USER**.</span></span>

<span data-ttu-id="35ada-129">Este método não está disponível atualmente no Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="35ada-129">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="35ada-130">Exemplos</span><span class="sxs-lookup"><span data-stu-id="35ada-130">Examples</span></span>

<span data-ttu-id="35ada-131">Os exemplos a seguir mostram o uso de **IsRestricted** para recuperar o valor de dados da restrição **undockwithoutlogon** da subchave do **sistema** .</span><span class="sxs-lookup"><span data-stu-id="35ada-131">The following examples show the use of **IsRestricted** to retrieve the data value of the **undockwithoutlogon** restriction from the **System** subkey.</span></span> <span data-ttu-id="35ada-132">O uso é mostrado para JScript e VBScript.</span><span class="sxs-lookup"><span data-stu-id="35ada-132">Usage is shown for JScript and VBScript.</span></span>

<span data-ttu-id="35ada-133">JScript</span><span class="sxs-lookup"><span data-stu-id="35ada-133">JScript:</span></span>


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



<span data-ttu-id="35ada-134">VBScript</span><span class="sxs-lookup"><span data-stu-id="35ada-134">VBScript:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="35ada-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="35ada-135">Requirements</span></span>



| <span data-ttu-id="35ada-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="35ada-136">Requirement</span></span> | <span data-ttu-id="35ada-137">Valor</span><span class="sxs-lookup"><span data-stu-id="35ada-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35ada-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="35ada-138">Minimum supported client</span></span><br/> | <span data-ttu-id="35ada-139">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="35ada-139">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="35ada-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="35ada-140">Minimum supported server</span></span><br/> | <span data-ttu-id="35ada-141">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="35ada-141">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="35ada-142">parâmetro</span><span class="sxs-lookup"><span data-stu-id="35ada-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="35ada-143"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="35ada-143"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="35ada-144">INSERI</span><span class="sxs-lookup"><span data-stu-id="35ada-144">IDL</span></span><br/>                      | <dl> <span data-ttu-id="35ada-145"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="35ada-145"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="35ada-146">DLL</span><span class="sxs-lookup"><span data-stu-id="35ada-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="35ada-147"><dt>Shell32.dll (versão 5,0 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="35ada-147"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
