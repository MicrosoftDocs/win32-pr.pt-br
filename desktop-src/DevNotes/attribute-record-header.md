---
description: Representa um registro de atributo.
ms.assetid: f9d9458c-b179-441c-9f62-ff0ac2f75329
title: Estrutura de ATTRIBUTE_RECORD_HEADER
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
ms.openlocfilehash: ae710ca04f11cb70c1bad9b5e6fec25f8fb5e94f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826129"
---
# <a name="attribute_record_header-structure"></a>Estrutura de cabeçalho de \_ registro de atributo \_

\[Essa estrutura é válida somente para a versão 3 de volumes NTFS; Ele pode ser alterado em versões futuras.\]

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

O código do tipo de atributo.



| Valor                                                                                                                                                                                                                                           | Significado                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="_STANDARD_INFORMATION"></span><span id="_standard_information"></span><dl> <dt>**$Standard \_ INFORMAÇÕES**</dt> <dt>0x10</dt> </dl> | Atributos de arquivo (como somente leitura e arquivo), carimbos de data/hora (como criação de arquivo e última modificação) e a contagem de vínculos físicos.<br/> |
| <span id="_ATTRIBUTE_LIST"></span><span id="_attribute_list"></span><dl> <dt>**$Attribute \_ LISTA**</dt> <dt>0x20</dt> </dl>                   | Uma lista de atributos que compõem o arquivo e a referência de arquivo do registro de arquivo MFT no qual cada atributo está localizado.<br/>     |
| <span id="_FILE_NAME"></span><span id="_file_name"></span><dl> <dt>**$File \_ NOME**</dt> <dt>0x30</dt> </dl>                                  | O nome do arquivo, em caracteres Unicode.<br/>                                                                                     |
| <span id="_OBJECT_ID"></span><span id="_object_id"></span><dl> <dt>**$Object \_ ID**</dt> <dt>0x40</dt> </dl>                                  | Um identificador de objeto de 64 bytes atribuído pelo serviço de rastreamento de link.<br/>                                                              |
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

O tamanho do registro de atributo, em bytes. Esse valor reflete o tamanho necessário para a variante de registro e é sempre arredondado para o limite de quadword mais próximo.

</dd> <dt>

**FormCode**
</dt> <dd>

O código de formulário de atributo.



| Valor                                                                                                                                                                                                                            | Significado                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span id="RESIDENT_FORM"></span><span id="resident_form"></span><dl> <dt>**Residente \_ na FORMULÁRIO**</dt> <dt>0x00</dt> </dl>          | O valor está contido no registro de arquivo e imediatamente segue o cabeçalho de registro de atributo.<br/> |
| <span id="NONRESIDENT_FORM"></span><span id="nonresident_form"></span><dl> Não <dt>**residente \_ FORMULÁRIO**</dt> <dt>0x01</dt> </dl> | O valor está contido em outros setores no disco.<br/>                                           |



 

</dd> <dt>

**NameLength**
</dt> <dd>

O tamanho do nome de atributo opcional, em caracteres, ou 0 se não houver nenhum nome de atributo. O comprimento máximo do nome de atributo é de 255 caracteres.

</dd> <dt>

**NameOffset**
</dt> <dd>

O deslocamento do nome do atributo desde o início do registro de atributo, em bytes. Se o membro **NameLength** for 0, esse membro será indefinido.

</dd> <dt>

**Sinalizadores**
</dt> <dd>

Os sinalizadores de atributo.

<dl> <dt>

<span id="ATTRIBUTE_FLAG_COMPRESSION_MASK"></span><span id="attribute_flag_compression_mask"></span>**Atributo \_ \_ \_ Máscara de compactação de sinalizador** (0x00FF)
</dt> <dt>

<span id="ATTRIBUTE_FLAG_SPARSE"></span><span id="attribute_flag_sparse"></span>**Atributo \_ SINALIZAr \_ esparso** (0x8000)
</dt> <dt>

<span id="ATTRIBUTE_FLAG_ENCRYPTED"></span><span id="attribute_flag_encrypted"></span>**Atributo \_ SINALIZAr \_ criptografado** (0x4000)
</dt> </dl> </dd> <dt>

**Instância**
</dt> <dd>

A instância exclusiva para esse atributo no registro de arquivo.

</dd> <dt>

**Isolada**
</dt> <dd>

Se o membro **FormCode** for \_ um formulário residente, a União será uma estrutura **residente** . Se **FormCode** for \_ um formulário não residente, Union será uma estrutura não **residente** .

<dl> <dt>

**Ponteiro**
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

