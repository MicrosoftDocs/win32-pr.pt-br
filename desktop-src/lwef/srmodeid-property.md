---
title: Propriedade SRModeID
description: Propriedade SRModeID
ms.assetid: 4c784fc5-d2c2-4e5b-ba5f-f59b4507f40f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 898f90a70c29d409eaa12df3d3fde845e35bd5ff
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105786259"
---
# <a name="srmodeid-property"></a>Propriedade SRModeID

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**
</dt> <dd>

Retorna ou define o mecanismo de reconhecimento de fala usado pelo caractere.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

*agente do ***. Caracteres ("*** characterid * * *").* *  \[  =  *Modeid* SRModeID\]



| Parte     | Descrição                                                             |
|----------|-------------------------------------------------------------------------|
| *Modeid* | Uma expressão de cadeia de caracteres que corresponde à ID de modo de um mecanismo de fala. |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

A propriedade determina o mecanismo de reconhecimento de fala usado pelo caractere para entrada de fala. A ID de modo para um mecanismo de reconhecimento de fala é uma cadeia de caracteres formatada definida pelo fornecedor de fala que identifica exclusivamente o mecanismo. Para obter mais informações, consulte [acessando um mecanismo de fala em seu código](accessing-a-speech-engine-in-your-code.md).

Se você especificar uma ID de modo para um mecanismo de fala que não está instalado, se o usuário tiver desabilitado o reconhecimento de fala (na folha de propriedades do Microsoft Agent) ou se o idioma do mecanismo de fala especificado não corresponder à configuração de [**LanguageID**](languageid-property.md) do caractere, o servidor gerará um erro.

Se você consultar essa propriedade e ainda não tiver (com êxito) definir o mecanismo de reconhecimento de fala, o servidor retornará a ID de modo do mecanismo que o SAPI retorna com base na configuração [**LanguageID**](languageid-property.md) do caractere. Se você não tiver definido a **LanguageID** do caractere, o Agent retornará a ID de modo do mecanismo que o SAPI retorna com base na configuração de ID de idioma padrão do usuário. Se não houver nenhum mecanismo correspondente, o servidor retornará uma cadeia de caracteres vazia (""). A consulta dessa propriedade não exige que [**SpeechInput. Enabled**](https://www.bing.com/search?q=**SpeechInput.Enabled**) seja definido como **true**. No entanto, se você consultar a propriedade quando a entrada de fala estiver desabilitada, o servidor retornará uma cadeia de caracteres vazia.

Quando a entrada de fala está habilitada (na janela Opções de caractere avançado), a consulta ou a configuração dessa propriedade carregará o mecanismo associado (se ele ainda não estiver carregado) e iniciará os serviços de fala. Ou seja, a chave de escuta está disponível e a dica de escuta é exibível. (A chave de escuta e a dica de escuta serão habilitadas somente se elas também estiverem habilitadas em opções de caractere avançadas.) No entanto, se você consultar a propriedade quando a fala estiver desabilitada, o servidor não iniciará os serviços de fala.

Essa propriedade aplica-se somente ao uso do caractere do aplicativo cliente; a configuração não afeta outros clientes do caractere ou outros caracteres do seu aplicativo cliente.

Os requisitos do mecanismo de fala do Microsoft Agent são baseados no Microsoft Speech API. Os mecanismos que dão suporte aos requisitos SAPI do Microsoft Agent podem ser instalados e usados com o Agent.

> [!Note]  
> Essa propriedade também retornará a cadeia de caracteres vazia se você não tiver nenhum suporte de som compatível instalado no sistema.

 

> [!Note]  
> A consulta dessa propriedade normalmente não retorna um erro. No entanto, se o mecanismo de fala demorar muito tempo para ser carregado, você poderá receber um erro indicando que a consulta atingiu o tempo limite.

 

## <a name="see-also"></a>Consulte Também

[**Propriedade LanguageID**](languageid-property.md)


 

 




