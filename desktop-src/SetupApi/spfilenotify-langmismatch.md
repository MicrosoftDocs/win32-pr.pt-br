---
description: A \_ notificação SPFILENOTIFY LANGMISMATCH será enviada para a rotina de retorno de chamada se o idioma do arquivo a ser copiado não corresponder ao idioma de um arquivo de destino existente.
ms.assetid: dff3969e-5847-4ad5-b7d4-237144bbe8e6
title: Mensagem de SPFILENOTIFY_LANGMISMATCH (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3d7828c90dd4dabb8e1cb73a8dcca7ae33ebd3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105755781"
---
# <a name="spfilenotify_langmismatch-message"></a><span data-ttu-id="a6bf4-103">\_Mensagem SPFILENOTIFY LANGMISMATCH</span><span class="sxs-lookup"><span data-stu-id="a6bf4-103">SPFILENOTIFY\_LANGMISMATCH message</span></span>

<span data-ttu-id="a6bf4-104">A notificação **SPFILENOTIFY \_ LANGMISMATCH** será enviada para a rotina de retorno de chamada se o idioma do arquivo a ser copiado não corresponder ao idioma de um arquivo de destino existente.</span><span class="sxs-lookup"><span data-stu-id="a6bf4-104">The **SPFILENOTIFY\_LANGMISMATCH** notification is sent to the callback routine if the language of the file to be copied does not match the language of an existing target file.</span></span> <span data-ttu-id="a6bf4-105">Ele pode ser enviado para a rotina de retorno de chamada isoladamente ou combinada, usando o operador OR, com [**SPFILENOTIFY \_ TARGETEXISTS**](spfilenotify-targetexists.md) e/ou [**SPFILENOTIFY \_ TARGETNEWER**](spfilenotify-targetnewer.md).</span><span class="sxs-lookup"><span data-stu-id="a6bf4-105">It can be sent to the callback routine alone or combined, by using the OR operator, with [**SPFILENOTIFY\_TARGETEXISTS**](spfilenotify-targetexists.md) and/or [**SPFILENOTIFY\_TARGETNEWER**](spfilenotify-targetnewer.md).</span></span>


```C++
SPFILENOTIFY_LANGMISMATCH
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) LanguageInfo;
            
```



## <a name="parameters"></a><span data-ttu-id="a6bf4-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a6bf4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6bf4-107">*Param1*</span><span class="sxs-lookup"><span data-stu-id="a6bf4-107">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="a6bf4-108">Ponteiro para uma estrutura [**FILEpaths**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) que contém informações sobre os caminhos dos arquivos de origem e de destino.</span><span class="sxs-lookup"><span data-stu-id="a6bf4-108">Pointer to a [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) structure that contains information about the paths of the source and target files.</span></span>

</dd> <dt>

<span data-ttu-id="a6bf4-109">*Param2*</span><span class="sxs-lookup"><span data-stu-id="a6bf4-109">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="a6bf4-110">Identifica os idiomas incompatíveis.</span><span class="sxs-lookup"><span data-stu-id="a6bf4-110">Identifies the mismatched languages.</span></span> <span data-ttu-id="a6bf4-111">Esse membro tem o identificador de idioma do arquivo de origem na palavra inferior e o identificador de idioma do arquivo de destino existente na palavra alta.</span><span class="sxs-lookup"><span data-stu-id="a6bf4-111">This member has the language identifier of the source file in the low word, and the language identifier of the existing target file in the high word.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a6bf4-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a6bf4-112">Return value</span></span>

<span data-ttu-id="a6bf4-113">A rotina de retorno de chamada deve retornar um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="a6bf4-113">The callback routine should return one of the following values.</span></span>



| <span data-ttu-id="a6bf4-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="a6bf4-114">Return code</span></span>                                                                          | <span data-ttu-id="a6bf4-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="a6bf4-115">Description</span></span>                                                             |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a6bf4-116"><dt>**TRUE**</dt></span><span class="sxs-lookup"><span data-stu-id="a6bf4-116"><dt>**TRUE**</dt></span></span> </dl>  | <span data-ttu-id="a6bf4-117">Copie o arquivo e substitua o arquivo existente.</span><span class="sxs-lookup"><span data-stu-id="a6bf4-117">Copy the file and overwrite the existing file.</span></span><br/>               |
| <dl> <span data-ttu-id="a6bf4-118"><dt>**FOR**</dt></span><span class="sxs-lookup"><span data-stu-id="a6bf4-118"><dt>**FALSE**</dt></span></span> </dl> | <span data-ttu-id="a6bf4-119">Ignore a operação de cópia.</span><span class="sxs-lookup"><span data-stu-id="a6bf4-119">Skip the copy operation.</span></span> <span data-ttu-id="a6bf4-120">Não substitua o arquivo existente.</span><span class="sxs-lookup"><span data-stu-id="a6bf4-120">Do not overwrite the existing file.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="a6bf4-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a6bf4-121">Requirements</span></span>



| <span data-ttu-id="a6bf4-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="a6bf4-122">Requirement</span></span> | <span data-ttu-id="a6bf4-123">Valor</span><span class="sxs-lookup"><span data-stu-id="a6bf4-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a6bf4-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a6bf4-124">Minimum supported client</span></span><br/> | <span data-ttu-id="a6bf4-125">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="a6bf4-125">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="a6bf4-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a6bf4-126">Minimum supported server</span></span><br/> | <span data-ttu-id="a6bf4-127">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a6bf4-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a6bf4-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a6bf4-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="a6bf4-129"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="a6bf4-129"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a6bf4-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="a6bf4-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6bf4-131">Visão geral</span><span class="sxs-lookup"><span data-stu-id="a6bf4-131">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="a6bf4-132">Notificações</span><span class="sxs-lookup"><span data-stu-id="a6bf4-132">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="a6bf4-133">**FILEPATHS**</span><span class="sxs-lookup"><span data-stu-id="a6bf4-133">**FILEPATHS**</span></span>](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)
</dt> <dt>

[<span data-ttu-id="a6bf4-134">**SetupCommitFileQueue**</span><span class="sxs-lookup"><span data-stu-id="a6bf4-134">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[<span data-ttu-id="a6bf4-135">**SetupDefaultQueueCallback**</span><span class="sxs-lookup"><span data-stu-id="a6bf4-135">**SetupDefaultQueueCallback**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> <dt>

[<span data-ttu-id="a6bf4-136">**SetupInstallFile**</span><span class="sxs-lookup"><span data-stu-id="a6bf4-136">**SetupInstallFile**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea)
</dt> <dt>

[<span data-ttu-id="a6bf4-137">**SetupInstallFileEx**</span><span class="sxs-lookup"><span data-stu-id="a6bf4-137">**SetupInstallFileEx**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfileexa)
</dt> <dt>

[<span data-ttu-id="a6bf4-138">**SetupInstallFromInfSection**</span><span class="sxs-lookup"><span data-stu-id="a6bf4-138">**SetupInstallFromInfSection**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona)
</dt> </dl>

 

 




