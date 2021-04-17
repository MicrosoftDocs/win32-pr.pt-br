---
description: A \_ notificação FILEextraíted do SPFILENOTIFY é enviada a uma rotina de retorno de chamada por SetupIterateCabinet para indicar que um arquivo foi extraído do gabinete ou que uma extração falhou e o processamento do gabinete foi cancelado.
ms.assetid: 70ffe06c-e72d-4bb8-a13c-e2946ff72fa6
title: Mensagem de SPFILENOTIFY_FILEEXTRACTED (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efdd66c7f218e632ba817d00a6e6c9447052e350
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105749443"
---
# <a name="spfilenotify_fileextracted-message"></a><span data-ttu-id="a8217-103">SPFILENOTIFY \_ extracçãod Message</span><span class="sxs-lookup"><span data-stu-id="a8217-103">SPFILENOTIFY\_FILEEXTRACTED message</span></span>

<span data-ttu-id="a8217-104">A **notificação \_ fileextraíted do SPFILENOTIFY** é enviada a uma rotina de retorno de chamada por [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) para indicar que um arquivo foi extraído do gabinete ou que uma extração falhou e o processamento do gabinete foi cancelado.</span><span class="sxs-lookup"><span data-stu-id="a8217-104">The **SPFILENOTIFY\_FILEEXTRACTED** notification is sent to a callback routine by [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) to indicate either that a file was extracted from the cabinet or that an extraction failed and cabinet processing has been canceled.</span></span>


```C++
SPFILENOTIFY_FILEEXTRACTED
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a><span data-ttu-id="a8217-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a8217-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8217-106">*Param1*</span><span class="sxs-lookup"><span data-stu-id="a8217-106">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="a8217-107">Ponteiro [**para uma estrutura de arquivo**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) de dados que contém informações de caminho para o arquivos extraídos.</span><span class="sxs-lookup"><span data-stu-id="a8217-107">Pointer to a [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) structure that contains path information for the extracted file.</span></span> <span data-ttu-id="a8217-108">O membro **SourceFile** da estrutura **filePaths** contém o caminho de origem completo do gabinete.</span><span class="sxs-lookup"><span data-stu-id="a8217-108">The **SourceFile** member of the **FILEPATHS** structure contains the full source path of the cabinet.</span></span> <span data-ttu-id="a8217-109">O membro **TargetFile** fornece o caminho de destino completo do arquivo a ser instalado no sistema.</span><span class="sxs-lookup"><span data-stu-id="a8217-109">The **TargetFile** member supplies the full target path of the file to be installed on the system.</span></span>

</dd> <dt>

<span data-ttu-id="a8217-110">*Param2*</span><span class="sxs-lookup"><span data-stu-id="a8217-110">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="a8217-111">Não utilizado.</span><span class="sxs-lookup"><span data-stu-id="a8217-111">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8217-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a8217-112">Return value</span></span>

<span data-ttu-id="a8217-113">A rotina de retorno de chamada do gabinete deve retornar um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="a8217-113">The cabinet callback routine should return one of the following values.</span></span>



| <span data-ttu-id="a8217-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="a8217-114">Return code</span></span>                                                                               | <span data-ttu-id="a8217-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="a8217-115">Description</span></span>                                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a8217-116"><dt>**SEM \_ erros**</dt></span><span class="sxs-lookup"><span data-stu-id="a8217-116"><dt>**NO\_ERROR**</dt></span></span> </dl>  | <span data-ttu-id="a8217-117">Nenhum erro foi encontrado, continue processando o gabinete.</span><span class="sxs-lookup"><span data-stu-id="a8217-117">No error was encountered, continue processing the cabinet.</span></span><br/>                                                                                                                                |
| <dl> <span data-ttu-id="a8217-118"><dt>**ERRO \_ xxx**</dt></span><span class="sxs-lookup"><span data-stu-id="a8217-118"><dt>**ERROR\_XXX**</dt></span></span> </dl> | <span data-ttu-id="a8217-119">Ocorreu um erro do tipo especificado.</span><span class="sxs-lookup"><span data-stu-id="a8217-119">An error of the specified type occurred.</span></span> <span data-ttu-id="a8217-120">[**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) retornará zero.</span><span class="sxs-lookup"><span data-stu-id="a8217-120">[**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) will return zero.</span></span> <span data-ttu-id="a8217-121">[**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retornará o código de erro especificado.</span><span class="sxs-lookup"><span data-stu-id="a8217-121">[**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) will return the specified error code.</span></span><br/> |



 

> [!Note]  
> <span data-ttu-id="a8217-122">Não há uma rotina de retorno de chamada de gabinete padrão fornecida com a API de instalação.</span><span class="sxs-lookup"><span data-stu-id="a8217-122">There is no default cabinet callback routine supplied with the Setup API.</span></span> <span data-ttu-id="a8217-123">O aplicativo de instalação deve fornecer uma rotina de retorno de chamada para manipular as notificações enviadas pela função [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) .</span><span class="sxs-lookup"><span data-stu-id="a8217-123">Your setup application should supply a callback routine to handle the notifications sent by the [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) function.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a8217-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a8217-124">Requirements</span></span>



| <span data-ttu-id="a8217-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8217-125">Requirement</span></span> | <span data-ttu-id="a8217-126">Valor</span><span class="sxs-lookup"><span data-stu-id="a8217-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a8217-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a8217-127">Minimum supported client</span></span><br/> | <span data-ttu-id="a8217-128">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="a8217-128">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="a8217-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a8217-129">Minimum supported server</span></span><br/> | <span data-ttu-id="a8217-130">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a8217-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a8217-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a8217-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="a8217-132"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="a8217-132"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8217-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="a8217-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8217-134">Visão geral</span><span class="sxs-lookup"><span data-stu-id="a8217-134">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="a8217-135">Notificações</span><span class="sxs-lookup"><span data-stu-id="a8217-135">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="a8217-136">**FILEPATHS**</span><span class="sxs-lookup"><span data-stu-id="a8217-136">**FILEPATHS**</span></span>](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)
</dt> <dt>

[<span data-ttu-id="a8217-137">**SetupIterateCabinet**</span><span class="sxs-lookup"><span data-stu-id="a8217-137">**SetupIterateCabinet**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta)
</dt> </dl>

 

