---
title: Função DsSetAuthIdentity (Ntdsbcli. h)
description: Define o contexto de segurança no qual as APIs de backup do diretório são chamadas.
ms.assetid: bfa2f847-6fe3-4f9b-bafa-acf6a7c861d9
ms.tgt_platform: multiple
keywords:
- Função DsSetAuthIdentity Active Directory
topic_type:
- apiref
api_name:
- DsSetAuthIdentity
- DsSetAuthIdentityA
- DsSetAuthIdentityW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40d973d5f818b4bd81278a1466487ae89ebf888f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455355"
---
# <a name="dssetauthidentity-function"></a><span data-ttu-id="39953-104">Função DsSetAuthIdentity</span><span class="sxs-lookup"><span data-stu-id="39953-104">DsSetAuthIdentity function</span></span>

<span data-ttu-id="39953-105">\[Essa função está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="39953-105">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="39953-106">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="39953-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="39953-107">A partir do Windows Vista, use [serviço de cópias de sombra de volume (VSS)](../vss/volume-shadow-copy-service-overview.md) em vez disso.\]</span><span class="sxs-lookup"><span data-stu-id="39953-107">Beginning with Windows Vista, use [Volume Shadow Copy Service (VSS)](../vss/volume-shadow-copy-service-overview.md) instead.\]</span></span>

<span data-ttu-id="39953-108">A função **DsSetAuthIdentity** define o contexto de segurança sob o qual as APIs de backup do diretório são chamadas.</span><span class="sxs-lookup"><span data-stu-id="39953-108">The **DsSetAuthIdentity** function sets the security context under which the directory backup APIs are called.</span></span>

## <a name="syntax"></a><span data-ttu-id="39953-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="39953-109">Syntax</span></span>


```C++
HRESULT DsSetAuthIdentity(
  _In_ LPCTSTR szUserName,
  _In_ LPCTSTR szDomainName,
  _In_ LPCTSTR szPassword
);
```



## <a name="parameters"></a><span data-ttu-id="39953-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="39953-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39953-111">*szUserName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="39953-111">*szUserName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39953-112">A cadeia de caracteres terminada em nulo que especifica o nome de usuário.</span><span class="sxs-lookup"><span data-stu-id="39953-112">The null-terminated string that specifies the user name.</span></span>

</dd> <dt>

<span data-ttu-id="39953-113">*szDomainName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="39953-113">*szDomainName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39953-114">A cadeia de caracteres terminada em nulo que especifica o nome do domínio ao qual o usuário pertence.</span><span class="sxs-lookup"><span data-stu-id="39953-114">The null-terminated string that specifies the name of the domain that the user belongs to.</span></span>

</dd> <dt>

<span data-ttu-id="39953-115">*szPassword* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="39953-115">*szPassword* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39953-116">A cadeia de caracteres terminada em nulo que especifica a senha do usuário no domínio especificado.</span><span class="sxs-lookup"><span data-stu-id="39953-116">The null-terminated string that specifies the password of the user in the specified domain.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39953-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="39953-117">Return value</span></span>

<span data-ttu-id="39953-118">Se for bem-sucedido, retorna um código de êxito **HRESULT** padrão; caso contrário, um código de falha será retornado.</span><span class="sxs-lookup"><span data-stu-id="39953-118">If successful, returns a standard **HRESULT** success codes; otherwise, a failure code is returned.</span></span>

## <a name="remarks"></a><span data-ttu-id="39953-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="39953-119">Remarks</span></span>

<span data-ttu-id="39953-120">Se **DsSetAuthIdentity** não for chamado, o contexto de segurança do processo atual será assumido.</span><span class="sxs-lookup"><span data-stu-id="39953-120">If **DsSetAuthIdentity** is not called, security context of the current process is assumed.</span></span>

## <a name="requirements"></a><span data-ttu-id="39953-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="39953-121">Requirements</span></span>



| <span data-ttu-id="39953-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="39953-122">Requirement</span></span> | <span data-ttu-id="39953-123">Valor</span><span class="sxs-lookup"><span data-stu-id="39953-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="39953-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="39953-124">Minimum supported client</span></span><br/> | <span data-ttu-id="39953-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="39953-125">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="39953-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="39953-126">Minimum supported server</span></span><br/> | <span data-ttu-id="39953-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="39953-127">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="39953-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="39953-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="39953-129"><dt>Ntdsbcli. h</dt></span><span class="sxs-lookup"><span data-stu-id="39953-129"><dt>Ntdsbcli.h</dt></span></span> </dl>   |
| <span data-ttu-id="39953-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="39953-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="39953-131"><dt>Ntdsbcli. lib</dt></span><span class="sxs-lookup"><span data-stu-id="39953-131"><dt>Ntdsbcli.lib</dt></span></span> </dl> |
| <span data-ttu-id="39953-132">DLL</span><span class="sxs-lookup"><span data-stu-id="39953-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="39953-133"><dt>Ntdsbcli.dll</dt></span><span class="sxs-lookup"><span data-stu-id="39953-133"><dt>Ntdsbcli.dll</dt></span></span> </dl> |
| <span data-ttu-id="39953-134">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="39953-134">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="39953-135">**DsSetAuthIdentityW** (Unicode) e **DsSetAuthIdentityA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="39953-135">**DsSetAuthIdentityW** (Unicode) and **DsSetAuthIdentityA** (ANSI)</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="39953-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="39953-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39953-137">Fazendo backup e restaurando um servidor de Active Directory</span><span class="sxs-lookup"><span data-stu-id="39953-137">Backing Up and Restoring an Active Directory Server</span></span>](backing-up-and-restoring-an-active-directory-server.md)
</dt> <dt>

[<span data-ttu-id="39953-138">Funções de backup de diretório</span><span class="sxs-lookup"><span data-stu-id="39953-138">Directory Backup Functions</span></span>](directory-backup-functions.md)
</dt> </dl>

 

