---
description: Ocorre quando as informações de nome de um objeto DIDiskQuotaUser são resolvidas.
ms.assetid: df32cb17-ad90-4535-a36b-60c5b4e9999f
title: Função onusernamechanged (Dskquota. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OnUserNameChanged
api_type:
- DllExport
api_location:
- Shell32.dll
ms.openlocfilehash: 98906f281c6c93a64754c1aa5cecfc6624599c40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104296936"
---
# <a name="onusernamechanged-function"></a><span data-ttu-id="2ef2f-103">Função onusernamechanged</span><span class="sxs-lookup"><span data-stu-id="2ef2f-103">OnUserNameChanged function</span></span>

<span data-ttu-id="2ef2f-104">Ocorre quando as informações de nome de um objeto [**DIDiskQuotaUser**](didiskquotauser-object.md) são resolvidas.</span><span class="sxs-lookup"><span data-stu-id="2ef2f-104">Occurs when the name information for a [**DIDiskQuotaUser**](didiskquotauser-object.md) object has been resolved.</span></span>

## <a name="parameters"></a><span data-ttu-id="2ef2f-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2ef2f-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ef2f-106">*oUser*</span><span class="sxs-lookup"><span data-stu-id="2ef2f-106">*oUser*</span></span> 
</dt> <dd>

<span data-ttu-id="2ef2f-107">O **objeto** que é avaliado para o objeto [**DIDiskQuotaUser**](didiskquotauser-object.md) associado ao usuário cujo nome foi resolvido.</span><span class="sxs-lookup"><span data-stu-id="2ef2f-107">The **Object** that evaluates to the [**DIDiskQuotaUser**](didiskquotauser-object.md) object associated with the user whose name has been resolved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ef2f-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2ef2f-108">Return value</span></span>

<span data-ttu-id="2ef2f-109">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="2ef2f-109">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2ef2f-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="2ef2f-110">Remarks</span></span>

<span data-ttu-id="2ef2f-111">Quando um cliente [**enumera os usuários**](didiskquotauser-object.md)ou chama o método [**adduser**](diskquotacontrol-adduser.md) ou [**FindUser**](diskquotacontrol-finduser.md) , o nome de usuário deve ser resolvido para o Sid (ID de segurança) associado.</span><span class="sxs-lookup"><span data-stu-id="2ef2f-111">When a client [**enumerates users**](didiskquotauser-object.md), or calls the [**AddUser**](diskquotacontrol-adduser.md) or [**FindUser**](diskquotacontrol-finduser.md) method, the user name must be resolved to the associated security ID (SID).</span></span> <span data-ttu-id="2ef2f-112">Como esse procedimento pode ser demorado, um cliente pode ter a resolução de nomes feita de forma assíncrona em um thread em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="2ef2f-112">Because this procedure can be time-consuming, a client can have name resolution done asynchronously on a background thread.</span></span> <span data-ttu-id="2ef2f-113">Quando o nome de um usuário é resolvido, o objeto [**DiskQuotaControl**](diskquotacontrol-object.md) notifica seu cliente acionando o evento **onnomedeusuáriochanged** .</span><span class="sxs-lookup"><span data-stu-id="2ef2f-113">When a user's name is resolved, the [**DiskQuotaControl**](diskquotacontrol-object.md) object notifies its client by firing the **OnUserNameChanged** event.</span></span> <span data-ttu-id="2ef2f-114">Um objeto **DIDiskQuotaUser** associado ao usuário é passado como um parâmetro.</span><span class="sxs-lookup"><span data-stu-id="2ef2f-114">A **DIDiskQuotaUser** object associated with the user is passed as a parameter.</span></span> <span data-ttu-id="2ef2f-115">Esse objeto permite que o cliente modifique as configurações de cota do usuário.</span><span class="sxs-lookup"><span data-stu-id="2ef2f-115">This object allows the client to modify the user's quota settings.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ef2f-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2ef2f-116">Requirements</span></span>



| <span data-ttu-id="2ef2f-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="2ef2f-117">Requirement</span></span> | <span data-ttu-id="2ef2f-118">Valor</span><span class="sxs-lookup"><span data-stu-id="2ef2f-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ef2f-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2ef2f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="2ef2f-120">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="2ef2f-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2ef2f-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2ef2f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="2ef2f-122">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="2ef2f-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="2ef2f-123">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="2ef2f-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="2ef2f-124"><dt>Dskquota. h</dt></span><span class="sxs-lookup"><span data-stu-id="2ef2f-124"><dt>Dskquota.h</dt></span></span> </dl>                         |
| <span data-ttu-id="2ef2f-125">DLL</span><span class="sxs-lookup"><span data-stu-id="2ef2f-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2ef2f-126"><dt>Shell32.dll (versão 5,0 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="2ef2f-126"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ef2f-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="2ef2f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ef2f-128">**Objeto DiskQuotaControl**</span><span class="sxs-lookup"><span data-stu-id="2ef2f-128">**DiskQuotaControl Object**</span></span>](diskquotacontrol-object.md)
</dt> </dl>

 

 




