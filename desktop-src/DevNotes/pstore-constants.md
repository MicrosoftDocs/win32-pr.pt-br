---
description: As constantes a seguir são usadas por Pstore.
ms.assetid: 4bdccb86-2e0e-461c-9a74-184861b7db1e
title: Constantes Pstore (Pstore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PST_E_OK
- PST_E_TYPE_EXISTS
- PST_AUTHENTICODE
- PST_BINARY_CHECK
- PST_SECURITY_DESCRIPTOR
api_type:
- HeaderDef
api_location:
- Pstore.h
ms.openlocfilehash: 1c80fe7235a859ef0a754420fe5bd22caa10d6bb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105755919"
---
# <a name="pstore-constants"></a><span data-ttu-id="757e3-103">Constantes de Pstore</span><span class="sxs-lookup"><span data-stu-id="757e3-103">PStore Constants</span></span>

<span data-ttu-id="757e3-104">\[O armazenamento protegido (Pstore) está disponível para uso no Windows Server 2003 e no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="757e3-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="757e3-105">Ele só está disponível para operações somente leitura no Windows Server 2008 e no Windows Vista, mas pode estar indisponível nas versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="757e3-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="757e3-106">A Pstore usa uma implementação mais antiga da proteção de dados.</span><span class="sxs-lookup"><span data-stu-id="757e3-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="757e3-107">Os desenvolvedores são altamente incentivados a aproveitar a proteção de dados mais forte fornecida pelas funções [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="757e3-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="757e3-108">As constantes a seguir são usadas por Pstore.</span><span class="sxs-lookup"><span data-stu-id="757e3-108">The following constants are used by PStore.</span></span>

<span data-ttu-id="757e3-109">Códigos de erro de armazenamento protegido</span><span class="sxs-lookup"><span data-stu-id="757e3-109">Protected Storage Error Codes</span></span>



| <span data-ttu-id="757e3-110">Constante/valor</span><span class="sxs-lookup"><span data-stu-id="757e3-110">Constant/value</span></span>                                                                                                                                                                                                                               | <span data-ttu-id="757e3-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="757e3-111">Description</span></span>                                                        |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------|
| <span id="PST_E_OK"></span><span id="pst_e_ok"></span><dl> <span data-ttu-id="757e3-112"><dt>**PST \_ E \_ OK**</dt> <dt>0x00000000l</dt></span><span class="sxs-lookup"><span data-stu-id="757e3-112"><dt>**PST\_E\_OK**</dt> <dt>0x00000000L</dt></span></span> </dl>                             | <span data-ttu-id="757e3-113">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="757e3-113">The operation was successful.</span></span><br/>                           |
| <span id="PST_E_TYPE_EXISTS"></span><span id="pst_e_type_exists"></span><dl> <span data-ttu-id="757e3-114"><dt>**PST \_ O \_ tipo E \_ existe**</dt> <dt>0x800C0004L</dt></span><span class="sxs-lookup"><span data-stu-id="757e3-114"><dt>**PST\_E\_TYPE\_EXISTS**</dt> <dt>0x800C0004L</dt></span></span> </dl> | <span data-ttu-id="757e3-115">O item de dados já existe no armazenamento protegido.</span><span class="sxs-lookup"><span data-stu-id="757e3-115">The data item already exists in the protected storage.</span></span> <br/> |



<span data-ttu-id="757e3-116">Valores de cláusula de acesso</span><span class="sxs-lookup"><span data-stu-id="757e3-116">Access Clause Values</span></span>



| <span data-ttu-id="757e3-117">Constante/valor</span><span class="sxs-lookup"><span data-stu-id="757e3-117">Constant/value</span></span>                                                                                                                                                                                                                                      | <span data-ttu-id="757e3-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="757e3-118">Description</span></span>                                                                             |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------|
| <span id="PST_AUTHENTICODE"></span><span id="pst_authenticode"></span><dl> <span data-ttu-id="757e3-119"><dt>**PST \_ AUTHENTICODE**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="757e3-119"><dt>**PST\_AUTHENTICODE**</dt> <dt>1</dt></span></span> </dl>                       | <span data-ttu-id="757e3-120">Aponta para uma estrutura de [**\_ AUTHENTICODEDATA de PST**](pst-authenticodedata.md) .</span><span class="sxs-lookup"><span data-stu-id="757e3-120">Points to a [**PST\_AUTHENTICODEDATA**](pst-authenticodedata.md) structure.</span></span><br/> |
| <span id="PST_BINARY_CHECK_"></span><span id="pst_binary_check_"></span><dl> <span data-ttu-id="757e3-121"><dt> **\_ \_ Seleção binária de PST**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="757e3-121"><dt>**PST\_BINARY\_CHECK** </dt> <dt>2</dt></span></span> </dl>                   | <span data-ttu-id="757e3-122">Aponta para uma estrutura de **\_ BINARYCHECKDATA de PST** .</span><span class="sxs-lookup"><span data-stu-id="757e3-122">Points to a **PST\_BINARYCHECKDATA** structure.</span></span><br/>                              |
| <span id="PST_SECURITY_DESCRIPTOR"></span><span id="pst_security_descriptor"></span><dl> <span data-ttu-id="757e3-123"><dt>**PST \_ \_Descritor de segurança**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="757e3-123"><dt>**PST\_SECURITY\_DESCRIPTOR**</dt> <dt>4</dt></span></span> </dl> | <span data-ttu-id="757e3-124">Aponta para um descritor de segurança válido do Windows.</span><span class="sxs-lookup"><span data-stu-id="757e3-124">Points to a valid Windows security descriptor.</span></span> <br/>                              |



## <a name="requirements"></a><span data-ttu-id="757e3-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="757e3-125">Requirements</span></span>



| <span data-ttu-id="757e3-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="757e3-126">Requirement</span></span> | <span data-ttu-id="757e3-127">Valor</span><span class="sxs-lookup"><span data-stu-id="757e3-127">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="757e3-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="757e3-128">Header</span></span><br/> | <dl> <span data-ttu-id="757e3-129"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="757e3-129"><dt>Pstore.h</dt></span></span> </dl> |



 

 
