---
description: Sugere a política de segurança a ser aplicada ao navegador.
ms.assetid: 73541611-2024-4c33-ab03-e3204244c46c
title: 'Método IItemPreviewerExt:: SuggestBrowserPolicy'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IItemPreviewerExt.SuggestBrowserPolicy
api_type:
- COM
api_location: ''
ms.openlocfilehash: 0a4f248edbfa4a1779016e40d73051d8c1d9acac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104460986"
---
# <a name="iitempreviewerextsuggestbrowserpolicy-method"></a><span data-ttu-id="ef185-103">Método IItemPreviewerExt:: SuggestBrowserPolicy</span><span class="sxs-lookup"><span data-stu-id="ef185-103">IItemPreviewerExt::SuggestBrowserPolicy method</span></span>

<span data-ttu-id="ef185-104">Sugere a política de segurança a ser aplicada ao navegador.</span><span class="sxs-lookup"><span data-stu-id="ef185-104">Suggests the security policy to be applied to the browser.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef185-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ef185-105">Syntax</span></span>


```C++
HRESULT SuggestBrowserPolicy(
  [in]          DWORD dwContext,
  [out, retval] DWORD *pdwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="ef185-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ef185-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef185-107">*dwContext* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ef185-107">*dwContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef185-108">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="ef185-108">Type: **DWORD**</span></span>

<span data-ttu-id="ef185-109">O identificador de contexto para a operação.</span><span class="sxs-lookup"><span data-stu-id="ef185-109">The context identifier for the operation.</span></span> <span data-ttu-id="ef185-110">Substitua o padrão *dwContext* para definir o identificador de contexto como um valor de sua escolha.</span><span class="sxs-lookup"><span data-stu-id="ef185-110">Override the *dwContext* default to set the context identifier to a value of your choosing.</span></span>

</dd> <dt>

<span data-ttu-id="ef185-111">*pdwFlags* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="ef185-111">*pdwFlags* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="ef185-112">Tipo: \**DWORD \** _</span><span class="sxs-lookup"><span data-stu-id="ef185-112">Type: \**DWORD\** _</span></span>

<span data-ttu-id="ef185-113">Um ponteiro para um valor DWORD que contém sinalizadores de verificação de verificação.</span><span class="sxs-lookup"><span data-stu-id="ef185-113">A pointer to a DWORD value containing verification check flags.</span></span> <span data-ttu-id="ef185-114">O sinalizador _ *BROWSERPOLICY \_ \_ conteúdo não confiável*\* desabilita qualquer possibilidade de a visualização ser capaz de executar script ou ActiveX.</span><span class="sxs-lookup"><span data-stu-id="ef185-114">The _ *BROWSERPOLICY\_UNTRUSTED\_CONTENT*\* flag disables any possibility of the preview being able to run script or ActiveX.</span></span> <span data-ttu-id="ef185-115">O parâmetro *pdwFlags* não deve ser um ponteiro **nulo** .</span><span class="sxs-lookup"><span data-stu-id="ef185-115">The parameter *pdwFlags* must not be a **NULL** pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef185-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ef185-116">Return value</span></span>

<span data-ttu-id="ef185-117">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="ef185-117">Type: **HRESULT**</span></span>

<span data-ttu-id="ef185-118">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="ef185-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ef185-119">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ef185-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="ef185-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="ef185-120">Remarks</span></span>

<span data-ttu-id="ef185-121">A interface [**IItemPreviewerExt**](-search-iitempreviewerext.md) tem suporte apenas no Windows XP e no windows Server 2003 e não deve mais ser usada.</span><span class="sxs-lookup"><span data-stu-id="ef185-121">The [**IItemPreviewerExt**](-search-iitempreviewerext.md) interface is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

<span data-ttu-id="ef185-122">Para visualizar os anexos com um manipulador de protocolo de terceiros em computadores que executam o Windows XP ou o Windows Server 2003, pode ser necessário usar a interface [**IItemPreviewerExt**](-search-iitempreviewerext.md) e as seguintes APIs: as interfaces [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPropertyBag**](iitempropertybag.md) e [**ISearchItem**](-search-isearchitem.md) , a estrutura [**LINKINFO**](-search-linkinfo.md) e a enumeração [**LinkId**](-search-linktype.md) .</span><span class="sxs-lookup"><span data-stu-id="ef185-122">To preview attachments with a third-party protocol handler on computers running Windows XP or Windows Server 2003, it may be necessary to use the [**IItemPreviewerExt**](-search-iitempreviewerext.md) interface, and the following APIs: the [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPropertyBag**](iitempropertybag.md) and [**ISearchItem**](-search-isearchitem.md) interfaces, the [**LINKINFO**](-search-linkinfo.md) structure, and the [**LINKTYPE**](-search-linktype.md) enumeration.</span></span>

<span data-ttu-id="ef185-123">O uso do sinalizador de **\_ \_ conteúdo não confiável BROWSERPOLICY** é altamente recomendável para desabilitar qualquer possibilidade da visualização ser capaz de executar script ou ActiveX.</span><span class="sxs-lookup"><span data-stu-id="ef185-123">Using the **BROWSERPOLICY\_UNTRUSTED\_CONTENT** flag is strongly recommended to disable any possibility of the preview being able to run script or ActiveX.</span></span> <span data-ttu-id="ef185-124">O método **IItemPreviewerExt:: SuggestBrowserPolicy** pode retornar informações sobre se o item que está sendo visualizado é confiável ou não.</span><span class="sxs-lookup"><span data-stu-id="ef185-124">The **IItemPreviewerExt::SuggestBrowserPolicy** method can return information on whether the item being previewed is trusted or not.</span></span> <span data-ttu-id="ef185-125">Isso permitirá que o controle Trident do previsor execute o script e até controles ActiveX.</span><span class="sxs-lookup"><span data-stu-id="ef185-125">This will allow the previewer trident control to execute script, and even ActiveX controls.</span></span> <span data-ttu-id="ef185-126">Como o pré-visor geralmente usa arquivos temporários para gerar a visualização, fazer isso pode resultar em execução de código e script inesperado na zona do computador local.</span><span class="sxs-lookup"><span data-stu-id="ef185-126">Because the previewer often uses temporary files to generate the preview, doing so can result in unexpected script and code execution in the Local Computer zone.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef185-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ef185-127">Requirements</span></span>



| <span data-ttu-id="ef185-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="ef185-128">Requirement</span></span> | <span data-ttu-id="ef185-129">Valor</span><span class="sxs-lookup"><span data-stu-id="ef185-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ef185-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ef185-130">Minimum supported client</span></span><br/> | <span data-ttu-id="ef185-131">\[Somente aplicativos de área de trabalho do Windows XP com SP2\]</span><span class="sxs-lookup"><span data-stu-id="ef185-131">Windows XP with SP2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="ef185-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ef185-132">Minimum supported server</span></span><br/> | <span data-ttu-id="ef185-133">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ef185-133">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="ef185-134">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="ef185-134">Redistributable</span></span><br/>          | <span data-ttu-id="ef185-135">Windows Desktop Search (WDS) 3,0</span><span class="sxs-lookup"><span data-stu-id="ef185-135">Windows Desktop Search (WDS) 3.0</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="ef185-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="ef185-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef185-137">**IItemPreviewerExt**</span><span class="sxs-lookup"><span data-stu-id="ef185-137">**IItemPreviewerExt**</span></span>](-search-iitempreviewerext.md)
</dt> </dl>

 

 




