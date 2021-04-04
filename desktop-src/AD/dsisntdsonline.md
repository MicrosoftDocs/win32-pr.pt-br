---
title: Função DsIsNTDSOnline (Ntdsbcli. h)
description: Determina se Active Directory Domain Services estão online no servidor especificado.
ms.assetid: 8f46e4d8-6d05-402c-a5b4-291fd2d6609b
ms.tgt_platform: multiple
keywords:
- Função DsIsNTDSOnline Active Directory
topic_type:
- apiref
api_name:
- DsIsNTDSOnline
- DsIsNTDSOnlineA
- DsIsNTDSOnlineW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57f6728f4481eb8820055b48f10cfa0f94c7aaa1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085595"
---
# <a name="dsisntdsonline-function"></a><span data-ttu-id="875ed-104">Função DsIsNTDSOnline</span><span class="sxs-lookup"><span data-stu-id="875ed-104">DsIsNTDSOnline function</span></span>

<span data-ttu-id="875ed-105">\[Essa função está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="875ed-105">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="875ed-106">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="875ed-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="875ed-107">A partir do Windows Vista, use [serviço de cópias de sombra de volume (VSS)](../vss/volume-shadow-copy-service-overview.md) em vez disso.\]</span><span class="sxs-lookup"><span data-stu-id="875ed-107">Beginning with Windows Vista, use [Volume Shadow Copy Service (VSS)](../vss/volume-shadow-copy-service-overview.md) instead.\]</span></span>

<span data-ttu-id="875ed-108">A função **DsIsNTDSOnline** determina se os Active Directory Domain Services estão online no servidor especificado.</span><span class="sxs-lookup"><span data-stu-id="875ed-108">The **DsIsNTDSOnline** function determines if Active Directory Domain Services are online on the specified server.</span></span>

## <a name="syntax"></a><span data-ttu-id="875ed-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="875ed-109">Syntax</span></span>


```C++
HRESULT DsIsNTDSOnline(
  _In_  LPCTSTR szServerName,
  _Out_ BOOL    *pfNTDSOnline
);
```



## <a name="parameters"></a><span data-ttu-id="875ed-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="875ed-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="875ed-111">*szServerName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="875ed-111">*szServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="875ed-112">Ponteiro para uma cadeia de caracteres terminada em nulo que contém o nome do servidor a ser testado.</span><span class="sxs-lookup"><span data-stu-id="875ed-112">Pointer to a null-terminated string that contains the name of the server to test.</span></span> <span data-ttu-id="875ed-113">Barras invertidas precedentes são opcionais.</span><span class="sxs-lookup"><span data-stu-id="875ed-113">Preceding backslashes are optional.</span></span> <span data-ttu-id="875ed-114">O servidor deve ser o mesmo computador do qual essa função é chamada.</span><span class="sxs-lookup"><span data-stu-id="875ed-114">The server must be the same computer that this function is called from.</span></span> <span data-ttu-id="875ed-115">O nome do servidor não pode conter nenhum caractere de sublinhado ( \_ ).</span><span class="sxs-lookup"><span data-stu-id="875ed-115">The server name cannot contain any underscore (\_) characters.</span></span> <span data-ttu-id="875ed-116">Um exemplo de um nome de servidor é " \\ \\ Server1".</span><span class="sxs-lookup"><span data-stu-id="875ed-116">An example of a server name is "\\\\server1".</span></span>

</dd> <dt>

<span data-ttu-id="875ed-117">*pfNTDSOnline* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="875ed-117">*pfNTDSOnline* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="875ed-118">Ponteiro para o valor **bool** que recebe o resultado.</span><span class="sxs-lookup"><span data-stu-id="875ed-118">Pointer to **BOOL** value that receives the result.</span></span> <span data-ttu-id="875ed-119">Receberá **true** se o serviço de diretório estiver online ou **false** se o serviço de diretório estiver offline.</span><span class="sxs-lookup"><span data-stu-id="875ed-119">Receives **TRUE** if the directory service is online or **FALSE** if the directory service is offline.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="875ed-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="875ed-120">Return value</span></span>

<span data-ttu-id="875ed-121">Retornará **S \_ OK** se a função for bem-sucedida ou um código de erro do contrário.</span><span class="sxs-lookup"><span data-stu-id="875ed-121">Returns **S\_OK** if the function is successful or an error code otherwise.</span></span> <span data-ttu-id="875ed-122">A lista a seguir lista os possíveis códigos de erro.</span><span class="sxs-lookup"><span data-stu-id="875ed-122">The following list lists possible error codes.</span></span>

<dl> <dt>

<span data-ttu-id="875ed-123">**ERRO de \_ acesso \_ negado**</span><span class="sxs-lookup"><span data-stu-id="875ed-123">**ERROR\_ACCESS\_DENIED**</span></span>
</dt> <dd>

<span data-ttu-id="875ed-124">O chamador não tem os privilégios de acesso apropriados para chamar essa função.</span><span class="sxs-lookup"><span data-stu-id="875ed-124">The caller does not have the proper access privileges to call this function.</span></span> <span data-ttu-id="875ed-125">A função [**DsSetAuthIdentity**](dssetauthidentity.md) pode ser usada para definir as credenciais a serem usadas para as funções de backup e restauração.</span><span class="sxs-lookup"><span data-stu-id="875ed-125">The [**DsSetAuthIdentity**](dssetauthidentity.md) function can be used to set the credentials to use for the backup and restore functions.</span></span>

</dd> <dt>

<span data-ttu-id="875ed-126">**hrCouldNotConnect**</span><span class="sxs-lookup"><span data-stu-id="875ed-126">**hrCouldNotConnect**</span></span>
</dt> <dd>

<span data-ttu-id="875ed-127">O servidor em *szServerName* não pode ser encontrado, não é um controlador de domínio ou *szServerName* não está formatado corretamente.</span><span class="sxs-lookup"><span data-stu-id="875ed-127">The server in *szServerName* cannot be found, is not a domain controller, or *szServerName* is not formatted correctly.</span></span> <span data-ttu-id="875ed-128">Esse valor é definido em Ntdsbmsg. h.</span><span class="sxs-lookup"><span data-stu-id="875ed-128">This value is defined in Ntdsbmsg.h.</span></span>

</dd> <dt>

<span data-ttu-id="875ed-129">**Associação de RPC \_ S \_ inválida \_**</span><span class="sxs-lookup"><span data-stu-id="875ed-129">**RPC\_S\_INVALID\_BINDING**</span></span>
</dt> <dd>

<span data-ttu-id="875ed-130">A função [**DsIsNTDSOnline**](dsisntdsonline.md) está sendo chamada remotamente ou o servidor em *szServerName* não é um controlador de domínio.</span><span class="sxs-lookup"><span data-stu-id="875ed-130">The [**DsIsNTDSOnline**](dsisntdsonline.md) function is being called remotely or the server in *szServerName* is not a domain controller.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="875ed-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="875ed-131">Remarks</span></span>

<span data-ttu-id="875ed-132">Chame essa função antes de chamar qualquer uma das funções de backup ou restauração do diretório.</span><span class="sxs-lookup"><span data-stu-id="875ed-132">Call this function before calling any of the directory backup or restore functions.</span></span> <span data-ttu-id="875ed-133">O diretório deve estar online para executar um backup.</span><span class="sxs-lookup"><span data-stu-id="875ed-133">The directory must be online in order to perform a backup.</span></span> <span data-ttu-id="875ed-134">O diretório deve estar offline para executar uma restauração.</span><span class="sxs-lookup"><span data-stu-id="875ed-134">The directory must by offline to perform a restore.</span></span>

<span data-ttu-id="875ed-135">Essa função só pode ser chamada de um controlador de domínio que também seja o servidor de destino especificado em *szServerName*.</span><span class="sxs-lookup"><span data-stu-id="875ed-135">This function can only be called from a domain controller that is also the target server specified in *szServerName*.</span></span> <span data-ttu-id="875ed-136">Esta função não pode ser chamada remotamente.</span><span class="sxs-lookup"><span data-stu-id="875ed-136">This function cannot be called remotely.</span></span>

## <a name="requirements"></a><span data-ttu-id="875ed-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="875ed-137">Requirements</span></span>



| <span data-ttu-id="875ed-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="875ed-138">Requirement</span></span> | <span data-ttu-id="875ed-139">Valor</span><span class="sxs-lookup"><span data-stu-id="875ed-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="875ed-140">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="875ed-140">Minimum supported client</span></span><br/> | <span data-ttu-id="875ed-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="875ed-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="875ed-142">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="875ed-142">Minimum supported server</span></span><br/> | <span data-ttu-id="875ed-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="875ed-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="875ed-144">parâmetro</span><span class="sxs-lookup"><span data-stu-id="875ed-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="875ed-145"><dt>Ntdsbcli. h</dt></span><span class="sxs-lookup"><span data-stu-id="875ed-145"><dt>Ntdsbcli.h</dt></span></span> </dl>   |
| <span data-ttu-id="875ed-146">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="875ed-146">Library</span></span><br/>                  | <dl> <span data-ttu-id="875ed-147"><dt>Ntdsbcli. lib</dt></span><span class="sxs-lookup"><span data-stu-id="875ed-147"><dt>Ntdsbcli.lib</dt></span></span> </dl> |
| <span data-ttu-id="875ed-148">DLL</span><span class="sxs-lookup"><span data-stu-id="875ed-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="875ed-149"><dt>Ntdsbcli.dll</dt></span><span class="sxs-lookup"><span data-stu-id="875ed-149"><dt>Ntdsbcli.dll</dt></span></span> </dl> |
| <span data-ttu-id="875ed-150">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="875ed-150">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="875ed-151">**DsIsNTDSOnlineW** (Unicode) e **DsIsNTDSOnlineA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="875ed-151">**DsIsNTDSOnlineW** (Unicode) and **DsIsNTDSOnlineA** (ANSI)</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="875ed-152">Confira também</span><span class="sxs-lookup"><span data-stu-id="875ed-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="875ed-153">**DsSetAuthIdentity**</span><span class="sxs-lookup"><span data-stu-id="875ed-153">**DsSetAuthIdentity**</span></span>](dssetauthidentity.md)
</dt> <dt>

[<span data-ttu-id="875ed-154">Funções de backup de diretório</span><span class="sxs-lookup"><span data-stu-id="875ed-154">Directory Backup Functions</span></span>](directory-backup-functions.md)
</dt> <dt>

[<span data-ttu-id="875ed-155">Fazendo backup e restaurando um servidor de Active Directory</span><span class="sxs-lookup"><span data-stu-id="875ed-155">Backing Up and Restoring an Active Directory Server</span></span>](backing-up-and-restoring-an-active-directory-server.md)
</dt> </dl>

 

