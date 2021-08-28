---
description: A estrutura de dados PROPERTYINFO define uma propriedade do protocolo.
ms.assetid: 878777ab-141d-4cc5-b0c1-f2ac8f770bf0
title: Estrutura PROPERTYINFO (Netmon.h)
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
ms.openlocfilehash: 8dc20b94fbf889b4c04712eadbee5d7d834d3cf260962fe01ef7837e5893c4a4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120128946"
---
# <a name="propertyinfo-structure"></a>Estrutura PROPERTYINFO

A **estrutura de dados PROPERTYINFO** define uma propriedade do protocolo.

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

De definir esse campo como zero. Na saída, Monitor de Rede retorna um handle para a propriedade depois que a propriedade é adicionada ao banco de dados de propriedades.

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

Descrição da propriedade. A descrição aparece na barra Monitor de Rede status.

</dd> <dt>

**DataType**
</dt> <dd>

Tipo de dados da propriedade. Esse membro pode ter um dos valores a seguir.



| Valor                                                                                                                                                                                                       | Significado                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PROP_TYPE_VOID"></span><span id="prop_type_void"></span><dl> <dt>**TIPO \_ DE PROP \_ VOID**</dt> </dl>                                           | O tipo de propriedade é desconhecido. Não há nenhum formato ou comprimento implícito.<br/>                                                                                                                                                                                                                                  |
| <span id="PROP_TYPE_SUMMARY"></span><span id="prop_type_summary"></span><dl> <dt>**RESUMO DO \_ TIPO \_ PROP**</dt> </dl>                                  | Resumindo o tipo de propriedade. Indica a primeira instância de propriedade anexada pelo analisador a um quadro. PROP \_ TYPE SUMMARY pode servir como um espaço reservado para grupos de \_ propriedades. Esse valor indica que a propriedade não está definida no *protocolo RFC.*<br/> |
| <span id="PROP_TYPE_BYTE"></span><span id="prop_type_byte"></span><dl> <dt>**BYTE \_ DE TIPO \_ PROP**</dt> </dl>                                           | Dados numéricos com um tamanho de um byte (entidade de 8 bits).<br/>                                                                                                                                                                                                                                             |
| <span id="PROP_TYPE_WORD"></span><span id="prop_type_word"></span><dl> <dt>**PALAVRA DE \_ TIPO \_ PROP**</dt> </dl>                                           | Dados numéricos com um tamanho de dois bytes (entidade de 16 bits).<br/>                                                                                                                                                                                                                                           |
| <span id="PROP_TYPE_DWORD"></span><span id="prop_type_dword"></span><dl> <dt>**PROP \_ TYPE \_ DWORD**</dt> </dl>                                        | Dados numéricos com um tamanho de quatro bytes (entidade de 32 bits).<br/>                                                                                                                                                                                                                                          |
| <span id="PROP_TYPE_LARGEINT"></span><span id="prop_type_largeint"></span><dl> <dt>**TIPO PROP \_ \_ LARGEINT**</dt> </dl>                               | Dados numéricos com um tamanho de oito bytes (entidade de 64 bits).<br/>                                                                                                                                                                                                                                         |
| <span id="PROP_TYPE_ADDR"></span><span id="prop_type_addr"></span><dl> <dt>**ADDR \_ DE \_ TIPO PROP**</dt> </dl>                                           | Endereço MAC (entidade de 6 byte).<br/>                                                                                                                                                                                                                                                                     |
| <span id="PROP_TYPE_TIME"></span><span id="prop_type_time"></span><dl> <dt>**HORA DO \_ TIPO \_ PROP**</dt> </dl>                                           | **Estrutura SYSTEMTIME.**<br/>                                                                                                                                                                                                                                                                        |
| <span id="PROP_TYPE_STRING"></span><span id="prop_type_string"></span><dl> <dt>**CADEIA DE \_ CARACTERES DE TIPO \_ PROP**</dt> </dl>                                     | Dados de texto ASCII. Esse tipo de dados não é terminado em NULL. <br/> Para dados Unicode, quando dados de texto ASCII são especificados, o sinalizador UNICODE IFLAG também deve ser definido quando a função de instância de propriedade attach \_ é chamada.<br/>                                                                          |
| <span id="PROP_TYPE_IP_ADDRESS"></span><span id="prop_type_ip_address"></span><dl> <dt>**ENDEREÇO \_ IP DO TIPO \_ \_ PROP**</dt> </dl>                        | Endereço IP. (entidade de 4 byte).<br/>                                                                                                                                                                                                                                                                     |
| <span id="PROP_TYPE_IPX_ADDRESS"></span><span id="prop_type_ipx_address"></span><dl> <dt>**ENDEREÇO \_ \_ IPX DO TIPO \_ PROP**</dt> </dl>                     | Endereço IPX. (entidade de 10 byte).<br/>                                                                                                                                                                                                                                                                   |
| <span id="PROP_TYPE_BYTESWAPPED_WORD"></span><span id="prop_type_byteswapped_word"></span><dl> <dt>**PROP \_ TYPE \_ BYTESWAPPED \_ WORD**</dt> </dl>      | Obsoleto. Para dados WORD trocados por byte, defina **DataType** como PROP TYPE WORD e defina o sinalizador IFLAG SWAPPED ao chamar uma função de instância \_ \_ de propriedade \_ Attach. <br/>                                                                                                                                |
| <span id="PROP_TYPE_BYTESWAPPED_DWORD"></span><span id="prop_type_byteswapped_dword"></span><dl> <dt>**PROP \_ TYPE \_ BYTESWAPPED \_ DWORD**</dt> </dl>   | Obsoleto. Para dados DWORD trocados por byte, defina **DataType** como PROP TYPE DWORD e defina o sinalizador IFLAG SWAPPED ao chamar uma função de instância \_ \_ de propriedade \_ Attach. <br/>                                                                                                                              |
| <span id="PROP_TYPE_TYPED_STRING"></span><span id="prop_type_typed_string"></span><dl> <dt>**CADEIA DE \_ CARACTERES \_ DIGITADA DO TIPO \_ PROP**</dt> </dl>                  | Obsoleto. Para dados de cadeia de caracteres de tipo variável, defina **DataType** como PROP TYPE STRING e defina o sinalizador UNICODE IFLAG ao chamar uma função de instância \_ \_ de propriedade \_ **Attach.**<br/>                                                                                                                           |
| <span id="PROP_TYPE_RAW_DATA"></span><span id="prop_type_raw_data"></span><dl> <dt>**DADOS \_ BRUTOS \_ DO TIPO \_ PROP**</dt> </dl>                              | Dados brutos de comprimento e formato desconhecidos.<br/>                                                                                                                                                                                                                                                           |
| <span id="PROP_TYPE_COMMENT"></span><span id="prop_type_comment"></span><dl> <dt>**COMENTÁRIO \_ DE TIPO \_ PROP**</dt> </dl>                                  | O mesmo que PROP \_ TYPE \_ VOID.<br/>                                                                                                                                                                                                                                                                        |
| <span id="PROP_TYPE_SRCFRIENDLYNAME"></span><span id="prop_type_srcfriendlyname"></span><dl> <dt>**PROP \_ TYPE \_ SRCFRIENDLYNAME**</dt> </dl>          | Endereço do nome amigável de origem. Monitor de Rede fornece suporte de formatação integrado para esse tipo de dados.<br/>                                                                                                                                                                                |
| <span id="PROP_TYPE_DSTFRIENDLYNAME"></span><span id="prop_type_dstfriendlyname"></span><dl> <dt>**PROP \_ TYPE \_ DSTFRIENDLYNAME**</dt> </dl>          | Endereço do nome amigável de destino. Monitor de Rede fornece suporte de formatação integrado para esse tipo de dados.<br/>                                                                                                                                                                           |
| <span id="PROP_TYPE_TOKENRING_ADDRESS"></span><span id="prop_type_tokenring_address"></span><dl> <dt>**TIPO DE PROP \_ \_ TOKENRING \_ ADDRESS**</dt> </dl>   | Endereço de anel de token. Monitor de Rede fornece suporte de formatação integrado para esse tipo de dados.<br/>                                                                                                                                                                                             |
| <span id="PROP_TYPE_FDDI_ADDRESS"></span><span id="prop_type_fddi_address"></span><dl> <dt>**ENDEREÇO \_ \_ FDDI DO TIPO \_ PROP**</dt> </dl>                  | Endereço FDDI. Monitor de Rede fornece suporte de formatação integrado para esse tipo de dados.<br/>                                                                                                                                                                                                   |
| <span id="PROP_TYPE_ETHERNET_ADDRESS"></span><span id="prop_type_ethernet_address"></span><dl> <dt>**ENDEREÇO \_ ETHERNET DO TIPO \_ \_ PROP**</dt> </dl>      | Endereço Ethernet. Monitor de Rede fornece suporte de formatação integrado para esse tipo de dados.<br/>                                                                                                                                                                                               |
| <span id="PROP_TYPE_OBJECT_IDENTIFIER"></span><span id="prop_type_object_identifier"></span><dl> <dt>**IDENTIFICADOR \_ DE OBJETO DE TIPO \_ \_ PROP**</dt> </dl>   | Identificador de objeto SNMP codificado em BER.<br/>                                                                                                                                                                                                                                                              |
| <span id="PROP_TYPE_VINES_IP_ADDRESS"></span><span id="prop_type_vines_ip_address"></span><dl> <dt>**ENDEREÇO IP \_ \_ DE VINES DO TIPO \_ \_ PROP**</dt> </dl>     | Endereço IP do Vines (entidade de 6 byte).<br/>                                                                                                                                                                                                                                                                |
| <span id="PROP_TYPE_VAR_LEN_SMALL_INT"></span><span id="prop_type_var_len_small_int"></span><dl> <dt>**PROP \_ TYPE \_ VAR \_ LEN \_ SMALL \_ INT**</dt> </dl> | Valor numérico sem um comprimento pré-determinado, mas não mais de 8 bytes de comprimento. O comprimento dos dados anexados determina o comprimento do valor.<br/>                                                                                                                                                |



 

