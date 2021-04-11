---
title: Estrutura EapHostPeerNapInfo (Eaphostpeerapis. h)
description: Contém as informações de NAP (proteção de acesso à rede) em um suplicante de EAP.
ms.assetid: 703eda56-5932-44d5-ae7f-0a6328d82237
keywords:
- Estrutura EapHostPeerNapInfo EAPHost
topic_type:
- apiref
api_name:
- EapHostPeerNapInfo
api_location:
- eaphostpeerapis.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3221f40dea9e84e410a1a643bbbcdc94e9039b21
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009684"
---
# <a name="eaphostpeernapinfo-structure"></a><span data-ttu-id="3105f-104">Estrutura EapHostPeerNapInfo</span><span class="sxs-lookup"><span data-stu-id="3105f-104">EapHostPeerNapInfo structure</span></span>

<span data-ttu-id="3105f-105">A estrutura **EapHostPeerNapInfo** contém as informações de NAP (proteção de acesso à rede) em um suplicante de EAP.</span><span class="sxs-lookup"><span data-stu-id="3105f-105">The **EapHostPeerNapInfo** structure contains the Network Access Protection (NAP) information on an EAP supplicant.</span></span>

## <a name="syntax"></a><span data-ttu-id="3105f-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3105f-106">Syntax</span></span>


```C++
typedef struct _tagEapHostPeerNapInfo {
  ISOLATION_STATE isolationState;
  ProbationTime   probationTime;
  UINT32          stringCorrelationIdLength;
} EapHostPeerNapInfo;
```



## <a name="members"></a><span data-ttu-id="3105f-107">Membros</span><span class="sxs-lookup"><span data-stu-id="3105f-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="3105f-108">**isolamentostate**</span><span class="sxs-lookup"><span data-stu-id="3105f-108">**isolationState**</span></span>
</dt> <dd>

<span data-ttu-id="3105f-109">Uma estrutura de [**\_ estado de isolamento**](/windows/desktop/api/eaphostpeertypes/ne-eaphostpeertypes-isolation_state) que especifica o estado de isolamento NAP de um computador.</span><span class="sxs-lookup"><span data-stu-id="3105f-109">An [**ISOLATION\_STATE**](/windows/desktop/api/eaphostpeertypes/ne-eaphostpeertypes-isolation_state) structure that specifies the NAP isolation state of a computer.</span></span> <span data-ttu-id="3105f-110">O estado de isolamento determina o nível de acesso à rede concedido.</span><span class="sxs-lookup"><span data-stu-id="3105f-110">The isolation state determines the level of network access granted.</span></span>

</dd> <dt>

<span data-ttu-id="3105f-111">**experiênciatime**</span><span class="sxs-lookup"><span data-stu-id="3105f-111">**probationTime**</span></span>
</dt> <dd>

<span data-ttu-id="3105f-112">Uma estrutura de **experiênciatime** que especifica o tempo necessário para a conexão sair da quarentena após a qual a conexão será descartada.</span><span class="sxs-lookup"><span data-stu-id="3105f-112">A **ProbationTime** structure that specifies the time required for the connection to come out of quarantine after which the connection will be dropped.</span></span> <span data-ttu-id="3105f-113">Uma estrutura de modo de **experiência** é idêntica a uma estrutura [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime) .</span><span class="sxs-lookup"><span data-stu-id="3105f-113">A **ProbationTime** structure is identical to a [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime) structure.</span></span>

</dd> <dt>

<span data-ttu-id="3105f-114">**stringCorrelationIdLength**</span><span class="sxs-lookup"><span data-stu-id="3105f-114">**stringCorrelationIdLength**</span></span>
</dt> <dd>

<span data-ttu-id="3105f-115">O comprimento, em bytes, do [STRINGCORRELATIONID](/windows/desktop/NAP/nap-datatypes) NAP que segue essa estrutura.</span><span class="sxs-lookup"><span data-stu-id="3105f-115">The length, in bytes, of the NAP [stringCorrelationId](/windows/desktop/NAP/nap-datatypes) that follows this structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3105f-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="3105f-116">Remarks</span></span>

<span data-ttu-id="3105f-117">A estrutura **EapHostPeerNapInfo** precede a [stringCorrelationId](/windows/desktop/NAP/nap-datatypes) de NAP do tipo de dados **WCHAR** no fluxo de bytes RPC.</span><span class="sxs-lookup"><span data-stu-id="3105f-117">The **EapHostPeerNapInfo** structure precedes the NAP [stringCorrelationId](/windows/desktop/NAP/nap-datatypes) of data type **WCHAR** in the RPC byte stream.</span></span>

## <a name="requirements"></a><span data-ttu-id="3105f-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3105f-118">Requirements</span></span>



| <span data-ttu-id="3105f-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="3105f-119">Requirement</span></span> | <span data-ttu-id="3105f-120">Valor</span><span class="sxs-lookup"><span data-stu-id="3105f-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="3105f-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3105f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="3105f-122">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="3105f-122">Windows 7 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="3105f-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3105f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="3105f-124">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="3105f-124">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="3105f-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3105f-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="3105f-126"><dt>Eaphostpeerapis. h</dt></span><span class="sxs-lookup"><span data-stu-id="3105f-126"><dt>Eaphostpeerapis.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3105f-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="3105f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3105f-128">Estruturas do suplicante EAPHost</span><span class="sxs-lookup"><span data-stu-id="3105f-128">EAPHost Supplicant Structures</span></span>](eap-host-supplicant-structures.md)
</dt> <dt>

[<span data-ttu-id="3105f-129">**EapHostPeerGetAuthStatus**</span><span class="sxs-lookup"><span data-stu-id="3105f-129">**EapHostPeerGetAuthStatus**</span></span>](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetauthstatus)
</dt> <dt>

[<span data-ttu-id="3105f-130">**EapHostPeerMethodAuthParams**</span><span class="sxs-lookup"><span data-stu-id="3105f-130">**EapHostPeerMethodAuthParams**</span></span>](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerauthparams)
</dt> </dl>

 

