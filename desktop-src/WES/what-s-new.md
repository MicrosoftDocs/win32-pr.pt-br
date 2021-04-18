---
title: O que há de novo (log de eventos do Windows)
description: Esta página resume os novos recursos que foram adicionados à API do log de eventos do Windows para cada versão.
ms.assetid: 90adf08c-177f-46ae-82e1-f7cca5a46db8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 652d82f67292316dd7aec599955d69dd70ab39a3
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "105781296"
---
# <a name="whats-new-windows-event-log"></a>O que há de novo (log de eventos do Windows)

Esta página resume os novos recursos que foram adicionados à API do log de eventos do Windows para cada versão.

## <a name="windows-7-and-windows-server-2008-r2"></a>Windows 7 e Windows Server 2008 R2

A seguir estão as alterações feitas no esquema [EventManifest](eventmanifestschema-schema.md) :

-   O tipo complexo [**TaskEventDefinitionType**](eventmanifestschema-taskeventdefinitiontype-complextype.md) foi removido. Para fornecer a mesma funcionalidade, use opcodes específicos da tarefa (consulte o elemento **opcodes** do tipo complexo [**TaskType**](eventmanifestschema-tasktype-complextype.md) .
-   Foram adicionados os tipos simples [**CSymbolType**](eventmanifestschema-csymboltype-simpletype.md), [**FilePath**](eventmanifestschema-filepath-simpletype.md)e [**strTableRef**](eventmanifestschema-strtableref-simpletype.md) para restringir valores atribuídos a atributos desses tipos.
-   Adicionado o atributo **Filters** ao tipo complexo [**ProviderType**](eventmanifestschema-providertype-complextype.md) . Os provedores podem usar filtros da mesma forma que os provedores usam o nível e as palavras-chave para determinar se devem gravar um evento.
-   Foram adicionados os seguintes tipos de saída que você pode especificar para itens de dados definidos em um modelo de dados de evento:
    -   Win: DateTimeCultureInsensitive
    -   Win: HResult
    -   Win: NTSTATUS
-   Os tipos de saída agora são respeitados, enquanto antes eles foram ignorados.

As seguintes alterações foram feitas na versão do compilador de [**mensagem**](message-compiler--mc-exe-.md) fornecida com a versão do Windows 7 do SDK do Windows:

-   Argumentos adicionados para que o compilador gere o código de log com base em seu manifesto. Você também pode solicitar que o compilador gere código para registrar eventos em sistemas operacionais anteriores ao Windows Vista. Para obter uma lista dos argumentos, consulte a seção "argumentos específicos para gerar código usado para registrar eventos" do tópico do [**compilador de mensagens**](message-compiler--mc-exe-.md) .
-   O compilador agora impõe uma validação semântica e sintática estrita no manifesto. Isso pode causar alguns manifestos que foram compilados com êxito em versões anteriores do compilador de mensagem para exigir alterações a fim de compilar com êxito usando a versão mais recente.
