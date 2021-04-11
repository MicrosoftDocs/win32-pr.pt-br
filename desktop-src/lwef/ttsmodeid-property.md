---
title: Propriedade TTSModeID
description: Propriedade TTSModeID
ms.assetid: 9205c37e-e006-466a-9b33-b98408c01ed7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6852f203f5df716df6cfc5962f9cfa911d8fc1a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104160276"
---
# <a name="ttsmodeid-property"></a>Propriedade TTSModeID

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**
</dt> <dd>

Retorna ou define o modo do mecanismo de TTS usado para o caractere.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

*agente do ***. Caracteres ("*** characterid * * *").* *  \[  =  *Modeid* TTSModeID\]



| Parte     | Descrição                                                             |
|----------|-------------------------------------------------------------------------|
| *Modeid* | Uma expressão de cadeia de caracteres que corresponde à ID de modo de um mecanismo de fala. |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

Esta propriedade determina a ID do modo de mecanismo de TTS (conversão de texto em fala) para a saída falada de um caractere. A ID de modo para um mecanismo de TTS é uma cadeia de caracteres formatada definida pelo fornecedor de fala que identifica exclusivamente o modo do mecanismo. Para obter mais informações, consulte [acessando um mecanismo de fala em seu código](accessing-a-speech-engine-in-your-code.md).

Definir essa propriedade substitui a tentativa do servidor de carregar um mecanismo com base na configuração de TTS compilada do caractere e na configuração [**LanguageID**](languageid-property.md) atual do caractere. No entanto, se você especificar uma ID de modo para um mecanismo que não está instalado ou se o usuário tiver desabilitado a saída de fala na folha de propriedades do Microsoft Agent (**AudioOutput. Enabled = False**), o servidor gerará um erro.

Se você não tiver definido (ou não com êxito) uma ID de modo TTS para o caractere, o servidor verificará se a configuração do modo TTS compilado do caractere corresponde à configuração [**LanguageID**](languageid-property.md) do caractere e se o mecanismo de TTS associado está instalado. Nesse caso, o modo TTS usado pelo caractere para a saída falada e essa propriedade retorna essa ID de modo. Caso contrário, o servidor solicitará um mecanismo de fala de SAPI compatível que corresponda à **LanguageID** do caractere, bem como o gênero e a idade definidos para a ID do modo compilado do caractere. Se você não tiver definido o **LanguageID** do caractere, sua **LanguageID** será o idioma atual do usuário. Se nenhum mecanismo de correspondência puder ser encontrado, a consulta para essa propriedade retornará uma cadeia de caracteres vazia para a ID de modo do mecanismo. Da mesma forma, se você consultar essa propriedade quando o usuário tiver desabilitado a saída de fala na folha de propriedades do Microsoft Agent (**AudioOutput. Enabled = False**), o valor será uma cadeia de caracteres vazia.

Consultar ou definir essa propriedade carregará o mecanismo associado (se ele ainda não estiver carregado). No entanto, se o mecanismo especificado na configuração TTS compilada do caractere estiver instalado e corresponder à configuração de ID de idioma do caractere, o mecanismo será carregado quando o caractere for carregado.

Essa propriedade aplica-se somente ao uso do caractere do aplicativo cliente; a configuração não afeta outros clientes do caractere ou outros caracteres do seu aplicativo cliente.

Os requisitos do mecanismo de fala do Microsoft Agent são baseados no Microsoft Speech API. Os mecanismos que dão suporte aos requisitos SAPI do Microsoft Agent podem ser instalados e usados com o Agent.

> [!Note]  
> Essa propriedade também retornará a cadeia de caracteres vazia se você não tiver nenhum suporte de som compatível instalado no sistema.

 

> [!Note]  
> A configuração do **TTSModeID** pode falhar se o Speech.dll não estiver instalado e o mecanismo especificado não corresponder à configuração do modo TTS compilado do caractere.

 

> [!Note]  
> A consulta dessa propriedade normalmente não retorna um erro. No entanto, se o mecanismo de fala demorar muito tempo para ser carregado, você poderá receber um erro indicando que a consulta atingiu o tempo limite.

 

## <a name="see-also"></a>Consulte Também

[**Propriedade LanguageID**](languageid-property.md)


 

 




