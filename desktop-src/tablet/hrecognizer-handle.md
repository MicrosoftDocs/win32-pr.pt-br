---
description: Um identificador HRECOGNIZER é usado para criar um contexto de reconhecedor, recuperar os atributos e as propriedades do reconhecedor e determinar quais propriedades de pacote o reconhecedor exige para executar o reconhecimento.
ms.assetid: 1fc1901e-8c4d-4ef1-8c38-52d46ce10a48
title: Identificador HRECOGNIZER (recapitular. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e78086ff86453ef8b0157bb3b274f3c47be0dc0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296398"
---
# <a name="hrecognizer-handle"></a><span data-ttu-id="0cd87-103">Identificador de HRECOGNIZER</span><span class="sxs-lookup"><span data-stu-id="0cd87-103">HRECOGNIZER Handle</span></span>

<span data-ttu-id="0cd87-104">Um identificador **HRECOGNIZER** é usado para criar um contexto de reconhecedor, recuperar os atributos e as propriedades do reconhecedor e determinar quais propriedades de pacote o reconhecedor exige para executar o reconhecimento.</span><span class="sxs-lookup"><span data-stu-id="0cd87-104">An **HRECOGNIZER** handle is used to create a recognizer context, retrieve the recognizer's attributes and properties, and determine which packet properties the recognizer requires to perform recognition.</span></span>


```C++
typedef HANDLE HRECOGNIZER;
```



## <a name="remarks"></a><span data-ttu-id="0cd87-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="0cd87-105">Remarks</span></span>

<span data-ttu-id="0cd87-106">As funções a seguir usam um **HRECOGNIZER**.</span><span class="sxs-lookup"><span data-stu-id="0cd87-106">The following functions use an **HRECOGNIZER**.</span></span>



| <span data-ttu-id="0cd87-107">Função</span><span class="sxs-lookup"><span data-stu-id="0cd87-107">Function</span></span>                                                               | <span data-ttu-id="0cd87-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="0cd87-108">Description</span></span>                                                                                        |
|------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0cd87-109">**Recognizer**</span><span class="sxs-lookup"><span data-stu-id="0cd87-109">**CreateRecognizer**</span></span>](/windows/desktop/api/recapis/nf-recapis-createrecognizer)                           | <span data-ttu-id="0cd87-110">Cria um reconhecedor.</span><span class="sxs-lookup"><span data-stu-id="0cd87-110">Creates a recognizer.</span></span><br/>                                                                   |
| [<span data-ttu-id="0cd87-111">**DestroyRecognizer**</span><span class="sxs-lookup"><span data-stu-id="0cd87-111">**DestroyRecognizer**</span></span>](/windows/desktop/api/recapis/nf-recapis-destroyrecognizer)                         | <span data-ttu-id="0cd87-112">Destrói um reconhecedor.</span><span class="sxs-lookup"><span data-stu-id="0cd87-112">Destroys a recognizer.</span></span><br/>                                                                  |
| [<span data-ttu-id="0cd87-113">**GetRecoAttributes**</span><span class="sxs-lookup"><span data-stu-id="0cd87-113">**GetRecoAttributes**</span></span>](/windows/desktop/api/recapis/nf-recapis-getrecoattributes)                         | <span data-ttu-id="0cd87-114">Retorna os atributos do reconhecedor.</span><span class="sxs-lookup"><span data-stu-id="0cd87-114">Returns the attributes of the recognizer.</span></span><br/>                                               |
| [<span data-ttu-id="0cd87-115">**CreateContext**</span><span class="sxs-lookup"><span data-stu-id="0cd87-115">**CreateContext**</span></span>](/windows/desktop/api/recapis/nf-recapis-createcontext)                                 | <span data-ttu-id="0cd87-116">Cria um contexto de reconhecedor.</span><span class="sxs-lookup"><span data-stu-id="0cd87-116">Creates a recognizer context.</span></span><br/>                                                           |
| [<span data-ttu-id="0cd87-117">**DestroyContext**</span><span class="sxs-lookup"><span data-stu-id="0cd87-117">**DestroyContext**</span></span>](/windows/desktop/api/recapis/nf-recapis-destroycontext)                               | <span data-ttu-id="0cd87-118">Destrói um contexto de reconhecedor.</span><span class="sxs-lookup"><span data-stu-id="0cd87-118">Destroys a recognizer context.</span></span><br/>                                                          |
| [<span data-ttu-id="0cd87-119">**GetAllRecognizers**</span><span class="sxs-lookup"><span data-stu-id="0cd87-119">**GetAllRecognizers**</span></span>](/windows/desktop/api/recapis/nf-recapis-getallrecognizers)                         | <span data-ttu-id="0cd87-120">Obtém todos os reconhecedores.</span><span class="sxs-lookup"><span data-stu-id="0cd87-120">Gets all recognizers.</span></span><br/>                                                                   |
| [<span data-ttu-id="0cd87-121">**GetResultPropertyList**</span><span class="sxs-lookup"><span data-stu-id="0cd87-121">**GetResultPropertyList**</span></span>](/windows/desktop/api/recapis/nf-recapis-getresultpropertylist)                 | <span data-ttu-id="0cd87-122">Recupera uma lista de propriedades que o reconhecedor pode retornar para um intervalo de resultados.</span><span class="sxs-lookup"><span data-stu-id="0cd87-122">Retrieves a list of properties the recognizer can return for a result range.</span></span><br/>            |
| [<span data-ttu-id="0cd87-123">**GetPreferredPacketDescription**</span><span class="sxs-lookup"><span data-stu-id="0cd87-123">**GetPreferredPacketDescription**</span></span>](/windows/desktop/api/recapis/nf-recapis-getpreferredpacketdescription) | <span data-ttu-id="0cd87-124">Recupera uma descrição de pacote que contém as propriedades de pacote que o reconhecedor usa.</span><span class="sxs-lookup"><span data-stu-id="0cd87-124">Retrieves a packet description that contains the packet properties the recognizer uses.</span></span><br/> |
| [<span data-ttu-id="0cd87-125">**GetUnicodeRanges**</span><span class="sxs-lookup"><span data-stu-id="0cd87-125">**GetUnicodeRanges**</span></span>](/windows/desktop/api/recapis/nf-recapis-getunicoderanges)                           | <span data-ttu-id="0cd87-126">Recupera os intervalos de pontos Unicode que o reconhecedor dá suporte.</span><span class="sxs-lookup"><span data-stu-id="0cd87-126">Retrieves the ranges of Unicode points that the recognizer supports.</span></span><br/>                    |
| [<span data-ttu-id="0cd87-127">**LoadCachedAttributes**</span><span class="sxs-lookup"><span data-stu-id="0cd87-127">**LoadCachedAttributes**</span></span>](/windows/desktop/api/recapis/nf-recapis-loadcachedattributes)                   | <span data-ttu-id="0cd87-128">Carrega os atributos armazenados em cache de um reconhecedor.</span><span class="sxs-lookup"><span data-stu-id="0cd87-128">Loads the cached attributes of a recognizer.</span></span><br/>                                            |



 

## <a name="requirements"></a><span data-ttu-id="0cd87-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0cd87-129">Requirements</span></span>



| <span data-ttu-id="0cd87-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="0cd87-130">Requirement</span></span> | <span data-ttu-id="0cd87-131">Valor</span><span class="sxs-lookup"><span data-stu-id="0cd87-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="0cd87-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0cd87-132">Minimum supported client</span></span><br/> | <span data-ttu-id="0cd87-133">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="0cd87-133">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                        |
| <span data-ttu-id="0cd87-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0cd87-134">Minimum supported server</span></span><br/> | <span data-ttu-id="0cd87-135">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="0cd87-135">None supported</span></span><br/>                                                            |
| <span data-ttu-id="0cd87-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0cd87-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="0cd87-137"><dt>Recapitular. h</dt></span><span class="sxs-lookup"><span data-stu-id="0cd87-137"><dt>Recapis.h</dt></span></span> </dl> |



 

 




