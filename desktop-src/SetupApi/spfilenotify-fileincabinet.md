---
description: A \_ notificação SPFILENOTIFY FILEINCABINET é enviada a uma rotina de retorno de chamada por SetupIterateCabinet para cada arquivo encontrado no gabinete. A rotina de retorno de chamada deve retornar um valor que indica se deseja extrair o arquivo.
ms.assetid: c6d89759-c0d4-4741-b992-43eaa0dc4f01
title: Mensagem de SPFILENOTIFY_FILEINCABINET (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 496db3cef814f2bf366f4cb6f91132efe01a2406
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105756361"
---
# <a name="spfilenotify_fileincabinet-message"></a><span data-ttu-id="e16ce-104">\_Mensagem SPFILENOTIFY FILEINCABINET</span><span class="sxs-lookup"><span data-stu-id="e16ce-104">SPFILENOTIFY\_FILEINCABINET message</span></span>

<span data-ttu-id="e16ce-105">A notificação **SPFILENOTIFY \_ FILEINCABINET** é enviada a uma rotina de retorno de chamada por [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) para cada arquivo encontrado no gabinete.</span><span class="sxs-lookup"><span data-stu-id="e16ce-105">The **SPFILENOTIFY\_FILEINCABINET** notification is sent to a callback routine by [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) for each file found in the cabinet.</span></span> <span data-ttu-id="e16ce-106">A rotina de retorno de chamada deve retornar um valor que indica se deseja extrair o arquivo.</span><span class="sxs-lookup"><span data-stu-id="e16ce-106">The callback routine must return a value indicating whether to extract the file.</span></span>


```C++
SPFILENOTIFY_FILEINCABINET
  Param1 = (UINT) FileInCabinetInfo;
  Param2 = (UINT) CabinetFile;
            
```



## <a name="parameters"></a><span data-ttu-id="e16ce-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e16ce-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e16ce-108">*Param1*</span><span class="sxs-lookup"><span data-stu-id="e16ce-108">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="e16ce-109">Ponteiro para um [**arquivo \_ na estrutura de \_ \_ informações do gabinete**](/windows/desktop/api/Setupapi/ns-setupapi-file_in_cabinet_info_a) que contém informações sobre o arquivo no gabinete.</span><span class="sxs-lookup"><span data-stu-id="e16ce-109">Pointer to a [**FILE\_IN\_CABINET\_INFO**](/windows/desktop/api/Setupapi/ns-setupapi-file_in_cabinet_info_a) structure that contains information about the file in the cabinet.</span></span>

</dd> <dt>

<span data-ttu-id="e16ce-110">*Param2*</span><span class="sxs-lookup"><span data-stu-id="e16ce-110">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="e16ce-111">Ponteiro para uma cadeia de caracteres terminada em nulo que contém o nome do arquivo de gabinete.</span><span class="sxs-lookup"><span data-stu-id="e16ce-111">Pointer to a null-terminated string that contains the filename of the cabinet file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e16ce-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e16ce-112">Return value</span></span>

<span data-ttu-id="e16ce-113">Sua rotina de retorno de chamada deve retornar um dos itens a seguir.</span><span class="sxs-lookup"><span data-stu-id="e16ce-113">Your callback routine should return one of the following.</span></span>



| <span data-ttu-id="e16ce-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="e16ce-114">Return code</span></span>                                                                                 | <span data-ttu-id="e16ce-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="e16ce-115">Description</span></span>                                  |
|---------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="e16ce-116"><dt>**FILEOP \_ ignorar**</dt></span><span class="sxs-lookup"><span data-stu-id="e16ce-116"><dt>**FILEOP\_SKIP**</dt></span></span> </dl> | <span data-ttu-id="e16ce-117">Não Extraia o arquivo, pule-o.</span><span class="sxs-lookup"><span data-stu-id="e16ce-117">Do not extract the file, skip it.</span></span><br/> |
| <dl> <span data-ttu-id="e16ce-118"><dt>**FILEOP \_ doit**</dt></span><span class="sxs-lookup"><span data-stu-id="e16ce-118"><dt>**FILEOP\_DOIT**</dt></span></span> </dl> | <span data-ttu-id="e16ce-119">Extraia o arquivo.</span><span class="sxs-lookup"><span data-stu-id="e16ce-119">Extract the file.</span></span><br/>                 |



 

<span data-ttu-id="e16ce-120">Se a rotina de retorno de chamada retornar FILEOP \_ doit, o nome a ser usado para o arquivo extraído deverá ser especificado no membro **FullTargetName** do [**arquivo \_ na estrutura de \_ \_ informações do gabinete**](/windows/desktop/api/Setupapi/ns-setupapi-file_in_cabinet_info_a) passada para a rotina em *param1*.</span><span class="sxs-lookup"><span data-stu-id="e16ce-120">If your callback routine returns FILEOP\_DOIT, the name to use for the extracted file should be specified in the **FullTargetName** member of the [**FILE\_IN\_CABINET\_INFO**](/windows/desktop/api/Setupapi/ns-setupapi-file_in_cabinet_info_a) structure passed to the routine in *Param1*.</span></span>

> [!Note]  
> <span data-ttu-id="e16ce-121">Não há rotina de retorno de chamada de gabinete padrão.</span><span class="sxs-lookup"><span data-stu-id="e16ce-121">There is no default cabinet callback routine.</span></span> <span data-ttu-id="e16ce-122">O aplicativo de instalação deve fornecer uma rotina de retorno de chamada para manipular as notificações enviadas pelo [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta).</span><span class="sxs-lookup"><span data-stu-id="e16ce-122">The setup application should supply a callback routine to handle the notifications sent by [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e16ce-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e16ce-123">Requirements</span></span>



| <span data-ttu-id="e16ce-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="e16ce-124">Requirement</span></span> | <span data-ttu-id="e16ce-125">Valor</span><span class="sxs-lookup"><span data-stu-id="e16ce-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e16ce-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e16ce-126">Minimum supported client</span></span><br/> | <span data-ttu-id="e16ce-127">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="e16ce-127">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="e16ce-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e16ce-128">Minimum supported server</span></span><br/> | <span data-ttu-id="e16ce-129">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e16ce-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e16ce-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e16ce-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="e16ce-131"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="e16ce-131"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e16ce-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="e16ce-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e16ce-133">Visão geral</span><span class="sxs-lookup"><span data-stu-id="e16ce-133">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="e16ce-134">Notificações</span><span class="sxs-lookup"><span data-stu-id="e16ce-134">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="e16ce-135">**ARQUIVO \_ em \_ informações do gabinete \_**</span><span class="sxs-lookup"><span data-stu-id="e16ce-135">**FILE\_IN\_CABINET\_INFO**</span></span>](/windows/desktop/api/Setupapi/ns-setupapi-file_in_cabinet_info_a)
</dt> <dt>

[<span data-ttu-id="e16ce-136">**SetupIterateCabinet**</span><span class="sxs-lookup"><span data-stu-id="e16ce-136">**SetupIterateCabinet**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta)
</dt> </dl>

 

 




