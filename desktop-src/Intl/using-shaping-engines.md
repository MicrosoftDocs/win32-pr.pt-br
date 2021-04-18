---
description: O Uniscribe usa vários mecanismos de shaping que contêm o conhecimento de layout para scripts específicos.
ms.assetid: 3cdd18f3-51d3-4d1c-be31-f5709074cbe7
title: Usando mecanismos de shaping
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a106e993aba515af38edd2b809ef60454a186cde
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105749600"
---
# <a name="using-shaping-engines"></a>Usando mecanismos de shaping

O Uniscribe usa vários mecanismos de shaping que contêm o conhecimento de layout para scripts específicos. Ele também aproveita o mecanismo de modelagem de layout OpenType para manipular recursos de script específicos de fontes, como geração de glifos, medição de extensão e suporte à quebra de palavras. O Uniscribe gerencia a reordenação de caracteres bidirecionais usando o algoritmo bidirecional Unicode e entende formatos de fonte de layout não-OpenType para formatação árabe, Hebraico e tailandês.

Como os intervalos de ponto de código exatos atribuídos a cada mecanismo de shaping podem variar, os números de script não são publicados, com exceção do SCRIPT \_ indefinido. No entanto, seu aplicativo pode testar os atributos de scripts chamando a função [**ScriptGetProperties**](/windows/desktop/api/Usp10/nf-usp10-scriptgetproperties) , que acessa a tabela global de propriedades de script. O aplicativo pode usar as propriedades de script global para ajudar a combinar suas próprias regras de layout com as divisões do mecanismo de shaping necessárias.

O aplicativo acessa um mecanismo de shaping com uma chamada para a função [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) . Todos os mecanismos de modelagem de script complexos, os mecanismos de modelagem de dígitos e os mecanismos de formatação ASCII validam a fonte indicada no identificador de contexto do dispositivo antes do Shaping. Scripts complexos devem ser moldados usando o script retornado pela função [**ScriptItemize**](/windows/desktop/api/Usp10/nf-usp10-scriptitemize) para que você possa ser legível. Outras execuções permanecerão legíveis se moldado com SCRIPT \_ especificado no membro **eScript** da estrutura [**de \_ análise de script**](/windows/win32/api/usp10/ns-usp10-script_analysis) , embora elas possam perder qualidade tipográfica.

[**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) retornará 0 se for bem-sucedido ou \_ \_ o script USP E não estará \_ \_ na \_ fonte se a fonte fornecida pelo aplicativo não contiver marcas de formatação ou glifos suficientes. Se o aplicativo especificar o SCRIPT \_ indefinido e alguns caracteres não forem suportados pela fonte, a função ainda terá sucesso. Nesse caso, o aplicativo deve verificar o buffer de saída de glifo para a presença de glifos ausentes. Para obter estratégias para lidar com glifos ausentes, consulte [usando o fallback de fonte](using-font-fallback.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o Uniscribe](using-uniscribe.md)
</dt> </dl>

 

 



