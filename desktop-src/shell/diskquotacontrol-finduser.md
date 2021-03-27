---
description: Localiza a entrada de um usuário, por nome, no arquivo de cota do volume.
title: Método DiskQuotaControl. FindUser
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.FindUser
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: e5767d28-4c0a-49bc-a1d3-ba809411456d
ms.openlocfilehash: af1bc9c0398d37f04e47515a2b85cb4520795b7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967309"
---
# <a name="diskquotacontrolfinduser-method"></a><span data-ttu-id="de3fa-103">Método DiskQuotaControl. FindUser</span><span class="sxs-lookup"><span data-stu-id="de3fa-103">DiskQuotaControl.FindUser method</span></span>

<span data-ttu-id="de3fa-104">Localiza a entrada de um usuário, por nome, no arquivo de cota do volume.</span><span class="sxs-lookup"><span data-stu-id="de3fa-104">Finds a user's entry, by name, in the volume's quota file.</span></span>

## <a name="syntax"></a><span data-ttu-id="de3fa-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="de3fa-105">Syntax</span></span>


```JScript
DiskQuotaControl.FindUser(
  sLogonName
)
```



## <a name="parameters"></a><span data-ttu-id="de3fa-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="de3fa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de3fa-107">*sLogonName*</span><span class="sxs-lookup"><span data-stu-id="de3fa-107">*sLogonName*</span></span> 
</dt> <dd>

<span data-ttu-id="de3fa-108">Tipo: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="de3fa-108">Type: **String**</span></span>

<span data-ttu-id="de3fa-109">Um valor de cadeia de caracteres que contém o nome de logon do usuário.</span><span class="sxs-lookup"><span data-stu-id="de3fa-109">A string value that contains the user's logon name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de3fa-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="de3fa-110">Return value</span></span>

<span data-ttu-id="de3fa-111">Retorna uma expressão de objeto que é avaliada como o objeto [**DIDiskQuotaUser**](didiskquotauser-object.md) do usuário.</span><span class="sxs-lookup"><span data-stu-id="de3fa-111">Returns an object expression that evaluates to the user's [**DIDiskQuotaUser**](didiskquotauser-object.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="de3fa-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="de3fa-112">Remarks</span></span>

<span data-ttu-id="de3fa-113">Esse método retorna um objeto [**DIDiskQuotaUser**](didiskquotauser-object.md) , mesmo se não houver nenhuma entrada para o usuário no arquivo de cota.</span><span class="sxs-lookup"><span data-stu-id="de3fa-113">This method returns a [**DIDiskQuotaUser**](didiskquotauser-object.md) object even if there is no entry for the user in the quota file.</span></span> <span data-ttu-id="de3fa-114">O objeto de usuário retornado tem limite de aviso e limites de cota rígido definidos para os valores padrão do volume.</span><span class="sxs-lookup"><span data-stu-id="de3fa-114">The returned user object has warning threshold and hard quota limits set to the volume's default values.</span></span>

<span data-ttu-id="de3fa-115">A cadeia de caracteres retornada de [**TranslateLogonNameToSID**](diskquotacontrol-translatelogonnametosid.md) pode ser passada no lugar do parâmetro *sLogonName* .</span><span class="sxs-lookup"><span data-stu-id="de3fa-115">The string returned from [**TranslateLogonNameToSID**](diskquotacontrol-translatelogonnametosid.md) may be passed in place of the *sLogonName* parameter.</span></span> <span data-ttu-id="de3fa-116">Quando o **FindUser** recebe uma cadeia de caracteres Sid, ele usa o Sid correspondente para a pesquisa direta do registro de cota do usuário no volume.</span><span class="sxs-lookup"><span data-stu-id="de3fa-116">When **FindUser** receives a SID string it uses the corresponding SID for direct lookup of the user's quota record on the volume.</span></span> <span data-ttu-id="de3fa-117">Isso ignora o cache de nome SID.</span><span class="sxs-lookup"><span data-stu-id="de3fa-117">This bypasses the SID-name cache.</span></span> <span data-ttu-id="de3fa-118">Nos casos em que **FindUser** falha devido a uma incompatibilidade no formato (por exemplo, compatível com Sam e UPN) do nome de logon fornecido e o nome de logon armazenado em cache, o nome de logon pode ser convertido em uma cadeia de caracteres de Sid usando **TranslateLogonNameToSID** , então passado novamente para **FindUser**.</span><span class="sxs-lookup"><span data-stu-id="de3fa-118">In cases where **FindUser** fails due to a mismatch in format (for example, SAM-compatible and UPN) of the logon name provided and the logon name cached, the logon name can be translated to a SID string using **TranslateLogonNameToSID** then passed again to **FindUser**.</span></span> <span data-ttu-id="de3fa-119">O código VBScript a seguir ilustra essa técnica.</span><span class="sxs-lookup"><span data-stu-id="de3fa-119">The following VBScript code illustrates this technique.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="de3fa-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="de3fa-120">Requirements</span></span>



| <span data-ttu-id="de3fa-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="de3fa-121">Requirement</span></span> | <span data-ttu-id="de3fa-122">Valor</span><span class="sxs-lookup"><span data-stu-id="de3fa-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de3fa-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="de3fa-123">Minimum supported client</span></span><br/> | <span data-ttu-id="de3fa-124">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="de3fa-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="de3fa-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="de3fa-125">Minimum supported server</span></span><br/> | <span data-ttu-id="de3fa-126">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="de3fa-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="de3fa-127">DLL</span><span class="sxs-lookup"><span data-stu-id="de3fa-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="de3fa-128"><dt>Shell32.dll (versão 5,0 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="de3fa-128"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de3fa-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="de3fa-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de3fa-130">**Objeto DiskQuotaControl**</span><span class="sxs-lookup"><span data-stu-id="de3fa-130">**DiskQuotaControl Object**</span></span>](diskquotacontrol-object.md)
</dt> </dl>

 

 




