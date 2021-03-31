---
title: Método SendMessage da classe Win32_VirtualDesktopSession
description: Envie uma mensagem para o usuário por meio da sessão de área de trabalho virtual.
ms.assetid: 4bb9183e-c016-48f2-8e8c-0d5fb395c435
ms.tgt_platform: multiple
keywords:
- Método SendMessage Serviços de Área de Trabalho Remota
- Método SendMessage Serviços de Área de Trabalho Remota, classe Win32_VirtualDesktopSession
- Classe Win32_VirtualDesktopSession Serviços de Área de Trabalho Remota, método SendMessage
topic_type:
- apiref
api_name:
- Win32_VirtualDesktopSession.SendMessage
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1e3e72f5c401b8cbb0e5e5de45f594d61af6275
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369573"
---
# <a name="sendmessage-method-of-the-win32_virtualdesktopsession-class"></a><span data-ttu-id="29e82-106">Método SendMessage da classe Win32 \_ VirtualDesktopSession</span><span class="sxs-lookup"><span data-stu-id="29e82-106">SendMessage method of the Win32\_VirtualDesktopSession class</span></span>

<span data-ttu-id="29e82-107">Envie uma mensagem para o usuário por meio da sessão de área de trabalho virtual.</span><span class="sxs-lookup"><span data-stu-id="29e82-107">Send a message to the user through the virtual desktop session.</span></span>

## <a name="syntax"></a><span data-ttu-id="29e82-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="29e82-108">Syntax</span></span>


```mof
uint32 SendMessage(
  [in] string Title,
  [in] string Message
);
```



## <a name="parameters"></a><span data-ttu-id="29e82-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="29e82-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29e82-110">*Título* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="29e82-110">*Title* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29e82-111">O título do mensagens das.</span><span class="sxs-lookup"><span data-stu-id="29e82-111">The title of the messge.</span></span>

</dd> <dt>

<span data-ttu-id="29e82-112">*Mensagem* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="29e82-112">*Message* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29e82-113">O conteúdo da mensagem.</span><span class="sxs-lookup"><span data-stu-id="29e82-113">The content of the message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29e82-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="29e82-114">Return value</span></span>

<span data-ttu-id="29e82-115">Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="29e82-115">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="29e82-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="29e82-116">Requirements</span></span>



| <span data-ttu-id="29e82-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="29e82-117">Requirement</span></span> | <span data-ttu-id="29e82-118">Valor</span><span class="sxs-lookup"><span data-stu-id="29e82-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="29e82-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="29e82-119">Minimum supported client</span></span><br/> | <span data-ttu-id="29e82-120">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="29e82-120">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="29e82-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="29e82-121">Minimum supported server</span></span><br/> | <span data-ttu-id="29e82-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="29e82-122">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="29e82-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="29e82-123">Namespace</span></span><br/>                | <span data-ttu-id="29e82-124">\\RDMs CIMv2 \\ raiz</span><span class="sxs-lookup"><span data-stu-id="29e82-124">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="29e82-125">MOF</span><span class="sxs-lookup"><span data-stu-id="29e82-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="29e82-126"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="29e82-126"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="29e82-127">DLL</span><span class="sxs-lookup"><span data-stu-id="29e82-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="29e82-128"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="29e82-128"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="29e82-129">Consulte também</span><span class="sxs-lookup"><span data-stu-id="29e82-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29e82-130">**\_VirtualDesktopSession Win32**</span><span class="sxs-lookup"><span data-stu-id="29e82-130">**Win32\_VirtualDesktopSession**</span></span>](win32-virtualdesktopsession.md)
</dt> </dl>

 

 





