---
title: Função DsRestoreRegisterComplete (Ntdsbcli. h)
description: Chamado para desbloquear um servidor de Active Directory após a conclusão de uma operação de restauração.
ms.assetid: 781cd2ec-d2e2-4f3a-903d-feda4b871de5
ms.tgt_platform: multiple
keywords:
- Função DsRestoreRegisterComplete Active Directory
topic_type:
- apiref
api_name:
- DsRestoreRegisterComplete
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff5e5e01b29281860dff59fbcd08a3b48ec66c4a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009486"
---
# <a name="dsrestoreregistercomplete-function"></a><span data-ttu-id="dbed2-104">Função DsRestoreRegisterComplete</span><span class="sxs-lookup"><span data-stu-id="dbed2-104">DsRestoreRegisterComplete function</span></span>

<span data-ttu-id="dbed2-105">\[Essa função está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="dbed2-105">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="dbed2-106">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="dbed2-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="dbed2-107">Em vez disso, use o [serviço de cópias de sombra de volume (VSS)](../vss/volume-shadow-copy-service-overview.md) .\]</span><span class="sxs-lookup"><span data-stu-id="dbed2-107">Use [Volume Shadow Copy Service (VSS)](../vss/volume-shadow-copy-service-overview.md) instead.\]</span></span>

<span data-ttu-id="dbed2-108">A função **DsRestoreRegisterComplete** é chamada para desbloquear um servidor de Active Directory após a conclusão de uma operação de restauração.</span><span class="sxs-lookup"><span data-stu-id="dbed2-108">The **DsRestoreRegisterComplete** function is called to unlock an Active Directory server after a restore operation is complete.</span></span> <span data-ttu-id="dbed2-109">Essa função é equivalente à função [**DsRestoreRegister**](dsrestoreregister.md) .</span><span class="sxs-lookup"><span data-stu-id="dbed2-109">This function is counterpart to the [**DsRestoreRegister**](dsrestoreregister.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="dbed2-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dbed2-110">Syntax</span></span>


```C++
HRESULT DsRestoreRegisterComplete(
  _In_ HBC     hbc,
  _In_ HRESULT hrRestoreState
);
```



## <a name="parameters"></a><span data-ttu-id="dbed2-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dbed2-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dbed2-112">*HBC* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="dbed2-112">*hbc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dbed2-113">Contém o identificador de contexto de restauração obtido com a função [**DsRestorePrepare**](dsrestoreprepare.md) .</span><span class="sxs-lookup"><span data-stu-id="dbed2-113">Contains the restoration context handle obtained with the [**DsRestorePrepare**](dsrestoreprepare.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="dbed2-114">*hrRestoreState* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="dbed2-114">*hrRestoreState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dbed2-115">Contém o status final da operação de restauração.</span><span class="sxs-lookup"><span data-stu-id="dbed2-115">Contains the final status of the restore operation.</span></span> <span data-ttu-id="dbed2-116">Esse parâmetro deve conter **S \_ OK** se a operação de restauração tiver sido bem-sucedida ou um código de erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="dbed2-116">This parameter should contain **S\_OK** if the restore operation was successful or an error code otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dbed2-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="dbed2-117">Return value</span></span>

<span data-ttu-id="dbed2-118">Retornará **S \_ OK** se a função for bem-sucedida, ou um código de erro Win32 ou RPC.</span><span class="sxs-lookup"><span data-stu-id="dbed2-118">Returns **S\_OK** if the function is successful or a Win32 or RPC error code otherwise.</span></span> <span data-ttu-id="dbed2-119">A lista a seguir lista os possíveis códigos de erro.</span><span class="sxs-lookup"><span data-stu-id="dbed2-119">The following list lists possible error codes.</span></span>

<dl> <dt>

<span data-ttu-id="dbed2-120">**ERRO de \_ acesso \_ negado**</span><span class="sxs-lookup"><span data-stu-id="dbed2-120">**ERROR\_ACCESS\_DENIED**</span></span>
</dt> <dd>

<span data-ttu-id="dbed2-121">O chamador não tem os privilégios de acesso apropriados para chamar essa função.</span><span class="sxs-lookup"><span data-stu-id="dbed2-121">The caller does not have the proper access privileges to call this function.</span></span> <span data-ttu-id="dbed2-122">A função [**DsSetAuthIdentity**](dssetauthidentity.md) pode ser usada para definir as credenciais a serem usadas para as funções de backup e restauração.</span><span class="sxs-lookup"><span data-stu-id="dbed2-122">The [**DsSetAuthIdentity**](dssetauthidentity.md) function can be used to set the credentials to use for the backup and restore functions.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dbed2-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="dbed2-123">Remarks</span></span>

<span data-ttu-id="dbed2-124">Antes de reiniciar o controlador de domínio, chame essa função para fornecer o status da operação de restauração.</span><span class="sxs-lookup"><span data-stu-id="dbed2-124">Before you restart the domain controller, call this function to provide the status of the restore operation.</span></span> <span data-ttu-id="dbed2-125">Se o status não for bem-sucedido, o serviço de diretório não será iniciado até que um banco de dados válido tenha sido restaurado.</span><span class="sxs-lookup"><span data-stu-id="dbed2-125">If the status is not successful, the directory service will not start until a valid database has been restored.</span></span> <span data-ttu-id="dbed2-126">Essa função conclui a operação de restauração e permite que Active Directory Domain Services iniciem.</span><span class="sxs-lookup"><span data-stu-id="dbed2-126">This function completes the restore operation and allows Active Directory Domain Services to start.</span></span>

## <a name="requirements"></a><span data-ttu-id="dbed2-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dbed2-127">Requirements</span></span>



| <span data-ttu-id="dbed2-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="dbed2-128">Requirement</span></span> | <span data-ttu-id="dbed2-129">Valor</span><span class="sxs-lookup"><span data-stu-id="dbed2-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dbed2-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dbed2-130">Minimum supported client</span></span><br/> | <span data-ttu-id="dbed2-131">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="dbed2-131">None supported</span></span><br/>                                                               |
| <span data-ttu-id="dbed2-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dbed2-132">Minimum supported server</span></span><br/> | <span data-ttu-id="dbed2-133">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="dbed2-133">None supported</span></span><br/>                                                               |
| <span data-ttu-id="dbed2-134">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="dbed2-134">End of client support</span></span><br/>    | <span data-ttu-id="dbed2-135">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="dbed2-135">None supported</span></span><br/>                                                               |
| <span data-ttu-id="dbed2-136">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="dbed2-136">End of server support</span></span><br/>    | <span data-ttu-id="dbed2-137">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="dbed2-137">None supported</span></span><br/>                                                               |
| <span data-ttu-id="dbed2-138">parâmetro</span><span class="sxs-lookup"><span data-stu-id="dbed2-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="dbed2-139"><dt>Ntdsbcli. h</dt></span><span class="sxs-lookup"><span data-stu-id="dbed2-139"><dt>Ntdsbcli.h</dt></span></span> </dl>   |
| <span data-ttu-id="dbed2-140">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="dbed2-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="dbed2-141"><dt>Ntdsbcli. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dbed2-141"><dt>Ntdsbcli.lib</dt></span></span> </dl> |
| <span data-ttu-id="dbed2-142">DLL</span><span class="sxs-lookup"><span data-stu-id="dbed2-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dbed2-143"><dt>Ntdsbcli.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dbed2-143"><dt>Ntdsbcli.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dbed2-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="dbed2-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbed2-145">**DsRestoreRegister**</span><span class="sxs-lookup"><span data-stu-id="dbed2-145">**DsRestoreRegister**</span></span>](dsrestoreregister.md)
</dt> <dt>

[<span data-ttu-id="dbed2-146">**DsRestorePrepare**</span><span class="sxs-lookup"><span data-stu-id="dbed2-146">**DsRestorePrepare**</span></span>](dsrestoreprepare.md)
</dt> <dt>

[<span data-ttu-id="dbed2-147">**DsSetAuthIdentity**</span><span class="sxs-lookup"><span data-stu-id="dbed2-147">**DsSetAuthIdentity**</span></span>](dssetauthidentity.md)
</dt> <dt>

[<span data-ttu-id="dbed2-148">Restaurando um servidor de Active Directory</span><span class="sxs-lookup"><span data-stu-id="dbed2-148">Restoring an Active Directory Server</span></span>](restoring-an-active-directory-server.md)
</dt> <dt>

[<span data-ttu-id="dbed2-149">Funções de backup de diretório</span><span class="sxs-lookup"><span data-stu-id="dbed2-149">Directory Backup Functions</span></span>](directory-backup-functions.md)
</dt> </dl>

 

