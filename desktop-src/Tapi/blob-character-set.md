---
description: A enumeração do conjunto de caracteres de BLOB \_ \_ indica o conjunto de caracteres usado pelo blob de conferência atual.
ms.assetid: 79131b84-19b5-492b-a44e-9d47c365b298
title: Enumeração de BLOB_CHARACTER_SET (Sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66b180a8574f1643a5fc1be134be99c951faaf1d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811935"
---
# <a name="blob_character_set-enumeration"></a><span data-ttu-id="e1dc3-103">Enumeração do conjunto de \_ caracteres do blob \_</span><span class="sxs-lookup"><span data-stu-id="e1dc3-103">BLOB\_CHARACTER\_SET enumeration</span></span>

<span data-ttu-id="e1dc3-104">\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="e1dc3-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="e1dc3-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="e1dc3-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="e1dc3-106">A enumeração do **\_ \_ conjunto de caracteres de blob** indica o conjunto de caracteres usado pelo blob de conferência atual.</span><span class="sxs-lookup"><span data-stu-id="e1dc3-106">The **BLOB\_CHARACTER\_SET** enum indicates the character set used by the current conference blob.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1dc3-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e1dc3-107">Syntax</span></span>


```C++
} BLOB_CHARACTER_SET;
```



## <a name="constants"></a><span data-ttu-id="e1dc3-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="e1dc3-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="e1dc3-109"><span id="BCS_ASCII"></span><span id="bcs_ascii"></span>**ASCII do BCS \_**</span><span class="sxs-lookup"><span data-stu-id="e1dc3-109"><span id="BCS_ASCII"></span><span id="bcs_ascii"></span>**BCS\_ASCII**</span></span>
</dt> <dd>

<span data-ttu-id="e1dc3-110">Formato ASCII padrão.</span><span class="sxs-lookup"><span data-stu-id="e1dc3-110">Standard ASCII format.</span></span>

</dd> <dt>

<span data-ttu-id="e1dc3-111"><span id="BCS_UTF7"></span><span id="bcs_utf7"></span>**UTF7 de BCS \_**</span><span class="sxs-lookup"><span data-stu-id="e1dc3-111"><span id="BCS_UTF7"></span><span id="bcs_utf7"></span>**BCS\_UTF7**</span></span>
</dt> <dd>

<span data-ttu-id="e1dc3-112">Formato de transformação de sete bits do Unicode.</span><span class="sxs-lookup"><span data-stu-id="e1dc3-112">Seven-bit transformation format of Unicode.</span></span> <span data-ttu-id="e1dc3-113">Para obter detalhes sobre esse formato, realize uma pesquisa na Internet para o RFC 1642.</span><span class="sxs-lookup"><span data-stu-id="e1dc3-113">For details on this format, conduct an Internet search for RFC 1642.</span></span>

</dd> <dt>

<span data-ttu-id="e1dc3-114"><span id="BCS_UTF8"></span><span id="bcs_utf8"></span>**BCS \_ UTF8**</span><span class="sxs-lookup"><span data-stu-id="e1dc3-114"><span id="BCS_UTF8"></span><span id="bcs_utf8"></span>**BCS\_UTF8**</span></span>
</dt> <dd>

<span data-ttu-id="e1dc3-115">Formato de transformação UCS 8.</span><span class="sxs-lookup"><span data-stu-id="e1dc3-115">UCS Transformation Format 8.</span></span> <span data-ttu-id="e1dc3-116">Para obter detalhes sobre esse formato, realize uma pesquisa na Internet para ISO (o Organização Internacional de Normalização) e o IEC (o International Electrotechnical Commission) Document ISO/IEC JTC1/SC2/WG2 N 1036, com data de 1º de agosto de 1994, por WG2 Project editor.</span><span class="sxs-lookup"><span data-stu-id="e1dc3-116">For details on this format, conduct an Internet search for ISO (the International Organization for Standardization) and IEC (the International Electrotechnical Commission) document ISO/IEC JTC1/SC2/WG2 N 1036, dated August 1, 1994, by WG2 Project Editor.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e1dc3-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e1dc3-117">Requirements</span></span>



| <span data-ttu-id="e1dc3-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="e1dc3-118">Requirement</span></span> | <span data-ttu-id="e1dc3-119">Valor</span><span class="sxs-lookup"><span data-stu-id="e1dc3-119">Value</span></span> |
|-------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="e1dc3-120">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="e1dc3-120">TAPI version</span></span><br/> | <span data-ttu-id="e1dc3-121">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="e1dc3-121">Requires TAPI 3.0 or later</span></span><br/>                                               |
| <span data-ttu-id="e1dc3-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e1dc3-122">Header</span></span><br/>       | <dl> <span data-ttu-id="e1dc3-123"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="e1dc3-123"><dt>Sdpblb.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e1dc3-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="e1dc3-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1dc3-125">**ITDirectoryObjectConference**</span><span class="sxs-lookup"><span data-stu-id="e1dc3-125">**ITDirectoryObjectConference**</span></span>](/windows/desktop/api/Rend/nn-rend-itdirectoryobjectconference)
</dt> <dt>

[<span data-ttu-id="e1dc3-126">**obter \_ CharacterSet**</span><span class="sxs-lookup"><span data-stu-id="e1dc3-126">**get\_CharacterSet**</span></span>](itconferenceblob-get-characterset.md)
</dt> <dt>

[<span data-ttu-id="e1dc3-127">**Init**</span><span class="sxs-lookup"><span data-stu-id="e1dc3-127">**Init**</span></span>](itconferenceblob-init.md)
</dt> <dt>

[<span data-ttu-id="e1dc3-128">**SetConferenceBlob**</span><span class="sxs-lookup"><span data-stu-id="e1dc3-128">**SetConferenceBlob**</span></span>](itconferenceblob-setconferenceblob.md)
</dt> </dl>

 

 




