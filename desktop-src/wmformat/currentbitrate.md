---
title: CurrentBitrate
description: O atributo CurrentBitrate contém a taxa de bits total atual dos fluxos ativos no arquivo.
ms.assetid: 961f36d5-a408-40d9-9ca1-0ed7c484858f
keywords:
- Formato de mídia do Windows CurrentBitrate
topic_type:
- apiref
api_name:
- CurrentBitrate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdcd8db7d60c65bcb7ceedcac4498ac650f90d9a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "105808273"
---
# <a name="currentbitrate"></a><span data-ttu-id="5a92f-104">CurrentBitrate</span><span class="sxs-lookup"><span data-stu-id="5a92f-104">CurrentBitrate</span></span>

<span data-ttu-id="5a92f-105">O atributo CurrentBitrate contém a taxa de bits total atual dos fluxos ativos no arquivo.</span><span class="sxs-lookup"><span data-stu-id="5a92f-105">The CurrentBitrate attribute contains the current total bit rate of the active streams in the file.</span></span>

## <a name="global-constant"></a><span data-ttu-id="5a92f-106">Constante global</span><span class="sxs-lookup"><span data-stu-id="5a92f-106">Global Constant</span></span>

<span data-ttu-id="5a92f-107">g \_ wszWMCurrentBitrate</span><span class="sxs-lookup"><span data-stu-id="5a92f-107">g\_wszWMCurrentBitrate</span></span>

## <a name="data-type"></a><span data-ttu-id="5a92f-108">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="5a92f-108">Data Type</span></span>

<span data-ttu-id="5a92f-109">**WMT \_ tipo \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="5a92f-109">**WMT\_TYPE\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="5a92f-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="5a92f-110">Remarks</span></span>

<span data-ttu-id="5a92f-111">Este é um atributo codificado.</span><span class="sxs-lookup"><span data-stu-id="5a92f-111">This is a coded attribute.</span></span>

<span data-ttu-id="5a92f-112">O valor recuperado para **CurrentBitrate** é diferente, dependendo do objeto usado.</span><span class="sxs-lookup"><span data-stu-id="5a92f-112">The value retrieved for **CurrentBitrate** is different depending upon the object used.</span></span> <span data-ttu-id="5a92f-113">No objeto leitor ou leitor síncrono, o valor é a taxa de bits real no momento da chamada.</span><span class="sxs-lookup"><span data-stu-id="5a92f-113">In the reader or synchronous reader object, the value is the actual bit rate at the time of the call.</span></span> <span data-ttu-id="5a92f-114">No objeto editor de metadados, o valor é a taxa média de bits do arquivo.</span><span class="sxs-lookup"><span data-stu-id="5a92f-114">In the metadata editor object, the value is the average bit rate of the file.</span></span>

<span data-ttu-id="5a92f-115">A taxa de bits real de um arquivo é igual às taxas de bits de todos os fluxos ativos mais alguma sobrecarga.</span><span class="sxs-lookup"><span data-stu-id="5a92f-115">The actual bit rate of a file is equal to the bit rates of all active streams plus some overhead.</span></span> <span data-ttu-id="5a92f-116">Esse é o valor que é, por exemplo, exibido ao reproduzir um arquivo com o Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="5a92f-116">This is the value that is, for example, displayed when playing a file with the Windows Media Player.</span></span>

<span data-ttu-id="5a92f-117">Este atributo não pode ser duplicado no nível do arquivo.</span><span class="sxs-lookup"><span data-stu-id="5a92f-117">This attribute cannot be duplicated at the file level.</span></span> <span data-ttu-id="5a92f-118">Se esse atributo for usado para um fluxo individual, ele será tratado como metadados personalizados e não transmitirá seu significado normal para os objetos do SDK do Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="5a92f-118">If this attribute is used for an individual stream, it will be treated as custom metadata and will not convey its normal meaning to the objects of the Windows Media Format SDK.</span></span>

## <a name="see-also"></a><span data-ttu-id="5a92f-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="5a92f-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a92f-120">**Lista de Atributos**</span><span class="sxs-lookup"><span data-stu-id="5a92f-120">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




