---
description: Coloca o formulário original do Word no objeto IWordFormSink.
ms.assetid: 333A3109-6C0A-42AE-9E10-87F53C7F737C
title: 'IWordFormSink: método utWord de:P (Search. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordFormSink.PutWord
api_type:
- COM
api_location:
- search.h
ms.openlocfilehash: 438cb41e50f264bd373ae2ef8e84598b651b0352
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105763279"
---
# <a name="iwordformsinkputword-method"></a><span data-ttu-id="df367-103">IWordFormSink: método utWord de:P</span><span class="sxs-lookup"><span data-stu-id="df367-103">IWordFormSink::PutWord method</span></span>

<span data-ttu-id="df367-104">Coloca o formulário original do Word no objeto [**IWordFormSink**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink) .</span><span class="sxs-lookup"><span data-stu-id="df367-104">Puts the original word form in the [**IWordFormSink**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="df367-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="df367-105">Syntax</span></span>


```C++
HRESULT PutWord(
  [in] const WCHAR *pwcInBuf ,
  [in]       ULONG cwc
);
```



## <a name="parameters"></a><span data-ttu-id="df367-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="df367-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df367-107">*pwcInBuf* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="df367-107">*pwcInBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df367-108">Um ponteiro para um buffer que contém a forma alternativa final de uma palavra, que é sempre a palavra original.</span><span class="sxs-lookup"><span data-stu-id="df367-108">A pointer to a buffer that contains the final alternative form of a word, which is always the original word.</span></span>

</dd> <dt>

<span data-ttu-id="df367-109">*CWC* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="df367-109">*cwc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df367-110">O número de caracteres em *pwcInBuf*.</span><span class="sxs-lookup"><span data-stu-id="df367-110">The number of characters in *pwcInBuf*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df367-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="df367-111">Return value</span></span>

<span data-ttu-id="df367-112">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="df367-112">This method can return one of these values.</span></span>



| <span data-ttu-id="df367-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="df367-113">Return code</span></span>                                                                          | <span data-ttu-id="df367-114">Description</span><span class="sxs-lookup"><span data-stu-id="df367-114">Description</span></span>                                           |
|--------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <span data-ttu-id="df367-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="df367-115"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="df367-116">A operação foi concluída com êxito.</span><span class="sxs-lookup"><span data-stu-id="df367-116">The operation was completed successfully.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="df367-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="df367-117">Remarks</span></span>

<span data-ttu-id="df367-118">**PutWord** é chamado do método [**GenerateWordForms**](/windows/win32/api/indexsrv/nf-indexsrv-istemmer-generatewordforms) da implementação [**IStemmer**](/windows/win32/api/indexsrv/nn-indexsrv-istemmer) .</span><span class="sxs-lookup"><span data-stu-id="df367-118">**PutWord** is called from the [**GenerateWordForms**](/windows/win32/api/indexsrv/nf-indexsrv-istemmer-generatewordforms) method of the [**IStemmer**](/windows/win32/api/indexsrv/nn-indexsrv-istemmer) implementation.</span></span> <span data-ttu-id="df367-119">Esse método manipula a forma original de uma palavra e é chamado por último.</span><span class="sxs-lookup"><span data-stu-id="df367-119">This method handles the original form of a word and is called last.</span></span> <span data-ttu-id="df367-120">Todos os formulários alternativos anteriores para uma palavra são colocados no objeto [**IWordFormSink**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink) chamando [**IWordFormSink::P utaltword**](iwordformsink-putphrase.md).</span><span class="sxs-lookup"><span data-stu-id="df367-120">All preceding alternative forms for a word are put in the [**IWordFormSink**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink) object by calling [**IWordFormSink::PutAltWord**](iwordformsink-putphrase.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="df367-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="df367-121">Requirements</span></span>



| <span data-ttu-id="df367-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="df367-122">Requirement</span></span> | <span data-ttu-id="df367-123">Valor</span><span class="sxs-lookup"><span data-stu-id="df367-123">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="df367-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="df367-124">Minimum supported client</span></span><br/> | <span data-ttu-id="df367-125">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="df367-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="df367-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="df367-126">Minimum supported server</span></span><br/> | <span data-ttu-id="df367-127">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="df367-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="df367-128">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="df367-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="df367-129"><dt>Pesquisar. h</dt></span><span class="sxs-lookup"><span data-stu-id="df367-129"><dt>Search.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df367-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="df367-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df367-131">**IWordFormSink**</span><span class="sxs-lookup"><span data-stu-id="df367-131">**IWordFormSink**</span></span>](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink)
</dt> </dl>

 

 
