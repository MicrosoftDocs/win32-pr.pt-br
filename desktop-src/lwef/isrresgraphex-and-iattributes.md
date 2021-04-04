---
title: ISRResGraphEx e IAttributes
description: ISRResGraphEx e IAttributes
ms.assetid: 6eb37da1-5252-4c41-891c-c19cca6fb7d1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 659d7d4723bfc5145fb8abcc77043031a0e48e8b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104007376"
---
# <a name="isrresgraphex-and-iattributes"></a>ISRResGraphEx e IAttributes

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

Os objetos de resultados retornados pelo mecanismo devem dar suporte à interface ISRResGraphEx e à interface IAttributes. Simplesmente dar suporte à interface ISRResGraphEx é suficiente para habilitar o editor de som a fornecer informações de quebra de palavras, mas não fornece o suporte necessário para informações de fonema.

O editor de som requer que os mecanismos também ofereçam suporte a um atributo DWord especial, **SRATTR \_ PHONESEG**. O editor consulta os mecanismos para ver a interface IAttributes e tenta definir o **SRATTR \_ PHONESEG** como 1. Se essa chamada for realizada com sucesso, o editor de som assumirá que os resultados do mecanismo oferecerão suporte à coleta de informações de segmentação de fonema do objeto de resultados.

`#define    SRATTR_PHONESEG    MAKELONG (1, SRVEN_MICROSOFT)`

Quando um objeto de resultados é transmitido para o editor de som, ele consulta esse objeto para sua implementação de ISRResGraphEx. ISRResGraphEx contém uma função de membro, DataGet, com assinatura de tipo

`HRESULT  DataGet  (DWord, dwID, GUID gAttrib, SDATA *psData)`

Em que **dwID** é o identificador do objeto de grafo, **GATTRIB** é um GUID correspondente ao atributo procurado e **psData** é um ponteiro para um objeto SDATA que contém os dados retornados. O mecanismo é responsável por alocar os dados armazenados em **psData** por meio de [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc). O aplicativo de chamada (neste caso, o editor de som) é responsável por liberá-lo por meio de [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) quando ele é concluído.

DataGet é necessário para reconhecer três GUIDs predefinidos, listados na documentação do SAPI. Um mecanismo que retorna um código de êxito para a chamada para **dwordset (SRATTR \_ PHONESEG, 1)** também é necessário para reconhecer um GUID específico, **SRGARC \_ PHONEMESEGMENTATION**, quando chamado com um **dwID** que corresponde a uma borda no grafo.

`DEFINE_GUID(SRGARC_PHONMESEGMENTATION, 0xd05405b0, 0x1db1, 0x11d2, 0x94, 0x2, 0x0, 0xc0, 0x4f, 0x8e, 0xf4, 0x8f);`

Quando a chamada retorna, **psData** deve apontar para uma matriz de estrutura alinhada em DWORD do tipo **PHONESEG**, definida por:

``` syntax
typedef struct tagSRPHONESEG {
   DWORD   dwSize;       // Size of the SRPHONESEG structure + phone data
   QWORD   qwStartTime;  // SAPI timestamp of the start of the seqment
   …QWORD   qwEndTime;    // SAPI timestamp of the end of the seqment
   int      nScore;      // The segment's score
   WCHAR   aPhones[0];   // Array of phone(s) making up the segment
} SRPHONESEG,  *PSRPHONESEG;
```

onde **qwStartTime** e **qwEndTime** apontam para o início e o fim de cada fonema que compõem a palavra coberta pela borda, e **aPhones** é uma matriz de caracteres Unicode correspondente à representação IPA do telefone, que foi produzido nesse segmento. (Em alguns idiomas, há fonemas que são escritos com mais de um fonema IPA. Em inglês, por exemplo, o som "Long I" na palavra "Live" é, na verdade, um diphthong, composto de dois fonemas mais simples concatenados juntos.) A matriz **aPhones** deve ser terminada em zero e preenchida no final para fazer com que cada estrutura **SRPHONESEG** na matriz tenha um múltiplo par de quatro bytes de comprimento.

Por exemplo, suponha que a palavra falada no arco 4 fosse "feita". Em seguida, a chamada para DataGet (4, **SRGARC \_ PHONEMESEGMENTATION**, &SD) pode retornar uma matriz de três segmentos de fonema,/m/em execução de **qwStartTime**= 328434 bytes a **qwEndTime**= 330354 bytes,/1e/em execução de **qwStartTime**= 330354 bytes para **qwEndTime**= 344114 bytes e/d/em execução de **qwStartTime**= 344114 bytes para **qwEndTime**= 347314 bytes. Eles seriam apresentados como uma matriz empacotada de três estruturas **SRPHONESEG** de tamanhos 28, 32 e 28 bytes, respectivamente. Observe que há algum preenchimento no final da estrutura do meio **SRPHONESEG** , para que o próximo item na matriz comece com um limite de 4 bytes.

O SDK do SAPI 4,0 inclui uma ferramenta (SRFunc) para testar a conformidade com a especificação SAPI 4,0. Incluídos nessa ferramenta há um teste de conformidade com esse conjunto de interfaces. O código-fonte para essa ferramenta é um bom ponto de partida para entender como essas interfaces irão interagir com o editor de som e depurar as interfaces durante o desenvolvimento.

 

 