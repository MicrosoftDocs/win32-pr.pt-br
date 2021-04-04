---
description: A função SceSvcAttachmentUpdate é chamada pelos snap-ins de configuração de segurança para passar alterações de configuração para o banco de dados de segurança.
ms.assetid: 2b5b3718-8ccb-480a-97fb-c8115d8f3a5c
title: Função de retorno de chamada SceSvcAttachmentUpdate
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SceSvcAttachmentUpdate
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 5bc4c9426f6a085c72f2fc3d872de4d7da59156b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646991"
---
# <a name="scesvcattachmentupdate-callback-function"></a><span data-ttu-id="d0a72-103">Função de retorno de chamada SceSvcAttachmentUpdate</span><span class="sxs-lookup"><span data-stu-id="d0a72-103">SceSvcAttachmentUpdate callback function</span></span>

<span data-ttu-id="d0a72-104">A função **SceSvcAttachmentUpdate** é chamada pelos snap-ins de configuração de segurança para passar alterações de configuração para o banco de dados de segurança.</span><span class="sxs-lookup"><span data-stu-id="d0a72-104">The **SceSvcAttachmentUpdate** function is called by the Security Configuration snap-ins to pass configuration changes to the security database.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0a72-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d0a72-105">Syntax</span></span>


```C++
SCESTATUS WINAPI SceSvcAttachmentUpdate(
  _In_ PSCESVC_CALLBACK_INFO     pSceCbInfo,
  _In_ SCESVC_CONFIGURATION_INFO *ServiceInfo
);
```



## <a name="parameters"></a><span data-ttu-id="d0a72-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d0a72-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0a72-107">*pSceCbInfo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d0a72-107">*pSceCbInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0a72-108">Ponteiro para uma estrutura de [**\_ \_ informações de retorno de chamada SCESVC**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) que contém o identificador de retorno de chamada e ponteiros de função para o SCE.</span><span class="sxs-lookup"><span data-stu-id="d0a72-108">Pointer to a [**SCESVC\_CALLBACK\_INFO**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) structure which contains the callback handle and function pointers to SCE.</span></span>

</dd> <dt>

<span data-ttu-id="d0a72-109">*Informações* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d0a72-109">*ServiceInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0a72-110">Informações de configuração atualizadas.</span><span class="sxs-lookup"><span data-stu-id="d0a72-110">Updated configuration information.</span></span> <span data-ttu-id="d0a72-111">A estrutura de dados usada para essas informações são as [**\_ \_ informações de configuração do SCESVC**](/windows/win32/api/scesvc/ns-scesvc-scesvc_configuration_info).</span><span class="sxs-lookup"><span data-stu-id="d0a72-111">The data structure used for this information is [**SCESVC\_CONFIGURATION\_INFO**](/windows/win32/api/scesvc/ns-scesvc-scesvc_configuration_info).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0a72-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d0a72-112">Return value</span></span>

