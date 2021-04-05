---
title: Propriedade ConnectionOptions. Password (WSManDisp. h)
description: Define a senha de uma conta local ou de domínio no computador remoto. Essa propriedade determina a senha para autenticação.
ms.assetid: 61ba54b6-7da0-423e-b5b2-c4dd8aacd042
ms.tgt_platform: multiple
keywords:
- Gerenciamento Remoto do Windows de propriedade de senha
- Propriedade Password Gerenciamento Remoto do Windows, objeto ConnectionOptions
- Objeto ConnectionOptions Gerenciamento Remoto do Windows, Propriedade Password
topic_type:
- apiref
api_name:
- ConnectionOptions.Password
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d4d553bf3f2a0a245e358e09a89eb1c00751e58
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085858"
---
# <a name="connectionoptionspassword-property"></a><span data-ttu-id="3c1e4-107">Propriedade ConnectionOptions. Password</span><span class="sxs-lookup"><span data-stu-id="3c1e4-107">ConnectionOptions.Password property</span></span>

<span data-ttu-id="3c1e4-108">Define a senha de uma conta local ou de domínio no computador remoto.</span><span class="sxs-lookup"><span data-stu-id="3c1e4-108">Sets the password of a local or a domain account on the remote computer.</span></span> <span data-ttu-id="3c1e4-109">Essa propriedade determina a senha para autenticação.</span><span class="sxs-lookup"><span data-stu-id="3c1e4-109">This property determines the password for authentication.</span></span> <span data-ttu-id="3c1e4-110">Para obter mais informações, consulte [autenticação para conexões remotas](authentication-for-remote-connections.md).</span><span class="sxs-lookup"><span data-stu-id="3c1e4-110">For more information, see [Authentication for Remote Connections](authentication-for-remote-connections.md).</span></span>

<span data-ttu-id="3c1e4-111">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="3c1e4-111">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c1e4-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="3c1e4-112">Syntax</span></span>


```VB
ConnectionOptions.Password As String
```



## <a name="property-value"></a><span data-ttu-id="3c1e4-113">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="3c1e4-113">Property value</span></span>

<span data-ttu-id="3c1e4-114">Cadeia de caracteres que contém a senha de uma conta local ou de domínio no computador remoto.</span><span class="sxs-lookup"><span data-stu-id="3c1e4-114">String that contains the password of a local or a domain account on the remote computer.</span></span>

<span data-ttu-id="3c1e4-115">Se nenhum valor for fornecido e o sinalizador **WSManFlagCredUsernamePassword** não estiver definido, a senha da conta que está executando o script será usada.</span><span class="sxs-lookup"><span data-stu-id="3c1e4-115">If no value is supplied and the **WSManFlagCredUsernamePassword** flag is not set, the password of the account that is running the script is used.</span></span>

<span data-ttu-id="3c1e4-116">Se nenhum valor for fornecido e o sinalizador **WSManFlagCredUsernamePassword** estiver definido, o script solicitará que o usuário insira a senha (e o nome de usuário, se isso não for fornecido).</span><span class="sxs-lookup"><span data-stu-id="3c1e4-116">If no value is supplied and the **WSManFlagCredUsernamePassword** flag is set, the script prompts the user to enter the password (and the user name, if this is not supplied).</span></span> <span data-ttu-id="3c1e4-117">Se um nome de usuário e senha válidos não forem inseridos, um erro de acesso negado será retornado.</span><span class="sxs-lookup"><span data-stu-id="3c1e4-117">If a valid user name and password are not entered, then an access denied error is returned.</span></span>

## <a name="remarks"></a><span data-ttu-id="3c1e4-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="3c1e4-118">Remarks</span></span>

<span data-ttu-id="3c1e4-119">Lembre-se de que você não pode recuperar a senha.</span><span class="sxs-lookup"><span data-stu-id="3c1e4-119">Be aware that you cannot retrieve the password.</span></span> <span data-ttu-id="3c1e4-120">A senha só pode ser definida com esta propriedade.</span><span class="sxs-lookup"><span data-stu-id="3c1e4-120">The password can only be set with this property.</span></span>

<span data-ttu-id="3c1e4-121">Se você criar um objeto [**ConnectionOptions**](connectionoptions.md) e usar um nome de usuário e senha para se conectar ao gerenciamento remoto do Windows, o sinalizador **WSManFlagCredUserNamePassword** deverá ser definido na chamada para [**WSMan. CreateSession**](wsman-createsession.md).</span><span class="sxs-lookup"><span data-stu-id="3c1e4-121">If you create a [**ConnectionOptions**](connectionoptions.md) object and use a user name and password to connect to Windows Remote Management, then the **WSManFlagCredUserNamePassword** flag should be set on the call to [**WSMan.CreateSession**](wsman-createsession.md).</span></span>

<span data-ttu-id="3c1e4-122">Para obter mais informações sobre como definir senhas, consulte a seção comentários em [**ConnectionOptions**](connectionoptions.md).</span><span class="sxs-lookup"><span data-stu-id="3c1e4-122">For more information about setting passwords, see the Remarks section in [**ConnectionOptions**](connectionoptions.md).</span></span>

## <a name="examples"></a><span data-ttu-id="3c1e4-123">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3c1e4-123">Examples</span></span>

<span data-ttu-id="3c1e4-124">O exemplo de código a seguir cria um objeto [**ConnectionOptions**](connectionoptions.md) e define a **senha**.</span><span class="sxs-lookup"><span data-stu-id="3c1e4-124">The following code example creates a [**ConnectionOptions**](connectionoptions.md) object and sets the **Password**.</span></span>


```VB
' Create a WSMan object. 
Set objWsman = CreateObject( "WSMAN.Automation" )
' Create a ConnectionOptions object
Set objOptions = objWSMan.CreateConnectionOptions
objOptions.Password = "<password>"
```



## <a name="requirements"></a><span data-ttu-id="3c1e4-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3c1e4-125">Requirements</span></span>



| <span data-ttu-id="3c1e4-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="3c1e4-126">Requirement</span></span> | <span data-ttu-id="3c1e4-127">Valor</span><span class="sxs-lookup"><span data-stu-id="3c1e4-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c1e4-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3c1e4-128">Minimum supported client</span></span><br/> | <span data-ttu-id="3c1e4-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3c1e4-129">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="3c1e4-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3c1e4-130">Minimum supported server</span></span><br/> | <span data-ttu-id="3c1e4-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3c1e4-131">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="3c1e4-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3c1e4-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="3c1e4-133"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="3c1e4-133"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="3c1e4-134">INSERI</span><span class="sxs-lookup"><span data-stu-id="3c1e4-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3c1e4-135"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3c1e4-135"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="3c1e4-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3c1e4-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="3c1e4-137"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="3c1e4-137"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="3c1e4-138">DLL</span><span class="sxs-lookup"><span data-stu-id="3c1e4-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3c1e4-139"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3c1e4-139"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="3c1e4-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="3c1e4-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c1e4-141">**ConnectionOptions**</span><span class="sxs-lookup"><span data-stu-id="3c1e4-141">**ConnectionOptions**</span></span>](connectionoptions.md)
</dt> </dl>

 

 





