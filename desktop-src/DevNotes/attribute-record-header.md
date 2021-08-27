---
description: Representa um registro de atributo.
ms.assetid: f9d9458c-b179-441c-9f62-ff0ac2f75329
title: ATTRIBUTE_RECORD_HEADER estrutura
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ATTRIBUTE_RECORD_HEADER
api_type:
- NA
api_location: ''
ms.openlocfilehash: 9664af36448bb125dc8d5fde3c4d22b04e58b1ca341acad561b94708acbf143c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120045377"
---
# <a name="attribute_record_header-structure"></a>Estrutura DE \_ \_ HEADER DE REGISTRO DE ATRIBUTO

\[Essa estrutura é válida somente para a versão 3 dos volumes NTFS; ele pode ser alterado em versões futuras.\]

Representa um registro de atributo.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _ATTRIBUTE_RECORD_HEADER {
  ATTRIBUTE_TYPE_CODE TypeCode;
  ULONG               RecordLength;
  UCHAR               FormCode;
  UCHAR               NameLength;
  USHORT              NameOffset;
  USHORT              Flags;
  USHORT              Instance;
  union {
    struct {
      ULONG  ValueLength;
      USHORT ValueOffset;
      UCHAR  Reserved[2];
    } Resident;
    struct {
      VCN      LowestVcn;
      VCN      HighestVcn;
      USHORT   MappingPairsOffset;
      UCHAR    Reserved[6];
      LONGLONG AllocatedLength;
      LONGLONG FileSize;
      LONGLONG ValidDataLength;
      LONGLONG TotalAllocated;
    } Nonresident;
  } Form;
} ATTRIBUTE_RECORD_HEADER, *PATTRIBUTE_RECORD_HEADER;
```



## <a name="members"></a>Membros

<dl> <dt>

**TypeCode**
</dt> <dd>

O código de tipo de atributo.



| Valor                                                                                                                                                                                                                                           | Significado                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="_STANDARD_INFORMATION"></span><span id="_standard_information"></span><dl> <dt>**$STANDARD \_ Informações**</dt> <dt>0x10</dt> </dl> | Atributos de arquivo (como somente leitura e arquivo morto), carimbos de data/hora (como criação de arquivo e última modificação) e a contagem de link rígido.<br/> |
| <span id="_ATTRIBUTE_LIST"></span><span id="_attribute_list"></span><dl> <dt>**$ATTRIBUTE \_ LIST**</dt> <dt>0x20</dt> </dl>                   | Uma lista de atributos que comem o arquivo e a referência de arquivo do registro de arquivo MFT no qual cada atributo está localizado.<br/>     |
| <span id="_FILE_NAME"></span><span id="_file_name"></span><dl> <dt>**$FILE \_ NOME**</dt> <dt>0x30</dt> </dl>                                  | O nome do arquivo, em caracteres Unicode.<br/>                                                                                     |
| <span id="_OBJECT_ID"></span><span id="_object_id"></span><dl> <dt>**$OBJECT \_ ID**</dt> <dt>0x40</dt> </dl>                                  | Um identificador de objeto de 64 byte atribuído pelo serviço de acompanhamento de link.<br/>                                                              |
| <span id="_VOLUME_NAME"></span><span id="_volume_name"></span><dl> <dt>**$VOLUME \_ NOME**</dt> <dt>0x60</dt> </dl>                            | Rótulo do volume. Presente no arquivo $Volume.<br/>                                                                                   |
| <span id="_VOLUME_INFORMATION"></span><span id="_volume_information"></span><dl> <dt>**$VOLUME \_ Informações**</dt> <dt>0x70</dt> </dl>       | As informações de volume. Presente no arquivo $Volume.<br/>                                                                             |
| <span id="_DATA"></span><span id="_data"></span><dl> <dt>**$DATA**</dt> <dt>0x80</dt> </dl>                                                  | O conteúdo do arquivo.<br/>                                                                                                        |
| <span id="_INDEX_ROOT"></span><span id="_index_root"></span><dl> <dt>**$INDEX \_ Root**</dt> <dt>0x90</dt> </dl>                               | Usado para implementar a alocação de nome de arquivo para diretórios grandes.<br/>                                                                     |
| <span id="_INDEX_ALLOCATION"></span><span id="_index_allocation"></span><dl> <dt>**$INDEX \_ ALOCAÇÃO**</dt> <dt>0xA0</dt> </dl>             | Usado para implementar a alocação de nome de arquivo para diretórios grandes.<br/>                                                                     |
| <span id="_BITMAP"></span><span id="_bitmap"></span><dl> <dt>**$BITMAP**</dt> <dt>0xB0</dt> </dl>                                            | Um índice de bitmap para um diretório grande.<br/>                                                                                            |
| <span id="_REPARSE_POINT"></span><span id="_reparse_point"></span><dl> <dt>**$REPARSE \_ PONTO**</dt> <dt>0xC0</dt> </dl>                      | Os dados de ponto de análise.<br/>                                                                                                          |



 

</dd> <dt>

**Recordlength**
</dt> <dd>

O tamanho do registro de atributo, em bytes. Esse valor reflete o tamanho necessário para a variante de registro e é sempre arredondado para o limite quadword mais próximo.

</dd> <dt>

**FormCode**
</dt> <dd>

O código do formulário de atributo.



| Valor                                                                                                                                                                                                                            | Significado                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span id="RESIDENT_FORM"></span><span id="resident_form"></span><dl> <dt>**RESIDENTE \_ FORMULÁRIO**</dt> <dt>0x00</dt> </dl>          | O valor está contido no registro de arquivo e segue imediatamente o header do registro de atributo.<br/> |
| <span id="NONRESIDENT_FORM"></span><span id="nonresident_form"></span><dl> <dt>**NONRESIDENT \_ FORMULÁRIO**</dt> <dt>0x01</dt> </dl> | O valor está contido em outros setores no disco.<br/>                                           |



 

</dd> <dt>

**NameLength**
</dt> <dd>

O tamanho do nome do atributo opcional, em caracteres ou 0 se não houver nenhum nome de atributo. O comprimento máximo do nome do atributo é de 255 caracteres.

</dd> <dt>

**NameOffset**
</dt> <dd>

O deslocamento do nome do atributo do início do registro de atributo, em bytes. Se o **membro NameLength** for 0, esse membro será indefinido.

</dd> <dt>

**Sinalizadores**
</dt> <dd>

Os sinalizadores de atributo.

<dl> <dt>

<span id="ATTRIBUTE_FLAG_COMPRESSION_MASK"></span><span id="attribute_flag_compression_mask"></span>**ATRIBUTO \_ MÁSCARA \_ DE \_ COMPACTAÇÃO DE** SINALIZADOR (0x00FF)
</dt> <dt>

<span id="ATTRIBUTE_FLAG_SPARSE"></span><span id="attribute_flag_sparse"></span>**ATRIBUTO \_ FLAG \_ SPARSE** (0x8000)
</dt> <dt>

<span id="ATTRIBUTE_FLAG_ENCRYPTED"></span><span id="attribute_flag_encrypted"></span>**ATRIBUTO \_ FLAG \_ ENCRYPTED** (0x4000)
</dt> </dl> </dd> <dt>

**Instância**
</dt> <dd>

A instância exclusiva para esse atributo no registro de arquivo.

</dd> <dt>

**Formulário**
</dt> <dd>

Se o **membro FormCode** for RESIDENT \_ FORM, a união será uma **estrutura Residente.** Se **FormCode** for NONRESIDENT \_ FORM, a união será **uma estrutura Nonresident.**

<dl> <dt>

**Residente**
</dt> <dd> <dl> <dt>

**ValueLength**
</dt> <dd>

O tamanho do valor do atributo, em bytes.

</dd> <dt>

**ValueOffset**
</dt> <dd>

O deslocamento para o valor do início do registro de atributo, em bytes.

</dd> <dt>

**Reserved**
</dt> <dd>

Reservado.

</dd> </dl> </dd> <dt>

**Não identificador**
</dt> <dd> <dl> <dt>

**LowestVcn**
</dt> <dd>

O vcn (número de cluster virtual) mais baixo coberto por esse registro de atributo.

</dd> <dt>

**HighestVcn**
</dt> <dd>

O VCN mais alto coberto por esse registro de atributo.

</dd> <dt>

**MappingPairsOffset**
</dt> <dd>

O deslocamento para a matriz de pares de mapeamento do início do registro de atributo, em bytes. Para obter mais informações, consulte Comentários.

</dd> <dt>

**Reserved**
</dt> <dd>

Reservado.

</dd> <dt>

**AllocatedLength**
</dt> <dd>

O tamanho alocado do arquivo, em bytes. Esse valor é um múltiplo do tamanho do cluster. Esse membro não será válido se **o membro LowestVcn** for não zero.

</dd> <dt>

**FileSize**
</dt> <dd>

O tamanho do arquivo (byte mais alto que pode ser lido mais 1), em bytes. Esse membro não será válido se **LowestVcn** for não zero.

</dd> <dt>

**ValidDataLength**
</dt> <dd>

O comprimento de dados válido (byte inicializado mais 1), em bytes. Esse valor é arredondado para o limite de cluster mais próximo. Esse membro não será válido se **LowestVcn** for não zero.

</dd> <dt>

**TotalAllocated**
</dt> <dd>

O total alocado para o arquivo (a soma dos clusters alocados).

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="remarks"></a>Comentários

Observe que não há nenhum arquivo de header associado para essa estrutura.

Essa definição de estrutura é válida somente para a versão principal 3 e a versão secundária 0 ou 1, conforme relatado por [**FSCTL \_ GET \_ NTFS \_ VOLUME \_ DATA**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).

Os registros de atributo são sempre alinhados em um limite quadword.

Se o atributo não for identificador, o header do registro de atributo conterá uma lista de informações de recuperação que fornece um mapeamento entre VCN e LCN (número de cluster lógico) para o atributo. Se as informações de recuperação não se ajustarem no segmento de arquivo base, poderão ser armazenadas em um segmento de registro de arquivo externo por conta própria. Se ele ainda não se ajustar a um segmento de registro de arquivo externo, haverá um provisionamento na lista de atributos para conter várias entradas para um atributo que requer informações de recuperação adicionais.

A matriz de pares de mapeamento é armazenada em um formato compactado e pressupo que as informações são descompactadas e armazenadas em cache pelo sistema. Ele consiste em uma série de pares NextVcn/CurrentLcn. Por exemplo, se um arquivo tiver uma única sequência de 8 clusters começando em LCN 128 e o arquivo for iniciado em LowestVcn 0, a matriz de pares de mapeamento terá apenas uma entrada, que é NextVcn=8 e CurrentLcn=128. A matriz é um fluxo de byte que armazena as alterações nas variáveis de trabalho quando processadas sequencialmente. O fluxo de byte deve ser interpretado como um fluxo terminado em zero de triplos, da seguinte maneira:

count byte = *v* + (*l* \* 16)

em *que v* é o número de bytes VCN de ordem baixa alterados e *l* é o número de bytes LCN de ordem baixa alterados.

O algoritmo de descompactação é o seguinte:

1.  Inicialize NextVcn como `Attribute->LowestVcn` e CurrentLcn como 0.
2.  Inicialize o ponteiro de fluxo de byte para `(PCHAR)Attribute + Attribute->AttributeForm->Nonresident->MappingPairsOffset` .
3.  De definir CurrentVcn como NextVcn.
4.  Leia o próximo byte do fluxo. Se for 0, então, quebre; else extract *v* and *l* conforme descrito anteriormente.
5.  Interprete os *próximos* bytes v como uma quantidade assinada, com o byte de ordem baixa primeiro. Desempacotar o sinal estendido em 64 bits e adicioná-lo ao NextVcn.
6.  Interprete os *próximos* bytes l como uma quantidade assinada, com o byte de ordem baixa primeiro. Desempacotar o sinal estendido em 64 bits e adicioná-lo ao CurrentLcn. Se isso produzir um CurrentLcn de 0, os VCNs de CurrentVcn para NextVcn–1 não serão alocados.
7.  Atualize as informações de mapeamento armazenadas em cache de CurrentVcn, NextVcn e CurrentLcn.
8.  Vá para a etapa 3.

## <a name="see-also"></a>Confira também

<dl> <dt>

[Tabela de arquivos mestre](master-file-table.md)
</dt> </dl>

 

 
