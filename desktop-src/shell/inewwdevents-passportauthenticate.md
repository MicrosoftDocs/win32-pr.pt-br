---
description: Permite que as páginas do lado do servidor hospedadas em um assistente verifiquem se o usuário foi autenticado por meio de um conta Microsoft.
ms.assetid: 8b99eb84-c434-489a-b177-1e00f18d2dcc
title: Método NewWDEvents. PassportAuthenticate (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NewWDEvents.PassportAuthenticate
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 48e6cfbcbf525784fe33520702bbd9c05226f353
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103663493"
---
# <a name="newwdeventspassportauthenticate-method"></a><span data-ttu-id="e8d2c-103">Método NewWDEvents. PassportAuthenticate</span><span class="sxs-lookup"><span data-stu-id="e8d2c-103">NewWDEvents.PassportAuthenticate method</span></span>

<span data-ttu-id="e8d2c-104">Permite que as páginas do lado do servidor hospedadas em um assistente verifiquem se o usuário foi autenticado por meio de um conta Microsoft.</span><span class="sxs-lookup"><span data-stu-id="e8d2c-104">Enables server-side pages hosted in a wizard to verify that the user has been authenticated through a Microsoft account.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8d2c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e8d2c-105">Syntax</span></span>


```JScript
bRetVal = NewWDEvents.PassportAuthenticate(
  bstrSignInUrl
)
```



## <a name="parameters"></a><span data-ttu-id="e8d2c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e8d2c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8d2c-107">*bstrSignInUrl* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e8d2c-107">*bstrSignInUrl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8d2c-108">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="e8d2c-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="e8d2c-109">Uma cadeia de caracteres que contém a URL de uma página da Web que redireciona para o log de conta Microsoft na interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="e8d2c-109">A string containing the URL of a webpage that redirects to the Microsoft account log on UI.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8d2c-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e8d2c-110">Return value</span></span>

<span data-ttu-id="e8d2c-111">Tipo: **booliano**</span><span class="sxs-lookup"><span data-stu-id="e8d2c-111">Type: **Boolean**</span></span>

<span data-ttu-id="e8d2c-112">Defina como **true** se a autenticação for realizada com sucesso; caso contrário, **false** .</span><span class="sxs-lookup"><span data-stu-id="e8d2c-112">Set to **true** if authentication succeeds, **false** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="e8d2c-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="e8d2c-113">Remarks</span></span>

<span data-ttu-id="e8d2c-114">Esse método pode ser chamado mesmo se um usuário já estiver conectado a um conta Microsoft.</span><span class="sxs-lookup"><span data-stu-id="e8d2c-114">This method may be called even if a user is already logged on to a Microsoft account.</span></span> <span data-ttu-id="e8d2c-115">Nesse caso, o método retorna **true** sem exibir o log de conta Microsoft na interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="e8d2c-115">In that case, the method returns **true** without displaying the Microsoft account log on UI.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8d2c-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e8d2c-116">Requirements</span></span>



| <span data-ttu-id="e8d2c-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="e8d2c-117">Requirement</span></span> | <span data-ttu-id="e8d2c-118">Valor</span><span class="sxs-lookup"><span data-stu-id="e8d2c-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8d2c-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e8d2c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e8d2c-120">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="e8d2c-120">Windows XP \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="e8d2c-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e8d2c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e8d2c-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e8d2c-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="e8d2c-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e8d2c-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="e8d2c-124"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="e8d2c-124"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="e8d2c-125">INSERI</span><span class="sxs-lookup"><span data-stu-id="e8d2c-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e8d2c-126"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e8d2c-126"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="e8d2c-127">DLL</span><span class="sxs-lookup"><span data-stu-id="e8d2c-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e8d2c-128"><dt>Shell32.dll (versão 6,0 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="e8d2c-128"><dt>Shell32.dll (version 6.0 or later)</dt></span></span> </dl> |



 

 
