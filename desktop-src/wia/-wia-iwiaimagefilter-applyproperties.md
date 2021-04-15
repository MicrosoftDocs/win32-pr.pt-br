---
description: Permite que o filtro de processamento de imagens grave Propriedades de volta para o driver (e dispositivo).
ms.assetid: b9bb8d81-2945-46ba-a0a2-7009000574aa
title: 'Método IWiaImageFilter:: Applyproperties (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaImageFilter.ApplyProperties
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 3c20527ee587b975adea34e7c480349836620015
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105768387"
---
# <a name="iwiaimagefilterapplyproperties-method"></a><span data-ttu-id="39bdb-103">Método IWiaImageFilter:: Applyproperties</span><span class="sxs-lookup"><span data-stu-id="39bdb-103">IWiaImageFilter::ApplyProperties method</span></span>

<span data-ttu-id="39bdb-104">Permite que o filtro de processamento de imagens grave Propriedades de volta para o driver (e dispositivo).</span><span class="sxs-lookup"><span data-stu-id="39bdb-104">Enables the image processing filter to write properties back to the driver (and device).</span></span>

## <a name="syntax"></a><span data-ttu-id="39bdb-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="39bdb-105">Syntax</span></span>


```C++
HRESULT ApplyProperties(
  [in] IWiaPropertyStorage *pWiaPropertyStorage
);
```



## <a name="parameters"></a><span data-ttu-id="39bdb-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="39bdb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39bdb-107">*pWiaPropertyStorage* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="39bdb-107">*pWiaPropertyStorage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39bdb-108">Tipo: \**[**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) \** _</span><span class="sxs-lookup"><span data-stu-id="39bdb-108">Type: \**[**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage)\** _</span></span>

<span data-ttu-id="39bdb-109">Especifica um ponteiro para o [_ *IWiaPropertyStorage* \*](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) para as propriedades a serem aplicadas.</span><span class="sxs-lookup"><span data-stu-id="39bdb-109">Specifies a pointer to the [_ *IWiaPropertyStorage*\*](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) for the properties to be applied.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39bdb-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="39bdb-110">Return value</span></span>

<span data-ttu-id="39bdb-111">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="39bdb-111">Type: **HRESULT**</span></span>

<span data-ttu-id="39bdb-112">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="39bdb-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="39bdb-113">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="39bdb-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="39bdb-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="39bdb-114">Remarks</span></span>

<span data-ttu-id="39bdb-115">Não chame esse método diretamente do seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="39bdb-115">Do not call this method directly from your application.</span></span> <span data-ttu-id="39bdb-116">Ele é chamado pela aquisição de imagem do Windows (WIA) 2,0 depois que o filtro de processamento de imagem processou os dados brutos.</span><span class="sxs-lookup"><span data-stu-id="39bdb-116">It is called by Windows Image Acquisition (WIA) 2.0 after the image processing filter has processed the raw data.</span></span>

<span data-ttu-id="39bdb-117">*pWiaPropertyStorage* é a interface [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) na qual o filtro de processamento de imagem deve gravar propriedades.</span><span class="sxs-lookup"><span data-stu-id="39bdb-117">*pWiaPropertyStorage* is the [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) interface into which the image processing filter should write properties.</span></span> <span data-ttu-id="39bdb-118">Um filtro de processamento de imagem deve usar apenas o método [IPropertyStorage:: WriteMultiple](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-writemultiple) para gravar propriedades.</span><span class="sxs-lookup"><span data-stu-id="39bdb-118">An image processing filter should use only the [IPropertyStorage::WriteMultiple](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-writemultiple) method to write properties.</span></span>

<span data-ttu-id="39bdb-119">Esse método permite que o filtro de processamento de imagens grave Propriedades de volta para o driver (e dispositivo).</span><span class="sxs-lookup"><span data-stu-id="39bdb-119">This method allows the image processing filter to write properties back to the driver (and device).</span></span> <span data-ttu-id="39bdb-120">Isso pode ser necessário para filtros que implementam recursos como a exposição automática durante a verificação de filmes.</span><span class="sxs-lookup"><span data-stu-id="39bdb-120">This may be necessary for filters that implement features such as auto-exposure during film scanning.</span></span>

## <a name="requirements"></a><span data-ttu-id="39bdb-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="39bdb-121">Requirements</span></span>



| <span data-ttu-id="39bdb-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="39bdb-122">Requirement</span></span> | <span data-ttu-id="39bdb-123">Valor</span><span class="sxs-lookup"><span data-stu-id="39bdb-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="39bdb-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="39bdb-124">Minimum supported client</span></span><br/> | <span data-ttu-id="39bdb-125">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="39bdb-125">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="39bdb-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="39bdb-126">Minimum supported server</span></span><br/> | <span data-ttu-id="39bdb-127">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="39bdb-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="39bdb-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="39bdb-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="39bdb-129"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="39bdb-129"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="39bdb-130">INSERI</span><span class="sxs-lookup"><span data-stu-id="39bdb-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="39bdb-131"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="39bdb-131"><dt>Wia.idl</dt></span></span> </dl> |



 

 
