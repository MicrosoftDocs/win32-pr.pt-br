---
title: Enumeração HeaderDisplayStyle
description: Usado por IResultsViewer HeaderStyle para definir ou retornar o estilo de cabeçalho atual.
ms.assetid: 13ae6317-d990-4ccf-83b3-275caf953611
keywords:
- Recursos do ambiente Windows herdado de enumeração HeaderDisplayStyle
topic_type:
- apiref
api_name:
- HeaderDisplayStyle
api_location:
- WdsView.idl
api_type:
- IDLDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc65b17fa61b799fc9ab8ea7cc1b01380a5843c7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761062"
---
# <a name="headerdisplaystyle-enumeration"></a><span data-ttu-id="00495-104">Enumeração HeaderDisplayStyle</span><span class="sxs-lookup"><span data-stu-id="00495-104">HeaderDisplayStyle enumeration</span></span>

> [!NOTE]
> <span data-ttu-id="00495-105">O Windows Desktop Search 2. x é uma tecnologia obsoleta que originalmente estava disponível como um suplemento para o Windows XP e o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="00495-105">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="00495-106">Em versões posteriores, use a [API de pesquisa do Windows](../search/-search-reference-entry-page.md) em vez disso.</span><span class="sxs-lookup"><span data-stu-id="00495-106">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="00495-107">Usado por [**IResultsViewer:: HeaderStyle**](-search-2x-iresultsviewer-headerstyle.md) para definir ou retornar o estilo de cabeçalho atual.</span><span class="sxs-lookup"><span data-stu-id="00495-107">Used by [**IResultsViewer::HeaderStyle**](-search-2x-iresultsviewer-headerstyle.md) to set or return the current header style.</span></span>

## <a name="syntax"></a><span data-ttu-id="00495-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="00495-108">Syntax</span></span>


```C++
typedef enum HeaderDisplayStyleEnum { 
  FullHeader     = 0,
  CompactHeader  = 1,
  NoHeader       = 2
} HeaderDisplayStyle;
```



## <a name="constants"></a><span data-ttu-id="00495-109">Constantes</span><span class="sxs-lookup"><span data-stu-id="00495-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="00495-110"><span id="FullHeader"></span><span id="fullheader"></span><span id="FULLHEADER"></span>**FullHeader**</span><span class="sxs-lookup"><span data-stu-id="00495-110"><span id="FullHeader"></span><span id="fullheader"></span><span id="FULLHEADER"></span>**FullHeader**</span></span>
</dt> <dd>

<span data-ttu-id="00495-111">Indica ou define o uso de cabeçalhos completos.</span><span class="sxs-lookup"><span data-stu-id="00495-111">Indicates or sets the use of full headers.</span></span>

</dd> <dt>

<span data-ttu-id="00495-112"><span id="CompactHeader"></span><span id="compactheader"></span><span id="COMPACTHEADER"></span>**CompactHeader**</span><span class="sxs-lookup"><span data-stu-id="00495-112"><span id="CompactHeader"></span><span id="compactheader"></span><span id="COMPACTHEADER"></span>**CompactHeader**</span></span>
</dt> <dd>

<span data-ttu-id="00495-113">Indica ou define o uso de cabeçalhos de compactação.</span><span class="sxs-lookup"><span data-stu-id="00495-113">Indicates or sets the use of compact headers.</span></span>

</dd> <dt>

<span data-ttu-id="00495-114"><span id="NoHeader"></span><span id="noheader"></span><span id="NOHEADER"></span>**Noheader**</span><span class="sxs-lookup"><span data-stu-id="00495-114"><span id="NoHeader"></span><span id="noheader"></span><span id="NOHEADER"></span>**NoHeader**</span></span>
</dt> <dd>

<span data-ttu-id="00495-115">Indica ou define o uso de nenhum cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="00495-115">Indicates or sets the use of no headers.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="00495-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="00495-116">Requirements</span></span>



| <span data-ttu-id="00495-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="00495-117">Requirement</span></span> | <span data-ttu-id="00495-118">Valor</span><span class="sxs-lookup"><span data-stu-id="00495-118">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="00495-119">INSERI</span><span class="sxs-lookup"><span data-stu-id="00495-119">IDL</span></span><br/> | <dl> <span data-ttu-id="00495-120"><dt>WdsView. idl</dt></span><span class="sxs-lookup"><span data-stu-id="00495-120"><dt>WdsView.idl</dt></span></span> </dl> |



 

 





