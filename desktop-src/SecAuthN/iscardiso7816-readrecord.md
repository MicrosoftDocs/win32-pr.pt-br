---
description: O método ReadRecord constrói um comando APDU (unidade de dados de protocolo de aplicativo) que lê o conteúdo dos registros especificados ou a parte inicial de um registro de um arquivo elementar.
ms.assetid: b00a3242-93bc-4779-8c62-89157fbcb5d1
title: 'Método ISCardISO7816:: ReadRecord (Scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.ReadRecord
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 0cb9697315a6f9dd2436cd7a64d54fa6b44e00f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010984"
---
# <a name="iscardiso7816readrecord-method"></a>Método ISCardISO7816:: ReadRecord

\[O método **ReadRecord** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional. Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]

O método **ReadRecord** constrói um comando APDU ( [*unidade de dados de protocolo de aplicativo*](../secgloss/a-gly.md) ) que lê o conteúdo dos registros especificados ou a parte inicial de um registro de um arquivo elementar.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ReadRecord(
  [in]      BYTE       byRecordId,
  [in]      BYTE       byRefCtrl,
  [in]      LONG       lBytesToRead,
  [in, out] LPSCARDCMD *ppCmd
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*byRecordId* \[ no\]
</dt> <dd>

Registro o número ou a ID do primeiro registro a ser lido (00 indica o registro atual).

</dd> <dt>

*byRefCtrl* \[ no\]
</dt> <dd>

Codificação do controle de referência.



| Valor                                                                                                                                                                                | Significado                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Current_EF"></span><span id="current_ef"></span><span id="CURRENT_EF"></span><dl> <dt>**EF atual**</dt> </dl>     | Posição do bit: 00000---<br/> EF selecionado no momento.<br/>                    |
| <span id="Short_EF_ID"></span><span id="short_ef_id"></span><span id="SHORT_EF_ID"></span><dl> <dt>**ID curta do EF**</dt> </dl> | Posição do bit: xxxxx---<br/> Identificador curto do EF.<br/>                      |
| <span id="RFU"></span><span id="rfu"></span><dl> <dt>**RFU**</dt> </dl>                                                       | Posição do bit: 11111---<br/>                                                      |
| <span id="Record__"></span><span id="record__"></span><span id="RECORD__"></span><dl> <dt>**Gravável \#**</dt> </dl>            | Posição do bit:-----1xx<br/> Uso do número de registro em P1.<br/>             |
| <span id="Read_Record"></span><span id="read_record"></span><span id="READ_RECORD"></span><dl> <dt>**Ler registro**</dt> </dl> | Posição do bit:-----100<br/> Leia o registro P1.<br/>                           |
| <span id="Up_to_Last"></span><span id="up_to_last"></span><span id="UP_TO_LAST"></span><dl> <dt>**Até o último**</dt> </dl>     | Posição do bit:-----101<br/> Leia todos os registros de P1 até o último. <br/> |
| <span id="Up_to_P1"></span><span id="up_to_p1"></span><span id="UP_TO_P1"></span><dl> <dt>**Até P1**</dt> </dl>             | Posição do bit:-----110<br/> Leia todos os registros do último até P1. <br/> |
| <span id="RFU"></span><span id="rfu"></span><dl> <dt>**RFU**</dt> </dl>                                                       | Posição do bit:-----111<br/>                                                      |
| <span id="Record_ID"></span><span id="record_id"></span><span id="RECORD_ID"></span><dl> <dt>**ID do Registro**</dt> </dl>         | Posição do bit:-----0XX<br/> Uso do número de registro em P1.<br/>             |
| <span id="First_Occur"></span><span id="first_occur"></span><span id="FIRST_OCCUR"></span><dl> <dt>**Primeira ocorrência**</dt> </dl> | Posição do bit:-----000<br/> Leia a primeira ocorrência. <br/>                   |
| <span id="Last_Occur"></span><span id="last_occur"></span><span id="LAST_OCCUR"></span><dl> <dt>**Última ocorrência**</dt> </dl>     | Posição do bit:-----001<br/> Leia a última ocorrência. <br/>                    |
| <span id="Next_Occur"></span><span id="next_occur"></span><span id="NEXT_OCCUR"></span><dl> <dt>**Na próxima ocorrência**</dt> </dl>     | Posição do bit:-----010<br/> Leia a próxima ocorrência. <br/>                    |
| <span id="Previous"></span><span id="previous"></span><span id="PREVIOUS"></span><dl> <dt>**Anterior**</dt> </dl>             | Posição do bit:-----011<br/> Ler ocorrência anterior. <br/>                |
| <span id="Secret"></span><span id="secret"></span><span id="SECRET"></span><dl> <dt>**RADIUS**</dt> </dl>                     | Posição do bit:---xxxxx<br/>                                                      |



 

</dd> <dt>

*lBytesToRead* \[ no\]
</dt> <dd>

Número de bytes a serem lidos do EF transparente.

Se o campo Le contiver apenas zeros, dependendo de b3b2b1 de P2 e dentro do limite de 256 para comprimento curto ou 65536 para comprimento estendido, o comando deverá ler completamente o único registro solicitado ou a sequência de registros solicitada.

</dd> <dt>

*ppCmd* \[ entrada, saída\]
</dt> <dd>

Na entrada, um ponteiro para um objeto de interface [**ISCardCmd**](iscardcmd.md) ou **nulo**.

No retorno, ele é preenchido com o comando APDU construído por essa operação. Se *ppCmd* foi definido como **NULL**, um objeto [**ISCardCmd**](iscardcmd.md) de [*cartão inteligente*](../secgloss/s-gly.md) será criado internamente e retornado por meio do ponteiro *ppCmd* .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O método retorna um dos seguintes valores possíveis.



| Código de retorno                                                                                   | Description                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operação concluída com sucesso.<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Parâmetro inválido.<br/>                |
| <dl> <dt>**\_ponteiro E**</dt> </dl>     | Um ponteiro inadequado foi passado.<br/>      |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Sem memória.<br/>                    |



 

## <a name="remarks"></a>Comentários

O comando encapsulado só poderá ser executado se o status de segurança do [*cartão inteligente*](../secgloss/s-gly.md) satisfizer os atributos de segurança do arquivo elementar que está sendo lido.

Se outro arquivo elementar estiver selecionado atualmente no momento da emissão desse comando, ele poderá ser processado sem a identificação do arquivo selecionado no momento.

Quando o comando contém um identificador elementar curto válido, ele define o arquivo como o arquivo elementar atual.

Os arquivos elementares sem uma estrutura de registro não podem ser lidos. O comando encapsulado aborta se aplicado a um arquivo elementar sem uma estrutura de registro.

Para obter uma lista de todos os métodos fornecidos por essa interface, consulte [**ISCardISO7816**](iscardiso7816.md).

Além dos códigos de erro COM listados acima, essa interface pode retornar um código de erro de cartão inteligente se uma função de cartão inteligente foi chamada para concluir a solicitação. Para obter mais informações, consulte [valores de retorno de cartão inteligente](authentication-return-values.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                             |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                    |
| Fim do suporte do cliente<br/>    | Windows XP<br/>                                                                   |
| Fim do suporte do servidor<br/>    | Windows Server 2003<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>Scardssp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Scardsrv. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCardISO7816 é definido como 53B6AA68-3F56-11D0-916B-00AA00C18068<br/>        |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**AppendRecord**](iscardiso7816-appendrecord.md)
</dt> <dt>

[**ISCardISO7816**](iscardiso7816.md)
</dt> <dt>

[**Atualizarregistro**](iscardiso7816-updaterecord.md)
</dt> <dt>

[**WriteRecord**](iscardiso7816-writerecord.md)
</dt> </dl>

 

 
