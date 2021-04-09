---
title: Função DsRestorePrepare (Ntdsbcli. h)
description: Conecta-se ao servidor de diretório especificado e o prepara para a operação de restauração.
ms.assetid: e847d57a-32e1-49c0-800c-7ce0e5f442fa
ms.tgt_platform: multiple
keywords:
- Função DsRestorePrepare Active Directory
topic_type:
- apiref
api_name:
- DsRestorePrepare
- DsRestorePrepareA
- DsRestorePrepareW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb040a315b6cc94f2d296b032a954b00473a4ca2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085473"
---
# <a name="dsrestoreprepare-function"></a><span data-ttu-id="949b3-104">Função DsRestorePrepare</span><span class="sxs-lookup"><span data-stu-id="949b3-104">DsRestorePrepare function</span></span>

<span data-ttu-id="949b3-105">\[Essa função está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="949b3-105">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="949b3-106">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="949b3-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="949b3-107">A partir do Windows Vista, use [serviço de cópias de sombra de volume (VSS)](../vss/volume-shadow-copy-service-overview.md) em vez disso.\]</span><span class="sxs-lookup"><span data-stu-id="949b3-107">Beginning with Windows Vista, use [Volume Shadow Copy Service (VSS)](../vss/volume-shadow-copy-service-overview.md) instead.\]</span></span>

<span data-ttu-id="949b3-108">A função **DsRestorePrepare** conecta-se ao servidor de diretório especificado e o prepara para a operação de restauração.</span><span class="sxs-lookup"><span data-stu-id="949b3-108">The **DsRestorePrepare** function connects to the specified directory server and prepares it for the restore operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="949b3-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="949b3-109">Syntax</span></span>


```C++
HRESULT DsRestorePrepare(
  _In_  LPCWSTR szServerName,
  _In_  ULONG   rtFlag,
  _In_  PVOID   pvExpiryToken,
  _In_  DWORD   cbExpiryTokenSize,
  _Out_ HBC     *phbc
);
```



## <a name="parameters"></a><span data-ttu-id="949b3-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="949b3-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="949b3-111">*szServerName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="949b3-111">*szServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="949b3-112">Ponteiro para uma cadeia de caracteres terminada em nulo que contém o nome do servidor a ser restaurado.</span><span class="sxs-lookup"><span data-stu-id="949b3-112">Pointer to a null-terminated string that contains the name of the server to restore.</span></span> <span data-ttu-id="949b3-113">Barras invertidas precedentes são opcionais.</span><span class="sxs-lookup"><span data-stu-id="949b3-113">Preceding backslashes are optional.</span></span> <span data-ttu-id="949b3-114">O servidor deve ser o mesmo computador do qual essa função é chamada.</span><span class="sxs-lookup"><span data-stu-id="949b3-114">The server must be the same computer that this function is called from.</span></span> <span data-ttu-id="949b3-115">O nome do servidor não pode conter nenhum caractere de sublinhado ( \_ ).</span><span class="sxs-lookup"><span data-stu-id="949b3-115">The server name cannot contain any underscore (\_) characters.</span></span> <span data-ttu-id="949b3-116">Um exemplo de um nome de servidor é " \\ \\ Server1".</span><span class="sxs-lookup"><span data-stu-id="949b3-116">An example of a server name is "\\\\server1".</span></span>

</dd> <dt>

<span data-ttu-id="949b3-117">*rtFlag* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="949b3-117">*rtFlag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="949b3-118">Especifica o tipo de restauração a ser executada.</span><span class="sxs-lookup"><span data-stu-id="949b3-118">Specifies the type of restoration to perform.</span></span> <span data-ttu-id="949b3-119">Isso pode ser zero ou um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="949b3-119">This can be zero or one of the following values.</span></span>

<dt>

<span id="RESTORE_TYPE_CATCHUP"></span><span id="restore_type_catchup"></span>

<span data-ttu-id="949b3-120"><span id="RESTORE_TYPE_CATCHUP"></span><span id="restore_type_catchup"></span>**tipo de restauração \_ \_ catchup**</span><span class="sxs-lookup"><span data-stu-id="949b3-120"><span id="RESTORE_TYPE_CATCHUP"></span><span id="restore_type_catchup"></span>**RESTORE\_TYPE\_CATCHUP**</span></span>


</dt> <dd>

<span data-ttu-id="949b3-121">Padrão.</span><span class="sxs-lookup"><span data-stu-id="949b3-121">Default.</span></span> <span data-ttu-id="949b3-122">A versão restaurada é reconciliada por meio da lógica de reconciliação padrão para que a DIT restaurada possa sincronizar com outros computadores de servidor corporativo.</span><span class="sxs-lookup"><span data-stu-id="949b3-122">The restored version is reconciled through the standard reconciliation logic so that the restored DIT can synchronize with other enterprise server computers.</span></span>

</dd> <dt>

<span id="RESTORE_TYPE_AUTHORATATIVE"></span><span id="restore_type_authoratative"></span>

<span data-ttu-id="949b3-123"><span id="RESTORE_TYPE_AUTHORATATIVE"></span><span id="restore_type_authoratative"></span>**tipo de restauração \_ \_ AUTHORATATIVE**</span><span class="sxs-lookup"><span data-stu-id="949b3-123"><span id="RESTORE_TYPE_AUTHORATATIVE"></span><span id="restore_type_authoratative"></span>**RESTORE\_TYPE\_AUTHORATATIVE**</span></span>


</dt> <dd>

<span data-ttu-id="949b3-124">Sem suporte.</span><span class="sxs-lookup"><span data-stu-id="949b3-124">Not Supported.</span></span>

</dd> <dt>

<span id="RESTORE_TYPE_ONLINE"></span><span id="restore_type_online"></span>

<span data-ttu-id="949b3-125"><span id="RESTORE_TYPE_ONLINE"></span><span id="restore_type_online"></span>**RESTAURAR \_ tipo \_ online**</span><span class="sxs-lookup"><span data-stu-id="949b3-125"><span id="RESTORE_TYPE_ONLINE"></span><span id="restore_type_online"></span>**RESTORE\_TYPE\_ONLINE**</span></span>


</dt> <dd>

<span data-ttu-id="949b3-126">Sem suporte.</span><span class="sxs-lookup"><span data-stu-id="949b3-126">Not Supported.</span></span> <span data-ttu-id="949b3-127">A restauração é executada quando o NTDS está online.</span><span class="sxs-lookup"><span data-stu-id="949b3-127">Restoration is performed when NTDS is online.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="949b3-128">*pvExpiryToken* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="949b3-128">*pvExpiryToken* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="949b3-129">Ponteiro para o token de expiração associado ao backup que está sendo restaurado.</span><span class="sxs-lookup"><span data-stu-id="949b3-129">Pointer to the expiry token associated with the backup being restored.</span></span> <span data-ttu-id="949b3-130">Esse token foi obtido da função [**DsBackupPrepare**](dsbackupprepare.md) quando foi feito o backup do diretório.</span><span class="sxs-lookup"><span data-stu-id="949b3-130">This token was obtained from the [**DsBackupPrepare**](dsbackupprepare.md) function when the directory was backed up.</span></span>

<span data-ttu-id="949b3-131">Se esse parâmetro for **NULL**, o identificador retornado em *phbc* só poderá ser usado para obter os diretórios de restauração com a função [**DsRestoreGetDatabaseLocations**](dsrestoregetdatabaselocations.md) .</span><span class="sxs-lookup"><span data-stu-id="949b3-131">If this parameter is **NULL**, the handle returned in *phbc* can only be used to obtain the restoration directories with the [**DsRestoreGetDatabaseLocations**](dsrestoregetdatabaselocations.md) function.</span></span> <span data-ttu-id="949b3-132">O identificador não pode ser usado para nenhuma outra função de restauração.</span><span class="sxs-lookup"><span data-stu-id="949b3-132">The handle cannot be used for any other restoration functions.</span></span>

</dd> <dt>

<span data-ttu-id="949b3-133">*cbExpiryTokenSize* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="949b3-133">*cbExpiryTokenSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="949b3-134">Contém o tamanho, em bytes, do token de expiração em *pvExpiryToken*.</span><span class="sxs-lookup"><span data-stu-id="949b3-134">Contains the size, in bytes, of the expiry token in *pvExpiryToken*.</span></span>

</dd> <dt>

<span data-ttu-id="949b3-135">*phbc* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="949b3-135">*phbc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="949b3-136">Ponteiro para um valor **HBC** que recebe o identificador para a restauração.</span><span class="sxs-lookup"><span data-stu-id="949b3-136">Pointer to an **HBC** value that receives the handle for the restore.</span></span> <span data-ttu-id="949b3-137">Esse identificador é usado ao chamar outras funções de restauração do serviço de diretório, como [**DsBackupOpenFile**](dsbackupopenfile.md) e [**DsRestoreEnd**](dsrestoreend.md).</span><span class="sxs-lookup"><span data-stu-id="949b3-137">This handle is used when calling other Directory Service restore functions, such as [**DsBackupOpenFile**](dsbackupopenfile.md) and [**DsRestoreEnd**](dsrestoreend.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="949b3-138">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="949b3-138">Return value</span></span>

<span data-ttu-id="949b3-139">Se for bem-sucedido, retorna um código **HRESULT** padrão; caso contrário, um código de falha será retornado.</span><span class="sxs-lookup"><span data-stu-id="949b3-139">If successful, returns a standard **HRESULT** codes; otherwise, a failure code is returned.</span></span>

## <a name="remarks"></a><span data-ttu-id="949b3-140">Comentários</span><span class="sxs-lookup"><span data-stu-id="949b3-140">Remarks</span></span>

<span data-ttu-id="949b3-141">A função **DsRestorePrepare** requer que o chamador seja um membro do grupo Administradores no servidor.</span><span class="sxs-lookup"><span data-stu-id="949b3-141">The **DsRestorePrepare** function requires that the caller is a member of the Administrators group on the server.</span></span>

<span data-ttu-id="949b3-142">**DsRestorePrepare** pode ser usado com ou sem um token fornecido.</span><span class="sxs-lookup"><span data-stu-id="949b3-142">**DsRestorePrepare** may be used with or without a token provided.</span></span> <span data-ttu-id="949b3-143">Se o token for fornecido, ele será verificado quanto à expiração e todas as operações serão permitidas no contexto retornado.</span><span class="sxs-lookup"><span data-stu-id="949b3-143">If the token is provided, it is checked for expiration, and all operations are allowed on the context returned.</span></span> <span data-ttu-id="949b3-144">Se o token não for fornecido, o contexto retornado será restrito e poderá ser usado somente para a função [**DsRestoreGetDatabaseLocations**](dsrestoregetdatabaselocations.md) .</span><span class="sxs-lookup"><span data-stu-id="949b3-144">If the token is not provided, the context returned is restricted, and may be used only for the [**DsRestoreGetDatabaseLocations**](dsrestoregetdatabaselocations.md) function.</span></span> <span data-ttu-id="949b3-145">Ele não pode ser usado para a função [**DsRestoreRegister**](dsrestoreregister.md) .</span><span class="sxs-lookup"><span data-stu-id="949b3-145">It may not be used for the [**DsRestoreRegister**](dsrestoreregister.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="949b3-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="949b3-146">Requirements</span></span>



| <span data-ttu-id="949b3-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="949b3-147">Requirement</span></span> | <span data-ttu-id="949b3-148">Valor</span><span class="sxs-lookup"><span data-stu-id="949b3-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="949b3-149">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="949b3-149">Minimum supported client</span></span><br/> | <span data-ttu-id="949b3-150">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="949b3-150">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="949b3-151">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="949b3-151">Minimum supported server</span></span><br/> | <span data-ttu-id="949b3-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="949b3-152">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="949b3-153">parâmetro</span><span class="sxs-lookup"><span data-stu-id="949b3-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="949b3-154"><dt>Ntdsbcli. h</dt></span><span class="sxs-lookup"><span data-stu-id="949b3-154"><dt>Ntdsbcli.h</dt></span></span> </dl>   |
| <span data-ttu-id="949b3-155">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="949b3-155">Library</span></span><br/>                  | <dl> <span data-ttu-id="949b3-156"><dt>Ntdsbcli. lib</dt></span><span class="sxs-lookup"><span data-stu-id="949b3-156"><dt>Ntdsbcli.lib</dt></span></span> </dl> |
| <span data-ttu-id="949b3-157">DLL</span><span class="sxs-lookup"><span data-stu-id="949b3-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="949b3-158"><dt>Ntdsbcli.dll</dt></span><span class="sxs-lookup"><span data-stu-id="949b3-158"><dt>Ntdsbcli.dll</dt></span></span> </dl> |
| <span data-ttu-id="949b3-159">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="949b3-159">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="949b3-160">**DsRestorePrepareW** (Unicode) e **DsRestorePrepareA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="949b3-160">**DsRestorePrepareW** (Unicode) and **DsRestorePrepareA** (ANSI)</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="949b3-161">Confira também</span><span class="sxs-lookup"><span data-stu-id="949b3-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="949b3-162">Restaurando um servidor de Active Directory</span><span class="sxs-lookup"><span data-stu-id="949b3-162">Restoring an Active Directory Server</span></span>](restoring-an-active-directory-server.md)
</dt> <dt>

[<span data-ttu-id="949b3-163">Funções de backup de diretório</span><span class="sxs-lookup"><span data-stu-id="949b3-163">Directory Backup Functions</span></span>](directory-backup-functions.md)
</dt> <dt>

[<span data-ttu-id="949b3-164">**DsRestoreGetDatabaseLocations**</span><span class="sxs-lookup"><span data-stu-id="949b3-164">**DsRestoreGetDatabaseLocations**</span></span>](dsrestoregetdatabaselocations.md)
</dt> <dt>

[<span data-ttu-id="949b3-165">**DsRestoreRegister**</span><span class="sxs-lookup"><span data-stu-id="949b3-165">**DsRestoreRegister**</span></span>](dsrestoreregister.md)
</dt> <dt>

[<span data-ttu-id="949b3-166">**DsRestoreRegisterComplete**</span><span class="sxs-lookup"><span data-stu-id="949b3-166">**DsRestoreRegisterComplete**</span></span>](dsrestoreregistercomplete.md)
</dt> <dt>

[<span data-ttu-id="949b3-167">**DsRestoreEnd**</span><span class="sxs-lookup"><span data-stu-id="949b3-167">**DsRestoreEnd**</span></span>](dsrestoreend.md)
</dt> </dl>

 

