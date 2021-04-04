---
description: A função SceSvcAttachmentAnalyze é chamada pelo mecanismo de configuração de segurança quando o sistema é analisado.
ms.assetid: 8e8a39b9-c4e2-446e-8e0c-eb2113234c1a
title: Função de retorno de chamada SceSvcAttachmentAnalyze
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SceSvcAttachmentAnalyze
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 296d755a0b082b46122432936d30614019b8b9a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646993"
---
# <a name="scesvcattachmentanalyze-callback-function"></a><span data-ttu-id="e3616-103">Função de retorno de chamada SceSvcAttachmentAnalyze</span><span class="sxs-lookup"><span data-stu-id="e3616-103">SceSvcAttachmentAnalyze callback function</span></span>

<span data-ttu-id="e3616-104">A função **SceSvcAttachmentAnalyze** é chamada pelo mecanismo de configuração de segurança quando o sistema é analisado.</span><span class="sxs-lookup"><span data-stu-id="e3616-104">The **SceSvcAttachmentAnalyze** function is called by the Security Configuration Engine when the system is analyzed.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3616-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e3616-105">Syntax</span></span>


```C++
SCESTATUS WINAPI SceSvcAttachmentAnalyze(
  _In_ PSCESVC_CALLBACK_INFO pSceCbInfo
);
```



## <a name="parameters"></a><span data-ttu-id="e3616-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e3616-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3616-107">*pSceCbInfo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e3616-107">*pSceCbInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3616-108">Ponteiro para uma estrutura de [**\_ \_ informações de retorno de chamada SCESVC**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) que contém um identificador de banco de dados opaco e ponteiros de função de retorno de chamada para consultar, definir e informações gratuitas.</span><span class="sxs-lookup"><span data-stu-id="e3616-108">Pointer to a [**SCESVC\_CALLBACK\_INFO**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) structure which contains an opaque database handle and callback function pointers to query, set, and free information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3616-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e3616-109">Return value</span></span>

<span data-ttu-id="e3616-110">Se essa função for bem-sucedida, ela retornará SCESTATUS \_ Success.</span><span class="sxs-lookup"><span data-stu-id="e3616-110">If this function succeeds, it returns SCESTATUS\_SUCCESS.</span></span> <span data-ttu-id="e3616-111">Caso contrário, ele retorna um código de erro.</span><span class="sxs-lookup"><span data-stu-id="e3616-111">Otherwise it returns an error code.</span></span> <span data-ttu-id="e3616-112">Para obter mais informações sobre os códigos de erro de configuração de segurança, consulte [valores de retorno de anexo](management-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="e3616-112">For more information about the Security Configuration error codes, see [Attachment Return Values](management-return-values.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e3616-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="e3616-113">Remarks</span></span>

<span data-ttu-id="e3616-114">A função **SceSvcAttachmentAnalyze** deve fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="e3616-114">The **SceSvcAttachmentAnalyze** function must do the following:</span></span>

-   <span data-ttu-id="e3616-115">Consulte diretamente as informações de configuração do serviço.</span><span class="sxs-lookup"><span data-stu-id="e3616-115">Directly query configuration information from the service.</span></span>
-   <span data-ttu-id="e3616-116">Chame a função de retorno de chamada apontada pelo membro **pfQueryInfo** da estrutura de [**\_ \_ informações de retorno de chamada SCESVC**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) (pSceCbInfo->pfQueryInfo) para recuperar informações do banco de dados de segurança.</span><span class="sxs-lookup"><span data-stu-id="e3616-116">Call the callback function pointed to by the **pfQueryInfo** member of the [**SCESVC\_CALLBACK\_INFO**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) structure (pSceCbInfo->pfQueryInfo) to retrieve information from the security database.</span></span>
-   <span data-ttu-id="e3616-117">Computar as diferenças entre as informações com base no tipo e na sintaxe.</span><span class="sxs-lookup"><span data-stu-id="e3616-117">Compute the differences between the information based on type and syntax.</span></span>
-   <span data-ttu-id="e3616-118">Chame a função de retorno de chamada apontada pelo membro **pfSetInfo** da estrutura de [**\_ \_ informações de retorno de chamada SCESVC**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) (pSceCbInfo->pfSetInfo) para atualizar o banco de dados de segurança com as informações de serviço recuperadas que são diferentes.</span><span class="sxs-lookup"><span data-stu-id="e3616-118">Call the callback function pointed to by the **pfSetInfo** member of the [**SCESVC\_CALLBACK\_INFO**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) structure (pSceCbInfo->pfSetInfo) to update the security database with the retrieved service information that is different.</span></span>

<span data-ttu-id="e3616-119">Para obter mais informações, consulte [Implementing SceSvcAttachmentAnalyze](implementing-scesvcattachmentanalyze.md).</span><span class="sxs-lookup"><span data-stu-id="e3616-119">For more information, see [Implementing SceSvcAttachmentAnalyze](implementing-scesvcattachmentanalyze.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e3616-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e3616-120">Requirements</span></span>



| <span data-ttu-id="e3616-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3616-121">Requirement</span></span> | <span data-ttu-id="e3616-122">Valor</span><span class="sxs-lookup"><span data-stu-id="e3616-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e3616-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e3616-123">Minimum supported client</span></span><br/> | <span data-ttu-id="e3616-124">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="e3616-124">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="e3616-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e3616-125">Minimum supported server</span></span><br/> | <span data-ttu-id="e3616-126">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e3616-126">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e3616-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="e3616-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3616-128">Implementando SceSvcAttachmentAnalyze</span><span class="sxs-lookup"><span data-stu-id="e3616-128">Implementing SceSvcAttachmentAnalyze</span></span>](implementing-scesvcattachmentanalyze.md)
</dt> <dt>

[<span data-ttu-id="e3616-129">**informações de retorno de chamada do SCESVC \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e3616-129">**SCESVC\_CALLBACK\_INFO**</span></span>](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info)
</dt> <dt>

[<span data-ttu-id="e3616-130">**SceSvcAttachmentConfig**</span><span class="sxs-lookup"><span data-stu-id="e3616-130">**SceSvcAttachmentConfig**</span></span>](scesvcattachmentconfig.md)
</dt> </dl>

 

 




