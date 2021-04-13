---
title: Propriedade de estado ITsSbSession
description: Recupera ou especifica o estado da sessão.
ms.assetid: 4e769ff7-2bd5-4fcb-b2d7-4dedc853482b
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota de propriedade de estado
- Serviços de Área de Trabalho Remota de propriedade de estado, interface ITsSbSession
- Serviços de Área de Trabalho Remota de interface ITsSbSession, propriedade State
topic_type:
- apiref
api_name:
- ITsSbSession.State
- ITsSbSession.get_State
- ITsSbSession.put_State
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb939a518ab1050d932349cd70c85bcd22edf3d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455941"
---
# <a name="itssbsessionstate-property"></a><span data-ttu-id="87ff4-106">Propriedade ITsSbSession:: State</span><span class="sxs-lookup"><span data-stu-id="87ff4-106">ITsSbSession::State property</span></span>

<span data-ttu-id="87ff4-107">Recupera ou especifica o estado da sessão.</span><span class="sxs-lookup"><span data-stu-id="87ff4-107">Retrieves or specifies the session state.</span></span>

<span data-ttu-id="87ff4-108">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="87ff4-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="87ff4-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="87ff4-109">Syntax</span></span>


```C++
HRESULT put_State(
  [in]          TSSESSION_STATE State
);

HRESULT get_State(
  [out, retval] TSSESSION_STATE *pState
);
```



## <a name="property-value"></a><span data-ttu-id="87ff4-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="87ff4-110">Property value</span></span>

<span data-ttu-id="87ff4-111">Um valor da enumeração [**de \_ estado TSSESSION**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-tssession_state) que indica o estado de uma sessão.</span><span class="sxs-lookup"><span data-stu-id="87ff4-111">A value of the [**TSSESSION\_STATE**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-tssession_state) enumeration that indicates the state of a session.</span></span>

## <a name="requirements"></a><span data-ttu-id="87ff4-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="87ff4-112">Requirements</span></span>



| <span data-ttu-id="87ff4-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="87ff4-113">Requirement</span></span> | <span data-ttu-id="87ff4-114">Valor</span><span class="sxs-lookup"><span data-stu-id="87ff4-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="87ff4-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="87ff4-115">Minimum supported client</span></span><br/> | <span data-ttu-id="87ff4-116">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="87ff4-116">None supported</span></span><br/>                                                            |
| <span data-ttu-id="87ff4-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="87ff4-117">Minimum supported server</span></span><br/> | <span data-ttu-id="87ff4-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="87ff4-118">Windows Server 2012</span></span><br/>                                                       |
| <span data-ttu-id="87ff4-119">INSERI</span><span class="sxs-lookup"><span data-stu-id="87ff4-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="87ff4-120"><dt>Sbtsv. idl</dt></span><span class="sxs-lookup"><span data-stu-id="87ff4-120"><dt>Sbtsv.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87ff4-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="87ff4-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87ff4-122">**ITsSbSession**</span><span class="sxs-lookup"><span data-stu-id="87ff4-122">**ITsSbSession**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbsession)
</dt> <dt>

[<span data-ttu-id="87ff4-123">**\_estado TSSESSION**</span><span class="sxs-lookup"><span data-stu-id="87ff4-123">**TSSESSION\_STATE**</span></span>](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-tssession_state)
</dt> </dl>

 

 