</dd> <dt>

**DataQualifier**
</dt> <dd>

O qualificador de dados de uma propriedade. Esse membro fornece informações precisas sobre o tipo de dados.

**DataQualifier** pode ter um dos valores a seguir.



| Valor                                                                                                                                                                                                  | Significado                                                                                                                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PROP_QUAL_NONE"></span><span id="prop_qual_none"></span><dl> <dt>**PROP \_ QUAL \_ NONE**</dt> </dl>                                      | O tipo de dados de propriedade é a única especificação da propriedade. <br/> Quando esse valor é definido, o membro de união da estrutura é definido como **NULL** e, em seguida, ignorado.<br/>                                                                                                                                        |
| <span id="PROP_QUAL_RANGE"></span><span id="prop_qual_range"></span><dl> <dt>**INTERVALO DE \_ QUAL \_ PROP**</dt> </dl>                                   | Espera-se que o valor numérico está dentro de um determinado intervalo. Defina o intervalo no **membro lpRange.**<br/>                                                                                                                                                                                                                |
| <span id="PROP_QUAL_SET"></span><span id="prop_qual_set"></span><dl> <dt>**PROP \_ QUAL \_ SET**</dt> </dl>                                         | O valor de uma propriedade é comparado a um conjunto de valores que são especificados no membro **lpSet** da União da estrutura. O valor de uma propriedade pode ser um **byte**, **Word**, **DWORD**, **LARGEINT** ou **time**.<br/>                                                                                                |
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

 

