---
title: OptimalBitrate
description: O atributo OptimalBitrate contém a taxa de bits na qual o arquivo é melhor tocado.
ms.assetid: cd13b9b5-34d2-4ebb-9f10-3bf42dd9de81
keywords:
- Formato de mídia do Windows OptimalBitrate
topic_type:
- apiref
api_name:
- OptimalBitrate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff71c6b64cbc4bf4ccc4f346e62a5eae066e78ce
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "105782723"
---
# <a name="optimalbitrate"></a><span data-ttu-id="49fde-104">OptimalBitrate</span><span class="sxs-lookup"><span data-stu-id="49fde-104">OptimalBitrate</span></span>

<span data-ttu-id="49fde-105">O atributo **OptimalBitrate** contém a taxa de bits na qual o arquivo é melhor tocado.</span><span class="sxs-lookup"><span data-stu-id="49fde-105">The **OptimalBitrate** attribute contains the bit rate at which the file is best played.</span></span>

## <a name="global-constant"></a><span data-ttu-id="49fde-106">Constante global</span><span class="sxs-lookup"><span data-stu-id="49fde-106">Global Constant</span></span>

<span data-ttu-id="49fde-107">g \_ wszWMOptimalBitrate</span><span class="sxs-lookup"><span data-stu-id="49fde-107">g\_wszWMOptimalBitrate</span></span>

## <a name="data-type"></a><span data-ttu-id="49fde-108">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="49fde-108">Data Type</span></span>

<span data-ttu-id="49fde-109">**WMT \_ tipo \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="49fde-109">**WMT\_TYPE\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="49fde-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="49fde-110">Remarks</span></span>

<span data-ttu-id="49fde-111">Este é um atributo codificado.</span><span class="sxs-lookup"><span data-stu-id="49fde-111">This is a coded attribute.</span></span>

<span data-ttu-id="49fde-112">Para arquivos que contêm fluxos de taxa de bits variável (VBR), esse valor é a taxa de bits de pico para os fluxos no arquivo.</span><span class="sxs-lookup"><span data-stu-id="49fde-112">For files that contain variable bit rate (VBR) streams, this value is the peak bit rate for the streams in the file.</span></span> <span data-ttu-id="49fde-113">Para arquivos sem VBR, esse valor é o mesmo que [**taxa de bits**](bit-rate.md).</span><span class="sxs-lookup"><span data-stu-id="49fde-113">For files without VBR, this value is the same as [**Bitrate**](bit-rate.md).</span></span>

<span data-ttu-id="49fde-114">Este atributo não pode ser duplicado no nível do arquivo.</span><span class="sxs-lookup"><span data-stu-id="49fde-114">This attribute cannot be duplicated at the file level.</span></span> <span data-ttu-id="49fde-115">Se esse atributo for usado para um fluxo individual, ele será tratado como metadados personalizados e não transmitirá seu significado normal para os objetos do SDK do Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="49fde-115">If this attribute is used for an individual stream, it will be treated as custom metadata and will not convey its normal meaning to the objects of the Windows Media Format SDK.</span></span>

## <a name="see-also"></a><span data-ttu-id="49fde-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="49fde-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49fde-117">**Lista de Atributos**</span><span class="sxs-lookup"><span data-stu-id="49fde-117">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