<span data-ttu-id="d0a72-113">Se essa função for bem-sucedida, ela retornará SCESTATUS \_ Success.</span><span class="sxs-lookup"><span data-stu-id="d0a72-113">If this function succeeds, it returns SCESTATUS\_SUCCESS.</span></span> <span data-ttu-id="d0a72-114">Caso contrário, ele retorna um código de erro.</span><span class="sxs-lookup"><span data-stu-id="d0a72-114">Otherwise it returns an error code.</span></span> <span data-ttu-id="d0a72-115">Para obter mais informações sobre os códigos de erro de configuração de segurança, consulte [valores de retorno de anexo](management-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="d0a72-115">For more information about the Security Configuration error codes, see [Attachment Return Values](management-return-values.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="d0a72-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="d0a72-116">Remarks</span></span>

<span data-ttu-id="d0a72-117">A função **SceSvcAttachmentUpdate** deve fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="d0a72-117">The **SceSvcAttachmentUpdate** function must do the following:</span></span>

-   <span data-ttu-id="d0a72-118">Chame a função de retorno de chamada apontada pelo membro **pfQueryInfo** da estrutura de [**\_ \_ informações de retorno de chamada SCESVC**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) (pSceCbInfo->pfQueryInfo) para recuperar as informações de configuração de base atuais do banco de dados de segurança.</span><span class="sxs-lookup"><span data-stu-id="d0a72-118">Call the callback function pointed to by the **pfQueryInfo** member of the [**SCESVC\_CALLBACK\_INFO**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) structure (pSceCbInfo->pfQueryInfo) to retrieve the current base configuration information from the security database.</span></span>
-   <span data-ttu-id="d0a72-119">Chame a função de retorno de chamada apontada pelo membro **pfQueryInfo** da estrutura de [**\_ \_ informações de retorno de chamada SCESVC**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) (pSceCbInfo->pfQueryInfo) para recuperar o último conjunto de diferenças (informações de análise) do banco de dados de segurança.</span><span class="sxs-lookup"><span data-stu-id="d0a72-119">Call the callback function pointed to by the **pfQueryInfo** member of the [**SCESVC\_CALLBACK\_INFO**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) structure (pSceCbInfo->pfQueryInfo) to retrieve the last set of differences (analysis information) from the security database.</span></span>
-   <span data-ttu-id="d0a72-120">Use as informações de serviço fornecidas (consulte *serviceInfo*) para calcular a nova configuração de base.</span><span class="sxs-lookup"><span data-stu-id="d0a72-120">Use the supplied service information (see *ServiceInfo*) to compute the new base configuration.</span></span>
-   <span data-ttu-id="d0a72-121">Use as informações de serviço fornecidas (consulte *serviceInfo*) e a análise para calcular as novas informações de diferença.</span><span class="sxs-lookup"><span data-stu-id="d0a72-121">Use the supplied service information (see *ServiceInfo*) and the analysis to compute the new difference information.</span></span>
-   <span data-ttu-id="d0a72-122">Chame a função de retorno de chamada apontada pelo membro **pfSetInfo** da estrutura de [**\_ \_ informações de retorno de chamada SCESVC**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) (pSceCbInfo->pfSetInfo) para definir a nova configuração de base no banco de dados de segurança.</span><span class="sxs-lookup"><span data-stu-id="d0a72-122">Call the callback function pointed to by the **pfSetInfo** member of the [**SCESVC\_CALLBACK\_INFO**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) structure (pSceCbInfo->pfSetInfo)to set the new base configuration in the security database.</span></span>
-   <span data-ttu-id="d0a72-123">Chame a função de retorno de chamada apontada pelo membro **pfSetInfo** da estrutura de [**\_ \_ informações de retorno de chamada SCESVC**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) (pSceCbInfo->pfSetInfo) para definir as novas informações de análise no banco de dados de segurança.</span><span class="sxs-lookup"><span data-stu-id="d0a72-123">Call the callback function pointed to by the **pfSetInfo** member of the [**SCESVC\_CALLBACK\_INFO**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) structure (pSceCbInfo->pfSetInfo) to set the new analysis information in the security database.</span></span>

<span data-ttu-id="d0a72-124">Para obter mais informações, consulte [Implementing SceSvcAttachmentUpdate](implementing-scesvcattachmentupdate.md)</span><span class="sxs-lookup"><span data-stu-id="d0a72-124">For more information, see [Implementing SceSvcAttachmentUpdate](implementing-scesvcattachmentupdate.md)</span></span>

## <a name="requirements"></a><span data-ttu-id="d0a72-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d0a72-125">Requirements</span></span>



| <span data-ttu-id="d0a72-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="d0a72-126">Requirement</span></span> | <span data-ttu-id="d0a72-127">Valor</span><span class="sxs-lookup"><span data-stu-id="d0a72-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d0a72-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d0a72-128">Minimum supported client</span></span><br/> | <span data-ttu-id="d0a72-129">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="d0a72-129">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="d0a72-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d0a72-130">Minimum supported server</span></span><br/> | <span data-ttu-id="d0a72-131">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d0a72-131">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d0a72-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="d0a72-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0a72-133">**informações de retorno de chamada do SCESVC \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d0a72-133">**SCESVC\_CALLBACK\_INFO**</span></span>](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info)
</dt> <dt>

[<span data-ttu-id="d0a72-134">**\_informações de configuração do SCESVC \_**</span><span class="sxs-lookup"><span data-stu-id="d0a72-134">**SCESVC\_CONFIGURATION\_INFO**</span></span>](/windows/win32/api/scesvc/ns-scesvc-scesvc_configuration_info)
</dt> </dl>

 

 




