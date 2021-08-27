---
description: A estrutura definida define um conjunto de valores.
ms.assetid: 88e0ffa1-71a2-4a3f-bdf1-964de0adea62
title: DEFINIR estrutura (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SET
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: d66ba5dd3a977967d0020a00d5813c3f689142b1e58c631c99f9bd10fceba3ec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120074396"
---
# <a name="set-structure"></a>DEFINIR estrutura

A estrutura **definida** define um conjunto de valores.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _SET {
  DWORD nEntries;
  union {
    LPBYTE               lpByteTable;
    LPWORD               lpWordTable;
    LPDWORD              lpDwordTable;
    LPLARGEINT           lpLargeIntTable;
    LPSYSTEMTIME         lpSystemTimeTable;
    LPLABELED_BYTE       lpLabeledByteTable;
    LPLABELED_WORD       lpLabeledWordTable;
    LPLABELED_DWORD      lpLabeledDwordTable;
    LPLABELED_LARGEINT   lpLabeledLargeIntTable;
    LPLABELED_SYSTEMTIME lpLabeledSystemTimeTable;
    LPLABELED_BIT        lpLabeledBit;
    LPVOID               lpVoidTable;
  };
} SET, *LPSET;
```



## <a name="members"></a>Membros

<dl> <dt>

**nEntries**
</dt> <dd>

Número total de entradas em um conjunto.

</dd> <dt>

**lpByteTable**
</dt> <dd>

Ponteiro para uma matriz de valores de BYTE.

</dd> <dt>

**lpWordTable**
</dt> <dd>

Ponteiro para uma matriz de valores de palavra.

</dd> <dt>

**lpDwordTable**
</dt> <dd>

Ponteiro para uma matriz de valores DWORD.

</dd> <dt>

**lpLargeIntTable**
</dt> <dd>

Ponteiro para uma matriz de estruturas [LARGEINT](largeint.md) .

</dd> <dt>

**lpSystemTimeTable**
</dt> <dd>

Ponteiro para uma matriz de valores de SYSTEMTIME.

</dd> <dt>

**lpLabeledByteTable**
</dt> <dd>

Ponteiro para uma matriz de estruturas de [ \_ byte rotuladas](labeled-byte.md) . Cada estrutura de **\_ bytes rotulada** define um valor e um rótulo. Monitor de Rede exibirá um rótulo se encontrar um valor correspondente no pacote de protocolo.

</dd> <dt>

**lpLabeledWordTable**
</dt> <dd>

Ponteiro para uma matriz de estruturas de [ \_ palavras rotuladas](labeled-word.md) que definem um conjunto de valores e rótulos de palavra.

</dd> <dt>

**lpLabeledDwordTable**
</dt> <dd>

Ponteiro para uma matriz de estruturas [ \_ DWORD rotuladas](labeled-dword.md) que definem um conjunto de valores e rótulos DWORD.

</dd> <dt>

**lpLabeledLargeIntTable**
</dt> <dd>

Ponteiro para uma matriz de estruturas [ \_ LARGEINT rotuladas](labeled-largeint.md) que definem um conjunto de valores e rótulos LARGEINT.

</dd> <dt>

**lpLabeledSystemTimeTable**
</dt> <dd>

Ponteiro para uma matriz de estruturas [ \_ SYSTEMTIME rotuladas](labeled-systemtime.md) que definem um conjunto de valores e rótulos do sistema.

</dd> <dt>

**lpLabeledBit**
</dt> <dd>

Ponteiro para uma matriz de estruturas de [ \_ bits rotuladas](labeled-bit.md) que definem um conjunto de pares de bits rotulados. Cada BIT pode especificar dois rótulos um rótulo para cada Estado (0 ou 1) do BIT.

</dd> <dt>

**lpVoidTable**
</dt> <dd>

Ponteiro para uma matriz de valores.

</dd> </dl>

## <a name="remarks"></a>Comentários

A estrutura **definida** é usada para definir um conjunto de dados de comparação que monitor de rede pode usar para interpretar o valor de uma propriedade em um pacote de protocolo. Quando um conjunto de dados de comparação é necessário, um ponteiro para a estrutura do **conjunto** é especificado no membro **LpSet** da estrutura [PROPERTYINFO](propertyinfo.md) .

A DLL do analisador pode fornecer um conjunto de valores e um conjunto de rótulos. O membro da **União** que você seleciona em uma estrutura de **conjunto** aponta para uma matriz de estruturas que define cada membro de um conjunto.

-   Conjunto de valores

    Um conjunto de valores é usado quando você deseja que Monitor de Rede inclua um indicador em conjunto ou não em conjunto com o valor encontrado no pacote de protocolo. Por exemplo, se um conjunto DWORD for especificado, Monitor de Rede exibirá um rótulo para cada valor DWORD encontrado no pacote de protocolo, indicando que o DWORD está ou não está especificado no conjunto.

    Um conjunto de valores pode ser baseado em tipos de dados BYTE, WORD, DWORD, LARGEINT e SYSTEMTIME.

-   Conjunto de rótulos

    Um conjunto de rótulos é usado quando você deseja que Monitor de Rede exiba um rótulo definido pelo usuário em vez dos valores de propriedade especificados em um conjunto.

    Um conjunto de rótulos pode ser baseado em pares BYTE, WORD, DWORD, LARGEINT, SYSTEMTIME e de rótulo de bits.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[BIT ROTULAdo \_](labeled-bit.md)
</dt> <dt>

[PROPERTYINFO](propertyinfo.md)
</dt> </dl>

 

 




