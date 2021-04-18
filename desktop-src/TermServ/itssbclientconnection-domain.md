---
title: Propriedade de domínio ITsSbClientConnection
description: Recupera um valor que indica o nome de domínio do cliente de Conexão de Área de Trabalho Remota (RDC).
ms.assetid: 628f450d-10f4-4405-8d7c-ae58c72c2755
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota de propriedade de domínio
- Serviços de Área de Trabalho Remota de propriedade de domínio, interface ITsSbClientConnection
- Serviços de Área de Trabalho Remota de interface ITsSbClientConnection, propriedade de domínio
topic_type:
- apiref
api_name:
- ITsSbClientConnection.Domain
- ITsSbClientConnection.get_Domain
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 678d6fc6838b615faeec9fa36b736b3105b64453
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105810978"
---
# <a name="itssbclientconnectiondomain-property"></a><span data-ttu-id="856ca-106">ITsSbClientConnection: Propriedade omain de:D</span><span class="sxs-lookup"><span data-stu-id="856ca-106">ITsSbClientConnection::Domain property</span></span>

<span data-ttu-id="856ca-107">Recupera um valor que indica o nome de domínio do cliente de Conexão de Área de Trabalho Remota (RDC).</span><span class="sxs-lookup"><span data-stu-id="856ca-107">Retrieves a value that indicates the domain name of the Remote Desktop Connection (RDC) client.</span></span>

<span data-ttu-id="856ca-108">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="856ca-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="856ca-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="856ca-109">Syntax</span></span>


```C++
HRESULT get_Domain(
  [out, retval] BSTR *pVal
);
```



## <a name="property-value"></a><span data-ttu-id="856ca-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="856ca-110">Property value</span></span>

<span data-ttu-id="856ca-111">Um ponteiro para uma variável **BSTR** que contém o nome de domínio do cliente RDC.</span><span class="sxs-lookup"><span data-stu-id="856ca-111">A pointer to a **BSTR** variable that contains the domain name of the RDC client.</span></span> <span data-ttu-id="856ca-112">Quando você terminar de usar a cadeia de caracteres, libere-a chamando a função [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) .</span><span class="sxs-lookup"><span data-stu-id="856ca-112">When you have finished using the string, free it by calling the [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="856ca-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="856ca-113">Requirements</span></span>



| <span data-ttu-id="856ca-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="856ca-114">Requirement</span></span> | <span data-ttu-id="856ca-115">Valor</span><span class="sxs-lookup"><span data-stu-id="856ca-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="856ca-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="856ca-116">Minimum supported client</span></span><br/> | <span data-ttu-id="856ca-117">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="856ca-117">None supported</span></span><br/>                                                            |
| <span data-ttu-id="856ca-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="856ca-118">Minimum supported server</span></span><br/> | <span data-ttu-id="856ca-119">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="856ca-119">Windows Server 2012</span></span><br/>                                                       |
| <span data-ttu-id="856ca-120">INSERI</span><span class="sxs-lookup"><span data-stu-id="856ca-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="856ca-121"><dt>Sbtsv. idl</dt></span><span class="sxs-lookup"><span data-stu-id="856ca-121"><dt>Sbtsv.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="856ca-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="856ca-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="856ca-123">**ITsSbClientConnection**</span><span class="sxs-lookup"><span data-stu-id="856ca-123">**ITsSbClientConnection**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbclientconnection)
</dt> </dl>

 

