---
title: Método INapServerInfo GetNapServerInfo (NapServerManagement. h)
description: Recupera informações sobre o servidor NAP.
ms.assetid: 02f7ce40-3443-4263-86b2-4276cbc7b694
keywords:
- Método GetNapServerInfo NAP
- Método GetNapServerInfo NAP, interface INapServerInfo
- INapServerInfo interface NAP, método GetNapServerInfo
topic_type:
- apiref
api_name:
- INapServerInfo.GetNapServerInfo
api_location:
- qsvrmgmt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b182b9e1a5c8d7974128b062fd284c5af3f060f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645246"
---
# <a name="inapserverinfogetnapserverinfo-method"></a><span data-ttu-id="02f78-106">Método INapServerInfo:: GetNapServerInfo</span><span class="sxs-lookup"><span data-stu-id="02f78-106">INapServerInfo::GetNapServerInfo method</span></span>

> [!Note]  
> <span data-ttu-id="02f78-107">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="02f78-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="02f78-108">O método **INapServerInfo:: GetNapServerInfo** recupera informações sobre o servidor NAP.</span><span class="sxs-lookup"><span data-stu-id="02f78-108">The **INapServerInfo::GetNapServerInfo** method retrieves information about the NAP server.</span></span>

## <a name="syntax"></a><span data-ttu-id="02f78-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="02f78-109">Syntax</span></span>


```C++
HRESULT GetNapServerInfo(
  [out] CountedString **serverName,
  [out] CountedString **serverDescription,
  [out] CountedString **protocolVersion
);
```



## <a name="parameters"></a><span data-ttu-id="02f78-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="02f78-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02f78-111">*nome do Server* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="02f78-111">*serverName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="02f78-112">Um ponteiro para um ponteiro para uma estrutura de [**contadostring**](/windows/win32/api/naptypes/ns-naptypes-countedstring) que contém o nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="02f78-112">A pointer to a pointer to a [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) structure that contains the server name.</span></span>

</dd> <dt>

<span data-ttu-id="02f78-113">*FQDN* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="02f78-113">*serverDescription* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="02f78-114">Um ponteiro para um ponteiro para uma estrutura de [**contadostring**](/windows/win32/api/naptypes/ns-naptypes-countedstring) que contém a descrição do servidor.</span><span class="sxs-lookup"><span data-stu-id="02f78-114">A pointer to a pointer to a [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) structure that contains the server description.</span></span>

</dd> <dt>

<span data-ttu-id="02f78-115">*protocolVersion* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="02f78-115">*protocolVersion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="02f78-116">Um ponteiro para um ponteiro para uma estrutura de [**contadostring**](/windows/win32/api/naptypes/ns-naptypes-countedstring) que contém a versão do protocolo.</span><span class="sxs-lookup"><span data-stu-id="02f78-116">A pointer to a pointer to a [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) structure that contains the protocol version.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02f78-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="02f78-117">Return value</span></span>

<span data-ttu-id="02f78-118">Outros códigos de erro específicos de COM também podem ser retornados.</span><span class="sxs-lookup"><span data-stu-id="02f78-118">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="02f78-119">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="02f78-119">Return code</span></span>                                                                                     | <span data-ttu-id="02f78-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="02f78-120">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="02f78-121"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="02f78-121"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="02f78-122">Operação bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="02f78-122">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="02f78-123"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="02f78-123"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="02f78-124">Erro de permissões, acesso negado.</span><span class="sxs-lookup"><span data-stu-id="02f78-124">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="02f78-125"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="02f78-125"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="02f78-126">O limite de recursos do sistema não pôde executar a operação.</span><span class="sxs-lookup"><span data-stu-id="02f78-126">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="02f78-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="02f78-127">Requirements</span></span>



| <span data-ttu-id="02f78-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="02f78-128">Requirement</span></span> | <span data-ttu-id="02f78-129">Valor</span><span class="sxs-lookup"><span data-stu-id="02f78-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="02f78-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="02f78-130">Minimum supported client</span></span><br/> | <span data-ttu-id="02f78-131">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="02f78-131">None supported</span></span><br/>                                                                          |
| <span data-ttu-id="02f78-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="02f78-132">Minimum supported server</span></span><br/> | <span data-ttu-id="02f78-133">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="02f78-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="02f78-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="02f78-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="02f78-135"><dt>NapServerManagement. h</dt></span><span class="sxs-lookup"><span data-stu-id="02f78-135"><dt>NapServerManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="02f78-136">INSERI</span><span class="sxs-lookup"><span data-stu-id="02f78-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="02f78-137"><dt>NapServerManagement. idl</dt></span><span class="sxs-lookup"><span data-stu-id="02f78-137"><dt>NapServerManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="02f78-138">DLL</span><span class="sxs-lookup"><span data-stu-id="02f78-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="02f78-139"><dt>Qsvrmgmt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="02f78-139"><dt>Qsvrmgmt.dll</dt></span></span> </dl>            |



## <a name="see-also"></a><span data-ttu-id="02f78-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="02f78-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02f78-141">**INapServerInfo**</span><span class="sxs-lookup"><span data-stu-id="02f78-141">**INapServerInfo**</span></span>](inapserverinfo.md)
</dt> <dt>

[<span data-ttu-id="02f78-142">**Contado**</span><span class="sxs-lookup"><span data-stu-id="02f78-142">**CountedString**</span></span>](/windows/win32/api/naptypes/ns-naptypes-countedstring)
</dt> </dl>

 

 





