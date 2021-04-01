---
description: A estrutura de dados PROPERTYINFO define uma propriedade do protocolo.
ms.assetid: 878777ab-141d-4cc5-b0c1-f2ac8f770bf0
title: Estrutura PROPERTYINFO (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PROPERTYINFO
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 435b08c5dd5e020dce2bde9be03a0d41299836c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921469"
---
# <a name="propertyinfo-structure"></a>Estrutura de PROPERTYINFO

A estrutura de dados **PROPERTYINFO** define uma propriedade do protocolo.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _PROPERTYINFO {
  HPROPERTY hProperty;
  DWORD     Version;
  LPSTR     Label;
  LPSTR     Comment;
  BYTE      DataType;
  BYTE      DataQualifier;
  union {
    LPVOID  lpExtendedInfo;
    LPRANGE lpRange;
    LPSET   lpSet;
    DWORD   Bitmask;
    DWORD   Value;
  };
  WORD      FormatStringSize;
  LPVOID    InstanceData;
} PROPERTYINFO, *LPPROPERTYINFO;
```



## <a name="members"></a>Membros

<dl> <dt>

**hProperty**
</dt> <dd>

Defina esse campo como zero. Na saída, Monitor de Rede retorna um identificador para a propriedade depois que a propriedade é adicionada ao banco de dados de propriedades.

</dd> <dt>

**Versão**
</dt> <dd>

Reservado. Deve ser definido como zero.

</dd> <dt>

**Rótulo**
</dt> <dd>

Nome da propriedade.

</dd> <dt>

**Comentário**
</dt> <dd>

Descrição da propriedade. A descrição é exibida na barra de Status Monitor de Rede.

</dd> <dt>

**DataType**
</dt> <dd>

Tipo de dados da propriedade. Esse membro pode ter um dos valores a seguir.



| Valor                                                                                                                                                                                                       | Significado                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PROP_TYPE_VOID"></span><span id="prop_type_void"></span><dl> <dt>**tipo de PROP \_ \_ void**</dt> </dl>                                           | O tipo de propriedade é desconhecido. Não há comprimento ou formato implícito.<br/>                                                                                                                                                                                                                                  |
| <span id="PROP_TYPE_SUMMARY"></span><span id="prop_type_summary"></span><dl> <dt>**\_Resumo do tipo prop \_**</dt> </dl>                                  | Resumindo o tipo de propriedade. Indica a primeira instância de propriedade que o analisador anexa a um quadro. O \_ \_ Resumo do tipo prop pode servir como um espaço reservado para grupos de propriedades. Esse valor indica que a propriedade não está definida na *RFC* do protocolo.<br/> |
| <span id="PROP_TYPE_BYTE"></span><span id="prop_type_byte"></span><dl> <dt>**\_byte do tipo prop \_**</dt> </dl>                                           | Dados numéricos com um tamanho de um byte (entidade de 8 bits).<br/>                                                                                                                                                                                                                                             |
| <span id="PROP_TYPE_WORD"></span><span id="prop_type_word"></span><dl> <dt>**tipo de PROP \_ \_ Word**</dt> </dl>                                           | Dados numéricos com um tamanho de dois bytes (entidade de 16 bits).<br/>                                                                                                                                                                                                                                           |
| <span id="PROP_TYPE_DWORD"></span><span id="prop_type_dword"></span><dl> <dt>**tipo de PROP \_ \_ DWORD**</dt> </dl>                                        | Dados numéricos com um tamanho de quatro bytes (entidade de 32 bits).<br/>                                                                                                                                                                                                                                          |
| <span id="PROP_TYPE_LARGEINT"></span><span id="prop_type_largeint"></span><dl> <dt>**tipo de PROP \_ \_ LARGEINT**</dt> </dl>                               | Dados numéricos com um tamanho de oito bytes (entidade de 64 bits).<br/>                                                                                                                                                                                                                                         |
| <span id="PROP_TYPE_ADDR"></span><span id="prop_type_addr"></span><dl> <dt>**\_endereço do tipo prop \_**</dt> </dl>                                           | Endereço MAC (entidade de 6 bytes).<br/>                                                                                                                                                                                                                                                                     |
| <span id="PROP_TYPE_TIME"></span><span id="prop_type_time"></span><dl> <dt>**\_hora do tipo de prop \_**</dt> </dl>                                           | Estrutura **SYSTEMTIME** .<br/>                                                                                                                                                                                                                                                                        |
| <span id="PROP_TYPE_STRING"></span><span id="prop_type_string"></span><dl> <dt>**Cadeia de caracteres do \_ tipo prop \_**</dt> </dl>                                     | Dados de texto ASCII. Este tipo de dados não é encerrado em nulo. <br/> Para dados Unicode, quando os dados de texto ASCII são especificados, o \_ sinalizador Unicode IFLAG também deve ser definido quando a função de instância da propriedade Attach é chamada.<br/>                                                                          |
| <span id="PROP_TYPE_IP_ADDRESS"></span><span id="prop_type_ip_address"></span><dl> <dt>**\_ \_ endereço IP do tipo prop \_**</dt> </dl>                        | Endereço IP. (entidade de 4 bytes).<br/>                                                                                                                                                                                                                                                                     |
| <span id="PROP_TYPE_IPX_ADDRESS"></span><span id="prop_type_ipx_address"></span><dl> <dt>**\_ \_ Endereço IPX do tipo prop \_**</dt> </dl>                     | Endereço IPX. (entidade de 10 bytes).<br/>                                                                                                                                                                                                                                                                   |
| <span id="PROP_TYPE_BYTESWAPPED_WORD"></span><span id="prop_type_byteswapped_word"></span><dl> <dt>**PROPs \_ Type \_ BYTESWAPPED \_ Word**</dt> </dl>      | Obsoleto. Para dados do WORD trocados por byte, defina **DataType** como prop \_ Type \_ Word e defina o \_ sinalizador permutated IFLAG ao chamar uma função de instância de propriedade **Attach** .<br/>                                                                                                                                |
| <span id="PROP_TYPE_BYTESWAPPED_DWORD"></span><span id="prop_type_byteswapped_dword"></span><dl> <dt>**tipo de PROP \_ \_ BYTESWAPPED \_ DWORD**</dt> </dl>   | Obsoleto. Para dados DWORD trocados por byte, defina **DataType** como prop \_ Type \_ DWORD e defina o \_ sinalizador permutated IFLAG ao chamar uma função de instância da propriedade **Attach** .<br/>                                                                                                                              |
| <span id="PROP_TYPE_TYPED_STRING"></span><span id="prop_type_typed_string"></span><dl> <dt>**\_cadeia de \_ caracteres tipada do tipo prop \_**</dt> </dl>                  | Obsoleto. Para dados de cadeia de caracteres de tipo variável, defina **DataType** como prop \_ Type \_ String e defina o \_ sinalizador Unicode IFLAG ao chamar uma função de instância de propriedade **Attach** .<br/>                                                                                                                           |
| <span id="PROP_TYPE_RAW_DATA"></span><span id="prop_type_raw_data"></span><dl> <dt>**\_ \_ dados brutos do tipo prop \_**</dt> </dl>                              | Dados brutos de comprimento e formato desconhecidos.<br/>                                                                                                                                                                                                                                                           |
| <span id="PROP_TYPE_COMMENT"></span><span id="prop_type_comment"></span><dl> <dt>**\_Comentário do tipo prop \_**</dt> </dl>                                  | O mesmo que o tipo de PROP \_ \_ void.<br/>                                                                                                                                                                                                                                                                        |
| <span id="PROP_TYPE_SRCFRIENDLYNAME"></span><span id="prop_type_srcfriendlyname"></span><dl> <dt>**tipo de PROP \_ \_ SRCFRIENDLYNAME**</dt> </dl>          | Endereço do nome amigável da fonte. Monitor de Rede não fornece suporte de formatação interno para esse tipo de dados.<br/>                                                                                                                                                                                |
| <span id="PROP_TYPE_DSTFRIENDLYNAME"></span><span id="prop_type_dstfriendlyname"></span><dl> <dt>**tipo de PROP \_ \_ DSTFRIENDLYNAME**</dt> </dl>          | Endereço do nome amigável de destino. Monitor de Rede não fornece suporte de formatação interno para esse tipo de dados.<br/>                                                                                                                                                                           |
| <span id="PROP_TYPE_TOKENRING_ADDRESS"></span><span id="prop_type_tokenring_address"></span><dl> <dt>**\_ \_ endereço TOKENRING do tipo prop \_**</dt> </dl>   | Endereço de token ring. Monitor de Rede não fornece suporte de formatação interno para esse tipo de dados.<br/>                                                                                                                                                                                             |
| <span id="PROP_TYPE_FDDI_ADDRESS"></span><span id="prop_type_fddi_address"></span><dl> <dt>**\_ \_ endereço FDDI do tipo prop \_**</dt> </dl>                  | Endereço FDDI. Monitor de Rede não fornece suporte de formatação interno para esse tipo de dados.<br/>                                                                                                                                                                                                   |
| <span id="PROP_TYPE_ETHERNET_ADDRESS"></span><span id="prop_type_ethernet_address"></span><dl> <dt>**\_ \_ endereço Ethernet do tipo prop \_**</dt> </dl>      | Endereço Ethernet. Monitor de Rede não fornece suporte de formatação interno para esse tipo de dados.<br/>                                                                                                                                                                                               |
| <span id="PROP_TYPE_OBJECT_IDENTIFIER"></span><span id="prop_type_object_identifier"></span><dl> <dt>**\_identificador de \_ objeto do tipo prop \_**</dt> </dl>   | Identificador de objeto SNMP codificado em BER.<br/>                                                                                                                                                                                                                                                              |
| <span id="PROP_TYPE_VINES_IP_ADDRESS"></span><span id="prop_type_vines_ip_address"></span><dl> <dt>**\_ \_ endereço IP de Vines do tipo prop \_ \_**</dt> </dl>     | Endereço IP de Vines (entidade de 6 bytes).<br/>                                                                                                                                                                                                                                                                |
| <span id="PROP_TYPE_VAR_LEN_SMALL_INT"></span><span id="prop_type_var_len_small_int"></span><dl> <dt>**tipo de PROP \_ \_ var \_ Len \_ pequeno \_ int**</dt> </dl> | Valor numérico sem um comprimento predeterminado, mas não mais do que 8 bytes de comprimento. O comprimento dos dados anexados determina o comprimento do valor.<br/>                                                                                                                                                |



 

</dd> <dt>

**Dataqualificador**
</dt> <dd>

O qualificador de dados de uma propriedade. Esse membro fornece informações precisas sobre o tipo de dados.

O **Dataqualificador** pode ter um dos valores a seguir.



| Valor                                                                                                                                                                                                  | Significado                                                                                                                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PROP_QUAL_NONE"></span><span id="prop_qual_none"></span><dl> <dt>**PROP \_ igual \_ None**</dt> </dl>                                      | O tipo de dados Property é a única especificação da propriedade. <br/> Quando esse valor é definido, o membro Union da estrutura é definido como **NULL** e, em seguida, ignorado.<br/>                                                                                                                                        |
| <span id="PROP_QUAL_RANGE"></span><span id="prop_qual_range"></span><dl> <dt>**\_intervalo de igual prop \_**</dt> </dl>                                   | Espera-se que o valor numérico esteja dentro de um determinado intervalo. Defina o intervalo no membro **lpRange** .<br/>                                                                                                                                                                                                                |
| <span id="PROP_QUAL_SET"></span><span id="prop_qual_set"></span><dl> <dt>**\_conjunto de igual prop \_**</dt> </dl>                                         | O valor de uma propriedade é comparado a um conjunto de valores que são especificados no membro **lpSet** da União da estrutura. O valor de uma propriedade pode ser um **byte**, **Word**, **DWORD**, **LARGEINT** ou **time**.<br/>                                                                                                |
| <span id="PROP_QUAL_BITFIELD"></span><span id="prop_qual_bitfield"></span><dl> <dt>**campo de igual de PROP \_ \_**</dt> </dl>                          | Obsoleto.<br/>                                                                                                                                                                                                                                                                                                            |
| <span id="PROP_QUAL_LABELED_SET"></span><span id="prop_qual_labeled_set"></span><dl> <dt>**PROP \_ igual \_ rotulado \_ conjunto**</dt> </dl>                | O valor de uma propriedade é comparado a um valor em um conjunto de pares de rótulo de valor. Os pares de rótulo de valor são especificados no membro **lpSet** da União da estrutura. <br/> No momento da exibição, se o valor da propriedade corresponder a um valor no conjunto, então o valor e o rótulo associado serão exibidos.<br/> |
| <span id="PROP_QUAL_LABELED_BITFIELD"></span><span id="prop_qual_labeled_bitfield"></span><dl> <dt>**PROP \_ igual \_ rotulado como campo de bits \_**</dt> </dl> | Obsoleto. \_ \_ Em vez disso, use os sinalizadores prop igual.<br/>                                                                                                                                                                                                                                                                             |
| <span id="PROP_QUAL_CONST"></span><span id="prop_qual_const"></span><dl> <dt>**\_igual \_ const de prop**</dt> </dl>                                   | O valor de uma propriedade é comparado a uma constante que é especificada no membro de **valor** da União. <br/> No momento da exibição, se os valores de propriedade e a constante não corresponderem, uma mensagem de erro formatada será exibida com o valor definido como normal.<br/>                                                             |
| <span id="PROP_QUAL_FLAGS"></span><span id="prop_qual_flags"></span><dl> <dt>**\_sinalizadores de igual de prop \_**</dt> </dl>                                   | O valor da propriedade é comparado a BITs específicos identificados no membro **lpSet** da União.<br/>                                                                                                                                                                                                              |
| <span id="PROP_QUAL_ARRAY"></span><span id="prop_qual_array"></span><dl> <dt>**\_matriz igual \_ prop**</dt> </dl>                                   | O valor de uma propriedade especifica uma matriz de valores. O comprimento dos dados anexados determina o comprimento de uma matriz. <br/> Quando o \_ valor da matriz prop igual \_ é definido, o membro Union da estrutura de dados **PROPERTYINFO** é definido como **NULL** e ignorado.<br/>                                                    |



 

</dd> <dt>

**lpExtendedInfo**
</dt> <dd>

Reservado (membro de União).

</dd> <dt>

**lpRange**
</dt> <dd>

Ponteiro para uma estrutura de [intervalo](range.md) que define um intervalo de valores. Esse membro deve ser definido se o membro **Dataqualificador** dessa estrutura estiver definido como prop \_ igual \_ Range (membro of Union).

</dd> <dt>

**lpSet**
</dt> <dd>

Ponteiro para uma estrutura de [conjunto](set.md) que especifica um conjunto de valores ou rótulos. Esse membro deve ser definido se o membro **Dataqualificador** da estrutura estiver definido como prop \_ igual \_ set, prop \_ igual \_ labeld \_ set ou os \_ sinalizadores igual prop \_ (member of Union).

</dd> <dt>

**Bitmask**
</dt> <dd>

Obsoleto (membro de União).

</dd> <dt>

**Valor**
</dt> <dd>

Valor constante usado quando **Dataqualificador** é definido como prop \_ igual \_ const (membro de Union).

</dd> <dt>

**FormatStringSize**
</dt> <dd>

Tamanho máximo usado somente para a descrição da propriedade.

</dd> <dt>

**InstanceData**
</dt> <dd>

Especifique a função de formato que é chamada para formatar os dados exibidos para a propriedade. Para usar o formatador genérico, especifique a função **FormatPropertyInstance** .

</dd> </dl>

## <a name="remarks"></a>Comentários

A estrutura **PROPERTYINFO** é usada em chamadas para a função [AddProperty](/previous-versions/bb251873(v=msdn.10)) . A função **AddProperty** adiciona uma única definição de propriedade ao banco de [*dados de propriedades*](p.md)do analisador.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[AddProperty](/previous-versions/bb251873(v=msdn.10))
</dt> <dt>

[AMPLITUDE](range.md)
</dt> <dt>

[SET](set.md)
</dt> </dl>

 

