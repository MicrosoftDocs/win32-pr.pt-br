---
title: ISRResGraphEx e IAttributes
description: ISRResGraphEx e IAttributes
ms.assetid: 6eb37da1-5252-4c41-891c-c19cca6fb7d1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81f5e08b77b917e4630afcaeb8baed5aac4e13c20a1ed289418681abbbdca20b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118748992"
---
# <a name="isrresgraphex-and-iattributes"></a>ISRResGraphEx e IAttributes

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

Os objetos de resultados retornados pelo mecanismo devem dar suporte à interface ISRResGraphEx e à interface IAttributes. Simplesmente dar suporte à interface ISRResGraphEx é suficiente para permitir que o editor de som forneça informações de quebra de palavras, mas não fornece o suporte necessário para informações de phoneme.

O editor de som requer que os mecanismos também deem suporte a um atributo DWord especial, **SRATTR \_ PHONESEG.** O editor consulta os mecanismos para ver a interface IAttributes e tenta definir **o SRATTR \_ PHONESEG** como 1. Se essa chamada for bem-sucedida, o editor de som pressupõe que os resultados do mecanismo darão suporte à coleta de informações de segmentação de phoneme do objeto de resultados.

`#define    SRATTR_PHONESEG    MAKELONG (1, SRVEN_MICROSOFT)`

Quando um objeto de resultados é transmitido para o editor de som, ele consulta esse objeto para sua implementação de ISRResGraphEx. ISRResGraphEx contém uma função membro, DataGet, com assinatura de tipo

`HRESULT  DataGet  (DWord, dwID, GUID gAttrib, SDATA *psData)`

Em **que dwID** é o identificador do objeto de grafo, **gAttrib** é um GUID correspondente ao atributo procurado e **psData** é um ponteiro para um objeto SDATA que contém os dados retornados. O mecanismo é responsável por alocar os dados armazenados em **psData** por meio [**de CoTaskMemAlloc.**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) O aplicativo de chamada (nesse caso, o editor de som) é responsável por libera-lo por meio de [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) quando ele é concluído.

DataGet é necessário para reconhecer três GUIDs predefinidos, que estão listados na documentação do SAPI. Um mecanismo que retorna um código de êxito para a chamada para **DWORDSet(SRATTR \_ PHONESEG, 1)** também é necessário para reconhecer um GUID específico, **SRGARC \_ PHONEMESEGMENTATION,** quando chamado com **um dwID** que corresponde a uma borda no grafo.

`DEFINE_GUID(SRGARC_PHONMESEGMENTATION, 0xd05405b0, 0x1db1, 0x11d2, 0x94, 0x2, 0x0, 0xc0, 0x4f, 0x8e, 0xf4, 0x8f);`

Quando a chamada retorna, **psData** deve apontar para uma matriz de estrutura alinhada a DWORD do tipo **PHONESEG**, definida por:

``` syntax
typedef struct tagSRPHONESEG {
   DWORD   dwSize;       // Size of the SRPHONESEG structure + phone data
   QWORD   qwStartTime;  // SAPI timestamp of the start of the seqment
   …QWORD   qwEndTime;    // SAPI timestamp of the end of the seqment
   int      nScore;      // The segment's score
   WCHAR   aPhones[0];   // Array of phone(s) making up the segment
} SRPHONESEG,  *PSRPHONESEG;
```

em **que qwStartTime** e **qwEndTime** apontam para o início e o fim de cada phoneme que compensou a palavra coberta pela borda, e **aPhones** é uma matriz de caracteres Unicode correspondentes à representação IPA do telefone, que foram produzidos neste segmento. (Em alguns idiomas, há fonemas que são escritos com mais de um phoneme IPA. Em inglês, por exemplo, o som "I longo" na palavra "ao vivo" é, na verdade, um diphthong, com dois fonemas mais simples concatenados juntos.) A **matriz aPhones** deve ser terminada em zero e preenchimento no final para tornar cada **estrutura SRPHONESEG** na matriz um múltiplo de até mesmo vários de quatro bytes.

Por exemplo, suponha que a palavra falada no arco 4 foi "made". Em seguida, a chamada para DataGet(4, **SRGARC \_ PHONEMESEGMENTATION**, &sd) pode retornar uma matriz de três segmentos de phoneme, /m/ running from **qwStartTime**=328434 bytes to **qwEndTime**=330354 bytes, /1e/ running from **qwStartTime**=330354 bytes to **qwEndTime**=344114 bytes e /d/ running from **qwStartTime**=344114 bytes to **qwEndTime**=347314 bytes. Eles seriam apresentados como uma matriz empacotada de três **estruturas SRPHONESEG** de tamanhos de 28, 32 e 28 bytes, respectivamente. Observe que há algum preenchimento no final da estrutura **SRPHONESEG** intermediária, para que o próximo item na matriz comece em um limite de 4 byte.

O SDK do SAPI 4.0 inclui uma ferramenta (SRFunc) para testar a conformidade com a especificação sapi 4.0. Incluído nessa ferramenta é um teste de conformidade com esse conjunto de interfaces. O código-fonte dessa ferramenta é um bom lugar para começar a entender como essas interfaces interagirão com o editor de som e depurar as interfaces durante o desenvolvimento.

 

 