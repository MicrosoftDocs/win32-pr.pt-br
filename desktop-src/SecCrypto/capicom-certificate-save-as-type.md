---
description: Define o formato de um arquivo que contém informações de certificado.
ms.assetid: 417a6d1b-6329-418c-823c-d82b94207fd6
title: Enumeração de CAPICOM_CERTIFICATE_SAVE_AS_TYPE (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_CERTIFICATE_SAVE_AS_TYPE
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 1e5365594a5a1cf1f06691c63b37c04f38530575
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754608"
---
# <a name="capicom_certificate_save_as_type-enumeration"></a><span data-ttu-id="0566d-103">\_ \_ \_ Enumeração de tipo de \_ certificado capicor</span><span class="sxs-lookup"><span data-stu-id="0566d-103">CAPICOM\_CERTIFICATE\_SAVE\_AS\_TYPE enumeration</span></span>

<span data-ttu-id="0566d-104">O tipo de enumeração do **certificado CAPICOM \_ \_ Salvar \_ como \_ tipo** define o formato de um arquivo que contém informações de certificado.</span><span class="sxs-lookup"><span data-stu-id="0566d-104">The **CAPICOM\_CERTIFICATE\_SAVE\_AS\_TYPE** enumeration type defines the format of a file containing certificate information.</span></span> <span data-ttu-id="0566d-105">Esse tipo de enumeração foi introduzido pelo CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="0566d-105">This enumeration type was introduced by CAPICOM 2.0.</span></span>

## <a name="members"></a><span data-ttu-id="0566d-106">Membros</span><span class="sxs-lookup"><span data-stu-id="0566d-106">Members</span></span>



| <span data-ttu-id="0566d-107">Membro</span><span class="sxs-lookup"><span data-stu-id="0566d-107">Member</span></span>                                  | <span data-ttu-id="0566d-108">DESCRIÇÃO</span><span class="sxs-lookup"><span data-stu-id="0566d-108">Description</span></span>                                                                                                                                   | <span data-ttu-id="0566d-109">Valor</span><span class="sxs-lookup"><span data-stu-id="0566d-109">Value</span></span> |
|-----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|-------|
| <span data-ttu-id="0566d-110">**\_salvar certificado de CApicom \_ \_ como \_ pfx**</span><span class="sxs-lookup"><span data-stu-id="0566d-110">**CAPICOM\_CERTIFICATE\_SAVE\_AS\_PFX**</span></span> | <span data-ttu-id="0566d-111">O arquivo de saída será formatado como um arquivo PFX (PKCS 12) e quaisquer chaves privadas associadas que sejam exportáveis também serão salvas.</span><span class="sxs-lookup"><span data-stu-id="0566d-111">The output file will be formatted as a PFX (PKCS 12) file and any associated private keys which are exportable will also be saved.</span></span><br/> | <span data-ttu-id="0566d-112">0</span><span class="sxs-lookup"><span data-stu-id="0566d-112">0</span></span>     |
| <span data-ttu-id="0566d-113">**\_salvar certificado de CApicom \_ \_ como \_ cer**</span><span class="sxs-lookup"><span data-stu-id="0566d-113">**CAPICOM\_CERTIFICATE\_SAVE\_AS\_CER**</span></span> | <span data-ttu-id="0566d-114">O arquivo de saída será formatado como um arquivo CER sem chaves privadas salvas.</span><span class="sxs-lookup"><span data-stu-id="0566d-114">The output file will be formatted as a CER file with no private keys saved.</span></span><br/>                                                        | <span data-ttu-id="0566d-115">1</span><span class="sxs-lookup"><span data-stu-id="0566d-115">1</span></span>     |



## <a name="remarks"></a><span data-ttu-id="0566d-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="0566d-116">Remarks</span></span>

<span data-ttu-id="0566d-117">O tipo de enumeração do **certificado de CAPICOM \_ \_ Salvar \_ como \_ tipo** é usado pelo método [**Certificate. Save**](certificate-save.md) .</span><span class="sxs-lookup"><span data-stu-id="0566d-117">The **CAPICOM\_CERTIFICATE\_SAVE\_AS\_TYPE** enumeration type is used by the [**Certificate.Save**](certificate-save.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="0566d-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0566d-118">Requirements</span></span>



| <span data-ttu-id="0566d-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="0566d-119">Requirement</span></span> | <span data-ttu-id="0566d-120">Valor</span><span class="sxs-lookup"><span data-stu-id="0566d-120">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="0566d-121">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="0566d-121">Redistributable</span></span><br/> | <span data-ttu-id="0566d-122">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="0566d-122">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="0566d-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0566d-123">Header</span></span><br/>          | <dl> <span data-ttu-id="0566d-124"><dt>CAPICOM. h</dt></span><span class="sxs-lookup"><span data-stu-id="0566d-124"><dt>Capicom.h</dt></span></span> </dl> |



 

 




