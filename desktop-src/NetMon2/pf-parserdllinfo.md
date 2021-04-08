---
description: A estrutura de PARSERDLLINFO de PF \_ define os analisadores localizados na DLL do analisador.
ms.assetid: a7473b58-7767-4224-be3b-e96132d98adf
title: Estrutura de PF_PARSERDLLINFO (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PF_PARSERDLLINFO
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: ab4a3673c567a72cb5d0284a07d5603913e77550
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922124"
---
# <a name="pf_parserdllinfo-structure"></a><span data-ttu-id="741f3-103">Estrutura de PARSERDLLINFO de PF \_</span><span class="sxs-lookup"><span data-stu-id="741f3-103">PF\_PARSERDLLINFO structure</span></span>

<span data-ttu-id="741f3-104">A estrutura de **\_ PARSERDLLINFO de PF** define os analisadores localizados na DLL do analisador.</span><span class="sxs-lookup"><span data-stu-id="741f3-104">The **PF\_PARSERDLLINFO** structure defines the parsers located in the parser DLL.</span></span>

## <a name="syntax"></a><span data-ttu-id="741f3-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="741f3-105">Syntax</span></span>


```C++
typedef struct _PF_PARSERDLLINFO {
  DWORD         nParsers;
  PF_PARSERINFO ParserInfo[];
} PF_PARSERDLLINFO, *PPF_PARSERDLLINFO;
```



## <a name="members"></a><span data-ttu-id="741f3-106">Membros</span><span class="sxs-lookup"><span data-stu-id="741f3-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="741f3-107">**nParsers**</span><span class="sxs-lookup"><span data-stu-id="741f3-107">**nParsers**</span></span>
</dt> <dd>

<span data-ttu-id="741f3-108">Número de analisadores na DLL do analisador.</span><span class="sxs-lookup"><span data-stu-id="741f3-108">Number of parsers in the parser DLL.</span></span>

</dd> <dt>

<span data-ttu-id="741f3-109">**ParserInfo**</span><span class="sxs-lookup"><span data-stu-id="741f3-109">**ParserInfo**</span></span>
</dt> <dd>

<span data-ttu-id="741f3-110">Matriz de [estruturas \_ PARSERINFO de PF](pf-parserinfo.md) que descrevem cada analisador na DLL do analisador.</span><span class="sxs-lookup"><span data-stu-id="741f3-110">Array of [PF\_PARSERINFO](pf-parserinfo.md) structures that describe each parser in the parser DLL.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="741f3-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="741f3-111">Remarks</span></span>

<span data-ttu-id="741f3-112">A estrutura de **\_ PARSERDLLINFO de PF** é retornada pela função de exportação [ParserAutoInstallInfo](parserautoinstallinfo.md) que é implementada na DLL do analisador.</span><span class="sxs-lookup"><span data-stu-id="741f3-112">The **PF\_PARSERDLLINFO** structure is returned by the [ParserAutoInstallInfo](parserautoinstallinfo.md) export function that is implemented in the parser DLL.</span></span> <span data-ttu-id="741f3-113">A função **ParserAutoInstallInfo** identifica o número de analisadores na dll e usa uma matriz de estruturas [ \_ PARSERINFO de PF](pf-parserinfo.md) para descrever cada analisador.</span><span class="sxs-lookup"><span data-stu-id="741f3-113">The **ParserAutoInstallInfo** function identifies the number of parsers in the DLL, and uses an array of [PF\_PARSERINFO](pf-parserinfo.md) structures to describe each parser.</span></span>

<span data-ttu-id="741f3-114">A estrutura de PARSERDLLINFO de PF \_ deve ser alocada usando **HeapAlloc**.</span><span class="sxs-lookup"><span data-stu-id="741f3-114">The PF\_PARSERDLLINFO structure must be allocated using **HeapAlloc**.</span></span>



| <span data-ttu-id="741f3-115">Para obter informações sobre</span><span class="sxs-lookup"><span data-stu-id="741f3-115">For information on</span></span>                                               | <span data-ttu-id="741f3-116">Consulte</span><span class="sxs-lookup"><span data-stu-id="741f3-116">See</span></span>                                                                         |
|------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="741f3-117">Quais analisadores são e como eles funcionam com Monitor de Rede.</span><span class="sxs-lookup"><span data-stu-id="741f3-117">What parsers are, and how they work with Network Monitor.</span></span>        | [<span data-ttu-id="741f3-118">Analisadores</span><span class="sxs-lookup"><span data-stu-id="741f3-118">Parsers</span></span>](parsers.md)                                                      |
| <span data-ttu-id="741f3-119">Quais pontos de entrada são incluídos na DLL do analisador.</span><span class="sxs-lookup"><span data-stu-id="741f3-119">Which entry points are included in the parser DLL.</span></span>               | [<span data-ttu-id="741f3-120">Arquitetura de DLL do analisador</span><span class="sxs-lookup"><span data-stu-id="741f3-120">Parser DLL Architecture</span></span>](parser-dll-architecture.md)                      |
| <span data-ttu-id="741f3-121">Como implementar **ParserAutoInstallInfo**  inclui um exemplo.</span><span class="sxs-lookup"><span data-stu-id="741f3-121">How to implement **ParserAutoInstallInfo**  includes an example.</span></span> | [<span data-ttu-id="741f3-122">Implementando ParserAutoIstallInfo</span><span class="sxs-lookup"><span data-stu-id="741f3-122">Implementing ParserAutoIstallInfo</span></span>](implementing-parserautoinstallinfo.md) |



 

## <a name="requirements"></a><span data-ttu-id="741f3-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="741f3-123">Requirements</span></span>



| <span data-ttu-id="741f3-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="741f3-124">Requirement</span></span> | <span data-ttu-id="741f3-125">Valor</span><span class="sxs-lookup"><span data-stu-id="741f3-125">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="741f3-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="741f3-126">Minimum supported client</span></span><br/> | <span data-ttu-id="741f3-127">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="741f3-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="741f3-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="741f3-128">Minimum supported server</span></span><br/> | <span data-ttu-id="741f3-129">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="741f3-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="741f3-130">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="741f3-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="741f3-131"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="741f3-131"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="741f3-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="741f3-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="741f3-133">PARSERINFO de PF \_</span><span class="sxs-lookup"><span data-stu-id="741f3-133">PF\_PARSERINFO</span></span>](pf-parserinfo.md)
</dt> <dt>

[<span data-ttu-id="741f3-134">ParserAutoInstallInfo</span><span class="sxs-lookup"><span data-stu-id="741f3-134">ParserAutoInstallInfo</span></span>](parserautoinstallinfo.md)
</dt> </dl>

 

 




