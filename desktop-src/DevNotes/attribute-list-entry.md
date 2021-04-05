---
description: Representa uma entrada na lista de atributos.
ms.assetid: daa0c97d-2ebe-4e14-b1f8-e4be3075b13e
title: Estrutura de ATTRIBUTE_LIST_ENTRY
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
ms.openlocfilehash: 67ee65a22c9e880c76d3b250c4859077f471b018
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826130"
---
# <a name="attribute_list_entry-structure"></a>Estrutura de entrada da \_ lista de atributos \_

\[Essa estrutura é válida somente para a versão 3 de volumes NTFS; Ele pode ser alterado em versões futuras.\]

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

O código do tipo de atributo.



| Valor                                                                                                                                                                                                                                           | Significado                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="_STANDARD_INFORMATION"></span><span id="_standard_information"></span><dl> <dt>**$Standard \_ INFORMAÇÕES**</dt> <dt>0x10</dt> </dl> | Atributos de arquivo (como somente leitura e arquivo), carimbos de data/hora (como criação de arquivo e última modificação) e a contagem de vínculos físicos.<br/> |
| <span id="_ATTRIBUTE_LIST"></span><span id="_attribute_list"></span><dl> <dt>**$Attribute \_ LISTA**</dt> <dt>0x20</dt> </dl>                   | Uma lista de atributos que compõem o arquivo e a referência de arquivo do registro de arquivo MFT no qual cada atributo está localizado.<br/>     |
| <span id="_FILE_NAME"></span><span id="_file_name"></span><dl> <dt>**$File \_ NOME**</dt> <dt>0x30</dt> </dl>                                  | O nome do arquivo, em caracteres Unicode.<br/>                                                                                     |
| <span id="_OBJECT_ID"></span><span id="_object_id"></span><dl> <dt>**$Object \_ ID**</dt> <dt>0x40</dt> </dl>                                  | Um identificador de objeto de 16 bytes atribuído pelo serviço de rastreamento de link.<br/>                                                              |
| <span id="_VOLUME_NAME"></span><span id="_volume_name"></span><dl> <dt>**$Volume \_ NOME**</dt> <dt>0x60</dt> </dl>                            | Rótulo do volume. Presente no arquivo de $Volume.<br/>                                                                                   |
| <span id="_VOLUME_INFORMATION"></span><span id="_volume_information"></span><dl> <dt>**$Volume \_**</dt> <dt>0X70</dt> de informações </dl>       | As informações de volume. Presente no arquivo de $Volume.<br/>                                                                             |
| <span id="_DATA"></span><span id="_data"></span><dl> <dt>**$Data**</dt> <dt>0x80</dt> </dl>                                                  | O conteúdo do arquivo.<br/>                                                                                                        |
| <span id="_INDEX_ROOT"></span><span id="_index_root"></span><dl> <dt>**$Index \_**</dt> <dt>0x90</dt> raiz </dl>                               | Usado para implementar a alocação de nome de arquivo para diretórios grandes.<br/>                                                                     |
| <span id="_INDEX_ALLOCATION"></span><span id="_index_allocation"></span><dl> <dt>**$Index \_**</dt> <dt>0XA0</dt> de alocação </dl>             | Usado para implementar a alocação de nome de arquivo para diretórios grandes.<br/>                                                                     |
| <span id="_BITMAP"></span><span id="_bitmap"></span><dl> <dt>**$Bitmap**</dt> <dt>0xb0</dt> </dl>                                            | Um índice de bitmap para um diretório grande.<br/>                                                                                            |
| <span id="_REPARSE_POINT"></span><span id="_reparse_point"></span><dl> <dt>**$REPARSE \_**</dt> <dt>0XC0</dt> do ponto </dl>                      | Os dados do ponto de nova análise.<br/>                                                                                                          |



 

</dd> <dt>

**RecordLength**
</dt> <dd>

O tamanho dessa estrutura, mais o buffer de nome opcional, em bytes.

</dd> <dt>

**AttributeNameLength**
</dt> <dd>

O tamanho do nome do atributo opcional, em caracteres. Se existir um nome, esse valor será diferente de zero e a estrutura será seguida imediatamente por uma cadeia de caracteres Unicode do número especificado.

</dd> <dt>

**AttributeNameOffset**
</dt> <dd>

Reservado.

</dd> <dt>

**LowestVcn**
</dt> <dd>

O VCN (número de cluster virtual) mais baixo para este atributo. Esse membro é zero, a menos que o atributo exija vários segmentos de registro de arquivo e, a menos que essa entrada seja uma referência a um segmento diferente do primeiro. Nesse caso, esse valor é o VCN mais baixo que é descrito pelo segmento referenciado.

</dd> <dt>

**SegmentReference**
</dt> <dd>

O segmento de tabela de arquivos mestre (MFT) no qual o atributo reside. Consulte [**\_ \_ referência de segmento de MFT**](mft-segment-reference.md).

</dd> <dt>

**Reserved**
</dt> <dd>

Reservado.

</dd> <dt>

**AttributeName**
</dt> <dd>

O início do nome de atributo opcional.

</dd> </dl>

## <a name="remarks"></a>Comentários

A lista de atributos é uma lista ordenada de estruturas de **\_ \_ entrada de lista de atributos** alinhados por quadword. Essa lista é ordenada primeiro pelo código de tipo de atributo e, em seguida, pelo nome do atributo (se presente). Dois atributos não podem ter o mesmo código de tipo, nome e VCN mais baixo. Portanto, pode haver no máximo um atributo para cada código de tipo sem um nome.

Essa definição de estrutura é válida somente para a versão principal 3 e secundária 0 ou 1, conforme relatado [**pelo \_ fsctl \_ obter \_ \_ dados de volume NTFS**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).

Observe que não há nenhum arquivo de cabeçalho associado para essa estrutura.

## <a name="see-also"></a>Confira também

<dl> <dt>

[Tabela de arquivos mestre](master-file-table.md)
</dt> </dl>

 

 
