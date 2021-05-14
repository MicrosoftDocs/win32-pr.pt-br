---
description: Traduz um nome de logon para a ID de segurança de usuário correspondente no formato de cadeia de caracteres.
title: Método DiskQuotaControl. TranslateLogonNameToSID
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.TranslateLogonNameToSID
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 3b6b0d03-e9ef-4575-bb67-f7b7b39d2a16
ms.openlocfilehash: 5f0a2591b0f5df6bc0f50994fcbf101b7bfbb36d
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841557"
---
# <a name="diskquotacontroltranslatelogonnametosid-method"></a><span data-ttu-id="b94bd-103">Método DiskQuotaControl. TranslateLogonNameToSID</span><span class="sxs-lookup"><span data-stu-id="b94bd-103">DiskQuotaControl.TranslateLogonNameToSID method</span></span>

<span data-ttu-id="b94bd-104">Traduz um nome de logon para a ID de segurança de usuário correspondente no formato de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="b94bd-104">Translates a logon name to the corresponding user security ID in string format.</span></span>

## <a name="syntax"></a><span data-ttu-id="b94bd-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b94bd-105">Syntax</span></span>


```JScript
DiskQuotaControl.TranslateLogonNameToSID(
  logonname
)
```



## <a name="parameters"></a><span data-ttu-id="b94bd-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b94bd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b94bd-107">*LogonName*</span><span class="sxs-lookup"><span data-stu-id="b94bd-107">*logonname*</span></span> 
</dt> <dd>

<span data-ttu-id="b94bd-108">Tipo: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b94bd-108">Type: **String**</span></span>

<span data-ttu-id="b94bd-109">Um valor de cadeia de caracteres que especifica o nome de logon do usuário.</span><span class="sxs-lookup"><span data-stu-id="b94bd-109">A string value that specifies the user's logon name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b94bd-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b94bd-110">Return value</span></span>

<span data-ttu-id="b94bd-111">Retorna a ID de segurança do usuário (SID) no formato de cadeia de caracteres correspondente ao nome de logon fornecido.</span><span class="sxs-lookup"><span data-stu-id="b94bd-111">Returns the user security ID (SID) in string format corresponding to the provided logon name.</span></span> <span data-ttu-id="b94bd-112">A cadeia de caracteres retornada inclui as chaves de circunscrição padrão.</span><span class="sxs-lookup"><span data-stu-id="b94bd-112">The returned string includes the standard enclosing braces.</span></span> <span data-ttu-id="b94bd-113">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="b94bd-113">For example:</span></span>

<span data-ttu-id="b94bd-114">"{S-1-5-21-2127521184-1604012920-1887927527-19009}"</span><span class="sxs-lookup"><span data-stu-id="b94bd-114">"{S-1-5-21-2127521184-1604012920-1887927527-19009}"</span></span>

## <a name="remarks"></a><span data-ttu-id="b94bd-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="b94bd-115">Remarks</span></span>

<span data-ttu-id="b94bd-116">A cadeia de caracteres SID retornada pode ser passada para o método [**FindUser**](diskquotacontrol-finduser.md) no lugar de um nome de logon.</span><span class="sxs-lookup"><span data-stu-id="b94bd-116">The returned SID string can be passed to the [**FindUser**](diskquotacontrol-finduser.md) method in place of a logon name.</span></span>

<span data-ttu-id="b94bd-117">Quando uma chamada para o método [**FindUser**](diskquotacontrol-finduser.md)( *LogonName*) falhar, isso pode ser devido a uma incompatibilidade entre o formulário (por exemplo, o Sam do Gerenciador de contas de segurança \[ \] e \[ o UPN do nome principal do usuário \] ) do nome de logon fornecido e o formulário armazenado no cache de nome de Sid.</span><span class="sxs-lookup"><span data-stu-id="b94bd-117">When a call to the [**FindUser**](diskquotacontrol-finduser.md)( *logonname*) method fails, it could be due to a mismatch between the form (for example, Security Account Manager \[SAM\] compatible and User Principal Name \[UPN\]) of the logon name provided and the form stored in the SID-name cache.</span></span> <span data-ttu-id="b94bd-118">Nesses casos, o nome de logon pode ser convertido em um SID e a chamada para **FindUser** repetida.</span><span class="sxs-lookup"><span data-stu-id="b94bd-118">In such cases, the logon name can be converted to a SID and the call to **FindUser** repeated.</span></span> <span data-ttu-id="b94bd-119">**FindUser** reconhece uma cadeia de caracteres Sid e irá ignorar a pesquisa de cache de nome Sid.</span><span class="sxs-lookup"><span data-stu-id="b94bd-119">**FindUser** recognizes a SID string and will bypass the SID-name cache lookup.</span></span> <span data-ttu-id="b94bd-120">O código do Microsoft Visual Basic Scripting Edition (VBScript) a seguir ilustra essa técnica.</span><span class="sxs-lookup"><span data-stu-id="b94bd-120">The following Microsoft Visual Basic Scripting Edition (VBScript) code illustrates this technique.</span></span>


```
Function Find(dqc, name)
    On Error Resume Next
    SET Find = dqc.FindUser(name)

    If Err.Number <> 0 Then
        Err.Clear
        SET Find = dqc.FindUser(dqc.TranslateLogonNameToSID(name))
    End If    

End Function
```



<span data-ttu-id="b94bd-121">A conversão de nome para SID pode ser um processo lento quando comparada a pesquisas no cache de nome de SID.</span><span class="sxs-lookup"><span data-stu-id="b94bd-121">Name-to-SID translation can be a slow process when compared to lookups in the SID-name cache.</span></span> <span data-ttu-id="b94bd-122">Portanto, é recomendável que [**FindUser**](diskquotacontrol-finduser.md) primeiro seja chamado com um nome de logon.</span><span class="sxs-lookup"><span data-stu-id="b94bd-122">Therefore, it is recommended that [**FindUser**](diskquotacontrol-finduser.md) first be called with a logon name.</span></span> <span data-ttu-id="b94bd-123">O exemplo acima usa essa técnica.</span><span class="sxs-lookup"><span data-stu-id="b94bd-123">The example above uses this technique.</span></span>

## <a name="requirements"></a><span data-ttu-id="b94bd-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b94bd-124">Requirements</span></span>



| <span data-ttu-id="b94bd-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="b94bd-125">Requirement</span></span> | <span data-ttu-id="b94bd-126">Valor</span><span class="sxs-lookup"><span data-stu-id="b94bd-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b94bd-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b94bd-127">Minimum supported client</span></span><br/> | <span data-ttu-id="b94bd-128">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="b94bd-128">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b94bd-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b94bd-129">Minimum supported server</span></span><br/> | <span data-ttu-id="b94bd-130">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b94bd-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="b94bd-131">DLL</span><span class="sxs-lookup"><span data-stu-id="b94bd-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b94bd-132"><dt>Shell32.dll (versão 5.0 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="b94bd-132"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b94bd-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="b94bd-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b94bd-134">**Objeto DiskQuotaControl**</span><span class="sxs-lookup"><span data-stu-id="b94bd-134">**DiskQuotaControl Object**</span></span>](diskquotacontrol-object.md)
</dt> </dl>

 

 




