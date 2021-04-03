---
title: Estrutura de PROTOCOL_SPECIFIC_DATA (RTM. h)
description: A \_ estrutura de dados específica de protocolo \_ contém memória reservada para dados específicos de um protocolo de roteamento específico.
ms.assetid: b6c3a342-4726-4f7b-9511-dbe1393faf98
keywords:
- RAS da estrutura de PROTOCOL_SPECIFIC_DATA
- RAS de ponteiro de estrutura de PPROTOCOL_SPECIFIC_DATA
topic_type:
- apiref
api_name:
- PROTOCOL_SPECIFIC_DATA
api_location:
- Rtm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3162aa377c051f6b329e993dfaca3bed17fae780
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644822"
---
# <a name="protocol_specific_data-structure"></a><span data-ttu-id="857bf-105">\_Estrutura de dados específica de protocolo \_</span><span class="sxs-lookup"><span data-stu-id="857bf-105">PROTOCOL\_SPECIFIC\_DATA structure</span></span>

<span data-ttu-id="857bf-106">\[Essa API foi substituída pela API do [Gerenciador de tabela de roteamento versão 2](about-routing-table-manager-version-2.md) e não estará disponível além do Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="857bf-106">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="857bf-107">Os aplicativos devem usar a API da versão 2 do Gerenciador de tabela de roteamento.\]</span><span class="sxs-lookup"><span data-stu-id="857bf-107">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="857bf-108">A estrutura de **\_ \_ dados específica de protocolo** contém memória reservada para dados específicos de um protocolo de roteamento específico.</span><span class="sxs-lookup"><span data-stu-id="857bf-108">The **PROTOCOL\_SPECIFIC\_DATA** structure contains memory reserved for data specific to a particular routing protocol.</span></span>

## <a name="syntax"></a><span data-ttu-id="857bf-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="857bf-109">Syntax</span></span>


```C++
typedef struct _PROTOCOL_SPECIFIC_DATA {
  DWORD PSD_Data[4];
} PROTOCOL_SPECIFIC_DATA, *PPROTOCOL_SPECIFIC_DATA;
```



## <a name="members"></a><span data-ttu-id="857bf-110">Membros</span><span class="sxs-lookup"><span data-stu-id="857bf-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="857bf-111">**\_Dados PSD**</span><span class="sxs-lookup"><span data-stu-id="857bf-111">**PSD\_Data**</span></span>
</dt> <dd>

<span data-ttu-id="857bf-112">Especifica uma matriz de variáveis **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="857bf-112">Specifies an array of **DWORD** variables.</span></span> <span data-ttu-id="857bf-113">Essa memória é reservada para dados que são específicos para protocolos de roteamento.</span><span class="sxs-lookup"><span data-stu-id="857bf-113">This memory is reserved for data that is specific to routing protocols.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="857bf-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="857bf-114">Requirements</span></span>



| <span data-ttu-id="857bf-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="857bf-115">Requirement</span></span> | <span data-ttu-id="857bf-116">Valor</span><span class="sxs-lookup"><span data-stu-id="857bf-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="857bf-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="857bf-117">Minimum supported client</span></span><br/> | <span data-ttu-id="857bf-118">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="857bf-118">None supported</span></span><br/>                                                        |
| <span data-ttu-id="857bf-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="857bf-119">Minimum supported server</span></span><br/> | <span data-ttu-id="857bf-120">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="857bf-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="857bf-121">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="857bf-121">End of server support</span></span><br/>    | <span data-ttu-id="857bf-122">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="857bf-122">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="857bf-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="857bf-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="857bf-124"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="857bf-124"><dt>Rtm.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="857bf-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="857bf-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="857bf-126">Referência da versão 1 do Gerenciador de tabela de roteamento</span><span class="sxs-lookup"><span data-stu-id="857bf-126">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="857bf-127">Estruturas da versão 1 do Gerenciador de tabela de roteamento</span><span class="sxs-lookup"><span data-stu-id="857bf-127">Routing Table Manager Version 1 Structures</span></span>](routing-table-manager-version-1-structures.md)
</dt> <dt>

[<span data-ttu-id="857bf-128">**\_rota de IP RTM \_**</span><span class="sxs-lookup"><span data-stu-id="857bf-128">**RTM\_IP\_ROUTE**</span></span>](rtm-ip-route.md)
</dt> <dt>

[<span data-ttu-id="857bf-129">**\_rota IPX do RTM \_**</span><span class="sxs-lookup"><span data-stu-id="857bf-129">**RTM\_IPX\_ROUTE**</span></span>](rtm-ipx-route.md)
</dt> </dl>

 

 





