---
description: A estrutura PROTOCOLINFO descreve um protocolo.
ms.assetid: 7f936c93-a942-4591-9abc-59872df0964e
title: Estrutura PROTOCOLINFO (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PROTOCOLINFO
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: ed1410148a72c57b860fdfdaee447dcca505d99c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105778417"
---
# <a name="protocolinfo-structure"></a><span data-ttu-id="adf9d-103">Estrutura PROTOCOLINFO</span><span class="sxs-lookup"><span data-stu-id="adf9d-103">PROTOCOLINFO structure</span></span>

<span data-ttu-id="adf9d-104">A estrutura **PROTOCOLINFO** descreve um protocolo.</span><span class="sxs-lookup"><span data-stu-id="adf9d-104">The **PROTOCOLINFO** structure describes a protocol.</span></span>

## <a name="syntax"></a><span data-ttu-id="adf9d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="adf9d-105">Syntax</span></span>


```C++
typedef struct _PROTOCOLINFO {
  DWORD              ProtocolID;
  LPPROPERTYDATABASE PropertyDatabase;
  BYTE               ProtocolName[16];
  BYTE               HelpFile[16];
  BYTE               Comment[128];
} PROTOCOLINFO, *LPPROTOCOLINFO;
```



## <a name="members"></a><span data-ttu-id="adf9d-106">Membros</span><span class="sxs-lookup"><span data-stu-id="adf9d-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="adf9d-107">**Protocolid**</span><span class="sxs-lookup"><span data-stu-id="adf9d-107">**ProtocolID**</span></span>
</dt> <dd>

<span data-ttu-id="adf9d-108">Identificador de protocolo atribuído pelo sistema da sessão de execução especificada.</span><span class="sxs-lookup"><span data-stu-id="adf9d-108">System-assigned protocol identifier of the specified run session.</span></span>

</dd> <dt>

<span data-ttu-id="adf9d-109">**PropertyDatabase**</span><span class="sxs-lookup"><span data-stu-id="adf9d-109">**PropertyDatabase**</span></span>
</dt> <dd>

<span data-ttu-id="adf9d-110">Banco de dados de propriedades do protocolo especificado.</span><span class="sxs-lookup"><span data-stu-id="adf9d-110">Property database of the specified protocol.</span></span>

</dd> <dt>

<span data-ttu-id="adf9d-111">**ProtocolName**</span><span class="sxs-lookup"><span data-stu-id="adf9d-111">**ProtocolName**</span></span>
</dt> <dd>

<span data-ttu-id="adf9d-112">Nome de protocolo abreviado.</span><span class="sxs-lookup"><span data-stu-id="adf9d-112">Abbreviated protocol name.</span></span>

</dd> <dt>

<span data-ttu-id="adf9d-113">**HelpFile**</span><span class="sxs-lookup"><span data-stu-id="adf9d-113">**HelpFile**</span></span>
</dt> <dd>

<span data-ttu-id="adf9d-114">Nome de arquivo de ajuda opcional associado ao protocolo.</span><span class="sxs-lookup"><span data-stu-id="adf9d-114">Optional Help file name associated with the protocol.</span></span>

</dd> <dt>

<span data-ttu-id="adf9d-115">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="adf9d-115">**Comment**</span></span>
</dt> <dd>

<span data-ttu-id="adf9d-116">Um comentário que descreve o protocolo.</span><span class="sxs-lookup"><span data-stu-id="adf9d-116">A comment describing the protocol.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="adf9d-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="adf9d-117">Requirements</span></span>



| <span data-ttu-id="adf9d-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="adf9d-118">Requirement</span></span> | <span data-ttu-id="adf9d-119">Valor</span><span class="sxs-lookup"><span data-stu-id="adf9d-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="adf9d-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="adf9d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="adf9d-121">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="adf9d-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="adf9d-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="adf9d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="adf9d-123">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="adf9d-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="adf9d-124">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="adf9d-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="adf9d-125"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="adf9d-125"><dt>Netmon.h</dt></span></span> </dl> |



 

 




