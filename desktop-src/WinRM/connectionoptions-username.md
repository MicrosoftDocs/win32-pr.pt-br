---
title: Propriedade ConnectionOptions. UserName (WSManDisp. h)
description: Define e Obtém o nome de usuário de uma conta local ou de domínio no computador remoto. Essa propriedade determina o nome de usuário para autenticação.
ms.assetid: e8f70143-f002-4b39-97a3-006b9713262d
ms.tgt_platform: multiple
keywords:
- Propriedade de nome de usuário Gerenciamento Remoto do Windows
- Propriedade UserName Gerenciamento Remoto do Windows, objeto ConnectionOptions
- Objeto ConnectionOptions Gerenciamento Remoto do Windows, Propriedade UserName
topic_type:
- apiref
api_name:
- ConnectionOptions.UserName
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba4d6c751dbe579372b863566412e740c2a646a5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085857"
---
# <a name="connectionoptionsusername-property"></a><span data-ttu-id="a8f10-107">Propriedade ConnectionOptions. UserName</span><span class="sxs-lookup"><span data-stu-id="a8f10-107">ConnectionOptions.UserName property</span></span>

<span data-ttu-id="a8f10-108">Define e Obtém o nome de usuário de uma conta local ou de domínio no computador remoto.</span><span class="sxs-lookup"><span data-stu-id="a8f10-108">Sets and gets the user name of a local or a domain account on the remote computer.</span></span> <span data-ttu-id="a8f10-109">Essa propriedade determina o nome de usuário para autenticação.</span><span class="sxs-lookup"><span data-stu-id="a8f10-109">This property determines the user name for authentication.</span></span> <span data-ttu-id="a8f10-110">Para obter mais informações, consulte [autenticação para conexões remotas](authentication-for-remote-connections.md).</span><span class="sxs-lookup"><span data-stu-id="a8f10-110">For more information, see [Authentication for Remote Connections](authentication-for-remote-connections.md).</span></span>

<span data-ttu-id="a8f10-111">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="a8f10-111">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8f10-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="a8f10-112">Syntax</span></span>


```VB
ConnectionOptions.UserName As String
```



## <a name="property-value"></a><span data-ttu-id="a8f10-113">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="a8f10-113">Property value</span></span>

<span data-ttu-id="a8f10-114">Cadeia de caracteres que contém o nome de usuário de uma conta local ou de domínio no computador remoto.</span><span class="sxs-lookup"><span data-stu-id="a8f10-114">String that contains the user name of a local or a domain account on the remote computer.</span></span>

<span data-ttu-id="a8f10-115">Se nenhum valor for fornecido e o sinalizador **WSManFlagCredUsernamePassword** não estiver definido, o nome de usuário da conta que está executando o script será usado.</span><span class="sxs-lookup"><span data-stu-id="a8f10-115">If no value is supplied and the **WSManFlagCredUsernamePassword** flag is not set, the user name of the account that is running the script is used.</span></span>

<span data-ttu-id="a8f10-116">Se nenhum valor for fornecido e o sinalizador **WSManFlagCredUsernamePassword** estiver definido, o script solicitará que o usuário insira o nome de usuário e a senha.</span><span class="sxs-lookup"><span data-stu-id="a8f10-116">If no value is supplied and the **WSManFlagCredUsernamePassword** flag is set, the script prompts the user to enter the user name and password.</span></span> <span data-ttu-id="a8f10-117">Se um nome de usuário e senha válidos não forem inseridos, um erro de acesso negado será retornado.</span><span class="sxs-lookup"><span data-stu-id="a8f10-117">If a valid user name and password are not entered, then an access denied error is returned.</span></span>

## <a name="remarks"></a><span data-ttu-id="a8f10-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="a8f10-118">Remarks</span></span>

<span data-ttu-id="a8f10-119">A sintaxe a seguir é usada para especificar essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="a8f10-119">The following syntax is used to specify this property.</span></span>


```VB
Set ConnectionOptions = wsman.CreateConnectionOptions
ConnectionOptions.UserName = "<UserName>"
```



