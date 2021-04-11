---
description: Especifica se o carregador de topologia enumera os tipos de mídia fornecidos pela origem da mídia.
ms.assetid: 2675ef16-2018-47e8-bb22-2fc0d62e6681
title: Atributo MF_TOPOLOGY_ENUMERATE_SOURCE_TYPES (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 015042bbf9994f81058c621239224196e6ec9ac8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296311"
---
# <a name="mf_topology_enumerate_source_types-attribute"></a>\_Atributo de \_ tipos de origem de enumeração de topologia MF \_ \_

Especifica se o carregador de topologia enumera os tipos de mídia fornecidos pela origem da mídia.

## <a name="data-type"></a>Tipo de dados

**UINT32**

Use um dos valores a seguir.



| Valor                                                                                                                                    | Significado                                             |
|------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="FALSE"></span><span id="false"></span><dl> <dt>FALSE * * * *</dt> </dl> | Não enumere os tipos de mídia de origem.<br/> |
| <span id="TRUE"></span><span id="true"></span><dl> <dt>VERDADEIRO * * * *</dt> </dl>    | Enumere os tipos de mídia de origem.<br/>        |



 

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para definir esse atributo, chame [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Aplica-se a

[**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a>Comentários

Cada fluxo em uma fonte de mídia pode oferecer mais de um tipo de mídia. A lista de tipos é enumerada por meio da interface [**IMFMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) no descritor de fluxo.

A ordem na qual o carregador de topologia tenta os tipos de mídia de uma fonte de mídia é controlada por dois atributos:

-   O \_ atributo da topologia MF \_ enumerar \_ \_ tipos de origem na topologia.
-   O atributo do [**\_ \_ \_ método MF TOPONODE Connect**](mf-toponode-connect-method-attribute.md) no nó de origem.

Se o \_ atributo de \_ tipos de origem enumerar topologia MF \_ \_ for **false** ou não estiver definido, o carregador de topologia usará o tipo de mídia atual do fluxo. Ele não enumera a lista de tipos possíveis. Se o tipo de mídia atual for incompatível com o nó de topologia downstream e nenhuma combinação de decodificadores/conversores puder ser encontrada, a resolução da topologia falhará.

Se o \_ atributo de \_ tipos de origem enumerar topologia MF \_ \_ for **true**, o carregador de topologia enumerará os tipos de mídia da fonte até encontrar um tipo compatível. Nesse caso, a ordem exata das operações dependerá se o atributo do [**\_ \_ \_ método MF TOPONODE Connect**](mf-toponode-connect-method-attribute.md) no nó de origem inclui o sinalizador **do \_ MF \_ Connect \_ resolver \_ OUTPUTTYPES independente** .

Se \_ a topologia MF \_ enumerar \_ tipos de origem \_ for **true** e o sinalizador **\_ \_ \_ \_ OUTPUTTYPES de resolução independente do MF Connect** for definido, o carregador de topologia esgotará cada tipo de mídia antes de passar para a próxima, da seguinte maneira:

``` syntax
foreach media type T
    connect directly using T
    if failed, connect with converters using T
    if failed, connect with decoders using T
```

Se \_ a topologia MF \_ enumerar \_ tipos de origem \_ for **true** , mas o **MF \_ Connect \_ resolver \_ \_ OUTPUTTYPES independente** não estiver definido, o carregador de topologia tentará uma conexão direta com cada tipo de mídia e tentará cada tipo de mídia com conversores e, por fim, tentará cada tipo de mídia com decodificadores:

``` syntax
foreach media type T
    connect directly using T
if failed,
    foreach media type T
        connect with converters using T
if failed
    foreach media type T
        connect with decoders using T
```

Se \_ a topologia MF \_ enumerar \_ tipos de origem \_ for **false**, o sinalizador **\_ \_ \_ \_ OUTPUTTYPES de resolução de conexão do MF Connect** será ignorado.

O valor padrão da \_ topologia MF \_ enumerar \_ tipos de origem \_ é **false**, para compatibilidade com aplicativos existentes.

A constante de GUID para esse atributo é exportada de mfuuid. lib.

### <a name="example"></a>Exemplo

Aqui está um exemplo que ilustra o **sinalizador \_ \_ \_ \_ OUTPUTTYPES de resolução independente do MF Connect** . Suponha que a topologia tenha o \_ \_ atributo de tipos de origem enumerar topologia MF \_ \_ definido como **true**.

A origem de mídia oferece os seguintes tipos:

-   T1, T2, T3

O coletor de mídia aceita os seguintes tipos:

-   T3, T4

Caso 1: o sinalizador de **OUTPUTTYPES do MF \_ Connect de \_ resolução \_ independente \_** está definido.

1.  O carregador de topologia tenta uma conexão direta com T1. O coletor rejeita T1.
2.  O carregador de topologia insere um decodificador que aceita T1 e gera T4. O coletor aceita T4.
3.  A topologia final contém: Media Source → Decoder → Media Sink.

Caso 2: o sinalizador não está definido.

1.  O carregador de topologia tenta uma conexão direta com T1. O coletor rejeita T1.
2.  O carregador de topologia tenta uma conexão direta com T2. O coletor rejeita T2.
3.  O carregador de topologia tenta uma conexão direta com T3. O coletor aceita T3.
4.  A topologia final contém: Media Source → Media Sink.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                         |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]<br/>                            |
| parâmetro<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de topologia](topology-attributes.md)
</dt> </dl>

 

 




