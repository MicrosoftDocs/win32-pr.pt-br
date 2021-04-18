---
description: A estrutura de PARSERINFO de PF \_ define um analisador por vez. Na estrutura PF \_ PARSERINFO, um analisador é definido pelas informações sobre o protocolo que o analisador detecta.
ms.assetid: e1180952-9560-4386-9320-919dfb8171b3
title: Estrutura de PF_PARSERINFO (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PF_PARSERINFO
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 28ebeaad31e6f40ceb961d8c303a22590966947f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105778535"
---
# <a name="pf_parserinfo-structure"></a><span data-ttu-id="3da44-104">Estrutura de PARSERINFO de PF \_</span><span class="sxs-lookup"><span data-stu-id="3da44-104">PF\_PARSERINFO structure</span></span>

<span data-ttu-id="3da44-105">A estrutura de **\_ PARSERINFO de PF** define um analisador por vez.</span><span class="sxs-lookup"><span data-stu-id="3da44-105">The **PF\_PARSERINFO** structure defines one parser at a time.</span></span> <span data-ttu-id="3da44-106">Na estrutura **PF \_ PARSERINFO** , um analisador é definido pelas informações sobre o protocolo que o analisador detecta.</span><span class="sxs-lookup"><span data-stu-id="3da44-106">In the **PF\_PARSERINFO** structure, a parser is defined by the information about the protocol that the parser detects.</span></span>

## <a name="syntax"></a><span data-ttu-id="3da44-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3da44-107">Syntax</span></span>


```C++
typedef struct _PF_PARSERINFO {
  char           szProtocolName[MAX_PROTOCOL_NAME_LEN];
  char           szComment[MAX_PROTOCOL_COMMENT_LEN];
  char           szHelpFile[MAX_PATH];
  PPF_FOLLOWSET  pWhoCanPrecedeMe;
  PPF_FOLLOWSET  pWhoCanFollowMe;
  PPF_HANDOFFSET pWhoHandsOffToMe;
  PPF_HANDOFFSET pWhoDoIHandOffTo;
} PF_PARSERINFO, *PPF_PARSERINFO;
```



## <a name="members"></a><span data-ttu-id="3da44-108">Membros</span><span class="sxs-lookup"><span data-stu-id="3da44-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="3da44-109">**szProtocolName**</span><span class="sxs-lookup"><span data-stu-id="3da44-109">**szProtocolName**</span></span>
</dt> <dd>

<span data-ttu-id="3da44-110">Nome do protocolo que o analisador detecta.</span><span class="sxs-lookup"><span data-stu-id="3da44-110">Name of the protocol that the parser detects.</span></span>

</dd> <dt>

<span data-ttu-id="3da44-111">**szComment**</span><span class="sxs-lookup"><span data-stu-id="3da44-111">**szComment**</span></span>
</dt> <dd>

<span data-ttu-id="3da44-112">Breve descrição do protocolo.</span><span class="sxs-lookup"><span data-stu-id="3da44-112">Brief description of the protocol.</span></span>

</dd> <dt>

<span data-ttu-id="3da44-113">**szHelpFile**</span><span class="sxs-lookup"><span data-stu-id="3da44-113">**szHelpFile**</span></span>
</dt> <dd>

<span data-ttu-id="3da44-114">Nome do arquivo de ajuda de protocolo, se houver.</span><span class="sxs-lookup"><span data-stu-id="3da44-114">Name of the protocol Help file, if any.</span></span>

</dd> <dt>

<span data-ttu-id="3da44-115">**pWhoCanPrecedeMe**</span><span class="sxs-lookup"><span data-stu-id="3da44-115">**pWhoCanPrecedeMe**</span></span>
</dt> <dd>

<span data-ttu-id="3da44-116">Ponteiro para uma estrutura de [ \_ acompanhamento de PF](pf-followset.md) que lista os protocolos que podem preceder o protocolo que a estrutura **PF \_ PARSERINFO** descreve.</span><span class="sxs-lookup"><span data-stu-id="3da44-116">Pointer to a [PF\_FOLLOWSET](pf-followset.md) structure that lists the protocols that can precede the protocol the **PF\_PARSERINFO** structure describes.</span></span> <span data-ttu-id="3da44-117">Monitor de Rede adiciona o protocolo analisador ao [*seguinte conjunto*](f.md) de todos os protocolos no conjunto.</span><span class="sxs-lookup"><span data-stu-id="3da44-117">Network Monitor adds the parser protocol to the [*follow set*](f.md) of all the protocols in the set.</span></span>

</dd> <dt>

<span data-ttu-id="3da44-118">**pWhoCanFollowMe**</span><span class="sxs-lookup"><span data-stu-id="3da44-118">**pWhoCanFollowMe**</span></span>
</dt> <dd>

<span data-ttu-id="3da44-119">Ponteiro para uma estrutura de [ \_ acompanhamento de PF](pf-followset.md) que lista o protocolo que pode seguir o protocolo que a estrutura **PF \_ PARSERINFO** descreve.</span><span class="sxs-lookup"><span data-stu-id="3da44-119">Pointer to a [PF\_FOLLOWSET](pf-followset.md) structure that lists the protocol that can follow the protocol the **PF\_PARSERINFO** structure describes.</span></span> <span data-ttu-id="3da44-120">Monitor de Rede adiciona os protocolos do conjunto ao conjunto de [*acompanhamento*](f.md) do protocolo analisador.</span><span class="sxs-lookup"><span data-stu-id="3da44-120">Network Monitor adds the protocols of the set to the [*follow set*](f.md) of the parser protocol.</span></span>

</dd> <dt>

<span data-ttu-id="3da44-121">**pWhoHandsOffToMe**</span><span class="sxs-lookup"><span data-stu-id="3da44-121">**pWhoHandsOffToMe**</span></span>
</dt> <dd>

<span data-ttu-id="3da44-122">Ponteiro para uma estrutura de [ \_ entrega de PF](pf-handoffset.md) que é descrita no protocolo que a estrutura **de \_ PARSERINFO do PF** descreve.</span><span class="sxs-lookup"><span data-stu-id="3da44-122">Pointer to a [PF\_HANDOFFSET](pf-handoffset.md) structure that hands-off to the protocol that the **PF\_PARSERINFO** structure describes.</span></span> <span data-ttu-id="3da44-123">Monitor de Rede adiciona o protocolo analisador aos [*conjuntos de entrega*](h.md) de todos os protocolos no conjunto.</span><span class="sxs-lookup"><span data-stu-id="3da44-123">Network Monitor adds the parser protocol to the [*handoff sets*](h.md) of all the protocols in the set.</span></span>

</dd> <dt>

<span data-ttu-id="3da44-124">**pWhoDoIHandOffTo**</span><span class="sxs-lookup"><span data-stu-id="3da44-124">**pWhoDoIHandOffTo**</span></span>
</dt> <dd>

<span data-ttu-id="3da44-125">Ponteiro para uma estrutura de [ \_ entrega do PF](pf-handoffset.md) que lista os protocolos para os quais o protocolo analisador é immãos.</span><span class="sxs-lookup"><span data-stu-id="3da44-125">Pointer to a [PF\_HANDOFFSET](pf-handoffset.md) structure that lists the protocols that the parser protocol hands off to.</span></span> <span data-ttu-id="3da44-126">Monitor de Rede adiciona os protocolos desse conjunto ao conjunto de [*entrega*](h.md) do protocolo analisador.</span><span class="sxs-lookup"><span data-stu-id="3da44-126">Network Monitor adds the protocols of this set to the [*handoff set*](h.md) of the parser protocol.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3da44-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="3da44-127">Remarks</span></span>

<span data-ttu-id="3da44-128">A estrutura de **\_ PARSERINFO de PF** é usada na estrutura de **\_ PARSERDLLINFO de PF** para fornecer uma descrição de um analisador.</span><span class="sxs-lookup"><span data-stu-id="3da44-128">The **PF\_PARSERINFO** structure is used in the **PF\_PARSERDLLINFO** structure to provide a description of a parser.</span></span> <span data-ttu-id="3da44-129">Monitor de Rede usa a descrição do analisador para atualizar o arquivo de [*Parser.ini*](p.md) e os arquivos ini dos analisadores que precedem e seguem o protocolo descrito na estrutura **PF \_ PARSERINFO** .</span><span class="sxs-lookup"><span data-stu-id="3da44-129">Network Monitor uses the parser description to update the [*Parser.ini*](p.md) file, and the INI files of the parsers that precede and follow the protocol described in the **PF\_PARSERINFO** structure.</span></span>

<span data-ttu-id="3da44-130">Um conjunto de acompanhamento especifica os protocolos que seguem um protocolo.</span><span class="sxs-lookup"><span data-stu-id="3da44-130">A follow set specifies the protocols that follow a protocol.</span></span> <span data-ttu-id="3da44-131">Monitor de Rede usa um conjunto de acompanhamento quando o analisador não pode identificar o próximo protocolo dos dados em uma instância de protocolo.</span><span class="sxs-lookup"><span data-stu-id="3da44-131">Network Monitor uses a follow set when the parser cannot identify the next protocol from the data in a protocol instance.</span></span> <span data-ttu-id="3da44-132">Um conjunto de acompanhamento é armazenado no arquivo de [*Parser.ini*](p.md) .</span><span class="sxs-lookup"><span data-stu-id="3da44-132">A follow set is stored in the [*Parser.ini*](p.md) file.</span></span> <span data-ttu-id="3da44-133">Quando o analisador é instalado pela primeira vez, Monitor de Rede atualiza o conjunto de protocolos do analisador que estão listados em **pWhoCanPrecedeMe** e **pWhoCanFollowMe**.</span><span class="sxs-lookup"><span data-stu-id="3da44-133">When the parser is installed for the first time, Network Monitor updates the follow set of the parser protocols that are listed in **pWhoCanPrecedeMe** and **pWhoCanFollowMe**.</span></span>

<span data-ttu-id="3da44-134">Um conjunto de entregas especifica os protocolos que seguem um protocolo.</span><span class="sxs-lookup"><span data-stu-id="3da44-134">A handoff set specifies the protocols that follow a protocol.</span></span> <span data-ttu-id="3da44-135">O analisador usa um conjunto de entrega somente quando o analisador pode identificar o próximo protocolo dos dados em uma instância de protocolo.</span><span class="sxs-lookup"><span data-stu-id="3da44-135">The parser uses a handoff set only when the parser can identify the next protocol from the data in a protocol instance.</span></span> <span data-ttu-id="3da44-136">Um conjunto de entregas é armazenado nos arquivos INI de cada analisador.</span><span class="sxs-lookup"><span data-stu-id="3da44-136">A handoff set is stored in the INI files of each parser.</span></span> <span data-ttu-id="3da44-137">Quando o analisador é instalado pela primeira vez, Monitor de Rede atualiza o conjunto de entrega dos protocolos analisadores listados em **pWhoHandsOffToMe** e **pWhoDoIHandOffTo**.</span><span class="sxs-lookup"><span data-stu-id="3da44-137">When the parser is installed for the first time, Network Monitor updates the handoff set of the parser protocols that are listed in **pWhoHandsOffToMe** and **pWhoDoIHandOffTo**.</span></span>



| <span data-ttu-id="3da44-138">Para obter informações sobre</span><span class="sxs-lookup"><span data-stu-id="3da44-138">For information on</span></span>                                               | <span data-ttu-id="3da44-139">Consulte</span><span class="sxs-lookup"><span data-stu-id="3da44-139">See</span></span>                                                                          |
|------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="3da44-140">Quais analisadores são e como eles funcionam com Monitor de Rede.</span><span class="sxs-lookup"><span data-stu-id="3da44-140">What parsers are, and how they work with Network Monitor.</span></span>        | [<span data-ttu-id="3da44-141">Analisadores</span><span class="sxs-lookup"><span data-stu-id="3da44-141">Parsers</span></span>](parsers.md)                                                       |
| <span data-ttu-id="3da44-142">O que os conjuntos de acompanhamento contêm.</span><span class="sxs-lookup"><span data-stu-id="3da44-142">What follow sets contain.</span></span>                                        | [<span data-ttu-id="3da44-143">Especificando um conjunto de acompanhamento</span><span class="sxs-lookup"><span data-stu-id="3da44-143">Specifying a Follow Set</span></span>](specifying-a-follow-set.md)                       |
| <span data-ttu-id="3da44-144">O que os conjuntos de entrega contêm.</span><span class="sxs-lookup"><span data-stu-id="3da44-144">What handoff sets contain.</span></span>                                       | [<span data-ttu-id="3da44-145">Especificando um conjunto de entrega</span><span class="sxs-lookup"><span data-stu-id="3da44-145">Specifying a Handoff Set</span></span>](specifying-a-handoff-set.md)                     |
| <span data-ttu-id="3da44-146">Quais pontos de entrada são incluídos na DLL do analisador.</span><span class="sxs-lookup"><span data-stu-id="3da44-146">What entry points are included in the parser DLL.</span></span>                | [<span data-ttu-id="3da44-147">Arquitetura de DLL do analisador</span><span class="sxs-lookup"><span data-stu-id="3da44-147">Parser DLL Architecture</span></span>](parser-dll-architecture.md)                       |
| <span data-ttu-id="3da44-148">Como implementar **ParserAutoInstallInfo**  inclui um exemplo.</span><span class="sxs-lookup"><span data-stu-id="3da44-148">How to implement **ParserAutoInstallInfo**  includes an example.</span></span> | [<span data-ttu-id="3da44-149">Implementando ParserAutoInstallInfo</span><span class="sxs-lookup"><span data-stu-id="3da44-149">Implementing ParserAutoInstallInfo</span></span>](implementing-parserautoinstallinfo.md) |



 

## <a name="requirements"></a><span data-ttu-id="3da44-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3da44-150">Requirements</span></span>



| <span data-ttu-id="3da44-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="3da44-151">Requirement</span></span> | <span data-ttu-id="3da44-152">Valor</span><span class="sxs-lookup"><span data-stu-id="3da44-152">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="3da44-153">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3da44-153">Minimum supported client</span></span><br/> | <span data-ttu-id="3da44-154">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="3da44-154">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="3da44-155">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3da44-155">Minimum supported server</span></span><br/> | <span data-ttu-id="3da44-156">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="3da44-156">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="3da44-157">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="3da44-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="3da44-158"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="3da44-158"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3da44-159">Confira também</span><span class="sxs-lookup"><span data-stu-id="3da44-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3da44-160">ParserAutoInstallInfo</span><span class="sxs-lookup"><span data-stu-id="3da44-160">ParserAutoInstallInfo</span></span>](parserautoinstallinfo.md)
</dt> <dt>

[<span data-ttu-id="3da44-161">seguir do PF \_</span><span class="sxs-lookup"><span data-stu-id="3da44-161">PF\_FOLLOWSET</span></span>](pf-followset.md)
</dt> <dt>

[<span data-ttu-id="3da44-162">teleentregador de PF \_</span><span class="sxs-lookup"><span data-stu-id="3da44-162">PF\_HANDOFFSET</span></span>](pf-handoffset.md)
</dt> <dt>

[<span data-ttu-id="3da44-163">PARSERDLLINFO de PF \_</span><span class="sxs-lookup"><span data-stu-id="3da44-163">PF\_PARSERDLLINFO</span></span>](pf-parserdllinfo.md)
</dt> </dl>

 

 




