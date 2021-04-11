---
description: A função de exportação ParserAutoInstallInfo identifica o analisador ou analisadores que estão localizados em uma DLL. ParserAutoInstallInfo deve ser implementado em todas as DLLs do analisador.
ms.assetid: 7af3bf3c-d415-4af9-8f5c-c9a76535bd1a
title: Função de retorno de chamada ParserAutoInstallInfo (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ParserAutoInstallInfo
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: 7702ae8aad5ae24acf3835451b7b8eff3a26ceb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296197"
---
# <a name="parserautoinstallinfo-callback-function"></a><span data-ttu-id="daac2-104">Função de retorno de chamada ParserAutoInstallInfo</span><span class="sxs-lookup"><span data-stu-id="daac2-104">ParserAutoInstallInfo callback function</span></span>

<span data-ttu-id="daac2-105">A função de exportação **ParserAutoInstallInfo** identifica o analisador ou analisadores que estão localizados em uma dll.</span><span class="sxs-lookup"><span data-stu-id="daac2-105">The **ParserAutoInstallInfo** export function identifies the parser, or parsers that are located in a DLL.</span></span> <span data-ttu-id="daac2-106">**ParserAutoInstallInfo** deve ser implementado em todas as DLLs do analisador.</span><span class="sxs-lookup"><span data-stu-id="daac2-106">**ParserAutoInstallInfo** should be implemented in all parser DLLs.</span></span>

## <a name="syntax"></a><span data-ttu-id="daac2-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="daac2-107">Syntax</span></span>


```C++
PPF_PARSERDLLINFO WINAPI ParserAutoInstallInfo(void);
```



## <a name="parameters"></a><span data-ttu-id="daac2-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="daac2-108">Parameters</span></span>

<span data-ttu-id="daac2-109">Esta função de retorno de chamada não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="daac2-109">This callback function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="daac2-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="daac2-110">Return value</span></span>

<span data-ttu-id="daac2-111">Se a função for bem-sucedida, o valor de retorno será uma estrutura de [ \_ PARSERDLLINFO de PF](pf-parserdllinfo.md) que descreve os analisadores na dll.</span><span class="sxs-lookup"><span data-stu-id="daac2-111">If the function is successful, the return value is a [PF\_PARSERDLLINFO](pf-parserdllinfo.md) structure that describes the parsers in the DLL.</span></span>

<span data-ttu-id="daac2-112">Se a função não for bem-sucedida, o valor de retorno será **false**.</span><span class="sxs-lookup"><span data-stu-id="daac2-112">If the function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="daac2-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="daac2-113">Remarks</span></span>

<span data-ttu-id="daac2-114">Quando Monitor de Rede é carregado pela primeira vez, ele chama **ParserAutoInstallInfo** (se existir) para instalar automaticamente cada analisador e, em seguida, enumera todas as DLLs do analisador no subdiretório do analisador.</span><span class="sxs-lookup"><span data-stu-id="daac2-114">When Network Monitor loads for the first time, it calls **ParserAutoInstallInfo** (if it exists) to automatically install each parser, and then enumerate all the parser DLLs in the parser subdirectory.</span></span>

<span data-ttu-id="daac2-115">As informações retornadas na estrutura **PF \_ PARSERDLLINFO** incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="daac2-115">The information returned in the **PF\_PARSERDLLINFO** structure includes the following:</span></span>

-   <span data-ttu-id="daac2-116">O número de analisadores na DLL (normalmente um).</span><span class="sxs-lookup"><span data-stu-id="daac2-116">The number of parsers in the DLL (typically one).</span></span>
-   <span data-ttu-id="daac2-117">O nome e uma breve descrição do protocolo que cada analisador detecta.</span><span class="sxs-lookup"><span data-stu-id="daac2-117">The name and a brief description of the protocol that each parser detects.</span></span>
-   <span data-ttu-id="daac2-118">Um arquivo de ajuda opcional para cada protocolo.</span><span class="sxs-lookup"><span data-stu-id="daac2-118">An optional Help file for each protocol.</span></span>
-   <span data-ttu-id="daac2-119">Os protocolos que precedem cada protocolo.</span><span class="sxs-lookup"><span data-stu-id="daac2-119">The protocols that precede each protocol.</span></span>
-   <span data-ttu-id="daac2-120">Os protocolos que seguem cada protocolo.</span><span class="sxs-lookup"><span data-stu-id="daac2-120">The protocols that follow each protocol.</span></span>

<span data-ttu-id="daac2-121">Cada DLL do analisador deve conter um analisador.</span><span class="sxs-lookup"><span data-stu-id="daac2-121">Each parser DLL should contain one parser.</span></span> <span data-ttu-id="daac2-122">No entanto, Monitor de Rede permite que você crie uma DLL que contenha mais de um analisador.</span><span class="sxs-lookup"><span data-stu-id="daac2-122">However, Network Monitor allows you to create a DLL that contains more than one parser.</span></span> <span data-ttu-id="daac2-123">Por exemplo, tcpip.dll é uma DLL Monitor de Rede com mais de um analisador.</span><span class="sxs-lookup"><span data-stu-id="daac2-123">For example, tcpip.dll is a Network Monitor DLL with more than one parser.</span></span>



| <span data-ttu-id="daac2-124">Para obter informações sobre</span><span class="sxs-lookup"><span data-stu-id="daac2-124">For information on</span></span>                                               | <span data-ttu-id="daac2-125">Consulte</span><span class="sxs-lookup"><span data-stu-id="daac2-125">See</span></span>                                                                          |
|------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="daac2-126">Quais analisadores são e como eles funcionam com Monitor de Rede.</span><span class="sxs-lookup"><span data-stu-id="daac2-126">What parsers are, and how they work with Network Monitor.</span></span>        | [<span data-ttu-id="daac2-127">Analisadores</span><span class="sxs-lookup"><span data-stu-id="daac2-127">Parsers</span></span>](parsers.md)                                                       |
| <span data-ttu-id="daac2-128">Quais pontos de entrada são incluídos na DLL do analisador.</span><span class="sxs-lookup"><span data-stu-id="daac2-128">Which entry points are included in the parser DLL.</span></span>               | [<span data-ttu-id="daac2-129">Arquitetura de DLL do analisador</span><span class="sxs-lookup"><span data-stu-id="daac2-129">Parser DLL Architecture</span></span>](parser-dll-architecture.md)                       |
| <span data-ttu-id="daac2-130">Como implementar **ParserAutoInstallInfo**  inclui um exemplo.</span><span class="sxs-lookup"><span data-stu-id="daac2-130">How to implement **ParserAutoInstallInfo**  includes an example.</span></span> | [<span data-ttu-id="daac2-131">Implementando ParserAutoInstallInfo</span><span class="sxs-lookup"><span data-stu-id="daac2-131">Implementing ParserAutoInstallInfo</span></span>](implementing-parserautoinstallinfo.md) |



 

## <a name="requirements"></a><span data-ttu-id="daac2-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="daac2-132">Requirements</span></span>



| <span data-ttu-id="daac2-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="daac2-133">Requirement</span></span> | <span data-ttu-id="daac2-134">Valor</span><span class="sxs-lookup"><span data-stu-id="daac2-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="daac2-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="daac2-135">Minimum supported client</span></span><br/> | <span data-ttu-id="daac2-136">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="daac2-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="daac2-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="daac2-137">Minimum supported server</span></span><br/> | <span data-ttu-id="daac2-138">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="daac2-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="daac2-139">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="daac2-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="daac2-140"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="daac2-140"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="daac2-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="daac2-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="daac2-142">PARSERDLLINFO de PF \_</span><span class="sxs-lookup"><span data-stu-id="daac2-142">PF\_PARSERDLLINFO</span></span>](pf-parserdllinfo.md)
</dt> </dl>

 

 




