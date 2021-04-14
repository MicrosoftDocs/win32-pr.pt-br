---
description: A \_ notificação SPFILENOTIFY TARGETEXISTS será enviada para a rotina de retorno de chamada se o arquivo a ser copiado tiver sido colocado na fila com o \_ sinalizador de cópia NoOverwrite do SP \_ e esse arquivo já existir no diretório de destino.
ms.assetid: 5c6e0c59-0340-4aa6-94db-8d9a5d202758
title: Mensagem de SPFILENOTIFY_TARGETEXISTS (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1d0c1a1ffba520789113b0dc78246657a4fe324
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104370748"
---
# <a name="spfilenotify_targetexists-message"></a><span data-ttu-id="712db-103">\_Mensagem SPFILENOTIFY TARGETEXISTS</span><span class="sxs-lookup"><span data-stu-id="712db-103">SPFILENOTIFY\_TARGETEXISTS message</span></span>

<span data-ttu-id="712db-104">A notificação **SPFILENOTIFY \_ TARGETEXISTS** será enviada para a rotina de retorno de chamada se o arquivo a ser copiado tiver sido colocado na fila com o \_ sinalizador de cópia NoOverwrite do SP \_ e esse arquivo já existir no diretório de destino.</span><span class="sxs-lookup"><span data-stu-id="712db-104">The **SPFILENOTIFY\_TARGETEXISTS** notification is sent to the callback routine if the file to be copied was queued with the SP\_COPY\_NOOVERWRITE flag and that file already exists in the target directory.</span></span> <span data-ttu-id="712db-105">Ele pode ser enviado para a rotina de retorno de chamada isoladamente ou combinada, usando o operador OR, com as notificações [**SPFILENOTIFY \_ LANGMISMATCH**](spfilenotify-langmismatch.md) e/ou [**SPFILENOTIFY \_ TARGETNEWER**](spfilenotify-targetnewer.md) .</span><span class="sxs-lookup"><span data-stu-id="712db-105">It can be sent to the callback routine alone or combined, by using the OR operator, with the [**SPFILENOTIFY\_LANGMISMATCH**](spfilenotify-langmismatch.md) and/or [**SPFILENOTIFY\_TARGETNEWER**](spfilenotify-targetnewer.md) notifications.</span></span>


```C++
SPFILENOTIFY_TARGETEXISTS
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a><span data-ttu-id="712db-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="712db-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="712db-107">*Param1*</span><span class="sxs-lookup"><span data-stu-id="712db-107">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="712db-108">Ponteiro para uma estrutura [**FILEpaths**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) que contém informações sobre os caminhos para os arquivos de origem e de destino.</span><span class="sxs-lookup"><span data-stu-id="712db-108">Pointer to a [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) structure that contains information about the paths for the source and target files.</span></span>

</dd> <dt>

<span data-ttu-id="712db-109">*Param2*</span><span class="sxs-lookup"><span data-stu-id="712db-109">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="712db-110">Esse parâmetro não é usado a menos que essa notificação seja combinada, usando o operador OR, com a notificação [**SPFILENOTIFY \_ LANGMISMATCH**](spfilenotify-langmismatch.md) .</span><span class="sxs-lookup"><span data-stu-id="712db-110">This parameter is not used unless this notification is combined, by using the OR operator, with the [**SPFILENOTIFY\_LANGMISMATCH**](spfilenotify-langmismatch.md) notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="712db-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="712db-111">Return value</span></span>

<span data-ttu-id="712db-112">A rotina de retorno de chamada deve retornar um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="712db-112">The callback routine should return one of the following values.</span></span>



| <span data-ttu-id="712db-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="712db-113">Return code</span></span>                                                                          | <span data-ttu-id="712db-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="712db-114">Description</span></span>                                            |
|--------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <span data-ttu-id="712db-115"><dt>**TRUE**</dt></span><span class="sxs-lookup"><span data-stu-id="712db-115"><dt>**TRUE**</dt></span></span> </dl>  | <span data-ttu-id="712db-116">Substitua o arquivo no diretório de destino.</span><span class="sxs-lookup"><span data-stu-id="712db-116">Overwrite the file in the target directory.</span></span><br/> |
| <dl> <span data-ttu-id="712db-117"><dt>**FOR**</dt></span><span class="sxs-lookup"><span data-stu-id="712db-117"><dt>**FALSE**</dt></span></span> </dl> | <span data-ttu-id="712db-118">Ignore a operação de cópia atual.</span><span class="sxs-lookup"><span data-stu-id="712db-118">Skip the current copy operation.</span></span><br/>            |



 

## <a name="requirements"></a><span data-ttu-id="712db-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="712db-119">Requirements</span></span>



| <span data-ttu-id="712db-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="712db-120">Requirement</span></span> | <span data-ttu-id="712db-121">Valor</span><span class="sxs-lookup"><span data-stu-id="712db-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="712db-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="712db-122">Minimum supported client</span></span><br/> | <span data-ttu-id="712db-123">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="712db-123">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="712db-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="712db-124">Minimum supported server</span></span><br/> | <span data-ttu-id="712db-125">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="712db-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="712db-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="712db-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="712db-127"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="712db-127"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="712db-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="712db-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="712db-129">Visão geral</span><span class="sxs-lookup"><span data-stu-id="712db-129">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="712db-130">Notificações</span><span class="sxs-lookup"><span data-stu-id="712db-130">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="712db-131">**FILEPATHS**</span><span class="sxs-lookup"><span data-stu-id="712db-131">**FILEPATHS**</span></span>](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)
</dt> <dt>

[<span data-ttu-id="712db-132">**SetupCommitFileQueue**</span><span class="sxs-lookup"><span data-stu-id="712db-132">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[<span data-ttu-id="712db-133">**SetupDefaultQueueCallback**</span><span class="sxs-lookup"><span data-stu-id="712db-133">**SetupDefaultQueueCallback**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> <dt>

[<span data-ttu-id="712db-134">**SetupInstallFile**</span><span class="sxs-lookup"><span data-stu-id="712db-134">**SetupInstallFile**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea)
</dt> <dt>

[<span data-ttu-id="712db-135">**SetupInstallFileEx**</span><span class="sxs-lookup"><span data-stu-id="712db-135">**SetupInstallFileEx**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfileexa)
</dt> <dt>

[<span data-ttu-id="712db-136">**SetupInstallFromInfSection**</span><span class="sxs-lookup"><span data-stu-id="712db-136">**SetupInstallFromInfSection**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona)
</dt> </dl>

 

 