<span data-ttu-id="a8f10-120">Você pode fornecer o **nome de usuário** e a [**senha**](connectionoptions-password.md) para uma conta de domínio ao usar a autenticação [*Negotiate*](windows-remote-management-glossary.md) ou *Kerberos* , ou para uma conta local com autenticação [*básica*](windows-remote-management-glossary.md) .</span><span class="sxs-lookup"><span data-stu-id="a8f10-120">You can supply **UserName** and [**Password**](connectionoptions-password.md) for a domain account when using [*negotiate*](windows-remote-management-glossary.md) or *Kerberos* authentication, or for a local account with [*Basic*](windows-remote-management-glossary.md) authentication.</span></span> <span data-ttu-id="a8f10-121">Para se conectar a uma conta local, os sinalizadores [**WSMan. CreateSession**](wsman-createsession.md) devem conter a combinação do sinalizador **WSManFlagUseBasic** e do sinalizador **WsmanFlagCredUserNamePassword** .</span><span class="sxs-lookup"><span data-stu-id="a8f10-121">To connect to a local account, the [**WSMan.CreateSession**](wsman-createsession.md) flags must contain the combination of the **WSManFlagUseBasic** flag and the **WsmanFlagCredUserNamePassword** flag.</span></span> <span data-ttu-id="a8f10-122">Para se conectar a uma conta de domínio, os sinalizadores **WSMan. CreateSession** devem conter a combinação do sinalizador **WSManFlagUseNegotiate** e do sinalizador **WsmanFlagCredUserNamePassword** , ou a combinação do sinalizador **WSManFlagUseKerberos** e do sinalizador **WsmanFlagCredUserNamePassword** .</span><span class="sxs-lookup"><span data-stu-id="a8f10-122">To connect to a domain account, the **WSMan.CreateSession** flags must contain the combination of the **WSManFlagUseNegotiate** flag and the **WsmanFlagCredUserNamePassword** flag, or the combination of the **WSManFlagUseKerberos** flag and the **WsmanFlagCredUserNamePassword** flag.</span></span> <span data-ttu-id="a8f10-123">Para uma conta de domínio, o **nome de usuário** deve ser especificado no formato "computador \\ nome de usuário", em que a parte "computador" da cadeia de caracteres pode ser o nome ou o endereço IP.</span><span class="sxs-lookup"><span data-stu-id="a8f10-123">For a domain account, **UserName** must be specified in the form "computer\\username", where the "computer" part of the string can be either the name or the IP address.</span></span> <span data-ttu-id="a8f10-124">Para obter mais informações, consulte [autenticação para conexões remotas](authentication-for-remote-connections.md).</span><span class="sxs-lookup"><span data-stu-id="a8f10-124">For more information, see [Authentication for Remote Connections](authentication-for-remote-connections.md).</span></span>


```VB
Set ConnectionOptions = Wsman.CreateConnectionOptions
ConnectionOptions.Username = "MyUserName"
ConnectionOptions.Password = "MyPassword"
Set NewSession = Wsman.CreateSession("127.0.51.1", _
  (WSMan.SessionFlagUseBasic Or _
  WSMan.SessionFlagCredUsernamePassword), ConnectionOptions)
```



<span data-ttu-id="a8f10-125">Para se conectar a uma conta de domínio, os sinalizadores [**WSMan. CreateSession**](wsman-createsession.md) devem conter a combinação do sinalizador **WSManFlagUseNegotiate** e o sinalizador **WsmanFlagCredUserNamePassword** para se conectar a uma conta de domínio, o que exige autenticação de negociação.</span><span class="sxs-lookup"><span data-stu-id="a8f10-125">For connecting to a domain account, the [**WSMan.CreateSession**](wsman-createsession.md) flags must contain the combination of the **WSManFlagUseNegotiate** flag and the **WsmanFlagCredUserNamePassword** flag for connecting to a domain account, which requires Negotiate authentication.</span></span>


```VB
Set ConnectionOptions = Wsman.CreateConnectionOptions
ConnectionOptions.Username = "MyUserName"
ConnectionOptions.Password = "MyPassword"
Set NewSession = Wsman.CreateSession("127.0.51.1", _
  (WSMan.SessionFlagUseNegotiate Or _
  WSMan.SessionFlagCredUsernamePassword), ConnectionOptions)
```



## <a name="requirements"></a><span data-ttu-id="a8f10-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a8f10-126">Requirements</span></span>



| <span data-ttu-id="a8f10-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8f10-127">Requirement</span></span> | <span data-ttu-id="a8f10-128">Valor</span><span class="sxs-lookup"><span data-stu-id="a8f10-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8f10-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a8f10-129">Minimum supported client</span></span><br/> | <span data-ttu-id="a8f10-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a8f10-130">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="a8f10-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a8f10-131">Minimum supported server</span></span><br/> | <span data-ttu-id="a8f10-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a8f10-132">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="a8f10-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a8f10-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="a8f10-134"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="a8f10-134"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="a8f10-135">INSERI</span><span class="sxs-lookup"><span data-stu-id="a8f10-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a8f10-136"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a8f10-136"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="a8f10-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a8f10-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="a8f10-138"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="a8f10-138"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="a8f10-139">DLL</span><span class="sxs-lookup"><span data-stu-id="a8f10-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a8f10-140"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a8f10-140"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a8f10-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="a8f10-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8f10-142">**ConnectionOptions**</span><span class="sxs-lookup"><span data-stu-id="a8f10-142">**ConnectionOptions**</span></span>](connectionoptions.md)
</dt> </dl>

 

 





