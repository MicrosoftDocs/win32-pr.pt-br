---
description: Define ou Obtém um valor que controla como o SID (identificador de segurança do usuário) é resolvido para nomes de usuário.
title: Propriedade DiskQuotaControl. UserNameResolution
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.UserNameResolution
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: dc936421-e66d-4762-912a-c586f9cdace4
ms.openlocfilehash: 169f4db6e135392e9548767520f6d2b0bd2d527c
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841457"
---
# <a name="diskquotacontrolusernameresolution-property"></a><span data-ttu-id="259dc-103">Propriedade DiskQuotaControl. UserNameResolution</span><span class="sxs-lookup"><span data-stu-id="259dc-103">DiskQuotaControl.UserNameResolution property</span></span>

<span data-ttu-id="259dc-104">Define ou Obtém um valor que controla como o SID (identificador de segurança do usuário) é resolvido para nomes de usuário.</span><span class="sxs-lookup"><span data-stu-id="259dc-104">Sets or gets a value that controls how user security identifier (SID) are resolved to user names.</span></span>

<span data-ttu-id="259dc-105">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="259dc-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="259dc-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="259dc-106">Syntax</span></span>


```JScript
iUserNameResolution = DiskQuotaControl.UserNameResolution
DiskQuotaControl.UserNameResolution = iUserNameResolution
```



## <a name="property-value"></a><span data-ttu-id="259dc-107">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="259dc-107">Property value</span></span>

<span data-ttu-id="259dc-108">Essa propriedade pode ser definida como um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="259dc-108">This property can be set to one of the following values.</span></span>



| <span data-ttu-id="259dc-109">Tipo de resolução</span><span class="sxs-lookup"><span data-stu-id="259dc-109">Resolution Type</span></span> | <span data-ttu-id="259dc-110">Valor</span><span class="sxs-lookup"><span data-stu-id="259dc-110">Value</span></span> | <span data-ttu-id="259dc-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="259dc-111">Description</span></span>                                                                                                                                              |
|-----------------|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="259dc-112">dqResolveNone</span><span class="sxs-lookup"><span data-stu-id="259dc-112">dqResolveNone</span></span>   | <span data-ttu-id="259dc-113">0</span><span class="sxs-lookup"><span data-stu-id="259dc-113">0</span></span>     | <span data-ttu-id="259dc-114">Não resolva as informações de nome de usuário.</span><span class="sxs-lookup"><span data-stu-id="259dc-114">Do not resolve user name information.</span></span>                                                                                                                    |
| <span data-ttu-id="259dc-115">dqResolveSync</span><span class="sxs-lookup"><span data-stu-id="259dc-115">dqResolveSync</span></span>   | <span data-ttu-id="259dc-116">1</span><span class="sxs-lookup"><span data-stu-id="259dc-116">1</span></span>     | <span data-ttu-id="259dc-117">Aguarde enquanto resolve informações de nome.</span><span class="sxs-lookup"><span data-stu-id="259dc-117">Wait while resolving name information.</span></span>                                                                                                                   |
| <span data-ttu-id="259dc-118">dqResolveAsync</span><span class="sxs-lookup"><span data-stu-id="259dc-118">dqResolveAsync</span></span>  | <span data-ttu-id="259dc-119">2</span><span class="sxs-lookup"><span data-stu-id="259dc-119">2</span></span>     | <span data-ttu-id="259dc-120">Não aguarde enquanto as informações de nome são resolvidas.</span><span class="sxs-lookup"><span data-stu-id="259dc-120">Do not wait while resolving name information.</span></span> <span data-ttu-id="259dc-121">O evento [**Onusernamechanged**](diskquotacontrol-onusernamechanged.md) é acionado quando o nome é resolvido.</span><span class="sxs-lookup"><span data-stu-id="259dc-121">The [**OnUserNameChanged**](diskquotacontrol-onusernamechanged.md) event fires when the name is resolved.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="259dc-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="259dc-122">Remarks</span></span>

<span data-ttu-id="259dc-123">Essa propriedade afeta a enumeração de objetos [**DIDiskQuotaUser**](didiskquotauser-object.md) e os métodos [**adduser**](diskquotacontrol-adduser.md) e [**FindUser**](diskquotacontrol-finduser.md) .</span><span class="sxs-lookup"><span data-stu-id="259dc-123">This property affects the enumeration of [**DIDiskQuotaUser**](didiskquotauser-object.md) objects, and the [**AddUser**](diskquotacontrol-adduser.md) and [**FindUser**](diskquotacontrol-finduser.md) methods.</span></span>

## <a name="requirements"></a><span data-ttu-id="259dc-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="259dc-124">Requirements</span></span>



| <span data-ttu-id="259dc-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="259dc-125">Requirement</span></span> | <span data-ttu-id="259dc-126">Valor</span><span class="sxs-lookup"><span data-stu-id="259dc-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="259dc-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="259dc-127">Minimum supported client</span></span><br/> | <span data-ttu-id="259dc-128">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="259dc-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="259dc-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="259dc-129">Minimum supported server</span></span><br/> | <span data-ttu-id="259dc-130">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="259dc-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="259dc-131">DLL</span><span class="sxs-lookup"><span data-stu-id="259dc-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="259dc-132"><dt>Shell32.dll (versão 5,0 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="259dc-132"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="259dc-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="259dc-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="259dc-134">**Objeto DiskQuotaControl**</span><span class="sxs-lookup"><span data-stu-id="259dc-134">**DiskQuotaControl Object**</span></span>](diskquotacontrol-object.md)
</dt> </dl>

 

 




