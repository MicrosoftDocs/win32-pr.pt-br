---
description: Representa uma entrada na lista de atributos.
ms.assetid: daa0c97d-2ebe-4e14-b1f8-e4be3075b13e
title: ATTRIBUTE_LIST_ENTRY estrutura
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ATTRIBUTE_LIST_ENTRY
api_type:
- NA
api_location: ''
ms.openlocfilehash: 0c0154de52dbefa6d29278ca05e924db6f6c1d84b124fe21b3092e728a0d07fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956135"
---
# <a name="attribute_list_entry-structure"></a>Estrutura ATTRIBUTE \_ LIST \_ ENTRY

\[Essa estrutura é válida somente para a versão 3 dos volumes NTFS; ele pode ser alterado em versões futuras.\]

Representa uma entrada na lista de atributos.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _ATTRIBUTE_LIST_ENTRY {
  ATTRIBUTE_TYPE_CODE   AttributeTypeCode;
  USHORT                RecordLength;
  UCHAR                 AttributeNameLength;
  UCHAR                 AttributeNameOffset;
  VCN                   LowestVcn;
  MFT_SEGMENT_REFERENCE SegmentReference;
  USHORT                Reserved;
  WCHAR                 AttributeName[1];
} ATTRIBUTE_LIST_ENTRY, *PATTRIBUTE_LIST_ENTRY;
```



## <a name="members"></a>Membros

<dl> <dt>

**AttributeTypeCode**
</dt> <dd>

O código de tipo de atributo.



| Valor                                                                                                                                                                                                                                           | Significado                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="_STANDARD_INFORMATION"></span><span id="_standard_information"></span><dl> <dt>**$STANDARD \_ Informações**</dt> <dt>0x10</dt> </dl> | Atributos de arquivo (como somente leitura e arquivo morto), carimbos de data/hora (como criação de arquivo e última modificação) e a contagem de link rígido.<br/> |
| <span id="_ATTRIBUTE_LIST"></span><span id="_attribute_list"></span><dl> <dt>**$ATTRIBUTE \_ LIST**</dt> <dt>0x20</dt> </dl>                   | Uma lista de atributos que comem o arquivo e a referência de arquivo do registro de arquivo MFT no qual cada atributo está localizado.<br/>     |
| <span id="_FILE_NAME"></span><span id="_file_name"></span><dl> <dt>**$FILE \_ NOME**</dt> <dt>0x30</dt> </dl>                                  | O nome do arquivo, em caracteres Unicode.<br/>                                                                                     |
| <span id="_OBJECT_ID"></span><span id="_object_id"></span><dl> <dt>**$OBJECT \_ ID**</dt> <dt>0x40</dt> </dl>                                  | Um identificador de objeto de 16 byte atribuído pelo serviço de acompanhamento de link.<br/>                                                              |
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

O tamanho dessa estrutura, além do buffer de nome opcional, em bytes.

</dd> <dt>

**AttributeNameLength**
</dt> <dd>

O tamanho do nome do atributo opcional, em caracteres. Se existir um nome, esse valor será diferente de zero e a estrutura será seguida imediatamente por uma cadeia de caracteres Unicode do número especificado de caracteres.

</dd> <dt>

**AttributeNameOffset**
</dt> <dd>

Reservado.

</dd> <dt>

**LowestVcn**
</dt> <dd>

O vcn (número de cluster virtual) mais baixo para esse atributo. Esse membro é zero, a menos que o atributo exija vários segmentos de registro de arquivo e, a menos que essa entrada seja uma referência a um segmento diferente do primeiro. Nesse caso, esse valor é o VCN mais baixo descrito pelo segmento referenciado.

</dd> <dt>

**SegmentReference**
</dt> <dd>

O segmento MFT (tabela de arquivos mestre) no qual o atributo reside. Consulte [**REFERÊNCIA DE SEGMENTO \_ MFT \_**](mft-segment-reference.md).

</dd> <dt>

**Reserved**
</dt> <dd>

Reservado.

</dd> <dt>

**AttributeName**
</dt> <dd>

O início do nome do atributo opcional.

</dd> </dl>

## <a name="remarks"></a>Comentários

A lista de atributos é uma lista ordenada de estruturas **ATTRIBUTE \_ LIST \_ ENTRY** alinhadas a quadword. Essa lista é ordenada primeiro pelo código de tipo de atributo e, em seguida, pelo nome do atributo (se presente). Nenhum dois atributos podem ter o mesmo código de tipo, nome e VCN mais baixo. Portanto, pode haver no máximo um atributo para cada código de tipo sem um nome.

Essa definição de estrutura é válida somente para a versão principal 3 e a versão secundária 0 ou 1, conforme relatado por [**FSCTL \_ GET \_ NTFS \_ VOLUME \_ DATA**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).

Observe que não há nenhum arquivo de header associado para essa estrutura.

## <a name="see-also"></a>Confira também

<dl> <dt>

[Tabela de arquivos mestre](master-file-table.md)
</dt> </dl>

 

 
