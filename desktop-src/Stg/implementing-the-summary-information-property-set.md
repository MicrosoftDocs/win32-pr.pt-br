---
title: Implementando o conjunto de propriedades de informações de resumo
description: Há diretrizes a serem seguidas ao implementar um conjunto de propriedades de informações resumidas para o armazenamento estruturado.
ms.assetid: e1204de5-b712-4bd5-bffb-6a12ec8d7052
keywords:
- Implementando o conjunto de propriedades de informações de resumo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69e5ae6208aa5cb7a325d1cccf77f17e969c5b75
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103634835"
---
# <a name="implementing-the-summary-information-property-set"></a><span data-ttu-id="507af-104">Implementando o conjunto de propriedades de informações de resumo</span><span class="sxs-lookup"><span data-stu-id="507af-104">Implementing the Summary Information Property Set</span></span>

<span data-ttu-id="507af-105">Há diretrizes a serem seguidas ao implementar um conjunto de propriedades de informações resumidas para o armazenamento estruturado.</span><span class="sxs-lookup"><span data-stu-id="507af-105">There are guidelines to follow when implementing a summary information property set for Structured Storage.</span></span>

<span data-ttu-id="507af-106">Veja a seguir as diretrizes para implementar [o conjunto de propriedades Resumo de informações](the-summary-information-property-set.md):</span><span class="sxs-lookup"><span data-stu-id="507af-106">The following are the guidelines for implementing [The Summary Information Property Set](the-summary-information-property-set.md):</span></span>

-   <span data-ttu-id="507af-107">**Pid \_ MODELO** refere-se a um documento externo contendo informações de formato e estilo.</span><span class="sxs-lookup"><span data-stu-id="507af-107">**PID\_TEMPLATE** refers to an external document containing format and style information.</span></span> <span data-ttu-id="507af-108">O processo pelo qual o modelo está localizado é definido pela implementação.</span><span class="sxs-lookup"><span data-stu-id="507af-108">The process by which the template is located is implementation-defined.</span></span>
-   <span data-ttu-id="507af-109">**Pid \_ LASTAUTHOR** é o nome armazenado nas informações do usuário pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="507af-109">**PID\_LASTAUTHOR** is the name stored in User Information by the application.</span></span> <span data-ttu-id="507af-110">Por exemplo, Mary cria um documento em seu computador e o fornece a João, que, em seguida, modifica e salva.</span><span class="sxs-lookup"><span data-stu-id="507af-110">For example, Mary creates a document on her computer and gives it to John, who then modifies and saves it.</span></span> <span data-ttu-id="507af-111">Mary é o autor, João é o último salvo por valor.</span><span class="sxs-lookup"><span data-stu-id="507af-111">Mary is the author, John is the last saved by value.</span></span>
-   <span data-ttu-id="507af-112">**Pid \_ REVNUMBER** é o número de vezes que o comando arquivo/salvar foi chamado neste documento.</span><span class="sxs-lookup"><span data-stu-id="507af-112">**PID\_REVNUMBER** is the number of times the File/Save command has been called on this document.</span></span>
-   <span data-ttu-id="507af-113">Cada um dos valores de data/hora deve ser armazenado em UTC (horário coordenado universal).</span><span class="sxs-lookup"><span data-stu-id="507af-113">Each of the date/time values must be stored in Universal Coordinated Time (UTC).</span></span>
-   <span data-ttu-id="507af-114">**Pid \_ CREATE \_ DTM** é uma propriedade somente leitura; Essa propriedade deve ser definida quando um documento é criado, mas não deve ser alterada posteriormente.</span><span class="sxs-lookup"><span data-stu-id="507af-114">**PID\_CREATE\_DTM** is a read-only property; this property should be set when a document is created, but should not be subsequently changed.</span></span>
-   <span data-ttu-id="507af-115">Para **a \_ miniatura de PID**, os aplicativos devem armazenar dados no formato de **\_ METAFILEPICT** do CF **ou do CF \_** .</span><span class="sxs-lookup"><span data-stu-id="507af-115">For **PID\_THUMBNAIL**, applications should store data in **CF\_DIB** or **CF\_METAFILEPICT** format.</span></span> <span data-ttu-id="507af-116">**CF \_ METAFILEPICT** é recomendado.</span><span class="sxs-lookup"><span data-stu-id="507af-116">**CF\_METAFILEPICT** is recommended.</span></span>
-   <span data-ttu-id="507af-117">**Pid \_ SEGURANÇA** é o nível de segurança sugerido para o documento.</span><span class="sxs-lookup"><span data-stu-id="507af-117">**PID\_SECURITY** is the suggested security level for the document.</span></span> <span data-ttu-id="507af-118">Ao observar o nível de segurança no documento, um aplicativo que não seja o originador do documento pode ajustar sua interface do usuário para as propriedades.</span><span class="sxs-lookup"><span data-stu-id="507af-118">By noting the security level on the document, an application other than the originator of the document can adjust its user interface to the properties.</span></span> <span data-ttu-id="507af-119">Um aplicativo não deve exibir nenhuma informação sobre um documento protegido por senha ou habilitar modificações em documentos Read-Only ou bloqueados para anotações em vigor.</span><span class="sxs-lookup"><span data-stu-id="507af-119">An application should not display any information about a password-protected document or enable modifications to enforced Read-Only or Locked-for-Annotations documents.</span></span> <span data-ttu-id="507af-120">Se o usuário tentar modificar as propriedades, o aplicativo deverá avisar o usuário sobre o status de Read-Only recomendado.</span><span class="sxs-lookup"><span data-stu-id="507af-120">If the user attempts to modify properties, the application should warn the user about the Read-Only Recommended status.</span></span>



| <span data-ttu-id="507af-121">Nível de segurança</span><span class="sxs-lookup"><span data-stu-id="507af-121">Security level</span></span>         | <span data-ttu-id="507af-122">Valor</span><span class="sxs-lookup"><span data-stu-id="507af-122">Value</span></span> |
|------------------------|-------|
| <span data-ttu-id="507af-123">Nenhum</span><span class="sxs-lookup"><span data-stu-id="507af-123">None</span></span>                   | <span data-ttu-id="507af-124">0</span><span class="sxs-lookup"><span data-stu-id="507af-124">0</span></span>     |
| <span data-ttu-id="507af-125">Protegido por senha</span><span class="sxs-lookup"><span data-stu-id="507af-125">Password protected</span></span>     | <span data-ttu-id="507af-126">1</span><span class="sxs-lookup"><span data-stu-id="507af-126">1</span></span>     |
| <span data-ttu-id="507af-127">Somente leitura recomendado</span><span class="sxs-lookup"><span data-stu-id="507af-127">Read-only recommended</span></span>  | <span data-ttu-id="507af-128">2</span><span class="sxs-lookup"><span data-stu-id="507af-128">2</span></span>     |
| <span data-ttu-id="507af-129">Imposto somente leitura</span><span class="sxs-lookup"><span data-stu-id="507af-129">Read-only enforced</span></span>     | <span data-ttu-id="507af-130">4</span><span class="sxs-lookup"><span data-stu-id="507af-130">4</span></span>     |
| <span data-ttu-id="507af-131">Bloqueado para anotações</span><span class="sxs-lookup"><span data-stu-id="507af-131">Locked for annotations</span></span> | <span data-ttu-id="507af-132">8</span><span class="sxs-lookup"><span data-stu-id="507af-132">8</span></span>     |



 

 

 




