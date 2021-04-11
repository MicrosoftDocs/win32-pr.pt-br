---
description: A \_ notificação SPFILENOTIFY NEEDNEWCABINET é enviada pelo SetupIterateCabinet para indicar que o arquivo atual continua em outro gabinete.
ms.assetid: 01207429-11fb-4e2c-89ba-54321992e953
title: Mensagem de SPFILENOTIFY_NEEDNEWCABINET (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3187d48b89579c329a4d0163e151824288462344
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171663"
---
# <a name="spfilenotify_neednewcabinet-message"></a><span data-ttu-id="bbbdc-103">\_Mensagem SPFILENOTIFY NEEDNEWCABINET</span><span class="sxs-lookup"><span data-stu-id="bbbdc-103">SPFILENOTIFY\_NEEDNEWCABINET message</span></span>

<span data-ttu-id="bbbdc-104">A notificação **SPFILENOTIFY \_ NEEDNEWCABINET** é enviada pelo [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) para indicar que o arquivo atual continua em outro gabinete.</span><span class="sxs-lookup"><span data-stu-id="bbbdc-104">The **SPFILENOTIFY\_NEEDNEWCABINET** notification is sent by [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) to indicate that the current file continues in another cabinet.</span></span> <span data-ttu-id="bbbdc-105">Sua rotina de retorno de chamada pode então chamar [**SetupPromptForDisk**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska)ou criar sua própria caixa de diálogo para solicitar que o usuário insira o próximo disco.</span><span class="sxs-lookup"><span data-stu-id="bbbdc-105">Your callback routine can then call [**SetupPromptForDisk**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska), or create its own dialog box to prompt the user to insert the next disk.</span></span>


```C++
SPFILENOTIFY_NEEDNEWCABINET
  Param1 = (UINT) CabinetInfo;
  Param2 = (UINT) NewPath;
            
```



## <a name="parameters"></a><span data-ttu-id="bbbdc-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bbbdc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bbbdc-107">*Param1*</span><span class="sxs-lookup"><span data-stu-id="bbbdc-107">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="bbbdc-108">Ponteiro para uma estrutura de [**\_ informações de gabinete**](/windows/desktop/api/Setupapi/ns-setupapi-cabinet_info_a) que contém informações sobre o gabinete e o arquivo a ser extraído.</span><span class="sxs-lookup"><span data-stu-id="bbbdc-108">Pointer to a [**CABINET\_INFO**](/windows/desktop/api/Setupapi/ns-setupapi-cabinet_info_a) structure that contains information about the cabinet and the file to be extracted.</span></span>

</dd> <dt>

<span data-ttu-id="bbbdc-109">*Param2*</span><span class="sxs-lookup"><span data-stu-id="bbbdc-109">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="bbbdc-110">Se o retorno de chamada não retornar nenhum \_ erro, esse parâmetro será um ponteiro para uma cadeia de caracteres terminada em nulo.</span><span class="sxs-lookup"><span data-stu-id="bbbdc-110">If the callback returns NO\_ERROR, this parameter is a pointer to a null-terminated string.</span></span> <span data-ttu-id="bbbdc-111">Se a cadeia de caracteres não estiver vazia, ela especificará um novo caminho para o gabinete.</span><span class="sxs-lookup"><span data-stu-id="bbbdc-111">If the string is not empty, it specifies a new path to the cabinet.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bbbdc-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bbbdc-112">Return value</span></span>

<span data-ttu-id="bbbdc-113">Sua rotina deve retornar um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="bbbdc-113">Your routine should return one of the following values.</span></span>



| <span data-ttu-id="bbbdc-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="bbbdc-114">Return code</span></span>                                                                                 | <span data-ttu-id="bbbdc-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="bbbdc-115">Description</span></span>                                                                                                                                                                                                                                  |
|---------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="bbbdc-116"><dt>**SEM \_ erros**</dt></span><span class="sxs-lookup"><span data-stu-id="bbbdc-116"><dt>**NO\_ERROR**</dt></span></span> </dl>    | <span data-ttu-id="bbbdc-117">Nenhum erro foi encontrado, continue processando o gabinete.</span><span class="sxs-lookup"><span data-stu-id="bbbdc-117">No error was encountered, continue processing the cabinet.</span></span><br/>                                                                                                                                                                        |
| <dl> <span data-ttu-id="bbbdc-118"><dt>\**Erro \_* do XXX \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="bbbdc-118"><dt>\**ERROR\_* XXX\*\*\*</dt></span></span> </dl> | <span data-ttu-id="bbbdc-119">Ocorreu um erro do tipo especificado.</span><span class="sxs-lookup"><span data-stu-id="bbbdc-119">An error of the specified type occurred.</span></span> <span data-ttu-id="bbbdc-120">A função [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) retornará **false** e o código de erro especificado será retornado por uma chamada para [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="bbbdc-120">The [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) function will return **FALSE**, and the specified error code will be returned by a call to [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span><br/> |



 

> [!Note]  
> <span data-ttu-id="bbbdc-121">Não há rotina de retorno de chamada de gabinete padrão; Portanto, você deve fornecer uma rotina de retorno de chamada para manipular as notificações enviadas pelo [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta).</span><span class="sxs-lookup"><span data-stu-id="bbbdc-121">There is no default cabinet callback routine; thus, you must supply a callback routine to handle the notifications sent by [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta).</span></span>

 

## <a name="remarks"></a><span data-ttu-id="bbbdc-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="bbbdc-122">Remarks</span></span>

<span data-ttu-id="bbbdc-123">Se a rotina de retorno de chamada não retornar nenhum \_ erro, o [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) verificará o buffer apontado por *param2*.</span><span class="sxs-lookup"><span data-stu-id="bbbdc-123">If the callback routine returns NO\_ERROR, [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) checks the buffer pointed to by *Param2*.</span></span> <span data-ttu-id="bbbdc-124">Se o buffer não estiver vazio, ele conterá um novo caminho de origem.</span><span class="sxs-lookup"><span data-stu-id="bbbdc-124">If the buffer is not empty, then it contains a new source path.</span></span> <span data-ttu-id="bbbdc-125">Se o buffer estiver vazio, o caminho de origem será considerado inalterado.</span><span class="sxs-lookup"><span data-stu-id="bbbdc-125">If the buffer is empty, the source path is assumed to be unchanged.</span></span>

<span data-ttu-id="bbbdc-126">Sua função de retorno de chamada deve garantir que o gabinete esteja acessível antes de retornar, chamando a função [**SetupPromptForDisk**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska) , se for necessário inserir uma nova mídia.</span><span class="sxs-lookup"><span data-stu-id="bbbdc-126">Your callback function should ensure that the cabinet is accessible before it returns, calling the [**SetupPromptForDisk**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska) function, if new media needs to be inserted.</span></span>

## <a name="requirements"></a><span data-ttu-id="bbbdc-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bbbdc-127">Requirements</span></span>



| <span data-ttu-id="bbbdc-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="bbbdc-128">Requirement</span></span> | <span data-ttu-id="bbbdc-129">Valor</span><span class="sxs-lookup"><span data-stu-id="bbbdc-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bbbdc-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bbbdc-130">Minimum supported client</span></span><br/> | <span data-ttu-id="bbbdc-131">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="bbbdc-131">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="bbbdc-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bbbdc-132">Minimum supported server</span></span><br/> | <span data-ttu-id="bbbdc-133">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="bbbdc-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bbbdc-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bbbdc-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="bbbdc-135"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="bbbdc-135"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bbbdc-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="bbbdc-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bbbdc-137">Visão geral</span><span class="sxs-lookup"><span data-stu-id="bbbdc-137">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="bbbdc-138">Notificações</span><span class="sxs-lookup"><span data-stu-id="bbbdc-138">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="bbbdc-139">**informações do gabinete \_**</span><span class="sxs-lookup"><span data-stu-id="bbbdc-139">**CABINET\_INFO**</span></span>](/windows/desktop/api/Setupapi/ns-setupapi-cabinet_info_a)
</dt> <dt>

[<span data-ttu-id="bbbdc-140">**SetupIterateCabinet**</span><span class="sxs-lookup"><span data-stu-id="bbbdc-140">**SetupIterateCabinet**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta)
</dt> </dl>

 

