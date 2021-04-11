---
title: Propriedade de nome de usuário ITsSbClientConnection
description: Recupera um valor que indica o nome do usuário que iniciou a conexão.
ms.assetid: 74f4b8fb-efd4-46d7-9d2f-dd9ef583eb54
ms.tgt_platform: multiple
keywords:
- Propriedade de nome de usuário Serviços de Área de Trabalho Remota
- Propriedade UserName Serviços de Área de Trabalho Remota, interface ITsSbClientConnection
- Serviços de Área de Trabalho Remota de interface ITsSbClientConnection, Propriedade UserName
topic_type:
- apiref
api_name:
- ITsSbClientConnection.UserName
- ITsSbClientConnection.get_UserName
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94bd3c1e5bb588ffb276b336cd945f32a0c19afd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104295877"
---
# <a name="itssbclientconnectionusername-property"></a><span data-ttu-id="65d5c-106">Propriedade ITsSbClientConnection:: UserName</span><span class="sxs-lookup"><span data-stu-id="65d5c-106">ITsSbClientConnection::UserName property</span></span>

<span data-ttu-id="65d5c-107">Recupera um valor que indica o nome do usuário que iniciou a conexão.</span><span class="sxs-lookup"><span data-stu-id="65d5c-107">Retrieves a value that indicates the name of the user who initiated the connection.</span></span>

<span data-ttu-id="65d5c-108">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="65d5c-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="65d5c-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="65d5c-109">Syntax</span></span>


```C++
HRESULT get_UserName(
  [out, retval] BSTR *pVal
);
```



## <a name="property-value"></a><span data-ttu-id="65d5c-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="65d5c-110">Property value</span></span>

<span data-ttu-id="65d5c-111">Um ponteiro para um nome de usuário.</span><span class="sxs-lookup"><span data-stu-id="65d5c-111">A pointer to a user name.</span></span> <span data-ttu-id="65d5c-112">Quando você terminar de usar a cadeia de caracteres, libere-a chamando a função [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) .</span><span class="sxs-lookup"><span data-stu-id="65d5c-112">When you have finished using the string, free it by calling the [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="65d5c-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="65d5c-113">Requirements</span></span>



| <span data-ttu-id="65d5c-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="65d5c-114">Requirement</span></span> | <span data-ttu-id="65d5c-115">Valor</span><span class="sxs-lookup"><span data-stu-id="65d5c-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="65d5c-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="65d5c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="65d5c-117">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="65d5c-117">None supported</span></span><br/>                                                            |
| <span data-ttu-id="65d5c-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="65d5c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="65d5c-119">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="65d5c-119">Windows Server 2012</span></span><br/>                                                       |
| <span data-ttu-id="65d5c-120">INSERI</span><span class="sxs-lookup"><span data-stu-id="65d5c-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="65d5c-121"><dt>Sbtsv. idl</dt></span><span class="sxs-lookup"><span data-stu-id="65d5c-121"><dt>Sbtsv.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65d5c-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="65d5c-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65d5c-123">**ITsSbClientConnection**</span><span class="sxs-lookup"><span data-stu-id="65d5c-123">**ITsSbClientConnection**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbclientconnection)
</dt> </dl>

 