**Não residente**
</dt> <dd> <dl> <dt>

**LowestVcn**
</dt> <dd>

O número mais baixo do cluster virtual (VCN) coberto por este registro de atributo.

</dd> <dt>

**HighestVcn**
</dt> <dd>

O VCN mais alto coberto por este registro de atributo.

</dd> <dt>

**MappingPairsOffset**
</dt> <dd>

O deslocamento para a matriz de pares de mapeamento desde o início do registro de atributo, em bytes. Para obter mais informações, consulte Comentários.

</dd> <dt>

**Reserved**
</dt> <dd>

Reservado.

</dd> <dt>

**AllocatedLength**
</dt> <dd>

O tamanho alocado do arquivo, em bytes. Esse valor é um múltiplo par do tamanho do cluster. Esse membro não será válido se o membro **LowestVcn** for diferente de zero.

</dd> <dt>

**Tamanho**
</dt> <dd>

O tamanho do arquivo (byte mais alto que pode ser lido mais 1), em bytes. Esse membro não será válido se **LowestVcn** for diferente de zero.

</dd> <dt>

**ValidDataLength**
</dt> <dd>

O comprimento de dados válido (mais alto byte inicializado mais 1), em bytes. Esse valor é arredondado para o limite de cluster mais próximo. Esse membro não será válido se **LowestVcn** for diferente de zero.

</dd> <dt>

**TotalAllocated**
</dt> <dd>

O total alocado para o arquivo (a soma dos clusters alocados).

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="remarks"></a>Comentários

Observe que não há nenhum arquivo de cabeçalho associado para essa estrutura.

Essa definição de estrutura é válida somente para a versão principal 3 e secundária 0 ou 1, conforme relatado [**pelo \_ fsctl \_ obter \_ \_ dados de volume NTFS**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).

Os registros de atributo são sempre alinhados em um limite de quadword.

Se o atributo não for residente, o cabeçalho de registro de atributo conterá uma lista de informações de recuperação que fornece um mapeamento entre o VCN e o número de cluster lógico (LCN) para o atributo. Se as informações de recuperação não couberem no segmento de arquivo base, elas poderão ser armazenadas em um segmento de registro de arquivo externo por si só. Se ainda não couber em um segmento de registro de arquivo externo, há uma provisão na lista de atributos para conter várias entradas para um atributo que requer informações adicionais de recuperação.

A matriz de pares de mapeamento é armazenada em um formato compactado e pressupõe que as informações sejam descompactadas e armazenadas em cache pelo sistema. Ele consiste em uma série de pares NextVcn/CurrentLcn. Por exemplo, se um arquivo tiver uma única execução de 8 clusters começando no LCN 128 e o arquivo iniciar em LowestVcn 0, a matriz de pares de mapeamento terá apenas uma entrada, que é NextVcn = 8 e CurrentLcn = 128. A matriz é um fluxo de bytes que armazena as alterações nas variáveis de trabalho quando processadas sequencialmente. O fluxo de bytes deve ser interpretado como um fluxo de percurso de terminação zero, da seguinte maneira:

contagem byte = *v* + (*l* \* 16)

em que *v* é o número de bytes de VCN de ordem baixa alterados e *l* é o número de bytes de LCN de ordem baixa alterados.

O algoritmo de descompactação é o seguinte:

1.  Inicialize NextVcn `Attribute->LowestVcn` e CurrentLcn como 0.
2.  Inicialize o ponteiro de fluxo de bytes para `(PCHAR)Attribute + Attribute->AttributeForm->Nonresident->MappingPairsOffset` .
3.  Defina CurrentVcn como NextVcn.
4.  Leia o próximo byte do fluxo. Se for 0, interrompa; caso contrário, extraia o *v* e o *l* conforme descrito anteriormente.
5.  Interprete os próximos *v* bytes como uma quantidade assinada, com o byte de ordem inferior primeiro. Desembale o registro de ti estendido em 64 bits e adicione-o a NextVcn.
6.  Interprete os próximos *l* bytes como uma quantidade assinada, com o byte de ordem inferior primeiro. Desembale o registro de ti estendido em 64 bits e adicione-o a CurrentLcn. Se isso produzir um CurrentLcn de 0, o VCNs de CurrentVcn para NextVcn – 1 não será alocado.
7.  Atualize as informações de mapeamento em cache de CurrentVcn, NextVcn e CurrentLcn.
8.  Vá para a etapa 3.

## <a name="see-also"></a>Confira também

<dl> <dt>

[Tabela de arquivos mestre](master-file-table.md)
</dt> </dl>

 

 
