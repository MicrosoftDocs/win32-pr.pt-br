---
description: As ações personalizadas do ICE se comunicam chamando MsiProcessMessage e postando uma mensagem de tipo de usuário do INSTALLMESSAGE \_ .
ms.assetid: 36307589-de0e-4eaf-b439-e7ba3cd96fb3
title: Diretrizes de mensagens ICE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf4bee7dbf22184883e49da4d5a5f66f9debb577
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920868"
---
# <a name="ice-message-guidelines"></a><span data-ttu-id="1cde9-103">Diretrizes de mensagens ICE</span><span class="sxs-lookup"><span data-stu-id="1cde9-103">ICE Message Guidelines</span></span>

<span data-ttu-id="1cde9-104">As ações personalizadas do ICE se comunicam chamando [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) e postando uma mensagem de tipo de usuário do INSTALLMESSAGE \_ .</span><span class="sxs-lookup"><span data-stu-id="1cde9-104">ICE custom actions communicate by calling [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) and posting an INSTALLMESSAGE\_USER type message.</span></span>

<span data-ttu-id="1cde9-105">Ao criar uma cadeia de caracteres de mensagem para uma ação personalizada de ICE, formate a cadeia de caracteres da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="1cde9-105">When authoring a message string for an ICE custom action, format the string as follows.</span></span>

<span data-ttu-id="1cde9-106">*Nome do Ice* <tab> *Tipo* <tab> de mensagem *Descrição* <tab> do *URL de ajuda ou local* <tab> *Nome* <tab> da tabela *Nome* <tab> da coluna *Chave primária* <tab> *Chave primária* <tab> *Chave primária* .</span><span class="sxs-lookup"><span data-stu-id="1cde9-106">*Name of ICE* <tab> *Message Type* <tab> *Description* <tab> *Help URL or location* <tab> *Table Name* <tab> *Column Name* <tab> *Primary Key* <tab> *Primary Key* <tab> *Primary Key* .</span></span> <span data-ttu-id="1cde9-107">.</span><span class="sxs-lookup"><span data-stu-id="1cde9-107">.</span></span> <span data-ttu-id="1cde9-108">.</span><span class="sxs-lookup"><span data-stu-id="1cde9-108">.</span></span> <span data-ttu-id="1cde9-109">(repita para quantas chaves primárias forem necessárias)</span><span class="sxs-lookup"><span data-stu-id="1cde9-109">(repeat for as many primary keys as needed)</span></span>

<span data-ttu-id="1cde9-110">Os três primeiros campos da cadeia de caracteres são necessários em cada mensagem.</span><span class="sxs-lookup"><span data-stu-id="1cde9-110">The first three fields of the string are required in every message.</span></span>

<span data-ttu-id="1cde9-111">O campo tipo de mensagem Especifica se o ICE relata uma mensagem de falha, erro, aviso ou informativa.</span><span class="sxs-lookup"><span data-stu-id="1cde9-111">The Message Type field specifies whether the ICE reports a Failure, Error, Warning, or Informational message.</span></span>



| <span data-ttu-id="1cde9-112">Valor</span><span class="sxs-lookup"><span data-stu-id="1cde9-112">Value</span></span> | <span data-ttu-id="1cde9-113">Tipo de mensagem</span><span class="sxs-lookup"><span data-stu-id="1cde9-113">Message type</span></span>                                                                                                                                                          |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1cde9-114">0</span><span class="sxs-lookup"><span data-stu-id="1cde9-114">0</span></span>     | <span data-ttu-id="1cde9-115">Mensagem de falha relatando a falha da ação personalizada do ICE.</span><span class="sxs-lookup"><span data-stu-id="1cde9-115">Failure message reporting the failure of the ICE custom action.</span></span>                                                                                                       |
| <span data-ttu-id="1cde9-116">1</span><span class="sxs-lookup"><span data-stu-id="1cde9-116">1</span></span>     | <span data-ttu-id="1cde9-117">Mensagem de erro que relata a criação do banco de dados que causa comportamento incorreto.</span><span class="sxs-lookup"><span data-stu-id="1cde9-117">Error message reporting database authoring that cause incorrect behavior.</span></span>                                                                                             |
| <span data-ttu-id="1cde9-118">2</span><span class="sxs-lookup"><span data-stu-id="1cde9-118">2</span></span>     | <span data-ttu-id="1cde9-119">Mensagem de aviso que relata a criação de banco de dados que causa comportamento incorreto em determinados casos.</span><span class="sxs-lookup"><span data-stu-id="1cde9-119">Warning message reporting database authoring that causes incorrect behavior in certain cases.</span></span> <span data-ttu-id="1cde9-120">Os avisos também podem relatar efeitos colaterais inesperados de criação de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="1cde9-120">Warnings can also report unexpected side-effects of database authoring.</span></span> |
| <span data-ttu-id="1cde9-121">3</span><span class="sxs-lookup"><span data-stu-id="1cde9-121">3</span></span>     | <span data-ttu-id="1cde9-122">Mensagem informativa.</span><span class="sxs-lookup"><span data-stu-id="1cde9-122">Informational message.</span></span>                                                                                                                                                |



 

