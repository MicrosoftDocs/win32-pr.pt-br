---
description: A estrutura CAPTUREFILTER contém dados de filtro de captura.
ms.assetid: 773187c6-31c7-4439-850d-1dd43d42f701
title: Estrutura CAPTUREFILTER (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPTUREFILTER
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: de5ab95ab395d50afb41223a458342706da1df7434d524f21c230436b3b9c7b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117796346"
---
# <a name="capturefilter-structure"></a>Estrutura CAPTUREFILTER

A estrutura **CAPTUREFILTER** contém dados de filtro de captura.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _CAPTUREFILTER {
  DWORD          FilterFlags;
  LPBYTE         lpSapTable;
  LPWORD         lpEtypeTable;
  WORD           nSaps;
  WORD           nEtypes;
  LPADDRESSTABLE AddressTable;
  EXPRESSION     FilterExpression;
  TRIGGER        Trigger;
  DWORD          nFrameBytesToCopy;
  RESERVED       Reserved;
} CAPTUREFILTER, *LPCAPTUREFILTER;
```



## <a name="members"></a>Membros

<dl> <dt>

**FilterFlags**
</dt> <dd>

Sinalizadores que descrevem o conteúdo do filtro de captura.



| Valor                                                                                                                                                                                                                                                                                                   | Significado                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="CAPTUREFILTER_FLAGS_INCLUDE_ALL_SAPS"></span><span id="capturefilter_flags_include_all_saps"></span><dl> <dt>**CAPTUREFILTER \_ \_Os sinalizadores incluem \_ todos os \_ SAPs**</dt> <dt>0x0001</dt> </dl>       | Inclui todos os SAPs como quadros aceitáveis.<br/>  |
| <span id="CAPTUREFILTER_FLAGS_INCLUDE_ALL_ETYPES"></span><span id="capturefilter_flags_include_all_etypes"></span><dl> <dt>**CAPTUREFILTER \_ \_Os sinalizadores incluem \_ todos os \_ ETYPES**</dt> <dt>0x0002</dt> </dl> | Incluir todos os ETYPEs como quadros aceitáveis.<br/> |
| <span id="CAPTUREFILTER_FLAGS_LOCAL_ONLY"></span><span id="capturefilter_flags_local_only"></span><dl> <dt>**CAPTUREFILTER \_ 0x0008 \_ \_ somente locais de sinalizadores**</dt> <dt></dt> </dl>                          | Sem modo P<br/>                                |
| <span id="CAPTUREFILTER_FLAGS_KEEP_RAW"></span><span id="capturefilter_flags_keep_raw"></span><dl> <dt>**CAPTUREFILTER \_ Os \_ sinalizadores \_ mantêm**</dt> o <dt>0x0020</dt> bruto </dl>                                | Mantenha os quadros MAC SMT e token ring.<br/>      |



 

</dd> <dt>

**lpSapTable**
</dt> <dd>

Ponteiro para uma matriz de valores SAP. Esse membro indica os valores SAP que são válidos para passar para o driver. Se CAPTUREFILTER \_ flags \_ incluir \_ todos os \_ SAPs for definido, isso se tornará uma lista de exceção (inclua todos os SAPs, exceto esses).

</dd> <dt>

**lpEtypeTable**
</dt> <dd>

Ponteiro para uma matriz de valores de ETYPE. Isso indica os valores de ETYPE que são válidos para passar para o driver. Se \_ os sinalizadores CAPTUREFILTERs \_ incluírem \_ todos os \_ ETYPEs forem definidos, isso se tornará uma lista de exceção (inclua todos os ETYPEs, exceto estes).

</dd> <dt>

**nSaps**
</dt> <dd>

Número de SAPs na tabela SAP.

</dd> <dt>

**nEtypes**
</dt> <dd>

Número de ETYPEs na tabela ETYPE.

</dd> <dt>

**Endereço de endereçamento**
</dt> <dd>

Nome da tabela de endereços.

</dd> <dt>

**FilterExpression**
</dt> <dd>

Uma estrutura de expressão. Contém a parte de correspondência de padrões do filtro de captura.

</dd> <dt>

**Gatilho**
</dt> <dd>

Reservado.

</dd> <dt>

**nFrameBytesToCopy**
</dt> <dd>

Se esse membro não for 0, ele especificará quantos bytes serão mantidos de cada quadro recebido. Se for 0, mantenha todo o quadro.

</dd> <dt>

**Reserved**
</dt> <dd>

Reservado.

</dd> </dl>

## <a name="remarks"></a>Comentários

A combinação de sinalizadores, valores e expressões determina quais quadros serão passados pelo driver que usa esses dados de estrutura. Para obter mais informações sobre como implementar uma estrutura **CAPTUREFILTER** , consulte [filtros de captura](capture-filters.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Endereço de endereçamento](addresstable.md)
</dt> <dt>

[ADDRESSPAIR](addresspair.md)
</dt> <dt>

[EXPRESSÃO](expression.md)
</dt> <dt>

[ANDEXP](andexp.md)
</dt> <dt>

[PATTERNMATCH](patternmatch.md)
</dt> </dl>

 

 




