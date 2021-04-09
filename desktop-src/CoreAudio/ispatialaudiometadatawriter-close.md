---
description: Conclui todas as operações necessárias no buffer de metadados e libera o objeto ISpatialAudioMetadataItems especificado.
ms.assetid: 2417E624-6535-49E2-9CF4-F927F731BE41
title: 'Método ISpatialAudioMetadataWriter:: Close'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISpatialAudioMetadataWriter.Close
api_type:
- COM
api_location:
- spatialaudiometadata.h
ms.openlocfilehash: 719c0d156c616c623d3e9a0d8a78620b735a7151
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089452"
---
# <a name="ispatialaudiometadatawriterclose-method"></a><span data-ttu-id="c9550-103">Método ISpatialAudioMetadataWriter:: Close</span><span class="sxs-lookup"><span data-stu-id="c9550-103">ISpatialAudioMetadataWriter::Close method</span></span>

<span data-ttu-id="c9550-104">Conclui todas as operações necessárias no buffer de metadados e libera o objeto [**ISpatialAudioMetadataItems**](/windows/desktop/api/SpatialAudioMetadata/nn-spatialaudiometadata-ispatialaudiometadataitems) especificado.</span><span class="sxs-lookup"><span data-stu-id="c9550-104">Completes any needed operations on the metadata buffer and releases the specified [**ISpatialAudioMetadataItems**](/windows/desktop/api/SpatialAudioMetadata/nn-spatialaudiometadata-ispatialaudiometadataitems) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9550-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c9550-105">Syntax</span></span>


```C++
HRESULT Close();
```



## <a name="parameters"></a><span data-ttu-id="c9550-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c9550-106">Parameters</span></span>

<span data-ttu-id="c9550-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="c9550-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c9550-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c9550-108">Return value</span></span>

<span data-ttu-id="c9550-109">Se o método for bem sucedido, ele retornará S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c9550-109">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="c9550-110">Se falhar, os códigos de retorno possíveis incluem, mas não se limitam a, os valores mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="c9550-110">If it fails, possible return codes include, but are not limited to, the values shown in the following table.</span></span>



| <span data-ttu-id="c9550-111">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="c9550-111">Return code</span></span>                                                                                                                     | <span data-ttu-id="c9550-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="c9550-112">Description</span></span>                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c9550-113"><dt>**SPTLAUD \_ MD \_ CLNT \_ E \_ nenhum \_ item \_ aberto**</dt></span><span class="sxs-lookup"><span data-stu-id="c9550-113"><dt>**SPTLAUD\_MD\_CLNT\_E\_NO\_ITEMS\_OPEN**</dt></span></span> </dl>            | <span data-ttu-id="c9550-114">O [**ISpatialAudioMetadataItems**](/windows/desktop/api/SpatialAudioMetadata/nn-spatialaudiometadata-ispatialaudiometadataitems) fornecido não foi aberto com uma chamada para [**Open**](/windows/desktop/api/SpatialAudioMetadata/nf-spatialaudiometadata-ispatialaudiometadatawriter-open).</span><span class="sxs-lookup"><span data-stu-id="c9550-114">The supplied [**ISpatialAudioMetadataItems**](/windows/desktop/api/SpatialAudioMetadata/nn-spatialaudiometadata-ispatialaudiometadataitems) has not been opened with a call to [**Open**](/windows/desktop/api/SpatialAudioMetadata/nf-spatialaudiometadata-ispatialaudiometadatawriter-open).</span></span><br/> |
| <dl> <span data-ttu-id="c9550-115"><dt>**SPTLAUD \_ MD \_ CLNT \_ E \_ nenhum \_ item \_ gravado**</dt></span><span class="sxs-lookup"><span data-stu-id="c9550-115"><dt>**SPTLAUD\_MD\_CLNT\_E\_NO\_ITEMS\_WRITTEN**</dt></span></span> </dl>         | <span data-ttu-id="c9550-116">Nenhum item de metadados foi gravado no [**ISpatialAudioMetadataItems**](/windows/desktop/api/SpatialAudioMetadata/nn-spatialaudiometadata-ispatialaudiometadataitems)fornecido.</span><span class="sxs-lookup"><span data-stu-id="c9550-116">No metadata items have been written to the supplied [**ISpatialAudioMetadataItems**](/windows/desktop/api/SpatialAudioMetadata/nn-spatialaudiometadata-ispatialaudiometadataitems).</span></span><br/>                                              |
| <dl> <span data-ttu-id="c9550-117"><dt>**SPTLAUD \_ MD \_ CLNT \_ E \_ item \_ deve \_ ter \_ comandos**</dt></span><span class="sxs-lookup"><span data-stu-id="c9550-117"><dt>**SPTLAUD\_MD\_CLNT\_E\_ITEM\_MUST\_HAVE\_COMMANDS**</dt></span></span> </dl> | <span data-ttu-id="c9550-118">Nenhum comando de metadados foi gravado no [**ISpatialAudioMetadataItems**](/windows/desktop/api/SpatialAudioMetadata/nn-spatialaudiometadata-ispatialaudiometadataitems)fornecido.</span><span class="sxs-lookup"><span data-stu-id="c9550-118">No metadata commands have been written to the supplied [**ISpatialAudioMetadataItems**](/windows/desktop/api/SpatialAudioMetadata/nn-spatialaudiometadata-ispatialaudiometadataitems).</span></span><br/>                                           |



 

## <a name="see-also"></a><span data-ttu-id="c9550-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="c9550-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9550-120">**ISpatialAudioMetadataWriter**</span><span class="sxs-lookup"><span data-stu-id="c9550-120">**ISpatialAudioMetadataWriter**</span></span>](/windows/desktop/api/SpatialAudioMetadata/nn-spatialaudiometadata-ispatialaudiometadatawriter)
</dt> </dl>

 

 




