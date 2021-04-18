---
title: Propriedade de nome de usuário ITsSbSession
description: Recupera o nome de usuário desta sessão.
ms.assetid: 0034e8cc-b67b-4e30-a059-47a269bab0fd
ms.tgt_platform: multiple
keywords:
- Propriedade de nome de usuário Serviços de Área de Trabalho Remota
- Propriedade UserName Serviços de Área de Trabalho Remota, interface ITsSbSession
- Serviços de Área de Trabalho Remota de interface ITsSbSession, Propriedade UserName
topic_type:
- apiref
api_name:
- ITsSbSession.Username
- ITsSbSession.get_Username
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5fb66f0639d659fcb6800680ffc3b3486ad12b8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105780571"
---
# <a name="itssbsessionusername-property"></a><span data-ttu-id="bdd7a-106">Propriedade ITsSbSession:: username</span><span class="sxs-lookup"><span data-stu-id="bdd7a-106">ITsSbSession::Username property</span></span>

<span data-ttu-id="bdd7a-107">Recupera o nome de usuário desta sessão.</span><span class="sxs-lookup"><span data-stu-id="bdd7a-107">Retrieves the user name for this session.</span></span>

<span data-ttu-id="bdd7a-108">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="bdd7a-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="bdd7a-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bdd7a-109">Syntax</span></span>


```C++
HRESULT get_Username(
  [out, retval] BSTR *userName
);
```



## <a name="property-value"></a><span data-ttu-id="bdd7a-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="bdd7a-110">Property value</span></span>

<span data-ttu-id="bdd7a-111">Um ponteiro para uma variável **BSTR** que recebe o nome de usuário para esta sessão.</span><span class="sxs-lookup"><span data-stu-id="bdd7a-111">A pointer to a **BSTR** variable that receives the user name for this session.</span></span>

## <a name="requirements"></a><span data-ttu-id="bdd7a-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bdd7a-112">Requirements</span></span>



| <span data-ttu-id="bdd7a-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="bdd7a-113">Requirement</span></span> | <span data-ttu-id="bdd7a-114">Valor</span><span class="sxs-lookup"><span data-stu-id="bdd7a-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="bdd7a-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bdd7a-115">Minimum supported client</span></span><br/> | <span data-ttu-id="bdd7a-116">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="bdd7a-116">None supported</span></span><br/>                                                            |
| <span data-ttu-id="bdd7a-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bdd7a-117">Minimum supported server</span></span><br/> | <span data-ttu-id="bdd7a-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="bdd7a-118">Windows Server 2012</span></span><br/>                                                       |
| <span data-ttu-id="bdd7a-119">INSERI</span><span class="sxs-lookup"><span data-stu-id="bdd7a-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="bdd7a-120"><dt>Sbtsv. idl</dt></span><span class="sxs-lookup"><span data-stu-id="bdd7a-120"><dt>Sbtsv.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bdd7a-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="bdd7a-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bdd7a-122">**ITsSbSession**</span><span class="sxs-lookup"><span data-stu-id="bdd7a-122">**ITsSbSession**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbsession)
</dt> </dl>

 

 





