---
description: A função SceSvcAttachmentConfig é chamada pelo mecanismo de configuração de segurança quando o sistema é configurado.
ms.assetid: ad20649a-2391-421b-a08c-a4ea6a882abc
title: Função de retorno de chamada SceSvcAttachmentConfig
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SceSvcAttachmentConfig
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: c78caa3b8e08ade9c674a11d113a8b91b8f5fad1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646992"
---
# <a name="scesvcattachmentconfig-callback-function"></a><span data-ttu-id="f99e0-103">Função de retorno de chamada SceSvcAttachmentConfig</span><span class="sxs-lookup"><span data-stu-id="f99e0-103">SceSvcAttachmentConfig callback function</span></span>

<span data-ttu-id="f99e0-104">A função **SceSvcAttachmentConfig** é chamada pelo mecanismo de configuração de segurança quando o sistema é configurado.</span><span class="sxs-lookup"><span data-stu-id="f99e0-104">The **SceSvcAttachmentConfig** function is called by the Security Configuration Engine when the system is configured.</span></span>

## <a name="syntax"></a><span data-ttu-id="f99e0-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f99e0-105">Syntax</span></span>


```C++
SCESTATUS WINAPI SceSvcAttachmentConfig(
  _In_ PSCESVC_CALLBACK_INFO pSceCbInfo
);
```



## <a name="parameters"></a><span data-ttu-id="f99e0-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f99e0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f99e0-107">*pSceCbInfo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f99e0-107">*pSceCbInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f99e0-108">Ponteiro para uma estrutura de [**\_ \_ informações de retorno de chamada SCESVC**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) que contém o identificador de banco de dados e as funções de retorno de chamada para consultar, definir e liberar informações.</span><span class="sxs-lookup"><span data-stu-id="f99e0-108">Pointer to a [**SCESVC\_CALLBACK\_INFO**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) structure that contains the database handle and the callback functions to query, set, and free information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f99e0-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f99e0-109">Return value</span></span>

<span data-ttu-id="f99e0-110">Se essa função for bem-sucedida, ela retornará SCESTATUS \_ Success.</span><span class="sxs-lookup"><span data-stu-id="f99e0-110">If this function succeeds, it returns SCESTATUS\_SUCCESS.</span></span> <span data-ttu-id="f99e0-111">Caso contrário, ele retorna um código de erro.</span><span class="sxs-lookup"><span data-stu-id="f99e0-111">Otherwise it returns an error code.</span></span> <span data-ttu-id="f99e0-112">Para obter mais informações sobre os códigos de erro de configuração de segurança, consulte [valores de retorno de anexo](management-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="f99e0-112">For more information about the Security Configuration error codes, see [Attachment Return Values](management-return-values.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f99e0-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="f99e0-113">Remarks</span></span>

<span data-ttu-id="f99e0-114">Ao implementar essa função, use a função de retorno de chamada apontada pelo membro **pfQueryInfo** da estrutura de [**\_ \_ informações de retorno de chamada SCESVC**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) (pSceCbInfo->pfQueryInfo) para recuperar informações de configuração.</span><span class="sxs-lookup"><span data-stu-id="f99e0-114">When implementing this function, use the callback function pointed to by the **pfQueryInfo** member of the [**SCESVC\_CALLBACK\_INFO**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) structure (pSceCbInfo->pfQueryInfo) to retrieve configuration information.</span></span> <span data-ttu-id="f99e0-115">Em seguida, configure o serviço usando as informações retornadas.</span><span class="sxs-lookup"><span data-stu-id="f99e0-115">Then configure the service using the returned information.</span></span>

<span data-ttu-id="f99e0-116">Essa função deve fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="f99e0-116">This function must do the following:</span></span>

-   <span data-ttu-id="f99e0-117">Consultar informações de configuração do conjunto de ferramentas de configuração de segurança usando a função de retorno de chamada apontada pelo membro **pfQueryInfo** da estrutura de [**informações de retorno de \_ chamada \_ SCESVC**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) (pSceCbInfo->pfQueryInfo).</span><span class="sxs-lookup"><span data-stu-id="f99e0-117">Query configuration information from the Security Configuration tool set using the callback function pointed to by the **pfQueryInfo** member of the [**SCESVC\_CALLBACK\_INFO**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) structure (pSceCbInfo->pfQueryInfo).</span></span>
-   <span data-ttu-id="f99e0-118">Configure o serviço usando as informações de configuração.</span><span class="sxs-lookup"><span data-stu-id="f99e0-118">Configure the service using the configuration information.</span></span>

<span data-ttu-id="f99e0-119">Para obter mais informações, consulte [Implementing SceSvcAttachmentConfig](implementing-scesvcattachmentconfig.md)</span><span class="sxs-lookup"><span data-stu-id="f99e0-119">For more information, see [Implementing SceSvcAttachmentConfig](implementing-scesvcattachmentconfig.md)</span></span>

## <a name="requirements"></a><span data-ttu-id="f99e0-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f99e0-120">Requirements</span></span>



| <span data-ttu-id="f99e0-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="f99e0-121">Requirement</span></span> | <span data-ttu-id="f99e0-122">Valor</span><span class="sxs-lookup"><span data-stu-id="f99e0-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f99e0-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f99e0-123">Minimum supported client</span></span><br/> | <span data-ttu-id="f99e0-124">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="f99e0-124">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="f99e0-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f99e0-125">Minimum supported server</span></span><br/> | <span data-ttu-id="f99e0-126">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f99e0-126">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f99e0-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="f99e0-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f99e0-128">**informações de retorno de chamada do SCESVC \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f99e0-128">**SCESVC\_CALLBACK\_INFO**</span></span>](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info)
</dt> <dt>

[<span data-ttu-id="f99e0-129">**SceSvcAttachmentAnalyze**</span><span class="sxs-lookup"><span data-stu-id="f99e0-129">**SceSvcAttachmentAnalyze**</span></span>](scesvcattachmentanalyze.md)
</dt> </dl>

 

 