<span data-ttu-id="1cde9-123">Se a ajuda não estiver disponível, o campo URL da ajuda poderá ser a cadeia de caracteres vazia.</span><span class="sxs-lookup"><span data-stu-id="1cde9-123">If help is not available, the Help URL field may be the empty string.</span></span>

<span data-ttu-id="1cde9-124">Mensagens de erro e de aviso devem fornecer o nome da tabela, o nome da coluna e os campos de chave primária.</span><span class="sxs-lookup"><span data-stu-id="1cde9-124">Error and Warning messages should provide the Table Name, Column Name, and Primary Key fields.</span></span> <span data-ttu-id="1cde9-125">Se qualquer um desses campos for omitido, todos os campos após o primeiro campo em branco deverão ser deixados fora da mensagem.</span><span class="sxs-lookup"><span data-stu-id="1cde9-125">If any of these fields are omitted, all of the fields following the first blank field must be left out of the message.</span></span> <span data-ttu-id="1cde9-126">Por exemplo, é fornecido um nome de tabela sem um nome de coluna e chaves primárias ou um nome de tabela e um nome de coluna é fornecido sem chaves primárias.</span><span class="sxs-lookup"><span data-stu-id="1cde9-126">For example, a table name is provided without a column name and primary keys or a table name and a column name is provided with no primary keys.</span></span> <span data-ttu-id="1cde9-127">No entanto, um nome de coluna e chaves primárias não podem ser usados sem um nome de tabela.</span><span class="sxs-lookup"><span data-stu-id="1cde9-127">However a column name and primary keys cannot be used without a table name.</span></span> <span data-ttu-id="1cde9-128">Várias chaves primárias podem ser listadas até que todas as chaves primárias nessa tabela tenham valores fornecidos.</span><span class="sxs-lookup"><span data-stu-id="1cde9-128">Multiple primary keys may be listed until all the primary keys in that table have been given values.</span></span>

## <a name="examples"></a><span data-ttu-id="1cde9-129">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1cde9-129">Examples</span></span>

<span data-ttu-id="1cde9-130">A primeira mensagem ilustrada pelo [Ice de exemplo em C++](sample-ice-in-c-.md):</span><span class="sxs-lookup"><span data-stu-id="1cde9-130">The first message illustrated by the [Sample ICE in C++](sample-ice-in-c-.md):</span></span>

<span data-ttu-id="1cde9-131">"ICE01 \\ T3 \\ tCreated 04/29/1998 por <inserir nome do autor aqui>".</span><span class="sxs-lookup"><span data-stu-id="1cde9-131">"ICE01\\t3\\tCreated 04/29/1998 by <insert author's name here>."</span></span>

<span data-ttu-id="1cde9-132">A segunda mensagem postada pelo ICE de exemplo:</span><span class="sxs-lookup"><span data-stu-id="1cde9-132">The second message posted by the sample ICE:</span></span>

<span data-ttu-id="1cde9-133">"ICE01 \\ T3 \\ tLast modificou 05/06/1999 por <inserir nome do autor aqui>".</span><span class="sxs-lookup"><span data-stu-id="1cde9-133">"ICE01\\t3\\tLast modified 05/06/1999 by <insert author's name here>."</span></span>

<span data-ttu-id="1cde9-134">A terceira mensagem postada pelo ICE de exemplo.</span><span class="sxs-lookup"><span data-stu-id="1cde9-134">The third message posted by the sample ICE.</span></span>

<span data-ttu-id="1cde9-135">"ICE01 \\ T3 \\ tSimple Ice para ilustrar o conceito de Ice".</span><span class="sxs-lookup"><span data-stu-id="1cde9-135">"ICE01\\t3\\tSimple ICE to illustrating the ICE concept".</span></span>

 

 



