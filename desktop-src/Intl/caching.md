---
description: O Uniscribe salva mapeamentos de CMap (Unicode-to-glifo), larguras de glifo e tabelas de formatação de script OpenType.
ms.assetid: c06c0eaf-41cb-4fd1-9750-a78355217f12
title: Caching (internacionalização)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a01d8444fa222c2b6f6c7b03d0e1be70c1e04b1509ab020b8769d87b2b5cbc0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119500826"
---
# <a name="caching-internationalization"></a>Caching (internacionalização)

O Uniscribe salva mapeamentos de CMap (Unicode-to-glifo), larguras de glifo e tabelas de formatação de script OpenType. Um identificador para as tabelas de uma determinada fonte de um tamanho específico é chamado de "cache de script". Muitas funções de Uniscribe chamam um parâmetro de identificador de contexto de dispositivo e um ponteiro para uma estrutura de [**\_ cache de script**](script-cache.md) . Essas funções procuram primeiro informações por meio do cache de script, usando o contexto do dispositivo somente quando as tabelas necessárias ainda não estiverem armazenadas em cache. Ao chamar a função [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape), [**ScriptPlace**](/windows/desktop/api/Usp10/nf-usp10-scriptplace)ou [**ScriptTextOut**](/windows/desktop/api/Usp10/nf-usp10-scripttextout) , o aplicativo deve passar um ponteiro para uma estrutura **de \_ cache de script** . O identificador deve ser inicializado como **nulo** antes da primeira vez que o aplicativo o transmite para uma função de Uniscribe. O aplicativo nunca deve passar o mesmo identificador para diferentes fontes ou tamanhos diferentes.

Um aplicativo pode liberar um cache de script a qualquer momento. O Uniscribe mantém contagens de referência em seus caches de fonte e de forma livre, libera dados de fonte somente quando todos os tamanhos da fonte são liberados e libera dados de forma somente quando todas as fontes às quais a forma oferece suporte são liberadas. Quando o aplicativo é concluído com um estilo, ele deve chamar a função [**ScriptFreeCache**](/windows/desktop/api/Usp10/nf-usp10-scriptfreecache) para liberar o cache de script para o estilo.

Para [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) e [**ScriptPlace**](/windows/desktop/api/Usp10/nf-usp10-scriptplace), é válido para o aplicativo passar um contexto de dispositivo nulo. Geralmente, a chamada terá sucesso, pois as tabelas necessárias já estão armazenadas em cache. Se a formatação ou o posicionamento exigir acesso a um contexto de dispositivo, **ScriptShape** ou **ScriptPlace** retornará imediatamente com o \_ código de erro E pendente. Em seguida, o aplicativo deve selecionar a fonte no contexto do dispositivo. Para a maioria dos aplicativos, isso ajuda o desempenho, evitando a preparação repetida de um identificador de contexto de dispositivo com chamadas para [**SelectObject**](/windows/win32/api/wingdi/nf-wingdi-selectobject).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o Uniscribe](using-uniscribe.md)
</dt> </dl>

 

 
