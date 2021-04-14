---
title: Propriedade ITsSbSession InitialProgram
description: Recupera ou especifica o programa inicial para esta sessão.
ms.assetid: c299c4f7-3c5f-468f-9fc7-81eac322dfa2
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade InitialProgram
- Propriedade InitialProgram Serviços de Área de Trabalho Remota, interface ITsSbSession
- Serviços de Área de Trabalho Remota de interface ITsSbSession, Propriedade InitialProgram
topic_type:
- apiref
api_name:
- ITsSbSession.InitialProgram
- ITsSbSession.get_InitialProgram
- ITsSbSession.put_InitialProgram
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 307f8bb4330caf4b84b8650c9ccc2551c94da76d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455150"
---
# <a name="itssbsessioninitialprogram-property"></a><span data-ttu-id="c47d1-106">Propriedade ITsSbSession:: InitialProgram</span><span class="sxs-lookup"><span data-stu-id="c47d1-106">ITsSbSession::InitialProgram property</span></span>

<span data-ttu-id="c47d1-107">Recupera ou especifica o programa inicial para esta sessão.</span><span class="sxs-lookup"><span data-stu-id="c47d1-107">Retrieves or specifies the initial program for this session.</span></span> <span data-ttu-id="c47d1-108">O programa inicial é o programa que é iniciado quando a sessão do usuário é iniciada.</span><span class="sxs-lookup"><span data-stu-id="c47d1-108">The initial program is the program that is launched when the user session starts.</span></span>

<span data-ttu-id="c47d1-109">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="c47d1-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="c47d1-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="c47d1-110">Syntax</span></span>


```C++
HRESULT put_InitialProgram(
  [in]          BSTR Application
);

HRESULT get_InitialProgram(
  [out, retval] BSTR *app
);
```



## <a name="property-value"></a><span data-ttu-id="c47d1-111">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="c47d1-111">Property value</span></span>

<span data-ttu-id="c47d1-112">Uma variável **BSTR** que contém o programa inicial.</span><span class="sxs-lookup"><span data-stu-id="c47d1-112">A **BSTR** variable that contains the initial program.</span></span>

## <a name="requirements"></a><span data-ttu-id="c47d1-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c47d1-113">Requirements</span></span>



| <span data-ttu-id="c47d1-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="c47d1-114">Requirement</span></span> | <span data-ttu-id="c47d1-115">Valor</span><span class="sxs-lookup"><span data-stu-id="c47d1-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c47d1-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c47d1-116">Minimum supported client</span></span><br/> | <span data-ttu-id="c47d1-117">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="c47d1-117">None supported</span></span><br/>                                                            |
| <span data-ttu-id="c47d1-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c47d1-118">Minimum supported server</span></span><br/> | <span data-ttu-id="c47d1-119">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c47d1-119">Windows Server 2012</span></span><br/>                                                       |
| <span data-ttu-id="c47d1-120">INSERI</span><span class="sxs-lookup"><span data-stu-id="c47d1-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c47d1-121"><dt>Sbtsv. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c47d1-121"><dt>Sbtsv.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c47d1-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="c47d1-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c47d1-123">**ITsSbSession**</span><span class="sxs-lookup"><span data-stu-id="c47d1-123">**ITsSbSession**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbsession)
</dt> </dl>

 

 





