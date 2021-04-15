---
description: Este tópico contém informações sobre como escrever um analisador de protocolo e inclui exemplos das funções de exportação que a DLL do analisador deve implementar.
ms.assetid: 0be87b33-aab0-4986-8a86-914e0a7b8f2d
title: Gravando um analisador de protocolo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 338c224dd036df747af6ab805dae273f6ad3f510
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104505754"
---
# <a name="writing-a-protocol-parser"></a><span data-ttu-id="cb772-103">Gravando um analisador de protocolo</span><span class="sxs-lookup"><span data-stu-id="cb772-103">Writing a Protocol Parser</span></span>

<span data-ttu-id="cb772-104">Este tópico contém informações sobre como escrever um analisador de protocolo e inclui exemplos das funções de exportação que a DLL do analisador deve implementar.</span><span class="sxs-lookup"><span data-stu-id="cb772-104">This topic contains information about writing a protocol parser, and includes examples of the export functions that the parser DLL must implement.</span></span>

<span data-ttu-id="cb772-105">Os tópicos a seguir estão incluídos nesta seção.</span><span class="sxs-lookup"><span data-stu-id="cb772-105">The following topics are included in this section.</span></span>



| <span data-ttu-id="cb772-106">Termo</span><span class="sxs-lookup"><span data-stu-id="cb772-106">Term</span></span>                                                                                                                                                                                                                                                             | <span data-ttu-id="cb772-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="cb772-107">Description</span></span>                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb772-108"><span id="Programming_Considerations"></span><span id="programming_considerations"></span><span id="PROGRAMMING_CONSIDERATIONS"></span>[Considerações sobre programação](programming-considerations.md)</span><span class="sxs-lookup"><span data-stu-id="cb772-108"><span id="Programming_Considerations"></span><span id="programming_considerations"></span><span id="PROGRAMMING_CONSIDERATIONS"></span>[Programming Considerations](programming-considerations.md)</span></span><br/>                                                   | <span data-ttu-id="cb772-109">Identifica as dicas básicas de programação para ajudá-lo a escrever uma DLL do analisador.</span><span class="sxs-lookup"><span data-stu-id="cb772-109">Identifies the basic programming tips to help you write a parser DLL.</span></span><br/>                                                                                    |
| <span data-ttu-id="cb772-110"><span id="Implementing_Parser_Export_Functions"></span><span id="implementing_parser_export_functions"></span><span id="IMPLEMENTING_PARSER_EXPORT_FUNCTIONS"></span>[Implementando funções de exportação do parser](implementing-parser-export-functions.md)</span><span class="sxs-lookup"><span data-stu-id="cb772-110"><span id="Implementing_Parser_Export_Functions"></span><span id="implementing_parser_export_functions"></span><span id="IMPLEMENTING_PARSER_EXPORT_FUNCTIONS"></span>[Implementing Parser Export Functions](implementing-parser-export-functions.md)</span></span><br/> | <span data-ttu-id="cb772-111">Fornece exemplos de implementação de funções de exportação.</span><span class="sxs-lookup"><span data-stu-id="cb772-111">Provides examples of implementing export functions.</span></span><br/>                                                                                                      |
| <span data-ttu-id="cb772-112"><span id="Formatting_Displayed_Data"></span><span id="formatting_displayed_data"></span><span id="FORMATTING_DISPLAYED_DATA"></span>[Formatando dados exibidos](formatting-displayed-data.md)</span><span class="sxs-lookup"><span data-stu-id="cb772-112"><span id="Formatting_Displayed_Data"></span><span id="formatting_displayed_data"></span><span id="FORMATTING_DISPLAYED_DATA"></span>[Formatting Displayed Data](formatting-displayed-data.md)</span></span><br/>                                                        | <span data-ttu-id="cb772-113">Identifica o processo de formatação de dados que são exibidos no painel de detalhes da interface do usuário do Monitor de Rede.</span><span class="sxs-lookup"><span data-stu-id="cb772-113">Identifies the process of formatting data that is displayed in the details pane of the Network Monitor UI.</span></span><br/>                                               |
| <span data-ttu-id="cb772-114"><span id="Specifying_a_Follow_Set"></span><span id="specifying_a_follow_set"></span><span id="SPECIFYING_A_FOLLOW_SET"></span>[Especificando um conjunto de acompanhamento](specifying-a-follow-set.md)</span><span class="sxs-lookup"><span data-stu-id="cb772-114"><span id="Specifying_a_Follow_Set"></span><span id="specifying_a_follow_set"></span><span id="SPECIFYING_A_FOLLOW_SET"></span>[Specifying a Follow Set](specifying-a-follow-set.md)</span></span><br/>                                                                  | <span data-ttu-id="cb772-115">Identifica o processo de especificar um conjunto de acompanhamento e mostra como Monitor de Rede acessa o conjunto de acompanhamento de um analisador para determinar o próximo protocolo.</span><span class="sxs-lookup"><span data-stu-id="cb772-115">Identifies the process of specifying a follow set, and shows you how Network Monitor accesses the follow set of a parser to determine the next protocol.</span></span><br/> |
| <span data-ttu-id="cb772-116"><span id="Specifying_a_Handoff_Set"></span><span id="specifying_a_handoff_set"></span><span id="SPECIFYING_A_HANDOFF_SET"></span>[Especificando um conjunto de entrega](specifying-a-handoff-set.md)</span><span class="sxs-lookup"><span data-stu-id="cb772-116"><span id="Specifying_a_Handoff_Set"></span><span id="specifying_a_handoff_set"></span><span id="SPECIFYING_A_HANDOFF_SET"></span>[Specifying a Handoff Set](specifying-a-handoff-set.md)</span></span><br/>                                                             | <span data-ttu-id="cb772-117">Identifica o processo de especificar um conjunto de entregas e mostra como o analisador acessa seu conjunto de entrega para obter um identificador para o próximo protocolo.</span><span class="sxs-lookup"><span data-stu-id="cb772-117">Identifies the process of specifying a handoff set, and shows you how the parser accesses its handoff set to get a handle to the next protocol.</span></span><br/>          |



 

 

 




