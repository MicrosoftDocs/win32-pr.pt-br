---
title: Propriedade de nome ITsSbEnvironment
description: Recupera um valor que indica o nome do ambiente que hospeda o computador de destino.
ms.assetid: 8104bdae-f445-425b-b326-cc3333839d29
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota de propriedade de nome
- Propriedade Name Serviços de Área de Trabalho Remota, interface ITsSbEnvironment
- Serviços de Área de Trabalho Remota de interface ITsSbEnvironment, Propriedade Name
topic_type:
- apiref
api_name:
- ITsSbEnvironment.Name
- ITsSbEnvironment.get_Name
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b5ac2fd725ec07102c08e93b2bfb39dabe701ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918191"
---
# <a name="itssbenvironmentname-property"></a><span data-ttu-id="ad7e5-106">Propriedade ITsSbEnvironment:: Name</span><span class="sxs-lookup"><span data-stu-id="ad7e5-106">ITsSbEnvironment::Name property</span></span>

<span data-ttu-id="ad7e5-107">Recupera um valor que indica o nome do ambiente que hospeda o computador de destino.</span><span class="sxs-lookup"><span data-stu-id="ad7e5-107">Retrieves a value that indicates the name of the environment that hosts the target computer.</span></span>

<span data-ttu-id="ad7e5-108">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="ad7e5-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad7e5-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ad7e5-109">Syntax</span></span>


```C++
HRESULT get_Name(
  [out, retval] BSTR *pVal
);
```



## <a name="property-value"></a><span data-ttu-id="ad7e5-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="ad7e5-110">Property value</span></span>

<span data-ttu-id="ad7e5-111">Um ponteiro para uma variável **BSTR** que contém o nome do ambiente.</span><span class="sxs-lookup"><span data-stu-id="ad7e5-111">A pointer to a **BSTR** variable that contains the name of the environment.</span></span>

## <a name="remarks"></a><span data-ttu-id="ad7e5-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="ad7e5-112">Remarks</span></span>

<span data-ttu-id="ad7e5-113">Esse método retorna uma cadeia de caracteres que não é usada diretamente pelo agente de Conexão de Área de Trabalho Remota (agente de conexão RD).</span><span class="sxs-lookup"><span data-stu-id="ad7e5-113">This method returns a string that is not directly used by Remote Desktop Connection Broker (RD Connection Broker).</span></span> <span data-ttu-id="ad7e5-114">O agente de conexão RD passa essa cadeia de caracteres para plug-ins de recurso.</span><span class="sxs-lookup"><span data-stu-id="ad7e5-114">RD Connection Broker passes this string to resource plug-ins.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad7e5-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ad7e5-115">Requirements</span></span>



| <span data-ttu-id="ad7e5-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="ad7e5-116">Requirement</span></span> | <span data-ttu-id="ad7e5-117">Valor</span><span class="sxs-lookup"><span data-stu-id="ad7e5-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ad7e5-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ad7e5-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ad7e5-119">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="ad7e5-119">None supported</span></span><br/>                                                            |
| <span data-ttu-id="ad7e5-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ad7e5-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ad7e5-121">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ad7e5-121">Windows Server 2012</span></span><br/>                                                       |
| <span data-ttu-id="ad7e5-122">INSERI</span><span class="sxs-lookup"><span data-stu-id="ad7e5-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ad7e5-123"><dt>Sbtsv. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ad7e5-123"><dt>Sbtsv.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad7e5-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="ad7e5-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad7e5-125">**ITsSbEnvironment**</span><span class="sxs-lookup"><span data-stu-id="ad7e5-125">**ITsSbEnvironment**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbenvironment)
</dt> </dl>

 

 





