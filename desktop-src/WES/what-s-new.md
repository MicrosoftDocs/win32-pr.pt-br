---
title: Novidades (Windows log de eventos)
description: Esta página resume os novos recursos que foram adicionados à API Windows log de eventos para cada versão.
ms.assetid: 90adf08c-177f-46ae-82e1-f7cca5a46db8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40f80af15d6f8b6d95533fff296ee22ea3c82d2add5f21964a7863ac3d676f5c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119904116"
---
# <a name="whats-new-windows-event-log"></a>Novidades (Windows log de eventos)

Esta página resume os novos recursos que foram adicionados à API Windows log de eventos para cada versão.

## <a name="windows-7-and-windows-server-2008-r2"></a>Windows 7 e Windows Server 2008 R2

Veja a seguir as alterações feitas no [esquema EventManifest:](eventmanifestschema-schema.md)

-   Removido o [**tipo complexo TaskEventDefinitionType.**](eventmanifestschema-taskeventdefinitiontype-complextype.md) Para fornecer a mesma funcionalidade, use opcodes específicos da tarefa (consulte o elemento **opcodes** do [**tipo complexo TaskType.**](eventmanifestschema-tasktype-complextype.md)
-   Adicionados os tipos simples [**CSymbolType**](eventmanifestschema-csymboltype-simpletype.md), [**filePath**](eventmanifestschema-filepath-simpletype.md)e [**strTableRef**](eventmanifestschema-strtableref-simpletype.md) para restringir valores atribuídos a atributos desses tipos.
-   Adicionado o **atributo filters** ao tipo [**complexo ProviderType.**](eventmanifestschema-providertype-complextype.md) Os provedores podem usar filtros da mesma maneira que os provedores usam palavras-chave e nível para determinar se devem gravar um evento.
-   Adicionados os seguintes tipos de saída que você pode especificar para itens de dados definidos em um modelo de dados de evento:
    -   win:DateTimeCultureInsensitive
    -   win:HResult
    -   win:NTSTATUS
-   Os tipos de saída agora são ignorados, enquanto antes eram ignorados.

As seguintes alterações foram feitas na versão do [**Compilador**](message-compiler--mc-exe-.md) de Mensagens que acompanha a versão Windows 7 do SDK do Windows:

-   Argumentos adicionados para que o compilador gere código de log com base em seu manifesto. Você também pode solicitar que o compilador gere código para registrar eventos em sistemas operacionais antes do Windows Vista. Para ver uma lista dos argumentos, consulte a seção "Argumentos específicos para gerar o código usado para registrar eventos" do tópico [**Compilador de**](message-compiler--mc-exe-.md) Mensagens.
-   O compilador agora impõe validação sintática e semântica mais estrita no manifesto. Isso pode fazer com que alguns manifestos compilados com êxito em versões anteriores do compilador de mensagens exigem alterações para compilar com êxito usando a versão mais recente.
