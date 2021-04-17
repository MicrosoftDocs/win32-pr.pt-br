---
description: Uma constante numérica que especifica o número máximo de caracteres que alguns dos provedores de criptografia da Microsoft usarão ao obter a ID de usuário.
ms.assetid: cc15a166-9a0c-41ce-9cb1-ecdc922565c0
title: MAXUIDLEN (Wincrypt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 199d8e697deba86ffe48d4f76501f2d9d3a6d4e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105813104"
---
# <a name="maxuidlen"></a><span data-ttu-id="b742c-103">MAXUIDLEN</span><span class="sxs-lookup"><span data-stu-id="b742c-103">MAXUIDLEN</span></span>

<span data-ttu-id="b742c-104">MAXUIDLEN é uma constante numérica que especifica o número máximo de caracteres que alguns dos provedores de criptografia da Microsoft usarão ao obter a ID de usuário. MAXUIDLEN é definido em Wincrypt. h.</span><span class="sxs-lookup"><span data-stu-id="b742c-104">MAXUIDLEN is a numeric constant that specifies the maximum number of characters that some of the Microsoft cryptographic providers will use when obtaining the user ID.MAXUIDLEN is defined in Wincrypt.h.</span></span>



| <span data-ttu-id="b742c-105">Constante/valor</span><span class="sxs-lookup"><span data-stu-id="b742c-105">Constant/value</span></span>                                                                                                                                                                                                  | <span data-ttu-id="b742c-106">Description</span><span class="sxs-lookup"><span data-stu-id="b742c-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                   |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MAXUIDLEN"></span><span id="maxuidlen"></span><dl> <span data-ttu-id="b742c-107"><dt>**MAXUIDLEN**</dt> <dt>64 (0x40)</dt></span><span class="sxs-lookup"><span data-stu-id="b742c-107"><dt>**MAXUIDLEN**</dt> <dt>64 (0x40)</dt></span></span> </dl> | <span data-ttu-id="b742c-108">Quando o parâmetro *pszContainer* da função [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) é **nulo**, alguns dos provedores de criptografia da Microsoft usam o nome de logon do usuário conectado no momento como o nome do contêiner de chave.</span><span class="sxs-lookup"><span data-stu-id="b742c-108">When the *pszContainer* parameter of the [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) function is **NULL**, some of the Microsoft cryptographic providers use the logon name of the currently logged on user as the key container name.</span></span> <span data-ttu-id="b742c-109">MAXUIDLEN especifica o número máximo de caracteres, incluindo o caractere **nulo** de terminação, que esses provedores usarão para o nome de usuário.</span><span class="sxs-lookup"><span data-stu-id="b742c-109">MAXUIDLEN specifies the maximum number of characters, including the terminating **NULL** character, that these providers will use for the user name.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="b742c-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b742c-110">Requirements</span></span>



| <span data-ttu-id="b742c-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="b742c-111">Requirement</span></span> | <span data-ttu-id="b742c-112">Valor</span><span class="sxs-lookup"><span data-stu-id="b742c-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b742c-113">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b742c-113">Minimum supported client</span></span><br/> | <span data-ttu-id="b742c-114">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="b742c-114">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="b742c-115">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b742c-115">Minimum supported server</span></span><br/> | <span data-ttu-id="b742c-116">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b742c-116">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b742c-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b742c-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="b742c-118"><dt>Wincrypt. h</dt></span><span class="sxs-lookup"><span data-stu-id="b742c-118"><dt>Wincrypt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b742c-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="b742c-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b742c-120">**CryptAcquireContext**</span><span class="sxs-lookup"><span data-stu-id="b742c-120">**CryptAcquireContext**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta)
</dt> <dt>

[<span data-ttu-id="b742c-121">**CPAcquireContext**</span><span class="sxs-lookup"><span data-stu-id="b742c-121">**CPAcquireContext**</span></span>](https://www.bing.com/search?q=**CPAcquireContext**)
</dt> </dl>

 

 




